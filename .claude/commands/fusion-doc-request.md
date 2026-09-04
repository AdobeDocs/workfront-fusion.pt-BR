---
name: fusion-doc-request
description: Lide com uma solicitação de documentação do Fusion a partir do modelo
source-git-commit: 6726c582294758de0bbab19d6014ad80bb66e553
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---


# Solicitação de documentação do Fusion

Lida com a &quot;Nova solicitação de documentação do padrão {person}&quot; recorrente postada no canal do Slack `#fusion-documentation`: leia a solicitação, atualize os documentos e crie uma tarefa de rastreamento no mesmo formulário personalizado do Workfront usado para cada solicitação anterior desse tipo.

Este fluxo de trabalho é diferente da habilidade `fusion-release-notes`. Essa habilidade atualiza um artigo de referência e cria uma tarefa do Workfront; ela não cria ou atualiza uma página de nota de versão semanal do Fusion neste repositório, mesmo se a solicitação disser &quot;Precisa de anúncio: Sim&quot;. Use o `fusion-release-notes` somente se o usuário solicitar separadamente uma nota de versão semanal.

## Etapa 1: obter os detalhes da solicitação

Se receber um link do Slack, analise `channel_id` e `message_ts` da URL e busque o thread (`slack_get_thread_replies` ou `slack_read_thread`, dependendo da ferramenta MCP do Slack conectada - tente ambos se um falhar). Mantenha o link/URL permanente do thread - ele é necessário na Etapa 3.

As conexões do Slack neste ambiente são irregulares (tokens expirados, desconexões no meio da sessão). Se uma busca falhar:
- Tente novamente uma vez.
- Se ainda falhar, informe ao usuário claramente que a busca falhou e peça para ele colar o conteúdo da solicitação diretamente. Não adivinhe o conteúdo, e não desista silenciosamente sem dizer isso.

O modelo de solicitação tem estes campos - extraia cada um:

* **Título do recurso**
* **Descrição**
* **Pontos a serem adicionados à documentação** *(às vezes presente - seções/detalhes específicos que o solicitante deseja cobrir; trate-os como obrigatórios, não opcionais, se fornecidos)*
* **Data de lançamento esperada**
* **Precisa de notificação** *(Sim/Não - apenas informativo; consulte a observação acima. Não atue neste campo.)*

Se a solicitação for vinculada a uma página wiki Confluence com a especificação completa, busque (`get_wiki_content`) antes de gravar a documentação. Não dependa apenas do resumo do Slack para obter detalhes técnicos (nomes exatos de campo, etapas, rótulos de interface do usuário), extraia-os da especificação do wiki quando um estiver vinculado.

Se, em vez disso, a solicitação for vinculada a uma fonte secundária de não Confluência (por exemplo, uma publicação da Experience League Community, um artigo de suporte, um resumo gerado por IA) em vez de uma especificação autoritativa, você poderá usá-la para preencher detalhes técnicos que o texto do Slack não contiver, mas tratá-la como menos confiável do que a própria solicitação do Slack. Quando estiver em conflito com ou for adicionado ao texto do Slack (um nome diferente para o mesmo botão/campo, um detalhe não mencionado no Slack), não escolha silenciosamente um - escreva o documento usando o texto da solicitação do Slack como fonte principal e sinalize a discrepância em linha com um comentário do HTML (por exemplo, `<!-- BECKY CHECK ME: Slack calls this "Activate," but the linked community post calls it "Reactivate" - confirm against the live UI. -->`) de acordo com as orientações da Etapa 2.

## Etapa 2: atualizar a documentação

Encontre os artigos relevantes existentes neste repositório (grep para nomes de módulo relacionados, rótulos de interface do usuário ou nomes de configurações - não adivinhe o arquivo). Atualize-os para refletir a alteração, seguindo a estrutura existente, o nível do título e o estilo da casa desse artigo.

* Não invente detalhes técnicos (nomes de campos exatos, escopos de permissão, etapas de configuração) que não estejam na solicitação do Slack ou na especificação da wiki vinculada. Se algo não for confirmado, marque-o como um comentário do HTML (por exemplo, `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`), em vez de adivinhar - nunca como uma chamada visível. Ela não deve ser renderizada na página publicada.
* Se isso exigir um arquivo de artigo totalmente novo (não apenas uma edição para um existente), siga as convenções permanentes deste repositório: nenhum `exl-id`/`TQID` fabricado na frente e converta o arquivo para CRLF/sem BOM após criá-lo (o padrão da ferramenta `Write` é LF).
* Conectar uma nova página ao &quot;índice&quot; significa AMBOS, não apenas um. Uma página pode ser vinculada a partir de um subíndice, mas ainda ser invisível para os leitores:
  - O arquivo de navegação mestre da área do produto (por exemplo, `help/workfront-fusion/TOC.md`). Ele é o que realmente direciona a árvore de navegação publicada.
  - Qualquer subíndice do conteúdo interno/página de aterrissagem que também vincule a artigos desse tipo (por exemplo, `apps-and-modules-toc.md` para uma nova página de módulos do conector).
    Verifique explicitamente e confirme se a nova entrada está na mesma lista, no mesmo nível de aninhamento, já que seus artigos semelhantes mais próximos em cada arquivo - não suponha que adicioná-la a uma cubra a outra.

