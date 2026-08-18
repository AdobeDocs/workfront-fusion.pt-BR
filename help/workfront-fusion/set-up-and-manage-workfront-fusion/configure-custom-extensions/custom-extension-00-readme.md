---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 'Extensões personalizadas da interface do usuário: índice do artigo'
description: Extensões personalizadas no Workfront Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 603
ht-degree: 3%

---


# Extensões personalizadas da interface do usuário: índice do artigo

O Fusion pode exibir sua própria interface da Web dentro da interface. Você cria um pequeno aplicativo web, chamado de extensão, publica-o no Adobe e ele aparece como um botão na navegação do Fusion. Quando um usuário clica nele, sua interface do usuário é carregada na área principal do Fusion e recebe automaticamente informações sobre quem está conectado, em qual organização e equipe ele está trabalhando e muito mais.

Esta seção da documentação de fusão o orienta por todo o processo, sem assumir a experiência anterior com o Adobe App Builder ou estruturas de front-end. Também inclui o código necessário, juntamente com explicações desse código.

## Quando usar este guia

Use este guia se quiser adicionar uma tela ou ferramenta personalizada ao Fusion. Você não precisa ser um desenvolvedor especialista. Você precisa se sentir confortável copiando comandos em um terminal e editando alguns arquivos de texto.

Para criar uma extensão de interface do usuário personalizada, você precisará de uma Adobe ID e acesso a uma organização da Adobe (o mesmo tipo de acesso que você usa para fazer logon no Fusion).

## O que você vai criar

Ao final deste guia você terá:

1. Um projeto Adobe **App Builder** gratuito. É aqui que sua extensão fica.
1. Um pequeno aplicativo Web que renderiza sua interface personalizada.
1. Esse aplicativo web se conectou a um dos pontos de extensão do Fusion para que apareça na navegação do Fusion.
1. Sua interface do usuário lendo o contexto em tempo real do Fusion, como o usuário, a organização e a equipe atuais, e reagindo quando o usuário alterna entre organização ou equipe.
1. A extensão foi publicada para que outros usuários da organização possam visualizá-la.

<!--

## How it works, in one picture

```
  Fusion (the "Host")                         Your extension (the "Guest")
  ───────────────────────────────                         ──────────────────────────────
  Left navigation                             A web app hosted by Adobe
   └── Organization                            (App Builder + UI Extensibility)
       └── [Your extension button]  ── click ──▶ Fusion opens your UI in an iframe
                                              and sends it live context:
                                               * signed-in user
                                               * active organization
                                               * active team
                                               * Adobe IMS identifiers
```

Fusion is the **host**. Your extension is the **guest**. They run in separate browser frames and talk to each other through Adobe's **UI Extensibility SDK** (no custom networking required on your side).

-->

## Índice

Leia as páginas em ordem na primeira vez. Mais tarde você pode pular direto para o que você precisa.

| # | Página | O que ele cobre |
| --- | ------ | ---------------- |
| 1 | [Visão geral e principais conceitos](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md) | O vocabulário, a arquitetura e para que serve cada ponto de extensão do Fusion. |
| 2 | [Configurar as ferramentas e a conta do Adobe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) | Node.js, a CLI do Adobe I/O, fazendo logon e criando seu projeto na Adobe Developer Console. |
| 3 | [Criar o projeto e configurá-lo para Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md) | Gere um projeto App Builder genérico com a linha de comando `aio` (não um modelo específico do produto). Em seguida, aponte seu projeto para um ponto de extensão do Fusion e registre seu widget. |
| 5 | [Criar a interface](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md) | Renderize sua tela personalizada e conclua a conexão (&quot;handshake&quot;) com o Fusion. |
| 6 | [A referência de contexto do Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md) | Cada campo do Fusion envia a você, o que significa e como reagir a alterações. |
| 7 | [Publicar sua extensão](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md) | Crie, implante e torne sua extensão visível no Fusion. |
| 8 | [Solução de problemas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md) | Correções para os erros mais comuns. |
| 9 | [Apresentação de demonstração](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-09-demo-walkthrough.md) | Um script linear de copiar e colar: scaffold do modelo genérico do Shell da Experience Cloud → redirecionar para o Fusion → implantar no Stage → executar no Fusion. Melhor para uma demonstração ao vivo. |
| 10 | [Chamada de APIs do Workfront e Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md) | Chame APIs de back-end a partir de sua extensão sem acessar o CORS do navegador, usando um proxy de ação de tempo de execução. Abrange `require-adobe-auth`, cabeçalhos Fusion v3 e um exemplo trabalhado. |

## Nota de disponibilidade

Atualmente, o Fusion expõe esses pontos de extensão:

* `fusion/nav-organization/1` — aparece na seção **Organização**.
* `fusion/nav-team/1` — aparece na seção **Equipe**.

Antes de publicar em um desses, o ponto de extensão deve ser integrado para sua organização da Adobe. Se a etapa de publicação falhar informando que o ponto de extensão &quot;não existe&quot;, consulte [Solução de problemas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Documentação oficial do Adobe

Este guia é específico do Fusion. Para a plataforma subjacente, as referências canônicas são:

* [Visão geral de extensibilidade da interface do usuário](https://developer.adobe.com/uix/docs/)
* [Fluxo de desenvolvimento de extensão da interface do usuário](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [Gerenciamento de extensões da interface do usuário (publicar/aprovar/revogar)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Introdução ao Adobe App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
