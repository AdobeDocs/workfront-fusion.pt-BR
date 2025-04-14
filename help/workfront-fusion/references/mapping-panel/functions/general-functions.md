---
title: Funções gerais
description: As seguintes funções gerais estão disponíveis no painel Mapeamento do Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: 295004ab7536b85124bc366d6832c08365338d08
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Funções gerais

## Variáveis

Há duas variáveis gerais que podem ser usadas para identificar detalhes sobre uma execução:

* `executionID`: a ID de execução deste cenário
* `triggerTimestamp`: a hora em que essa execução foi disparada

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
