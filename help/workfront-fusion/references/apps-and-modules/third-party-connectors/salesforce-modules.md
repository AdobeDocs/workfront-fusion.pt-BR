---
title: Módulos do Salesforce
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Salesforce, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2984'
ht-degree: 0%

---

# [!DNL Salesforce] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Salesforce], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter uma introdução ao vídeo sobre o conector do Salesforce, consulte:

* [Salesforce](https://video.tv.adobe.com/v/3427027/){target=_blank}

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

>[!NOTE]
>
>* Nem todas as edições de [!DNL Salesforce] têm acesso à API. Para obter detalhes, consulte as informações sobre [!DNL Salesforce] edições com acesso à API no site da Comunidade [!DNL Salesforce].
>* Para obter informações sobre erros específicos retornados da API [!DNL Salesforce], consulte os documentos da API [!DNL Salesforce]. Você também pode verificar o status da API [!DNL Salesforce] em busca de possíveis interrupções de serviço.
>

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

Para usar módulos [!DNL Salesforce], você deve ter uma conta [!DNL Salesforce].

## Informações da API do Salesforce

O conector do Salesforce usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td> {{connection.instanceUrl}}</td>
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v62.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.15.14</td> 
  </tr>
 </tbody> 
 </table>

## Sobre a pesquisa de [!DNL Salesforce] objetos

Ao pesquisar objetos, você pode inserir palavras de pesquisa individuais ou criar uma consulta mais complexa usando curingas e operadores:

* Use o curinga asterisco (\*) como substituto para zero ou mais caracteres. Por exemplo, uma pesquisa por Ca\* encontra itens que começam com Ca
* Usar um curinga de ponto de interrogação (?) como um substituto para um caractere único. Por exemplo, uma pesquisa por João encontra itens com o termo João ou João, mas não João
* Use o operador de aspas (&quot; &quot;) para encontrar uma correspondência exata de frase. Por exemplo: &quot;reunião de segunda-feira&quot;

Para obter mais informações sobre as possibilidades de pesquisa, consulte a documentação do desenvolvedor do [!DNL Salesforce] sobre SOQL e SOSL.

## Criar uma conexão com [!DNL Salesforce]

Para criar uma conexão para seus módulos do [!DNL Salesforce]:

1. Em qualquer módulo [!DNL Salesforce], clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Nome da Conexão]</td>
        <td>
          <p>Insira um nome para a nova conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>
          <p>Selecione se estão se conectando a um ambiente de produção ou não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>
          <p>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID do Cliente]</td>
        <td>Insira a ID do cliente do Salesforce.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira o segredo do cliente do Salesforce. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Sandbox]</td>
        <td>Ative essa opção se esse for um ambiente de sandbox.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Versão da API]</td>
        <td>Insira a versão da API do Salesforce que deseja usar. A versão padrão é 62.0.</td>
      </tr>
    </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.


## [!DNL Salesforce] módulos e seus campos

* [Triggers](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

* [[!UICONTROL Assistir a um campo]](#watch-a-field)
* [[!UICONTROL Observar por Registros]](#watch-for-records)
* [[!UICONTROL Observar Mensagens de Saída]](#watch-outbound-messages)

#### [!UICONTROL Assistir a um campo]

Este módulo de acionador inicia um cenário quando um campo é atualizado em [!DNL Salesforce].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro] </td> 
   <td> <p>Selecione o tipo de registro que contém o campo que o módulo deve observar. Você deve escolher um tipo de registro que tenha o [!UICONTROL Field History] ativado na configuração [!DNL Salesforce]. Para obter mais informações, consulte <a href="https://help.salesforce.com/s/articleView?id=xcloud.tracking_field_history.htm&amp;type=5">Rastreamento do histórico do campo</a> na documentação [!DNL Salesforce]. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campo]</td> 
   <td> <p>Selecione os campos que você deseja que o módulo observe para alterações. Os campos disponíveis dependem do tipo de registro selecionado.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de campos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar por Registros]

Esse módulo de acionamento executa um cenário quando um registro em um objeto é criado ou atualizado. O módulo retorna todos os campos padrão associados ao registro ou aos registros, juntamente com quaisquer campos e valores personalizados que a conexão acesse. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo] </td> 
   <td> <p>Selecione o tipo de registro [!DNL Salesforce] que você deseja que o módulo assista.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campos de Registro]</td> 
   <td>Selecione os campos que você deseja que o módulo assista. Os campos disponíveis dependem do tipo de registro.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Contagem máxima de registros]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Observar]</td> 
   <td> <p>Determine se deseja que o cenário observe somente os novos registros do tipo selecionado ou os novos registros do tipo selecionado e todas as outras alterações nos registros desse tipo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar Mensagens de Saída]

