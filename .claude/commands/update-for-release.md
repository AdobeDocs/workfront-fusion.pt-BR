---
name: update-for-release
description: ""
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---


# Atualização para lançamento (Workfront)

Essa habilidade aborda a atualização de artigos de ajuda do Workfront para uma versão futura de recursos. O fluxo de trabalho é o inverso de `remove-preview-highlighting`: o novo comportamento está sendo adicionado aos artigos, marcados como Pré-visualização e (posteriormente, no GA) limpos por essa outra habilidade.

## Escopo

Aplicar quando **todos** forem verdadeiros:

1. O usuário está atualizando os artigos de ajuda do Workfront para um recurso que está sendo enviado (normalmente, Visualizar primeiro).
2. A alteração introduz um novo comportamento ou interface do usuário, não uma limpeza de DG. Para limpeza de GA, use **remove-preview-highlighting**.
3. O arquivo **não** é uma nota de versão. Para notas de versão, use **release-notes-formatter**.
4. O usuário forneceu o contexto do recurso: no mínimo, uma descrição curta e uma captura de tela; idealmente um URL PRD (Adobe Wiki).

Se o escopo não estiver claro, confirme antes de iniciar.

## Fluxo de trabalho necessário (humano no loop)

Faça **não** edição em massa do repositório. Mova um artigo de cada vez. Após cada artigo, pergunte se deseja continuar no próximo.

### &#x200B;1. Coletar contexto de recurso

Confirme com o usuário:

- **O que mudou** (resumo de 1-2 frases do novo comportamento ou interface do usuário).
- **Captura(s) de tela** da nova interface. Se fornecido, salve na pasta `assets/` do artigo de destino com um nome de arquivo kebab-case descritivo (por exemplo, `add-custom-message.png`). Se não for fornecido, pergunte se deve aguardar um ou continuar com uma referência de espaço reservado.
- **PRD URL** (Adobe Wiki), se disponível. Busque-o com a ferramenta `get_wiki_content` do MCP `user-Adobe Wiki Confluence`. Leia-o para encontrar comportamentos que o usuário não pode ver na interface do usuário: efeitos colaterais de notificação, o que acontece quando algo é editado ou adicionado posteriormente, limites de caracteres não exibidos, permissões etc.
- **Disponibilidade**: somente visualização, Visualização + versão rápida ou já disponível. Isso direciona a escolha do trecho na etapa 3.
- **Exclusões explícitas**: todos os artigos que o usuário deseja ignorar (por exemplo, &quot;este recurso não está em modelos&quot;).

### &#x200B;2. Artigos afetados pelo inventário

Pesquise o repositório com as palavras-chave da área de recursos (por exemplo, `approval workflow`, `document approval`, o rótulo de campo específico). Criar uma lista de candidatos:

- Artigos explicativos na árvore `help/quicksilver/.../` relevante.
- Artigos de visão geral e perguntas frequentes que mencionam a área de recursos.
- **Excluir** `product-announcements/` (as notas de versão usam uma habilidade diferente).
- **Excluir** páginas de índice/índice nas quais a única menção é o texto do link para outro artigo.
- **Excluir** artigos que o usuário disse para ignorar na etapa 1.

Apresentar a lista de candidatos ao usuário. Pergunte o que atualizar e o que ignorar. Referência cruzada `help/quicksilver/TOC.md` se um artigo irmão parecer ausente.

### &#x200B;3. Escolha o trecho de visualização

Leia `help/_includes/snippets.md` e escolha por disponibilidade:

| Disponibilidade | Trecho |
| --- | --- |
| Somente visualização — o conteúdo destacado é novo em um artigo disponível ao público em geral | `{{highlighted-preview}}` |
| Somente visualização — todo o artigo é novo | `{{highlighted-preview-article-level}}` |
| Pré-visualização + clientes de lançamento rápido, geral | `{{preview-fast-release-general}}` |

Se um trecho específico da versão já existir para o trimestre atual, prefira isso ao genérico. Confirme a escolha com o usuário antes de aplicar.

### &#x200B;4. Por artigo — mostrar primeiro, editar após OK

Para cada artigo na lista confirmada pelo usuário:

1. **Leia o arquivo.**

