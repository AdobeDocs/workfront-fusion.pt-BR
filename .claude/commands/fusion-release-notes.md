---
name: fusion-release-notes
description: Crie uma nova página de nota de versão semanal do Workfront Fusion e conecte-a à página de visão geral da atividade de lançamento e ao índice. Use quando o usuário quiser gravar, adicionar ou rascunhar uma nova nota de versão do Fusion ou página de lançamento semanal, ou solicitar o documento de novos recursos do Fusion para uma versão. Não use para notas de versão do Workfront (Quicksilver) em anúncios de produtos/versões de produtos — use o formatador de notas de versão para eles.
source-git-commit: 59a8d8ee83906bc16fc627bd348accc4e588cf9b
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 1%

---


# Notas de versão do Fusion

Cria uma nova página semanal de notas de versão do Adobe Workfront **Fusion** em `help/workfront-fusion/fusion-product-releases/` e a vincula a partir dos dois locais que a tornam detectável: a página de visão geral da atividade de lançamento e `help/workfront-fusion/TOC.md`.

Este é um sistema diferente das notas de versão do Quicksilver (Workfront principal) manipuladas pela habilidade `release-notes-formatter`:

| | Notas de versão do Fusion (esta habilidade) | Notas de versão do Quicksilver (`release-notes-formatter`) |
|---|---|---|
| Cadência | Semanal | Trimestralmente |
| Diretório | `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/` | `help/quicksilver/product-announcements/product-releases/` |
| Texto explicativo de data por recurso | Não — o título da página carrega a semana | Sim — `>[!NOTE]` bloco por recurso |
| Página de índice | `fusion-release-activity.md` (por ano/mês) | `{YY}-q{N}-release-overview.md` (por trimestre) |

## Etapa 1: reunir os recursos

Solicite ao usuário (se ainda não tiver sido fornecido) a lista de recursos/alterações a serem documentados para a semana e para cada um:

- Um título de recurso curto
- Uma descrição simples do que mudou e por que é importante
- Os artigos de ajuda aos quais ele se vincula (verifique se o caminho existe — não adivinhe)
- Se requer ação de usuário/administrador ou se é uma descontinuação (precisa de uma chamada `>[!IMPORTANT]`)

## Etapa 2: determine o nome e a data do arquivo

- Encontre a segunda-feira (ou data de lançamento) da semana que está sendo documentada e confirme-a com o usuário, se ambígua.
- Caminho do arquivo: `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md`
  - `{M}` e `{D}` não têm **zeros à esquerda**: `fusion-2026-7-20.md`, não `fusion-2026-07-20.md`.
  - Se a pasta do ano ainda não existir, crie-a.
- Verifique se já existe uma página para essa semana antes de criar uma nova.

## Etapa 3: escrever a página

### Frontmatter

```yaml
---
title: Workfront Fusion release activity Week of {Month} {Day}, {Year}
description: Workfront Fusion release activity Week of {Month} {Day}, {Year}
author: {Author}
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
```

Regras:
- `title` e `description` são idênticos.
- Sempre inclua a vírgula na data (`July 20, 2026`), mesmo que algumas páginas mais antigas a omitam — não copie essa inconsistência.
- **Use `hidefromtoc: true` para cada página nova. Não adicione um `exl-id` ou `TQID`.** Elas são atribuídas posteriormente quando a página é publicada; inventar uma está errado. (As páginas a partir de meados de 2026 seguirão este padrão — consulte `_fusion-release-notes-reference.md` se precisar verificar um exemplo.)

### Corpo

```markdown
# Workfront Fusion release activity: Week of {Month} {Day}, {Year}

This page describes all enhancements made in Adobe Workfront Fusion the week of {Month} {Day}, {Year}.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/en/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## {Feature title}

Feature description paragraph(s) — what changed, why, and how it affects existing scenarios/configurations if relevant.

For more information, see [{Help article title}](/help/workfront-fusion/{path-to-article}.md).

## {Next feature title}

...
```

