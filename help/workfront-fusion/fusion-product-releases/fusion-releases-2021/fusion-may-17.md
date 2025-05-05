---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Atividade de lançamento do Workfront Fusion: semana de 17 de maio de 2021'
description: Esta página descreve todas as melhorias feitas no Adobe Workfront Fusion na semana de 17 de maio de 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 2ea57c69-8db7-4500-9157-e2c2d8c74938
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Atividade de lançamento do Workfront Fusion: semana de 17 de maio de 2021

Esta página descreve todas as melhorias feitas no Adobe Workfront Fusion na semana de 17 de maio de 2021.

Para obter uma lista de todas as alterações recentes, consulte [atividade de versão do Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Para obter uma lista de correções de erros recentes no Workfront Fusion, consulte a página [Atualizações de Manutenção do Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=pt-BR) e verifique se há atualizações rotuladas como Atualização de Manutenção do Workfront Fusion.

## Copiar módulos em cenários do Workfront Fusion

Para facilitar o trabalho com os Cenários do Workfront Fusion, possibilitamos copiar e colar módulos. Agora é possível copiar um módulo ou grupo de módulos e colá-los no mesmo cenário ou em um diferente. A cópia de módulos preserva os valores de campo nesse módulo.


## Selecionar vários módulos em um cenário do Workfront Fusion

Agora, ao editar um cenário, é possível selecionar vários módulos de cada vez. Em seguida, é possível executar ações em massa nos módulos selecionados.

* Copiar
* Mover
* Excluir

Os módulos de cópia e movimentação preservam os valores do módulo e quaisquer linhas que os conectem.


## Os módulos agora preservam as informações não salvas

Para facilitar a criação de cenários, possibilitamos que os módulos preservem os valores de campo quando não estão em foco. Agora, ao clicar em um módulo sem salvá-lo e retornar a ele, os campos mostrarão os valores inseridos anteriormente. Quando o módulo é fechado, ele exibe um indicador de que há campos não salvos.

## O conector do Azure AD agora lida com registros novos e atualizados separadamente

Os novos registros e as atualizações dos registros existentes agora são manipulados por módulos separados.

* Para observar novos registros, você pode usar o módulo acionador Observar registros. Este módulo não observa mais os registros atualizados.
* Para obter registros atualizados, você pode usar o novo módulo Delta de Usuários/Grupos de Pesquisa. Este módulo retorna registros novos, atualizados e excluídos.
