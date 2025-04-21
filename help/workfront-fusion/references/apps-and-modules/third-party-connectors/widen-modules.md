---
title: Ampliar módulos
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o [!UICONTROL Widen], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 11376e58-a44b-4766-85dc-e2421b0112de
source-git-commit: b5387e4ba84d67d6ea2472282c212e396ba93d4f
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 0%

---

# [!DNL Widen] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam o [!UICONTROL Widen], bem como conectá-los a vários aplicativos e serviços de terceiros.

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion</p>
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

Para usar os módulos [!UICONTROL Widen], você deve ter uma conta [!UICONTROL Widen].

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

## Conectar [!DNL Widen] a [!DNL Workfront Fusion]  {#connect-widen-to-workfront-fusion}

Você pode criar uma conexão com sua conta do [!DNL Widen] diretamente de dentro de um módulo do [!DNL Widen].

1. Em qualquer módulo [!DNL Widen], clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. Selecione o ambiente e o tipo de conta aos quais você está se conectando. Isso é apenas para fins informativos e é exibido na área Conexões do Fusion.
1. Selecione o domínio [!DNL Widen] ao qual você deseja se conectar.
1. Insira o token para sua conta [!DNL Widen]. Para obter instruções sobre como localizar este token, consulte as [[!DNL Widen] Perguntas frequentes sobre API](https://community.widen.com/collective/s/article/API-FAQs).
1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## [!DNL Widen] módulos e seus campos

Ao configurar módulos do [!DNL Widen], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Widen] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Módulos acionadores](#trigger-modules)
* [Módulos de ação](#action-modules)
* [Pesquisar módulos](#search-modules)

### Módulos acionadores

#### [!UICONTROL Observar ativos]

Esse módulo de acionamento inicia um cenário quando um ativo é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de evento]</td> 
   <td> <p>Selecione se você deseja observar novos ativos ou ativos atualizados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expandir]</td> 
   <td> <p>Selecione as propriedades que deseja incluir na saída do módulo, além dos campos de ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Módulos de ação

* [[!UICONTROL Adicionar ativos a coleções]](#add-assets-to-collections)
* [[!UICONTROL Chamada de API personalizada]](#custom-api-call)
* [[!UICONTROL Baixar arquivo]](#download-file)
* [[!UICONTROL Ler informações do ativo]](#read-asset-info)
* [[!UICONTROL Remover ativos da coleção]](#remove-assets-from-collection)
* [[!UICONTROL Atualizar metadados de ativos]](#update-asset-metadata)
* [[!UICONTROL Carregar um arquivo]](#upload-a-file)

#### [!UICONTROL Adicionar ativos a coleções]

Este módulo de ação adiciona um ou mais ativos às coleções.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Coleções]</td> 
   <td>Para cada coleção à qual você deseja adicionar os ativos, clique em <strong>[ID de Coleção]</strong> e insira ou mapeie a [!UICONTROL ID de Coleção].</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> Para cada ativo que você deseja adicionar a uma coleção, clique em <strong>[!UICONTROL Assets ID]</strong> e insira ou mapeie a ID do ativo.</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Widen]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Widen].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Versão da API]</td> 
   <td>Selecione se você deseja usar a versão mais recente da API [!DNL Widen] ou a versão 1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira ou mapeie o URL da sua chamada de API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O [!UICONTROL Workfront Fusion] adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Baixar arquivo]

Este módulo de ação baixa um ativo da sua conta [!DNL Widen].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Ativo]</td> 
   <td> <p>Insira ou mapeie a ID do ativo que deseja baixar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler informações do ativo]

Este módulo de ação recupera um ativo individual por sua ID exclusiva.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Ativo]</td> 
   <td> <p>Insira ou mapeie a ID do ativo cujas informações você deseja ler.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expandir]</td> 
   <td> <p>Selecione as propriedades que deseja incluir na saída do módulo, além dos campos de ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remover ativos da coleção]

