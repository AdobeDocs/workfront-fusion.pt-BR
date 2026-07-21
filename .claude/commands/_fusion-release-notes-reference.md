---
source-git-commit: 59a8d8ee83906bc16fc627bd348accc4e588cf9b
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---
# Exemplos de Referência de Notas de Versão do Fusion

Exemplos trabalhados para a habilidade `fusion-release-notes`, com base nas páginas recentes reais de
`help/workfront-fusion/fusion-product-releases/fusion-releases-2026/`.

&#x200B;---

## Exemplo 1: semana com vários recursos simples

Baseado em `fusion-2026-6-22.md`.

```markdown
---
title: Workfront Fusion release activity Week of June 22, 2026
description: Workfront Fusion release activity Week of June 22, 2026
author: Becky
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
# Workfront Fusion release activity: Week of June 22, 2026

This page describes all enhancements made in Adobe Workfront Fusion the week of June 22, 2026.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/pt-br/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Create custom JavaScript packages to use in scenarios

To provide better flexibility and control of your scenarios, we've added the ability to create a custom JavaScript packages that you can then use in scenarios. You can create custom packages in the Packages area of Fusion. You then add functions or variables from these packages to your scenarios in the form of an Adobe App Builder module.

Packages include functions, along with any variables or dependencies the functions rely on. You can also test functions in your package before using them in your scenarios

Because custom packages work through Adobe App Builder, your organization must have an Adobe App Builder license to use them.

For more information on using custom functions in Fusion, see [Use custom function packages](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

## View changes between scenario versions

To make it easier to understand changes between scenario versions, we've added the ability to view and compare those changes. Now you can bring up a window that displays specific changes between two selected versions of the same scenario.

For more information, see [View and manage scenario versions](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md).
```

&#x200B;---

## Exemplo 2: semana com uma chamada action-required / deprecation

Baseado em `fusion-2026-3-9.md`.

```markdown
---
title: Workfront Fusion release activity Week of March 9, 2026
description: Workfront Fusion release activity Week of March 9, 2026
author: Becky
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
# Workfront Fusion release activity: Week of March 9, 2026

This page describes all enhancements made in Adobe Workfront Fusion the week of March 9, 2026.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/pt-br/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Log in to Fusion through Adobe IMS

>[!IMPORTANT]
>
>**Action Required: Migrate to IMS Login for Adobe Workfront Fusion by April 15.**
>
>To ensure that you will be able to log in after April 15, your Fusion administrator must migrate you to Adobe IMS. Please contact your Fusion administrator to be migrated.

As part of our ongoing security enhancements, Adobe is deprecating the legacy username and password login method for Adobe Workfront Fusion. Effective **April 15**, the legacy login flow **will no longer be supported**.

Going forward, access to Adobe Workfront Fusion will require authentication through the Adobe Identity Management System (IMS) login flow.

For instructions on provisioning access through the Adobe Admin Console, see [Add users to Adobe Workfront Fusion through the Adobe Admin Console](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-fusion-users-admin-console.md).

If you have questions or need assistance with the migration process, please contact your Adobe representative.

## New route labels

To make it easier to identify routes, we've added labels. Now, routes are labeled in the order they execute. Fallback and error handling routes are also labeled. Route labels also display any filters used for that route.

For more information on routes, see [Add a Router module and configure routes](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).
```

&#x200B;---

## Padrão de atualização da página de visão geral (`fusion-release-activity.md`)

Adicionar a semana de 20 de julho de 2026 a uma seção existente de mês de julho de 2026:

```markdown
## Fusion releases in 2026

### July 2026

* [Workfront Fusion release activity: Week of July 20, 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-20.md)
* [Workfront Fusion release activity: Week of July 13 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-13.md)
```

Começar um novo ano (somente exemplo — faça isso quando a primeira versão de {YYYY+1} for publicada):

```markdown
## Fusion releases in 2027

### January 2027

* [Workfront Fusion release activity: Week of January 4, 2027](/help/workfront-fusion/fusion-product-releases/fusion-releases-2027/fusion-2027-1-4.md)

## Fusion releases in 2026

+++ **Click to open**

### December 2026
...
+++
```

&#x200B;---

## Padrão de atualização do TOC.md

Adicionando a semana de 20 de julho de 2026 como a entrada mais recente:

```markdown
* Fusion release activity {#fusion-release-activity}
    * [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md)
    * Fusion releases - 2026 {#fusion-releases-2026}
        * [Workfront Fusion release activity: Week of July 20, 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-20.md)
        * [Workfront Fusion release activity: Week of July 13 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-13.md)
        ...
```

&#x200B;---

## Inconsistências conhecidas em páginas existentes (somente para referência — não as copie em novas páginas)

1. **Título de ano no local errado em TOC.md** — as entradas de janeiro a fevereiro de 2026 atualmente estão sob o cabeçalho `Fusion releases - 2025` em vez de `Fusion releases - 2026`. Este é um erro pré-existente, não a estrutura pretendida.
2. **Vírgula ausente antes do ano** — páginas como `fusion-2026-7-13.md` usam &quot;13 de julho de 2026&quot; em vez de &quot;13 de julho de 2026&quot; no título/descrição/H1. Sempre inclua a vírgula em novas páginas.
3. **`hidefromtoc`vs `exl-id`/`TQID`** — as páginas até `fusion-2026-4-27.md` têm um `exl-id` (e às vezes `TQID`); as páginas a partir de `fusion-2026-5-4.md` usam `hidefromtoc: true`. As novas páginas devem seguir o padrão mais recente (`hidefromtoc: true`, sem `exl-id`/`TQID`), pois esses identificadores são atribuídos posteriormente pelo pipeline de publicação.
4. **`{hide-from-toc}`prefixo no TOC.md** — usado para desenfatizar entradas mais antigas na navegação renderizada depois que elas envelhecem fora da exibição recente. Não adicione isso a uma entrada totalmente nova.
