---
title: Funções de string
description: As seguintes funções de string estão disponíveis no painel de mapeamento do Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: d3e49fce-85bc-4ee6-9a94-497a306e0c74
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# Funções de string

## [!UICONTROL length (text or buffer)]

Retorna o tamanho da string de texto (número de caracteres) ou do buffer binário (tamanho do buffer em bytes).

>[!BEGINSHADEBOX]

**Exemplo:**

`length( hello )`

Devoluções: 5

>[!ENDSHADEBOX]

## [!UICONTROL lower (text)]

Converte todos os caracteres alfabéticos em uma cadeia de texto em minúsculas.

>[!BEGINSHADEBOX]

**Exemplo:**

`lower( Hello )`

Retorna: olá

>[!ENDSHADEBOX]

## [!UICONTROL capitalize (text)]

Converte o primeiro caractere em uma cadeia de texto em maiúsculas.

>[!BEGINSHADEBOX]

**Exemplo:**

`capitalize( workfront )`

Devoluções: [!DNL Workfront]

>[!ENDSHADEBOX]

## [!UICONTROL startcase (text)]

Coloca a primeira letra de cada palavra em maiúscula e coloca em minúscula todas as outras letras.

>[!BEGINSHADEBOX]

**Exemplo:**
`startcase( hello WORLD )`

Devoluções: [!UICONTROL Hello World]

>[!ENDSHADEBOX]

## [!UICONTROL ascii (text; [remove diacritics])]

Remove todos os caracteres não ascii de uma cadeia de texto.

>[!BEGINSHADEBOX]

**Exemplos:**

* `ascii(` `Wěošrčkřfžrýoáníté` `)`

Devoluções: [!DNL Workfront]

* `ascii(` `ěščřž` `;` `true` `)`

Devoluções: [!UICONTROL escrz]

>[!ENDSHADEBOX]

## [!UICONTROL replace (text;search string; replacement string)]

Substitui a cadeia de caracteres de pesquisa pela nova cadeia.

>[!BEGINSHADEBOX]

**Exemplo:**

`replace( Hello World ; Hello ; Hi )`

Devoluções: [!UICONTROL Hi World]

>[!ENDSHADEBOX]

Expressões regulares (entre `/.../`) podem ser usadas como cadeia de caracteres de pesquisa com uma combinação de sinalizadores (como `g`, `i`, `m`) adicionados:

>[!BEGINSHADEBOX]

**Exemplo:**

![Substituir](assets/replace---1-350x31.png)

Todos estes números X X X X são substituídos por X

>[!ENDSHADEBOX]

A sequência de caracteres de substituição pode incluir os seguintes padrões de substituição especiais:

* `$&` Insere a subcadeia de caracteres correspondente.
* `$n` Onde n é um inteiro positivo menor que 100, insere a enésima cadeia de caracteres de subcorrespondência entre parênteses. Isso é indexado com 1.

>[!BEGINSHADEBOX]

**Exemplos:**

![Valor da variável](assets/variable-value-350x63.png)

Retorna: número de telefone `+420777111222`

![Retorno de variável](assets/variable-value---2-350x55.png)

Retorna: Telefone: `+420777111222`

>[!CAUTION]
>
>Não use grupos de captura nomeados, como `/ is (?<number>\d+)/`, no argumento de cadeia de caracteres de substituição. Isso resulta em um erro.


>[!ENDSHADEBOX]

Para obter mais informações sobre expressões regulares, consulte [Analisador de texto](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/text-parser.md).

## [!UICONTROL trim (text)]

Remove caracteres de espaço no início ou no fim do texto.

## [!UICONTROL upper (text)]

Converte todos os caracteres alfabéticos em uma cadeia de texto em maiúsculas.

>[!BEGINSHADEBOX]

**Exemplo:**

`upper( Hello )`

Devoluções: [!UICONTROL HELLO]

>[!ENDSHADEBOX]

## [!UICONTROL substring (text; start;end)]

Retorna uma parte de uma cadeia de texto entre a posição &quot;inicial&quot; e a posição &quot;final&quot;.

>[!BEGINSHADEBOX]

**Exemplos:**

* `substring( Hello ; 0 ; 3)`

  Retorna: ajuda

* `substring( Hello ; 1 ; 3 )`

  Devoluções: el

>[!ENDSHADEBOX]

## [!DNL indexOf (string; value; [start])]

Retorna a posição da primeira ocorrência de um valor especificado em uma string. Este método retorna &#39;-1&#39; se o valor procurado não estiver lá. O valor inicial indica onde a pesquisa deve começar na cadeia de caracteres.

>[!BEGINSHADEBOX]

**Exemplos:**

* `indexOf( Workfront ; o )`

  Devoluções: 1

* `indexOf( Workfront ; x )`

  Devoluções: -1

* `indexOf( Workfront ; o ; 3 )`

  Devoluções: 6

>[!ENDSHADEBOX]

## [!UICONTROL toBinary (value)]

Converte qualquer valor em dados binários.

Você também pode especificar a codificação como um segundo argumento para aplicar conversões binárias de hexadecimal ou base64 a dados binários.

