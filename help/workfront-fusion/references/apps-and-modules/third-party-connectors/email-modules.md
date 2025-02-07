---
title: Módulos de email
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode conectar sua conta de email a vários aplicativos e serviços de terceiros. Isso permite baixar emails via IMAP, enviar emails via SMTP, criar novos rascunhos, mover e copiar emails de uma pasta para outra pasta, marcar emails como lidos ou não lidos e excluir emails.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: add63edf94cc430113bf2cfd0c389cca04aa92f8
workflow-type: tm+mt
source-wordcount: '2023'
ht-degree: 0%

---

# Módulos de email

Em um cenário do [!DNL Adobe Workfront Fusion], você pode conectar sua conta de email a vários aplicativos e serviços de terceiros. Isso permite baixar emails via IMAP, enviar emails via SMTP, criar novos rascunhos, mover e copiar emails de uma pasta para outra pasta, marcar emails como lidos ou não lidos e excluir emails.

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

## Conectar seu email ao Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Conectar-se ao Google](#connect-to-google)
* [Conectar-se a outros serviços de email (IMAP)](#connect-to-other-email-services-smap)

### Conectar a [!DNL Google]

Use esta opção para criar cenários com módulos de email que exigem uma conexão com sua conta do [!DNL Google]. Esta é uma conta com escopos restritos.

Você pode criar uma conexão com sua conta do [!DNL Google] diretamente de dentro de um módulo de Email.

1. Em qualquer módulo Email, clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. Selecione **[!DNL Google]** como o tipo de conexão.
1. Insira um nome para a conexão.
1. (Opcional) Digite seu [!UICONTROL [!DNL Google] Client ID] e [!UICONTROL Client Secret].
1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

### Conectar-se a outros serviços de email (IMAP)

A conexão IMAP permite acessar a caixa de correio remotamente e ler ou manipular mensagens na caixa de correio. A conexão IMAP é usada pela maioria dos módulos de email.

1. Em qualquer módulo Email, clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. Selecione **[!UICONTROL Others (SMTP)]** como o tipo de conexão.
1. Insira um **[!UICONTROL Name]** para a conexão.
1. Selecione seu **[!UICONTROL Email provider]** na lista. Se o seu provedor de email não estiver na lista, selecione Outro.
1. Digite o **[!UICONTROL User name]** e seu **[!UICONTROL Password]** para a conta de email.
1. (Condicional) Se seu provedor não estiver na lista, digite seus **[!UICONTROL SMTP server]** e **[!UICONTROL Port]** e especifique se deseja **[!UICONTROL Use a secure connection (TLS)]**. Para encontrar essas informações, verifique a seção [!UICONTROL Help] da sua caixa de correio. Se você não tiver essas informações disponíveis, entre em contato com seu provedor de serviços de email.
1. Para usar um certificado autoassinado, habilite a opção **Rejeitar certificados não autorizados** e carregue seu certificado autoassinado. Para obter instruções, consulte [Carregar um certificado autoassinado](#upload-a-self-signed-certificate)
1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

#### Carregar um certificado autoassinado

Para adicionar um certificado autoassinado:

1. Clique em **Extrair**.
1. Selecione o tipo de arquivo que você está extraindo.
1. Selecione o arquivo que contém o certificado ou.
1. Digite a senha do arquivo.
1. Clique em **Salvar** para extrair o arquivo e retornar à configuração do módulo.

## [!UICONTROL Email] módulos e seus campos

Ao configurar módulos do [!UICONTROL Email], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Alguns dos campos de email podem já conter dados porque você os usou em outro módulo no cenário. Consulte a documentação de ajuda do email se precisar de informações sobre eles.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>A Identificação de Email Exclusiva conhecida como &#39;[!UICONTROL Email ID (UID)]&#39; é o identificador do email. A ID de e-mail é específica para cada uma das pastas de e-mail.

* [Acionadores](#triggers)
* [Ações](#actions)
* [Iteradores](#iterators)

### Acionadores

#### [!UICONTROL Watch Emails]

Esse módulo de acionamento inicia um cenário quando um novo email é recebido para processamento de acordo com critérios especificados.

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
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Digite o assunto do email que você deseja assistir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Digite quaisquer palavras-chave para ver apenas os emails que contêm as palavras-chave.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched]</td> 
   <td> <p>Habilite esta opção para marcar o e-mail não lido como lido após recuperar os detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Insira ou mapeie o número máximo de emails que [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Copy an Email]](#copy-an-email)
* [[!UICONTROL Create a Draft]](#create-a-draft)
* [[!UICONTROL Delete an Email]](#delete-an-email)
* [[!UICONTROL Get Emails]](#get-emails)
* [[!UICONTROL Mark an Email as Read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an Email as Unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an Email]](#move-an-email)
* [[!UICONTROL Send an Email]](#send-an-email)

#### [!UICONTROL Copy an Email]

Esse módulo de ação copia um email ou um rascunho para uma pasta selecionada.

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
   <td> <p>Insira o UID de email do email que deseja copiar para a pasta de destino.</p> <p>Você pode obter a UID do email usando o módulo [!UICONTROL Email] &gt; [!UICONTROL Watch Email] ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Draft]

Este módulo de ação cria e adiciona um novo rascunho a uma pasta selecionada.

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
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Insira ou mapeie o conteúdo do email no formato HTML usando tags HTML ou no texto sem formatação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Para cada anexo que você deseja adicionar, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Insira o nome do arquivo, incluindo a extensão. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Insira o caminho para a pasta onde deseja fazer upload do anexo.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Insira a ID de conteúdo para inserir o anexo (imagem) no conteúdo.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Para cada endereço de email para o qual deseja enviar uma cópia deste email, clique em <b>Adicionar item</b> e insira o endereço de email. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Para cada endereço de email para o qual você deseja enviar uma cópia deste email sem que o endereço apareça no email, clique em <b>Adicionar item</b> e insira o endereço de email.</p> </td> 
  </tr> 
  <!--<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, [!DNL Workfront Fusion] uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "[!UICONTROL from]" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, Sender, Date, To, and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> -->
 </tbody> 
</table>

#### [!UICONTROL Delete an Email]

Este módulo de ação remove um email ou um rascunho da pasta selecionada.

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
   <td>Selecione a pasta que contém o email que deseja excluir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que deseja excluir.</p> <p>Você pode obter a UID do email usando o módulo Email &gt; Assistir Email ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>Habilite esta opção para remover permanentemente todas as mensagens sinalizadas como [!UICONTROL Deleted] na caixa de correio atualmente aberta.</p> <p>Observação: em [!DNL Gmail], esse comportamento é orientado pela configuração na seção [!UICONTROL Settings] &gt;[!UICONTROL Forwarding POP/IMAP in IMAP access].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Emails]

Este módulo retorna emails que correspondem aos critérios especificados.

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
   <td role="rowheader">[!UICONTROL Recipient Email]</td> 
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
   <td> <p>Insira ou mapeie quaisquer palavras-chave para recuperar apenas os emails que contêm essas palavras-chave.</p> </td> 
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

#### [!UICONTROL Mark an Email as Read]

Este módulo de ação marca um email ou rascunho em uma pasta selecionada como lido, definindo o sinalizador [!UICONTROL Read].

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
   <td>Selecione a pasta que contém o email que você deseja marcar como lido.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que você deseja marcar como lido.</p> <p>Você pode obter a UID do email usando o módulo Email &gt; Assistir Email ou o módulo [!UICONTROL Search Email].</p> </td> 
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
   <td>Selecione a pasta que contém o email que você deseja marcar como não lido. Exemplo: Principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que você deseja marcar como não lido.</p> <p>Você pode obter a UID do email usando o módulo Email &gt; Assistir Email ou o módulo [!UICONTROL Search Email].</p> </td> 
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
   <td>Selecione a pasta que contém o email que você deseja mover. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Selecione a pasta à qual deseja adicionar o email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Insira o UID de email do email que você deseja mover para a pasta de destino.</p> <p>Você pode obter a UID do email usando o módulo Email &gt; Assistir Email ou o módulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

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
   <td> <p>Para cada anexo que você deseja adicionar, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Insira o nome do arquivo, incluindo a extensão. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Insira o caminho para a pasta onde deseja fazer upload do anexo.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Insira a ID de conteúdo para inserir o anexo (imagem) no conteúdo.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Para cada endereço de email para o qual deseja enviar uma cópia deste email, clique em <b>Adicionar item</b> e insira o endereço de email. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Para cada endereço de email para o qual você deseja enviar uma cópia deste email sem que o endereço apareça no email, clique em <b>Adicionar item</b> e insira o endereço de email.</p> </td> 
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
<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Insira ou mapeie o endereço de email (e o nome, se necessário) que aparece no campo [!UICONTROL From] no email. </p> <p>Importante: use a sintaxe correta: <code>name@email.com</code> ou <code>"Name" name@email.com</code>.</p> <p>Observação: normalmente, o [!DNL Workfront Fusion] usa o endereço de email que você inseriu ao criar a conexão como o endereço do remetente. Se você inserir qualquer outro endereço de email, poderá ocorrer um erro ao enviar uma mensagem porque sua conta talvez não tenha permissão para enviar emails de um endereço diferente do seu. Por exemplo, <code>test@mail.com</code> ou "<code>John Bush" test@email.com</code>.</p> </td> 
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