2. **Determinar o padrão de realce.** Pergunte ao usuário que se encaixa neste artigo (a resposta pode diferir de acordo com o artigo):

   - **Duplicação por seção**: anexar `in Production` ao cabeçalho de seção existente. Adicione uma nova seção com `in Preview` anexada, encapsulada em `<div class="preview"> ... </div>`. Use quando o novo comportamento alterar significativamente o procedimento: etapas extras, uma nova imagem, novas linhas de tabela ou texto diferente. Típica para procedimentos de instrução.
   - **Encapsulamento por linha**: adicione a(s) nova(s) frase(s) embutida(s) dentro da seção existente, encapsulada em `<span class="preview"> ... </span>`. Use quando a adição for uma ou duas frases que se encaixem naturalmente em um parágrafo, célula de tabela ou resposta de perguntas frequentes existente.
   - **Misto**: algumas seções no mesmo artigo usam duplicação por seção, outras usam quebra automática por linha. Mostre esta opção quando o artigo tiver seções de procedimentos e seções de estilo de Perguntas frequentes.

3. **Coloque o trecho** em sua própria linha imediatamente após o cabeçalho H1, com uma linha em branco acima e abaixo. O trecho fica **antes** do parágrafo de introdução.

4. **Armazenar novos detalhes em &quot;sempre incluir&quot; vs. &quot;pronto para revisão&quot;.** Este é o passo mais importante.

   - **Sempre incluir** (aplicar automaticamente, sem prompt): comportamentos invisíveis que o usuário não pode observar ao interagir com a interface. Exemplos:
      - Efeitos colaterais (por exemplo, &quot;editar novamente o email para todos os participantes&quot;)
      - Comportamento em outros objetos ou eventos posteriores
      - Pré-requisitos e permissões
      - Limites não mostrados na interface
      - Tudo o que o usuário pode aprender somente com o PRD, os documentos ou a equipe de produtos
   - **Acima para revisão** (presente ao usuário com `AskQuestion` como uma seleção múltipla): fatos que o usuário pode ver na tela ao usar o recurso. Exemplos:
      - Um contador de caracteres que a interface do usuário já mostra (ex.: `0 / 500`)
      - O estado expandido/recolhido padrão de um campo
      - Estado padrão selecionado de uma caixa de seleção visível
      - Rótulos de botão ao lado do campo
      - Mensagens de validação que aparecem em linha

   Para cada item &quot;up for review&quot;, forneça uma lógica de uma frase (&quot;Ajuda os novatos a planejar uma mensagem mais longa&quot;, &quot;Ajuda os usuários que não a veem em estágios posteriores a saberem expandi-la&quot;). Inclua apenas os itens que o usuário escolher. O princípio padrão é &quot;se o usuário puder vê-lo na tela enquanto está fazendo a tarefa, não reitere&quot; — mas o usuário recebe a chamada final.

5. **Propor edições.** Mostrar trechos antes/depois (ou uma descrição focalizada no estilo diff) do artigo, abrangendo: inserção de trechos, renomeações de cabeçalhos, novo conteúdo na Pré-visualização e onde ele se encontra, referência de captura de tela e quaisquer `class="preview"` wraps incorporados.

6. **Aguarde a aprovação explícita** (&quot;ok&quot;, &quot;apply&quot;, &quot;yes&quot;) antes de gravar o arquivo.

7. **Validar.** Depois de gravar, execute `ReadLints` no arquivo e relate quaisquer problemas. Leia novamente a seção alterada para confirmar a estrutura.

8. **Adiar edições em nível de prosa** para a habilidade **writing-quality**. Não refaça as regras de voz, capitalização, negrito ou padrões de link aqui. Leia `~/.cursor/skills/writing-quality/SKILL.md` se uma passagem de prosa for solicitada.

### &#x200B;5. Após cada artigo

Pergunte se deseja mover para o próximo artigo, parar, ignorar ou revisitar o atual.

### &#x200B;6. Fim de sessão — copiar/colar nota de versão

Quando o usuário terminar a sessão (diz &quot;concluído&quot;, &quot;é isso&quot;, &quot;parar&quot; ou não quer continuar no próximo artigo), pergunte:

> &quot;Deseja copiar/colar a entrada da nota de versão para a página de aprimoramento?&quot;

Em caso afirmativo, gere uma entrada de rascunho usando o contexto do recurso da etapa 1 e o artigo de ajuda principal atualizado nesta sessão. **Não o grave em nenhum arquivo** — forneça-o somente como copiar/colar texto.

Formate a entrada para corresponder à estrutura da página de área de produto da habilidade **notas-de-versão-formatter**:

```markdown
## {Feature name}

>[!NOTE]
>
>Preview: {date or TBD}
>Production fast release: {date or TBD}
>Production for everyone: {date or TBD}

{1–3 sentences describing what changed and why it helps users. Lead with the benefit, not the UI action.}

For more information, see [{Primary article title}](/help/quicksilver/{path-to-article}.md).
```

Regras:

- Use `TBD` para qualquer data ainda não conhecida; pergunte ao usuário se ele tem as datas.
- O nome do recurso é primeira letra maiúscula e os substantivos próprios.
- A descrição deve se concentrar no que os usuários agora podem fazer, não nos detalhes de implementação.
- O link para o artigo de instruções mais específico foi atualizado, não uma página de visão geral.
- Não inclua um bloco de datas `>[!NOTE]` se todas as datas forem desconhecidas e o usuário não quiser espaços reservados — omita-o e observe que ele precisa ser adicionado posteriormente.

## Regras de conteúdo

### Cabeçalhos

- Anexe exatamente **`in Production`** aos cabeçalhos de seção existentes que permanecem como referência do lado da produção.
- Acrescentar exatamente **`in Preview`** aos novos títulos de seção.
- Mantenha o restante do cabeçalho em maiúsculas e minúsculas (por `writing-quality`).

### Visualizar invólucros

- **Nível de seção**: quebra automática em `<div class="preview"> ... </div>`. Coloque tags de abertura e fechamento em suas próprias linhas, com uma linha em branco acima e abaixo de cada tag, de modo que os cabeçalhos e listas dentro ainda sejam renderizados.
- **Inline (nível de frase)**: quebra automática em `<span class="preview"> ... </span>` dentro do parágrafo, célula de tabela ou resposta da Pergunta frequente existente.
- Nunca aninhe um `<span class="preview">` dentro de um `<div class="preview">`.

### Posicionamento do trecho

- A linha de trecho vai imediatamente após o H1, com uma linha em branco acima e abaixo.
- O trecho fica **antes** do parágrafo de introdução, da chamada `>[!IMPORTANT]` e de qualquer bloco de requisitos de acesso.
- Um trecho por artigo.

### Capturas de tela

- Salve novas capturas de tela na pasta `assets/` do artigo com um nome de arquivo de caso kebab descritivo.
- Faça referência à nova captura de tela na nova seção Visualização. Se a captura de tela de uma seção em produção não refletir mais o recurso com precisão, deixe-a no lugar — ela ainda representa o comportamento de produção até a data de disponibilidade geral.
- Não fabrique nomes de arquivo de captura de tela; se nenhuma captura de tela tiver sido fornecida ainda, pergunte ao usuário.

### Notas e dicas

- Máximo de um `>[!NOTE]` (ou `>[!TIP]`, `>[!IMPORTANT]`, `>[!WARNING]`) por seção. Se a seção existente já tiver uma nota, combine o novo conteúdo relacionado na mesma nota como uma lista com marcadores em vez de empilhar.

### O que não fazer

- Não editar artigos em `product-announcements/`.
- Não edite em massa; um artigo de cada vez, com aprovação explícita a cada vez.
- Não inclua fatos observáveis da interface do usuário sem exibi-los ao usuário primeiro.
- Não modifique o conteúdo nos comentários do HTML `<!-- ... -->`, a menos que o usuário diga explicitamente para.
- Não altere `author:` ou campos de material de frente não relacionados.

## Verificações de qualidade antes de apresentar edições

- O trecho aparece uma vez, em sua própria linha, depois do H1, com linhas em branco acima e abaixo.
- Os cabeçalhos de seção existentes terminam com `in Production`.
- Os novos cabeçalhos de seção terminam com `in Preview` e a seção está dentro de `<div class="preview">`.
- Adições embutidas estão dentro de `<span class="preview">`.
- `ReadLints` está limpo no arquivo editado.
- O artigo é lido corretamente em ambos os estados (com o conteúdo da pré-visualização exibido e oculto).

## Referências

- Estilo da documentação do Workfront: consulte a habilidade **qualidade de escrita** em `~/.cursor/skills/writing-quality/SKILL.md`.
- Catálogo de trechos: `help/_includes/snippets.md` no repositório de documentos.
- Limpeza de GA (fluxo de trabalho inverso): consulte a habilidade **remove-preview-highlighting** em `.cursor/skills/remove-preview-highlighting/SKILL.md`.
- Adobe Wiki MCP para PRDs: servidor `user-Adobe Wiki Confluence`, ferramenta `get_wiki_content`.
