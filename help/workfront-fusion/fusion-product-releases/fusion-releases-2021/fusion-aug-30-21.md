---
title: 'Atividade de lançamento do Workfront Fusion: semana de terça-feira, 30 de agosto de 2021'
description: 'Atividade de lançamento do Workfront Fusion: semana de terça-feira, 30 de agosto de 2021'
author: Luke
draft: Probably
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: cac11147-5b3d-477b-869b-e255528c4bec
source-git-commit: bc4c5c047f4847b929c4b047be1897d8872709e9
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 18%

---

# Atividade de lançamento do Workfront Fusion: semana de terça-feira, 30 de agosto de 2021

Esta página descreve todos os aprimoramentos realizados no Adobe Workfront Fusion na semana de terça-feira, 30 de agosto de 2021.

Para obter uma lista de todas as alterações recentes, consulte a [atividade de lançamento do Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Para obter uma lista de correções de erros recentes no Workfront Fusion, consulte a página [Atualizações de manutenção do Workfront](https://experienceleague.adobe.com/pt-br/docs/workfront-known-issues/releases/current-updates) e verifique se há atualizações rotuladas como atualização de manutenção do Workfront Fusion.

## Filtrar eventos que acionam o módulo Workfront > Eventos de observação

1. Configure um filtro personalizado para eventos que acionam o módulo Workfront > Eventos de observação

   Para reduzir o número de execuções de cenários desnecessários, atualizamos o módulo Workfront > Registros de observação para ativar a filtragem de eventos. Agora, você pode definir um filtro ao criar um webhook. Isso permite que o cenário seja acionado somente quando o evento atender a determinados critérios.

   Atualmente, o filtro de eventos oferece as seguintes operações:

   * Igual: acione um cenário somente quando um evento corresponder às condições do filtro. Por exemplo, você pode configurar um filtro que aciona um cenário somente se o evento ocorrer em um projeto específico.
   * Diferente: acione um cenário somente se um evento não corresponder às condições do filtro. Por exemplo, você pode criar um filtro que aciona um cenário somente se o problema em que um evento ocorre não tiver um status Fechado.

   Anteriormente, o módulo Observar registros recuperava todos os registros. Os usuários só podem filtrar configurando filtros posteriormente no cenário.

   Para aproveitar a filtragem de eventos, crie um novo webhook no módulo Observar eventos. No momento, não é possível editar webhooks existentes para incluir essa funcionalidade. É altamente recomendável criar novos webhooks usando filtros de evento para seus cenários existentes.

1. Filtrar eventos acionados pela conexão atual.

   Para facilitar a configuração dos webhooks no módulo Workfront > Eventos de observação, incluímos o filtro de eventos mais comum. Agora, o webhook tem uma opção para filtrar todas as alterações feitas pelos módulos usando a conexão especificada para o módulo Observar eventos. Em outras palavras, com esse filtro ativado, qualquer alteração feita pelo usuário do Workfront associado a essa conexão não poderá acionar o cenário.

   Anteriormente, esse filtro não estava disponível. Portanto, foi mais fácil para as alterações feitas nos módulos do Workfront acionarem cenários que contêm esses módulos, potencialmente fazendo com que os cenários se acionassem em um loop infinito.
