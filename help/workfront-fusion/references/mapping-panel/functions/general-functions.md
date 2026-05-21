---
title: Funções gerais
description: As seguintes funções gerais estão disponíveis no painel Mapeamento do Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
TQID: https://experienceleague.adobe.com/1IX25ZtrWVizi5gZJfFw-acnW5eIuXpGgcXgXW0T-Hw
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 478
ht-degree: 6%

---

# Funções gerais

## Variáveis

Você pode usar essas variáveis gerais para identificar detalhes sobre uma execução:

* `executionID`: a ID de execução deste cenário
* `triggerTimestamp`: a hora em que essa execução foi disparada
* `scenarioID`: o ID do cenário em execução no momento
* `scenarioName`: o nome do cenário em execução
* `operationsConsumed`: o número de operações usadas nesse ponto do cenário.

## [!UICONTROL obter (objeto ou matriz; caminho)]

Retorna o caminho do valor de um objeto ou matriz. Para acessar objetos aninhados, use a notação de pontos. O primeiro item em uma matriz é o índice 1.

>[!BEGINSHADEBOX]

**Exemplos:**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (expressão; valor1; valor2)]

Retorna `value1` se a expressão for avaliada como verdadeira; caso contrário, retorna `value2`.

Para criar uma instrução if que retorne um valor somente se duas ou mais expressões forem avaliadas como true, use a palavra-chave `and`.

Para combinar instruções `if`, use os operadores `and` e `or`.

![e operador](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**Exemplos:**

* `if( 1 = 1 ; A ; B )`

  Retorna A

* `if( 1 = 2 ; A ; B )`

  Devoluções B

* `if( 1 = 2 and 1 = 2 ; A ; B )`

  Devoluções B

>[!ENDSHADEBOX]

## [!UICONTROL ifempty (value1; value2)]

Retorna `value1` se este valor não estiver vazio; caso contrário, retorna `value2`.

>[!BEGINSHADEBOX]

**Exemplos:**

* `ifempty(` `A` `;` `B` )

  Retorna A

* `ifempty(` `unknown` `;` `B` )

  Devoluções B

* `ifempty(` `""` `;` `B` )

  Devoluções B

>[!ENDSHADEBOX]

## [!UICONTROL opção (expressão; valor1; resultado1; [valor2; resultado2; ...]; [outra])]

Avalia um valor (chamado de expressão) em relação a uma lista de valores; retorna o resultado correspondente ao primeiro valor correspondente. Para incluir um valor `else`, adicione-o depois da expressão ou valor final.

>[!BEGINSHADEBOX]

**Exemplos:**

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

  Devoluções 2

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

  Devoluções 3

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

  Devoluções 4

  Nesta função, 4 é o valor a ser retornado se nenhuma expressão se aplicar (o valor `else`).

>[!ENDSHADEBOX]

## [!UICONTROL omit(object; key1; [key2; ...])]

Omite as chaves fornecidas do objeto e retorna o restante.

>[!BEGINSHADEBOX]

**Exemplo:**

`omit(` Usuário `;` senha `)`

Retorna uma coleção das informações do usuário, excluindo a senha.

>[!ENDSHADEBOX]

## [!UICONTROL pick(object; key1; [key2; ...])]

Seleciona somente as chaves fornecidas do objeto.

>[!BEGINSHADEBOX]

**Exemplo:**

`pick(` Usuário `;` senha `;` email `)`

Retorna uma coleção somente da senha e do endereço de email do usuário.

>[!ENDSHADEBOX]

## mergeCollections( coleção1; coleção2)

Mescla duas coleções combinando seus pares de valor chave. Se ambas as coleções contiverem a mesma chave, o valor da segunda coleção substituirá esse valor da primeira coleção.

### [!UICONTROL isBlank(value)]

Retorna `true` se o valor for `null` ou uma cadeia de caracteres vazia; caso contrário, retorna `false`. Ao contrário de `ifEmpty`, esta função não trata o número `0` ou cadeias de caracteres com somente espaços em branco como espaços em branco.

>[!BEGINSHADEBOX]

**Exemplo:**

* `isBlank("")     `

  Retorna verdadeiro
* `isBlank(null)   `

  Retorna verdadeiro
* `isBlank("Hello")`

  Retorna falso
* `isBlank(0)      `

  Retorna falso
* `isBlank(" ")    `

  Retorna falso

>[!ENDSHADEBOX]


### [!UICONTROL in(valor; valor1; valor2; ...)]

Retorna `true` se o valor for igual a um dos valores fornecidos (igualdade estrita, sem coerção de tipo).

>[!BEGINSHADEBOX]

**Exemplo:**

* `in("B"; "A"; "B"; "C")`

  Retorna verdadeiro
* `in("D"; "A"; "B"; "C")`

  Retorna falso
* `in(2; 1; 2; 3)        `

  Retorna verdadeiro
* `in("2"; 1; 2; 3)      `

  Retorna falso

>[!ENDSHADEBOX]

### [!UICONTROL ifin(valor; valor1; valor2; ...; expressãoVerdadeira; expressãoFalsa)]

Retorna `trueExpression` se o valor corresponder a qualquer um dos valores de correspondência fornecidos; caso contrário, retorna `falseExpression`. Exige pelo menos 3 argumentos (valor, um valor de correspondência e trueExpression + falseExpression).

>[!BEGINSHADEBOX]

**Exemplo:**

* `ifin("B"; "A"; "B"; "yes"; "no")`

  Retorna sim
* `ifin("D"; "A"; "B"; "yes"; "no")`

  Retorna não
* `ifin("X"; "X"; "found"; "not found")`

  Retornos encontrados

>[!ENDSHADEBOX]

### [!UICONTROL case(número_do_índice; value1; value2; ...)]

Retorna o valor na posição especificada pelo número do índice (com base em 1). Retorna `null` se o índice estiver fora dos limites ou for 0.

>[!BEGINSHADEBOX]

**Exemplo:**

* `case(1; "Sun"; "Mon"; "Tue")`

  Retorna Sun
* `case(2; "Sun"; "Mon"; "Tue")`

  Retorna Seg
* `case(3; "Sun"; "Mon"; "Tue")`

  Retorna verdadeiro
* `case(5; "a"; "b")           `

  Retorna nulo

>[!NOTE]
>
>Recomendamos usar para obter o nome do dia de uma data:
>`case(dayOfWeek(date); "Sun"; "Mon"; "Tue"; "Wed"; "Thu"; "Fri"; "Sat")`

>[!ENDSHADEBOX]

