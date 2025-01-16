---
title: Módulos do Gmail
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Gmail, bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 0%

---

# [!DNL Gmail] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Gmail], bem como conectá-los a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Para usar módulos [!DNL Gmail], você deve ter uma conta [!DNL Gmail].

## Conectar [!DNL Gmail] a [!DNL Workfront Fusion] {#connect-gmail-to-workfront-fusion}

* [Conectar [!DNL Gmail] a [!DNL Workfront Fusion] usando [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usingg-suite)
* [Conectar [!DNL Gmail] a [!DNL Workfront Fusion] usando [!DNL gmail.com] ou [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Conectar [!DNL Gmail] a [!DNL Workfront Fusion] usando[!DNL  Google Workspace] {#connect-gmail-to-workfront-fusion-using-g-suite}

Para obter instruções sobre como conectar sua conta do [!DNL Google Workspace] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md.

### Conectar [!DNL Gmail] a [!DNL Workfront Fusion] usando [!DNL gmail.com] ou [!DNL googlemail].com {#connect-gmail-to-workfront-fusion-using-gmail-com-or-googlemail-com}

Se você for [!DNL @gmail.com] ou [!DNL @googlemail.com] usuário, deve criar um cliente OAuth em [the [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) para obter um [!UICONTROL Client ID] e [!UICONTROL Client Secret].

Para obter instruções passo a passo sobre como criar o cliente OAuth e obter um [!UICONTROL Client ID] e [!UICONTROL Client Secret], consulte [Conectar o Adobe Workfront Fusion ao Google Services usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## [!DNL Gmail] módulos e seus campos

Ao configurar módulos do [!DNL Gmail], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Gmail] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Ações](#actions)
* [Iteradores](#iterators)

### Triggers

#### [!UICONTROL Watch emails]

Esse módulo de acionamento executa um cenário quando um novo email é recebido para ser processado.

O módulo retorna todos os campos padrão associados ao registro ou aos registros, juntamente com quaisquer campos e valores personalizados que a conexão acesse. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta de e-mail que deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter type] </td> 
   <td> <p>Selecione o tipo de filtro que deseja usar para assistir a emails</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Simple filter]</strong> </p> <p>Preencha os campos [!UICONTROL Criteria], [!UICONTROL Sender Email Address], [!UICONTROL Subject] e [!UICONTROL Search Phrase]</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail filter]</strong> </p> <p>No campo [!UICONTROL Query], insira a consulta que deseja usar para filtrar emails.</p> <p>Para obter mais informações sobre filtros [!DNL Gmail], consulte <a href="https://support.google.com/mail/answer/7190">Operadores de pesquisa</a> na documentação [!DNL Gmail].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteria]</td> 
   <td>Selecione se você deseja assistir a [!UICONTROL all email], [!UICONTROL only read emails] ou [!UICONTROL only unread] emails.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sender email address]</td> 
   <td> <p> Digite um endereço de e-mail para ver apenas os e-mails enviados a partir desse endereço.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Digite uma sequência de texto para ver somente os emails que tenham essa sequência de texto no assunto.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search phrase]</td> 
   <td>Digite uma sequência de texto para ver somente os emails que possuem essa sequência de texto em qualquer lugar do email.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mark email message(s) as read when fetched]</td> 
   <td> <p> Ative esta opção para marcar os e-mails recuperados como lidos.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of results]</td> 
   <td> <p> Defina o número máximo de resultados com os quais [!DNL Workfront Fusion] trabalhará durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Send an email]](#send-an-email)
* [[!UICONTROL Create a draft]](#create-a-draft)
* [[!UICONTROL Mark an email as read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an email as unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an email]](#move-an-email)
* [[!UICONTROL Copy an email]](#copy-an-email)
* [[!UICONTROL Delete an email]](#delete-an-email)
* [[!UICONTROL Modify email labels]](#modify-email-labels)

#### [!UICONTROL Send an email]

Esse módulo de ação envia um novo email.

Especifique o recipient do email.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL From]</td> 
   <td> <p>Insira ou mapeie um endereço de email de remetente.</p> <p>Observação: se você inserir um endereço de email incorreto, poderá ocorrer um erro ao enviar uma mensagem porque sua conta talvez não tenha permissão para enviar emails de um endereço diferente do seu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Clique em <strong>[!UICONTROL Add]</strong> e, em seguida, insira ou mapeie o endereço de email de cada destinatário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Insira ou mapeie o assunto do email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Insira ou mapeie o conteúdo do email (corpo da mensagem). Tags HTML são permitidas.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Clique em <strong>[!UICONTROL Add]</strong> para adicionar um anexo. Você pode mapear um arquivo dos módulos anteriores.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Clique em <strong>[!UICONTROL Add]</strong> e, em seguida, insira ou mapeie o endereço de email para cada destinatário de cópia.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Clique em <strong>[!UICONTROL Add]</strong> e, em seguida, insira ou mapeie o endereço de email para cada destinatário de cópia oculta.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a draft]

Esse módulo de ação cria um novo rascunho de email e o adiciona a uma pasta especificada por você.

Você especifica a pasta na qual deseja criar um rascunho.

O módulo retorna a ID do rascunho do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta [!DNL Gmail] na qual deseja criar um rascunho.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Clique em <strong>[!UICONTROL Add]</strong> e, em seguida, insira ou mapeie o endereço de email de cada destinatário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Insira ou mapeie o assunto do email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Insira ou mapeie o conteúdo do email (corpo da mensagem). Tags HTML são permitidas.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Clique em <strong>[!UICONTROL Add]</strong> para adicionar um anexo. Você pode mapear um arquivo dos módulos anteriores.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Clique em <strong>[!UICONTROL Add]</strong> e, em seguida, insira ou mapeie o endereço de email para cada destinatário de cópia.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Clique em <strong>[!UICONTROL Add]</strong> e, em seguida, insira ou mapeie o endereço de email para cada destinatário de cópia oculta.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as read]

Este módulo de ação marca um email como lido.

Especifique a ID do email e sua pasta.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta [!DNL Gmail] que contém o email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Insira ou mapeie a ID de email.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as unread]

Este módulo de ação marca um email ou rascunho de email como não lido.

Especifique a ID do email e sua pasta.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta [!DNL Gmail] que contém o email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)] </td> 
   <td> <p>Insira ou mapeie a ID de e-mail do e-mail que você deseja marcar como não lido.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an email]