Notas:
- Um H2 por recurso, na ordem que o usuário deu a eles (sem pedido forçado mais recente primeiro na página — é uma única semana).
- Nenhum texto explicativo de data `>[!NOTE]` por recurso — o título da página já contém a data.
- Se um recurso exigir ação ou for uma quebra de alteração/descontinuação, adicione uma chamada de `>[!IMPORTANT]` diretamente abaixo de H2, antes da descrição:

  ```markdown
  ## {Feature title}
  
  >[!IMPORTANT]
  >
  >**Action Required: {short summary of what the user must do and by when}**
  >
  >{Details of the requirement.}
  
  {Regular description paragraph(s).}
  ```
- Todos os recursos devem terminar com um &quot;Para obter mais informações, consulte [...]&quot; para o artigo de ajuda relevante. Verifique se o destino do link existe no repositório.

## Etapa 4: adicionar a página ao índice de visão geral

Editar `help/workfront-fusion/fusion-product-releases/fusion-release-activity.md`:

- Localize a seção `## Fusion releases in {current year}` (é **não** encapsulada em um bloco recolhível `+++` — somente anos passados são recolhidos).
- Localize ou crie o cabeçalho `### {Month} {Year}` para o mês do lançamento, diretamente abaixo do cabeçalho do ano.
  - Se o cabeçalho do mês ainda não existir, adicione-o **acima** do mês anterior (primeiro o mês mais recente).
- Adicione a nova página como o marcador **primeiro** sob o cabeçalho desse mês (semana mais recente primeiro):

  ```markdown
  * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```
- Se esta for a primeira versão de um novo ano, adicione um novo cabeçalho `## Fusion releases in {YYYY}` acima do cabeçalho do ano anterior e envolva a seção do ano *anterior* em um bloco recolhível `+++ **Click to open**` / `+++` se ainda não estiver (somente o ano atual permanece expandido).

## Etapa 5: adicionar a página ao índice

Editar `help/workfront-fusion/TOC.md`:

- Localizar `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` do ano atual, aninhado em `* Fusion release activity {#fusion-release-activity}`.
- Adicionar a nova página como a entrada **primeira** sob esse cabeçalho (mais recente primeiro), correspondendo ao recuo existente (8 espaços):

  ```markdown
        * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```
- Se o título do ano atual ainda não existir, adicione `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` acima do título do ano anterior.
- **Não** adicione o prefixo `{hide-from-toc}` a novas entradas — isso só é usado em entradas mais antigas quando elas envelhecem fora da navegação visível (consulte Inconsistências conhecidas abaixo).

### Inconsistências conhecidas a serem observadas (não replicar)

- Várias entradas do índice inicial de 2026 são aninhadas sob o cabeçalho `Fusion releases - 2025` por engano, mesmo que as próprias páginas sejam versões de 2026. Ao adicionar uma nova entrada, sempre verifique se ela aparece sob o título correspondente a **seu próprio ano**, não onde a entrada anterior estiver.
- Alguns títulos de página/H1 mais antigos omitem a vírgula antes do ano (`July 13 2026` em vez de `July 13, 2026`). Sempre use a vírgula em novas páginas.

## Etapa 6: lista de verificação final

- [ ] Arquivo criado no caminho correto sem zeros à esquerda na data
- [ O Frontmatter ] usa o `hidefromtoc: true`, mas não inventou o `exl-id`/`TQID`
- [ ] Correspondência de título/descrição, a data inclui vírgula
- [ ] Cada recurso tem uma descrição e um link verificado &quot;Para obter mais informações&quot;
- [ ] Os recursos Action-required/deprecation têm uma chamada `>[!IMPORTANT]`
- [ ] Nova página adicionada como a entrada mais recente em `fusion-release-activity.md`, no ano/mês correto
- [ ] Nova página adicionada como a entrada mais recente em `TOC.md`, sob o cabeçalho de ano correto
- [ ] Novos cabeçalhos de ano/mês criados, se necessário, com o ano anterior recolhido em `fusion-release-activity.md`

## Recursos adicionais

Para exemplos completos trabalhados (uma semana simples com vários recursos e uma com uma chamada de `>[!IMPORTANT]` ação necessária), consulte `.claude/commands/_fusion-release-notes-reference.md`.
