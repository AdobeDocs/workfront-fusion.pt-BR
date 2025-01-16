---
title: Módulos de email
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode conectar sua conta de email a vários aplicativos e serviços de terceiros. Isso permite baixar emails via IMAP, enviar emails via SMTP, criar novos rascunhos, mover e copiar emails de uma pasta para outra pasta, marcar emails como lidos ou não lidos e excluir emails.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 0%

---

# Módulos de email

Em um cenário do [!DNL Adobe Workfront Fusion], você pode conectar sua conta de email a vários aplicativos e serviços de terceiros. Isso permite baixar emails via IMAP, enviar emails via SMTP, criar novos rascunhos, mover e copiar emails de uma pasta para outra pasta, marcar emails como lidos ou não lidos e excluir emails.

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

## Conectar seu email ao Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Conectar-se ao Google](#connect-to-google)
* [Conectar-se a outros serviços de email (SMAP)](#connect-to-other-email-services-smap)

### Conectar a [!DNL Google]

Use esta opção para criar cenários com módulos de email que exigem uma conexão com sua conta do [!DNL Google]. Esta é uma conta com escopos restritos.

Você pode criar uma conexão com sua conta do [!DNL Google] diretamente de dentro de um módulo de Email.

1. Em qualquer módulo Email, clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. Selecione **[!DNL Google]** como o tipo de conexão.
1. Insira um nome para a conexão.
1. (Opcional) Digite seu [!UICONTROL [!DNL Google] Client ID] e [!UICONTROL Client Secret].
1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

### Conectar-se a outros serviços de email (SMAP)

A conexão SMAP permite que você acesse sua caixa de correio remotamente e leia ou manipule mensagens em sua caixa de correio. A conexão SMAP é usada pela maioria dos módulos de email.

1. Em qualquer módulo Email, clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. Selecione **[!UICONTROL Others (SMTP)]** como o tipo de conexão.
1. Insira um **[!UICONTROL Name]** para a conexão.
1. Selecione seu **[!UICONTROL Email provider]** na lista. Se o seu provedor de email não estiver na lista, selecione Outro.
1. Insira o **[!UICONTROL Email address]**, **[!UICONTROL Your full name]**, **[!UICONTROL User name]** e **[!UICONTROL Password]**.
1. (Condicional) Se seu provedor não estiver na lista, digite seus **[!UICONTROL SMTP server]** e **[!UICONTROL Port]** e especifique se deseja **[!UICONTROL Use a secure connection (TLS)]**. Para encontrar essas informações, verifique a seção [!UICONTROL Help] da sua caixa de correio. Se você não tiver essas informações disponíveis, entre em contato com seu provedor de serviços de email.
1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

## [!UICONTROL Email] módulos e seus campos

Ao configurar módulos do [!UICONTROL Email], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Alguns dos campos de email podem já conter dados porque você os usou em outro módulo no cenário. Consulte a documentação de ajuda do email se precisar de informações sobre eles.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>A Identificação de Email Exclusiva conhecida como &#39;[!UICONTROL Email ID (UID)]&#39; é o identificador do email. A ID de e-mail é específica para cada uma das pastas de e-mail.

* [Triggers](#triggers)
* [Ações](#actions)
* [Iteradores](#iterators)

### Triggers

#### [!UICONTROL Watch Emails]

Acionado quando um novo email é recebido para processamento de acordo com critérios especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!UICONTROL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta que contém os emails que você deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Selecione os critérios pelos quais você deseja assistir aos emails:</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Insira o endereço de email do remetente cujos emails você deseja assistir.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email Address]</td> 
   <td> <p> Insira o endereço de email do recipient cujos emails você deseja assistir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Digite o assunto do email que você deseja assistir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Insira quaisquer palavras-chave para observar apenas os emails que contêm frases específicas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched]</td> 
   <td> <p>Habilite esta opção para marcar o e-mail não lido como lido após recuperar os detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> O número máximo de emails [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Send an Email]](#send-an-email)
* [[!UICONTROL Create a Draft]](#create-a-draft)
* [[!UICONTROL Mark an Email as Read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an Email as Unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an Email]](#move-an-email)
* [[!UICONTROL Copy an Email]](#copy-an-email)
* [[!UICONTROL Delete an Email]](#delete-an-email)
* [[!UICONTROL Get Emails]](#get-emails)

#### [!UICONTROL Send an Email]

Envia um novo email.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!DNL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save Message after Sending]</td> 
   <td>Depois que a mensagem de email for enviada, ela será salva na sua caixa de correio. Habilite esta opção se quiser salvar emails enviados usando o [!DNL Workfront Fusion] na pasta <i>[!UICONTROL Sent mail]</i> ou em outra pasta na sua caixa de correio. Alguns serviços de email, como o [!DNL Gmail], salvam mensagens enviadas automaticamente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Adicione os endereços de email para os quais deseja enviar o email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Insira ou mapeie a linha de assunto do email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>Selecione o tipo [!UICONTROL content] para o email:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plaintext]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Insira ou mapeie o conteúdo do email no formato HTML usando tags HTML ou no texto sem formatação, dependendo do que você escolher no campo [!UICONTROL Content Type].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Adicionar um anexo:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Insira o nome do arquivo. Por exemplo, sample.doc.</p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Insira o caminho para a pasta onde será feito o upload do anexo.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Insira o [!UICONTROL content ID] para inserir o anexo (imagem) no conteúdo.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Insira ou mapeie um ou mais endereços de email para os quais deseja enviar uma cópia deste email. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Insira ou mapeie um ou mais endereços de email para os quais deseja enviar uma cópia deste email sem que o endereço de email apareça no email.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Insira ou mapeie o endereço de email (e o nome, se necessário) que aparece no campo [!UICONTROL From] no email. </p> <p>Importante: use a sintaxe correta: <code>name@email.com</code> ou <code>"Name" name@email.com</code>.</p> <p>Observação: normalmente, o [!DNL Workfront Fusion] usa o endereço de email que você inseriu ao criar a conexão como o endereço do remetente. Se você inserir qualquer outro endereço de email, poderá ocorrer um erro ao enviar uma mensagem porque sua conta talvez não tenha permissão para enviar emails de um endereço diferente do seu. Por exemplo, <code>test@mail.com</code> ou "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Insira ou mapeie o endereço de email que aparece no campo [!UICONTROL Sender] no email.</p> <p>Dica: se você não tiver certeza se deve usar esse campo ou o campo De, recomendamos escolher o campo De.</p> <p>Importante: Use a sintaxe correta: <code>name@email.com</code> ou <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> Se desejar que as respostas a este e-mail sejam enviadas para um endereço diferente do endereço "de", digite o endereço de e-mail para o qual deseja que as respostas a este e-mail sejam enviadas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> Se estiver respondendo a um email específico, insira ou mapeie a ID do email ao qual você está respondendo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Informe as IDs de mensagem de todas as respostas da thread.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Selecione a prioridade do email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Adicione os cabeçalhos:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Adicione a chave. Por exemplo, [!UICONTROL Sender], [!UICONTROL Date], [!UICONTROL To] e assim por diante.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Insira o valor da chave.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Draft]

Cria e adiciona um novo rascunho a uma pasta selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!UICONTROL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecione a pasta na qual deseja criar o rascunho de email.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Insira ou mapeie o endereço de email para o qual deseja enviar o email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Insira ou mapeie a linha de assunto do email.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>Selecione o tipo de conteúdo do email:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plain Text]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Insira ou mapeie o conteúdo do email no formato HTML usando tags HTML ou no texto sem formatação, dependendo do que você escolher no campo [!UICONTROL Content Type].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Adicionar um anexo:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Insira o nome do arquivo. Por exemplo, sample.doc.</p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Insira o caminho para a pasta onde será feito o upload do anexo.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Insira a ID de conteúdo para inserir o anexo (imagem) no conteúdo.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Insira ou mapeie um ou mais endereços de email para os quais deseja enviar uma cópia deste email. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Insira ou mapeie um ou mais endereços de email para os quais deseja enviar uma cópia deste email sem que o endereço de email apareça no email.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Insira ou mapeie o endereço de email (e o nome, se necessário) que aparece no campo [!UICONTROL From] no email. </p> <p>Importante: use a sintaxe correta: <code>name@email.com</code> ou <code>"Name" name@email.com</code>.</p> <p>Observação: normalmente, o [!DNL Workfront Fusion] usa o endereço de email que você inseriu ao criar a conexão como o endereço do remetente. Se você inserir qualquer outro endereço de email, poderá ocorrer um erro ao enviar uma mensagem porque sua conta talvez não tenha permissão para enviar emails de um endereço diferente do seu. Por exemplo, <code>test@mail.com</code> ou "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Insira ou mapeie o endereço de email que aparece no campo [!UICONTROL Sender] no email.</p> <p>Dica: se você não tiver certeza se deve usar esse campo ou o campo De, recomendamos escolher o campo De.</p> <p>Importante: Use a sintaxe correta: <code>name@email.com</code> ou <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> Se desejar que respostas a este email sejam enviadas para um endereço diferente do endereço "[!UICONTROL from]", digite o endereço de email para o qual deseja enviar respostas a este email.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> Se estiver respondendo a um email específico, insira ou mapeie a ID do email ao qual você está respondendo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Informe as IDs de mensagem de todas as respostas da thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Selecione a prioridade do email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Adicione os cabeçalhos:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Adicione a chave. Por exemplo, Remetente, Data, Para e assim por diante.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Insira o valor da chave.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Read]

Marca um email ou rascunho em uma pasta selecionada como lido ao definir o sinalizador [!UICONTROL Read].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!UICONTROL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecione a pasta do email que deseja marcar como lido. Exemplo: Principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que você deseja marcar como lido.</p> <p>Você pode obter a UID do email usando o módulo [!UICONTROL Email] &gt;[!UICONTROL Watch Email] ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Unread]

Marca um email ou rascunho em uma pasta selecionada como não lido ao configurar o sinalizador Não lido.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!UICONTROL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecione a pasta do email que deseja marcar como não lido. Exemplo: Principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que você deseja marcar como não lido.</p> <p>Você pode obter a UID do email usando o módulo [!UICONTROL Email] &gt;[!UICONTROL Watch Email] ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Email]

Move um email ou rascunho escolhido para uma pasta selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!UICONTROL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Selecione a pasta que contém o email a partir da qual deseja mover o email. Exemplo: Principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Selecione a pasta à qual deseja adicionar o email. Exemplo: Trabalho.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que você deseja mover para a pasta de destino.</p> <p>Você pode obter a UID do email usando o módulo [!UICONTROL Email] &gt;[!UICONTROL Watch Email] ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an Email]

Copia um email ou um rascunho para uma pasta selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!UICONTROL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Selecione a pasta da qual deseja copiar o email. Exemplo: Principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Selecione a pasta para a qual deseja copiar o email. Exemplo: Trabalho.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que deseja copiar para a pasta de destino.</p> <p>Você pode obter a UID do email usando o módulo [!UICONTROL Email] &gt;[!UICONTROL Watch Email] ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Email]