Esse módulo de acionamento executa um cenário quando alguém envia uma mensagem. O módulo retorna todos os campos padrão associados ao registro ou aos registros, juntamente com quaisquer campos e valores personalizados que a conexão acesse. Você pode mapear essas informações em módulos subsequentes no cenário.

Este módulo requer configuração extra. Deve haver um Fluxo configurado para mensagens de saída.

* Para obter instruções sobre Fluxos no Salesforce, consulte [Automatizar Tarefas com Fluxos](https://help.salesforce.com/s/articleView?id=platform.flow.htm) na documentação do Salesforce.
* Para obter informações sobre como configurar uma mensagem de saída no Salesforce, consulte [Enviar uma mensagem de saída do seu fluxo acionado por registro](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_outbound_message.htm), na documentação do Salesforce

<!--

1. Go to the [!DNL Salesforce] setup page.

   To access the setup page, locate and click the button labeled "[!UICONTROL Setup]" in the upper-right hand corner of the [!DNL Salesforce] account. From the [!DNL Salesforce] setup page, locate the "[!UICONTROL Quick Find / Search]" bar on the left hand side. Search for "[!UICONTROL Workflow Rules]." 

1. Click **[!UICONTROL Workflow Rules]**. 
1. On the the [!UICONTROL Workflow Rules] page that appears, click **[!UICONTROL New Rule]** and select the object type the rule will apply to (such as "[!UICONTROL Opportunity]" if you are monitoring updates to Opportunity records).
1. Click **[!UICONTROL Next]**.
1. Set a rule name, evaluation criteria, and rule criteria, then click **[!UICONTROL Save]** and **[!UICONTROL Next]**.

1. Click **[!UICONTROL Done]**.
1. From the newly created Workflow rule, click **[!UICONTROL Edit]**..
1. From the **[!UICONTROL Add Workflow Action]** drop-down list, select **[!UICONTROL New Outbound Message]**.

1. Specify name, description, Endpoint URL, and fields you want to include in the new outbound message, then click **[!UICONTROL Save]**.

   The **[!UICONTROL Endpoint URL]** field contains the URL provided on the [!DNL Salesforce] [!UICONTROL Outbound Message] in Workfront Fusion.

1. Configure a scenario beginning with the [!UICONTROL Outbound Message] event. 

1. Click the **</>** icon in the bottom right and copy the provided URL.
1. Return to the **[!UICONTROL Workflow Rules]** page, locate the newly created rule, then click **[!UICONTROL Activate]**.

-->

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook]</td> 
   <td> <p>Selecione o webhook que deseja usar para assistir mensagens de saída. Para adicionar um webhook, clique em <strong>[!UICONTROL Adicionar]</strong> e insira o nome e a conexão do webhook.</p> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro] </td> 
   <td> <p>Selecione o tipo de registro [!DNL Salesforce] que você deseja que o módulo veja para mensagens de saída.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campos]</td> 
   <td> <p>Selecione os campos que você deseja que o módulo observe para mensagens de saída. Os campos disponíveis dependem do tipo de registro.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Criar um Registro]](#create-a-record)
* [[!UICONTROL Chamada de API personalizada]](#custom-api-call)
* [[!UICONTROL Excluir um Registro]](#delete-a-record)
* [[!UICONTROL Baixar Anexo/Documento]](#download-attachmentdocument)
* [[!UICONTROL Ler um Registro]](#read-a-record)
* [[!UICONTROL Carregar Anexo/Documento]](#upload-attachmentdocument)
* [Carregar arquivo](#upload-file)

#### [!UICONTROL Criar um Registro]

Este módulo de ação cria um novo registro em um objeto.

O módulo permite selecionar quais dos campos do objeto estão disponíveis no módulo. Isso reduz o número de campos que você deve percorrer ao configurar o módulo.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo de Registro] </p> </td> 
   <td> <p>Selecione o tipo de registro [!DNL Salesforce] que você deseja que o módulo crie. Os campos ficam disponíveis com base no tipo de registro selecionado no campo [!UICONTROL Record Type]. Esses campos são baseados na API [!DNL Salesforce].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Selecionar campos a serem mapeados]</td> 
   <td> <p>Selecione os campos que você deseja que o módulo configure ao criar o novo registro. Os campos obrigatórios estão no topo da lista. </p> <p>Os campos selecionados são abertos abaixo deste campo. Agora é possível inserir valores nesses campos.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Salesforce]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Salesforce].

O módulo retorna o seguinte:

* **[!UICONTROL Código de Status]** (número): indica o sucesso ou a falha da sua solicitação HTTP. Esses são códigos padrão que você pode pesquisar na Internet.
* **[!UICONTROL Cabeçalhos]** (objeto): um contexto mais detalhado para o código de resposta/status que não está relacionado ao corpo de saída. Nem todos os cabeçalhos que aparecem em um cabeçalho de resposta são cabeçalhos de resposta, portanto, alguns podem não ser úteis para você.

  Os cabeçalhos de resposta dependem da solicitação HTTP escolhida ao configurar o módulo.

* **[!UICONTROL Corpo]** (objeto): dependendo da solicitação HTTP escolhida ao configurar o módulo, você poderá receber alguns dados de volta. Estes dados, como os dados de uma solicitação [!UICONTROL GET], estão contidos neste objeto.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo a <code> &lt;Instance URL&gt;/services/data/v62.0/</code>.</p> <p>Para obter a lista de pontos de extremidade disponíveis, consulte o <a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm">Guia do Desenvolvedor da API REST do Salesforce</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Método]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Por exemplo, <code>{"Content-type":"application/json"}</code>. O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão. Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Exemplo:** a chamada de API a seguir retorna a lista de todos os usuários da sua conta [!DNL Salesforce]:

* **URL**: `query`

* **Método**: [!UICONTROL GET]

* **Cadeia de Caracteres de Consulta**:

* **Chave**: `q`

* **Valor**: `SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`

Correspondências da pesquisa podem ser encontradas na Saída do módulo em **[!UICONTROL Pacote] > [!UICONTROL Corpo] > [!UICONTROL registros]**.

No nosso exemplo, 6 usuários foram retornados:

![Correspondências para a pesquisa](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)

>[!ENDSHADEBOX]

#### [!UICONTROL Excluir um Registro]

Este módulo de ação exclui um registro existente em um objeto.

Especifique a ID do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro] </td> 
   <td> <p>Selecione o tipo de registro [!DNL Salesforce] que você deseja que o módulo exclua.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Insira ou mapeie a ID [!DNL Salesforce] exclusiva do registro que você deseja que o módulo exclua.</p> <p>Para obter a ID, abra o objeto [!DNL Salesforce] no navegador e copie o texto no final da URL após a última barra (/). Por exemplo: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Baixar Anexo/Documento]

Este módulo de ação baixa um documento ou anexo de um registro.

Especifique a ID do registro e o tipo de download desejado.

O módulo retorna a ID do anexo ou documento e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acesse. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Tipo de Download]</td>
    <td> <p>Especifique o tipo de arquivo que deseja baixar da Salesforce.</p> 
     <ul> 
      <li>[!UICONTROL Anexo]</li> 
      <li>[!UICONTROL Documento]</li> 
      <li>[!UICONTROL ContentDocument] (Este é um documento que foi carregado para uma biblioteca em [!DNL Saleforce CRM Content] ou [!DNL Salesforce Files].)</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[!UICONTROL ID] / </p> <p>[!UICONTROL ID de Anexo] / </p> <p>[!UICONTROL ID do Documento de Conteúdo]</p> </td>
    <td> <p>Insira ou mapeie a ID [!DNL Salesforce] exclusiva do registro que você deseja que o módulo baixe.</p> <p>Para obter a ID, abra o objeto [!DNL Salesforce] no navegador e copie o texto no final da URL após a última barra (/). Por exemplo: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler um Registro]

