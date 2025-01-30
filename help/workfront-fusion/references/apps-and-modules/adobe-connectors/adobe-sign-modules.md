---
title: Módulos do Adobe Acrobat Sign
description: Com os  [!DNL Adobe Acrobat Sign] módulos, você pode iniciar um [!DNL Adobe Workfront Fusion] cenário com base nos eventos da sua [!DNL Adobe] conta da Acrobat Sign, criar, ler ou atualizar contratos e outros registros, pesquisar registros usando os critérios que você definiu e carregar documentos.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0ef9d40e-8ad6-434e-8fa0-076920ff29ea
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '5501'
ht-degree: 0%

---

# [!DNL Adobe Acrobat Sign] módulos

Com os módulos do [!DNL Adobe Acrobat Sign], você pode iniciar um cenário do [!DNL Adobe Workfront Fusion] com base em eventos na sua conta do [!DNL Adobe Acrobat Sign], criar, ler ou atualizar contratos e outros registros, pesquisar registros usando os critérios que você definiu e carregar documentos.

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

## Informações da API [!DNL Adobe Acrobat Sign]

O conector do Adobe Acrobat Sign usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v6 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.35.1</td> 
  </tr>
 </tbody> 
</table>


## Recomendações de uso do conector [!DNL Adobe Acrobat Sign]

O aplicativo [!DNL Adobe Sign] torna a automatização de processos de negócios de assinatura eletrônica no [!DNL Fusion] muito mais fácil e eficiente.

Os novos usuários do [!DNL Adobe Sign] devem estar muito atentos a algumas restrições de atualização de contratos. Normalmente, os contratos não são alterados depois de iniciados. Recomendamos que os novos usuários do [!DNL Adobe Sign] se concentrem na criação de novos contratos usando o módulo de criação de contratos. Isso tornará as automações do [!DNL Fusion] mais fáceis e funcionará melhor com o [!DNL Adobe Sign].

[!DNL Adobe Sign] contratos precisam de um campo para funcionar. Há algumas opções para fazer isso, mas a mais fácil e comum é carregar um documento transitório e mapeá-lo para o seu contrato.

![recomendações do Adobe Sign](/help/workfront-fusion/references/apps-and-modules/assets/adobe-sign-recommendations-350x168.png)

## [!DNL Adobe Acrobat Sign] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Acrobat Sign], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Acrobat Sign] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

<!--
* [Watch for agreements](#watch-for-agreements) 
* [Watch for events](#watch-for-events)
-->

+++ **[!UICONTROL Watch for agreements]**

Este módulo de acionador inicia um cenário quando um contrato é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Selecione se deseja observar novos registros, registros atualizados ou ambos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type] </td> 
   <td>Selecione o tipo de registro que você deseja que o registro assista.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Find text]</td> 
   <td> <p>Insira os termos que você deseja pesquisar. O módulo retorna registros que incluem esses termos como valores de campo.</p> <p>Para obter mais informações sobre a pesquisa de campos no [!DNL Adobe Acrobat Sign], consulte "Como funciona a pesquisa de texto" no <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">Adobe Sign Search - Como funciona</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned agreements]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch for events]**

Esse módulo de acionador inicia um cenário quando ocorre um evento selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td>Selecione o webhook que deseja usar ou clique em <b>[!UICONTROL Add]</b> e preencha os campos a seguir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p>Insira um nome para o webhook</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scopes]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Account]</p> </li> 
     <li> <p>[!UICONTROL Group]</p> </li> 
     <li> <p>[!UICONTROL User]</p> </li> 
     <li> <p>[!UICONTROL Resource]</p> <p>Se você selecionar [!UICONTROL Resource], insira a ID do recurso e o tipo de recurso.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource level]</td> 
   <td> <p>Selecione o tipo de recurso que deseja observar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agreements]</p> </li> 
     <li> <p>[!UICONTROL Widgets]</p> </li> 
     <li> <p>[!UICONTROL Megasigns]</p> </li> 
     <li> <p>[!UICONTROL Library Documents]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook subscription events]</td> 
   <td>Selecione os [!DNL Adobe Sign] eventos que você deseja que o módulo assista.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application display name]</td> 
   <td>O nome de exibição do aplicativo através do qual o webhook é criado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application name]</td> 
   <td>O nome de exibição do aplicativo através do qual o webhook é criado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Problem notification emails]</td> 
   <td> <p>Essa configuração funciona somente para contas de administrador</p> <p>Para cada endereço de email para o qual deseja enviar emails de notificação de problemas, clique em <b>[!UICONTROL Add]</b> e insira o endereço de email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement conditional parameters]</td> 
   <td>Se quiser adicionar parâmetros condicionais, selecione <b>[!UICONTROL Yes]</b> no tipo de registro ao qual deseja adicionar parâmetros e selecione <b>[!UICONTROL Yes]</b> em qualquer parâmetro que desejar habilitar.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Ações

