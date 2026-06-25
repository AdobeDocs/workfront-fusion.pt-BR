---
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---
# Modelos de referência das notas de versão

Modelos detalhados para cada tipo de página da nota de versão. Elas se baseiam nos modelos em
`help/quicksilver/product-announcements/product-releases/release-note-templates/` e
a formatação real usada em versões trimestrais recentes.

&#x200B;---

## Modelo de página de área de produto

```markdown
---
title: {Written Quarter} {Year} {Area} enhancements
description: {Written Quarter} {Year} {Area} enhancements
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} {Area} enhancements

This page describes {Area} enhancements made with the {Written Quarter} {Year} release to the Preview environment. These enhancements will be made available in the Production environment as noted.

For a list of all changes available at this point in the {Written Quarter} {Year} release cycle, see [{Written Quarter} {Year} release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title Here

>[!NOTE]
>
>Preview: {Month Day, Year}
>Production fast release: {Month Day, Year}
>Production for everyone: {Month Day, Year}

Feature description paragraph.

For more information, see [Help article title](/help/quicksilver/path/to/article.md).
```

### Regras para páginas de área de produto

- Usar marcação (não HTML) para conteúdo do corpo
- Cada recurso recebe um cabeçalho H2
- A chamada `>[!NOTE]` deve ter uma linha em branco antes dela
- O formato `>[!NOTE]` é exatamente:

  ```
  >[!NOTE]
  >
  >Preview: {date}
  >Production fast release: {date}
  >Production for everyone: {date}
  ```

- Se um recurso foi removido temporariamente, adicione uma linha após a data:

  ```
  >
  >This feature has been temporarily removed from the Production environment on {date}.
  ```

- Os links de ajuda usam caminhos absolutos que começam com `/help/quicksilver/`

&#x200B;---

## Modelo da página de visão geral

```markdown
---
title: {Written Quarter} {Year} release overview
description: This page provides information about functionality that is included in the {Written Quarter} {Year} release. These enhancements are planned to become available in the Production environment throughout the quarter.
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} release overview

This page provides information about functionality that is included in the {Written Quarter} {Year} release scheduled for {Release Month} {Year}.

The enhancements on this page are available in the Preview environment. This page will be updated with additional enhancements as the {Written Quarter} {Year} release nears its planned Production release.

>[!IMPORTANT]
>
>
>Monthly and quarterly releases are planned to be available on the Thursday of the second full week of the month, unless otherwise specified.
>
>|Monthly release|Quarterly release|
>|----|----|
>|<ul><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li></ul>|<ul><li>{VV}.{M} ({Month Day, Year})</li></ul>|
>
>Note that for the final release of each quarter ({VV}.{M} this quarter), users on the fast release schedule will receive the release one day early ({Month Day, Year}).
>
>For more information on the fast release process, see [Enable or disable the fast release process](/help/quicksilver/administration-and-setup/set-up-workfront/configure-system-defaults/enable-fast-release-process.md).

## Adobe Workfront enhancements

* [Administrator enhancements](#administrator-enhancements)
* [Document enhancements](#document-enhancements)
* [Project enhancements](#project-enhancements)
* [Reporting enhancements](#reporting-enhancements)
* [Requesting enhancements](#requesting-enhancements)
* [Other enhancements](#other-enhancements)
```

### Tabela de recursos de visão geral

Cada seção da área de produto H3 contém uma tabela do HTML. Use esta estrutura exata:

```html
### {Area} enhancements

<table>
            <col style="width: 50%;" />
            <col style="width: 25%;" />
            <tbody>
              <tr>
        <td><strong>Feature</strong>
        </td>
        <td><strong>Preview</strong></td>
        <td><strong>Fast release</strong></td>
        <td><strong>Quarterly</strong></td>
        </tr>
    <tr>
        <td>
            <a href="/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-{area}.md" class="MCXref xref" xrefformat="{para}">Feature Title</a><p>Short description of the feature.</p>
        </td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
    </tr>
            </tbody>
        </table>
```

#### Regras de tabela

