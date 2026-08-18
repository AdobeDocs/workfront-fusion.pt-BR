---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Configurar ferramentas e conta de extensão da interface do usuário
description: Configurar ferramentas e conta de extensão da interface do usuário
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
source-wordcount: 500
ht-degree: 0%

---


# Configurar ferramentas e conta de extensão da interface do usuário

Antes de criar uma Extensão de interface do usuário para o Workfront Fusion, é necessário configurar as ferramentas e a conta. Isso só precisa ser feito uma vez.

>[!NOTE]
>
>Este artigo presume alguma familiaridade com ferramentas de desenvolvimento de software.

<!--Access requirements-->

## Pré-requisitos

Para configurar as ferramentas de extensibilidade da interface do usuário e a conta do, é necessário o seguinte:

* **Uma Adobe ID** com acesso a uma organização da Adobe. Esta é a conta que você usa para fazer logon no Fusion.
* **Acesso de desenvolvedor ao App Builder.** O administrador da sua organização pode precisar conceder a você a função **Desenvolvedor** e adicionar você a um **Perfil de Produto** que inclua o App Builder. Se os comandos falharem posteriormente com &quot;você não é um desenvolvedor&quot; ou não puder ver sua organização, peça ao administrador da organização da Adobe para adicioná-lo.
* **Um Administrador do Sistema** <!--Adobe? Fusion?--> (possivelmente alguém na sua equipe) para a etapa final de lançamento. Criar e implantar precisa apenas da função de Desenvolvedor, mas **enviar uma extensão para aprovação/publicação requer a função de Administrador do Sistema**.

  Para obter mais informações sobre níveis de acesso do Adobe, consulte
  [Como obter acesso](https://developer.adobe.com/uix/docs/guides/get-access/) na documentação do Adobe.

* **Um computador no qual você pode instalar o software** e executar comandos de terminal (macOS, Windows ou Linux).

## Instalar Node.js

A ferramenta Adobe é executada em **Node.js**. Você deve instalar a versão **LTS** (18 ou 20).

1. Vá para <https://nodejs.org> e baixe o instalador do **LTS**.
1. Execute o instalador e aceite os padrões.
1. Confirme se funcionou abrindo um terminal e executando:

   ```sh
   node --version
   npm --version
   ```

   Você deve ver os números de versão (por exemplo, `v20.17.0` e `10.x`).

1. (Condicional) Se `node` não for encontrado, feche e reabra o terminal ou reinicie o computador.

1. Continue para [Instalar o Adobe I/O CLI (`aio`)](#install-the-adobe-io-cli-aio).

>[!TIP]
>
>* Se você trabalhar com várias versões de Nó, um gerenciador de versão como o `nvm` é conveniente, mas é opcional.
>* A CLI do Adobe requer o Nó 18 ou mais recente. Versões muito novas, que não são LTS, podem causar problemas ocasionalmente. Portanto, recomendamos o uso de LTS.

## Instalar a CLI do Adobe I/O (`aio`)

A ferramenta de linha de comando usada para criar, compilar e publicar sua extensão é chamada `aio`.

Para instalá-lo globalmente:

1. Use o seguinte comando `npm` na linha de comando.

   ```sh
   npm install -g @adobe/aio-cli
   ```

1. Confirme se ele foi instalado usando o seguinte comando:

   ```sh
   aio --version
   ```

   Você deve ver algo como `@adobe/aio-cli/11.x.x`.

1. Prossiga para [Fazer logon no Adobe](#sign-in-to-adobe).

>[!NOTE]
>
> Se você vir um erro de permissões no macOS/Linux, **não** use `sudo`. Em vez disso, corrija as permissões de pasta global do npm ou use um gerenciador de versão de Nó que é instalado em seu diretório inicial.

## Fazer logon no Adobe

1. Conecte a CLI à sua conta do Adobe com o seguinte comando:

   ```sh
   aio login
   ```

1. Na janela do navegador que é aberta, faça logon com sua Adobe ID e aprove o acesso.

1. Depois que o logon for bem-sucedido, feche a guia do navegador e retorne ao terminal.

1. (Opcional) Para sair mais tarde, (por exemplo, para alternar contas), use o comando: `aio logout`.
1. Continue em [Confirmar sua organização ativa](#confirm-your-active-organization).

## Confirmar sua organização ativa

Verifique em qual organização a CLI é apontada:

```sh
aio console org list      # see organizations you can use
aio console where         # see your currently selected org/project/workspace
```

Se você pertencer a várias organizações, selecione a correta:

```sh
aio console org select
```

Agora você está pronto para criar o projeto.
