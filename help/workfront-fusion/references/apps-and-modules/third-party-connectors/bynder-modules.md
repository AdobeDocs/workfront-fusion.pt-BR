---
title: Módulos do Bynder
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam  [!DNL Bynder], bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
TQID: https://experienceleague.adobe.com/2NCbEM8bb0s7m30uCFTWK-wYdhCYKEZC-W01Zr21mRw
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1863
ht-degree: 31%

---

# Módulos do [!DNL Bynder]

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam [!DNL Bynder], bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!DNL Bynder], você deve ter uma conta do [!DNL Bynder].

## Informações da API Bynder

O conector Bynder usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.25.21</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL Bynder] ao Workfront Fusion  {#connect-bynder-to-workfront-fusion}

>[!NOTE]
>
>O Bynder usa o tipo de concessão Authorization code / refresh token. Esse é o único tipo de concessão que o conector do Fusion Bynder usa.

* [Criar uma conexão com o  [!DNL Bynder] a partir do Workfront Fusion](#create-a-connection-to-bynder-from-workfront-fusion)
* [Gerar uma [!UICONTROL ID do Cliente] e um [!UICONTROL Segredo do Cliente] em [!DNL Bynder] (Opcional)](#generate-a-client-id-and-client-secret-in-bynder-optional)

### Criar uma conexão com [!DNL Bynder] a partir do Workfront Fusion

Você pode criar uma conexão do Workfront Fusion com sua conta do [!DNL Bynder] diretamente de dentro de um módulo [!DNL Bynder].

1. Em qualquer módulo [!DNL Bynder], clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. Selecione o domínio [!DNL Bynder] ao qual você deseja se conectar.
1. (Opcional) Clique em **[!UICONTROL Configurações avançadas]** e digite sua [!UICONTROL ID do Cliente] e [!UICONTROL Segredo do Cliente].

   Para obter instruções sobre como gerar a ID do Cliente e o Segredo do Cliente, consulte [Gerar uma ID do Cliente e um Segredo do Cliente em [!DNL Bynder] (Opcional)](#generate-a-client-id-and-client-secret-in-bynder-optional) neste artigo.

1. Na janela [!UICONTROL logon], digite seu nome de usuário (endereço de email) e senha.
1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

### Gerar uma [!UICONTROL ID do Cliente] e um [!UICONTROL Segredo do Cliente] em [!DNL Bynder] (Opcional)

Se você quiser criar uma conexão usando a ID de Cliente e o Segredo do Cliente, gere-os a partir da conta do [!DNL Bynder]. A ID e o Segredo do Cliente são gerados quando você cria um aplicativo no [!DNL Bynder].

Para obter instruções sobre como criar um aplicativo no [!DNL Bynder], consulte [Aplicativos do Oauth 2.0](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/) na documentação do [!DNL Bynder].

>[!NOTE]
>
>* Ao criar o aplicativo em [!DNL Bynder], insira o seguinte como `redirect uri`:
>
>   * Cluster dos EUA: `https://app.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Cluster UE: `https://app-eu.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Cluster Azure: `https://app-az.workfrontfusion.com/oauth/cb/workfront-bynder`
>* O Bynder usa o tipo de concessão Authorization code / refresh token. Esse é o único tipo de concessão que o conector do Fusion Bynder usa.

## Módulos do [!DNL Bynder] e seus campos

Ao configurar módulos do [!DNL Bynder], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos do [!DNL Bynder] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ações](#actions)
* [Pesquisas](#searches)
* [Acionadores](#triggers)

### Ações

* [[!UICONTROL Adicionar uma marca aos ativos]](#add-a-tag-to-assets)
* [[!UICONTROL Adicionar ativos a uma coleção]](#add-assets-to-a-collection)
* [[!UICONTROL Chamada de API personalizada]](#custom-api-call)
* [[!UICONTROL Baixar ativo]](#download-asset)
* [[!UICONTROL Ler metadados de ativos]](#read-asset-metadata)
* [[!UICONTROL Remover uma marca] dos ativos](#remove-a-tag-from-assets)
* [[!UICONTROL Remover ativos da coleção]](#remove-assets-from-collection)
* [[!UICONTROL Atualizar metadados de ativos]](#update-asset-metadata)
* [[!UICONTROL Carregar ativo]](#upload-asset)

#### [!UICONTROL Adicionar uma marca aos ativos]

Este módulo de ação adiciona uma tag a um ou mais ativos

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Marca]</td> 
   <td> <p>Insira ou mapeie a ID da tag que você deseja adicionar aos ativos.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs de Ativo]</td> 
   <td> <p>Para cada ativo que você deseja marcar, clique em <strong>[!UICONTROL Adicionar item]</strong> e, em seguida, insira ou mapeie a ID do ativo.</p> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL Adicionar ativos a uma coleção]

Este módulo de ação adiciona um ou mais ativos a uma coleção.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Coleção]</td> 
   <td> <p>Insira ou mapeie a ID da coleção onde deseja adicionar ativos.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs de Ativo]</td> 
   <td> <p>Para cada ativo que você deseja adicionar à coleção, clique em <strong>[!UICONTROL Adicionar item]</strong> e, em seguida, insira ou mapeie a ID do ativo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API do [!DNL Bynder]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Bynder].

Ao configurar esse módulo, os campos a seguir são exibidos.

O módulo retorna um código de status, juntamente com os cabeçalhos e o corpo da chamada de API.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Insira um caminho relativo a <code>https://{your-bynder-domain}/api/{api-version}/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
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

#### [!UICONTROL Baixar ativo]

Este módulo de ação baixa um único ativo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Insira ou mapeie a ID do ativo que deseja baixar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Versão do ativo]</td> 
   <td> <p>Insira ou mapeie a versão do ativo que deseja baixar. Para baixar a versão mais recente do ativo, deixe o campo vazio.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler metadados de ativos]

Esse módulo de ação lê os metadados de um ativo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Insira ou mapeie a ID do ativo para o qual deseja recuperar metadados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecione as informações que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remover uma marca dos ativos]

Este módulo de ação remove uma tag de um ou mais ativos

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Marca]</td> 
   <td> <p>Insira ou mapeie a ID da tag que você deseja remover dos ativos.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs de Ativo]</td> 
   <td> <p>Para cada ativo do qual você deseja remover uma marca, clique em <strong>[!UICONTROL Adicionar item]</strong> e digite ou mapeie a ID do ativo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remover ativos da coleção]

Este módulo de ação remove um ou mais ativos de uma coleção.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Coleção]</td> 
   <td> <p>Insira ou mapeie a ID da coleção onde deseja remover os ativos.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs de Ativo]</td> 
   <td> <p>Para cada ativo que você deseja remover da coleção, clique em <strong>[!UICONTROL Adicionar item]</strong> e, em seguida, insira ou mapeie a ID do ativo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar metadados de ativos]

