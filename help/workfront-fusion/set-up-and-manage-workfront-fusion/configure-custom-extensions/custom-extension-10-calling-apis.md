---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Chamada de APIs do Workfront e Fusion a partir de sua extensão
description: Chamada de APIs do Workfront e Fusion a partir de sua extensão
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1083
ht-degree: 0%

---


# Chamada de APIs do Workfront e Fusion a partir de sua extensão

>[!NOTE]
>
>Este artigo presume alguma familiaridade com ferramentas de desenvolvimento de software.

A referência de contexto do Fusion fornece o token IMS do usuário conectado, portanto, a próxima etapa natural é chamar as APIs do Workfront ou Fusion e mostrar os dados reais. Isso não é possível devido ao CORS. Este artigo mostra como contornar essa limitação usando uma ação de tempo de execução do App Builder como um proxy do lado do servidor e inclui um exemplo (o painel de assinaturas do evento).

## Por que uma chamada direta de navegador falha (CORS)

Sua interface visível é executada em um `<iframe>` veiculado pela CDN da Adobe (`https://<your-app>.adobeio-static.net`). Quando essa página faz `fetch(...)` a uma API do Workfront ou Fusion em uma origem **diferente**, o navegador impõe o CORS (Cross-Origin Resource Sharing, Compartilhamento de Recursos Entre Origens). A menos que a API retorne explicitamente `Access-Control-Allow-Origin` para a origem CDN, o navegador bloqueará a resposta. Essas APIs não incluem na lista de permissões origens de extensão arbitrárias, portanto, as chamadas diretas do convidado falham.

Para obter informações sobre o CORS, consulte [CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS).

## Chamar sua própria ação de tempo de execução sem o CORS

A correção para isso é chamar sua própria ação de tempo de execução sem o CORS.

Os aplicativos App Builder podem incluir ações de tempo de execução, que são pequenas funções sem servidor executadas no Adobe I/O Runtime no lado do servidor. As chamadas de servidor para servidor não estão sujeitas ao CORS do navegador. E como a ação faz parte do seu aplicativo, o convidado pode chamá-lo com um URL relativo, que tem a mesma origem e, portanto, não está bloqueado.

```
  Guest UI (browser, adobeio-static.net)
     │  fetch('/api/v1/web/<app>/wf-proxy?...')   ← relative = same-origin, no CORS
     ▼
  Your runtime action  (Adobe I/O Runtime, server-side)
     │  fetch('https://fusion.adobe.com/api/v3/...')  ← server-to-server, no CORS
     ▼
  Workfront / Fusion API
```

A ação recebe o token IMS do usuário do convidado e o encaminha até o upstream, para que as chamadas ainda sejam feitas em nome do usuário com suas permissões.

## Etapa 1: declarar a ação

As ações de tempo de execução são declaradas em `app.config.yaml` no `runtimeManifest` da extensão. Adicionar uma ação `wf-proxy` ao lado da sua extensão:

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
    runtimeManifest:
      packages:
        fusion-uix-guest:                # ← your package name; part of the action URL
          license: Apache-2.0
          actions:
            wf-proxy:
              function: src/fusion-nav-organization-1/actions/wf-proxy/index.js
              web: 'yes'                  # exposes it at /api/v1/web/<package>/wf-proxy
              runtime: nodejs:22
              inputs:
                LOG_LEVEL: debug
              annotations:
                require-adobe-auth: false # see note below
                final: true
