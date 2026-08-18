---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Solução de problemas de extensões personalizadas
description: Solução de problemas de extensões personalizadas
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 0%

---


# Solução de problemas de extensões personalizadas

>[!NOTE]
>
>Este artigo presume alguma familiaridade com ferramentas de desenvolvimento de software.

Este artigo apresenta algumas soluções para os problemas que você provavelmente encontrará ao criar extensões personalizadas, aproximadamente na ordem em que ocorrem durante o desenvolvimento.

## Lista de verificação rápida

Se algo não funcionar, verifique primeiro:

* O Node.js é versão 18 ou 20 (`node --version`).
* Você está conectado (`aio login`) e na organização/projeto/espaço de trabalho correta (`aio console where`).
* O nome do ponto de extensão corresponde exatamente, incluindo a versão: `fusion/nav-organization/1`.
* O `url` em `getWidget()` corresponde a uma rota no seu aplicativo.
* Sua interface visível chama `attach({ id })`.
* Você está olhando para o conjunto certo de extensões no Fusion:
  * Para ver uma build do Stage, implante no Stage e ative a opção de extensões do Stage no seu perfil do Fusion (Configurações do produto > Perfil do Fusion > Preferências).
  * Para ver uma extensão publicada, implante para produção e aprove-a.

## Erro 1060: &quot;O ponto de extensão não existe&quot;

**Mensagem completa:** `CoreConsoleAPISDK ... 1060: Extension point 'fusion/nav-organization/1' does not exist` durante `aio app deploy`.

**Significado:** O ponto de extensão do Fusion ainda não está habilitado (&quot;integrado&quot;) para sua organização da Adobe. A Adobe valida, no momento da implantação, se o ponto de extensão existe no catálogo da organização. Isto **não** um problema com seu código ou YAML.

**Correção:** Peça à equipe do Fusion para integrar os pontos de extensão (`fusion/nav-organization/1` e/ou `fusion/nav-team/1`) para sua organização IMS. Ao solicitar a integração, inclua:

* sua **IMS organization id** (`XXXX@AdobeOrg`),
* o(s) **ponto(s) de extensão** necessário(s),
* seus nomes de **projeto e espaço de trabalho do Developer Console**.

Depois que a integração for confirmada, execute `aio app deploy` novamente.


## &quot;Aguardando mensagem inicial do iframe de destino&quot; / o painel gira para sempre

**Significado:** O Fusion abriu sua interface do usuário visível, mas não concluiu o handshake. Portanto, o Fusion atingiu o tempo limite.

**Causas comuns:**

* `attach` está somente no componente de registro, não no widget visível.
* O `url` em `getWidget()` aponta para uma rota que renderiza o componente **registro** (ou uma página em branco) em vez do seu widget.
* O `id` passado para `attach` difere do `id` usado em `register`. Eles devem ser idênticos, portanto, mantenha ambos em `Constants.js`.

**Correção:** verifique se suas chamadas de componente **visíveis** `attach({ id })`:

```jsx
useEffect(() => {
  attach({ id: extensionId }).catch(console.error);
}, []);
```

Para obter mais informações, consulte [Criar a interface de extensão personalizada](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).



## O botão de navegação não é exibido no Fusion

Se o botão de navegação da sua extensão personalizada não aparecer no Fusion, verifique esses itens em ordem:

