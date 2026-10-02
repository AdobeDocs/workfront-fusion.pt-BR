---
title: Módulo MCP do Adobe Marketo Engage
description: O módulo MCP do Adobe Marketo Engage permite enviar um prompt em linguagem natural para o servidor MCP (Model Context Protocol) do Adobe Marketo Engage.
author: Becky
feature: Workfront Fusion
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: e14a7f57-c82c-4874-a495-5d036cbbdc3d
    internal-label: Resource management
subfeature_v2:
  - id: b70a979b-965d-47a9-a360-e7ec2a19b8c1
    internal-label: Digital content and documents
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 9e08c421a53c7ca499715fa8e32be6c10fbde1d9
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 9%
---
# Módulo MCP do Adobe Marketo Engage

O módulo MCP do Adobe Marketo Engage permite enviar um prompt em linguagem natural para o servidor MCP (Model Context Protocol) da Adobe Marketo Engage, usando um modelo de IA para interpretar a solicitação e chamar as próprias ferramentas da Marketo para preenchê-la. Ao contrário de um conector Marketo tradicional, em que cada módulo executa uma ação fixa, como &quot;Criar um lead&quot;, esse conector tem um único módulo que aceita uma instrução aberta em inglês simples e permite que a IA decida quais operações do Marketo são necessárias para satisfazê-las.

Esse conector é especificamente para o próprio servidor MCP da Marketo Engage

Para se conectar a MCPs para outros aplicativos, consulte [Adicionar um prompt de IA ao seu cenário](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: disponível para organizações com licenças baseadas em operação</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

* Você deve ter uma conta do Adobe Marketo Engage e uma instância válida do Marketo.

## Conectar o Adobe Marketo Engage MCP ao Workfront Fusion {#connect-adobe-marketo-engage-mcp-to-workfront-fusion}

Você pode criar uma conexão com sua instância do Marketo diretamente de dentro do módulo MCP do Adobe Marketo Engage.

1. No módulo MCP do Adobe Marketo Engage, clique em **Adicionar** ao lado do campo **Conexão**.
1. Preencha os seguintes campos:

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Insira um nome para a nova conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Selecione se você está se conectando a um ambiente de produção ou não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>
          <p>Insira a ID do cliente para o serviço de API REST do Marketo, conforme criado no Marketo LaunchPoint.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>
          <p>Insira o Segredo do cliente do serviço de API REST do Marketo, conforme criado no Marketo LaunchPoint.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Munchkin ID]</td>
        <td>
          <p>Insira a Munchkin ID da sua instância do Marketo (por exemplo, "123-ABC-456"). A Munchkin ID é mostrada no Marketo em <b>Admin → Munchkin</b>.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Clique em **Continuar** para criar a conexão e retornar ao módulo.

>[!IMPORTANT]
>
> * Use um usuário Marketo dedicado somente à API com a função e as permissões mínimas necessárias para o cenário, em vez de reutilizar uma conta de administrador.
> * A criação da conexão não valida as credenciais. O Fusion os salva sem uma chamada de teste, de modo que a conexão pode parecer criada com sucesso mesmo se um valor estiver errado ou digitado incorretamente. Se uma credencial estiver incorreta, a falha geralmente aparecerá mais tarde quando o módulo tentar acessar o Marketo pela primeira vez ou quando as listas de ferramentas não forem carregadas.

## O módulo: &quot;Processar um prompt de usuário&quot;

Esse é o único módulo que o conector fornece. Um cenário o utiliza fornecendo:

1. **Conexão** — a conexão Marketo criada acima.
2. **Digite seu prompt** — a instrução, em inglês simples (por exemplo, &quot;encontre todos os clientes em potencial adicionados à lista de Webinários de primavera na semana passada e diga-me quais não têm nome de empresa definido&quot;).
3. **Ferramentas** (opcional) — descrito abaixo. Esses campos só aparecem depois que uma conexão é selecionada.
4. **Chave LLM** (opcional, avançada) — descrita abaixo.

Ele retorna a resposta final da IA como texto, além de uma trilha de auditoria completa do que aconteceu ao produzir essa resposta.

## Módulo MCP do Adobe Marketo Engage e seus campos

### Processar um prompt de usuário

Esse módulo de ação envia uma instrução em inglês simples para o servidor MCP do Adobe Marketo Engage e retorna a resposta da IA.

