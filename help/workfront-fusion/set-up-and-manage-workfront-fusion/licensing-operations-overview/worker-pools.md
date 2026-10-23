---
title: Pools de Trabalhadores
description: Um pool de trabalhadores é uma quantidade de recursos de processamento do Workfront Fusion dedicados a uma ou mais organizações específicas. Todas as operações e o processamento do Fusion ocorrem no contexto de um pool de trabalhadores atribuído de uma organização.
author: Becky
feature: Workfront Fusion
exl-id: 8bf508a8-d1f9-455f-af89-62f688289137
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: b800142d824927e5765eed50a831731e6b5d9925
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 19%
---
# Pools de trabalhadores

Um pool de trabalhadores é uma quantidade de recursos de processamento do Workfront Fusion dedicados a uma organização específica. Todas as operações e o processamento do Fusion ocorrem no contexto de um pool de trabalhadores atribuído de uma organização.

Os pools de trabalho permitem que seus cenários sejam executados com mais eficiência e eliminam as chances de competir com outras organizações para a capacidade de processamento do Fusion.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote do Adobe Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Os pacotes Workfront Prime e Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p><p>Trabalho ou maior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Visão geral do pool de trabalhadores

Um pool de trabalhadores é uma maneira de processar execuções de cenário em paralelo. Cada pool de trabalhadores está associado a:

* Vários trabalhadores.
* Uma fila de execução.

Quando um cenário é executado, ele passa para a fila de execução do pool de trabalhadores. Os funcionários no pool extraem continuamente as tarefas do pool de execução e as processam em paralelo.

Se a profundidade da fila de execução aumentar e todos os workers existentes estiverem sendo usados, o Workfront Fusion dimensionará automaticamente o pool adicionando mais workers. Esse dimensionamento é dinâmico e orientado por eventos, o que significa exatos de capacidade ou contratos com base na carga em tempo real sem a ação da sua empresa ou da sua organização.

A equipe do Workfront Fusion monitora continuamente a utilização e o comportamento de dimensionamento dos pools, e pode revisar limites ou padrões para garantir um desempenho consistente à medida que o uso cresce.

## Renomear um pool de trabalhadores

Os proprietários e administradores da organização podem renomear os grupos de trabalhadores atribuídos à organização. Cada pool mostra um nome gerado pelo sistema por padrão. Você pode dar um nome personalizado a um pool, como `Marketing EU` ou `High-volume integrations`, e alterá-lo sempre que precisar.

Renomear um pool altera apenas sua forma de rótulo. Cenários, execuções e capacidade do pool não são afetados. O novo nome aparece onde quer que o pool seja exibido, como quando você atribui cenários a um pool.

>[!NOTE]
>
>A guia **[!UICONTROL Pools de trabalhadores]** aparece somente quando mais de um pool de trabalhadores está atribuído à sua organização. Se sua organização tiver um único pool de trabalhadores ou usar o pool compartilhado, você não verá a guia.

Para renomear um pool de trabalhadores:

1. Na navegação à esquerda, clique em **Visão geral da organização**
1. Clique na guia **[!UICONTROL Pools de trabalhadores]**, próxima à parte superior da página.

   A guia lista cada pool e mostra quantos cenários estão atribuídos a ele.

1. Clique em **[!UICONTROL Renomear]** ao lado do pool que você deseja renomear.
1. No painel que é aberto, digite o novo nome.
1. Clique em **Salvar**.
