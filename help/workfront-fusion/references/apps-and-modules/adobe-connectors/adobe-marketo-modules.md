---
title: Módulos do Marketo
description: Em um cenário  [!DNL Adobe Workfront Fusion] , é possível automatizar fluxos de trabalho que usam  [!DNL Marketo], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1814'
ht-degree: 0%

---

# [!DNL Marketo] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Marketo], bem como conectá-los a vários aplicativos e serviços de terceiros.

Para obter uma introdução ao vídeo sobre o conector do Marketo, consulte:

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

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

Para usar módulos [!DNL Marketo], você deve ter uma conta [!DNL Marketo].

## Informações da API do Marketo

O conector do Marketo usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL Marketo] ao Workfront Fusion {#connect-marketo-to-workfront-fusion}

Você pode criar uma conexão com sua conta [!DNL Marketo] diretamente de dentro de qualquer módulo [!DNL Marketo].

1. Em qualquer módulo do Marketo, clique em **Adicionar** ao lado do campo Conexão.
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
          <p>Insira um nome para a nova conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Selecione se estão se conectando a um ambiente de produção ou não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Account / Munchkin ID]</td>
        <td>
          <p>Insira sua conta do [!DNL Marketo] ou a ID do [!DNL Marketo] [!UICONTROL Munchkin]. Esta é a parte exclusiva da URL Base ou do Ponto de Extremidade atribuída à sua conta, que você usa para acessar [!DNL Marketo] por meio da API [!UICONTROL REST]. Para obter instruções sobre como localizar, consulte [URL Base](https://developers.marketo.com/rest-api/base-url/) na documentação do [!DNL Marketo].</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira a ID do cliente do Marketo. Para obter instruções sobre como localizar, consulte [Authentication](https://developers.marketo.com/rest-api/authentication/) na documentação do [!DNL Marketo].</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Digite o segredo do cliente do Marketo. Para obter instruções sobre como localizar esses itens, consulte [Authentication](https://developers.marketo.com/rest-api/authentication/) na documentação do [!DNL Marketo].</td>
      </tr>
     </tbody>
    </table>
1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

## [!DNL Marketo] Módulos e seus campos

Ao configurar módulos do [!DNL Marketo], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Marketo] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

* [[!UICONTROL Watch events (Instant)]](#watch-events-instant)
* [[!UICONTROL Watch records]](#watch-records)

#### [!UICONTROL Watch events (Instant)]

Este módulo de acionamento inicia um cenário quando um registro é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Insira o webhook que você deseja que o módulo use.</p> <p>Para obter mais informações sobre webhooks, consulte <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch records]

Este módulo de acionamento inicia um cenário quando um registro é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Activity]</strong> </p> <p>Selecione o tipo de atividade que deseja observar. </p> <p>O módulo observa somente novas atividades.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>No campo <b>Tipo de Evento</b>, selecione se deseja procurar novos registros, registros atualizados, registros novos e atualizados ou atualizações de campo específicas. Se você optar por assistir a atualizações de campo específicas, selecione o campo que deseja que o módulo assista.</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p>No campo <b>Tipo de Evento</b>, selecione se deseja procurar novos registros, registros atualizados ou registros novos e atualizados.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecione os campos que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Add Leads to a List]](#add-leads-to-a-list)
* [[!UICONTROL Clone a Program]](#clone-a-program)
* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Custom API call]](#custom-api-call)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Remove Leads from a List]](#remove-leads-from-a-list)
* [[!UICONTROL Schedule a Campaign]](#schedule-a-campaign)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a File]](#upload-a-file)

#### [!UICONTROL Add Leads to a List]

Este módulo de ação adiciona um ou mais leads a uma lista usando a ID de lead. Você pode adicionar até 300 leads de cada vez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Insira ou mapeie a ID da lista onde deseja adicionar clientes potenciais.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Para cada cliente potencial que deseja adicionar à lista, clique em <b>[!UICONTROL Add]</b> e, em seguida, insira ou mapeie a ID do cliente potencial que deseja adicionar. Você pode adicionar até 300 clientes em potencial para o módulo adicionar à lista.</p> <p>Clique no botão de alternância do mapa para mapear uma coleção existente de clientes potenciais que deseja adicionar à lista.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clone a Program]

Este módulo de ação faz uma cópia de um programa usando a ID do programa existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Existing Program ID]</td> 
   <td>Insira ou mapeie a ID do programa que você deseja copiar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Program Name]</p> </td> 
   <td> <p>Insira ou mapeie um nome para o novo programa</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Insira ou mapeie a ID da pasta em que deseja que o novo programa esteja localizado.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a record]

