---
name: add-mini-tocs
description: ""
source-git-commit: 4ec81401b5a76edd620b9779414ee578966b4315
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Adicionar mini sumários

Digitaliza um arquivo do Markdown e insere um mini índice em cada cabeçalho qualificado que tem subtítulos diretos.

## Fluxo de trabalho (WRK)

1. Leia o arquivo de destino.
2. Identifique cada cabeçalho no nível `##` ou mais profundo que tenha pelo menos um cabeçalho filho direto (um nível `#` mais profundo).
3. Para cada um desses cabeçalhos principais, crie uma lista com marcadores de links somente para seus filhos diretos.
4. Insira a lista imediatamente antes do primeiro cabeçalho filho, após qualquer texto introdutório que siga o cabeçalho pai.
5. Se um mini sumário já existir nessa posição, compare-o com os cabeçalhos filhos atuais dessa seção. Se a lista estiver desatualizada (entradas ausentes, entradas extras ou links incorretos), substitua-a pela lista atualizada. Se já corresponder, ignore.
6. Grave o arquivo atualizado.

## Escopo

- **Nunca** crie um mini sumário sob o título do artigo `#`. Mini índices são adicionados somente sob `##` títulos e mais profundos.
- Um cabeçalho `##` obtém uma lista de seus `###` filhos diretos.
- Um cabeçalho `###` obtém uma lista de seus `####` filhos diretos.
- E assim por diante para níveis mais profundos.

## Formato do link

Cada entrada na lista usa este formato exato:

```
* [Heading text](#anchor)
```

### Regras de geração de âncora

Converta o texto do cabeçalho em uma âncora da seguinte maneira:

1. Todo o texto em minúsculas.
2. Remova os caracteres que não sejam letras, números, espaços ou hifens.
3. Substituir espaços por hifens.
4. Remova qualquer formatação de código com quebra automática (mantenha o texto dentro).

Exemplo: `### Create or edit a function` → `#create-or-edit-a-function`

## Regras de aninhamento

- Vincular somente **filhos diretos** (um nível mais profundo que o pai) em cada lista.
- Não inclua netos ou títulos mais profundos na mesma lista.
- Se esses cabeçalhos filhos tiverem filhos, eles receberão seu próprio mini sumário separado inserido abaixo deles.

**Exemplo de estrutura:**

```
## Manage a package          ← parent: gets a list of ### headings
### Functions                ← child of ##, parent of ####: gets a list of #### headings
#### Create a function       ← child of ###
#### Delete a function       ← child of ###
### Variables                ← child of ##
### History                  ← child of ##
```

Resultados em:

Em `## Manage a package`:

```
* [Functions](#functions)
* [Variables](#variables)
* [History](#history)
```

Em `### Functions`:

```
* [Create a function](#create-a-function)
* [Delete a function](#delete-a-function)
```

## Posicionamento

Insira a mini lista de sumário imediatamente antes do primeiro cabeçalho filho. Se houver texto de introdução entre o cabeçalho pai e o primeiro cabeçalho filho, a lista vai após esse texto, diretamente acima do primeiro cabeçalho filho. Sempre inclua uma linha em branco antes e depois da lista do mini índice.

## O que ignorar

- `#` títulos (o título do artigo): nunca adicione um mini índice aqui.
- Cabeçalhos principais com apenas um filho direto: ignorar — uma lista de item único não adiciona nenhum valor de navegação.
- Seções sem cabeçalhos filhos: ignorar.