<table style="table-layout:auto"> 
 <col/>
 <col/>
 <tbody>
  <tr>
   <td role="rowheader">Chave LLM <i>(Opcional, avançada)</i></td>
   <td><p>Por padrão, esse módulo processa seu prompt usando o próprio serviço de IA da Adobe e você não precisa selecionar uma chave.</p><p>Para usar seu próprio provedor de IA, selecione uma chave LLM existente ou crie uma nova clicando em <b>Adicionar</b> e inserindo as seguintes informações:</p>
    <ul>
     <li><b>Nome da chave</b>: insira um nome para a nova chave.</li>
     <li><b>LLM</b>: selecione o modelo de idioma grande ao qual esta chave está associada. Os provedores compatíveis são OpenAI, Anthropic Claude e Amazon Bedrock.</li>
     <li><b>Chave</b>: insira ou mapeie sua chave de API para o provedor selecionado.</li>
     <li><b>Modelo</b>: selecione o modelo LLM que a chave usará.</li>
     <li><b>Outros campos</b>: insira valores para quaisquer outros campos exigidos pelo seu LLM.</li>
    </ul>
   </td>
  </tr>
  <tr>
   <td role="rowheader">Conexão</td>
   <td><p>Para obter instruções sobre como conectar sua conta do Marketo ao Workfront Fusion, consulte <a href="#connect-adobe-marketo-engage-mcp-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Marketo Engage MCP ao Workfront Fusion</a> neste artigo.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Prompt do usuário</td>
   <td><p>Insira ou mapeie a instrução, em inglês simples, que você deseja que a IA execute.</p><p>Exemplo: <i>Localize todos os clientes potenciais adicionados à lista de Webinários da primavera nos últimos 7 dias e resuma quais setores são mais comuns.</i></p></td>
  </tr>
 </tbody>
</table>

### Saída do módulo

A saída é um pacote único que contém o seguinte:

* Resposta: a resposta final da IA, como texto. Você pode mapear esses dados em módulos subsequentes.
* Trilha de auditoria: o registro detalhado da execução, incluindo uma ID de sessão, o prompt original, horas de início e término, duração total, status geral, a resposta final e uma lista de chamadas de ferramenta. Cada entrada de chamada de ferramenta registra qual ferramenta Marketo executou, seus argumentos, sua saída, sua hora e duração de início e término, se teve êxito e sua ordem na sequência.
* Resumo: A mesma execução condensada em contagens: total de chamadas de ferramenta, chamadas bem-sucedidas, chamadas com falha, tempo de processamento e status.

### Modelos de IA

Por padrão, o módulo usa o próprio serviço de IA gerenciada da Adobe automaticamente, sem chave ou credenciais para inserir.

Em vez disso, você pode selecionar uma chave LLM específica para usar OpenAI, Anthropic Claude ou Amazon Bedrock, se a sua organização tiver uma conta com uma dessas.

### Escolha de quais ações do Marketo a IA pode realizar

Depois que uma conexão é selecionada, o módulo pergunta ao servidor MCP do Marketo quais ferramentas ele oferece e as apresenta como listas de seleção múltipla, cada uma mostrando quantas ferramentas contém:

* Ferramentas somente leitura: ações que pesquisam apenas algo e nunca alteram nada, como encontrar um lead, listar membros da campanha ou ler os detalhes de um programa.
* Ferramentas de gravação/exclusão: ações que alteram algo, como criar ou atualizar um cliente potencial, adicionar alguém a uma lista, ativar uma campanha ou aprovar ou enviar um email.
* Outras ferramentas: uma terceira lista que aparece somente se o servidor do Marketo oferecer ferramentas que não foram rotuladas como somente leitura ou não. Elas são mostradas separadamente em vez de serem consideradas seguras ou inseguras. Se o servidor rotular tudo, essa lista não aparecerá.

Se nenhuma ferramenta for selecionada, a IA poderá usar todas elas. Você pode restringir uma lista a ações específicas. Por exemplo, selecionar apenas 2 ações &quot;gravar&quot; específicas, deixando apenas a opção &quot;somente leitura&quot;, significa que a IA pode pesquisar o que precisar livremente, mas só pode fazer esses dois tipos específicos de alterações. Deixar uma lista vazia significa que todas as ações nessa categoria são permitidas. A restrição da IA exige escolher ativamente quais ações específicas permitir nessa categoria. Dessa forma, você pode garantir que a IA não execute uma ação destrutiva inesperada contra dados de marketing em tempo real, enquanto ainda permite que ela colete informações livremente.