Esse módulo de ação atualiza os metadados de um ativo existente.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Insira ou mapeie a ID do ativo para o qual deseja atualizar os metadados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Selecione os campos para os quais deseja inserir informações e, em seguida, insira ou mapeie as informações com as quais deseja atualizar os metadados nesses campos. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metapropriedades]</p> </td> 
   <td>Selecione as opções que deseja atualizar e, em seguida, insira ou mapeie as informações nessas propriedades. As metapropriedades são informações sobre o ativo que não representam campos específicos no ativo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar ativo]

Esse módulo de ação carrega um único ativo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Salvar como]</td> 
   <td> <p>Selecione como deseja salvar o arquivo que você está fazendo upload.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Novo ativo]</strong> </p> <p>Selecione os campos e metapropriedades para os quais você deseja inserir informações e insira as informações nesses campos.</p> <p>Insira ou mapeie a ID da marca que você deseja usar para o ativo carregado.</p> </li> 
     <li> <p><strong>[!UICONTROL Nova versão de ativo]</strong> </p> <p>Insira a ID do ativo para o qual você está fazendo upload de uma nova versão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carregamento de arquivo assíncrono]</td> 
   <td>Ative essa opção ao fazer upload de arquivos grandes. Isso impede que arquivos grandes bloqueiem a execução do cenário.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Listar registro]](#list-record)
* [[!UICONTROL Pesquisar Assets]](#search-assets)

#### [!UICONTROL Listar registro]

Este módulo de pesquisa recupera todos os itens de um tipo específico.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja listar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Ler todas as coleções]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Ler informações sobre todas as marcas]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Ler todos os ativos de uma coleção]</strong> </p> <p>Insira ou mapeie a ID da coleção da qual você deseja listar ativos.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecione os campos que deseja incluir na saída do módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar Assets]

Este módulo de pesquisa procura por ativos com base nos critérios que você forneceu.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td> <p>Informe os critérios de pesquisa. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Campo]</strong> </p> <p>Selecione o campo que deseja usar na pesquisa</p> </li> 
     <li> <p><strong>[!UICONTROL Operador Lógico]</strong> </p> <p>Selecione o operador que deseja usar na pesquisa.</p> </li> 
     <li> <p><strong>[!UICONTROL Valor]</strong> </p> <p>Insira ou mapeie o valor a ser procurado no campo selecionado. O tipo de valor deve ser igual ao tipo de dados do campo selecionado. </p> <p>Para obter mais informações sobre tipos de dados, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipos de dados de item</a>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conjunto de resultados]</td> 
   <td>Selecione se deseja retornar o primeiro ativo correspondente ou todos os ativos correspondentes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classificar por]</td> 
   <td> <p>Selecione o campo pelo qual deseja classificar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Direção de Classificação]</td> 
   <td> <p>Selecione se deseja classificar em ordem crescente ou decrescente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecione os campos que deseja incluir na saída do módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Acionadores

#### [!UICONTROL Observar ativos]

Esse módulo de acionamento inicia um cenário quando um ativo é criado ou atualizado.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao Workfront Fusion, consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao Workfront Fusion </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Tipo de evento</td>
    <td>Selecione se deseja iniciar o cenário quando um novo ativo for criado ou quando um ativo existente for atualizado.</td>
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL Collections]</td>
   <td> <p>Selecione a coleção que você deseja observar para novos ativos. Para observar todas as coleções, deixe este campo vazio.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Saídas</td>
    <td>Selecione os campos que deseja incluir na saída.</td>
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Limit]</td>

<td> <p>Insira o número máximo de registros que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>
