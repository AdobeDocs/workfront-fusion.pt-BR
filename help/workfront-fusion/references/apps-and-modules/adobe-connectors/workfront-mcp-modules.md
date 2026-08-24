---
title: Módulos MCP do Adobe Workfront
description: Com o módulo MCP do Adobe Workfront, você pode enviar um prompt em inglês simples para o servidor MCP do Adobe Workfront e permitir que um modelo de IA execute a solicitação.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 88515edc81bafe2d1a81df627fd51dd4ed674c02
workflow-type: tm+mt
source-wordcount: 884
ht-degree: 16%

---

# Módulos MCP do Adobe Workfront

O conector MCP do Adobe Workfront é uma integração dedicada do Fusion para o próprio servidor MCP (Model Context Protocol) da Adobe Workfront. Ao contrário de um conector típico, em que cada módulo executa uma ação fixa, esse conector tem um único módulo que aceita uma instrução em inglês simples e aberta e permite que um modelo de IA decida quais operações do Workfront são necessárias para cumpri-la.

Por exemplo, você pode entrar no prompt &quot;Encontrar todos os meus projetos ativos que estão atrasados no cronograma e resumir seu status&quot;, e o módulo retorna uma resposta sintetizada, em vez de ter que encadear vários módulos Get e Filter.

Você pode restringir quais ações do Workfront a IA pode realizar, de modo que mesmo um cenário autônomo possa garantir que nenhuma ação destrutiva inesperada seja executada.

Por padrão, esse módulo usa o Adobe Managed AI, que usa o modelo `claude-sonnet-5`. Você pode configurar o módulo para usar um LLM diferente, usando uma chave e outras credenciais fornecidas.

>[!NOTE]
>
>O uso do Adobe Managed AI é limitado a US$ 25 por organização, por mês.

Para obter mais informações sobre o MCP em cenários do Fusion, consulte [Adicionar um prompt de IA ao seu cenário](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conectar o Adobe Workfront MCP ao Workfront Fusion

O conector MCP do Adobe Workfront usa o OAuth 2.0 para se conectar ao Workfront. Ao contrário de outros conectores do Workfront, não há campos de conexão manual, como host, ID do cliente ou Segredo do cliente a serem preenchidos.

Para criar uma conexão:

1. No módulo MCP do Adobe Workfront, clique em **[!UICONTROL Adicionar]** ao lado do campo Conexão.
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
          <p>Insira um nome para essa conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
      </tr>
    </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

   Se você não estiver conectado ao Workfront, será direcionado para uma tela de logon. Faça logon e aprove o acesso.

Você será redirecionado de volta para o Workfront Fusion e a nova conexão estará disponível no módulo.

>[!NOTE]
>
>Na primeira utilização, a conexão se registra automaticamente no servidor MCP do Workfront e reutiliza esse registro para cada conexão subsequente que você criar.

## Módulo MCP do Adobe Workfront e seus campos

### Processar um prompt de usuário

Esse módulo de ação processa um prompt em inglês simples no servidor MCP do Workfront, usando o modelo de idioma especificado, e retorna a resposta da IA.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody>

<tr> 
   <td>Chave LLM <i>(Opcional, avançada)</i></td> 
   <td> <p>Por padrão, esse módulo processa seu prompt usando a IA gerenciada da Adobe e você não precisa selecionar uma chave.</p> <p>Para usar seu próprio provedor de IA, selecione uma chave LLM existente ou crie uma nova clicando em <b>Adicionar</b> e inserindo as seguintes informações:</p>
     <ul>
       <li><b>Nome da chave</b>: insira um nome para a nova chave.</li>
       <li><b>LLM</b>: selecione o modelo de idioma grande ao qual esta chave está associada. Os provedores compatíveis são OpenAI, Anthropic e Amazon Bedrock.</li>
       <li><b>Chave</b>: insira ou mapeie sua chave de API para o provedor selecionado.</li>
       <li><b>Modelo</b>: selecione o modelo LLM que a chave usará.</li>
       <li><b>Outros campos</b>: insira valores para quaisquer outros campos exigidos pelo seu LLM.</li>
      </ul>
    </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-adobe-workfront-mcp-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Workfront MCP ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Ferramentas somente leitura <i>(Opcional)</i></td> 
   <td> <p>Restringir quais ações do Workfront somente leitura a IA pode chamar. Se nenhuma ferramenta for selecionada, todas as ferramentas somente leitura serão permitidas.</p> </td> 
  </tr> 
  <tr> 
   <td>Ferramentas de gravação/exclusão <i>(Opcional)</i></td> 
   <td> <p>Insira as ações de gravação ou exclusão do Workfront que a IA tem permissão para chamar. Se deixar isso vazio, todas as ferramentas de gravação e exclusão serão permitidas.</p> <p>Para garantir que um cenário autônomo nunca execute uma ação destrutiva, recomendamos deixar esse campo definido como uma seleção deliberadamente vazia, em vez de deixá-lo irrestrito.</p> </td> 
  </tr> 
  <tr> 
   <td>Insira seu prompt</td> 
   <td> <p>Insira ou mapeie a instrução, em inglês simples, que você deseja que a IA execute.</p> <p>Exemplo: <i>Localize todos os projetos atribuídos a mim que estão atrasados no cronograma.</i></p> </td> 
  </tr>  </tbody> 
</table>

Para obter uma lista das ferramentas que você pode selecionar para os campos Ferramentas somente leitura e Ferramentas de gravação/exclusão, consulte [Ferramentas do servidor MCP do Adobe Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-tools) na documentação do Workfront.

O módulo retorna as seguintes informações, que você pode mapear nos módulos subsequentes no cenário:

* **Resposta**: a resposta final da IA, como texto.
* **Trilha de Auditoria**: Um registro da sessão, incluindo o prompt original, a hora de início e término e os detalhes de cada chamada de ferramenta feita pela IA, como o nome da ferramenta, os argumentos, se ela teve êxito, a duração e a saída.
* **Resumo**: totais para a sessão, incluindo o número de chamadas de ferramenta tentadas, quantos tiveram êxito ou falharam, tempo total de processamento e status geral.
