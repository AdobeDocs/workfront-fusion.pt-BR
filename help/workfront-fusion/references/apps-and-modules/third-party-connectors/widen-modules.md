---
title: Ampliar módulos
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam [!UICONTROL Widen], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 11376e58-a44b-4766-85dc-e2421b0112de
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 1%

---

# [!DNL Widen] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!UICONTROL Widen], bem como conectá-los a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!UICONTROL Widen], você deve ter uma conta [!UICONTROL Widen].

## Ampliar informações da API

O conector Widen usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.10.11</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!DNL Widen] a [!DNL Workfront Fusion] {#connect-widen-to-workfront-fusion}

Você pode criar uma conexão com sua conta do [!DNL Widen] diretamente de dentro de um módulo do [!DNL Widen].

1. Em qualquer módulo [!DNL Widen], clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. Selecione o domínio [!DNL Widen] ao qual você deseja se conectar.
1. Insira o token para sua conta [!DNL Widen]. Para obter instruções sobre como localizar este token, consulte as [[!DNL Widen] Perguntas frequentes sobre API](https://community.widen.com/collective/s/article/API-FAQs).
1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

## [!DNL Widen] módulos e seus campos

Ao configurar módulos do [!DNL Widen], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Widen] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Módulos acionadores](#trigger-modules)
* [Módulos de ação](#action-modules)
* [Pesquisar módulos](#search-modules)

### Módulos acionadores

#### [!UICONTROL Watch assets]

Esse módulo de acionamento inicia um cenário quando um ativo é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p>Selecione se você deseja observar novos ativos ou ativos atualizados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Selecione as propriedades que deseja incluir na saída do módulo, além dos campos de ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Módulos de ação

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read asset info]](#read-asset-info)
* [[!UICONTROL Add assets to collections]](#add-assets-to-collections)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Download File]](#download-file)
* [[!UICONTROL Upload] um arquivo](#upload-a-file)

#### [!UICONTROL Custom API Call]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Widen]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Widen].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Selecione se você deseja usar a versão mais recente da API [!DNL Widen] ou a versão 1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira ou mapeie o URL da sua chamada de API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read asset info]

Este módulo de ação recupera um ativo individual por sua ID exclusiva.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Insira ou mapeie a ID do ativo cujas informações você deseja ler.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Selecione as propriedades que deseja incluir na saída do módulo, além dos campos de ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add assets to collections]

Este módulo de ação adiciona um ou mais ativos às coleções.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td> <p>Para cada coleção à qual você deseja adicionar os ativos:</p> 
    <ol> 
     <li value="1"> <p> Clique em <strong>[!UICONTROL Add]</strong>.</p> </li> 
     <li value="2"> <p>Insira ou mapeie o [!UICONTROL Collection ID].</p> </li> 
     <li value="3"> <p>Clique em <strong>[!UICONTROL Add item]</strong>.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> <p>Para cada ativo que você deseja adicionar a uma coleção:</p> 
    <ol> 
     <li value="1"> <p> Clique em <strong>[!UICONTROL Add]</strong>.</p> </li> 
     <li value="2"> <p>Insira ou mapeie a ID do ativo.</p> </li> 
     <li value="3"> <p>Clique em <strong>[!UICONTROL Add item]</strong>.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection]

Este módulo de ação remove um ou mais ativos das coleções.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td> <p>Para cada coleção da qual você deseja remover os ativos:</p> 
    <ol> 
     <li value="1"> <p> Clique em <strong>[!UICONTROL Add]</strong>.</p> </li> 
     <li value="2"> <p>Insira ou mapeie a ID da coleção.</p> </li> 
     <li value="3"> <p>Clique em <strong>[!UICONTROL Add item]</strong>.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ASSETS ID</td> 
   <td> <p>Para cada ativo que você deseja remover de uma coleção:</p> 
    <ol> 
     <li value="1"> <p> Clique em <strong>[!UICONTROL Add]</strong>.</p> </li> 
     <li value="2"> <p>Insira ou mapeie a ID do ativo.</p> </li> 
     <li value="3"> <p>Clique em <strong>[!UICONTROL Add item]</strong>.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

Esse módulo de ação atualiza os campos de metadados de um ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Insira ou mapeie a ID do ativo no qual deseja atualizar os metadados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata type]</td> 
   <td> <p>Selecione o tipo de metadados para os metadados que deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Selecione os campos de metadados que deseja atualizar. Para cada campo, insira o novo valor do campo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download File]

Este módulo de ação baixa um ativo da sua conta [!DNL Widen].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Insira ou mapeie a ID do ativo que deseja baixar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

Este módulo de ação carrega um arquivo na conta do [!DNL Widen].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Profile]</td> 
   <td> <p>Selecione o perfil de upload que deseja que o módulo use.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Method]</td> 
   <td> <p>Selecione como deseja fazer upload do arquivo.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL From File]</strong> </p> <p>Selecione ou mapeie o arquivo de origem de um módulo anterior.</p> </li> 
     <li> <p><strong>[!UICONTROL By URL]</strong> </p> <p>Insira ou mapeie o URL do arquivo que você deseja fazer upload.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Insira ou mapeie um nome para o arquivo carregado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata Type]</td> 
   <td>Selecione o tipo de metadados para o arquivo que você deseja fazer upload.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Selecione os campos de metadados que deseja incluir no upload do arquivo. Para cada campo, insira o [!UICONTROL value] para o campo.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisar módulos

* [[!UICONTROL Read collection assets]](#read-collection-assets)
* [[!UICONTROL Search assets]](#search-assets)

#### [!UICONTROL Read collection assets]

Este módulo de ação recupera uma lista de ativos em uma coleção.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Insira ou mapeie a ID da coleção que contém os ativos que você deseja ler.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>Informe ou mapeie o número do primeiro item que deseja listar. Essa é uma maneira de paginar os registros.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>Selecione a propriedade pela qual deseja classificar os ativos. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Selecione se deseja classificar ativos em ordem crescente ou decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search assets]

Este módulo de pesquisa recupera uma lista de ativos que correspondem aos critérios de pesquisa específicos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search query]</td> 
   <td> <p>Informe os critérios pelos quais deseja pesquisar ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>Selecione como deseja classificar os ativos. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Selecione se deseja classificar ativos em ordem crescente ou decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include deleted]</td> 
   <td>Habilite essa opção para incluir ativos excluídos na pesquisa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Include archived]</p> </td> 
   <td> <p>Ative essa opção para incluir ativos arquivados na pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search document text]</td> 
   <td>Habilite esta opção para incluir o texto do documento na pesquisa, ou falso para incluir apenas ativos para os quais o título corresponde aos critérios de pesquisa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Offset]</td> 
   <td>Informe ou mapeie o número do primeiro item para o qual deseja recuperar detalhes. Essa é uma maneira de paginar os registros.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scroll]</td> 
   <td>Ative essa opção para permitir a rolagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Selecione as propriedades que deseja incluir na saída do módulo, além dos campos de ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
 </tbody> 
</table>
