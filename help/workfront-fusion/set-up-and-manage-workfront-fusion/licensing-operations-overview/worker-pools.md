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
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%
---
# Pools de trabalhadores

Um pool de trabalhadores é uma quantidade de recursos de processamento do Workfront Fusion dedicados a uma organização específica. Todas as operações e o processamento do Fusion ocorrem no contexto de um pool de trabalhadores atribuído de uma organização.

Os pools de trabalho permitem que seus cenários sejam executados com mais eficiência e eliminam as chances de competir com outras organizações para a capacidade de processamento do Fusion.

## Visão geral do pool de trabalhadores

Um pool de trabalhadores é uma maneira de processar execuções de cenário em paralelo. Cada pool de trabalhadores está associado a:

* Vários trabalhadores.
* Uma fila de execução.

Quando um cenário é executado, ele passa para a fila de execução do pool de trabalhadores. Os funcionários no pool extraem continuamente as tarefas do pool de execução e as processam em paralelo.

Se a profundidade da fila de execução aumentar e todos os workers existentes estiverem sendo usados, o Workfront Fusion dimensionará automaticamente o pool adicionando mais workers. Esse dimensionamento é dinâmico e orientado por eventos, o que significa exatos de capacidade ou contratos com base na carga em tempo real sem a ação da sua empresa ou da sua organização.

A equipe do Workfront Fusion monitora continuamente a utilização e o comportamento de dimensionamento dos pools, e pode revisar limites ou padrões para garantir um desempenho consistente à medida que o uso cresce.
