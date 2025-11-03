---
title: Módulos do Split.io
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o  [!DNL Split.io], bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 7d738a96-5424-4c30-831f-82e1d4c6f9d2
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: tm+mt
source-wordcount: '1925'
ht-degree: 0%

---

# [!DNL Split.io] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Split.io], bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!DNL Split.io], você deve ter uma conta [!DNL Split.io].

## Informações da API Split.io

O conector Split.io usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
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

## Conectar o [!DNL Split.io] ao Workfront Fusion  {#connect-split-io-to-workfront-fusion}

Você pode criar uma conexão com sua conta do [!DNL Split.io] diretamente de dentro de um módulo do [!DNL Split.io].

1. Em qualquer módulo [!DNL Split.io], clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. Preencha os campos a seguir.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">[!UICONTROL Nome da Conexão]</td> 
       <td> <p>Insira um nome para a conexão.</p> </td> 
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
       <td role="rowheader">[!UICONTROL Chave de API]</td> 
       <td>Insira sua chave de API [!DNL Split.io].<p>Para obter mais informações sobre [!DNL Split.io] chaves de API, consulte <a href="https://help.split.io/hc/en-us/articles/360019916211-API-keys">chaves de API</a> na documentação [!DNL Split.io].</p></td> 
      </tr> 
     </tbody> 
    </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## [!DNL Split.io] módulos e seus campos

Ao configurar módulos do [!DNL split.io], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL split.io] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ações](#actions)
* [Pesquisas](#searches)

### Ações

* [[!UICONTROL Marcas Associadas]](#associate-tags)
* [[!UICONTROL Criar Divisão]](#create-split)
* [[!UICONTROL Criar Definição de Divisão no Ambiente]](#create-split-definition-in-environment)
* [[!UICONTROL Chamada de API personalizada]](#custom-api-call)
* [[!UICONTROL Excluir Divisão]](#delete-split)
* [[!UICONTROL Obter Divisão]](#get-split)
* [[!UICONTROL Obter Definição de Divisão no Ambiente]](#get-split-definition-in-environment)
* [[!UICONTROL Definição de Divisão de Atualização Parcial no Ambiente]](#partial-update-split-definition-in-environment)
* [[!UICONTROL Remover definição dividida do ambiente]](#remove-split-definition-from-environment)

#### [!UICONTROL Marcas Associadas]

Esse módulo de ação adiciona tags ao objeto especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho ao qual deseja adicionar uma tag.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Objeto]</td> 
   <td>Insira ou mapeie o nome do objeto ao qual você deseja adicionar tags.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Objeto]</td> 
   <td> <p>Insira ou mapeie o tipo de objeto ao qual você deseja adicionar tags.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Marcas]</td> 
   <td> <p>Para cada marca que você deseja adicionar, clique em <b>[!UICONTROL Adicionar item]</b> e insira ou mapeie a marca.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar Divisão]

Esse módulo de ação cria uma nova divisão em sua organização, considerando um tipo de tráfego.

>[!NOTE]
>
>A API não configura a divisão em nenhum ambiente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho em que deseja criar a divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Identificação ou Nome de Tipo de Tráfego]</td> 
   <td>Selecione ou mapeie o tipo de tráfego que deseja usar para criar a divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dividir Nome]</td> 
   <td> <p>Insira ou mapeie um nome para a divisão que deseja criar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dividir Descrição]</td> 
   <td>Insira ou mapeie uma descrição de [!UICONTROL divisão] para a divisão que você deseja criar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar Definição de Divisão no Ambiente]

Este módulo de ação configura uma definição de divisão para um ambiente específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho em que deseja criar uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome ou ID de Ambiente]</td> 
   <td>Selecione ou mapeie o ambiente em que deseja criar uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dividir Nome]</td> 
   <td> <p>Insira ou mapeie o nome da divisão para a qual deseja criar uma definição.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comentários]</td> 
   <td>Insira ou mapeie comentários que deseja adicionar à definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Regras]</td> 
   <td> <p>Para cada regra de direcionamento que você deseja adicionar à definição, clique em <b>[!UICONTROL Adicionar item]</b> e, em seguida, insira ou mapeie a regra. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Regra padrão]</td> 
   <td> <p>Insira ou mapeie a regra que você deseja que a divisão use para o tráfego que não atende às especificações das outras regras.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tratamento padrão]</td> 
   <td> <p>Insira ou mapeie o tratamento que deseja que a divisão use se a divisão for eliminada ou se o cliente não for incluído na alocação de tráfego.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tratamentos]</td> 
   <td> <p>Para cada tratamento que você deseja adicionar à definição, clique em <b>[!UICONTROL Adicionar item]</b> e, em seguida, insira ou mapeie o tratamento e o tamanho.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL split.io]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL split.io].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://api.split.io/internal/api/v2/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de registros com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir Divisão]

