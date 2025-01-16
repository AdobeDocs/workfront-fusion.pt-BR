---
title: Módulos do DocuSign
description: Os  [!DNL Adobe Workfront Fusion DocuSign] módulos permitem que você monitore e recupere o status do envelope, pesquise e recupere envelopes, ou baixe e envie um documento para entrar em sua  [!DNL DocuSign] conta.
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1632'
ht-degree: 0%

---

# Módulos do DocuSign

Os módulos do [!DNL Adobe Workfront Fusion] [!DNL DocuSign] permitem que você monitore e recupere o status dos envelopes, pesquise e recupere envelopes, ou baixe e envie um documento para entrar em sua conta do [!DNL DocuSign].

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

Para usar módulos [!DNL DocuSign], você deve ter uma conta [!DNL DocuSign].

## Informações da API do DocuSign

O conector DocuSign usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!DNL DocuSign] a [!DNL Workfront Fusion] {#connect-docusign-to-workfront-fusion}

Para criar uma conexão para seus módulos do [!DNL DocuSign]:

1. Clique em **[!UICONTROL Add]** ao lado da caixa [!UICONTROL Connection] quando você começar a configurar o primeiro módulo [!DNL DocuSign].
1. Insira o seguinte:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Digite um nome para a nova conexão [!DNL DocuSign]</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>Selecione se a conta à qual deseja se conectar é uma conta de produção ou uma conta de demonstração.</td> 
     </tr> 
    </tbody> 
   </table>

1. Continue conforme descrito em [Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md#connect).

## [!DNL DocuSign] módulos e seus campos

Ao configurar módulos do [!DNL DocuSign], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL DocuSign] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Ações](#actions)

### Triggers

#### [!UICONTROL Watch envelopes]

Esse módulo de acionamento inicia um cenário quando um envelope é enviado, entregue, assinado, concluído ou recusado.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecione a conta que contém os registros que você deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p> Selecione o tipo de evento que deseja assistir.</p> 
    <ul> 
     <li>[!UICONTROL Document completed]</li> 
     <li>[!UICONTROL Document declined]</li> 
     <li>[!UICONTROL Document sent]</li> 
     <li>[!UICONTROL Document signed]</li> 
     <li>[!UICONTROL New document in Inbox]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Output fields]</p> </td> 
   <td> <p>Selecione os campos que deseja incluir na saída do módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de registros com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download a document]](#download-a-document)
* [[!UICONTROL Read an envelope]](#read-an-envelope)
* [[!UICONTROL Upload a file to an envelope]](#upload-a-file-to-an-envelope)
* [[!UICONTROL Create a new envelope]](#create-a-new-envelope)
* [[!UICONTROL Add Recipient to Envelope]](#add-recipient-to-envelope)
* [[!UICONTROL Add custom field]](#add-custom-field)
* [[!UICONTROL Modify custom field]](#modify-custom-field)
* [[!UICONTROL Send envelope]](#send-envelope)

#### [!UICONTROL Custom API Call]

Esse módulo de ação permite executar uma chamada de API personalizada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao [!DNL Workfront Fusion], consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Account]</td> 
   <td>Insira ou mapeie a conta que deseja usar para acessar a API [!DNL DocuSign].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Digite o endereço no servidor Web com o qual você deseja que o módulo interaja.</p> <p>Você pode digitar uma URL relativa, o que significa que não é necessário incluir o protocolo (como <code>http://</code>) no início. Isso sugere ao servidor Web que a interação está ocorrendo no servidor.</p> <p>Por exemplo: <code>[!DNL /api/conversations].create</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Isso determina o tipo de conteúdo da solicitação.</p> <p>Por exemplo,<code> {"Content-type":"application/json"}</code></p> <p>Observação: se você estiver recebendo erros e for difícil determinar sua origem, considere modificar cabeçalhos com base na documentação [!DNL Workfront]. Se sua chamada de API personalizada retornar um erro de solicitação HTTP 422, tente usar um cabeçalho "Content-Type":"text/plain".</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de resultados com os quais trabalhar durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemplo:** Envelopes de Lista
>
>A chamada de API a seguir retorna envelopes a partir da data especificada em sua conta [!DNL DocuSign]:
>
>**URL**: `/v2.1/accounts/{accountId}/envelopes/`
>
>**Método**: `GET`
>
>**Cadeia de Caracteres de Consulta**:
>
>* **Chave**: `from_date`
>
>* **Valor**: `YYYY-MM-DD`
>
>Especifica quando a solicitação começa a verificar alterações de status para envelopes na conta.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)
>
>O resultado pode ser encontrado na Saída do módulo em Pacote > Corpo > envelopes.
>
>No nosso exemplo, 6 envelopes foram retornados:
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

#### [!UICONTROL Download a document]

Este módulo de ação baixa um único documento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao [!DNL Workfront Fusion], consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecione a conta que contém o documento que você deseja baixar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Insira ou mapeie a ID do envelope que deseja baixar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Document ID]</p> </td> 
   <td> <p>Insira ou mapeie a ID do documento que deseja baixar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Certificate]</td> 
   <td>Selecione <strong>[!UICONTROL Yes]</strong> se quiser incluir o certificado de assinatura de envelope no download.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents by User ID]</td> 
   <td>Selecione <strong>[!UICONTROL Yes]</strong> se você deseja permitir que os destinatários recuperem documentos por ID de usuário. Por exemplo, se um usuário estiver incluído em duas ordens de roteiro diferentes com visibilidades diferentes, o uso dessa opção retornará todos os documentos de ambos os roteiros.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encrypt]</td> 
   <td>Selecione <strong>[!UICONTROL Yes]</strong> se quiser que os bytes de PDF retornados na resposta sejam criptografados para todos os gerenciadores de chaves configurados em sua conta [!DNL DocuSign].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Selecione o idioma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Changes]</td> 
   <td>Quando definido como <strong>[!UICONTROL Yes]</strong>, quaisquer campos alterados para o PDF retornado são realçados em amarelo e as assinaturas ou iniciais opcionais são contornadas em vermelho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watermark]</td> 
   <td> <p>Selecione <strong>[!UICONTROL No]</strong> para remover a marca d'água dos documentos do PDF.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read an envelope]

Este módulo de ação lê informações sobre um envelope em [!DNL DocuSign] usando a ID de envelope.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao [!DNL Workfront Fusion], consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecione a conta que contém o documento do qual deseja ler informações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Insira ou mapeie a ID que contém o documento do qual você deseja ler as informações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file to an envelope]

