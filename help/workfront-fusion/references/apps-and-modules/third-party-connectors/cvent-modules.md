---
title: Módulos de evento
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam Cvent, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 1%

---

# [!DNL Cvent] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Cvent], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote de Automação e Integração do Adobe Workfront</p><p>Workfront Ultimate</p><p>Workfront Prime e pacotes Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Standard</p><p>Trabalhar ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (herdado): automação e integração do Workfront Fusion for Work </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos [!DNL Cvent], você deve ter uma conta [!DNL Cvent].

## Informações da API de evento

O Conector de evento usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> V200611.ASMX </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.7.14</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL Cvent] ao Adobe Workfront Fusion {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>Os módulos [!DNL Cvent] funcionam por meio de uma API [!UICONTROL SOAP]. Para criar uma conexão com [!DNL Cvent], você deve garantir o seguinte:
>
>* Você tem acesso de [!UICONTROL SOAP] à API [!DNL Cvent].
>* Os endereços IP do Workfront Fusion foram adicionados ao incluo na lista de permissões de sua organização.
>
>  Para obter uma lista de endereços IP do Workfront Fusion, consulte [Configurar Endereços IP para Fusion no incluo na lista de permissões de sua organização](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)


Você pode criar uma conexão com sua conta do [!DNL Cvent] diretamente de dentro de um módulo do [!DNL Cvent].

1. Em qualquer módulo [!DNL Cvent], clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. Selecione a região à qual deseja se conectar.

   * [!UICONTROL América do Norte]
   * [!UICONTROL Europa]
   * [!UICONTROL Sandbox]

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## [!DNL Cvent] módulos e seus campos

Ao configurar módulos do [!DNL Cvent], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Cvent] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ações](#actions)
* [Pesquisas](#searches)

### Ações

* [[!UICONTROL Chamada de API personalizada]](#create-meeting-request)
* [[!UICONTROL Ler um registro]](#read-a-record)
* [[!UICONTROL Registrar Convite]](#register-invitee)
* [[!UICONTROL Adicionar convite]](#add-invitee)
* [[!UICONTROL Excluir Contato]](#delete-contact)
* [[!UICONTROL Atualizar Contato]](#update-contact)
* [[!UICONTROL Criar solicitação de reunião]](#create-meeting-request)

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Cvent]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Cvent].

Ao configurar esse módulo, os campos a seguir são exibidos.

O módulo retorna o código de status a, juntamente com os cabeçalhos e o corpo da chamada de API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Cvent] ao Workfront Fusion, consulte <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Cvent] ao Adobe Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Operação</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo (XML)</td> 
   <td> <p>Insira ou mapeie o corpo da chamada à API. Isso deve incluir somente o XML. O módulo incluirá automaticamente cabeçalhos de autenticação. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler um registro]

Esse módulo de ação lê informações sobre um registro específico.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Cvent] ao Workfront Fusion, consulte <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Cvent] ao Adobe Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo de registro]</p> </td> 
   <td>Selecione o tipo de item do registro que deseja ler.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contato] / [!UICONTROL Evento] / [!UICONTROL ID do Convite]</td> 
   <td> <p>Insira ou mapeie a ID do item que você deseja ler.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td> <p>Selecione os campos que deseja incluir na saída do módulo. Os campos estão disponíveis com base no tipo de item selecionado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Registrar Convite]

Este módulo de ação registra um convidado para um evento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Cvent] ao Workfront Fusion, consulte <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Cvent] ao Adobe Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do convite</p> </td> 
   <td> <p>Insira ou mapeie a ID do convidado que você deseja registrar em um evento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de evento</td> 
   <td> <p>Insira ou mapeie a ID do evento para o qual você deseja registrar o convite.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Adicionar convite]

Este módulo de ação convida um contato para um evento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Cvent] ao Workfront Fusion, consulte <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Cvent] ao Adobe Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Contato]</p> </td> 
   <td> <p>Insira ou mapeie a ID do contato que deseja adicionar a um evento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Evento]</td> 
   <td> <p>Insira ou mapeie a ID do evento ao qual deseja adicionar o contato.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir Contato]

Este módulo de ação exclui um único contato no Evento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Cvent] ao Workfront Fusion, consulte <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Cvent] ao Adobe Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Contato]</td> 
   <td> <p>Insira ou mapeie a ID do contato que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar Contato]

Este módulo de ação atualiza um contato existente usando sua ID.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Cvent] ao Workfront Fusion, consulte <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Cvent] ao Adobe Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Contato]</p> </td> 
   <td> <p>Insira ou mapeie a ID do contato que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos]</td> 
   <td> <p>Selecione os campos para os quais deseja inserir informações e preencha os valores desejados para esses campos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos personalizados]</td> 
   <td> <p>Selecione os campos para os quais deseja inserir informações e preencha os valores desejados para esses campos.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar solicitação de reunião]

Este módulo de ação adiciona uma solicitação de reunião à sua conta.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Cvent] ao Workfront Fusion, consulte <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Cvent] ao Adobe Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Formulário]</p> </td> 
   <td> <p>Insira ou mapeie a ID do Formulário que deseja usar para criar a nova solicitação de reunião.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos de Solicitação de Reunião]</td> 
   <td> <p>Selecione os campos de solicitação de reunião para os quais deseja inserir informações e preencha os valores desejados para esses campos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos de Solicitação de Evento]</td> 
   <td> <p>Selecione os campos de solicitação de evento para os quais você deseja inserir informações e preencha os valores desejados para esses campos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos de Solicitação de RFP]</td> 
   <td> <p>Selecione os campos de solicitação de proposta para os quais deseja inserir informações e preencha os valores desejados para esses campos.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

#### [!UICONTROL Listar registros]

Este módulo de pesquisa recupera informações sobre todos os registros de um tipo específico.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Cvent] ao Workfront Fusion, consulte <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Cvent] ao Adobe Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo de registro]</p> </td> 
   <td> <p>Selecione o tipo de registro que deseja listar.</p> 
    <ul> 
     <li> <p>Todos os eventos da sua conta [!DNL Cvent]</p> </li> 
     <li> <p>Todas as sessões de um evento</p> </li> 
     <li> <p>Todos os convidados para um evento</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Evento]</td> 
   <td> <p>Se você estiver listando convidados ou sessões, informe ou mapeie a ID do evento ao qual esses convidados ou sessões estão associados.</p> </td> 
  </tr> 
 </tbody> 
</table>