<!--
* [Create a record](#create-a-record) 
* [Create an agreement](#create-an-agreement) 
* [Create related records](#create-related-records) 
* [Custom API Call](#custom-api-call) 
* [List records](#list-records) 
* [Read a record](#read-a-record) 
* [Read related records](#read-related-records) 
* [Update a record](#update-a-record) 
* [Update related record](#update-related-record) 
* [Upload document](#upload-document)
-->

+++ **[!UICONTROL Create a record]**

Este módulo de ação cria um novo registro do tipo selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Adicione os cabeçalhos da solicitação no formato de um objeto JSON padrão. Por exemplo, <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Group]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL Widget])</b> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group info]</td> 
   <td> <p>Insira ou mapeie os [!UICONTROL Name] e [!UICONTROL ID] do grupo e indique se este grupo é o grupo padrão para a conta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library document info]</td> 
   <td> <p>Preencha os seguintes campos:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Files to send]</b> </p> <p>Para cada arquivo que deseja adicionar, clique em <b>[!UICONTROL Add item]</b> e preencha os campos.</p> 
      <ul> 
       <li><b>[!UICONTROL Transient document ID]</b> <p>Insira a ID do documento transitório</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Preencha os seguintes campos:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Insira o tipo MIME do arquivo original. Os tipos MIME (Multipurpose Internet Mail Extension) são rótulos que permitem que o software identifique diferentes tipos de dados compartilhados na Internet. Servidores da Web e navegadores usam o tipo MIME para determinar o que deve ser feito com um arquivo. Por exemplo, um arquivo com o tipo MIME <code>text/html</code> será processado em um navegador de forma diferente de um arquivo com o tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Insira um nome para o arquivo.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Insira o URL do arquivo que deseja enviar.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Selecione se este documento precisa ser notariado.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Library template name]</b> </p> <p>Insira ou mapeie o nome do modelo de biblioteca</p> </li> 
     <li> <p><b>[!UICONTROL Sharing mode]</b> </p> <p>Especifique quem deve ter acesso ao documento da biblioteca.</p> </li> 
     <li> <p><b>[!UICONTROL Library document state]</b> </p> <p>Selecione se o documento está no estado de criação ou ativo.</p> </li> 
     <li> <p><b>[!UICONTROL Library template type]</b> </p> <p>Para cada tipo de modelo de biblioteca que você deseja usar, clique em <b>[!UICONTROL Add item]</b> e selecione o tipo de modelo.</p> </li> 
     <li> <p><b>[!UICONTROL Last event date]</b> </p> <p>Insira a última data em que um evento ocorreu no documento da biblioteca.</p> <p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
     <li> <p><b>[!UICONTROL Library document status]</b> </p> <p>Selecione o status do documento de biblioteca.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User info]</td> 
   <td> <p>Preencha os seguintes campos:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Email]</b> </p> <p>Insira o endereço de email do usuário.</p> </li> 
     <li> <p><b>[!UICONTROL Is account admin]</b> </p> <p>Marque essa opção se o usuário criado for um administrador de conta.</p> </li> 
     <li> <p><b>[!UICONTROL User ID]</b> </p> <p>Insira o identificador exclusivo do usuário</p> </li> 
     <li> <p><b>[!UICONTROL Account ID]</b> </p> <p>Digite o identificador exclusivo da conta do [!DNL Adobe Acrobat Sign] associada a este usuário.</p> </li> 
     <li> <p><b>[!UICONTROL First name]</b> </p> <p>Insira o nome do usuário.</p> </li> 
     <li> <p><b>[!UICONTROL Last name]</b> </p> <p>Insira o sobrenome do usuário</p> </li> 
     <li> <p><b>[!UICONTROL Company]</b> </p> <p>Insira o nome da empresa do usuário.</p> </li> 
     <li> <p><b>[!UICONTROL Initials]</b> </p> <p>Insira as iniciais do usuário.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Insira o local do usuário. Isso determina o idioma da interface do usuário. </p> </li> 
     <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Insira o número de telefone do usuário</p> </li> 
     <li> <p><b>ID do grupo primário</b> </p> <p>Insira o grupo ao qual o novo usuário é adicionado. Se nada for inserido, o usuário será adicionado ao grupo padrão da conta.</p> </li> 
     <li> <p><b>[!UICONTROL Job title]</b> </p> <p>Informe o cargo do usuário.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Web form info]</td> 
   <td> <p>Preencha os seguintes campos</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File info]</b> </p> <p>Para cada arquivo que deseja adicionar ao formulário web, clique em Add e preencha os seguintes campos:</p> 
      <ul> 
       <li> <p>[!UICONTROL File type]</p> <p>[!UICONTROL Document]</p> </li> 
       <li> <p>[!UICONTROL Transient document]</p> </li> 
       <li> <p>[!UICONTROL URL file info]</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form name]</b> </p> <p>Insira um nome para o formulário web. Esse nome é usado para identificar o formulário web em locais como emails e sites.</p> </li> 
     <li> <p><b>[!UICONTROL Web form state]</b> </p> <p>Selecione o estado em que o novo formulário web deve ser criado.</p> </li> 
     <li> <p><b>[!UICONTROL Web form participant set info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Para cada membro que você deseja adicionar ao conjunto de participantes, clique em <b>[!UICONTROL Add item]</b>. </p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Deixe essa opção em branco.</p> </li> 
         <li> <p><b>[!UICONTROL Security option]</b> </p> <p>Se quiser adicionar uma opção de segurança para autenticar este usuário, selecione <b>[!UICONTROL Yes]</b>, em seguida, selecione a opção de segurança e preencha todos os campos necessários.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Role]</b> </p> <p>Selecione a função. Todos os membros deste conjunto de participantes compartilham a função.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form additional participant sets info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Para cada membro que você deseja adicionar ao conjunto de participantes, clique em <b>[!UICONTROL Add item]</b>.</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Deixe essa opção em branco.</p> </li> 
         <li> <p><b>[!UICONTROL Security option]</b> </p> <p>Se quiser adicionar uma opção de segurança para autenticar este usuário, selecione <b>[!UICONTROL Yes]</b>, em seguida, selecione a opção de segurança e preencha todos os campos necessários.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Role]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Web form participant ID] </b> </p> <p>Insira a ID do participante do formulário web.</p> </li> 
       <li> <p><b>[!UICONTROL Order]</b> </p> <p>Especifique a ordem de quando este conjunto de participantes deve interagir com o formulário web. Por exemplo, o grupo de participantes que tem um valor de ordem 1 deve ir primeiro, 2 deve ir depois e assim por diante. Os números de ordem devem começar com um e não devem ter lacunas na série. </p> </li> 
       <li> <p><b>[!UICONTROL Provider participant set info]</b> </p> <p>Se o participante for desconhecido, informe se o provedor deve fornecer detalhes ao participante e informe uma mensagem com os detalhes necessários para o participante desconhecido.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Authentication failure info]</b> </p> <p>Para fornecer uma página de erro ou falha para seus usuários, selecione <b>[!UICONTROL Yes]</b> e preencha os seguintes campos:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Insira o URL da página de erro</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Ative esta opção se desejar que a página de erro apareça dentro do formulário web</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Insira o atraso, em segundos, antes que o usuário seja redirecionado para a página de erro.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL CC info]</b> </p> <p>Para cada endereço de email no qual você deseja receber um email quando o contrato final no formulário da Web for assinado, clique em <b>[!UICONTROL Add item]</b> e insira o endereço de email.</p> </li> 
     <li> <p><b>[!UICONTROL Completion info]</b> </p> <p style="font-style: normal;">Para fornecer uma página de sucesso aos seus usuários, selecione <b>[!UICONTROL Yes]</b> e preencha os seguintes campos:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Insira o URL da página de sucesso</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Ative esta opção se desejar que a página de sucesso apareça dentro do formulário web</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Insira o atraso, em segundos, antes que o usuário seja redirecionado para a página de sucesso.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Group ID]</b> </p> <p>Insira a ID do grupo ao qual o formulário web pertence. Se nada for inserido, o formulário web pertencerá ao grupo principal do usuário da conta.</p> </li> 
     <li> <p><b>[!UICONTROL Last event date]</b> </p> <p>Insira a data em que o último evento ocorreu no formulário web. Use o formato <code>yyyy-MM-dd'T'HH:mm:ssZ</code>.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Insira o local do usuário. Isso determina o idioma da interface do usuário. </p> </li> 
     <li> <p><b>[!UICONTROL Security optio]n</b> </p> <p>Digite a senha usada para proteger o documento. Você deve comunicar essa senha separadamente a todas as partes relevantes.</p> </li> 
     <li> <p><b>[!UICONTROL Vaulting info]</b> </p> <p>Se sua conta estiver configurada para compartimentalização de documentos e a opção para habilitar por contrato, você poderá habilitar essa opção para compartimentalizar este contrato.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create an agreement]**

