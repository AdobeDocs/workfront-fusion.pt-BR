---
title: Funções matemáticas
description: As seguintes funções matemáticas estão disponíveis no painel Mapeamento do Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: e11e581c092ebba343a0f2d6943ecbe4d0fe4c87
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 6%

---

# Funções matemáticas

## [!UICONTROL média ([matriz de valores]) média(valor1; [valor2], ...)]

Retorna o valor médio dos valores numéricos em uma matriz específica ou o valor médio dos valores numéricos inseridos individualmente.

## [!UICONTROL ceil (número)]

Retorna o menor inteiro maior ou igual a um número especificado.

>[!BEGINSHADEBOX]

**Exemplos:**

* `ceil(` `1.2` `)`

  Devoluções 2

* `ceil(` `4` `)`

  Devoluções 4

>[!ENDSHADEBOX]

## [!UICONTROL andar (número)]

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

## [!UICONTROL max ([matriz de valores]), max(valor1;valor2; ...)]

Retorna o maior número em uma matriz especificada ou o maior número entre os números inseridos individualmente.

## [!UICONTROL min ([matriz de valores]), min(valor1; valor2; ...)]

Retorna o menor número em uma matriz especificada ou o menor número entre os números inseridos individualmente.

## [!UICONTROL round (número)]

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

## [!UICONTROL soma ([matriz de valores]), soma(valor1; valor2; ...)]

Retorna a soma dos valores em uma matriz especificada ou a soma dos números inseridos individualmente.

## [!UICONTROL parseNumber (número; separador decimal)]

Analisa uma string com um número e retorna o número. Por exemplo, parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (número; pontos decimais; [separadorDecimal]; [separadorMilhares])]

Retorna um número no formato solicitado. Por padrão, o ponto decimal é uma vírgula (,) e o separador de milhares é um ponto (.).

>[!BEGINSHADEBOX]

**Exemplo:**

`formatNumber( 123456789 ; 3 ; , ; . )`

Retorna 123.456.789.000

>[!ENDSHADEBOX]

### [!UICONTROL ab(número)]

[!BADGE Novo!]{type=Informative}

Retorna o valor absoluto de um número.

>[!BEGINSHADEBOX]

**Exemplo:**

* `abs(-3.14)`

  Retorna 3,14
* `abs(3.14)`

  Retorna 3,14


### [!UICONTROL div(número1; número2; ...)]

[!BADGE Novo!]{type=Informative}

Divide todos os números na ordem informada.

>[!BEGINSHADEBOX]

**Exemplo:**

* `div(10; 2)`

  Devoluções 5
* `div(100; 5; 4)`

  Devoluções 5


### [!UICONTROL ln(número)]

[!BADGE Novo!]{type=Informative}

Retorna o logaritmo natural do número.


>[!BEGINSHADEBOX]

**Exemplo:**

* `ln(1)`

  Retorna 0
* `ln(2.718281828)`

  Devoluções 1


### [!UICONTROL log(número1; número2)]

[!BADGE Novo!]{type=Informative}

Retorna o logaritmo de `number2` à base `number1`.

>[!BEGINSHADEBOX]

**Exemplo:**

* `log(10; 100)`

  Devoluções 2
* `log(2; 8)`

  Devoluções 3


### [!UICONTROL número(sequência)]

[!BADGE Novo!]{type=Informative}

Converte uma cadeia de caracteres em número.

>[!BEGINSHADEBOX]

**Exemplo:**

* `number("3.14")`

  Retorna 3,14
* `number("42")`

  Retorna 42


### [!UICONTROL potência(número; potência)]

[!BADGE Novo!]{type=Informative}

Retorna um número elevado à potência especificada.

>[!BEGINSHADEBOX]

**Exemplo:**

* `power(2; 3)`

  Devoluções 8
* `power(4; 0.5)`

  Devoluções 2


### [!UICONTROL prod(número1; número2; ...)]

[!BADGE Novo!]{type=Informative}

Multiplica todos os números fornecidos.

>[!BEGINSHADEBOX]

**Exemplo:**

* `prod(2; 3; 4)`

  Retorna 24
* `prod(5; 5)`

  Retorna 25


### [!UICONTROL sortAscNum(number1; number2; ...)]

[!BADGE Novo!]{type=Informative}

Retorna os números fornecidos em ordem crescente.

>[!BEGINSHADEBOX]

**Exemplo:**

* `sortAscNum(3; 1; 2)`

  Retorna \[1, 2, 3]
* `sortAscNum(5; 3; 4)`

  Retorna \[3, 4, 5]


### [!UICONTROL sortDescNum(number1; number2; ...)]

[!BADGE Novo!]{type=Informative}

Retorna os números fornecidos em ordem decrescente.

>[!BEGINSHADEBOX]

**Exemplo:**

* `sortDescNum(3; 1; 2)`

  Retorna \[3, 2, 1]
* `sortDescNum(5; 3; 4)`

  Retorna \[5, 4, 3]


### [!UICONTROL sqrt(número)]

[!BADGE Novo!]{type=Informative}

Retorna a raiz quadrada de um número.

>[!BEGINSHADEBOX]

**Exemplo:**

* `sqrt(9)`

  Devoluções 3
* `sqrt(4)`

  Devoluções 2


### [!UICONTROL sub(número1; número2; ...)]

[!BADGE Novo!]{type=Informative}

Subtrai todos os números na ordem informada.

>[!BEGINSHADEBOX]

**Exemplo:**

* `sub(10; 3; 2)`

  Devoluções 5
* `sub(20; 5)`

  Retorna 15