```

A ação fica acessível em:

```
/api/v1/web/<package>/<action>     e.g.  /api/v1/web/fusion-uix-guest/wf-proxy
```

### `require-adobe-auth`: verdadeiro vs. falso

Essa anotação controla se o gateway do Adobe valida um token IMS antes da execução da ação.

* **`true`:** O padrão seguro.  O gateway rejeita chamadas não autenticadas. No entanto, o validador é estrito sobre quais cabeçalhos espera e pode rejeitar solicitações ou descartar cabeçalhos personalizados necessários para sua chamada de upstream. Se isso acontecer, ele será exibido como um `401` mesmo que seu token seja válido.
* **`false`:** Ignora a verificação de gateway. Sua ação é então publicamente invocável, então você **deve** impor a autorização você mesmo. Exigir um portador de `Authorization` na ação e rejeitar, se estiver ausente, em seguida, e encaminhá-lo para upstream, onde o Workfront e o Fusion o validarão. Combinado com um incluo na lista de permissões de destino estrito, descrito na Etapa 2, esse é o caminho confiável para um proxy que precisa passar cabeçalhos personalizados.

>[!TIP]
>
> Tente `true` primeiro. Se você vir um `401` que não pode explicar porque o token é válido e funciona em outro lugar, alterne para `false` **e** para manter a verificação do portador e inclua na lista de permissões em sua ação para que a segurança ainda seja imposta upstream.

## Etapa 2: Gravar a ação para um proxy ➡ incluído na lista de permissões

Criar `src/fusion-nav-organization-1/actions/wf-proxy/index.js`. Duas regras mantêm isso seguro: um incluo na lista de permissões de destinos upstream para que a ação não possa ser usada como uma retransmissão aberta e um token de portador necessário que seja encaminhado upstream.

```js
const fetch = require('node-fetch')
const { Core } = require('@adobe/aio-sdk')
const { errorResponse, getBearerToken, checkMissingRequestInputs } = require('../utils')

// Page-through query params (see "Paginate list results" below).
const pageQuery = (p) => {
  const q = new URLSearchParams()
  if (p.start != null) q.set('start', p.start)
  if (p.limit != null) q.set('limit', p.limit)
  return q
}

// Only these upstreams may be reached. Never build the URL from arbitrary input.
const TARGETS = {
  subscriptions: {
    method: 'GET',
    url: () => 'https://<your-wf-host>/attask/eventsubscription/api/v1/subscriptions',
  },
  hooks: {
    method: 'GET',
    // Fusion hooks are team-scoped: teamId is a REQUIRED query param (see below).
    url: (p) => {
      const q = pageQuery(p)
      if (p.teamId) q.set('teamId', p.teamId)
      return `https://fusion.adobe.com/api/v3/hooks?${q.toString()}`
    },
  },
  scenarios: {
    method: 'GET',
    url: (p) => {
      const q = pageQuery(p)
      if (p.fusionOrgId) q.set('organizationId', p.fusionOrgId)
      return `https://fusion.adobe.com/api/v3/scenarios?${q.toString()}`
    },
  },
}

async function main (params) {
  const logger = Core.Logger('main', { level: params.LOG_LEVEL || 'info' })
  try {
    const missing = checkMissingRequestInputs(params, ['target'], ['Authorization'])
    if (missing) return errorResponse(400, missing, logger)

    const target = TARGETS[params.target]
    if (!target) return errorResponse(400, `unknown target '${params.target}'`, logger)

    const token = getBearerToken(params)              // reads params.__ow_headers.authorization
    const headers = { authorization: `Bearer ${token}`, 'content-type': 'application/json' }
    if (params.orgId) headers['x-gw-ims-org-id'] = params.orgId        // Adobe IMS org id
    if (params.fusionOrgId) headers['x-organization-id'] = params.fusionOrgId  // Fusion tenant id
    if (params.teamId) headers['x-team-id'] = params.teamId            // Fusion team id

    const res = await fetch(target.url(params), { method: target.method, headers })
    const text = await res.text()
    let body
    try { body = JSON.parse(text) } catch (e) { body = text }

    if (!res.ok) {
      return { statusCode: res.status, body: { error: `upstream ${res.status}`, target: params.target, details: body } }
    }
    return { statusCode: 200, body }
  } catch (error) {
    logger.error(error)
    return errorResponse(500, 'server error: ' + error.message, logger)
  }
}

