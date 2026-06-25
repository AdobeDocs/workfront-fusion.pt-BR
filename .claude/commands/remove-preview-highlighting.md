---
name: remove-preview-highlighting
description: ""
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---


# Remover destaque da visualização (Workfront)

## Escopo

Aplicar somente quando **todos** forem verdadeiros:

1. O usuário invocou este fluxo de trabalho (por exemplo, diz **&quot;remover destaque de visualização&quot;** ou claramente a mesma intenção).
2. O caminho do arquivo do Markdown **não** contém **`product-announcements`** (exclua toda a árvore de pastas, por exemplo, notas de versão, betas, anúncios em `help/quicksilver/product-announcements/`).
3. O arquivo Markdown **não** está listado em **[Caminhos excluídos](#excluded-paths)** abaixo.
4. O arquivo Markdown aparece em `git log` como tendo conteúdo de visualização **adicionado ou modificado** pelo usuário Git atual dentro do intervalo de datas especificado pelo usuário (consulte a etapa Inventário).
5. O artigo tem **pelo menos um** de:
   - Ambiente de visualização **linguagem em prosa de corpo ou parágrafos de trecho reais** (padrões típicos: &quot;informações destacadas&quot;, &quot;Ambiente de visualização&quot;, &quot;ainda não disponível no geral&quot;, notas de versão rápidas)—**não** uma correspondência de **apenas texto do link** em uma página de índice/índice (veja abaixo); ou
   - Qualquer elemento HTML com **`class="preview"`** (ex.: `<span class="preview">`, `<div class="preview">`); ou
   - Um trecho de visualização **variável**, como **`{{highlighted-preview}}`** ou **`{{highlighted-preview-article-level}}`**.

Se o escopo não estiver claro, confirme antes de editar.

**TOC / páginas de índice — sempre ignore este caso:** **Nunca** coloque um arquivo no inventário quando o texto relacionado à visualização **somente** estiver **dentro** de um texto de exibição do link de Markdown apontando para **outro** artigo (por exemplo: *Enviar um relatório no ambiente de Pré-visualização Sandbox*) **e** o arquivo tem **não** `class="preview"`, **não** variáveis de trecho e **no** visualização do modelo em **prosa fora dos links**. Isso não é um destaque de visualização nessa página, é apenas uma menção ao índice. Aplica-se a qualquer índice/índice, não apenas a um arquivo.

### Caminhos excluídos

Nunca adicione esses itens ao inventário ou edite-os neste fluxo de trabalho, a menos que o usuário os substitua explicitamente:

- `help/quicksilver/documents/adobe-workfront-for-experience-manager-assets-essentials/send-to-aem.md` — Os limites de Visualização paralela vs. Produção precisam de uma decisão editorial deliberada fora da automação.
- `help/quicksilver/reports-and-dashboards/reports/creating-and-managing-reports/create-manage-reports.md` — relata o sumário; o único sinal de &quot;visualização&quot; é o link para o artigo de entrega Visualizar sandbox.

## Fluxo de trabalho necessário (humano no loop)

Fazer **não** edição em massa do repositório sem aprovação.

1. **Inventário**\
   a) **Pergunte ao usuário para qual versão trimestral** ele está removendo o realce de visualização (por exemplo, &quot;3º trimestre de 2026&quot; ou &quot;2026.07&quot;).\
   b) **Buscar o calendário de lançamento** de `https://wiki.corp.adobe.com/spaces/AWF/pages/3631617814/2026+Monthly+Release+Calendar` usando a ferramenta MCP adobe-wiki. Localizar:
   - A **Data da Versão de Produção** da **anterior** versão trimestral → `--since`.
   - A **Data da Versão de Produção** da versão trimestral **target** → `--until`.
   - As versões trimestrais são identificadas pela coluna &quot;Nome da versão trimestral&quot; (por exemplo, 2026.01, 2026.04, 2026.07, 2026.10).
   - **Se a data atual estiver no 4º trimestre (outubro-dezembro):** depois de buscar o calendário do ano atual, peça ao usuário para fornecer a URL para o calendário de lançamento do próximo ano e, em seguida, busque também para que todas as datas de produção trimestrais necessárias estejam disponíveis.
c. Determine o usuário Git atual e execute o seguinte usando as datas de lançamento de produção da etapa b:

   ```bash
   GIT_USER=$(git config user.name)
   git log --since="YYYY-MM-DD" --until="YYYY-MM-DD" \
     --author="$GIT_USER" --name-only --pretty=format: \
     -- "help/quicksilver/**/*.md" | sort -u | grep -v '^$'
   ```

   d) A partir desses resultados, **filtre para arquivos em que os compromissos do usuário atual no intervalo de datas realmente adicionou ou modificou o conteúdo de visualização**. Para cada arquivo candidato, verifique se as confirmações do usuário introduziram marcadores de visualização:

   ```bash
   git log --since="YYYY-MM-DD" --until="YYYY-MM-DD" \
     --author="$GIT_USER" -p -- "<file>" | \
   grep -q '^\+.*class="preview"\|^\+.*{{highlighted-preview\|^\+.*highlighted information\|^\+.*not yet generally available'
   ```

   Inclua o arquivo somente se este grep for compatível (código de saída 0). Isso evita falsos positivos em que um usuário fez uma edição não relacionada a um arquivo cujo destaque de visualização foi adicionado por outra pessoa.

   e. **Omitir** qualquer caminho em **`product-announcements`**, qualquer **[caminho Excluído](#excluded-paths)** e qualquer página de **índice/índice** de acordo com a regra de índice acima.\
   f) Apresenta a lista classificada resultante. Se o usuário disser que um arquivo listado não tem realce de visualização, remova-o da execução e ajuste os critérios em vez de forçar as edições.

