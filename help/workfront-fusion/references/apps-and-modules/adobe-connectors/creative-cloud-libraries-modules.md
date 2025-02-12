---
title: Módulos de bibliotecas do Adobe Creative Cloud
description: Com os módulos  [!DNL Adobe Workfront Fusion Adobe Creative Cloud] Bibliotecas, você pode iniciar um cenário quando um elemento ou biblioteca for criado ou atualizado. Você também pode carregar, recuperar, arquivar ou listar elementos ou fazer uma chamada para a API  [!DNL Adobe Creative Cloud Libraries] .
author: Becky
feature: Workfront Fusion
exl-id: 85607e4e-538a-427f-8a99-a0ab65a75ac2
source-git-commit: fedf8f3f4031faaad9f81ed38fbc77e40e3a85b6
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Módulos de bibliotecas da Adobe Creative Cloud

Com os módulos [!DNL Adobe Workfront Fusion] [!DNL Adobe Creative Cloud Libraries], é possível iniciar um cenário quando um elemento ou biblioteca é criado ou atualizado. Você também pode carregar, recuperar, arquivar ou listar elementos, ou fazer uma chamada para a API [!DNL Adobe Creative Cloud Libraries].

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.

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

Para usar módulos [!DNL Adobe Creative Cloud Libraries], você deve ter uma conta [!UICONTROL Adobe Creative Cloud].

## Informações da API de bibliotecas do Adobe Creative Cloud

O conector de bibliotecas Adobe Creative Cloud usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://cc-libraries.adobe.io/api/v1</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.1.7</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Adobe Creative Cloud Libraries] módulos e seus campos

Ao configurar módulos do [!UICONTROL Adobe Creative Cloud Libraries], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Creative Cloud Libraries] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Elementos](#elements)

* [Bibliotecas](#libraries)

* [Outro](#other)


### Elementos

* [[!UICONTROL Archive an Element]](#archive-an-element)

* [[!UICONTROL Get an Element]](#get-an-element)

* [[!UICONTROL List Elements]](#list-elements)

* [[!UICONTROL Upload an Element]](#upload-an-element)

* [!UICONTROL [Observar novo elemento na biblioteca]](#watch-new-element-in-library)

* [[!UICONTROL Watch Updated Elements]](#watch-updated-elements)


#### [!UICONTROL Archive an Element]

Este módulo de ação arquiva um elemento de uma biblioteca.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Selecione uma conexão existente com o Creative Cloud Libraries. No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Selecione ou mapeie a biblioteca que contém o elemento que você deseja arquivar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element ID]</td>
      <td>Selecione ou mapeie o elemento que deseja arquivar.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an Element]

Esse módulo de ação retorna um único elemento de uma biblioteca.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Selecione uma conexão existente com o Creative Cloud Libraries. No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td>Selecione ou mapeie a biblioteca que contém o elemento que você deseja recuperar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element ID]</td>
      <td>Insira ou mapeie a ID do elemento que você deseja recuperar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>Selecione o tipo de informação que o módulo retorna. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Default]</b>
            </p>
            <p>Dados base</p>
          </li>
          <li>
            <p><b>[!UICONTROL Details]</b>
            </p>
            <p>Todos os dados disponíveis</p>
          </li>
          <li>
            <p><b>[!UICONTROL Representations]</b>
            </p>
            <p>Uma lista nivelada de ativos associados ao elemento de biblioteca</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Elements]

Este módulo de ação recupera uma lista de elementos em uma biblioteca.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Selecione uma conexão existente com o Creative Cloud Libraries. No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Selecione ou mapeie a biblioteca da qual deseja listar elementos.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Order by]</td>
      <td>Selecione se deseja ordenar os resultados por nome ou pela última data em que o elemento foi modificado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type]</td>
      <td >Insira ou mapeie um tipo MIME para limitar os resultados aos elementos identificados com o tipo MIME especificado. Exemplo: <code>string</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>Selecione o tipo de informação que o módulo retorna. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Default]</b>
            </p>
            <p>Dados base</p>
          </li>
          <li>
            <p><b>[!UICONTROL Details]</b>
            </p>
            <p>Todos os dados disponíveis</p>
          </li>
          <li>
            <p><b>[!UICONTROL Representations]</b>
            </p>
            <p>Uma lista nivelada de ativos associados ao elemento de biblioteca</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch New Element in Library]

