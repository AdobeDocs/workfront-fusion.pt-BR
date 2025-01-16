---
title: Módulos de eventos do Adobe I/O
description: Com os módulos de Eventos de Adobe I/O, é possível iniciar um cenário do Adobe Workfront Fusion com base em eventos nos aplicativos de Adobe.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 1%

---

# Módulos de eventos do Adobe I/O

Com os módulos Eventos de Adobe I/O, é possível iniciar um cenário do Adobe Workfront Fusion com base em eventos em contas e serviços de Adobe que não têm um conector dedicado do Workfront Fusion.

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">plano do Adobe Workfront*</td> 
   <td> <p>Pro ou superior</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença da Adobe Workfront*</td> 
   <td> <p>Plano, Trabalho</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td> <p>Automação e integração do Workfront Fusion for Work </p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>Sua organização deve comprar o Adobe Workfront Fusion e o Adobe Workfront para usar a funcionalidade descrita neste artigo.</td> 
  </tr> 
 </tbody> 
</table>

&#42;Para saber qual plano, tipo de licença ou acesso você tem, contate o administrador do Workfront.

&#42;&#42;Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Pré-requisitos

Antes de usar o conector de Eventos Adobe I/O, você deve garantir que os seguintes pré-requisitos sejam atendidos:

* Você deve ter uma conta Adobe ativa.

## Informações da API de eventos Adobe I/O

O conector de Eventos Adobe I/O usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://api.adobe.io/events</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.6.7</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com Adobe I/O Events

Para criar uma conexão para os módulos de Eventos Adobe I/O:

1. Clique em Adicionar ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Nome da conexão</td>
        <td>
          <p>Insira um nome para esta conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Tipo</td>
        <td>
          <p>Selecione se deseja se conectar a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Escopos adicionais</td>
        <td>Para adicionar escopos adicionais, clique em <b>Adicionar item</b> e insira o escopo.</td>
      </tr>
      <tr>
        <td role="rowheader">ID do cliente</td>
        <td>Insira a ID do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console</td>
      </tr>
      <tr>
        <td role="rowheader">Segredo do cliente</td>
        <td>Insira o segredo do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console</td>
      </tr>
      </tr>
        <tr>
        <td role="rowheader">ID da organização do consumidor</td>
        <td>Informe a ID da organização do consumidor. Isso pode ser encontrado no URL da credencial do projeto: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">ID da credencial</td>
        <td>Insira sua ID de credencial. Isso pode ser encontrado no URL da credencial do projeto: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">IMS organization ID</td>
        <td>Insira a ID da organização do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console</td>
      </tr>
        <tr>
        <td role="rowheader">ID do Projeto</td>
        <td>Insira a ID do projeto. Isso pode ser encontrado no URL da credencial do projeto: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">WORKSPACE ID</td>
        <td>Para exibir a Workspace ID do seu projeto, baixe os detalhes do projeto na página Visão geral do projeto no Adobe Developer Console. </td>
      </tr>
    </tbody>
    </table>

1. Clique em **Continuar** para salvar a conexão e retornar ao módulo.

## Módulos de eventos Adobe I/O e seus campos

Ao configurar módulos do [!DNL Adobe I/O Events], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe I/O Events] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Triggers

#### Criar um registro de evento

Este módulo de ação usa um webhook para criar uma descrição do evento. Você pode configurar um webhook aqui. Se você estiver usando um webhook existente, os campos neste módulo serão somente leitura.

Para criar um webhook:

1. Clique em **Adicionar** ao lado do campo Webhook.
1. Preencha os seguintes campos:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Webhook name]</td>
        <td>Insira um nome para este webhook.</td>
       </tr>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe I/O Events], consulte <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Criar uma conexão com [!DNL Adobe I/O Events]</a> neste artigo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Webhook description]
         </td>
         <td>
           Insira uma descrição para este webhook.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event provider]
         </td>
         <td>
           Selecione o produto ou a conta da qual deseja criar eventos.
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
           Selecione os eventos que você deseja que o webhook assista. O cenário será acionado quando esses eventos ocorrerem.
         </td>
       </tr>
     </tbody>
   </table>

1. Clique em Salvar para salvar o webhook e retornar ao módulo.

### Ações

#### Obter todos os eventos de um diário

Este módulo de pesquisa recupera todos os eventos de um registro de um journal.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe I/O Events], consulte <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Criar uma conexão com [!DNL Adobe I/O Events]</a> neste artigo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Registration ID]
         </td>
         <td>
           Selecione o registro para o qual deseja recuperar eventos.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Maximum number of returned records]
         </td>
         <td>
              Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário. 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Return events that occur after]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Latest]
         </td>
         <td>
         Habilite esta opção para retornar o evento mais recente.
         </td>
       </tr>
     </tbody>
   </table>

#### Fazer uma chamada de API personalizada

Este módulo de ação faz uma chamada de API personalizada para a API [!DNL Adobe I/O Events]

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe I/O Events], consulte <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Criar uma conexão com [!DNL Adobe I/O Events]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Insira um caminho relativo a <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
  <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP em [!DNL Adobe Workfront Fusion]</a>.</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização e cabeçalhos x-api-key automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
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

### Pesquisas

#### Obter provedor e IDs de evento

Esse módulo de pesquisa obtém as IDs de eventos de Adobe I/O para o provedor e os eventos especificados.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe I/O Events], consulte <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Criar uma conexão com [!DNL Adobe I/O Events]</a> neste artigo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event provider]
         </td>
         <td>
           Selecione o provedor para o qual deseja recuperar a ID.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
              Selecione os eventos para os quais você deseja fornecer IDs. Eventos estão disponíveis com base no provedor de eventos. 
         </td>
       </tr>
     </tbody>
   </table>

<!--

Watch Events

This trigger module starts a scenario when an event occurs in the chosen Adobe product or service.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>Select the webhook that you want to use for this trigger, or add a new webhook. </p><p>To add a new webhook, <ol><li>Click <b>Add</b> next to the webhook field.</li><li>Enter the following: <ul><li>A name for the webhook</li><li>The connection that you want to use for this webhook</li><li>The source of the events you want to watch</li></ul></li><li>Click <b>Save</b> to save the webhook and return to the module. </td> 
   </tr> 
   </tbody> 
</table>

-->
