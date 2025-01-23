---
title: HTTP &gt; Fazer uma solicitação de autorização de chave de API
description: Este módulo de ação  [!DNL Adobe Workfront Fusion]  envia uma solicitação HTTPS para uma URL especificada que requer uma autorização de Autenticação de Chave de API e processa a resposta.
author: Becky
feature: Workfront Fusion
exl-id: 362b80b5-42f4-4b82-b06c-39c7c5a1eb1a
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# HTTP > [!UICONTROL Make an API Key Authorization request]

>[!NOTE]
>
>O [!DNL Adobe Workfront Fusion] exige uma licença do [!DNL Adobe Workfront Fusion] além de uma licença do Adobe Workfront.

Este módulo de ação [!DNL Adobe Workfront Fusion] envia uma solicitação HTTPS para uma URL especificada que requer uma autorização de Autenticação de Chave de API e processa a resposta.

>[!NOTE]
>
>Se você estiver se conectando a um produto Adobe que não tem um conector dedicado no momento, recomendamos o uso do módulo Adobe Authenticator.
>
>Para obter mais informações, consulte [módulo Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

Para obter informações sobre [!UICONTROL Adobe Workfront Fusion] licenças, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Configuração do módulo [!UICONTROL HTTP] >[!UICONTROL Make an API Key Authorization request]

Ao configurar o módulo [!UICONTROL HTTP] >[!UICONTROL Make an API Key Authorization request], o [!DNL Adobe Workfront Fusion] exibe os campos listados abaixo. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Credentials]</td> 
   <td> <p>Selecione a chave que contém suas credenciais de autenticação de Chave de API. Para adicionar uma nova chave, clique em <strong>[!UICONTROL Add]</strong> e configure as seguintes informações:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key name]</strong></p> <p>Insira um nome para este conjunto de credenciais de API.</p> </li> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Insira a chave da API.</p> </li> 
     <li> <p><strong>[!UICONTROL API Key placement]</strong> </p> <p>Selecione se deseja colocar a chave de API no cabeçalho ou no query da chamada de API.</p> </li> 
     <li> <p><strong>[!UICONTROL API Key parameter name]</strong> </p> <p>Insira o nome pelo qual a chamada de API identifica a chave da API, como "apiKey" ou "X-API-Key". Você pode encontrar essas informações na documentação do serviço Web ao qual o módulo está se conectando.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx)] </td> 
   <td> <p>Use esta opção para configurar o tratamento de erros.</p> <p>Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Tratamento de erros no Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Insira o URL para o qual você deseja enviar uma solicitação, como um endpoint de API, site etc.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Por exemplo, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Insira os pares de valor-chave da consulta desejados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>O Corpo HTTP são os bytes de dados transmitidos em uma mensagem de transação HTTP imediatamente após os cabeçalhos, se houver algum a ser usado.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>O tipo de corpo bruto geralmente é adequado para a maioria das solicitações de corpo HTTP, mesmo em situações em que a documentação do desenvolvedor não especifica os dados a serem enviados.</p> <p>Especifique um formulário de análise de dados no campo [!UICONTROL Content type].</p> <p>Apesar do tipo de conteúdo selecionado, o módulo insere dados em qualquer formato estipulado ou exigido pela documentação do desenvolvedor.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>Este tipo de corpo é para dados [!UICONTROL POST] usando <code>application/x-www-form-urlencoded</code>.</p> <p>Para <code>[!UICONTROL application/x-www-form-urlencoded]</code>, o corpo da mensagem HTTP enviada ao servidor é essencialmente uma cadeia de caracteres de consulta. As chaves e os valores são codificados em pares de valores chave separados por <code>&amp;</code> e por um <code>=</code> entre a chave e o valor. </p> <p>Para dados binários, use <code>[!UICONTROL multipart/form-data]</code>.</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>Exemplo: </b></span></span> 
       <p>Exemplo do formato de solicitação HTTP resultante:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>O [!UICONTROL Multipart/form-data] é uma solicitação HTTP de várias partes usada para enviar arquivos e dados. Normalmente, é usado para carregar arquivos no servidor.</p> <p>Adicione campos a serem enviados na solicitação. Cada campo deve conter um par de valor-chave.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>Informe a chave e o valor a serem enviados dentro do corpo da solicitação.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Informe a chave e especifique o arquivo de origem que deseja enviar no corpo da solicitação.</p> <p>Mapeie o arquivo que você deseja carregar do módulo anterior (como [!UICONTROL HTTP] &gt;[!UICONTROL Get a File] ou [!UICONTROL Google Drive] &gt;[!UICONTROL Download a File)] ou insira o nome do arquivo e os dados do arquivo manualmente.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Habilite esta opção para analisar respostas automaticamente e converter respostas JSON e XML para que você não precise usar os módulos [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON] ou [!UICONTROL XML] &gt; [!UICONTROL Parse XML].</p> <p>Antes de usar o conteúdo JSON ou XML analisado, execute o módulo uma vez manualmente para que o módulo possa reconhecer o conteúdo da resposta e permitir que você o mapeie em módulos subsequentes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>Especifique o tempo limite da solicitação em segundos (1-300). O padrão é 40 segundos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> Habilite essa opção para compartilhar cookies do servidor com todos os módulos HTTP em seu cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p> Faça upload do seu certificado se quiser usar o TLS usando seu certificado autoassinado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>Habilite esta opção para rejeitar conexões que estejam usando certificados TLS não verificados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> Ative essa opção para seguir os redirecionamentos de URL com respostas 3xx.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>Ative essa opção para seguir os redirecionamentos de URL com todos os códigos de resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>Por padrão, [!DNL Workfront Fusion] manipula vários valores para a mesma chave de parâmetro da cadeia de caracteres de consulta da URL que as matrizes. Por exemplo, <code>www.test.com?foo=bar&amp;foo=baz</code> será convertido em <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Ative esta opção para desativar este recurso. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> Habilite esta opção para solicitar uma versão compactada do site.</p> <p>Adiciona um cabeçalho <code>[!UICONTROL Accept-Encoding]</code> para solicitar conteúdo compactado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>Habilite esta opção para usar o TLS mútuo na solicitação HTTP.</p> <p>Para obter mais informações sobre TLS Mútuo, consulte <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">Usar TLS Mútuo em módulos HTTP em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
