---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Atividade de lançamento do Workfront Fusion: semana de 3 de maio de 2021'
description: Esta página descreve todos os aprimoramentos realizados no Adobe Workfront Fusion na semana de terça-feira, 3 de maio de 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
TQID: https://experienceleague.adobe.com/GZ5W-9Q1Y9M-cCVN1CupZVs8GuQPy4Dusifz-5sxJm8
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 35%

---

# Atividade de lançamento do Workfront Fusion: semana de 3 de maio de 2021

Esta página descreve todos os aprimoramentos realizados no Adobe Workfront Fusion na semana de terça-feira, 3 de maio de 2021.

Para obter uma lista de todas as alterações recentes, consulte a [atividade de lançamento do Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Para obter uma lista de correções de erros recentes no Workfront Fusion, consulte a página [Atualizações de manutenção do Workfront](https://experienceleague.adobe.com/pt-br/docs/workfront-known-issues/releases/current-updates) e verifique se há atualizações rotuladas como atualização de manutenção do Workfront Fusion.

## O conector do Salesforce agora pode pesquisar usando SOQL

O módulo Salesforce > Pesquisar registros agora tem a opção de pesquisar usando SOQL (Salesforce Object Query Language). Também é possível pesquisar usando as opções disponíveis anteriormente (pesquisas simples e SOSL).

## O novo tipo de conexão no conector DevOps do Azure requer menos escopos

Para aprimorar a segurança, adicionamos um novo tipo de conector ao Conector DevOps do Workfront Fusion Azure. Agora, ao criar uma conexão em um módulo DevOps do Azure, você pode selecionar entre dois tipos de conexões:

* DevOps do Azure

  Esse novo tipo de conexão limita escopos àqueles especificamente necessários para o Workfront Fusion.

* Azure DevOps (Solicitar todos os escopos)

  Este é o tipo de conexão herdado, que solicita todos os escopos disponíveis em uma conexão com o Azure DevOps.

Recomendamos que você use o tipo de conexão Azure DevOps em todos os novos cenários que usam Azure DevOps. Também recomendamos que você altere qualquer módulo do Azure DevOps em seus cenários existentes para usar o novo tipo de conexão. O tipo de conexão Azure DevOps herdado (Solicitar todos os escopos) será descontinuado em breve.
