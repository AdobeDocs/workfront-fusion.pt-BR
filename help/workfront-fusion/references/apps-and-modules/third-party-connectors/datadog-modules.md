---
title: Módulos do Datadog
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam Datadog, bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# [!DNL Datadog] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Datadog], bem como conectá-los a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!DNL Datadog], você deve ter uma conta [!DNL Datadog].

## Informações da API Datadog

O conector Datadog usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>1.0.11</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!DNL Datadog] a [!DNL Workfront Fusion] {#connect-datadog-to-workfront-fusion}

### Recuperar a chave de API e a chave de aplicativo {#retrieve-your-api-key-and-application-key}

Para conectar sua conta do [!DNL Datadog] ao [!DNL Workfront Fusion], você precisa recuperar uma Chave de API e uma chave de aplicativo da sua conta do [!DNL Datadog].

1. Faça logon em sua conta do [!DNL Datadog].
1. No painel de navegação esquerdo, clique em **[!UICONTROL Integrations]** e em **[!UICONTROL APIs]**.
1. Na tela principal, clique em **[!UICONTROL API Keys]**.
1. Passe o mouse sobre a barra roxa para revelar a chave de API.
1. Copie a chave da API para um local seguro.
1. Na tela principal, clique em **[!UICONTROL Application Keys]**.
1. Passe o mouse sobre a barra roxa para revelar a chave do aplicativo.
1. Copie a chave do aplicativo para um local seguro.

### Criar uma conexão com [!DNL Datadog] em [!DNL Workfront Fusion]

Você pode criar uma conexão com sua conta do [!DNL Datadog] diretamente de dentro de um módulo do [!UICONTROL Datadog].

1. Em qualquer módulo [!UICONTROL Datadog], clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. Preencha os campos do módulo da seguinte maneira:

<table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection Type]</td> 
      <td> <p> Selecione a opção [!UICONTROL [!DNL Datadog] Aplicativo] para obter acesso total à API [!DNL Datadog].</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection Name]</td> 
      <td> <p> Insira um nome para a conexão.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Domain] </td> 
      <td> <p>Selecione o domínio ao qual deseja se conectar (EUA ou UE).</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td> <p> Insira sua chave de API [!DNL Datadog]. </p> <p>Para obter instruções sobre como recuperar a chave de API, consulte <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Recuperar a chave de API e a chave do aplicativo</a> neste artigo.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Application Key]</td> 
      <td> <p> Insira sua chave do aplicativo [!DNL Datadog]. </p> <p>Para obter instruções sobre como recuperar a chave do aplicativo, consulte <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Recuperar a chave da API e a chave do aplicativo</a> neste artigo.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

## [!DNL Datadog] módulos e seus campos

Ao configurar módulos do [!DNL Datadog], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Datadog] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Ações

* [[!UICONTROL Post Timeseries Points]](#post-timeseries-points)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Post Timeseries Points]

O módulo permite publicar dados de série temporal que podem ser mostrados em gráfico nos painéis de [!DNL Datadog].

O limite para payloads compactados é de 3,2 megabytes (3200000) e 62 megabytes (62914560) para payloads descompactados.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Datadog] ao [!DNL Workfront Fusion], consulte <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Datadog] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Series]</td> 
   <td> <p>Adicione as séries de tempo que você deseja enviar para [!DNL Datadog].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Metric]</strong> </p> <p>Insira o nome da série temporal.</p> </li> 
     <li> <p><strong>[!UICONTROL Type]</strong> </p> <p>Selecione o tipo de métrica.</p> </li> 
     <li> <p><strong>[!UICONTROL Interval]</strong> </p> <p> Se o tipo da métrica for taxa ou contagem, defina o intervalo correspondente.</p> </li> 
     <li> <p><strong>[!UICONTROL Points]</strong> </p> <p>Adicionar pontos relacionados a uma métrica.</p> <p>Esta é uma matriz de pontos JSON. Cada ponto tem o formato: <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>Nota:  <p>O carimbo de data/hora deve estar em segundos.</p> <p>O carimbo de data/hora deve ser atual. O valor atual é definido como não mais de 10 minutos no futuro ou mais de 1 hora no passado.</p> <p> O formato do valor numérico deve ser um valor flutuante.</p> </p> <p>Este campo deve conter pelo menos 1 item.</p> </li> 
     <li> <p><strong>[!UICONTROL Host]</strong> </p> <p>Informe o nome do host que produziu a métrica.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Esse módulo de ação permite executar uma chamada de API personalizada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Datadog] ao [!DNL Workfront Fusion], consulte <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Datadog] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://api.datadoghq.com/api/</code>. Exemplo:<code> /v1/org</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
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
 </tbody> 
</table>

**Exemplo:** a chamada de API a seguir retorna todos os painéis na sua conta [!DNL Datadog]:

URL: `/v1/dashboard`

Método: `GET`

![Exemplo de chamada à API Datadog](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-example.png)

O resultado pode ser encontrado na Saída do módulo em Pacote > Corpo > painéis.

No nosso exemplo, 3 painéis foram retornados:

![Resposta da API Datadog](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-response-example.png)
