---
title: Módulos do Datadog
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam Datadog, bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
source-git-commit: 8a4e54a4c1783e4bc679778c6fcf21dcb4d3d537
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 1%

---

# [!DNL Datadog] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Datadog], bem como conectá-los a vários aplicativos e serviços de terceiros.

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
1. No painel de navegação esquerdo, clique em **[!UICONTROL Integrações]** e em **[!UICONTROL APIs]**.
1. Na tela principal, clique em **[!UICONTROL Chaves de API]**.
1. Passe o mouse sobre a barra roxa para revelar a chave de API.
1. Copie a chave da API para um local seguro.
1. Na tela principal, clique em **[!UICONTROL Chaves do Aplicativo]**.
1. Passe o mouse sobre a barra roxa para revelar a chave do aplicativo.
1. Copie a chave do aplicativo para um local seguro.

### Criar uma conexão com [!DNL Datadog] em [!DNL Workfront Fusion]

Você pode criar uma conexão com sua conta [!DNL Datadog] diretamente de dentro de um módulo [!UICONTROL Datadog].

1. Em qualquer módulo [!UICONTROL Datadog], clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. Preencha os campos do módulo da seguinte maneira:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Nome da Conexão]</td> 
      <td> <p> Insira um nome para a conexão.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Selecione se essa conexão é para um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Domínio] </td> 
      <td> <p>Selecione o domínio ao qual deseja se conectar (EUA ou UE).</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Localização da Chave de API] </td> 
      <td> <p>Selecione se deseja incluir a chave de API no cabeçalho ou na sequência de consulta.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Chave de API]</td> 
      <td> <p> Insira sua chave de API [!DNL Datadog]. </p> <p>Para obter instruções sobre como recuperar a chave de API, consulte <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Recuperar a chave de API e a chave do aplicativo</a> neste artigo.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## [!DNL Datadog] módulos e seus campos

Ao configurar módulos do [!DNL Datadog], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Datadog] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Ações

* [[!UICONTROL Fazer uma chamada de API]](#make-an-api-call)
* [[!UICONTROL Postar Pontos da Série Temporal]](#post-timeseries-points)

#### [!UICONTROL Fazer uma chamada de API]

Esse módulo de ação permite executar uma chamada de API personalizada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Datadog] ao [!DNL Workfront Fusion], consulte <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Datadog] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Usar Domínio Dedicado]</td> 
   <td>Alguns dos endpoints da API do Datadog que esperam muito tráfego de entrada estão em execução em seus domínios dedicados. Marque esta caixa para usar o domínio dedicado para sua chamada de API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://api.datadoghq.com/api/</code>. Exemplo:<code> /v1/org</code>.</td> 
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

#### [!UICONTROL Postar Pontos da Série Temporal]

O módulo permite publicar dados de série temporal que podem ser mostrados em gráfico nos painéis de [!DNL Datadog].

O limite para payloads compactados é de 3,2 megabytes (3200000) e 62 megabytes (62914560) para payloads descompactados.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Datadog] ao [!DNL Workfront Fusion], consulte <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Datadog] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td> Selecione o tipo de métrica que deseja usar. 
   <ul>
   <li>Medidor</li>
   <li>Taxa</li>
   <li>Contagem</li>
   </ul>
   </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intervalo]</td> 
   <td> Se o tipo da métrica for taxa ou contagem, defina o intervalo correspondente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pontos]</td> 
   <td><p>Adicionar pontos relacionados a uma métrica.</p> <p>Esta é uma matriz de pontos JSON. Cada ponto tem o formato: <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>Nota:  <p>O carimbo de data/hora deve estar em segundos.</p> <p>O carimbo de data/hora deve ser atual. O valor atual é definido como não mais de 10 minutos no futuro ou mais de 1 hora no passado.</p> <p> O formato do valor numérico deve ser um valor flutuante.</p> </p> <p>Este campo deve conter pelo menos 1 item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Host]</td> 
   <td>Informe o nome do host que produziu a métrica. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Marcas]</td> 
   <td> Para cada marca que você deseja adicionar à métrica, clique em <b>Adicionar item</b> e insira o valor da marca.</td> 
  </tr> 
 </tbody> 
</table>