Este módulo de ação lê dados de um único objeto em [!DNL Salesforce].

Especifique a ID do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Tipo de Registro]</td>
    <td>Selecione o tipo de registro [!DNL Salesforce] que você deseja que o módulo leia.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Campos de Registro]</td>
    <td>Selecione os campos que você deseja que o módulo leia. Você deve selecionar pelo menos um campo. Os campos disponíveis dependem do tipo de registro.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL ID]</td>
    <td> <p>Insira ou mapeie a ID [!DNL Salesforce] exclusiva do registro que você deseja que o módulo leia.</p> <p>Para obter a ID, abra o objeto [!DNL Salesforce] no navegador e copie o texto no final da URL após a última barra (/). Por exemplo: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Atualizar um Registro]

Este módulo de ação edita um registro em um objeto.

O módulo permite selecionar quais dos campos do objeto estão disponíveis no módulo. Isso reduz o número de campos que você deve percorrer ao configurar o módulo.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID do registro que você deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo de Registro] </p> </td> 
   <td> <p>Selecione o tipo de registro [!DNL Salesforce] que você deseja que o módulo atualize. Os campos ficam disponíveis com base no tipo de registro selecionado no campo Tipo de registro. Esses campos são baseados na API [!DNL Salesforce].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Selecionar campos a serem mapeados]</td> 
   <td> <p>Selecione os campos que você deseja que o módulo configure ao criar o novo registro. Os campos obrigatórios estão no topo da lista. </p> <p>Os campos selecionados são abertos abaixo deste campo. Agora é possível inserir valores nesses campos.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Carregar Anexo/Documento]