Esse módulo de ação exclui uma divisão da sua organização. Essa ação desconfigura automaticamente a definição de divisão de todos os ambientes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho no qual deseja excluir a divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dividir Nome]</td> 
   <td> <p>Insira ou mapeie o nome da divisão que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter Divisão]

Este módulo de ação recupera a divisão.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém a divisão que você deseja recuperar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dividir Nome]</td> 
   <td> <p>Insira ou mapeie o nome da divisão que deseja recuperar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter Definição de Divisão no Ambiente]

Esse módulo de ação recupera uma definição de divisão específica do ambiente designado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém a definição de divisão que deseja recuperar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome ou ID de Ambiente]</td> 
   <td>Selecione ou mapeie o ambiente que contém a definição de divisão que deseja recuperar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dividir Nome]</td> 
   <td> <p>Insira ou mapeie o nome da divisão para a qual deseja recuperar a definição de divisão.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Definição de Divisão de Atualização Parcial no Ambiente]

Este módulo de ação atualiza uma definição de divisão para um ambiente específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho no qual deseja atualizar uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome ou ID de Ambiente]</td> 
   <td>Selecione ou mapeie o ambiente em que deseja atualizar uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dividir Nome]</td> 
   <td> <p>Insira ou mapeie o nome da divisão para a qual deseja atualizar uma definição.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Atualizar conteúdo]</td> 
   <td> <p>Para cada atributo da divisão que você deseja atualizar, clique em <b>[!UICONTROL Adicionar item]</b> e insira ou mapeie as alterações desejadas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comentários]</td> 
   <td>Insira ou mapeie comentários que deseja adicionar à definição de divisão.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remover definição dividida do ambiente]

Este módulo de ação desconfigura uma definição de divisão para um ambiente específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho para o qual deseja remover uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome ou ID de Ambiente]</td> 
   <td>Selecione ou mapeie o ambiente no qual deseja remover uma definição de divisão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dividir Nome]</td> 
   <td> <p>Insira ou mapeie o nome da divisão para a qual deseja remover uma definição.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comentários]</td> 
   <td>Insira ou mapeie comentários que deseja adicionar à definição de divisão.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Marcas Associadas]

Esse módulo de ação adiciona tags ao objeto especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho ao qual deseja adicionar uma tag.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Objeto]</td> 
   <td>Insira ou mapeie o nome do objeto ao qual você deseja adicionar tags,</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Objeto]</td> 
   <td> <p>Insira ou mapeie o tipo de objeto ao qual você deseja adicionar tags.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Marcas]</td> 
   <td> <p>Para cada marca que você deseja adicionar, clique em <b>[!UICONTROL Adicionar item]</b> e insira ou mapeie a marca.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Obter ambientes]](#get-environments)
* [[!UICONTROL Obter Tipos de Tráfego]](#get-traffic-types)
* [[!UICONTROL Obter Espaços de Trabalho]](#get-workspaces)
* [[!UICONTROL Listar definições divididas em um ambiente]](#list-split-definitions-in-an-environment)
* [[!UICONTROL Listar Divisões]](#list-splits)

#### [!UICONTROL Obter ambientes]

Este módulo de pesquisa recupera uma lista de ambientes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém os ambientes que deseja listar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter Tipos de Tráfego]

Este módulo de pesquisa recupera uma lista de tipos de tráfego.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém os tipos de tráfego que deseja listar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter Espaços de Trabalho]

Este módulo de pesquisa recupera os espaços de trabalho de uma organização.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de espaços de trabalho que você deseja que o módulo recupere durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar definições divididas em um ambiente]

Este módulo de pesquisa recupera uma lista de definições de divisão em um determinado ambiente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém as definições de divisão que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome ou ID de Ambiente]</td> 
   <td>Selecione ou mapeie o ambiente que contém as definições de divisão que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de definições de divisão que você deseja que o módulo recupere durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar Divisões]

Este módulo de pesquisa recupera uma lista de divisões.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Split.io] ao Workfront Fusion, consulte <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Split.io] ao [!UICONTROL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie o espaço de trabalho que contém as divisões que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de divisões que você deseja que o módulo recupere durante cada ciclo de execução do cenário.</td> 
  </tr> 
 </tbody> 
</table>