2. **Start**\
   Pergunte se deve começar com o artigo **first** da lista (ou com um caminho que os nomes de usuário).

3. **Por artigo — mostrar primeiro, editar após OK**
   - Leia o arquivo.
   - Proponha edições claramente: **antes/depois de trechos** ou uma descrição focalizada do estilo de comparação do que será alterado.
   - **Aguarde** por aprovação explícita (por exemplo, &quot;ok&quot;, &quot;aplicar&quot;, &quot;sim&quot;) antes de gravar o arquivo.

4. **Após cada arquivo**\
   Pergunte se deseja mover para o artigo **próximo** (ou parar/ignorar).

## Regras de conteúdo (GA: visualizar o conteúdo no doc)

Ao remover o destaque de visualização para **disponibilidade geral**, a meta é: **manter o comportamento documentado para Visualização**, remover **ramificações obsoletas &quot;em produção&quot; / processo antigo** e **remover rótulos e invólucros somente visualização** para que o tópico seja lido como atual para todos os clientes.

### Etapas paralelas

- Se o artigo tiver uma etapa (ou item numerado) **enquadrada como &quot;em produção&quot;** (ou equivalente: produção atual / comportamento de produção existente) **e** uma etapa **paralela** enquadrada como **&quot;na visualização&quot;** (ou ambiente de Visualização):
   - **Remover** a etapa em produção (o caminho antigo).
   - **Manter** a **substância** da etapa de visualização, mas **reword** de modo que seja **não** específico da visualização (remover &quot;na visualização&quot;, &quot;Ambiente de visualização&quot; etc.). Ajuste a numeração para que a lista permaneça consistente.

Se a estrutura for ambígua (sem paralelo claro), **pare** e mostre ambos os candidatos; pergunte ao usuário qual bloco manter.

### Seções paralelas

- Se uma **seção** (cabeçalho + corpo) for **sobre &quot;no ambiente de produção&quot;** e houver uma **seção paralela** **sobre &quot;no ambiente de visualização&quot;**:
   - **Remover** a seção de ambiente de produção (o conteúdo substituído).
   - **Substitua** pelo conteúdo da seção de visualização, em seguida **remova** o texto do ambiente de visualização e qualquer wrapper **`class="preview"`** para que a seção seja neutra (pronta para GA).

### Trechos e avisos do início do artigo

- Remover blocos **apenas para visualização** (extensões/divisões ou parágrafos que explicam apenas que o conteúdo realçado é somente para visualização, versão rápida, sandbox etc.) assim que o recurso for GA.
- Remova links ou frases cuja finalidade **somente** seja a disponibilidade de visualização, a menos que o usuário diga para manter um aviso diferente.

### HTML `class="preview"`

- Remova as **marcas de abertura e fechamento** de elementos que usam **`class="preview"`**, **mantendo o conteúdo interno** (markdown/HTML dentro da marca).
- Manipular **`<span class="preview">`** e **`<div class="preview">`**, e o mesmo padrão em outras marcas (por exemplo, **`<p class="preview">`**, **`<li class="preview">`**) quando elas aparecerem no conteúdo de corpo **visível** (não comentado).
- Preservar estrutura de lista/tabela; corrigir listas quebradas ou espaços em branco perdidos após desempacotar.

### Seções comentadas (comentários do HTML)

- **Não** exclua, decomponha ou **modifique** qualquer conteúdo dentro de **`<!-- … -->`** comentários do HTML **a menos que o usuário diga explicitamente** o que fazer (por exemplo, excluir o comentário inteiro, remover as classes de visualização apenas dentro do comentário, remover o comentário para disponibilidade geral).
- Se o conteúdo relacionado à visualização ou **`class="preview"`** aparecer **somente** dentro dos comentários, **chame-o** ao revisar o artigo: diga o que está no comentário e **pergunte** o que fazer. **Padrão: deixar seções comentadas inalteradas.**

### O que não fazer

- Não execute este fluxo de trabalho em caminhos em **`product-announcements`** (notas de versão e relacionadas); o inventário deve excluí-los.
- Não faça o inventário ou edite os caminhos listados em **[Caminhos excluídos](#excluded-paths)**, a menos que o usuário solicite explicitamente a inclusão de um.
- **Não** remove ou edita automaticamente **blocos comentados** (`<!-- … -->`); siga as **seções comentadas** acima.
- Não remova &quot;Visualização&quot; quando for **não** sobre este padrão de disponibilidade de recursos (por exemplo, [Visualizar ambiente de Sandbox] (·) como um **nome do produto** em um contexto não relacionado). Use o julgamento e pergunte se não tem certeza.
- Não altere `author:` ou o assunto principal não relacionado, a menos que o usuário solicite.
- Não ignore a etapa **mostrar → aprovar**.

## Verificações de qualidade antes de apresentar edições

- Nenhum **`class="preview"`** restante no escopo de alteração acordado.
- Não há cabeçalhos duplicados órfãos ou números de etapa quebrados.
- A introdução lê corretamente **sem** contradizendo a disponibilidade geral (não &quot;somente na Pré-visualização&quot; para os recursos enviados).

## Referências

- Corresponder ao **[estilo de documentação do Workfront](https://experienceleague.adobe.com/pt-br?lang=pt-BR)** e às convenções de repositório (regras de confirmação/PR se o usuário estiver confirmando).