exports.main = main
```

`getBearerToken`, `errorResponse` e `checkMissingRequestInputs` vêm do `actions/utils.js` gerado, em que o modelo os estrutura. `getBearerToken` lê `params.__ow_headers.authorization`, que é onde o gateway coloca o cabeçalho `Authorization` de entrada.

## Etapa 3: chamar a ação do convidado

Na sua interface, `fetch` a ação com uma URL relativa (mesma origem) e envie o token IMS como um portador. Transmita as IDs de organização e equipe de que o upstream precisa como parâmetros de consulta.

```js
const PROXY_URL = "/api/v1/web/fusion-uix-guest/wf-proxy";

async function callProxy(target, token, { imsOrgId, fusionOrgId, teamId, start, limit } = {}) {
  const params = new URLSearchParams({ target });
  if (imsOrgId) params.set("orgId", imsOrgId);          // → x-gw-ims-org-id
  if (fusionOrgId) params.set("fusionOrgId", fusionOrgId); // → x-organization-id
  if (teamId) params.set("teamId", teamId);             // → x-team-id
  if (start != null) params.set("start", start);        // pagination offset
  if (limit != null) params.set("limit", limit);        // pagination page size
  const res = await fetch(`${PROXY_URL}?${params.toString()}`, {
    headers: { authorization: `Bearer ${token}` },
  });
  if (!res.ok) throw new Error(`${target} request failed: ${res.status}`);
  return res.json();
}
```

Obter `token`, `imsOrgId`, `fusionOrgId` e `teamId` do contexto:

```js
const token       = connection.sharedContext.get("imsToken");
const imsOrgId    = connection.sharedContext.get("imsOrgId");
const fusionOrgId = connection.sharedContext.get("organization")?.id; // Fusion tenant id
const teamId      = connection.sharedContext.get("team")?.id;
```

Para obter informações sobre o contexto, consulte [A referência de contexto do Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Especificações da API Fusion v3

O que funcionou para o painel no `https://fusion.adobe.com/api/v3`:

| Cabeçalho / parâmetro | Valor | Notas |
| ---------------- | ------- | ------- |
| `Authorization` | `Bearer <imsToken>` | O token IMS do usuário do contexto. |
| `x-organization-id` | `organization.id` | A ID de locatário do Fusion, não a ID da organização IMS. O Fusion identifica o locatário por meio disso. |
| `x-team-id` | `team.id` | Enviar quando a chamada tiver escopo de equipe. |
| `x-gw-ims-org-id` | `imsOrgId` | ID da organização IMS da Adobe para o gateway. |

Observe os seguintes avisos:

* **`GET /api/v3/hooks`tem escopo de equipe:** `teamId` é um **parâmetro de consulta obrigatório** (`/api/v3/hooks?teamId=...`). Sem ele, você ganha um `400`. Isso significa que os ganchos voltam somente para a *equipe ativa*; para cobrir uma organização, equipes de loop e mesclagem.
* **`GET /api/v3/scenarios`** funciona com `organizationId` (`/api/v3/scenarios?organizationId=...`).

