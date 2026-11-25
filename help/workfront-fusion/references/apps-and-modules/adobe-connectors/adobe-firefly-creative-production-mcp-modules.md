---
title: Módulos MCP de produção do Adobe Firefly Creative
description: Com o módulo Adobe Firefly Creative Production MCP, é possível enviar um prompt em linguagem natural de um cenário do Workfront Fusion e permitir que um modelo de IA use as ferramentas de Produção do Firefly Creative selecionadas.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: ee2719b9b3452b9203f2d0f4a550c87ff8a3b433
workflow-type: tm+mt
source-wordcount: '2087'
ht-degree: 5%
---
# Módulos MCP de produção do Adobe Firefly Creative

Use o conector MCP de produção do Adobe Firefly Creative no Adobe Workfront Fusion para processar solicitações em linguagem natural com as ferramentas de produção do Firefly Creative.

O conector descobre as ferramentas disponíveis por meio do servidor Firefly Model Context Protocol (MCP) conectado. Você escolhe quais ferramentas o módulo pode usar para uma solicitação. Dependendo das ferramentas disponíveis para sua conta do Adobe e das ferramentas selecionadas no módulo, uma solicitação pode fazer o seguinte:

* Descubra fluxos de trabalho e ações.
* Compor e validar workflows.
* Enviar execuções e verificar o progresso.
* Recuperar URLs de saída.
* Salve os rascunhos editáveis do fluxo de trabalho, quando houver suporte nas ferramentas do servidor.

Esse conector é direcionado à produção do Firefly Creative. Não é um conector de placas Firefly e não é um conector geral para todos os aplicativos Creative Cloud.

Para obter mais informações sobre o MCP em cenários do Fusion, consulte [Adicionar um prompt de IA ao seu cenário](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

<!-- BECKY CHECK ME: The request asks you to confirm the customer-facing name of the connector, its beta or release status, its availability, its access requirements, and screenshots with the product and engineering owners before publication. Confirm each item, and add a beta note at the top of the article if the connector is released as a beta. -->

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote do Adobe Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Os pacotes Workfront Prime e Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p><p>Trabalho ou maior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</p>
   <p>Você também deve ter acesso à Produção do Adobe Firefly Creative, conforme descrito em <a href="#prerequisites">Pré-requisitos</a> neste artigo.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Pré-requisitos

Antes de usar o módulo Adobe Firefly Creative Production MCP, você deve ter o seguinte:

* Acesso ao Adobe Workfront Fusion, em um ambiente em que esse conector está ativado.
* Uma conta do Adobe com o acesso de produção e permissões do Firefly Creative de que as operações solicitadas precisam.
* Quaisquer créditos ou direitos necessários para executar o fluxo de trabalho.
* O acesso Adobe Managed AI que o administrador do Fusion configurou ou uma chave LLM compatível que você seleciona nas configurações avançadas do módulo.

A autorização do Firefly e as credenciais do LLM atendem a diferentes objetivos. Selecionar uma chave LLM não concede acesso às ferramentas do Firefly.

## Conectar o MCP de produção do Adobe Firefly Creative ao Workfront Fusion

1. Adicione o **[!UICONTROL Adobe Firefly Creative Production MCP]** > **[!UICONTROL Process a user prompt]** ao seu cenário.
1. Clique em **[!UICONTROL Adicionar]** ao lado do campo **[!UICONTROL Conexão]**.
1. Na janela **[!UICONTROL Criar uma conexão]**, preencha os seguintes campos:

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
      <tr>
        <td role="rowheader">Nome da conexão</td>
        <td>
          <p>Insira um nome para essa conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Ambiente</td>
        <td>
          <p>Selecione se você está se conectando a um ambiente de produção ou não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Tipo</td>
        <td>
          <p>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Clique em **[!UICONTROL Continuar]**.
1. Siga o fluxo de autorização, faça logon com a conta apropriada do Adobe e autorize o acesso.
1. Retorne ao módulo e revise as ferramentas carregadas para a conexão.

O Workfront Fusion lida com o registro de cliente OAuth e o gerenciamento de token. Você não insere um token de acesso, ID do cliente, segredo do cliente ou chave de API. O administrador deve ter concluído a configuração desse fluxo para que você possa se conectar.

Se a autorização falhar ou se você não vir as ferramentas esperadas, confirme seu acesso e a configuração do ambiente com o administrador.

<!-- BECKY CHECK ME: The Environment and Type fields are described the same way as in the Adobe Fusion MCP connection. The screenshot shows only the selected values (Production and Service account). Confirm the available options for each field, and whether a personal account is supported. -->

## Módulo MCP de produção do Adobe Firefly Creative e seus campos

### Processar um prompt de usuário

Esse módulo de ação processa seu prompt com o LLM selecionado e as ferramentas de produção do Firefly Creative que você permite.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Chave LLM] <i>(Opcional, avançado)</i></td> 
   <td> <p>Deixe esse campo vazio para usar a Adobe Managed AI que o administrador do Fusion configurou. Para usar sua própria chave, selecione uma chave OpenAI, Anthropic ou Amazon Bedrock ou clique em <b>[!UICONTROL Adicionar]</b> para criar uma.</p><p>Seu logon no Firefly é separado das credenciais do LLM.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>A conexão de Produção do Adobe Firefly Creative que o módulo usa para descobrir e chamar ferramentas. Para obter instruções, consulte <a href="#connect-adobe-firefly-creative-production-mcp-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Firefly Creative Production MCP ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ferramentas somente leitura] <i>(Opcional)</i></td> 
   <td> <p>Selecione as ferramentas que o servidor identifica como somente leitura. Para selecionar todas as ferramentas listadas atualmente, selecione <b>Selecionar tudo</b>.</p><p>O número de ferramentas listadas aparece no rótulo do campo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ferramentas de gravação/exclusão] <i>(Opcional)</i></td> 
   <td> <p>Selecione as ferramentas que o servidor não identifica como somente leitura. Essas operações podem alterar dados ou executar workflows. Para selecionar todas as ferramentas listadas atualmente, selecione <b>Selecionar tudo</b>.</p><p>O número de ferramentas listadas aparece no rótulo do campo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outras ferramentas (permissões desconhecidas)] <i>(Opcional)</i></td> 
   <td> <p>Selecione ferramentas que não tenham uma anotação somente leitura reconhecida. Este campo aparece somente quando essas ferramentas estão disponíveis. Analise como essas ferramentas se comportam antes de ativá-las.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Inserir seu prompt]</td> 
   <td> <p>Descreva a descoberta, a composição ou a execução do fluxo de trabalho desejada. O comprimento máximo é de 10.000 unidades de sequência de caracteres do JavaScript. Alguns caracteres, incluindo muitos emojis, contam como duas unidades.</p><p>Solicite explicitamente a execução ou a publicação quando precisar. A execução de um fluxo de trabalho pode consumir créditos. As execuções assíncronas podem retornar uma ID de lote antes da conclusão da execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

