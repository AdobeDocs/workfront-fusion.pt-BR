---
title: Módulos do Split.io
description: Em um cenário  [!DNL Adobe Workfront Fusion] , é possível automatizar fluxos de trabalho que usam  [!DNL Split.io], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 7d738a96-5424-4c30-831f-82e1d4c6f9d2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1493'
ht-degree: 0%

---

# [!DNL Split.io] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Split.io], bem como conectá-los a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Pré-requisitos

Para usar módulos [!DNL Split.io], você deve ter uma conta [!DNL Split.io].

## Informações da API Split.io

O conector Split.io usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.split.io/internal/api</td>
   </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.34.1</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!DNL Split.io] a [!DNL Workfront Fusion] {#connect-split-io-to-workfront-fusion}

Você pode criar uma conexão com sua conta do [!DNL Split.io] diretamente de dentro de um módulo do [!DNL Split.io].

1. Em qualquer módulo [!DNL Split.io], clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. Insira um nome para a conexão.
1. Insira sua chave de API [!DNL Split.io].

   Para obter mais informações sobre [!DNL Split.io] chaves de API, consulte [chaves de API](https://help.split.io/hc/en-us/articles/360019916211-API-keys) na documentação [!DNL Split.io].

1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

## [!DNL Split.io] módulos e seus campos

Ao configurar módulos do [!DNL split.io], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL split.io] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ações](#actions)
* [Pesquisas](#searches)

### Ações

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Get Split]](#get-split)
* [[!UICONTROL Get Split Definition in Environment]](#get-split-definition-in-environment)
* [[!UICONTROL Create Split]](#create-split)
* [[!UICONTROL Delete Split]](#delete-split)
* [[!UICONTROL Create Split Definition in Environment]](#create-split-definition-in-environment)
* [[!UICONTROL Remove Split Definition from Environment]](#remove-split-definition-from-environment)
* [[!UICONTROL Partial Update Split Definition in Environment]](#partial-update-split-definition-in-environment)
* [[!UICONTROL Associate Tags]](#associate-tags)

#### [!UICONTROL Custom API Call]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL split.io]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL split.io].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://api.split.io/internal/api/v2/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de registros com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split]

Este módulo de ação recupera a divisão.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém a divisão que você deseja recuperar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Insira ou mapeie o nome da divisão que deseja recuperar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split Definition in Environment]

Esse módulo de ação recupera uma definição de divisão específica do ambiente designado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém a definição de divisão que deseja recuperar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Selecione ou mapeie o ambiente que contém a definição de divisão que deseja recuperar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Insira ou mapeie o nome da divisão para a qual deseja recuperar a definição de divisão.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split]

Esse módulo de ação cria uma nova divisão em sua organização, considerando um tipo de tráfego.

>[!NOTE]
>
>A API não configura a divisão em nenhum ambiente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho em que deseja criar a divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Traffic Type ID or Name]</td> 
   <td>Selecione ou mapeie o tipo de tráfego que deseja usar para criar a divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Insira ou mapeie um nome para a divisão que deseja criar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Description]</td> 
   <td>Insira ou mapeie uma descrição [!UICONTROL split] para a divisão que você deseja criar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Split]

Esse módulo de ação exclui uma divisão da sua organização. Essa ação desconfigura automaticamente a definição de divisão de todos os ambientes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho no qual deseja excluir a divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Insira ou mapeie o nome da divisão que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split Definition in Environment]

Este módulo de ação configura uma definição de divisão para um ambiente específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho em que deseja criar uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Selecione ou mapeie o ambiente em que deseja criar uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Insira ou mapeie o nome da divisão para a qual deseja criar uma definição.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Insira ou mapeie comentários que deseja adicionar à definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rules]</td> 
   <td> <p>Para cada regra de direcionamento que você deseja adicionar à definição, clique em <b>[!UICONTROL Add item]</b> e, em seguida, insira ou mapeie a regra.</p> <p>Para obter mais informações sobre regras de direcionamento, consulte <a href="https://docs.split.io/reference#create-split-definition-in-environment">Criar definição de divisão em um ambiente</a> na documentação [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default rule]</td> 
   <td> <p>Insira ou mapeie a regra que você deseja que a divisão use para o tráfego que não atende às especificações das outras regras.</p> <p>Para obter mais informações sobre regras de direcionamento, consulte <a href="https://docs.split.io/reference#create-split-definition-in-environment">Criar definição de divisão em um ambiente</a> na documentação [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default treatment]</td> 
   <td> <p>Insira ou mapeie o tratamento que deseja que a divisão use se a divisão for eliminada ou se o cliente não for incluído na alocação de tráfego.</p> <p>Para obter mais informações sobre tratamentos, consulte <a href="https://docs.split.io/reference#create-split-definition-in-environment">Criar definição de divisão em um ambiente</a> na documentação [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Treatments]</td> 
   <td> <p>Para cada tratamento que deseja adicionar à definição, clique em <b>[!UICONTROL Add item]</b> e, em seguida, insira ou mapeie o tratamento.</p> <p>Para obter mais informações sobre tratamentos, consulte <a href="https://docs.split.io/reference#create-split-definition-in-environment">Criar definição de divisão em um ambiente</a> na documentação [!DNL Split.io].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Split Definition from Environment]

