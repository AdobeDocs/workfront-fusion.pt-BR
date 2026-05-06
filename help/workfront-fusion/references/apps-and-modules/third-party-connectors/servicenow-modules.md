---
title: Módulos do ServiceNow
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam  [!DNL ServiceNow], bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: 3e39d284014c76a1cc300a075e61c25964c49995
workflow-type: tm+mt
source-wordcount: '1643'
ht-degree: 43%

---

# Módulos do [!DNL ServiceNow]

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam [!DNL ServiceNow], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos [!DNL ServiceNow], você deve ter uma conta do [!DNL ServiceNow].

## Informações da API do ServiceNow

O conector ServiceNow usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td><pre><code>https://&#123;&#123;connection.instance&#125;&#125;/api</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL ServiceNow] ao Workfront Fusion

Para criar uma conexão para os módulos do [!DNL ServiceNow]:

1. Clique em **[!UICONTROL Adicionar]** ao lado da caixa [!UICONTROL Conexão] ao começar a configurar o primeiro módulo [!DNL ServiceNow].
1. Insira o seguinte:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Insira um nome para a nova conexão [!DNL ServiceNow].</td> 
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
      <td role="rowheader"> <p>[!UICONTROL Nome de Usuário]</p> </td> 
      <td>Insira seu nome de usuário do [!DNL ServiceNow].</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Digite sua senha do ServiceNow.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Instância]</p> </td> 
      <td> <p>Digite o endereço da sua conta do [!DNL ServiceNow] sem <code>https://</code> (normalmente <code>&lt;company>.service-now.com</code>).</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **Continuar** para salvar a conexão e retornar ao módulo.

   <!--Markdown placeholder-->

## Módulos [!UICONTROL ServiceNow] e seus campos

Ao configurar módulos do [!DNL ServiceNow], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos do [!DNL ServiceNow] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Se um registro personalizado for selecionado em um campo &quot;[!UICONTROL Tipo de registro]&quot;, pode levar algum tempo para carregar os campos personalizados.
>
>* Se não houver registros personalizados, a lista suspensa de campos &quot;Tipo de registro&quot; estará vazia.

### Acionadores

#### [!UICONTROL Monitorar registros]

Esse módulo acionador ativa um cenário quando um registro é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de tabela]</td> 
   <td>Selecione se a tabela que você deseja observar é uma tabela personalizada ou uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo de registro que deseja assistir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Exibir]</td> 
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

* [[!UICONTROL Criar um registro]](#create-a-record)
* [[!UICONTROL Chamada de API personalizada]](#custom-api-call)
* [[!UICONTROL Desativar um usuário]](#deactivate-a-user)
* [[!UICONTROL Excluir um registro]](#delete-a-record)
* [[!UICONTROL Baixar um anexo]](#download-an-attachment)
* [[!UICONTROL Ler um registro]](#read-a-record)
* [[!UICONTROL Carregar um anexo]](#upload-an-attachment)
* [[!UICONTROL Atualizar um registro]](#update-a-record)

#### [!UICONTROL Criar um registro]

Este módulo de ação cria um novo registro [!DNL ServiceNow].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de tabela]</td> 
   <td>Selecione se deseja criar um registro em uma tabela personalizada ou em uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro [!DNL ServiceNow] que você deseja que o módulo crie. Em seguida, é possível preencher os campos disponíveis para esse tipo de registro.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API do [!DNL ServiceNow]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL ServiceNow].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL relativa]</td> 
   <td> Insira um caminho relativo a <code>https://&ltinstance_url&gt/api/</code>. </td> 
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
   <td> <p>Adicione a consulta para a chamada de API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Desativar um usuário]

Este módulo de ação desativa um usuário no [!DNL ServiceNow] usando a ID do sistema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Sistema do Usuário]</td> 
   <td> Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do usuário que você deseja que o módulo desative.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um registro]

Este módulo de ação exclui um incidente ou um usuário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione se deseja deletar um incidente ou um usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Sistema]</td> 
   <td>Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do registro que você deseja que o módulo exclua.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Baixar um anexo]

Este módulo de ação baixa um anexo em um registro [!DNL ServiceNow].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Sistema de Anexo]</td> 
   <td> Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do anexo que você deseja que o módulo baixe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler um registro]

Este módulo de ação lê um registro [!DNL ServiceNow] usando a ID do sistema.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Sistema de Registros]</td> 
   <td>Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do registro que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de tabela]</td> 
   <td>Selecione se o registro que deseja ler está em uma tabela personalizada ou em uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro [!DNL ServiceNow] que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Exibir]</td> 
   <td>Selecione o tipo de valores que deseja exibir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que devem ser gerados pelo módulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um registro]

Este módulo de ação cria um novo registro [!DNL ServiceNow].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Sistema de Registros]</td> 
   <td>Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do registro que você deseja que o módulo atualize.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de tabela]</td> 
   <td>Selecione se o registro que deseja atualizar é uma tabela personalizada ou uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro [!DNL ServiceNow] que você deseja que o módulo atualize. Em seguida, é possível preencher os campos disponíveis para esse tipo de registro.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um anexo]

Este módulo de ação carrega um anexo em um registro [!DNL ServiceNow].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome da tabela]</td> 
   <td>Insira ou mapeie o nome da tabela na qual deseja fazer upload do anexo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Sistema]</td> 
   <td>Insira ou mapeie a ID [!DNL ServiceNow] exclusiva do item para o qual você deseja carregar o anexo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

#### [!UICONTROL Pesquisar registros]

Este módulo procura por registros usando os critérios que você selecionar.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do ServiceNow ao Workfront Fusion, consulte <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Conectar [!DNL ServiceNow] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de tabela]</td> 
   <td>Selecione se a tabela que você deseja pesquisar é uma tabela personalizada ou uma tabela padrão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo de registro que deseja pesquisar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conjunto de resultados]</td> 
   <td>Selecione se deseja que o módulo retorne todos os registros que correspondem aos critérios ou apenas o primeiro registro que corresponda a ele. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contagem máxima de registros]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de pesquisa]</td> 
   <td> <p>Selecione o tipo de pesquisa que deseja que o módulo execute</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Consulta avançada]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Pesquisar Consulta]</p> <p>Insira a consulta de pesquisa personalizada. Para obter informações sobre [!DNL ServiceNow] consultas de pesquisa personalizadas, consulte a <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">documentação de consulta do ServiceNow</a>.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simples]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Critérios de Pesquisa]</p> <p>Informe os critérios pelos quais deseja que o módulo pesquise. </li> 
       <li> <p>[!UICONTROL Classificar por]</p> <p>Indique por qual campo você deseja que o módulo classifique os resultados e se eles devem ser classificados em ordem crescente ou decrescente.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Exibir]</td> 
   <td>Selecione o tipo de valores que deseja exibir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que devem ser gerados pelo módulo.</td> 
  </tr> 
 </tbody> 
</table>
