---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Apresentação de demonstração de uma extensão personalizada
description: Apresentação de demonstração de uma extensão personalizada
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 964
ht-degree: 0%

---


# Apresentação de demonstração da criação de uma extensão personalizada no Fusion

>[!NOTE]
>
>Este artigo presume alguma familiaridade com ferramentas de desenvolvimento de software.

Esta demonstração aborda a criação de uma extensão personalizada, implantação e execução no Fusion.

O serviço inclui:

* Faça o scaffold de um aplicativo App Builder a partir do modelo genérico do Shell da Experience Cloud.
* Redirecione o aplicativo para um ponto de extensão do Fusion.
* Implante o aplicativo no espaço de trabalho Preparo.
* Ative o Teste de preparo no Fusion e mostre o aplicativo em execução.

Começar a partir do modelo em vez de um `--standalone-app` vazio significa que a inicialização de SPA é gerada para você: `index.js`, `exc-runtime.js`, `App.js` com roteamento e `ErrorBoundary`, e uma amostra `ExtensionRegistration`. As etapas ao vivo da demonstração são redirecionar a configuração e editar dois arquivos, que é exatamente como o `fusion-uix-guest` real foi criado.

>[!NOTE]
>
> **Hora:** A demonstração ao vivo leva cerca de 10 minutos após a configuração das ferramentas. Você deve fazer a configuração única (Nó 18/20, `aio` CLI, `aio login`) **antes** da demonstração. Para obter instruções, consulte [Configurar ferramentas de extensão da interface e conta](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


## Antes de começar

Isso precisa ser feito apenas uma vez e pode ser feito fora da câmera antes da demonstração.

```sh
node --version          # must be 18 or 20
aio --version           # @adobe/aio-cli installed
aio login               # signs you into your Adobe org
aio console org select  # pick the org you'll demo in (same org as Fusion)
```

Duas coisas devem ser verdadeiras na organização da demonstração:

* O ponto de extensão `fusion/nav-organization/1` está integrado para a organização. Se não estiver integrado, a implantação falhará com o erro 1060. Para obter mais informações, consulte [Solução de problemas de extensões personalizadas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).
* O recurso de extensões personalizadas é ativado no host do Fusion. (Esse recurso está ativado por padrão). Como você vai ver uma demonstração de uma compilação de Palco em vez de uma publicada, você também vai ativar o switch **Extensões de preparo** no seu perfil do Fusion. (Esta opção é mostrada na Etapa 7.) O Fusion mostra somente as extensões publicadas até que você o faça.

## Etapa 1: gerar o aplicativo a partir do modelo genérico

```sh
aio app init my-fusion-extension --template @adobe/generator-app-excshell
cd my-fusion-extension
```

* Selecione **Criar novo projeto** quando solicitado e aceite o nome sugerido.
* `@adobe/generator-app-excshell` é o modelo genérico de extensão da interface do usuário do **Experience Cloud Shell** e não é específico do produto. Ele cria um SPA completo e funcional em `src/dx-excshell-1/`.

>[!NOTE]
>
>Se preferir o menu, execute `aio app init my-fusion-extension`, escolha **Adicionar extensões ou aplicativo independente** > **Modelos** e selecione **&quot;Extensão do App Builder UIX para o Experience Cloud Shell&quot;**.

Você receberá um conjunto de arquivos, incluindo o seguinte:

```
my-fusion-extension/
|-- app.config.yaml
|-- src/dx-excshell-1/
    |-- ext.config.yaml
    |-- web-src/src/
        |-- index.js          // SPA bootstrap (exc-app Runtime + React render)
        |-- exc-runtime.js    // Experience Cloud Shell runtime glue
        |-- components/
            |-- App.js                    // Router + ErrorBoundary (generated)
            |-- ExtensionRegistration.js  // sample registration (generated)
```

## Etapa 2: Adicionar a biblioteca de convidados do Fusion

O modelo já inclui o React, o React Spectrum e o exc-app. Adicione a biblioteca que conversa com o host Fusion:

```sh
npm install @adobe/uix-guest
```

## Etapa 3: Redirecionar a configuração para o Fusion

Abra **`app.config.yaml`** e altere **somente a chave do ponto de extensão** do Shell da Experience Cloud para o Fusion (deixe o caminho `$include` como está):

```yaml
extensions:
  fusion/nav-organization/1:                 # was: dx/excshell/1
    $include: src/dx-excshell-1/ext.config.yaml
```

Não é necessário alterar mais nada na configuração. O nome da pasta `dx-excshell-1` é interno e não afeta o Fusion, portanto, você pode deixá-lo. Renomear também significaria atualizar quaisquer caminhos de ação. Pule isso para a demonstração.

>[!NOTE]
>
>Se você estiver direcionando a seção **Equipe**, use `fusion/nav-team/1`. Para enviar **a organização e a equipe de** em produção, use **dois projetos separados**. Um pacote de ponto de extensão por nome de registro evita uma colisão de aplicativo compartilhado.

## Etapa 4: Editar arquivos de registro e widget

Todos os caminhos estão em `src/dx-excshell-1/web-src/src/components/`.

### **`ExtensionRegistration.js`**

O arquivo gerado registra uma amostra do Shell da Experience Cloud. Substitua seu `methods` pelo contrato do Fusion **`dashboard.getWidget`** para que o Fusion saiba seu título e onde está a interface do usuário:

```js
import { Text } from "@adobe/react-spectrum";
import { register } from "@adobe/uix-guest";
import metadata from "../../../../app-metadata.json";
import { extensionId } from "./Constants";

function ExtensionRegistration() {
  const init = async () => {
    await register({
      id: extensionId,
      metadata,
      methods: {
        dashboard: {
          getWidget() {
            return {
              id: extensionId,
              title: "My Fusion tool",          // label on the Fusion nav button
              description: "Hello from App Builder",
              url: "/index.html#/widget",       // route to the visible UI (4b)
              widgetSize: { defaultWidth: 6, defaultHeight: 6 },
              hideWidgetHeader: false,
            };
          },
        },
      },
    });
  };
  init().catch(console.error);

  return <Text>Registering with Fusion...</Text>;
}

export default ExtensionRegistration;
```

Se `Constants.js` não existir ao lado dele, crie-o:

```js
module.exports = { extensionId: "my-fusion-extension" };
```

### `DashboardWidget.js`

Crie este arquivo. Ele conclui o handshake e mostra o contexto do Fusion em tempo real:

```js
import { useEffect, useState } from "react";
import { Flex, Heading, Text, View } from "@adobe/react-spectrum";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

export default function DashboardWidget() {
  const [ctx, setCtx] = useState(null);

  useEffect(() => {
    attach({ id: extensionId })
      .then((guest) => {
        const read = () =>
          KEYS.reduce((acc, k) => ({ ...acc, [k]: guest.sharedContext.get(k) }), {});
        setCtx(read());
        guest.addEventListener("contextchange", () => setCtx(read()));
      })
      .catch((e) => console.error("attach failed", e));
  }, []);

  return (
    <View padding="size-300">
      <Heading level={2}>Hello from App Builder</Heading>
      {!ctx ? (
        <Text>Connecting to Fusion...</Text>
      ) : (
        <Flex direction="column" gap="size-100" marginTop="size-200">
          <Text>User: {ctx.user?.name ?? ctx.imsUserId}</Text>
          <Text>Organization: {ctx.organization?.name} (id {ctx.organization?.id})</Text>
          <Text>Team: {ctx.team?.name ?? "-"}</Text>
        </Flex>
      )}
    </View>
  );
}
```

### `App.js`

O roteador gerado já envia `index` / `index.html` para `ExtensionRegistration`. Adicionar uma rota para o widget e importá-lo:

```js
import DashboardWidget from "./DashboardWidget";
// ...inside <Routes>, alongside the existing ExtensionRegistration routes:
<Route exact path="widget" element={<DashboardWidget />} />
```

> O caminho da rota (`widget`) deve corresponder ao hash em `getWidget().url` (`/index.html#/widget`). Mantenha o `index.js` / `exc-runtime.js` gerado e o restante do `App.js` exatamente como andaime, pois essa é a inicialização que você deseja que o modelo forneça.

## Etapa 5: criação

```sh
aio app build
```

Isso compila o front-end e executa o gancho de metadados que gera `app-metadata.json`. Corrija os erros antes de continuar.

## Etapa 6: implantar no preparo

```sh
aio console workspace select     # choose Stage
aio app deploy
```

O `deploy` hospeda sua interface na CDN da Adobe e registra o ponto de extremidade de extensão no espaço de trabalho do Palco, que é o que permite que o Fusion a descubra. A CLI imprime a URL do ponto de extremidade, como `https://<project>-stage.adobeio-static.net`.

## Etapa 7: ativar o Teste de preparo e mostrar a extensão no Fusion

1. Abra o Fusion na Experience Cloud, conectado na mesma organização em que você implantou o.
1. Abra o menu de avatar do usuário e vá para **Configurações do Produto** > **Perfil do Fusion** > **Preferências**.
1. Ative a opção **Extensões de preparo** e confirme o recarregamento.

   O Fusion agora carrega extensões do espaço de trabalho do Stage e as marca **(Stage)**.
1. Vá para a área **Organização** da navegação à esquerda.

   Seu botão **&quot;Minha ferramenta Fusion (Preparo)&quot;** é exibido.
1. Clique no botão **&quot;Minha ferramenta Fusion (Preparo)&quot;**.
Sua interface do usuário é carregada no painel principal e mostra o usuário, a organização e a equipe ativos.
1. **Alternar a organização ou a equipe ativa** no Fusion.

   O painel é atualizado, o que demonstra o contexto ativo (`contextchange`).

>[!TIP]
>
>Se o botão não for exibido, recarregue uma vez, pois a descoberta é armazenada em cache por sessão. Em seguida, consulte [Solução de problemas de extensões personalizadas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).


## Iterando durante a demonstração

Faça uma alteração, depois recrie e implante novamente.  Os usuários verão a extensão atualizada na próxima vez que abrirem.

```sh
aio app build && aio app deploy
```

## Ir para a produção após a demonstração

O palco é suficiente para a demonstração. Para liberar recursos em toda a organização, alterne para o espaço de trabalho Produção, implante e envie a solicitação de aprovação. A solicitação deve ser enviada usando uma função de Administrador do sistema. Para ver o processo completo, consulte [Versão na Produção](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md#release-on-production).

## Demonstração do talk-track (opcional)

Você pode fazer os seguintes pontos durante a demonstração ao vivo:

* **&quot;Eu comecei a partir do modelo genérico do Shell da Experience Cloud.&quot;** Ele estrutura todo o shell SPA, então só redirecionei o ponto de extensão e editei dois arquivos.
* **&quot;O Fusion é o host, meu aplicativo é o convidado.&quot;** Eles são executados em quadros separados e conversam sobre o Adobe UI Extensibility SDK, sem rede personalizada.
* **&quot;Registro vs. exibição&quot;** O quadro oculto *registra* o que eu ofereço (`dashboard.getWidget`) e o quadro visível *anexa* e lê o contexto.
* **&quot;O teste de preparo é uma opção por usuário.&quot;** O Fusion mostra somente as extensões publicadas por padrão. Usei extensões do Stage no meu perfil do Fusion para carregar minha build do Stage, sem uma versão de produção.
* **&quot;Contexto ao vivo.&quot;** A alternância de organização ou equipe reenvia o contexto e o convidado é renderizado novamente.