Este módulo de ação cria um contrato, o envia para assinatura e retorna a ID do contrato.

>[!NOTE]
>
>Recomendamos carregar o documento para assinar como um documento transitório e, em seguida, mapeá-lo para o campo [!UICONTROL File to send] no módulo [!UICONTROL Create an agreement]. Para obter um exemplo, consulte &quot;Carregar documento&quot; neste artigo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Adicione os cabeçalhos da solicitação no formato de um objeto JSON padrão. Por exemplo, <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Files to send]</td> 
   <td> <p>Para cada item que você deseja incluir no contrato, clique em <b>[!UICONTROL Add Item]</b> e preencha os seguintes campos:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File Type]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Document]</b> </p> <p>Preencha os seguintes campos:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Created date]</b> </p> <p>Insira ou mapeie a data em que o documento foi criado no formato <code>yyyy-MM-dd'T'HH:mm:ssZ</code>. Por exemplo, <code>2016-02-25T18:46:19Z</code> representa a hora UTC.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Insira ou mapeie a ID do documento.</p> </li> 
         <li> <p><b>[!UICONTROL Label]</b> </p> <p>Insira ou mapeie um rótulo exclusivo para o arquivo. No caso de fluxo de trabalho personalizado, mapeará um arquivo para o elemento de arquivo correspondente na definição do fluxo de trabalho. Isso deve ser especificado no caso de uma solicitação de criação de contrato de fluxo de trabalho personalizado.</p> </li> 
         <li> <p><b>[!UICONTROL Number of pages]</b> </p> <p>Insira ou mapeie o número de páginas no documento.</p> </li> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Insira ou mapeie o tipo MIME do arquivo original. Os tipos MIME (Multipurpose Internet Mail Extension) são rótulos que permitem que o software identifique diferentes tipos de dados compartilhados na Internet. Servidores da Web e navegadores usam o tipo MIME para determinar o que deve ser feito com um arquivo. Por exemplo, um arquivo com o tipo MIME <code>text/html</code> será processado em um navegador de forma diferente de um arquivo com o tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Insira ou mapeie um nome para o documento.<br></p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Library document ID]</b> </p> <p>Insira a ID do documento de biblioteca</p> </li> 
       <li> <p><b>[!UICONTROL Transient document ID]</b> </p> <p>Insira a ID do documento transitório</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Preencha os seguintes campos:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Insira o tipo MIME do arquivo original. Os tipos MIME (Multipurpose Internet Mail Extension) são rótulos que permitem que o software identifique diferentes tipos de dados compartilhados na Internet. Servidores da Web e navegadores usam o tipo MIME para determinar o que deve ser feito com um arquivo. Por exemplo, um arquivo com o tipo MIME <code>text/html</code> será processado em um navegador de forma diferente de um arquivo com o tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Insira um nome para o arquivo.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Insira o URL do arquivo que deseja enviar.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Insira um rótulo para o arquivo.</p> </li> 
     <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Habilite esta opção para indicar que o arquivo deve ser notariado.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement name]</td> 
   <td>Informe um nome para o novo acordo. Esse nome é usado para identificar o contrato em locais como emails e sites.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant sets info]</td> 
   <td> <p>Para cada conjunto de participantes que deseja adicionar, clique em <b>[!UICONTROL Add item]</b> e preencha os campos a seguir.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Members]</b> </p> <p>Para cada pessoa que deseja adicionar ao conjunto de participantes, clique em <b>[!UICONTROL Add item]</b> e insira o endereço de email da pessoa.</p> </li> 
     <li> <p><b>[!UICONTROL Order]</b> </p> <p>Especifique a ordem de quando este conjunto de participantes deve assinar o contrato. Por exemplo, o grupo de participantes que tem um valor de ordem 1 deve assinar primeiro, 2 deve assinar próximo e assim por diante. Os números de ordem devem começar com um e não devem ter lacunas na série. </p> </li> 
     <li> <p><b>[!UICONTROL Role]</b> </p> <p>Selecione uma função para este conjunto de participantes. Todos os participantes do conjunto recebem essa função.</p> </li> 
     <li> <p><b>[!UICONTROL ID]</b> </p> <p>Insira ou mapeie o ID deste conjunto de participantes.</p> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Insira ou mapeie um rótulo exclusivo para o conjunto de participantes. Para fluxos de trabalho personalizados, o rótulo especificado no conjunto de participação deve mapeá-lo para a etapa de participação no fluxo de trabalho personalizado.</p> </li> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Informe um nome para o conjunto de participantes. Esse nome deve ser exclusivo dentro do contrato.</p> </li> 
     <li> <p><b>[!UICONTROL Private message]</b> </p> <p>Insira ou mapeie uma mensagem para este conjunto de participantes. Todos os participantes do conjunto recebem esta mensagem.</p> </li> 
     <li> <p><b>[!UICONTROL Visible pages]</b> </p> <p>Se a visibilidade limitada de documentos estiver habilitada para este contrato, especifique quais arquivos estarão visíveis para este conjunto de participantes. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Signature type]</td> 
   <td> <p>Selecione o tipo de assinatura exigido pelo contrato.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-sign]</b> </p> <p>O contrato deve ser assinado eletronicamente.</p> </li> 
     <li> <p><b>[!UICONTROL Written]</b> </p> <p>O contrato deve ser assinado manualmente e o contrato assinado deve ser digitalizado e carregado.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td> <p>Selecione um estado para este contrato.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Authoring]</b> </p> <p>Você ainda pode editar ou adicionar campos a este contrato.</p> </li> 
     <li> <p><b>[!UICONTROL Draft]</b> </p> <p>Você pode criar este contrato de forma incremental antes de enviá-lo.</p> </li> 
     <li> <p><b>[!UICONTROL In Process]</b> </p> <p>Este contrato será enviado imediatamente.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CCs]</td> 
   <td> <p>Você pode enviar este contrato às partes interessadas que não precisam assiná-lo, como as partes interessadas. Eles recebem um email no início do processo de assinatura e outro quando a assinatura final é recebida. Eles também recebem uma cópia PDF do contrato. </p> <p>Para cada pessoa que deseja CC neste contrato, clique em <b>[!UICONTROL Add item]</b> e preencha os seguintes campos:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Email]</b> </p> <p>Insira ou mapeie o endereço de email que você deseja incluir no contrato.</p> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Insira ou mapeie um rótulo para este endereço de email, conforme visto na descrição do fluxo de trabalho</p> </li> 
     <li> <p><b>[!UICONTROL Visible pages]</b> </p> </li> 
     <li> <p>Se a visibilidade limitada de documentos estiver habilitada para este contrato, especifique quais arquivos estarão visíveis para este conjunto de participantes. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email option]</td> 
   <td> <p>Para cada tipo de email, selecione se esse tipo de email será enviado a todos os participantes ou nenhum.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Completion emails]</b> </p> <p>Enviar um email quando este contrato for concluído, cancelado, expirado ou rejeitado.</p> </li> 
     <li> <p><b>[!UICONTROL In-Flight emails]</b> </p> <p>Email enviado quando este contrato é delegado ou substituído.</p> </li> 
     <li> <p><b>[!UICONTROL Agreement initiation emails]</b> </p> <p>Enviar um email quando este contrato for criado ou quando uma ação nele for solicitada.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td> <p>Insira ou mapeie uma ID para este contrato. Você pode especificar quando o contrato é criado e usá-lo para localizar o contrato em módulos ou consultas posteriores.</p> <p>Observação: o valor da ID externa está visível para todos os participantes por meio da API, portanto, não deve ser usado para conter um token confidencial.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Merge field info]</td> 
   <td> <p>Para cada campo no contrato para o qual você deseja colocar um valor padrão, clique em <b>[!UICONTROL Add item]</b> e insira o valor padrão e o nome do campo.</p> <p>Os valores serão apresentados aos signatários para campos editáveis. Para campos somente leitura, os valores fornecidos não serão editáveis durante o processo de assinatura.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Notary info]</td> 
   <td> <p>Preencha os seguintes campos:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Appointment]</b> </p> <p>Insira ou mapeie uma hora e uma data propostas para o compromisso a ser autenticado neste contrato.</p> </li> 
     <li> <p><b>[!UICONTROL Note]</b> </p> <p>Insira ou mapeie quaisquer notas que deseja incluir sobre a sessão de notário.</p> </li> 
     <li> <p><b>[!UICONTROL Payment]</b> </p> <p>Selecione se o notário é pago pelo signatário ou pelo remetente do contrato.</p> </li> 
     <li> <p><b>[!UICONTROL Notary Type]</b> </p> <p>Selecionar o tipo de notário</p> 
      <ul> 
       <li> <p>[!UICONTROL Provider notary]</p> <p>O notário é fornecido pelo notário.</p> </li> 
       <li> <p>[!UICONTROL BYON notary]</p> <p>O notário é fornecido pelo cliente.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Post sign option]</td> 
   <td> <p>Selecione se deseja que os signatários sejam direcionados a uma página de sucesso após a assinatura do contrato. Se você selecionar <b>[!UICONTROL Yes]</b>, preencha os seguintes campos:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Redirect delay]</b> </p> <p>Insira ou mapeie um número que represente o número de segundos antes de o signatário ser redirecionado para a página de sucesso. Se esse valor for maior que 0, o usuário verá primeiro a mensagem de sucesso [!DNL Adobe Sign] padrão e, depois de um atraso, será redirecionado para sua página de sucesso.</p> </li> 
     <li> <p><b>[!UICONTROL Redirect URL]</b> </p> <p>Insira ou mapeie um URL acessível publicamente para o qual o usuário será enviado após concluir com êxito o processo de assinatura.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Security option]</td> 
   <td> <p>Insira ou mapeie a senha secundária que será usada para proteger o documento PDF. </p> <p>Importante: [!DNL Adobe Sign] nunca compartilhará esta senha, portanto, você deve comunicá-la separadamente a todos os relevantes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vaulting info]</td> 
   <td>Se sua conta estiver configurada para compartimentalização de documentos e a opção para habilitar por contrato, você poderá habilitar essa opção para compartimentalizar este contrato.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create related records]**