>[!NOTE]
>
> A referência oficial é as [APIs do Workfront Fusion](https://developer.adobe.com/workfront-fusion-apis/) da Adobe. Os requisitos de cabeçalho/autenticação variam de acordo com o gateway. Esta tabela reflete o que a demonstração realmente precisava. Se uma chamada retornar `401`/`400`, verifique novamente esses cabeçalhos primeiro.

## Paginar resultados da lista

Os pontos de extremidade da lista do Fusion v3 (ganchos, cenários) retornam uma **página** de cada vez, não o conjunto inteiro. Uma resposta tem esta aparência:

```json
{
  "items": [ /* ...this page of records... */ ],
  "_page": { "start": 0, "limit": 100, "total": 342 }
}
```

Os registros estão em **`items`**, e os metadados de paginação estão em **`_page`**. Sua página com os parâmetros de consulta **`start`** (deslocamento) e **`limit`** (tamanho da página). O proxy acima passa por ambos, portanto, a página no convidado faz um loop até que você tenha coletado tudo:

```js
const PAGE_LIMIT = 100;

async function fetchAllPages(target, token, opts = {}) {
  const all = [];
  let start = 0;
  // Stop when a page returns fewer than PAGE_LIMIT items, or when _page.total is reached.
  for (;;) {
    const res = await callProxy(target, token, { ...opts, start, limit: PAGE_LIMIT });
    const items = res.items ?? [];
    all.push(...items);

    const total = res._page?.total;
    const done = items.length < PAGE_LIMIT || (total != null && all.length >= total);
    if (done) break;
    start += PAGE_LIMIT;
  }
  return all;
}
```

Se você preferir manter a paginação fora do navegador, faça o mesmo loop dentro da ação de tempo de execução e retorne a matriz `items` mesclada em uma resposta. De qualquer maneira, não suponha que a primeira página seja todo o conjunto de resultados. Uma equipe com mais de uma página de ganchos pareceria ter cenários ausentes.

## Lista de verificação de segurança

* **Incluir na lista de permissões upstreams.** Nunca crie o URL de destino a partir da entrada bruta do cliente. Mapeie uma chave curta `target` para uma URL fixa, como na Etapa 2. Isso impede que sua ação se torne uma retransmissão aberta.
* **Exigir o token de portador** na ação e encaminhá-lo para upstream. Permitir que o Workfront e o Fusion imponham as permissões do usuário.
* **Nunca registrar o token.** `imsToken` é uma credencial. Mantenha `LOG_LEVEL` atento ao que `stringParameters` imprime.
* **Encaminhar somente por HTTPS** para hosts confiáveis de Adobe e Workfront.

## Exemplo trabalhado: o painel de assinaturas do evento

O painel de demonstração junta três fontes para mostrar, por assinatura de evento do Workfront, se um cenário do Fusion correspondente é íntegro:

1. `fetchSubscriptions()` → Assinaturas de eventos do Workfront (com contadores recebidos/transmitidos).
1. `fetchHooks(teamId)` → Ganchos do Fusion para a equipe ativa (paginados com `fetchAllPages`).
1. `fetchScenarios(fusionOrgId)` → Cenários de fusão para a organização (paginado com `fetchAllPages`).

A **junção** os encadeia, mas há um valor que merece ser chamado: uma assinatura do Workfront e o Fusion a capturam apontam para ativa em **hosts diferentes**, portanto, seus campos de URL não são iguais a byte por byte. O que é estável é o token **no final da URL do webhook** (o último segmento de caminho). Corresponda nesse token à direita, não no URL completo. O gancho `scenarioId` corresponde ao `id` de um cenário:

```
subscription.targetUrl  ──(trailing token)──▶  hook.url
                                                hook.scenarioId  ──▶  scenario.id
```

```js
// Reduce a webhook URL to its trailing token so hosts/bases can differ.
function hookKey(url) {
  if (!url) return "";
  const path = String(url).trim().toLowerCase().split(/[?#]/)[0].replace(/\/+$/, "");
  const i = path.lastIndexOf("/");
  return i >= 0 ? path.slice(i + 1) : path;
}

// Index hooks by token, then look each subscription up by the same token.
const hooksByToken = new Map(hooks.map((h) => [hookKey(pick(h, ["url", "address", "targetUrl"], "")), h]));
const hook = hooksByToken.get(hookKey(pick(sub, ["url", "endpointUrl", "targetUrl", "target.url", "callbackUrl"], "")));
```

O status é derivado da associação:

* **Quebrado**: nenhum gancho correspondente ou o gancho é `gone`.
* **Filtragem**: correspondente, mas `passed < received` (os eventos chegam, mas são filtrados antes da execução do cenário).
* **Íntegro**: correspondido e em trânsito.

Como as formas de carga real variam, o cliente mapeia os campos defensivamente, tentando várias chaves candidatas por campo, de modo que uma pequena diferença de API não quebra a tabela:

```js
function pick(obj, keys, fallback) {
  for (const key of keys) {
    const value = key.split(".").reduce((acc, part) => (acc == null ? acc : acc[part]), obj);
    if (value != null) return value;
  }
  return fallback;
}
```

Este é apenas um exemplo. O mesmo padrão de proxy funciona para qualquer API do Workfront ou Fusion necessária.