Remove um email ou um rascunho da pasta selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!UICONTROL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecione a pasta do email que deseja excluir. Exemplo: Principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que deseja excluir.</p> <p>Você pode obter a UID do email usando o módulo [!UICONTROL Email] &gt;[!UICONTROL Watch Email] ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>Habilite esta opção para permitir que o módulo remova permanentemente todas as mensagens sinalizadas como [!UICONTROL Deleted] na caixa de correio atualmente aberta.</p> <p>Observação: em [!DNL Gmail], esse comportamento é orientado pela configuração na seção [!UICONTROL Settings] &gt;[!UICONTROL Forwarding POP/IMAP in IMAP access].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Emails]

Retorna emails que correspondem aos critérios especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta de email ao [!UICONTROL Workfront Fusion], consulte <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Conectar seu email ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta que contém os emails que deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched] </td> 
   <td> <p>Ative esta opção se quiser marcar o e-mail não lido como lido após recuperar os detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Selecione os critérios dos emails que deseja recuperar:</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Insira ou mapeie o endereço de email do remetente cujos emails você deseja recuperar.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email Address]</td> 
   <td> <p> Insira ou mapeie o endereço de email do recipient cujos emails você deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From date] </td> 
   <td> <p>Insira ou mapeie a data para recuperar os emails processados na data especificada ou após essa data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before date]</td> 
   <td> <p> Insira ou mapeie a data para recuperar os emails processados na data especificada ou antes dela.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Insira ou mapeie o assunto do email que você deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Insira ou mapeie quaisquer palavras-chave para recuperar apenas os emails que contêm frases específicas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Insira a ID de email (UID) do email cujos detalhes você deseja recuperar.</p> <p>Você pode obter a UID do email usando o módulo [!UICONTROL  Watch Email] de [!DNL Workfront Fusion] ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> O número máximo de emails [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> Selecione se deseja continuar a executar o módulo mesmo se não houver resultados retornados.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Iteradores

#### [!UICONTROL Iterate Attachments]

Repete os anexos recebidos um por um.

O módulo iterador de email permite gerenciar anexos de email separadamente. Por exemplo, você pode configurar o para observar emails e iterar os emails com anexos e receber alertas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module]</td> 
   <td> <p>Selecione o módulo que gera o email com os anexos através dos quais você deseja iterar.</p> </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais informações sobre iteradores, consulte [Módulo do iterador](/help/workfront-fusion/references/modules/iterator-module.md).