Esse módulo de ação cria registros vinculados a um módulo selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo do registro original ao qual deseja associar os registros criados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Insira ou mapeie a ID do objeto ao qual você deseja associar o registro criado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement related field]</td> 
   <td> <p>Selecione o tipo de campo relacionado que você deseja criar</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Form fields]</b> </p> <p>Insira a ID do modelo que contém os campos que você deseja criar</p> </li> 
     <li> <p><b>[!UICONTROL Reminders]</b> </p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Recipient participant ID]</b> </p> <p>Para cada participante que você deseja receber um lembrete, clique em [!UICONTROL Add item] e insira a ID do participante.</p> </li> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Para novos registros, o status deve ser [!UICONTROL Active].</p> </li> 
       <li> <p><b>[!UICONTROL First reminder delay]</b> </p> <p>Insira o atraso em horas antes de enviar o primeiro lembrete. O valor mínimo permitido é 1 hora e o valor máximo não pode ser maior do que a diferença entre a criação do contrato e a hora de expiração do contrato em horas. Se esse atraso não for definido, o primeiro lembrete será baseado na frequência.</p> </li> 
       <li> <p><b>[!UICONTROL Reminder frequency]</b> </p> <p>Defina a frequência com que deseja enviar o lembrete. Se a frequência não for fornecida, o lembrete será enviado uma vez.</p> </li> 
       <li> <p><b>[!UICONTROL Last sent date]</b> </p> <p>Este campo é definido pelo sistema.</p> </li> 
       <li> <p><b>[!UICONTROL Next sent date]</b> </p> <p>Este campo deve estar em branco ou definido como [!UICONTROL ONCE].</p> </li> 
       <li> <p><b>[!UICONTROL Note]</b> </p> <p>Insira uma nota a ser incluída no lembrete. Isso é útil para informar ao participante por que sua participação é necessária.</p> </li> 
       <li> <p><b>[!UICONTROL Start reminder counter from]</b> </p> <p>Selecione se o lembrete será enviado com base em quando o contrato será criado, em quando ele estiver disponível.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Signer identity report]</b> </p> <p>Digite a senha usada para proteger o documento PDF.</p> </li> 
     <li> <p><b>[!UICONTROL Views]</b> </p> <p>Insira os seguintes campos</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Selecione o nome da view que deseja criar.</p> </li> 
       <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para fazer logon automaticamente do usuário na URL retornada.</p> </li> 
       <li> <p><b>[!UICONTROL Frame Parent]</b> </p> <p>Insira ou mapeie uma lista separada por vírgulas de URLs de domínio pai em que os URLs retornados possam ser transformados em quadros. Se deixado em branco, as [!DNL Adobe Acrobat Sign] páginas não serão exibidas no iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Insira o idioma em que deseja criar a exibição. </p> </li> 
       <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para mostrar a página inserida sem um cabeçalho ou rodapé de navegação.</p> </li> 
       <li> <p><b>[!UICONTROL Can edit files]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se quiser que a seção de carregamento de arquivo seja editada adicionando ou removendo arquivos. Isso não é um mecanismo de controle de acesso. O padrão é [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se quiser que os links de documentos da biblioteca fiquem visíveis. O padrão é [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Local file]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se desejar que o botão de carregamento de arquivo local seja exibido. O padrão é [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Web connectors]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se desejar que os links para anexar documentos de fontes da Web apareçam. O padrão é Sim.</p> </li> 
       <li> <p><b>[!UICONTROL Is preview selected]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para definir a página Compor para o modo de criação.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Member share]</b> </p> <p>Para cada membro com o qual você deseja compartilhar o contrato, clique em <b>[!UICONTROL Add item]</b> e insira o endereço de email do membro e uma mensagem para esse membro.</p> </li> 
     <li> <p>[!UICONTROL Delegate participant set]</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Participant set ID]</b> </p> <p>Insira o ID do conjunto de participantes</p> </li> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Para cada membro que você deseja adicionar, clique em [!UICONTROL Add item] e insira as informações de endereço de email e telefone do membro.</p> </li> 
       <li> <p><b>[!UICONTROL Private message]</b> </p> <p>Insira uma mensagem. Todos os membros do conjunto de participantes recebem esta mensagem.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library view info]</td> 
   <td> <p>Preencha os seguintes campos:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Insira um nome para o modelo de biblioteca. Esse nome é usado em emails e sites.</p> </li> 
     <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para fazer logon automaticamente do usuário na URL retornada.</p> </li> 
     <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Insira ou mapeie uma lista separada por vírgulas de URLs de domínio pai em que os URLs retornados possam ser transformados em quadros. Se deixado em branco, as [!DNL Adobe Acrobat Sign] páginas não serão exibidas no iframe.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Insira o idioma em que deseja criar a exibição. </p> </li> 
     <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para mostrar a página inserida sem um cabeçalho ou rodapé de navegação.</p> </li> 
     <li> <p><b>[!UICONTROL Send view configuration]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se quiser configurar a exibição [!UICONTROL Send] e preencha os campos a seguir.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Agreement name]</b> </p> <p>Insira ou mapeie o nome do contrato para o documento de biblioteca na página de composição.</p> </li> 
       <li> <p><b>[!UICONTROL Can edit files]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se quiser que a seção de carregamento de arquivo seja editada adicionando ou removendo arquivos. Isso não é um mecanismo de controle de acesso. O padrão é [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Local file]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se quiser que os links de documentos da biblioteca fiquem visíveis. O padrão é [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Web connectors]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se desejar que os links para anexar documentos de fontes da Web apareçam. O padrão é [!UICONTROL Yes].</p> </li> 
       <li> <p><b>Visualização selecionada</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para definir a página Compor para o modo de criação.</p> </li> 
      </ul> <p> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User view info]</td> 
   <td> <p>Preencha os seguintes campos</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Selecione o nome da visualização do usuário solicitada.</p> </li> 
     <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para fazer logon do usuário automaticamente. Selecione <b>[!UICONTROL No]</b> para exigir credenciais. O padrão é [!UICONTROL No].</p> </li> 
     <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Insira ou mapeie uma lista separada por vírgulas de URLs de domínio pai em que os URLs retornados possam ser transformados em quadros. Se deixado em branco, as [!DNL Adobe Acrobat Sign] páginas não serão exibidas no iframe.</p> </li> 
     <li> <p><b>Nenhum sinalizador do Chrome</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para mostrar a página inserida sem um cabeçalho ou rodapé de navegação.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Widget related fields]</td> 
   <td> <p>Selecione o registro relacionado que deseja criar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Views]</p> <p>Preencha os campos a seguir.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Selecione o nome da exibição de formulário web solicitada</p> </li> 
       <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para fazer logon do usuário automaticamente. Selecione <b>[!UICONTROL No]</b> para exigir credenciais. O padrão é [!UICONTROL No].</p> </li> 
       <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Insira ou mapeie uma lista separada por vírgulas de URLs de domínio pai em que os URLs retornados possam ser transformados em quadros. Se deixado em branco, as [!DNL Adobe Acrobat Sign] páginas não serão exibidas no iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Insira o idioma em que deseja criar a exibição. </p> </li> 
       <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para mostrar a página inserida sem um cabeçalho ou rodapé de navegação.</p> </li> 
       <li> <p>[!UICONTROL Personalized signing view configuration]</p> <p>Se quiser configurar uma exibição de assinatura personalizada, selecione <b>[!UICONTROL Yes]</b> e preencha os seguintes campos:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Insira o endereço de email da pessoa que recebe o formulário web recém-criado</p> </li> 
         <li> <p><b>[!UICONTROL Comment]</b> </p> <p>Insira um comentário descrevendo como o chamador da API estabeleceu a identidade do signatário. Essas informações aparecem na trilha de auditoria [!DNL Adobe Acrobat Sign].</p> </li> 
         <li> <p><b>[!UICONTROL Expiration]</b> </p> <p>Insira uma data de expiração para a personalização deste formulário web. </p> <p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Reusable]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> se quiser que o signatário pretendido assine o formulário mais de uma vez.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Member share]</b> </p> <p>Para cada membro com o qual você deseja compartilhar o contrato, clique em <b>[!UICONTROL Add item]</b> e insira o endereço de email do membro e uma mensagem para esse membro.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Custom API Call]**
