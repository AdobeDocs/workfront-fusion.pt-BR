---
title: Módulos MCP do Adobe Experience Manager
description: Com o módulo MCP do Adobe Experience Manager, você pode enviar um prompt em inglês simples para o servidor MCP do Adobe Experience Manager e permitir que um modelo de IA execute a solicitação.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 4c23409465b4be9fd10ff6938a750bc662ba2fe4
workflow-type: tm+mt
source-wordcount: 1020
ht-degree: 11%

---

# Módulos MCP do Adobe Experience Manager

O conector MCP do Adobe Experience Manager é uma integração dedicada do Fusion para o próprio servidor MCP (Model Context Protocol) da Adobe Experience Manager. Diferentemente de um conector típico, em que cada módulo executa uma ação fixa, esse conector tem um único módulo que aceita uma instrução em inglês simples e aberta e permite que um modelo de IA decida quais operações do Adobe Experience Manager são necessárias para cumpri-la, em áreas como sites, ativos digitais, fragmentos de conteúdo, pastas, o repositório de conteúdo e IA de conteúdo.

Esse conector é dedicado ao próprio servidor MCP da Adobe Experience Manager. Ele não oferece suporte a outros servidores MCP não relacionados. Para um conector que você pode apontar para qualquer servidor MCP, use o conector do Agente MCP.

Para obter informações sobre o conector do Agente MCP, consulte [módulo do Agente MCP](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).

>[!NOTE]
>
>As respostas desse módulo são geradas por IA e, ocasionalmente, podem ser imperfeitas, mesmo com todas as proteções disponíveis em vigor. Esse módulo é apropriado para automação em que um humano não está revisando todas as execuções em tempo real, mas não é uma garantia do comportamento determinístico que você obteria de um módulo tradicional do Adobe Experience Manager.

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

* Você deve ter uma conta da Adobe Experience Manager para usar este módulo.

## Conectar o Adobe Experience Manager MCP ao Workfront Fusion {#connect-adobe-experience-manager-mcp-to-workfront-fusion}

O conector MCP do Adobe Experience Manager usa o OAuth para se conectar ao Adobe Experience Manager. Não há campos de conexão para preencher manualmente, como nome de usuário, senha ou chave de API.

Para criar uma conexão:

1. No módulo MCP do Adobe Experience Manager, clique em **[!UICONTROL Adicionar]** ao lado do campo Conexão.
1. Selecione se você está se conectando a um ambiente de Produção ou Não produção.
1. Selecione se você está se conectando a uma conta de Serviço ou a uma conta Pessoal
1. Clique em **Continuar**.

   Você é redirecionado para a página de logon do Adobe.
1. Na página de logon da Adobe, faça logon e aprove o acesso.

Você será redirecionado de volta para o Workfront Fusion e a nova conexão estará disponível no módulo.

## Módulo MCP do Adobe Experience Manager e seus campos

No momento, há apenas um módulo no conector MCP do Adobe Experience Manager.

### Processar um prompt de usuário

Esse módulo de ação envia uma instrução em inglês simples para o servidor MCP do Adobe Experience Manager e retorna a resposta da IA.

Cada execução desse módulo é uma execução única e independente, semelhante a enviar um email em vez de ter uma conversa em tempo real. A IA não pode fazer uma pergunta complementar e aguardar sua resposta. Em vez disso, faz o seu melhor julgamento e retorna uma resposta completa. Se o seu prompt for ambíguo, a IA declara qualquer suposição que fez como parte de sua resposta, em vez de parar para solicitar que você esclareça.

>[!IMPORTANT]
>
>Esse módulo só executa uma ação de gravação ou exclusão quando o prompt realmente solicita uma. Ele não executa nenhuma ação extra que você não solicitou, mesmo na mesma execução em que ele está realizando algo mais que você pediu.

Como cada execução é independente, o módulo não tem memória de execuções anteriores por si só. Para criar uma experiência de conversação com vários turnos em várias execuções, armazene a pergunta e a resposta anteriores. Você pode usar um Armazenamento de dados para isso e, em seguida, incluir esse histórico como texto no início do próximo prompt, seguido da nova pergunta.

Para obter informações sobre Repositórios de Dados, consulte [Repositório de Dados](/help/workfront-fusion/create-scenarios/data-stores/data-store-overview.md).

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
   <td><p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-mcp-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager MCP ao Workfront Fusion</a> neste artigo.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Prompt do usuário</td>
   <td><p>Insira ou mapeie a instrução, em inglês simples, que você deseja que a IA execute.</p><p>Exemplo: <i>Localize todos os ativos na pasta de marketing que não foram atualizados em 90 dias.</i></p></td>
  </tr>
  <tr>
   <td role="rowheader">Ferramentas somente leitura <i>(Opcional)</i></td>
   <td><p>Restringir quais ações do Adobe Experience Manager somente leitura a IA pode chamar — ações que procuram apenas algo, como localizar um ativo ou ler o conteúdo de uma página, e nunca alteram nada.</p><p>Se você deixar esse campo vazio, todas as ações somente leitura serão permitidas.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Ferramentas de gravação/exclusão <i>(Opcional)</i></td>
   <td><p>Restringir quais ações de gravação ou exclusão do Adobe Experience Manager a IA pode chamar — ações que alteram algo, como atualizar uma página, publicar conteúdo ou excluir um ativo.</p><p>Se deixar esse campo vazio, todas as ações de gravação e exclusão serão permitidas. Para garantir que um cenário autônomo nunca execute uma ação destrutiva, recomendamos deixar esse campo definido como uma seleção deliberadamente vazia, em vez de deixá-lo irrestrito.</p></td>
  </tr>
 </tbody>
</table>

O módulo retorna a resposta final da IA, como texto, juntamente com um registro do que aconteceu ao produzir essa resposta, incluindo quais ferramentas foram chamadas, se cada chamada teve êxito e quanto tempo o processamento levou.
