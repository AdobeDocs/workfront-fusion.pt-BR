---
title: Funções de matriz
description: As seguintes funções de matriz estão disponíveis no painel de mapeamento do Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 16c3915c-add1-4aab-a0e1-75fc590c42a6
source-git-commit: 9b61a3b18df1f755cc7ccc28889564e4bcb6cda0
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Funções de matriz

## [!UICONTROL junção (matriz; separador)]

Concatena todos os itens de uma matriz em uma cadeia de caracteres, usando o separador especificado entre cada item.

## [!UICONTROL comprimento (matriz)]

Retorna o número de itens em uma matriz.

## [!UICONTROL chaves (objeto)]

Retorna uma matriz das propriedades de um determinado objeto ou matriz.

## [!UICONTROL fatia (matriz; início; [fim])]

Retorna uma nova matriz contendo apenas itens selecionados.

## [!UICONTROL mesclar (matriz1; matriz2; ...)]

Mescla uma ou mais matrizes em uma matriz.

## [!UICONTROL contém (matriz; valor)]

Verifica se uma matriz contém o valor.

## [!UICONTROL remover (matriz; valor1; valor2; ...)]

Remove valores especificados nos parâmetros de uma matriz. Esta função só é eficaz em matrizes primitivas de texto ou números.

## [!UICONTROL adicionar (matriz; valor1; valor2; ...)]

Adiciona valores especificados em parâmetros a uma matriz e retorna essa matriz.

## [!UICONTROL mapa (matriz complexa; chave;[chave para filtragem];[valores possíveis para filtragem])]

Retorna uma matriz primitiva contendo valores de uma matriz complexa. Esta função permite filtrar valores. Use nomes de variáveis brutos para chaves.

>[!BEGINSHADEBOX]

**Exemplos:**

* `map(Emails[];email)`

  Retorna uma matriz primitiva com emails

* `map(Emails[];email;label;work)`

  Retorna uma matriz primitiva com emails com um rótulo igual a trabalho

>[!ENDSHADEBOX]

Para obter mais informações, consulte [Mapear uma matriz ou elemento de matriz](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).

## ordem aleatória

## [!UICONTROL classificar (matriz; [ordem]; [chave])]

Classifica os valores de uma matriz. Os valores válidos do parâmetro `order` são:

* `asc`

  (padrão) - ordem crescente: 1, 2, 3, ... para o tipo Número. A, B, C, a, b, c, ... para texto

* `desc`

  ordem decrescente: ..., 3, 2, 1 para o tipo Number. ..., c, b, a, C, B, A para texto.

* `asc ci`

  ordem crescente que não diferencia maiúsculas de minúsculas: A, a, B, b, C, c, ... para o tipo Text.

* `desc ci`

  ordem decrescente que não diferencia maiúsculas de minúsculas: ..., C, c, B, b, A, a para tipo de Texto.

Use o parâmetro `key` para acessar propriedades dentro de objetos complexos.

Use nomes de variáveis brutos para chaves.

Para acessar propriedades aninhadas, use a notação de pontos.

O primeiro item em uma matriz é o índice 1.

>[!BEGINSHADEBOX]

**Exemplos:**

* `sort(Contacts[];name)`

  Classifica uma matriz de contatos pela propriedade &quot;name&quot; em ordem crescente padrão

* `sort(Contacts[];desc;name)`

  Classifica uma matriz de contatos pela propriedade &quot;name&quot; em ordem descendente

* `sort(Contacts[];asc ci;name)`

  Classifica uma matriz de contatos pela propriedade &quot;name&quot; em ordem crescente que não diferencia maiúsculas de minúsculas

* `sort(Emails[];sender.name)`

  Classifica uma matriz de emails pela propriedade &quot;sender.name&quot;

>[!ENDSHADEBOX]

## [!UICONTROL inverter (matriz)]

O primeiro elemento da matriz se torna o último elemento, o segundo se torna o próximo ao último e assim por diante.

## [!UICONTROL nivelar (matriz)]

Cria uma nova matriz com todos os elementos de submatriz concatenados nela, recursivamente, até a profundidade especificada.

## [!UICONTROL distinct (matriz; [chave])]

Remove duplicatas dentro de uma matriz. Use o argumento &quot;[!UICONTROL key]&quot; para acessar propriedades dentro de objetos complexos. Para acessar propriedades aninhadas, use a notação de pontos. O primeiro item em uma matriz é o índice 1.

>[!BEGINSHADEBOX]

**Exemplo:** `distinct(Contacts[];name)`

Remove duplicatas dentro de uma matriz de contatos comparando a propriedade &quot;name&quot;

>[!ENDSHADEBOX]

## toCollection

* Esta função pega uma matriz que contém pares de valores chave e a converte em uma coleção. Há 3 argumentos para a função:

* (matriz) contendo pares de valores chave
* (string) o nome do campo a ser usado como chave
* (string) o nome do campo a ser usado como valor

>[!BEGINSHADEBOX]

Exemplo:

Dada uma matriz:

```
[{"name":"Bob", "age":22}, {"name":"Tim", "age":23}]
```

e argumentos

```
{{toCollection(6.array; "name"; "age")}}
```

a função retorna

```
{
    "Bob": 22,
    "Tim": 23
}
```

>[!ENDSHADEBOX]

## toArray

Esta função converte uma coleção em uma matriz de pares de valores chave.

>[!BEGINSHADEBOX]

**Exemplos:**

Dada a coleção

`{ key1: "value1", key2: "value2:}`

A função

`toArray({ key1: "value1", key2: "value2:})`

Retorna a matriz de pares de valores chave

`[{ key1: "value1"}, { key2: "value2"}]`

>[!ENDSHADEBOX]

## [!UICONTROL arrayDifference [array1, array2, modo]]

Retorna a diferença entre duas matrizes.

Insira um dos seguintes valores para o parâmetro `mode`.

* `classic`: retorna uma nova matriz que contém todos os elementos de `array1` que não existem em `array2`.

* `symmetric`: retorna uma matriz de elementos que não são comuns a ambas as matrizes.

  Em outras palavras, a função retorna uma matriz que contém todos os elementos de `array1` que não existem em `array2` e todos os elementos de `array2` que não existem em `array1`.

>[!BEGINSHADEBOX]

**Exemplos:**

Considerando as seguintes matrizes:

```
myArray = [1,2,3,4,5]
```

```
yourArray = [3,4,5,6,7]
```

* `arrayDifference [myArray, yourArray, classic]`

  Retorna `[1,2]`

* `arrayDifference [yourArray, myArray, classic]`

  Retorna `[6,7]`

* `arrayDifference [myArray, yourArray, symmetric]`

  Retorna `[1,2,6,7]`

>[!ENDSHADEBOX]

## desduplicar

## Palavras-chave

## emptyarray
