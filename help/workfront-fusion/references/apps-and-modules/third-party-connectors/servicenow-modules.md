---
title: Módulos do ServiceNow
description: Em um cenário  [!DNL Adobe Workfront Fusion] , é possível automatizar fluxos de trabalho que usam  [!DNL ServiceNow], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: 7357044d19f93a91d22cede81e7316ff86733fdf
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 0%

---

# [!DNL ServiceNow] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL ServiceNow], bem como conectá-los a vários aplicativos e serviços de terceiros.

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Herdados: Automação e integração do Workfront Fusion for Work </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos [!DNL ServiceNow], você deve ter uma conta [!DNL ServiceNow].

## Informações da API do ServiceNow

O conector ServiceNow usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://{{connection.instance}}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!DNL ServiceNow] a [!DNL Workfront Fusion]

Para criar uma conexão para seus módulos do [!DNL ServiceNow]:

1. Clique em **[!UICONTROL Add]** ao lado da caixa [!UICONTROL Connection] quando você começar a configurar o primeiro módulo [!DNL ServiceNow].
1. Insira o seguinte:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Digite um nome para a nova conexão [!DNL ServiceNow]</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Username]</p> </td> 
      <td>Insira seu nome de usuário do [!DNL ServiceNow].</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Digite sua senha do ServiceNow.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Instance]</p> </td> 
      <td> <p>Digite o endereço da sua conta do [!DNL ServiceNow] sem <code>https://</code> (normalmente <code>&lt;company>.service-now.com</code>).</p> </td> 
     </tr> 
    </tbody> 
   </table>

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow] módulos e seus campos

Ao configurar módulos do [!DNL ServiceNow], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL ServiceNow] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Se um registro personalizado for selecionado em um campo &quot;[!UICONTROL Record type]&quot;, pode levar algum tempo para carregar os campos personalizados.
>
>* Se não houver registros personalizados, a lista suspensa de campos &quot;Tipo de registro&quot; estará vazia.

### Acionadores

#### [!UICONTROL Watch records]

Esse módulo acionador ativa um cenário quando um registro é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecione se a tabela que você deseja observar é uma tabela personalizada ou uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo de registro que deseja assistir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selecione o tipo de valores que deseja exibir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que devem ser gerados pelo módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Selecione se deseja observar novos registros ou registros atualizados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Deactivate a User]](#deactivate-a-user)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)
* [[!UICONTROL Update a record]](#update-a-record)

#### [!UICONTROL Create a record]

Este módulo de ação cria um novo registro [!DNL ServiceNow].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecione se deseja criar um registro em uma tabela personalizada ou em uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro [!DNL ServiceNow] que você deseja que o módulo crie. Em seguida, é possível preencher os campos disponíveis para esse tipo de registro.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL ServiceNow]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL ServiceNow].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> Insira um caminho relativo para <code>https://&ltinstance_url&gt/api/</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Deactivate a User]

Este módulo de ação desativa um usuário no [!DNL ServiceNow] usando a ID do sistema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User System ID]</td> 
   <td> Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do usuário que você deseja que o módulo desative.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a record]

Este módulo de ação exclui um incidente ou um usuário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione se deseja deletar um incidente ou um usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do registro que você deseja que o módulo exclua.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

Este módulo de ação baixa um anexo em um registro [!DNL ServiceNow].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment System ID]</td> 
   <td> Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do anexo que você deseja que o módulo baixe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Este módulo de ação lê um registro [!DNL ServiceNow] usando a ID do sistema.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do registro que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecione se o registro que deseja ler está em uma tabela personalizada ou em uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro [!DNL ServiceNow] que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selecione o tipo de valores que deseja exibir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que devem ser gerados pelo módulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Este módulo de ação cria um novo registro [!DNL ServiceNow].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do registro que você deseja que o módulo atualize.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecione se o registro que deseja atualizar é uma tabela personalizada ou uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro [!DNL ServiceNow] que você deseja que o módulo atualize. Em seguida, é possível preencher os campos disponíveis para esse tipo de registro.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an attachment]

Este módulo de ação carrega um anexo em um registro [!DNL ServiceNow].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table name]</td> 
   <td>Insira ou mapeie o nome da tabela na qual deseja fazer upload do anexo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do item para o qual você deseja carregar o anexo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

#### [!UICONTROL Search for records]

Este módulo procura por registros usando os critérios que você selecionar.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao [!DNL Workfront Fusion], consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecione se a tabela que você deseja pesquisar é uma tabela personalizada ou uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo de registro que deseja pesquisar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Selecione se deseja que o módulo retorne todos os registros que correspondem aos critérios ou apenas o primeiro registro que corresponda a ele. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search type]</td> 
   <td> <p>Selecione o tipo de pesquisa que deseja que o módulo execute</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Advanced query]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Query]</p> <p>Insira a consulta de pesquisa personalizada. Para obter informações sobre [!DNL ServiceNow] consultas de pesquisa personalizadas, consulte a <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">documentação de consulta do ServiceNow</a>.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Criteria]</p> <p>Informe os critérios pelos quais deseja que o módulo pesquise. </li> 
       <li> <p>[!UICONTROL Sort by]</p> <p>Indique por qual campo você deseja que o módulo classifique os resultados e se eles devem ser classificados em ordem crescente ou decrescente.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selecione o tipo de valores que deseja exibir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que devem ser gerados pelo módulo.</td> 
  </tr> 
 </tbody> 
</table>
