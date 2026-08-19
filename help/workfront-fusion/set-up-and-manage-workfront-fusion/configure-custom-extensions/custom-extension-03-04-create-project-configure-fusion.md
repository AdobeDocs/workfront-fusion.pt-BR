---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Criar um projeto para Extensibilidade da interface
description: Criar um projeto para Extensibilidade da interface
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
source-wordcount: 1360
ht-degree: 0%

---

# Criar um projeto para Extensibilidade da interface

>[!NOTE]
>
>Este artigo presume alguma familiaridade com ferramentas de desenvolvimento de software.

Para criar uma extensão personalizada de interface do usuário, você deve criar um projeto do App Builder para ela.

Esta página descreve como gerar um projeto App Builder genérico com a linha de comando `aio`. &quot;Genérico&quot; significa que o projeto **não** inicia a partir de um modelo específico do produto. Começar com um aplicativo genérico mantém o projeto simples e permite que ele se conecte com o Workfront Fusion.

Pode ser útil se familiarizar com os seguintes conceitos e terminologia relacionados à criação de um projeto para uso com a Extensibilidade de IA do Adobe Fusion.

* O **Adobe Developer Console** (<https://developer.adobe.com/console>) é o painel da Web onde o projeto está.

* **Terminologia**:

  | Termo | O que significa |
  | ------ | --------------- |
  | **Organização** | A organização da Adobe da sua empresa. A mesma organização usada no Fusion. |
  | **Projeto** | Um container para um aplicativo/extensão. Você criará um projeto para sua extensão. |
  | **Workspace** | Uma cópia da configuração do projeto para uma fase de trabalho. Todos os projetos têm um espaço de trabalho de **Produção**, e você normalmente também usa um espaço de trabalho de **Preparo** para testes. Pense em espaços de trabalho como &quot;ambientes&quot;. |
  | **Credenciais/Serviços** | Permissões que seu aplicativo tem permissão para usar. Os padrões criados para você são suficientes para começar. |

* Há duas maneiras de criar um projeto:

  * **Automático (recomendado):** O comando `aio app init` cria o projeto e os espaços de trabalho para você ao gerar o código. Este artigo descreve esse processo.
  * **Manual:** Crie primeiro o projeto por conta própria na Developer Console e depois aponte `aio` para ele. Recomendamos fazer isso somente se sua organização exigir que os projetos sejam criados centralmente.

* Ao decidir qual espaço de trabalho usar, desenvolva e implante primeiro em **Preparar**. O Fusion carrega uma criação de Palco somente quando o usuário ativa o teste de Preparo em seu perfil do Fusion (menu de avatar do usuário > Configurações do produto > Perfil do Fusion > Preferências > Extensões de preparo); caso contrário, somente as extensões de Produção publicadas serão exibidas. Você também pode visualizar localmente com `aio app run` e, em seguida, promover para **Produção** mais tarde.

  Para obter mais informações sobre a promoção para produção, consulte [Publicar sua extensão](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).


## Executar `aio app init`

1. Abra um terminal.
1. No terminal, mova para a pasta onde você mantém os projetos.
1. Executar:

   ```sh
   aio app init my-fusion-extension --standalone-app
   ```

   * `my-fusion-extension` é o nome da pasta/aplicativo. Você pode selecionar esse nome, mas usar letras minúsculas, hifens e sem espaços.
   * O `--standalone-app` instrui a CLI a criar um **esqueleto de aplicativo simples**, em vez de pedir que você escolha um modelo de produto. Essa é a chave para evitar o modelo AEM (ou qualquer outro).

1. Quando solicitado, **selecione sua Organização** (se você pertencer a mais de uma).
1. Quando solicitado, selecione **Criar novo projeto** e aceite o nome sugerido, ou escolha um projeto vazio existente.

   O comando configura os espaços de trabalho **Preparo** e **Produção** automaticamente.

   O comando também gera arquivos na pasta `my-fusion-extension` e executa `npm install`.

1. Prossiga para [Confirmar criação do projeto](#confirm-project-creation).

>[!NOTE]
>
> **Se preferir o menu interativo:** execute `aio app init my-fusion-extension` > (sem `--standalone-app`). Quando ele pergunta **&quot;Quais modelos você deseja pesquisar?&quot;** ou mostra uma lista de verificação de modelos, não selecione um modelo de produto como o AEM. Escolha a opção para criar um **aplicativo independente** / **&quot;Todos os pontos de extensão → nenhum&quot;**.

## Verificar criação de projeto

1. No terminal, mova para a pasta criada:

   ```sh
   cd my-fusion-extension
   ```

   Você deve ver uma estrutura semelhante a esta (alguns arquivos omitidos):

   ```
   my-fusion-extension/
   |--- app.config.yaml   // main configuration (you will edit this)
   |---  package.json   //dependencies and scripts
   |---  src/    // your source code
   |---  web-src/  or  src/.../web-src/  // front-end files (HTML/JS)
   ```

   Os dois arquivos mais importantes para você são:

   * **`app.config.yaml`**: A configuração central. Em uma parte posterior do processo, você adicionará uma seção `extensions:` aqui que conecta seu aplicativo a um ponto de extensão do Fusion.
   * **`package.json`**: lista as bibliotecas que seu aplicativo usa. Você adicionará a biblioteca de convidados Extensibilidade da interface do usuário do Adobe aqui.

1. Continue em [Adicionar bibliotecas necessárias](#add-required-libraries).

>[!TIP]
>
> Não se preocupe se o layout gerado for um pouco diferente entre as versões da CLI. Esse procedimento informa exatamente quais arquivos criar e o que colocar neles, para que você possa corresponder à estrutura esperada, independentemente do ponto de partida.

## Adicionar bibliotecas necessárias

Sua extensão precisa de duas bibliotecas:

* **`@adobe/uix-guest`**: Permite que seu aplicativo se comunique com o Fusion (o host).
* **`@adobe/react-spectrum`**: componentes da interface do usuário React do Adobe, de modo que sua tela corresponda à aparência do Adobe. (Opcional, mas recomendado; você pode usar HTML simples.)

Para instalar essas bibliotecas:

1. No terminal, execute:

   ```sh
   npm install @adobe/uix-guest @adobe/react-spectrum
   ```

1. (Condicional) Se o projeto gerado ainda não incluir o React, instale-o também:

   ```sh
   npm install react react-dom react-router-dom
   ```

1. Continue para [Confirmar as compilações do projeto](#confirm-the-project-builds).

## Confirmar as compilações do projeto

Antes de alterar qualquer coisa, verifique se o projeto vazio é compilado

1. No terminal, execute:

   ```sh
   aio app build
   ```

   Se isso for concluído sem erros, as ferramentas e o projeto serão configurados corretamente. Você está pronto para conectar o projeto ao Fusion.

   >[!TIP]
   >
   > **Se a compilação falhar**, a causa mais comum é uma versão Node.js não suportada. Execute `node --version` e verifique se ele é 18 ou 20.
   >
   >* Para obter informações sobre como instalar o Node.js, consulte [Configurar as ferramentas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
   >* Para obter informações sobre outros possíveis erros, consulte [Solução de problemas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

1. Continue em [Configurar o projeto para Fusion](#configure-the-project-for-fusion).

## Configurar o projeto para Fusion

A próxima etapa na configuração da extensão personalizada é conectar o projeto genérico ao Workfront Fusion.

Você vai:

1. [Criar uma pasta para sua extensão](#create-a-folder-for-your-extension)
1. Conte à App Builder sobre um **ponto de extensão** do Fusion (em `app.config.yaml`).
1. Descreva as partes da sua extensão (em `ext.config.yaml`).
1. **Registre** seu widget para que o Fusion saiba seu título e onde está sua interface do usuário.

Usamos `fusion/nav-organization/1` em todo o. Para direcionar a seção Equipe, troque `fusion/nav-team/1` em todos os lugares. Para suportar ambos, repita o padrão para cada um.

## Criar uma pasta para sua extensão

1. Crie os arquivos para que o projeto tenha esta aparência:

   ```
   my-fusion-extension/
   |-- app.config.yaml
   |-- src/
          |-- fusion-nav-organization-1/          // one folder per extension point
             |-- ext.config.yaml
             |-- web-src/
                |-- src/
                   |-- components/
                      |-- App.js
                      |-- ExtensionRegistration.js
                      |-- DashboardWidget.js
                      |-- Constants.js
   ```

   Recomendamos nomear a pasta após o ponto de extensão (`fusion-nav-organization-1`). O nome exato depende de você, mas deve corresponder ao que você menciona em `app.config.yaml`.

1. Continuar para [Declarar o ponto de extensão em `app.config.yaml`](#declare-the-extension-point-in-appconfigyaml).

## Declarar o ponto de extensão em `app.config.yaml`

1. Abrir `app.config.yaml` e atualizar seu conteúdo para:

   ```yaml
   extensions:
     fusion/nav-organization/1:
       $include: src/fusion-nav-organization-1/ext.config.yaml
   ```

   Esse conteúdo descreve o seguinte:

   * `extensions:`: este aplicativo implementa um ou mais pontos de extensão.
   * `fusion/nav-organization/1`: o slot Fusion ao qual você está se conectando. **O nome deve corresponder exatamente**, incluindo a versão `1`.
   * `$include:`: aponta para um segundo arquivo de configuração (criado na próxima etapa) que descreve o conteúdo dessa extensão. Manter em um arquivo separado mantém `app.config.yaml` limpo e permite que você adicione mais pontos de extensão posteriormente.

   >[!NOTE]
   >
   >Se você estiver direcionando ambas as extensões, liste ambas, cada uma com sua própria pasta:
   >
   > ```yaml
   > extensions:
   >     fusion/nav-organization/1:
   >         $include: src/fusion-nav-organization-1/ext.config.yaml
   >     fusion/nav-team/1:
   >         $include: src/fusion-nav-team-1/ext.config.yaml
   > ```

   1. Continuar para [Descrever a extensão em `ext.config.yaml`](#describe-the-extension-in-extconfigyaml)

## Descrever a extensão em `ext.config.yaml`

1. Criar `src/fusion-nav-organization-1/ext.config.yaml` com:

   ```yaml
   operations:
      view:
       - type: web
         impl: index.html
   web: web-src
   hooks:
     pre-app-build: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
      pre-app-run: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
   ```

   Esse conteúdo descreve o seguinte:

   * **`operations.view`**: Declara que sua extensão fornece uma **visualização** (uma interface visível), veiculada a partir de `index.html`. É isso que faz com que sua extensão mostre uma tela em vez de ser executada somente em segundo plano.
   * **`web: web-src`**: a pasta que armazena seus arquivos front-end. O App Builder cria tudo aqui e o hospeda na Rede de entrega de conteúdo (CDN) da Adobe.
   * **`hooks`**: pequenos comandos que são executados automaticamente em tempo de compilação/execução. O script `generate-metadata.js` vem com `@adobe/uix-guest` e produz um arquivo `app-metadata.json` de que seu código de registro precisa (consulte a Etapa 4). Você não escreve esse script; você só faz referência a ele.

   >[!NOTE]
   >
   > Se também precisar de lógica do lado do servidor, você também pode adicionar `actions` sem servidor (pequenas funções de back-end). As ações são opcionais e não são necessárias para renderizar uma interface do usuário, portanto, as deixamos de fora para manter este guia focalizado. Se você os adicionar posteriormente, declare uma pasta `actions:` aqui e um `runtimeManifest:` em `app.config.yaml`. O motivo mais comum para adicionar um é chamar APIs do Workfront/Fusion sem acessar o CORS do navegador.
   > Para obter informações sobre como chamar APIs, consulte [Chamada de APIs do Workfront e Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).
1. Continue para [Definir uma ID de extensão estável](#set-a-stable-extension-id).

## Definir uma ID de extensão estável

Sua extensão requer uma ID exclusiva que ambos os quadros compartilham.

Para obter informações sobre quadros em relação a extensões personalizadas, consulte [Quadros incluídos em uma Extensão de Interface do Usuário](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

1. Criar `src/fusion-nav-organization-1/web-src/src/components/Constants.js`:

   ```js
   module.exports = {
     extensionId: 'my-fusion-extension'
   };
   ```

   Use o mesmo valor em todos os locais em que o código se refere à id da extensão.
1. Continue em [Registrar seu widget](#register-your-widget).


## Registrar seu widget

&quot;Registro&quot; é como o quadro de fundo oculto informa ao Fusion o que sua extensão oferece. Você declara um método `dashboard.getWidget()` que retorna o título do widget e a URL da interface visível.

1. Criar `src/fusion-nav-organization-1/web-src/src/components/ExtensionRegistration.js`.
A parte importante é a chamada `register(...)`:

   ```js
   import { register } from "@adobe/uix-guest";
   import metadata from "../../../../app-metadata.json";
   import { extensionId } from "./Constants";
   
   async function init() {
     await register({
       id: extensionId,
       metadata,
       methods: {
         dashboard: {
           getWidget() {
             return {
               id: extensionId,
               title: "My Fusion tool",        // shown on the Fusion nav button
               description: "What this tool does",
               url: "/index.html#/my-widget",  // route to your visible UI
               hideWidgetHeader: false          // false = Fusion shows the title
             };
           }
         }
       }
      });
   }
   
   init().catch(console.error);
   ```

   Pontos principais:

   * **`title`** é o rótulo que o Fusion coloca no botão de navegação. Se `hideWidgetHeader` for `false`, o Fusion também mostrará o título como um cabeçalho acima da interface do usuário.
   * **`url`** é a rota para sua interface do usuário *visível* dentro deste mesmo aplicativo. Aqui está uma rota de hash (`#/my-widget`) manipulada pelo seu roteador front-end (configurado na próxima página). Ele deve resolver para o componente que renderiza sua tela.
   * **`metadata`** vem de `app-metadata.json`, que o gancho `generate-metadata` cria para você no momento da compilação. Importe-o como mostrado.
   * O nome do método `dashboard.getWidget` é o contrato acordado que o Fusion chama para descobrir seu widget. Mantenha o namespace `dashboard` e o nome `getWidget`.

O back-end da sua extensão agora está concluído. A próxima etapa para criar a interface do usuário da extensão.

Para obter instruções sobre como criar a interface, consulte [Criar a interface de extensão personalizada](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