>[!BEGINSHADEBOX]

**Exemplos:**

* `toBinary( Workfront )`

  Retorna: 57 6f 72 6b 66 72 6f 6e 74

* `toBinary( V29ya2Zyb250 ; base64 )`

  Retorna: 57 6f 72 6b 66 72 6f 6e 74

>[!ENDSHADEBOX]

## [!UICONTROL toString (value)]

Converte qualquer valor em uma string.

## [!UICONTROL encodeURL (text)]

Codifica caracteres especiais em algum texto para um endereço de URL válido.

## [!UICONTROL decodeURL (text)]

Decodifica caracteres especiais em um URL para texto.

>[!BEGINSHADEBOX]

**Exemplo:**
`decodeURL( Automate%20your%20workflow )`

Devoluções: [!UICONTROL Automate your workflow]

>[!ENDSHADEBOX]

## [!UICONTROL escapeHTML (text)]

Escapa todas as tags HTML no texto.

>[!BEGINSHADEBOX]

**Exemplo:**

`escapeHTML( <b>Hello</b> )`

Devoluções: `&lt;b&gt;Hello&lt;/b&gt;`

>[!ENDSHADEBOX]

## [!UICONTROL escapeMarkdown(text)]

Escapa todas as tags do Markdown no texto.

>[!BEGINSHADEBOX]

**Exemplo:**

`escapeMarkdown( # Header )`

Devoluções: `&#35; Header`

>[!ENDSHADEBOX]

## [!UICONTROL stripHTML (text)]

Remove todas as tags HTML do texto.

>[!BEGINSHADEBOX]

**Exemplo:**

`stripHTML( <b>Hello</b> )`

Retorna: Olá

>[!ENDSHADEBOX]

## contains (texto; sequência de pesquisa)

Verifica se o texto contém a cadeia de caracteres de pesquisa.

>[!BEGINSHADEBOX]

**Exemplos:**

* `contains( Hello World ; Hello )`

  Devoluções: [!UICONTROL true]

* `contains( Hello World ; Bye )`

  Devoluções: [!UICONTROL false]

>[!ENDSHADEBOX]

## [!UICONTROL split (text; separator)]

Divide uma cadeia de caracteres em uma matriz de cadeias de caracteres, separando-a em subcadeias.

>[!BEGINSHADEBOX]

**Exemplo:**

`split( John, George, Paul ; , )`

>[!ENDSHADEBOX]

## [!UICONTROL md5 (text)]

Calcula o hash md5 de uma string.

>[!BEGINSHADEBOX]

**Exemplo:**

`md5( Workfront )`

Devoluções: `1448bbbeaa7a9b8091d426999f1f666b`

>[!ENDSHADEBOX]

## [!UICONTROL sha1 (text; [encoding]; [key])]

Calcula o hash sha1 de uma cadeia de caracteres. Se o argumento chave for especificado, o hash sha1 HMAC será retornado. Codificações suportadas: &quot;hex&quot; (padrão), &quot;base64&quot; ou &quot;latin1&quot;.

>[!BEGINSHADEBOX]

**Exemplo:**

`sha1( workfront )`

Retorna: b2b30b8ae1f9e5b40fbb0696eaabdbfd8d0c087f

>[!ENDSHADEBOX]

## [!UICONTROL sha256 (text; [encoding]; [key])]

Calcula o hash sha256 de uma string. Se o argumento chave for especificado, o hash sha256 HMAC será retornado. Codificações suportadas: &quot;hex&quot; (padrão), &quot;base64&quot; ou &quot;latin1&quot;.>

>[!BEGINSHADEBOX]

**Exemplo:**

`sha256( workfront )`

Retorna: ed3d7397eec7b94453035b67ba4468c883ee3bedeb57137f7371f2e0cf5e2bbc

>[!ENDSHADEBOX]

## [!UICONTROL sha512 (text; [output encoding]; [key]; [key encoding])]

Calcula o hash sha512 de uma string. Se o argumento de chave for especificado, o hash sha512 HMAC será retornado.

Codificações suportadas:

* &quot;[!UICONTROL hex]&quot; (padrão)
* &quot;[!UICONTROL base64]&quot;
* &quot;[!UICONTROL latin1]&quot;

Codificações de chave suportadas:

* &quot;[!UICONTROL text]&quot; (padrão)
* &quot;[!UICONTROL hex]&quot;
* &quot;[!UICONTROL base64]&quot; ou &quot;[!UICONTROL binary]&quot;

Ao usar a codificação de chave &quot;[!UICONTROL binary]&quot;, uma chave deve ser um buffer, não uma cadeia de caracteres.

>[!BEGINSHADEBOX]

**Exemplo:**

`sha512(workfront)`

Devoluções: 789ae41b9456357e4f27c6a09956a767abbb8d80b206003ffdd1e94dbc687cd119b85e1e19db58bb44b234493af3

>[!ENDSHADEBOX]

## [!UICONTROL base64 (text)]

Transforma texto em base64.

>[!BEGINSHADEBOX]

**Exemplo:**

`base64( workfront )`

Retorna: d29ya2Zyb250==

>[!ENDSHADEBOX]