Este módulo permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo a <code>https://api.[region].adobesign.com/api/rest/v6/</code></p> <p>Observação: para obter a lista de endpoints disponíveis, consulte a Referência de API [!DNL Adobe Sign].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Insira a string de consulta da solicitação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a transient document]</td> 
   <td> <p>Para fazer upload de um documento transitório, informe o arquivo de origem do documento que deseja fazer upload.</p> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List records]**

Esse módulo de ação lista todos os registros do tipo selecionado aos quais a conta tem acesso.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo de registro para o qual deseja recuperar registros relacionados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td> <p>Insira o local do usuário. Isso determina o idioma da interface do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td>Insira ou mapeie a ID Externa (uma ID atribuída fora de [!DNL Adobe Acrobat Sign]) para os contratos que você deseja retornar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group ID]</td> 
   <td>Insira a ID do grupo associado aos registros que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show hidden (records)]</td> 
   <td>Ative essa opção se desejar incluir registros ocultos nos resultados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cursor] / [!UICONTROL Start index]</td> 
   <td> <p>Insira o número do primeiro registro que o módulo deve retornar. </p> <p>Observação: este campo é combinado com o campo [!UICONTROL Maximum number of returned records] para paginação. Por exemplo, se [!UICONTROL Maximum number of returned events] for 100 e [!UICONTROL Start index] for 101, o módulo retornará os registros 101-200 ou a segunda página de resultados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned records]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros para o qual deseja que o módulo [action] durante cada ciclo de execução do cenário.</p> <p>Observação: este campo é combinado com o campo [!UICONTROL Cursor] ou [!UICONTROL Start Index] para paginação. Por exemplo, se [!UICONTROL Maximum number of returned events] for 100 e [!UICONTROL Start index] for 101, o módulo retornará os registros 101-200 ou a segunda página de resultados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent domain URLs]</td> 
   <td> <p>Insira ou mapeie uma lista separada por vírgulas de URLs de domínio pai em que os URLs retornados possam ser transformados em quadros. Se deixado em branco, as [!DNL Adobe Acrobat Sign] páginas não serão exibidas no iframe.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Read a record]**

