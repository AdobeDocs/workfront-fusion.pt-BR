---
title: Visão geral do cenário
description: O Adobe Workfront Fusion exige uma licença do Adobe Workfront Fusion, além de uma licença do Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: de81ad4c-27e5-4b6c-acf0-f01a8c85922e
source-git-commit: 34dad92019ca855f40698d3f3795788698c1cece
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Visão geral do cenário

O papel do Adobe Workfront Fusion é automatizar seus processos para que os usuários não precisem gastar muito tempo em tarefas de rotina. Ele funciona vinculando ações em e entre aplicativos e serviços para criar um cenário que transfere e transforma seus dados automaticamente. O cenário que você cria observa dados em um aplicativo ou serviço e processa esses dados para fornecer o resultado desejado.

Um cenário é composto de uma série de módulos que indicam como os dados devem ser transformados em um aplicativo ou transferidos entre aplicativos e serviços da Web.

## Visão geral dos elementos do cenário

Um cenário é criado com elementos diferentes. Entender a terminologia desses elementos facilita o uso da documentação.

* [Cenário](#scenario)
* [Acionador](#trigger)
* [Módulo](#module)
* [Rota](#route)
* [Segmento de cenário](#scenario-segment)
* [Conector &#x200B;](#connector)

### Cenário

Um **cenário** é uma série de etapas automatizadas criadas pelo usuário, criadas para mover e manipular dados. O termo &quot;cenário&quot; se refere a todo o grupo de etapas conectadas.

![Cenário](assets/entire-scenario-scenario.png)

### Acionador

Um cenário começa com um **acionador**. O acionador observa dados novos e atualizados e inicia o cenário quando determinadas condições configuradas no módulo são aplicadas. Os acionadores podem ser configurados para iniciar um cenário em um agendamento (pesquisa) ou sempre que ocorrerem alterações de dados (instantâneo).

![Acionador](assets/scenario-trigger.png)

### Módulo

O acionador é seguido por um número de **módulos**. Um módulo representa uma única etapa em um cenário que executa uma ação específica. Os módulos são configurados e encadeados para criar cenários.

![Módulo](assets/scenario-module.png)

### Rota

Um cenário pode ser dividido em **rotas**. Uma rota é uma seção do cenário que pode ou não ser usada para um determinado pacote de dados. As rotas são configuradas usando um módulo de roteador e filtros.

![Rota](assets/scenario-route.png)

### Segmento de cenário

Um segmento de cenário é uma seção de um cenário que consiste em uma série de módulos contíguos que se conectam ao mesmo aplicativo. Os segmentos de cenário geralmente representam um fluxo de trabalho curto no aplicativo.

![Segmento do cenário](assets/scenario-segment.png)

### Conector 

Um conector é o conjunto de módulos de um determinado aplicativo. O Workfront Fusion oferece conectores para muitos aplicativos de trabalho comuns, como Workfront, Salesforce e Jira, bem como conectores genéricos que podem ser usados para qualquer serviço da Web.

![Conectores](assets/scenario-connectors.png)

## Exemplos

Expanda as seções a seguir para exibir cenários de exemplo e suas explicações.

+++**Automatização de processos no Adobe Workfront**

O Workfront Fusion permite automatizar workflows simples ou complexos no Workfront, economizando tempo e garantindo que o processo seja executado de forma consistente.

Neste exemplo, o cenário é acionado quando um campo especificado é alterado em uma Tarefa ou Problema no Workfront. Quando acionado, o cenário obtém informações no projeto relacionado e cria uma atualização personalizada para uma pessoa atribuída a uma função específica no projeto.

![Exemplo de modelo](assets/fusion-template-example.png)

+++

+++**Conectando o Workfront a outro aplicativo ou serviço da Web**

>[!NOTE]
>
>Se sua organização usar o modelo de licenciamento herdado, ela deverá ter uma licença do Workfront Fusion for Work Automation and Integration para se conectar a outros aplicativos.

O Workfront Fusion pode se conectar a outros aplicativos e serviços Web. É possível acessar, importar, manipular ou exportar dados de outros aplicativos, integrando-os ao Workfront ou entre si.

Muitos aplicativos têm conectores dedicados do Workfront Fusion. Se não houver um conector dedicado para o aplicativo que deseja acessar, você poderá usar os módulos HTTP ou SOAP do Workfront Fusion para se conectar ao aplicativo por meio da API.

Neste exemplo, o cenário é acionado quando um usuário é adicionado a uma planilha do [!DNL Excel]. O cenário verifica se o usuário está no Workfront. Caso contrário, o cenário cria o usuário no Workfront e adiciona sua ID de usuário do Workfront de volta à planilha.

![Exemplo de integração](assets/fusion-integration-example.png)

Para obter uma lista de conectores dedicados, consulte [Referências de aplicativos Fusion e seus módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).


>[!IMPORTANT]
>
>O Adobe Workfront Fusion pode se conectar a quase qualquer serviço da Web. Se o aplicativo com o qual você deseja trabalhar não tiver um conector dedicado do Workfront Fusion, você poderá usar conectores universais para se conectar ao aplicativo ou serviço.
>
>Para obter uma lista de conectores universais, consulte [Conectores universais](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

+++

## Referências

* Para obter um glossário de termos usados no Workfront Fusion, consulte [glossário do Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).
* Para começar a criar um cenário de prática, consulte [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).
* Para obter informações sobre como criar e gerenciar cenários, consulte os artigos listados em:
   * [Criar cenários](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)
   * [Gerenciar cenários](/help/workfront-fusion/manage-scenarios/manage-scenarios-toc.md)