Este módulo de ação remove um ou mais ativos das coleções.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Coleções]</td> 
   <td>Para cada coleção da qual você deseja remover ativos, clique em <strong>[ID de Coleção]</strong> e insira ou mapeie a [!UICONTROL ID de Coleção].</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> Para cada ativo que você deseja remover de uma coleção, clique em <strong>[!UICONTROL Assets ID]</strong> e insira ou mapeie a ID do Ativo.</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar metadados de ativos]

Esse módulo de ação atualiza os campos de metadados de um ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Ativo]</td> 
   <td> <p>Insira ou mapeie a ID do ativo no qual deseja atualizar os metadados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de metadados]</td> 
   <td> <p>Selecione o tipo de metadados para os metadados que deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadados]</td> 
   <td>Selecione os campos de metadados que deseja atualizar. Para cada campo, insira o novo valor do campo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de ativos com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um arquivo]

Este módulo de ação carrega um arquivo na conta do [!DNL Widen].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carregar Perfil]</td> 
   <td> <p>Selecione o perfil de upload que deseja que o módulo use.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método de Carregamento]</td> 
   <td> <p>Selecione como deseja fazer upload do arquivo.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Do Arquivo]</strong> </p> <p>Selecione ou mapeie o arquivo de origem de um módulo anterior.</p> </li> 
     <li> <p><strong>[!UICONTROL Por URL]</strong> </p> <p>Insira ou mapeie o URL do arquivo que você deseja fazer upload.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do arquivo]</td> 
   <td>Insira ou mapeie um nome para o arquivo carregado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Metadados]</td> 
   <td>Selecione o tipo de metadados para o arquivo que você deseja fazer upload.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadados]</td> 
   <td>Selecione os campos de metadados que deseja incluir no upload do arquivo. Para cada campo, insira o [!UICONTROL value] para o campo.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisar módulos

* [[!UICONTROL Ler ativos da coleção]](#read-collection-assets)
* [[!UICONTROL Pesquisar ativos]](#search-assets)

#### [!UICONTROL Ler ativos da coleção]

Este módulo de ação recupera uma lista de ativos em uma coleção.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Coleção]</td> 
   <td> <p>Insira ou mapeie a ID da coleção que contém os ativos que você deseja ler.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Iniciar]</td> 
   <td>Informe ou mapeie o número do primeiro item que deseja listar. Essa é uma maneira de paginar os registros.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Máx.]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classificar por]</td> 
   <td> <p>Selecione a propriedade pela qual deseja classificar os ativos. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordem]</td> 
   <td>Selecione se deseja classificar ativos em ordem crescente ou decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar ativos]

Este módulo de pesquisa recupera uma lista de ativos que correspondem aos critérios de pesquisa específicos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
  <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Widen] ao [!DNL Workfront Fusion], consulte <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Widen] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pesquisar consulta]</td> 
   <td> <p>Informe os critérios pelos quais deseja pesquisar ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classificar por]</td> 
   <td> <p>Selecione como deseja classificar os ativos. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordem]</td> 
   <td>Selecione se deseja classificar ativos em ordem crescente ou decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Incluir excluído]</td> 
   <td>Habilite essa opção para incluir ativos excluídos na pesquisa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Incluir arquivado]</p> </td> 
   <td> <p>Ative essa opção para incluir ativos arquivados na pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pesquisar texto do documento]</td> 
   <td>Habilite esta opção para incluir o texto do documento na sua pesquisa, ou defina como falso para incluir somente ativos para os quais o título corresponde aos critérios de pesquisa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Deslocamento]</td> 
   <td>Informe ou mapeie o número do primeiro item para o qual deseja recuperar detalhes. Essa é uma maneira de paginar os registros.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rolagem]</td> 
   <td>Ative essa opção para permitir a rolagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expandir]</td> 
   <td> <p>Selecione as propriedades que deseja incluir na saída do módulo, além dos campos de ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
 </tbody> 
</table>