Este módulo de ação recupera informações de um único registro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo de registro para o qual deseja recuperar registros relacionados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
   <td>Insira ou mapeie a ID do registro que deseja recuperar.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Read related records]**

Leia informações adicionais relacionadas a um único registro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo de registro para o qual deseja recuperar registros relacionados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID] (Exemplo: [!UICONTROL Account ID])</td> 
   <td>Informe ou mapeie a ID do registro para o qual deseja recuperar registros relacionados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td>Insira informações em campos específicos com base no tipo de registro e em campos relacionados.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update a record]**

Este módulo de ação atualiza um único registro em [!DNL Adobe Acrobat Sign].

>[!IMPORTANT]
>
>* Como prática recomendada, se você estiver antecipando alterações substanciais em um contrato, recomendamos criar um novo contrato em vez de atualizar o contrato existente.
>* Algumas atualizações apresentam campos obrigatórios. Ao configurar sua atualização, preencha todos os campos obrigatórios. Os campos obrigatórios estão em negrito nos módulos [!DNL Workfront Fusion].
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID] </td> 
   <td>Insira ou mapeie a ID do registro que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo de registro que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td> <p>Insira informações em campos específicos com base no tipo de registro e em campos relacionados.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Agreement]</b> </p> <p>Como prática recomendada, se você estiver antecipando alterações substanciais em um contrato, recomendamos criar um novo contrato em vez de atualizar o contrato existente.</p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Selecione os campos que deseja atualizar e preencha os campos selecionados:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Selecione o novo status para o documento de biblioteca.</p> </li> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Insira ou mapeie o nome do modelo de biblioteca</p> </li> 
       <li> <p><b>[!UICONTROL Sharing mode]</b> </p> <p>Especifique quem deve ter acesso ao documento da biblioteca.</p> </li> 
       <li> <p><b>[!UICONTROL Library template type]</b> </p> <p>Para cada tipo de modelo de biblioteca que você deseja usar, clique em <b>[!UICONTROL Add item]</b> e selecione o tipo de modelo.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> <p>Selecione os campos que deseja atualizar e preencha os campos selecionados:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL First name]</b> </p> <p>Insira o nome do usuário.</p> </li> 
       <li> <p><b>[!UICONTROL Last name]</b> </p> <p>Insira o sobrenome do usuário</p> </li> 
       <li> <p><b>[!UICONTROL Company]</b> </p> <p>Insira o nome da empresa do usuário.</p> </li> 
       <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Insira o número de telefone do usuário</p> </li> 
       <li> <p><b>[!UICONTROL Primary group ID]</b> </p> <p>Insira o grupo ao qual o novo usuário é adicionado. Se nada for inserido, o usuário será adicionado ao grupo padrão da conta.</p> </li> 
       <li> <p><b>[!UICONTROL Job title]</b> </p> <p>Informe o cargo do usuário.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL widget])</b> </p> <p>Insira informações em campos específicos com base no tipo de registro e em campos relacionados.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update related record]**