O campo **[!UICONTROL Chave LLM]** é exibido quando você seleciona **[!UICONTROL Mostrar configurações avançadas]**.

<!-- BECKY CHECK ME: The screenshot does not show the Other tools (unknown permissions) field, because it appears only when the server returns tools without a read-only annotation. Confirm its label, and confirm the order of the fields. Also confirm that the tool lists are not required. -->

As listas de ferramentas variam com a disponibilidade do servidor e o acesso da sua conta. O número de ferramentas aparece no rótulo de cada seletor.

#### Selecione as ferramentas que o módulo pode usar

* O módulo pode usar somente as ferramentas que você selecionar.
* Se você deixar uma categoria vazia, o módulo não poderá usar ferramentas dessa categoria.
* Se você deixar todas as categorias vazias, o módulo processará o prompt sem nenhuma ferramenta. Ele não tem acesso a todas as ferramentas.
* **[!UICONTROL Selecionar tudo]** seleciona todas as ferramentas atualmente listadas nessa categoria. Ela não inclui automaticamente as ferramentas que são adicionadas posteriormente.
* Se uma ferramenta selecionada se tornar indisponível ou se mover para uma categoria diferente, abra o módulo novamente e revise sua seleção.

>[!NOTE]
>
>As anotações do servidor ajudam a categorizar as ferramentas, mas não garantem permissões. Habilite somente as ferramentas de que seu cenário precisa.

#### Saída