## Etapa 3: criar a tarefa do Workfront

Projeto: **Tarefas de documentação do produto - para problemas de desenvolvimento que exigem mensagens**. Resolva sua ID com `insights_find_id_by_name` (entidade `project`) em vez de codificá-la, caso ela mude - consulte Valores conhecidos abaixo para obter a última ID resolvida.

Campos de tarefa:

| Campo | Valor |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | da pesquisa de projeto acima |
| `parentID` | a ID da tarefa pai (`parentID`, um campo do sistema - sem prefixo `DE:`) - consulte Valores conhecidos abaixo. Isso torna a nova tarefa uma subtarefa, não uma tarefa de nível superior no projeto. |
| `assignedToID` | o usuário atual, de `insights_get_current_user` |
| `categoryID` | a ID de formulário personalizado da Documentação do produto - consulte Valores conhecidos abaixo. Se não estiver claro, consulte `task.task_categoryID` em qualquer tarefa irmã recente neste projeto para confirmar. |
| `description` | o **texto completo da mensagem do Slack** (todos os campos do modelo de solicitação, não uma paráfrase), seguido de um link para a conversa do Slack |
| `DE:Release notes` | uma nota de versão formatada, consulte o formato abaixo |
| `DE:Preview Date Known` | `Yes`, por padrão |
| `DE:Preview Date` | a **data de lançamento esperada** da solicitação, por padrão |
| Produto/Área | selecionar `Fusion` (um campo de enumeração no formulário Documentação do produto; confirme o nome exato do campo com `insights_search_fields` se ele nunca estiver claro) |

Defina os campos de data de visualização como parte dessa mesma chamada de criação - não os deixe para depois ou aguarde para ser solicitado. Se o usuário fornecer uma data diferente posteriormente ou se disser que a data ainda não é realmente conhecida, atualize de acordo, mas use o padrão para preenchê-las sempre.

Formato da nota de versão para o campo `DE:Release notes`. Sempre comece com `***FUSION***` em sua própria linha, em seguida, uma linha em branco e, em seguida, o título. Isso marca a nota como pertencente ao Fusion (em vez do Core Workfront) rapidamente:

```markdown
***FUSION***

## {Feature Title}

{Description of what changed and why it matters, in second person. A sentence or two is enough for a simple change - use multiple paragraphs and/or a bulleted list for anything with several parts or steps, the same way a full weekly release note would.}

For more information, see [{Article title}](/help/workfront-fusion/{path-to-article}.md).
```

Antes de criar a chamada, chame `read_workflow_docs` com `workfront://tools/create-any-object`. Essa chamada define campos personalizados e um valor de enumeração (`DE:Preview Date Known`), o que exige isso de acordo com as regras do servidor MCP.

## Etapa 4: Confirmar ao usuário

Relatar claramente:

* Quais arquivos de documento você alterou e o que adicionou.
* O nome da tarefa e o URL.
* Os valores exatos do campo definidos, incluindo os campos de data de visualização.
* Qualquer coisa com a qual você não tivesse total confiança, por exemplo, o Slack estava inacessível e você trabalhava somente com texto colado, o artigo de documento de destino era ambíguo ou um detalhe técnico não estava no material de origem e foi sinalizado em vez de adivinhado.

## Valores conhecidos (de execuções anteriores)

Confirme se eles ainda estão resolvidos, em vez de supor que sejam permanentes:

* O projeto &quot;Tarefas de documentação do produto - para problemas de desenvolvimento que exigem mensagens&quot; mapeia para a ID `5e69583f00236b9f767c3e3944100ee4`
* A tarefa pai &quot;Becky - Tarefas do canal Fusion-Documentation&quot; mapeia para a ID `6a9b065100003a7554832780c2015e93` (no mesmo projeto) - resolver com `insights_find_id_by_name` (entidade `task`) em vez de codificar, caso seja alterada
* O formulário personalizado (`categoryID`) da Documentação do produto é `5d7275b9000514604bd969d418725843`
* Campos personalizados usados: `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`