Esse módulo de ação atualiza registros relacionados a um objeto específico.

>[!IMPORTANT]
>
>* Como prática recomendada, se você estiver antecipando alterações substanciais em um contrato, recomendamos criar um novo contrato em vez de atualizar o contrato existente.
>* Algumas atualizações apresentam campos obrigatórios. Ao configurar sua atualização, preencha todos os campos obrigatórios. Os campos obrigatórios estão em negrito nos módulos [!DNL Workfront Fusion].
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecione o tipo do registro ao qual os campos relacionados estão associados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Insira ou mapeie a ID do objeto ao qual você deseja associar o registro criado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td> <p>Insira informações em campos específicos com base no tipo de registro e em campos relacionados.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Agreement]</b> </p> <p>Como prática recomendada, se você estiver antecipando alterações substanciais em um contrato, recomendamos criar um novo contrato em vez de atualizar o contrato existente.</p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Selecione os campos que deseja atualizar e preencha os campos selecionados:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Selecione o novo status para o documento de biblioteca.</p> </li> 
       <li> <p><b>[!UICONTROL Note]</b> </p> <p>Insira ou mapeie o texto da nota.</p> </li> 
       <li> <p><b>[!UICONTROL Visibility]</b> </p> <p>Selecione se o documento de biblioteca é exibido ou oculto.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> <p>Selecione os campos que deseja atualizar e preencha os campos selecionados:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Group info list]</b> </p> <p>Preencha os seguintes campos</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Status]</b> </p> <p>Selecione o novo status para o usuário.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Insira o identificador exclusivo do grupo</p> </li> 
         <li> <p><b>[!UICONTROL Is group admin]</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para tornar este usuário um administrador de grupo.</p> </li> 
         <li> <p><b>É o grupo principal</b> </p> <p>Selecione <b>[!UICONTROL Yes]</b> para atualizar este grupo para o grupo primário do usuário.</p> </li> 
         <li> <p><b>[!UICONTROL Created date]</b> </p> <p>Insira a data em que o grupo foi criado.</p> <p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coerção de tipo em [!UICONTROL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Insira ou mapeie o nome do grupo.</p> </li> 
         <li> <p><b>[!UICONTROL Library document creation visible]</b> </p> <p>Essas configurações determinam se o usuário pode criar documentos de biblioteca</p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Permitir</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Herdar configurações de grupo do grupo ou da conta</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL Send restricted to workflows]</b> </p> <p>Essas configurações determinam se o usuário pode criar contratos somente usando workflows.</p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Permitir</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Herdar configurações de grupo do grupo ou da conta</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL User can send]</b> </p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Permitir</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Herdar configurações de grupo do grupo ou da conta</p> </li> 
          </ul> </li> 
        </ul> </li> 
      </ul> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Selecione o novo estado do usuário e insira um comentário sobre por que você deseja ativar ou desativar o usuário.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Insira o local do usuário. Isso determina o idioma da interface do usuário. </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL widget])</b> </p> <p>Insira informações em campos específicos com base no tipo de registro e em campos relacionados.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Upload document]**