Como as listas são lidas em tempo real no servidor do Marketo, as ferramentas exatas mostradas podem mudar à medida que o Adobe atualiza esse servidor.

### Nenhum histórico de conversa persistente

Cada execução desse módulo é uma execução única e independente. A IA não pode fazer uma pergunta complementar e esperar uma resposta. Em vez disso, deve fazer o seu melhor julgamento e produzir uma resposta completa e definitiva numa única passagem. Se uma solicitação for ambígua, a IA fará uma suposição razoável, declarará essa suposição como parte de sua resposta e prosseguirá. Ele não vai parar e pedir ao usuário para esclarecer, porque não há como ele receber uma resposta em uma única execução.

A IA também é instruída a verificar os fatos com uma chamada de ferramenta em vez de depender da memória, pois os dados do Marketo podem ter sido alterados desde a execução anterior.

A IA só executa uma ação de gravação, atualização ou exclusão quando o prompt realmente solicita uma. Ele não executará uma ação que não foi solicitada, incluindo a ativação ou desativação de campanhas, a criação ou exclusão de clientes potenciais e listas e a aprovação ou envio de emails, mesmo que seja na mesma execução em que estiver fazendo algo que o usuário solicitou.

Como cada execução é independente, a IA não tem memória de uma execução anterior por si só. Um cenário que deseja uma experiência de bate-papo em várias rodadas deve fornecer explicitamente esse histórico como parte do novo prompt, armazenando a pergunta e a resposta anteriores no Data Store do Fusion ou transmitidas entre módulos e incluindo-o como texto no início do novo prompt, seguido da nova pergunta. Não há ID de sessão ou conversa que se lembre automaticamente de execuções anteriores.

## Exemplo de prompts

Você pode usar prompts como os seguintes:

* *Liste os clientes potenciais que ingressaram no programa &#39;Lançamento de Produto do 3º Trimestre&#39; nos últimos 7 dias e resuma de quais setores eles são.*
* *Verifique se a campanha inteligente &#39;Série de Boas-vindas&#39; está ativa no momento e diga quantas pessoas a ela pertencem.*
* *Localize o formulário usado em nossa página de preços e diga-me quais campos são marcados como obrigatórios.*
* *Adicionar o cliente potencial com email `jane@example.com` à lista estática &#39;Clientes do VIP&#39;.*
* *Resuma o desempenho de cada email no programa &#39;Spring Newsletter&#39;.*

<!--

## What a content writer should NOT claim

* Connection form: Do not describe the connection as an OAuth or "sign in with Adobe" flow. It is not one. It is three credential fields that the user copies out of Marketo's LaunchPoint and Munchkin admin pages. Screenshots or steps borrowed from the AEM MCP connector docs would be wrong here.
* Credential validation: Do not imply that the connection form validates the credentials. It saves them without testing them.
* Module scope: This is not a substitute for individual Marketo action modules. It is a single, flexible AI-driven module, not a set of deterministic single-purpose modules.
* Reliability: Results are AI-generated and can occasionally be imperfect, even with every safeguard above in place. This is appropriate for automation where a human is not reviewing every single run in real time, but it is not a guarantee of 100% deterministic behavior the way a traditional Marketo module is. This deserves extra emphasis for Marketo specifically, because a write action here can email real customers or alter real lead records.
* Tool restrictions: The read/write tool split limits what categories of Marketo actions the AI can take. It is not a way to sandbox or limit what the AI is capable of reasoning about or discussing in its answer text.
* Tool naming: Do not name specific Marketo MCP tools or actions unless they are verified against the live tool list. This document intentionally describes capability areas, such as leads, lists, campaigns, programs, emails, forms, snippets, and bulk operations, rather than exact tool names, since the server's exact tool set may evolve.
* API limits: Do not state Marketo API rate limits, quotas, or daily call caps as if this connector defines them. Any such limit comes from the user's own Marketo subscription and REST API allowance; verify with the Marketo team before publishing numbers.

## Reference links used while compiling this

* Adobe Marketo Engage MCP server (developer documentation):
  https://experienceleague.adobe.com/pt-br/docs/marketo-developer/marketo/mcp-server

  -->