Esse módulo de ação move um email ou rascunho de email para uma pasta especificada por você.

Você especifica a pasta, a pasta de destino e a ID do email.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta de origem [!DNL Gmail] que contém o email que você deseja mover.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p> Selecione a pasta de destino [!DNL Gmail] para a qual você deseja mover o email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Insira ou mapeie a ID de email do email que você deseja mover.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an email]

Esse módulo de ação copia um email ou rascunho de email para uma pasta especificada por você.

Você especifica a pasta, a pasta de destino e a ID do email.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta de origem [!DNL Gmail] que contém o email que você deseja copiar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p>Selecione a pasta de destino [!DNL Gmail] para a qual você deseja copiar o email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p>Insira ou mapeie a ID de e-mail do e-mail que deseja copiar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an email]

Esse módulo de ação remove um email ou um rascunho de email de uma pasta especificada.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] ID da mensagem]</p> </td> 
   <td> <p>Insira ou mapeie a ID de e-mail do e-mail que deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanently] </td> 
   <td> <p>Ative esta opção para permitir que o módulo exclua permanentemente o e-mail, em vez de movê-lo para a pasta de lixo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify email labels]

Esse módulo de ação modifica o rótulo em uma mensagem de email especificada.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao [!DNL Workfront Fusion], consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] ID da mensagem]</td> 
   <td> <p> Insira ou mapeie a ID de e-mail do e-mail que deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Labels to add]</p> </td> 
   <td> <p>Selecione ou mapeie o rótulo que deseja adicionar à mensagem de email selecionada.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Labels to remove]</td> 
   <td> <p> Selecione ou mapeie o rótulo que deseja remover da mensagem de email selecionada.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Os campos [!UICONTROL Label to add] e [!UICONTROL Label to remove] carregam apenas rótulos criados pelo usuário.

### Iteradores

#### [!UICONTROL Iterate attachments]

Você pode iterar anexos de email. Cada anexo é um conjunto separado na saída do módulo. Para obter mais informações, consulte [Módulo Iterador](/help/workfront-fusion/references/modules/iterator-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> <p>Selecione o módulo do qual deseja iterar anexos. </p> </td> 
  </tr> 
 </tbody> 
</table>