Este módulo de ação desconfigura uma definição de divisão para um ambiente específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho para o qual deseja remover uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Selecione ou mapeie o ambiente no qual deseja remover uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Insira ou mapeie o nome da divisão para a qual deseja remover uma definição.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Insira ou mapeie comentários que deseja adicionar à definição de divisão.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Partial Update Split Definition in Environment]

Este módulo de ação atualiza uma definição de divisão para um ambiente específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho no qual deseja atualizar uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Selecione ou mapeie o ambiente em que deseja atualizar uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Insira ou mapeie o nome da divisão para a qual deseja atualizar uma definição.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update content]</td> 
   <td> <p>Para cada atributo da divisão que você deseja atualizar, clique em <b>[!UICONTROL Add item]</b> e insira ou mapeie as alterações desejadas.</p> <p>Para obter mais informações, consulte <a href="https://docs.split.io/reference#partial-update-split-definition-in-environment">Definição de Divisão de Atualização Parcial em Ambiente</a> na documentação [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Insira ou mapeie comentários que deseja adicionar à definição de divisão.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Associate Tags]

Esse módulo de ação adiciona tags ao objeto especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho ao qual deseja adicionar uma tag.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Name]</td> 
   <td>Insira ou mapeie o nome do objeto ao qual você deseja adicionar tags,</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type]</td> 
   <td> <p>Insira ou mapeie o tipo de objeto ao qual você deseja adicionar tags.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> <p>Para cada marca que você deseja adicionar, clique em <b>[!UICONTROL Add item]</b> e insira ou mapeie a marca.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Get Workspaces]](#get-workspaces)
* [[!UICONTROL Get Environments]](#get-environments)
* [[!UICONTROL Get Splits]](#get-splits)
* [[!UICONTROL List Split Definitions in an Environment]](#list-split-definitions-in-an-environment)
* [[!UICONTROL Get Traffic Types]](#get-traffic-types)

#### [!UICONTROL Get Workspaces]

Este módulo de pesquisa recupera os espaços de trabalho de uma organização.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de espaços de trabalho que você deseja que o módulo recupere durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Environments]

Este módulo de pesquisa recupera uma lista de ambientes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém os ambientes que deseja listar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Splits]

Este módulo de pesquisa recupera uma lista de divisões.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém as divisões que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de divisões que você deseja que o módulo recupere durante cada ciclo de execução do cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Split Definitions in an Environment]

Este módulo de pesquisa recupera uma lista de definições de divisão em um determinado ambiente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém as definições de divisão que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Selecione ou mapeie o ambiente que contém as definições de divisão que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de definições de divisão que você deseja que o módulo recupere durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Traffic Types]

Este módulo de pesquisa recupera uma lista de tipos de tráfego.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao [!DNL Workfront Fusion], consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém os tipos de tráfego que deseja listar.</td> 
  </tr> 
 </tbody> 
</table>
