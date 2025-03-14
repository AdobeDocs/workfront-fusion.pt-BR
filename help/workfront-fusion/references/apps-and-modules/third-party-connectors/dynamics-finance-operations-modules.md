---
title: Módulos de finanças e operações do Microsoft Dynamics 365
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam Finanças e Operações do Microsoft Dynamics 365, bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 96f8d4f1-f97b-4da8-8d82-83cccb54ec68
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 Finance and Operations modules]

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Microsoft Dynamics 365], bem como conectá-los a vários aplicativos e serviços de terceiros.

>[!NOTE]
>
>O conector [!DNL Microsoft Dynamics 365 Finance and Operations] não dá suporte a [!DNL Dynamics 365].
>
>Para módulos do Microsoft Dynamics 365, consulte [[!DNL Microsoft Dynamics 365 modules]](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).



Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Criar uma conexão

Para criar uma conexão para os módulos de Finanças e Operações do Microsoft Dynamics 365:

1. Em qualquer módulo Finanças e Operações do Microsoft Dynamics 365, clique em **[!UICONTROL Add]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Selecione se você está criando uma conexão padrão do Dynamics Finance e Operations ou uma conexão usando um código de autorização.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Insira um nome para esta conexão.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira suas Finanças e Operações do Dynamics [!UICONTROL Client ID].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira suas Finanças e Operações do Dynamics [!UICONTROL Client Secret]. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tenant ID]</td>
        <td>Insira sua ID de locatário do Dynamics Finance e Operations.</td>
        </tr>
        <tr>
        <td role="rowheader">Recurso</td>
        <td>Insira a URL da sua conta de Finanças e Operações do Dynamics (sem https://)</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continue]** para salvar a conexão e retornar ao módulo.



## Módulos de finanças e operações do Microsoft Dynamics 365 e seus campos

>[!IMPORTANT]
>
>As entidades de dados disponíveis por meio da API de F&amp;O do Dynamics 365 podem variar por instância. Se você não tiver certeza de quais entidades estão disponíveis por meio da API, é útil pesquisar as entidades na sua instância usando o endpoint &quot;dados&quot;. O ponto de extremidade de &quot;dados&quot; no Dynamics 365 Finance and Operations é a URL raiz para acessar serviços OData. Esse endpoint permite interagir com várias entidades de dados expostas pelo sistema usando protocolos OData padrão.
>
>Você pode recuperar essas entidades usando o módulo de chamada de API personalizada.
>
><!--For more information -->



### Criar item de entidade

Este módulo de ação cria um novo item de entidade no Microsoft Dynamics 365 Finance and Operations.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Para obter instruções sobre como conectar o Microsoft Dynamics 365 Finance and Operations ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection" class="MCXref xref">Criar uma conexão</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Insira ou mapeie o tipo de entidade do Dynamics Finance e Operations que deseja criar.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
     <td> <p>Insira ou mapeie um corpo JSON que contenha os dados que você deseja incluir no novo item de entidade.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Excluir item de entidade

Este módulo de ação exclui um item de entidade do Dynamics Finance e de Operações. O item é identificado por seus campos Primary key.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Para obter instruções sobre como conectar o Microsoft Dynamics 365 Finance and Operations ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection" class="MCXref xref">Criar uma conexão</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Insira ou mapeie o tipo de entidade do Dynamics Finance e Operations que deseja excluir.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> Os campos Primary key identificam o item. Para cada campo de chave primária que você deseja fornecer, clique em <b>Adicionar item</b> e insira ou mapeie a chave exclusiva e o valor que identificam esse item. </td> 
  </tr> 
 </tbody> 
</table>

### Fazer uma chamada de API personalizada

Este módulo de ação faz uma chamada personalizada para a API de Finanças e Operações do Dynamics.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>Para obter instruções sobre como conectar o Microsoft Dynamics 365 Finance and Operations ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection" class="MCXref xref">Criar uma conexão</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Insira um caminho relativo ao URL do Dynamics Finance e de Operações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Isso determina o tipo de conteúdo da solicitação.</p> <p>Por exemplo,<code> {"Content-type":"application/json"}</code></p> <p>Observação: se você estiver recebendo erros e for difícil determinar sua origem, considere modificar cabeçalhos com base na documentação [!DNL Workfront]. Se sua Chamada de API personalizada retornar um Erro de solicitação HTTP 422, tente usar um cabeçalho <code>"Content-Type":"text/plain"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query string]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> <p>Dica: recomendamos que você envie informações por meio do corpo JSON, em vez de como parâmetros de consulta.</p> </td> 
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



### Ler item de entidade

Este módulo de ação retorna dados de um item de entidade. O item é identificado por seus campos Primary key.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Para obter instruções sobre como conectar o Microsoft Dynamics 365 Finance and Operations ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection" class="MCXref xref">Criar uma conexão</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Insira ou mapeie o tipo de entidade do Dynamics Finance and Operations que você deseja ler.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> Os campos Primary key identificam o item. Para cada campo de chave primária que você deseja fornecer, clique em <b>Adicionar item</b> e insira ou mapeie a chave exclusiva e o valor que identificam esse item. </td> 
  </tr> 
 </tbody> 
</table>

### Atualizar item de entidade

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Para obter instruções sobre como conectar o Microsoft Dynamics 365 Finance and Operations ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection" class="MCXref xref">Criar uma conexão</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Insira ou mapeie o tipo de entidade do Dynamics Finance and Operations que você deseja atualizar.</td> 
  </tr>  
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> Os campos Primary key identificam o item. Para cada campo de chave primária que você deseja fornecer, clique em <b>Adicionar item</b> e insira ou mapeie a chave exclusiva e o valor que identificam esse item. </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
     <td> <p>Insira ou mapeie um corpo JSON que contenha os dados que você deseja incluir no novo item de entidade.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisar

Este módulo de pesquisa retorna resultados com base nos critérios especificados.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo [!DNL Workfront] ao [!DNL Workfront Fusion], consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Workfront] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Entity]</td> 
   <td>Insira ou mapeie o tipo de entidade do Dynamics Finance and Operations que você deseja pesquisar.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Digite o campo pelo qual deseja pesquisar, o operador que deseja usar na consulta e o valor que está procurando no campo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort by]</td> 
   <td> <p>Insira ou mapeie o campo pelo qual deseja classificar os resultados.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!--

### List All

This module lists all records for a given entity.  The item is identified by its Primary key fields.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
     <td>Choose the Dynamics Finance and Operations entity type that you want the module to list.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
     <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Watch Record

This trigger module starts a scenario when a record of the given type is created or updated.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of [!DNL Workfront] record that you want the module to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to [!DNL Workfront] logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->