1. **Você está observando o conjunto correto de extensões?** Por padrão, o Fusion mostra somente as extensões publicadas, que foram implantadas na Produção e aprovadas. Se você estiver testando uma criação do Stage, ative o switch de extensões do Stage no seu perfil do Fusion (Configurações do produto > Perfil do Fusion > Preferências) e recarregue. Os itens de preparo estão rotulados como **(Estágio)**.
Para obter mais informações, consulte [Publicar sua extensão personalizada](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. **Foi revogado ou cancelado?** Uma extensão revogada ou cancelada para de aparecer no Fusion sem erros. Se um botão que estava funcionando anteriormente desaparecer, confirme se ele ainda está ativo no Adobe Exchange antes de procurar um problema de código.
1. **Ele foi implantado no espaço de trabalho correto?** Implante no espaço de trabalho que você está carregando, o espaço de trabalho Preparo quando estiver usando a opção Teste de preparo.
1. **Ele foi implantado na organização correta?** Entre no Fusion com uma conta na **mesma** organização IMS na qual você implantou.
1. **Está na seção correta?** `fusion/nav-organization/1` programas em **Organização**; `fusion/nav-team/1` programas em **Equipe** (você deve selecionar uma equipe primeiro).
1. **Há um erro de tipo de nome de ponto de extensão?** Deve ler exatamente `fusion/nav-organization/1` no caminho de inclusão `app.config.yaml` e `ext.config.yaml` da pasta.


## O botão é exibido, mas o painel está em branco

Se o botão for exibido, mas o painel estiver em branco, verifique o seguinte:

* **Incompatibilidade de rota:** `url` de `getWidget()` (como `/index.html#/my-widget`) deve corresponder a `<Route>` em `App.js`. Uma incompatibilidade carrega uma página sem componente.
* **Erro do JavaScript:** abra as ferramentas de desenvolvedor do navegador (F12) > guia **Console** e procure erros provenientes do iframe. Corrija o erro relatado e implante novamente.
* **Cabeçalho ausente/duplicado:** `hideWidgetHeader` em `getWidget()` controla se o Fusion mostra o título acima da sua interface do usuário. Defina como `true` se você renderizar seu próprio cabeçalho.

## O iframe está bloqueado (Política de segurança de conteúdo / &quot;recusou-se a enquadrar&quot;)

O Fusion só permite extensões hospedadas na CDN (`*.adobeio-static.net`) do App Builder da Adobe, que é onde o `aio app deploy` coloca seus arquivos por padrão. Se você hospeda sua interface em outro lugar, como um domínio personalizado, o Fusion se recusa a carregá-la. Implante por meio do App Builder conforme documentado ou pergunte à equipe do Fusion se seu domínio pode ser.

## O contexto está vazio ou obsoleto

* **Vazio logo após o carregamento:** Leia o contexto **após** `attach` resolve, não antes. Até lá, mostre um estado &quot;Conectando...&quot;.
* **Não é atualizado quando o usuário alterna a organização ou a equipe:** Inscreva-se no evento `contextchange` e leia novamente suas chaves dentro do manipulador. Para obter mais informações, consulte [Ler o contexto Compartilhamentos de fusão](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md#read-the-context-fusion-shares) no artigo Criar a interface de extensão personalizada.
* **As datas parecem incorretas:** os campos de data chegam como ISO **cadeias de caracteres**, não como objetos `Date`. Envolva-os em `new Date(...)`. Consulte [Datas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md#dates) no artigo A referência de contexto do Fusion.

## A chamada de uma API falha com um erro CORS

**Sintoma:** o Console do navegador mostra *&quot;Nenhum cabeçalho &#39;Access-Control-Allow-Origin&#39;&quot;* (ou a solicitação está bloqueada) quando a interface do usuário chama uma API do Workfront/Fusion diretamente.

**Correção:** não chame essas APIs do navegador. Rotear a chamada por meio de sua própria **ação de tempo de execução** do App Builder (no lado do servidor, sem CORS) e fazer com que o convidado chame a ação com uma URL relativa de mesma origem. Para obter mais informações, consulte [Chamada de APIs do Workfront e Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


## A ação de proxy retorna 401 mesmo com um token válido

**Significado:** com `require-adobe-auth: true`, o gateway da Adobe valida a chamada antes que sua ação seja executada e pode rejeitá-la ou descartar cabeçalhos personalizados de que você precisa, aparecendo como um `401`.

**Correção:** Defina `require-adobe-auth: false` na ação **e** para impor a autorização você mesmo. Exigir um portador de `Authorization` na ação, encaminhá-lo para upstream e manter um incluo na lista de permissões de destino estrito. Consulte [require-adobe-auth: true vs. false](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#require-adobe-auth-true-vs-false).

## Fusion `GET /api/v3/hooks` retorna 400

**Significado:** O ponto de extremidade dos ganchos é **de escopo de equipe**, portanto, `teamId` é um parâmetro de consulta obrigatório.

**Correção:** Chame `/api/v3/hooks?teamId=<team.id>`. Ganchos voltam apenas para a equipe ativa. Para cobrir uma organização, repita suas equipes e mescle. Os cenários, por outro lado, aceitam `organizationId`. Consulte [Especificações da API Fusion v3](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#fusion-v3-api-specifics).


## `aio` erros

* **`aio: command not found`:** A CLI não está instalada ou não está em seu PATH. Execute `npm install -g @adobe/aio-cli` novamente e abra um novo terminal.
* **Falha de compilação/implantação em uma versão de Nó totalmente nova:** Use o Nó **18 ou 20 LTS**. Versões muito novas, que não são LTS, às vezes quebram a cadeia de ferramentas.
* **&quot;Você não é um desenvolvedor&quot; / não pode ver sua organização:** O administrador da organização da Adobe deve conceder a você a função de **Desenvolvedor** e acesso à App Builder. Para obter mais informações, consulte [Configurar ferramentas e conta de extensão da interface](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
* **401 / token inválido durante a implantação ou descoberta:** sua sessão expirou ou você está misturando ambientes. Execute `aio logout` e depois `aio login`, confirme `aio console where` e implante no espaço de trabalho que você está carregando.

## Coleta de informações para suporte

Colete essas informações para agilizar o diagnóstico:

* O comando exato que você executou e a saída de erro **full**.
* Sua **ID de organização IMS**, **projeto** e **espaço de trabalho**.
* O **ponto de extensão** que você está direcionando.
* Se `aio app deploy` teve êxito e se a extensão foi **publicada** (ou, para um teste de Preparo, se a opção de extensões de Estágio está ativada).
* Quaisquer erros no **Console** do navegador (F12) ao abrir o painel no Fusion.
