---
title: Funções matemáticas
description: As seguintes funções matemáticas estão disponíveis no painel Mapeamento do Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Funções matemáticas

## [!UICONTROL average ([array of values]) average(value1; [value2], ...)]

Retorna o valor médio dos valores numéricos em uma matriz específica ou o valor médio dos valores numéricos inseridos individualmente.

## [!UICONTROL ceil (number)]

Retorna o menor inteiro maior ou igual a um número especificado.

>[!BEGINSHADEBOX]

**Exemplos:**

* `ceil(` `1.2` `)`

  Devoluções 2

* `ceil(` `4` `)`

  Devoluções 4

>[!ENDSHADEBOX]

## [!UICONTROL floor (number)]

Retorna o maior inteiro menor ou igual a um número especificado.

>[!BEGINSHADEBOX]

**Exemplos:**

* `floor(` `1.2` `)`

  Devoluções 1

* `floor(` `1.9` `)`

  Devoluções 1

* `floor(` `4` `)`

  Devoluções 4

>[!ENDSHADEBOX]

## [!UICONTROL max ([array of values]), max(value1;value2; ...)]

Retorna o maior número em uma matriz especificada ou o maior número entre os números inseridos individualmente.

## [!UICONTROL min ([array of values]), min(value1; value2; ...)]

Retorna o menor número em uma matriz especificada ou o menor número entre os números inseridos individualmente.

## [!UICONTROL round (number)]

Arredonda um valor numérico para o número inteiro mais próximo.

>[!BEGINSHADEBOX]

**Exemplos:**

* `round(` `1.2` `)`

  Devoluções 1

* `round(` `1.5` `)`

  Devoluções 2

* `round(` `1.7` `)`

  Devoluções 2

* `round(` `2` `)`

  Devoluções 2

>[!ENDSHADEBOX]

## [!UICONTROL sum ([array of values]), sum(value1; value2; ...)]

Retorna a soma dos valores em uma matriz especificada ou a soma dos números inseridos individualmente.

## [!UICONTROL parseNumber (number; decimal separator)]

Analisa uma string com um número e retorna o número. Por exemplo, parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

Retorna um número no formato solicitado. Por padrão, o ponto decimal é uma vírgula (,) e o separador de milhares é um ponto (.).

>[!BEGINSHADEBOX]

**Exemplo:**

`formatNumber( 123456789 ; 3 ; , ; . )`

Retorna 123.456.789.000

>[!ENDSHADEBOX]
