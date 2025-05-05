---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Atividade de lançamento do Workfront Fusion: semana de 3 de maio de 2021'
description: Esta página descreve todas as melhorias feitas no Adobe Workfront Fusion na semana de 3 de maio de 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Atividade de lançamento do Workfront Fusion: semana de 3 de maio de 2021

Esta página descreve todas as melhorias feitas no Adobe Workfront Fusion na semana de 3 de maio de 2021.

Para obter uma lista de todas as alterações recentes, consulte [atividade de versão do Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Para obter uma lista de correções de erros recentes no Workfront Fusion, consulte a página [Atualizações de Manutenção do Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=pt-BR) e verifique se há atualizações rotuladas como Atualização de Manutenção do Workfront Fusion.

## O conector do Salesforce agora pode pesquisar usando SOQL

O módulo Salesforce > Pesquisar registros agora tem a opção de pesquisar usando SOQL (Salesforce Object Query Language). Também é possível pesquisar usando as opções disponíveis anteriormente (pesquisas simples e SOSL).

## O novo tipo de conexão no conector DevOps do Azure requer menos escopos

Para aprimorar a segurança, adicionamos um novo tipo de conector ao Conector DevOps do Workfront Fusion Azure. Agora, ao criar uma conexão em um módulo DevOps do Azure, você pode selecionar entre dois tipos de conexões:

* DevOps do Azure

  Esse novo tipo de conexão limita escopos àqueles especificamente necessários para o Workfront Fusion.

* DevOps do Azure (Solicitar todos os escopos)

  Este é o tipo de conexão herdado, que solicita todos os escopos disponíveis em uma conexão com o Azure DevOps.

Recomendamos que você use o tipo de conexão DevOps do Azure em todos os seus novos cenários que usam DevOps do Azure. Também recomendamos que você altere quaisquer módulos DevOps do Azure em seus cenários existentes para usar o novo tipo de conexão. O tipo de conexão Azure DevOps herdado (Solicitar todos os escopos) será descontinuado em breve.