Este módulo de ação cria um novo registro em [!DNL Marketo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Folder]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Se você estiver criando uma Empresa ou um Cliente Potencial, selecione os campos para os quais deseja definir valores quando o novo registro for criado e, em seguida, insira valores para esses campos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Type]</td> 
   <td>Se você estiver criando um programa, selecione o tipo de programa que deseja criar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Channel] </td> 
   <td>Se estiver criando um programa, selecione o canal do programa no qual deseja criar o programa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Program Name]</td> 
   <td>Se você estiver criando uma Pasta ou um Programa, insira ou mapeie um nome para o novo registro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Se você estiver criando uma Pasta ou um Programa, insira ou mapeie uma descrição para o novo registro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID]</td> 
   <td>Se você estiver criando uma Pasta ou um Programa, informe ou mapeie a ID da pasta pai na qual deseja criar o novo registro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Se você estiver criando um Programa, adicione os custos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Se estiver criando um programa, adicione tags</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API call]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Marketo]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://{your-base-url}.mktorest.com/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] O adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Para cada campo que você deseja adicionar à chamada de API, clique em <b>Adicionar item</b> e insira a chave e o valor do campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Este módulo de ação baixa um arquivo usando a ID do arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Insira ou mapeie a ID do arquivo que deseja baixar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Este módulo de ação lê as informações sobre um registro usando sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaign]</p> </li> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL List]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione as informações que deseja incluir no pacote de saída deste módulo. Os campos estão disponíveis com base na [!UICONTROL Record Type] selecionada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL <Object> ID]</td> 
   <td>Insira ou mapeie a ID do objeto sobre o qual deseja recuperar informações.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Leads from a List]

Este módulo de ação remove um ou mais leads de uma lista usando a ID de lead. Você pode remover até 300 clientes em potencial por vez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Insira ou mapeie a ID da lista onde deseja remover clientes potenciais.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Para cada cliente potencial que deseja remover da lista, clique em <b>[!UICONTROL Add item]</b> e, em seguida, insira ou mapeie a ID do cliente potencial que deseja remover. Você pode adicionar até 300 clientes em potencial para o módulo remover da lista. </p> <p>Clique no botão de alternância do mapa para mapear uma coleção existente de clientes potenciais que você deseja remover da lista.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Schedule a Campaign]

Esse módulo de ação agenda uma campanha existente para uma determinada data.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Insira ou mapeie a ID da campanha que você deseja agendar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Schedule for Date]</p> </td> 
   <td>Selecione a data em que deseja que a campanha seja executada. Se esse campo ficar em branco, a campanha será executada cinco minutos após o início do cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Esse módulo de ação atualiza um registro existente usando sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Company] / [!UICONTROL Lead] / [!UICONTROL Program ID]</td> 
   <td>Insira ou mapeie a ID do registro que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Se você estiver atualizando uma Empresa ou um Cliente Potencial, selecione os campos para os quais deseja atualizar valores e informe valores para esses campos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Name]</td> 
   <td>Se você estiver atualizando um programa, digite ou mapeie um novo nome para o programa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Se você estiver atualizando um programa, insira ou mapeie uma nova descrição para o programa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Se você estiver atualizando um programa, insira ou mapeie uma nova data de início para o programa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Se você estiver atualizando um programa, insira ou mapeie uma nova data de término para o programa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Se você estiver atualizando um programa, adicione os custos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Se você estiver atualizando um programa, adicione tags</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

Este módulo de ação carrega um novo arquivo em [!UICONTROL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Insira ou mapeie a ID da pasta em que deseja que o novo arquivo esteja localizado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Insira uma descrição para o arquivo carregado.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search Records]](#update-a-record)

#### [!UICONTROL List records]

Este módulo de ação recupera todos os registros de um tipo específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja listar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Read all campaigns]</p> </li> 
     <li> <p>[!UICONTROL Read all programs]</p> </li> 
     <li> <p>[!UICONTROL Read all leads] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field]</td> 
   <td>Se você selecionou recuperar clientes em potencial, selecione se deseja recuperar clientes em potencial de uma lista ou de um programa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione as informações que deseja incluir no pacote de saída deste módulo. Os campos estão disponíveis com base na [!UICONTROL Record Type] selecionada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Records]

Este módulo de pesquisa recupera uma lista de registros que correspondem a critérios de pesquisa específicos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao [!DNL Workfront Fusion], consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecione o tipo de registro que deseja pesquisar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaigns]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programs]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Field]</p> </td> 
   <td> <p>Selecione o campo pelo qual deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value / values]</td> 
   <td>Insira o valor do campo que você deseja pesquisar. Se o campo permitir a pesquisa de vários valores, para cada valor que você deseja pesquisar, clique em <b>[!UICONTROL Add item]</b> e insira o valor.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Selecione as informações que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>