Carregue um documento transitório. Um documento transitório fica disponível por 7 dias após ser carregado.

>[!NOTE]
>
>Recomendamos fazer upload do documento para assinar como um documento transitório e, em seguida, mapeá-lo para o campo File to send no módulo Create an agreement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
   <td>Insira ou mapeie a ID do registro que deseja atualizar</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td>Insira o tipo MIME do arquivo original. Os tipos MIME (Multipurpose Internet Mail Extension) são rótulos que permitem que o software identifique diferentes tipos de dados compartilhados na Internet. Servidores da Web e navegadores usam o tipo MIME para determinar o que deve ser feito com um arquivo. Por exemplo, um arquivo com o tipo MIME <code>text/html</code> será processado em um navegador de forma diferente de um arquivo com o tipo MIME <code>image/jpeg</code>.</td> 
  </tr> 
 </tbody> 
</table>

**Exemplo:** neste fluxo de trabalho, o documento a ser assinado (baixado anteriormente do Workfront) é carregado como um documento transitório.

(/help/workfront-fusion/references/apps-and-modules/assets/sign-example-1-350x308.png)

O módulo [!UICONTROL Upload document] fornece ao documento uma ID [!DNL Adobe Acrobat Sign] que pode ser referenciada em módulos posteriores. Quando o contrato é criado, a ID do documento carregado é incluída no campo [!UICONTROL Files to send].

![Exemplo de assinatura](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-2-350x356.png)

+++

### Pesquisas

+++ **[!UICONTROL Search agreements]**

Este módulo de pesquisa pesquisa procura contratos com base nos critérios fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Acrobat Sign] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text filter]</td> 
   <td> <p>Pesquisar texto nos metadados do contrato. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Find text]</b> </p> <p>Insira o texto que deseja localizar nos metadados do contrato. Cada palavra é tratada como um item de texto separado. </p> </li> 
     <li> <p><b>[!UICONTROL Find text in]</b> </p> <p>Selecione os campos de metadados nos quais deseja localizar texto. Se você não selecionar nada, os módulos pesquisarão todos os metadados.</p> </li> 
    </ul> <p>O módulo retorna qualquer contrato que contenha qualquer um dos textos inseridos em qualquer um dos campos selecionados. Exemplo: inserir "campanha de primavera" e selecionar as opções Título e Nota retorna quaisquer contratos com as palavras "primavera" ou "Campanha" no Título ou Nota.</p> <p>Para obter mais informações sobre a pesquisa de campos no [!DNL Adobe Acrobat Sign], consulte "Como funciona a pesquisa de texto" no <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">[!DNL Adobe Sign] Search - Como funciona</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created date]</td> 
   <td>Selecione datas. O módulo retorna somente registros nos quais a data de criação corresponde a este critério.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expiration date]</td> 
   <td>Selecione datas. O módulo retorna somente registros em que a data de expiração corresponde a esse critério.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL Modified date]</p> </td> 
   <td>Selecione datas. O módulo retorna somente registros nos quais a data de modificação corresponde a este critério.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td> <p> A ID externa é uma ID atribuída pelo remetente ao contrato que pode ser de qualquer forma, mas geralmente na forma de "&lt;groupID&gt;:&lt;ID&gt;".</p> <p>Para cada ID externa que você deseja adicionar, clique em <b>[!UICONTROL Add]</b> e insira ou mapeie a ID externa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group ID]</td> 
   <td> <p>ID de grupo é um identificador atribuído quando o grupo foi criado.</p> <p>Para cada ID externa que você deseja adicionar, clique em <b>[!UICONTROL Add]</b> e insira ou mapeie a ID externa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Esta é a ID atribuída ao contrato específico. </p> <p>Para cada ID externa que você deseja adicionar, clique em <b>[!UICONTROL Add]</b> e insira ou mapeie a ID externa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent ID]</td> 
   <td> <p>Esta é a ID atribuída ao objeto principal do contrato. </p> <p>Para cada ID externa que você deseja adicionar, clique em <b>[!UICONTROL Add]</b> e insira ou mapeie a ID externa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant email]</td> 
   <td> <p>O endereço de email de um participante. </p> <p>Para cada ID externa que você deseja adicionar, clique em <b>[!UICONTROL Add]</b> e insira ou mapeie a ID externa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Role]</td> 
   <td>Selecione as funções que você deseja que os resultados retornados incluam.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td>Se desejar que o módulo classifique os resultados, selecione o campo pelo qual deseja classificar os resultados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort orde]r</td> 
   <td>Se desejar que o módulo classifique os resultados, selecione se deseja classificar em ordem crescente ou decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
   <td>Selecione os status que você deseja que os resultados retornados incluam.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selecione os tipos de acordo que você deseja que os resultados retornados incluam.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subtypes]</td> 
   <td>Selecione os subtipos de acordo que você deseja que os resultados retornados incluam. Somente os subtipos de recursos de contratos de modelo de biblioteca.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User ID]</td> 
   <td> <p>A ID do usuário com o qual o contrato está compartilhado.</p> <p>Para cada ID de usuário que você deseja adicionar, clique em <b>[!UICONTROL Add]</b> e insira ou mapeie a ID de usuário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Selecione o nível de visibilidade que você deseja que os resultados retornados incluam.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start index]</td> 
   <td> <p>Insira a posição do primeiro resultado que deseja retornar. Combine isso com o [!UICONTROL maximum returned results] para paginar resultados</p> <p>Exemplo: se você retornar 100 resultados por vez, digite 100 para retornar os resultados 100-200.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros para o qual deseja que o módulo [action] durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++