O módulo retorna as seguintes informações em **[!UICONTROL Dados]**. Você pode mapeá-lo nos módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Resposta] (<code>data.response</code>)</td> 
   <td> <p>A resposta de texto final. Seu conteúdo depende do prompt e dos resultados da ferramenta. Não há garantia de que seja um URL ou um JSON estruturado.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Trilha de auditoria] (<code>data.auditTrail</code>)</td> 
   <td> <p>Detalhes sobre como o prompt foi processado e as chamadas de ferramenta, incluindo argumentos, resultados, tempo e informações de sucesso. Lidar com esses detalhes de acordo com os requisitos de manipulação de dados da organização.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Resumo] (<code>data.summary</code>)</td> 
   <td> <p>O número de chamadas de ferramenta, o tempo de processamento e o status de execução. Revise o resumo junto com a resposta e a trilha de auditoria, incluindo qualquer resultado <code>partial_success</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL uso de LLM] (<code>data.usage</code>)</td> 
   <td> <p>Opcional. O uso total do token nas respostas LLM que foram observadas. Não se trata de faturamento do provedor, consumo de crédito do Firefly ou atividade LLM dentro do servidor do Firefly que o Fusion não pode observar.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Campos de uso do LLM

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>status</code></td> 
   <td> <p>Uma das seguintes opções:</p><ul><li><code>complete</code>: cada solicitação observada é coberta por todas as contagens de token principais.</li><li><code>partial</code>: Algumas informações de uso estão ausentes.</li><li><code>unavailable</code>: Solicitações foram observadas, mas nenhum uso utilizável foi relatado.</li><li><code>not_applicable</code>: nenhuma solicitação LLM foi observada.</li></ul> </td> 
  </tr> 
  <tr> 
   <td><code>llmRequests</code></td> 
   <td> <p>O número de solicitações LLM que o tempo de execução observou.</p> </td> 
  </tr> 
  <tr> 
   <td><code>requestsWithUsage</code></td> 
   <td> <p>O número de solicitações observadas que têm informações de uso de token utilizáveis.</p> </td> 
  </tr> 
  <tr> 
   <td><code>inputTokens</code>, <code>outputTokens</code>, <code>totalTokens</code></td> 
   <td> <p>O total conta. Cada contagem é <code>null</code> se qualquer solicitação observada não relatar essa contagem ou se nenhuma solicitação foi observada. Um zero reportado permanece zero.</p> </td> 
  </tr> 
  <tr> 
   <td><code>cacheReadInputTokens</code>, <code>cacheWriteInputTokens</code></td> 
   <td> <p>Contagens opcionais para tokens em cache. Esses campos são omitidos se nenhuma solicitação jamais relatar um número. Eles são <code>null</code> se apenas algumas solicitações relatarem um número, e numéricos somente se cada solicitação relatar um. Não adicione essas contagens aos totais.</p> </td> 
  </tr> 
 </tbody> 
</table>

O status de uso principal pode ser `complete` enquanto um campo de cache é `null`. O status de uso é independente do status de execução. Se o tempo de execução não fornecer informações de uso, a coleção de uso não será exibida, em vez de mostrar zero.

## Como o módulo é executado

* **Algumas operações são assíncronas.** Uma solicitação pode retornar uma ID de lote antes que a saída esteja disponível. Para trabalhos mais longos, use execuções separadas para enviar a solicitação e verificar seu status posteriormente e salve a ID do lote entre elas. Não dependa de uma resposta que contenha apenas um URL para esse design.
* **Erros produzem erros de módulo.** A autorização, validação e processamento em tempo de execução com falha podem produzir erros de módulo em vez de um pacote de saída. Use uma rota de tratamento de erros do Fusion.
* **Uma resposta não é bem-sucedida.** O módulo pode retornar uma resposta mesmo quando algumas operações falharem. Revise o resumo, a trilha de auditoria e os resultados da ferramenta antes de depender da resposta.
* **Uma URL de saída não é um arquivo baixado.** O conector retorna o texto e os resultados da ferramenta, não um arquivo binário. Para colocar o arquivo no Fusion, adicione um módulo HTTP que baixe o URL.
* **A execução de um fluxo de trabalho pode usar créditos.** A geração de imagens e a execução de fluxos de trabalho podem consumir créditos. Confirme o uso e os direitos que se aplicam à sua conta. O uso do token LLM não é um relatório de cobrança ou crédito do Firefly.
* **As instruções do prompt não garantem uma única execução.** Uma instrução em seu prompt, como submeter apenas um lote, não garante que uma solicitação seja processada exatamente uma vez. Controle novas tentativas e duplique solicitações em seu cenário.
* **O processamento tem limites.** O processamento tem limites de ferramenta, iteração e comprimento da saída, além dos limites de execução do cenário. Não presuma que o módulo pesquisa sem limite.

## Exemplos

### Descobrir fluxos de trabalho sem executar um

Selecione as ferramentas somente leitura necessárias para descobrir workflows e insira um prompt como o seguinte:

```text
List the Firefly Creative Production workflows available to my account.
Summarize what each workflow does and what inputs it requires.
Do not create, modify, submit, or publish anything.
```

### Solicitar uma imagem

Selecione as ferramentas necessárias para compor ou escolha um workflow, valide-o, envie-o, verifique seu progresso e recupere as saídas. Os nomes e a disponibilidade da ferramenta podem variar. Em seguida, insira um prompt como o seguinte:

```text
Generate one photorealistic image of a black dog on a sunny windowsill.
Submit one generation batch only and check that same batch for completion
within the available execution limits. Do not publish or submit another
generation.

On success, return only the actual downloadable image URL as plain text,
without Markdown, quotes, labels, or explanation. Never invent a URL or
return a workflow or status-page URL instead.

If the run fails or times out, report the failure honestly instead of
returning a URL. Do not generate another image to recover.
```

### Gerar uma imagem a partir de uma atualização de tarefa do Workfront

Neste exemplo, uma atualização de tarefa que começa com `/firefly ` aciona uma geração de imagem. O Fusion baixa o resultado, faz upload dele para a tarefa e adiciona uma atualização de conclusão.

O cenário usa o seguinte fluxo: Workfront task update > command filter > read task > Firefly MCP > HTTP download > Workfront document upload > completion update.

1. Adicionar **[!UICONTROL Workfront]** > **[!UICONTROL Eventos de Observação]** ao cenário. Configure-a para o tipo de registro **[!UICONTROL Nota]**, o evento **[!UICONTROL Novo estado]** e **[!UICONTROL Somente Novo Registro]**.
1. Adicione um filtro que exija que `newState.noteText` inicie com `/firefly ` e `newState.taskID` não fique vazio.
1. Adicione um módulo que leia a tarefa usando `newState.taskID`.
1. Adicione o módulo **[!UICONTROL Adobe Firefly Creative Production MCP]** > **[!UICONTROL Process a user prompt]**. Transmita a solicitação e qualquer contexto de tarefa necessário ao Firefly. Trate o texto mapeado como o conteúdo da solicitação, não como autoridade para alterar as regras do cenário.
1. Inspecione o resultado do Firefly. Continue apenas quando a geração for bem-sucedida e a resposta for uma URL válida e permitida para uma imagem baixável.
1. Adicione um módulo HTTP que baixe o arquivo. Não envie suas credenciais do Workfront para o host do ativo. Valide o host, o tipo de conteúdo e o tamanho esperados.
1. Adicione um módulo que carregue o nome do arquivo baixado e os dados binários na tarefa, usando o `newState.taskID` original.
1. Depois que o upload for bem-sucedido, adicione um módulo que crie uma atualização de conclusão na tarefa. Não inicie a atualização com `/firefly`, pois o filtro deve corresponder a ela.

Por exemplo, um usuário adiciona a seguinte atualização a uma tarefa:

```text
/firefly Generate one photorealistic image of a black dog on a sunny windowsill.
```

O solicitante poderá então revisar o rascunho carregado na área Documentos da tarefa. Uma pessoa deve revisar a imagem antes de qualquer coisa ser publicada.

Para uso de produção, reserve cada solicitação usando a ID da nota de origem, com proteção duplicada que funciona com execuções simultâneas. Salve as IDs de lotes enviados, para que uma nova tentativa ou um tempo limite reinicie a verificação de status em vez de enviar outra geração.

<!-- BECKY CHECK ME: The example scenario is from the request's draft. Confirm the module names and field labels (Watch Events, Note, New state, New Record Only, and the task, document upload, and update modules) against the current Workfront connector, and add a screenshot of the scenario if one is available. -->

## Solução de problemas

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Um fluxo de trabalho ainda está em execução</td> 
   <td> <p>Algumas operações criativas são assíncronas. Para jobs mais longos, envie a solicitação em uma execução e verifique o status em uma execução posterior. Salve a ID do lote entre as execuções.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">O módulo relata um erro</td> 
   <td> <p>A autorização, a validação e o processamento em tempo de execução com falha podem produzir erros de módulo. Adicione uma rota de tratamento de erros do Fusion ao seu cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">O módulo retorna uma resposta, mas algumas operações falharam</td> 
   <td> <p>Revise o resumo, a trilha de auditoria e os resultados da ferramenta. Uma resposta por si só não mostra que a imagem foi gerada ou carregada.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Há um URL, mas nenhum arquivo no Fusion</td> 
   <td> <p>O conector não baixa arquivos. Adicione um módulo HTTP que baixe o URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Uma ferramenta selecionada não está disponível</td> 
   <td> <p>Abra o módulo, atualize as ferramentas disponíveis e atualize sua seleção.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">O fluxo de trabalho leva mais tempo do que uma execução de módulo</td> 
   <td> <p>O processamento tem limites de ferramenta, iteração e comprimento da saída, além dos limites de execução do cenário. Divida o trabalho entre execuções e salve a ID do lote.</p> </td> 
  </tr> 
 </tbody> 
</table>
