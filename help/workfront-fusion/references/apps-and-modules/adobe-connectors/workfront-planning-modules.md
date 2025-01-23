---
title: Módulos do Adobe Workfront Planning
description: Com os  [!DNL Adobe Workfront Planning] módulos, você pode iniciar um [!DNL Adobe Workfront Fusion] cenário com base nos eventos da sua [!DNL Adobe] conta do Workfront Planning, criar, ler ou atualizar contratos e outros registros, pesquisar registros usando critérios definidos por você e carregar documentos.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 0%

---

# [!DNL Adobe Workfront Planning] módulos

Com os módulos [!DNL Adobe Workfront Planning], é possível acionar um cenário quando os eventos ocorrem no Workfront Planning. Você também pode criar, ler, atualizar e excluir registros ou executar uma chamada de API personalizada para sua conta do [!DNL Adobe Workfront Planning].

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho] </p>
   </td>  
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano [!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Adobe Workfront], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Informações da API do Adobe Workfront Planning

O conector do Adobe Workfront Planning usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://{{connection.host}}/maestro/api/{{common.maestroApiVersion}}/</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com [!DNL Adobe Workfront Planning] {#create-a-connection-to-adobe-workfront-planning}

Você pode criar uma conexão com sua conta do [!DNL Workfront Planning] diretamente de dentro de um módulo do [!DNL Workfront Fusion].

1. Em qualquer módulo [!DNL Adobe Workfront Planning], clique em **[!UICONTROL Add]** ao lado da caixa Conexão.

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
            <p>Insira um nome para esta conexão.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Environment]</td>
          <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Type]</td>
          <td>Selecione se você deseja se conectar a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(Opcional)</p></td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Client ID]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] de [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Opcional)</p></td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Client Secret]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] de [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(Opcional)</p></td>
          <td>Insira o URL que sua instância do Workfront usará para autenticar essa conexão. <p>O valor padrão é <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>Insira seu prefixo de host.<p>O valor padrão é <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>
1. Clique em **[!UICONTROL Continue]** para salvar a conexão e retornar ao módulo.

## [!DNL Adobe Workfront Planning] módulos e seus campos

### Acionadores

#### Assistir a eventos

Este módulo de acionamento inicia um cenário quando um registro, tipo de registro ou espaço de trabalho é criado, atualizado ou excluído no Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Selecione o webhook que deseja usar ou clique em Adicionar para criar um novo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>Selecione se deseja observar registros, tipos de registro ou espaços de trabalho.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Selecione se deseja observar o estado antigo ou o novo estado.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Acione um cenário quando o registro alterar <b>para</b> um determinado valor.</p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Acione um cenário quando o registro alterar <b>de</b> um determinado valor.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Se estiver observando registros, selecione o Workspace que deseja observar para os registros.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Se estiver observando registros, selecione o tipo de registro que deseja observar.</td>
    </tr>
    </tr>
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>É possível definir filtros para observar apenas os registros que atendem aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que deseja que o filtro avalie, o operador e o valor que deseja que o filtro permita. Você pode usar mais de um filtro adicionando regras AND.</p> <p>Observação: não é possível editar filtros em webhooks [!DNL Workfront] existentes. Para configurar filtros diferentes para assinaturas de evento [!DNL Workfront], remova o webhook atual e crie um novo.</p> <p>Para obter mais informações sobre filtros de evento, consulte <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtros de assinatura de evento no [!DNL Workfront] &gt; [!UICONTROL Watch Events] módulos</a> no artigo sobre módulos do Workfront.</p> </td> 
     </tr> 
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>Selecione se você deseja observar novos. registros atualizados, novos e atualizados ou excluídos.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Exclude updates made by this connection]</p>
      </td>
      <td>Habilite esta opção para impedir que o cenário seja acionado quando uma alteração for feita pela conexão usada por este módulo. Isso impede que outra instância do cenário seja acionada se esse cenário executar uma ação de acionamento.</td> 
      </tr>
  </tbody>
</table>

### Ações

* [Excluir um tipo de registro](#delete-a-record-type)
* [Fazer uma chamada de IA personalizada](#make-a-custom-api-call)

#### Excluir um tipo de registro

Este módulo de ação exclui um único tipo de registro no Workfront Planning por sua ID.

>[!WARNING]
>
>A exclusão de um tipo de registro no Workfront Planning também exclui todos os registros na tabela de tipo de registro.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Insira ou mapeie a ID do campo que deseja excluir.</td> 
      </tr>
  </tbody>
</table>

#### Fazer uma chamada de API personalizada

Este módulo faz uma chamada de API personalizada para a API [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Insira um caminho relativo a <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Para cada par de chave/valor que você deseja adicionar à sequência de consulta, clique em <b>Adicionar item</b> e insira a chave e o valor.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

<!--
### Searches

#### Search records

This action module retrieves a list of records based on criteria you specify.

-->

### Sem categoria


#### Criar um registro

Essa ação cria um único registro no Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Insira ou mapeie o tipo de registro que deseja criar. Os tipos de registro disponíveis baseiam-se na sua conta do Workfront Planning.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Outros campos</p>
      </td>
      <td>Esses campos se baseiam no tipo de registro selecionado.</td> 
      </tr>
     <tr>
  </tbody>
</table>

### Excluir um registro

Este módulo de ação exclui o registro especificado no Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Informe ou mapeie a ID do registro que deseja deletar.</td> 
      </tr>
  </tbody>
</table>

<!--

### Get all records

This action module retrieves all records from an [!DNL Adobe Workfront Planning] account.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

-->

### Obter um registro

Este módulo de ação recupera um único registro de [!DNL Adobe Workfront Planning], especificado por sua ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record ID]</td>
      <td>Insira ou mapeie a ID do registro que deseja recuperar.</td>
    </tr>
  </tbody>
</table>

### Obter registros por tipo de registro

Este módulo de ação recupera todos os registros do tipo especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Selecione ou mapeie o espaço de trabalho que contém os registros que deseja recuperar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Selecione o tipo de registro que deseja recuperar.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tbody>
</table>

### Obter tipos de registro

Este módulo de ação recupera uma lista de tipos de registros em uma conta [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
  </tbody>
</table>

### Atualizar registro

Essa ação atualiza um único registro no Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Insira ou mapeie o tipo de registro que deseja atualizar. Os tipos de registro disponíveis baseiam-se na sua conta do Workfront Planning.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Outros campos</p>
      </td>
      <td>Esses campos se baseiam no tipo de registro selecionado.</td> 
      </tr>
     <tr>
  </tbody>
</table>