Este módulo carrega um arquivo especificado em um envelope existente no DocuSign.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao [!DNL Workfront Fusion], consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecione a conta que contém o envelope no qual você deseja carregar um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Insira ou mapeie a ID do envelope no qual deseja fazer upload de um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou insira o nome e os dados do arquivo de origem.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a new envelope]

Este módulo de ação cria um novo envelope a partir de um modelo. Ele retorna a ID do novo envelope, bem como o status do novo envelope.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td>

<td> <p>Para obter instruções sobre como conectar sua conta do DocuSign ao Workfront Fusion, consulte os artigos em <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Account] </td>
   <td> <p>Selecione a conta que contém o envelope no qual você deseja carregar um arquivo.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template]</td>
   <td> <p> Selecione o modelo a partir do qual deseja criar o novo envelope. Os modelos estão disponíveis com base no [!UICONTROL Account] selecionado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL After creation]
   </td> 
   <td> <p>Selecione se deseja salvar o envelope como rascunho ou enviá-lo para assinatura.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template recipients]</td>
    <td>Selecionar o destinatário deste envelope</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Recipient to Envelope]

Este módulo de ação adiciona um ou mais destinatários a um envelope existente. Se o envelope já tiver sido enviado, o recipient receberá um email. Este módulo não é válido para envelopes que já foram concluídos.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta do DocuSign ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Account] </td>
   <td> <p>Selecione a conta que contém o envelope no qual deseja adicionar recipients.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>Selecione ou mapeie a ID do envelope ao qual deseja adicionar o recipient.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Recipient type]</td>
   <td> <p> Selecione o tipo de destinatário que deseja adicionar ao envelope.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon copy]</p> </li> 
     <li> <p>[!UICONTROL Certified delivery]</p> </li> 
     <li> <p>[!UICONTROL In-person signer]</p> </li> 
     <li> <p>[!UICONTROL Intermediary]</p> </li> 
     <li> <p>[!UICONTROL Signer]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>Insira ou mapeie o endereço de email do destinatário que deseja adicionar ao envelope.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Name]</td>
   <td>Insira ou mapeie o nome do destinatário que deseja adicionar ao envelope.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Routing order]</td>
   <td> <p>Insira ou mapeie o número do roteamento do recipient. O número do banco determina a ordem na qual os destinatários recebem e assinam seus documentos.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Email body]</td>
   <td>Insira ou mapeie o corpo (conteúdo) do email que é enviado ao destinatário.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Email subject]</td>
   <td>Insira ou mapeie o assunto do email enviado ao recipient.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private message]</td>
   <td> <li> <p>Somente o recipient selecionado vê a mensagem privada, bem como a mensagem geral. A mensagem privada é limitada a 1000 caracteres.</p> </li> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Authentication]</td> 
   <td> <p>Selecione o método de autenticação que deseja usar para confirmar a identidade do recipient.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL None]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Access code]</strong> </p> <p>Insira ou mapeie o código de acesso.</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>Insira ou mapeie o número de telefone</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>Insira ou mapeie o número de telefone</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add custom field]

Este módulo de ação adiciona um campo personalizado ao documento

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao [!DNL Workfront Fusion], consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecione a conta que contém o documento ao qual você deseja adicionar um campo personalizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Insira ou mapeie a ID do envelope que contém o documento ao qual você deseja adicionar um campo personalizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Insira ou mapeie um nome para o novo campo que deseja adicionar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Ative essa opção se desejar que o campo adicionado seja um campo obrigatório.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Ative essa opção se desejar que o campo fique visível.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Insira ou mapeie o valor (conteúdo) do campo adicionado. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify custom field]

Esse módulo de ação modifica um campo personalizado usando o nome do campo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao [!DNL Workfront Fusion], consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecione a conta que contém o documento no qual você deseja modificar um campo personalizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Insira ou mapeie a ID do envelope que contém o documento no qual você deseja modificar um campo personalizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field ID]</td> 
   <td>Insira ou mapeie a ID do campo que você deseja modificar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Insira ou mapeie o nome do campo que você deseja modificar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Habilite essa opção se desejar que o campo modificado seja obrigatório.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Ative essa opção se desejar que o campo fique visível.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Insira ou mapeie o valor (conteúdo) do campo modificado. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send envelope]

Esse módulo de ação envia um envelope de rascunho para seus recipients.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao [!DNL Workfront Fusion], consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecione a conta que contém o envelope de rascunho que você deseja enviar aos recipients.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Insira ou mapeie a ID do envelope de rascunho que você deseja enviar aos recipients.</p> </td> 
  </tr> 
 </tbody> 
</table>