Esse módulo de acionamento inicia um cenário quando um elemento é adicionado a uma biblioteca.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Selecione uma conexão existente com o Creative Cloud Libraries. No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Selecione a biblioteca que deseja observar por elementos atualizados.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Watch Updated Elements]

Esse módulo de acionamento inicia um cenário quando um elemento em uma biblioteca é atualizado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Selecione uma conexão existente com o Creative Cloud Libraries. No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Selecione a biblioteca que deseja observar para novos elementos.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>

### Bibliotecas

* [[!UICONTROL Watch New Libraries]](#watch-new-libraries)

* [[!UICONTROL Watch Updated Libraries]](#watch-updated-libraries)


#### [!UICONTROL Watch New Libraries]

Esse módulo de acionamento inicia um cenário quando uma nova biblioteca é criada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Selecione uma conexão existente com o Creative Cloud Libraries. No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch Updated Libraries]

Esse módulo de acionamento inicia um cenário quando uma biblioteca existente é atualizada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Selecione uma conexão existente com o Creative Cloud Libraries. No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>

### Outro

* [Fazer uma chamada de API](#make-an-api-call)
* [Fazer upload de um ativo](#upload-an-asset)

#### [!UICONTROL Make an API Call]

Este módulo faz uma chamada de API personalizada para a API [!DNL Adobe Creative Cloud Libraries].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Creative Cloud ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas.</a></p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Insira um caminho relativo para <code>https://cc-libraries.adobe.io/api</code>.</p>
    <p>Por exemplo <code>/v1/libraries</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL API version]</td>
      <td>
        <p>Selecione a versão da API [!DNL Adobe Analytics] à qual você deseja se conectar.</p>
      </td>
    </tr>    <tr>
      <td role="rowheader">[!UICONTROL Method]</td>
      <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]</td>
      <td>
        <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p>
        <p>Por exemplo: <code>{"name":"something-urgent"}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
       <tr>
      <td role="rowheader">[!UICONTROL Upload a transient document]</td>
      <td>
      <p>Para fazer upload de um documento transitório, informe o arquivo de origem do documento que deseja fazer upload.</p>
      <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p>
    </td>
    </tr>
</tbody>
</table>


#### [!UICONTROL Upload an Asset]

Esse módulo de ação faz upload de um pequeno ativo de arquivo para uma biblioteca existente. O tamanho máximo do arquivo é 1 GB.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Selecione uma conexão existente com o Creative Cloud Libraries. No momento, a criação de conexão não está disponível no conector do Creative Cloud Libraries. As conexões existentes funcionam conforme esperado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Selecione a biblioteca na qual você deseja fazer upload de um ativo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Invocation Mode]</td>
      <td>
        <p>Selecione o modo de processamento com o qual chamar este processo de solicitação.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL sync]</b>
            </p>
            <p>A chamada à API é processada de forma síncrona. A resposta é entregue quando o processamento é concluído (a menos que a chamada atinja o tempo limite.)</p>
          </li>
          <li>
            <p><b>[!UICONTROL async]</b>
            </p>
            <p>A resposta do monitor assíncrono é retornada imediatamente e o processamento de solicitações ocorre de forma assíncrona. A chamada é responsável por sondar o endpoint até a conclusão.</p>
          </li>
          <li>
            <p><b>[!UICONTROL sync,async]</b> (Padrão)</p>
            <p>Tentativa de processamento síncrono da solicitação. Quando o processamento se estende além de 5000 ms, a resposta do monitor assíncrono é retornada. O URL do monitor deve ser sondado até que a solicitação seja concluída.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element Type]</td>
      <td >Selecione o tipo de elemento que você deseja carregar</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File Type]</td>
      <td >Insira ou mapeie o tipo MIME do arquivo carregado.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source File]</td>
      <td>
        <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p>
      </td>
    </tr>
  </tbody>
</table>