Esse módulo de ação faz upload de um arquivo e o anexa a um registro especificado por você ou faz upload de um documento.

O módulo retorna a ID do anexo ou documento e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acesse. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Carregamento]</td> 
   <td>Selecione se você deseja que o módulo carregue um anexo ou um documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID do objeto para o qual você deseja fazer upload de um anexo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta]</td> 
   <td>Selecione a pasta na qual deseja fazer upload de um documento. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Arquivo Source]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
 </tbody> 
</table>

#### Carregar arquivo

Esse módulo de ação faz upload de um único arquivo para o Salesforce.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o[!DNL  Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vinculação de documentos]</td> 
   <td>Selecione se deseja aplicar um link de documento de conteúdo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL linkedEntityId]</td> 
   <td>Se estiver usando a vinculação de documentos, insira ou mapeie a ID do objeto vinculado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ShareType]</td> 
   <td>Se estiver usando a vinculação de documentos, selecione permissões para o arquivo.<ul><li><b>Permissão do visualizador</b><p>O usuário pode visualizar o arquivo.</p></li><li><b>Permissão do colaborador</b><p>O usuário pode visualizar e editar o arquivo.</p></li><li><b>Permissões inferidas</b><p>As permissões se baseiam nas permissões do usuário para o registro relacionado, como uma biblioteca.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibilidade]</td> 
   <td>Se estiver usando a vinculação de documentos, insira ou mapeie a visibilidade do documento.<ul><li><b>AllUsers</b><p>Disponível para todos os usuários com permissões</p></li><li><b>UsuáriosInternos</b><p>Disponível para usuários internos com permissões.</p></li><li><b>UsuáriosCompartilhados</b><p>Disponível para usuários que podem ver o feed no qual o arquivo é postado.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [Pesquisar](#search)
* [Pesquisar com consulta](#search-with-query)

#### [!UICONTROL Pesquisa]

Este módulo de ação recupera todos os registros que atendem a um determinado critério.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o[!DNL  Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td> <p>Selecione o tipo de objeto que deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pesquisar critérios]</td> 
   <td>Selecione o campo pelo qual deseja pesquisar, o operador que deseja usar na consulta e o valor que está procurando no campo. Você pode conectar consultas usando AND ou OR.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo. Os campos estão disponíveis com base no tipo de registro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conjunto de resultados]</td> 
   <td>Selecione se você deseja que o módulo retorne Todos os registros correspondentes ou somente o Primeiro registro correspondente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Máximo]</td> 
   <td>Insira ou mapeie o número máximo de registros que você deseja que o módulo recupere durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar com a consulta]

Este módulo de pesquisa procura registros em um objeto em [!DNL Salesforce] que correspondam à consulta de pesquisa especificada. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Salesforce] ao Workfront Fusion, consulte <a href="#create-a-connection-to-salesforce">Criar uma conexão com o Salesforce</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Pesquisa]</td> 
   <td> <p>Selecione o tipo de pesquisa que deseja que o módulo execute:</p> 
    <ul> 
     <li> <p>[!UICONTROL Simples]</p> </li> 
     <li> <p>[!UICONTROL Usando SOSL (Salesforce Object Search Language)]</p> </li> 
     <li> <p>[!UICONTROL Usando SOQL (Salesforce Object Query Language)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo] </p> </td> 
   <td> <p>Se você selecionou o tipo de pesquisa Simples, escolha o tipo de registro [!DNL Salesforce] que deseja que o módulo procure.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Consulta] / [!UICONTROL Consulta SOSL] / [!UICONTROL Consulta SOQL]</td> 
   <td> <p>Informe a consulta pela qual deseja pesquisar.</p> <p>Para obter mais informações sobre SOSL, consulte <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm">Salesforce Object Search Language (SOSL)</a> na documentação de [!DNL Salesforce].</p> <p>Para obter mais informações sobre SOQL, consulte <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm">Salesforce Object Query Language (SOQL)</a> na documentação de [!DNL Salesforce].</p> <p>Observação: observe que o valor do parâmetro <code>RETURNING </code> influencia a saída do módulo. Se você usar <code>LIMIT</code>, [!DNL Fusion] ignorará as configurações no campo [!UICONTROL Contagem máxima de registros]. Se você não definir um limite, o Fusion inserirá o valor [!UICONTROL LIMIT = Contagem máxima de registros].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Contagem máxima de registros]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>