- Célula de recurso: marca `<a>` com `class="MCXref xref" xrefformat="{para}"` seguida de descrição `<p>`
- O `href` vincula à página da área do produto (não é uma âncora específica)
- Células de data: encapsuladas em `<p>` marcas
- Para itens fora do cronograma, adicione `<p>[!BADGE Off schedule]{type=Neutral}</p>` após o link
- `<p></p>` vazio após o link ser aceitável quando nenhuma medalha for necessária
- Manter o recuo do HTML consistente com os arquivos existentes

### Visão geral das seções finais

Depois de todas as tabelas de área de produto:

```markdown
## Release notes for other areas

### Workfront Fusion enhancements

New features in Workfront Fusion are available in Production at a cadence outside of the standard release schedule. For more information about the latest features, see [Adobe Workfront Fusion release activity](https://experienceleague.adobe.com/en/docs/workfront-fusion/using/fusion-release-activity/fusion-release-activity).

### Workfront Planning enhancements

New features in Workfront Planning are available in Production. For more information about the latest features, see [{Written Quarter} {Year} release activity for Adobe Workfront Planning](/help/quicksilver/product-announcements/product-releases/planning-release-activity/planning-release-activity-{YY}-q{N}.md).

There are no updates for the following at this point in the release:

* Scenario Planner
* Proof
* Goals

## Desktop proofing viewer updates

{Version info if available, otherwise omit section}

## Announcements

{Announcement content}

### API version {NN}

{API version info}

### Workfront Maintenance Updates

For information about the maintenance updates made during the {Written Quarter} {Year} release, see [Workfront Maintenance Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html).

### Training updates

Explore the latest updates made to learning programs, learning paths, videos, and guides for each Adobe Workfront product release. For more information, see the "What's New" section of the [Workfront Tutorials page](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/home.html).
```

&#x200B;---

## Modelo de página de aparência

```markdown
---
title: Look-and-feel updates during the {Written Quarter} {Year} release time frame
description: Look-and-feel updates during the {Written Quarter} {Year} release time frame
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---

# Look-and-feel updates during the {Written Quarter} {Year} release time frame

This page describes minor updates to the look and feel of various areas of the Adobe Workfront application that were made within the {Written Quarter} {Year} release timeframe. These enhancements will be made available in the Production environment a minimum of 2 weeks after releasing to Preview.

For a list of all changes available with the {Written Quarter} {Year} release, see [{Written Quarter} {Year} Release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title

>[!NOTE]
>
>Preview release: {Month Day, Year}; Planned Production release: {Month Day, Year}

Description of the look-and-feel change.
```

&#x200B;---

## Formatos de Texto Explicativo de Data

### Páginas de área de produto (várias linhas)

```markdown
>[!NOTE]
>
>Preview: March 5, 2026
>Production fast release: April 15, 2026
>Production for everyone: April 16, 2026
```

### Páginas de aparência e comportamento (linha única)

```markdown
>[!NOTE]
>
>Preview release: March 5, 2026; Planned Production release: March 19, 2026
```

### Páginas semanais (linha única)

```markdown
>[!NOTE]
>
>Preview release: February 9, 2023; Planned Production release: February 23, 2023
```

&#x200B;---

## Inconsistências conhecidas a serem observadas

1. **Link de visão geral incorreto no trimestre** — As páginas de área do produto às vezes vinculam à visão geral do trimestre anterior (por exemplo, `26-q1` em vez de `26-q2`)
2. **As datas de visualização estão mostrando o ano errado** — As tabelas de visão geral às vezes mostram o ano anterior na coluna de Visualização (por exemplo, &quot;2025&quot; em vez de &quot;2026&quot;)
3. **Marcas de fechamento `</tr>` ausentes** — Algumas linhas da tabela HTML não têm marcas de fechamento adequadas
4. **`content-type: release-notes`** — Presente em arquivos mais antigos, omitido nas páginas da área do produto do segundo trimestre 26 mais recentes. Siga o padrão do trimestre atual.
5. **Erro de digitação no modelo** — o modelo de aparência e comportamento tem `relesae` em vez de `release`; sempre usar a ortografia correta
6. **Faltando `<p></p>` após o link de recurso** — Algumas linhas da tabela de visão geral omitem a marca `<p>` vazia após a marca `<a>`
