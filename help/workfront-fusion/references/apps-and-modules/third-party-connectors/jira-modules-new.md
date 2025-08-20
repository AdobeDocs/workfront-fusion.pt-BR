---
title: Módulos do Jira
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Software Jira, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
source-git-commit: d16c1d9f257d44b72cfb93caa2a814fd62b0b733
workflow-type: tm+mt
source-wordcount: '1564'
ht-degree: 5%

---

# Módulos do Jira

>[!NOTE]
>
>Essas instruções se aplicam à nova versão do conector Jira, que é simplesmente rotulada como Jira. Para obter instruções sobre os conectores herdados do Jira Cloud e do Jira Server, consulte [Módulos de software do Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Jira, bem como conectá-lo a vários aplicativos e serviços de terceiros.

O conector Jira pode ser usado para o Jira Cloud e o Jira Data Server.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença do Adobe Workfront</td> 
   <td> <p>Novo: Padrão</p><p>Ou</p><p>Atual: trabalho ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Atual: nenhum requisito de licença do Workfront Fusion</p>
   <p>Ou</p>
   <p>Herdados: Automação e integração do Workfront Fusion for Work </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo menu:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos Jira, você deve ter uma conta Jira.

## Conectar o Jira ao Workfront Fusion

Você pode criar uma conexão com sua conta Jira diretamente de dentro de um módulo Jira.

>[!IMPORTANT]
>
>* Para criar uma conexão básica com o data center Jira, você precisará de um token de acesso pessoal Jira.
>* Para criar uma conexão básica com a Jira Cloud, você precisará de um token de API Jira
>* Para criar uma conexão OAuth 2 com o Data Center do Jira Cloud ou Jira, você precisará de uma ID de cliente Jira e um Segredo do cliente.
>
>Para obter instruções sobre como criar qualquer um desses, consulte a documentação do Jira.

1. Em qualquer módulo Jira, clique em **Adicionar** ao lado do campo Conexão.
1. Configure os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Tipo de conexão</p> </td> 
      <td> <p>Selecione se você está criando uma conexão básica ou uma conexão OAuth 2.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Nome da conexão</p> </td> 
      <td> <p>Insira um nome para a nova conexão.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">URL do serviço</td>
      <td>Insira o URL da instância do Jira. Este é o endereço que você usa para acessar o Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Tipo de conta Jira</td>
       <td>Selecione se você está se conectando ao Jira Cloud ou ao Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">ID do cliente</td> 
      <td> <p>Se você estiver criando uma conexão OAuth 2, insira sua ID de cliente Jira</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Segredo do cliente</td> 
      <td> <p>Se você estiver criando uma conexão OAuth 2, digite o segredo do cliente Jira</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Email</td> 
      <td>Se estiver criando uma conexão básica com o Jira Cloud, insira seu endereço de email.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token de API</td> 
      <td>Se estiver criando uma conexão básica com o Jira Cloud, insira o token da API.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token de acesso pessoal</td> 
      <td>Se estiver criando uma conexão básica com o data center Jira, insira o token de acesso pessoal.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Versão da API</td> 
      <td>Selecione a versão da API Jira à qual você deseja que essa conexão se conecte.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.


## Módulos Jira e seus campos

Ao configurar módulos Jira, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Jira podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

#### Observar registros

Este módulo de acionamento inicia um cenário quando um registro é adicionado, atualizado ou excluído.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Webhook</td> 
   <td> <p>Selecione o webhook que deseja usar para assistir por registros ou crie um novo webhook. </p> <p>Para criar um novo webhook:</p> 
    <ol> 
     <li>Clique em <strong>Adicionar</strong></li> 
     <li>Insira um nome para o webhook.</li> 
     <li> Selecione a conexão que deseja usar com seu webhook. <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </li> 
     <li> <p>Selecione o tipo de registro que você deseja que o software assista:</p> 
      <ul> 
       <li>Problema</li> 
       <li>Comentário </li> 
       <li>Log de trabalho </li> 
       <li>Projeto </li> 
       <li>Sprint</li> 
       <li>Anexo </li> 
      </ul> </li> 
     <li>Selecione um ou mais tipos de evento que acionarão esse cenário.</li> 
     <li>Insira um filtro de Linguagem de consulta Jira para este módulo.<p>Para obter mais informações sobre JQL, consulte <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> no site de ajuda da Atlassian. </p></li>
     <li>Clique em <b>Salvar</b> para salvar o webhook. 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [Adicionar problema ao sprint](#add-issue-to-sprint)
* [Criar um registro](#create-a-record)
* [Chamada de API personalizada](#custom-api-call)
* [Excluir um registro](#delete-a-record)
* [Baixar um anexo](#download-an-attachment)
* [Ler um registro](#read-a-record)
* [Atualizar um registro](#update-a-record)

#### Adicionar problema ao sprint

Este módulo de ação adiciona um ou mais problemas a um sprint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do Sprint</td> 
   <td>Insira ou mapeie a ID de velocidade da velocidade à qual você deseja adicionar um problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID ou chaves do problema</td> 
   <td>Para cada problema ou chave que você deseja adicionar ao sprint, clique em <b>Adicionar item</b> e insira a ID ou chave do problema. Você pode inserir até 50 em um módulo.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar um registro

Este módulo de ação cria um novo registro no Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo crie.</p> 
    <ul> 
     <li>Anexo</li> 
     <li>Comentário</li> 
     <li>Problema</li> 
     <li>Projeto</li> 
     <li>Sprint </li> 
     <li>Log de trabalho</li> 
     <li>Usuário</li> 
     <li>Quadro</li> 
     <li>Categoria</li> 
     <li>Filtro</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Outros campos</td> 
   <td> Preencha os outros campos. Os campos estão disponíveis dependendo do tipo de registro selecionado. </td> 
  </tr> 
 </tbody> 
</table>

#### Chamada de API personalizada

Esse módulo de ação permite fazer uma chamada autenticada personalizada para a API Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Insira um caminho relativo a<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Método</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cabeçalhos</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p> O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sequência de consulta</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um registro

Este módulo de ação exclui o registro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo exclua. </p> 
    <ul> 
     <li>Comentário</li> 
     <li>Problema</li> 
     <li>Projeto</li> 
     <li>Sprint </li> 
     <li>Log de trabalho</li> 
     <li>Anexo</li> 
     <li>Quadro</li> 
     <li>Categoria</li> 
     <li>Filtro</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Tipo de registro)ID</td> 
   <td>Insira ou mapeie a ID ou a chave do registro que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Baixar um anexo

Este módulo de ação baixa o anexo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td>Insira ou mapeie a ID do anexo que deseja baixar.</td> 
  </tr> 
 </tbody> 
</table>

#### Ler um registro

Este módulo de ação lê os dados do registro especificado no Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione o tipo de registro Jira que deseja que o módulo leia.</p> 
    <ul> 
     <li>Anexo</li> 
     <li>Comentário</li> 
     <li>Problema</li> 
     <li>Projeto</li> 
     <li>Sprint </li> 
     <li>Log de trabalho</li> 
     <li>Usuário</li> 
     <li>Quadro</li> 
     <li>Categoria</li> 
     <li>Filtro</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Saídas</td> 
   <td>Selecione as saídas que deseja receber. As opções de saída estão disponíveis com base no tipo de registro selecionado no campo "Tipo de registro".</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID (Tipo de registro)</td> 
   <td> <p>Insira ou mapeie a Jira ID exclusiva do registro que você deseja que o módulo leia.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um registro

Este módulo de ação atualiza um registro existente, como um problema ou projeto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo atualize. Quando você seleciona um tipo de registro, outros campos específicos desse tipo de registro aparecem no módulo.</p> 
    <ul> 
     <li>Comentário</li> 
     <li>Problema</li> 
     <li>Projeto</li> 
     <li>Sprint </li> 
     <li>Problema de transição</li> 
     <li>Categoria </li> 
     <li>Filtro </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID ou chave</td> 
   <td>Insira ou mapeie a ID ou a chave do registro que deseja atualizar.</td> 
  <tr> 
   <td role="rowheader">Outros campos</td> 
   <td> Preencha os outros campos. Os campos estão disponíveis dependendo do tipo de registro selecionado. </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

#### Pesquisar registros

Este módulo de pesquisa procura registros em um objeto no Jira que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta Jira ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar Jira ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo procure. Quando você seleciona um tipo de registro, outros campos específicos desse tipo de registro aparecem no módulo.</p> 
    <ul> 
     <li>Problema</li> 
     <li>Projeto</li> 
     <li>Usuário</li> 
     <li>Sprint</li> 
     <li>Quadro</li> 
     <li>Log de trabalho</li> 
     <li>Comentário</li> 
     <li>Problema de transição</li> 
     <li>Categoria</li> 
    </ul> </td> 
  <tr> 
   <td role="rowheader"> <p>Máximo de Resultados</p> </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que você deseja que o módulo recupere durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Deslocamento</td> 
    <td> Insira ou mapeie a ID do primeiro item para o qual deseja recuperar detalhes. Essa é uma maneira de paginar os registros. Se você inserir o 5000º item como deslocamento, o módulo retornará os itens 5000-9999.</td> 
   </tr>
  <tr> 
   <td role="rowheader">Outros campos</td> 
   <td> Preencha os outros campos. Os campos estão disponíveis dependendo do tipo de registro selecionado. </td> 
  </tr> 
 </tbody> 
</table>
