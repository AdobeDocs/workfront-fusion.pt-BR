---
title: Perguntas frequentes sobre planejamento de cenário
description: As informações neste artigo podem ser úteis quando você começar a criar cenários no Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6a1d672d-0bd7-4a3a-b96d-6d8b4c97522d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 1%

---

# Perguntas frequentes sobre planejamento de cenário

As informações neste artigo podem ser úteis quando você começar a criar cenários no Workfront Fusion.

## O que é um cenário?

### Responder

Um cenário define uma sequência de etapas a serem executadas pelo Adobe Workfront Fusion. Para cada cenário, você especifica a fonte de dados, quais dados usar e como os dados devem ser processados. O Fusion permite criar cenários simples ou complexos, capazes de atender aos casos de uso da sua organização.

Para obter mais informações sobre cenários, consulte [Visão geral do cenário](/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md).

## Quantos módulos posso usar em um cenário?

### Responder

Você pode usar quantos módulos desejar em um cenário. Você pode separar módulos em rotas e pode especificar quais dados devem fluir em cada rota. Você também pode usar a saída de um módulo como entrada para outro módulo.

Embora não haja limite para o número de módulos em um cenário, mais de 150 módulos podem afetar o desempenho do cenário.

Para obter mais informações sobre módulos, consulte [Visão geral do módulo](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).

## [!DNL Workfront Fusion] pode trabalhar com arquivos?

### Responder

Sim. O Workfront Fusion pode receber, salvar, transformar, converter e criptografar arquivos. O Fusion também oferece uma ampla variedade de recursos integrados, projetados para permitir que os usuários trabalhem de forma eficaz e criativa com os dados contidos nos arquivos.

Para obter mais informações sobre como trabalhar com arquivos no Fusion, consulte [Mapear um arquivo entre módulos](/help/workfront-fusion/create-scenarios/map-data/map-files.md).

## Alguns acionadores permitem que os cenários sejam executados instantaneamente. O que significa &quot;instantaneamente&quot;?

### Responder

Os cenários podem ser executados em intervalos de acordo com o agendamento especificado, por exemplo, a cada hora ou a cada 5 minutos. Há acionadores especiais, chamados de acionadores instantâneos (webhooks), que podem iniciar seu cenário imediatamente após receberem dados de um determinado serviço. O Fusion processa os dados recebidos imediatamente, sem esperar a próxima execução programada.

Para obter mais informações sobre a diferença entre acionadores sondados e instantâneos, consulte [Módulos de acionador](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) no artigo Visão geral do módulo.

## O que é uma operação?

### Responder

Uma operação é qualquer tarefa executada por um módulo. Uma operação ocorre, por exemplo, toda vez que um acionador é executado e toda vez que uma ação executa uma tarefa.

Alguns planos do Fusion são baseados no número de operações que sua organização utiliza.

Para obter mais informações sobre operações, consulte [Operações](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

## O que é transferência de dados?

### Responder

Transferência de dados refere-se à quantidade de dados transferidos pelo seu cenário. Por exemplo, um cenário que recupera uma imagem de 100 KB do Workfront e, em seguida, carrega a imagem em um provedor de armazenamento de documentos. A quantidade de dados usada nesse cenário é de 200 KB.

## O que é uma conexão?

### Responder

Uma conexão é o vínculo entre sua conta do [!DNL Workfront Fusion] e o serviço de terceiros que você deseja usar. A conexão pode ser criada ao editar um cenário.

Para obter mais informações, consulte [Visão geral da conexão](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

## O que são agregadores?

### Responder

Um [!UICONTROL Aggregator] mescla dados em uma única coleção. Um exemplo disso são arquivos compactados em um arquivo zip e enviados como um anexo de email.

Para obter mais informações, consulte [[!UICONTROL Aggregator] módulo](/help/workfront-fusion/references/modules/aggregator-module.md).

## O que acontece se eu permitir que o [!DNL Workfront Fusion] processe um email contendo mais de um anexo?

### Responder

Se você usar o módulo [!UICONTROL Email] [!UICONTROL Retrieve attachments], cada anexo será enviado individualmente através do restante dos módulos no cenário. Módulos semelhantes também estão disponíveis em outros aplicativos que recebem vários arquivos de uma só vez.
