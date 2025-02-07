---
title: Conectar o Adobe Workfront Fusion ao Google Services usando um cliente OAuth personalizado
description: Você pode usar o Adobe Workfront Fusion para se conectar aos Serviços da Google usando um cliente OAuth personalizado. Esse procedimento requer uma conta existente do Google.
author: Becky
feature: Workfront Fusion
exl-id: 2f0bc289-4ecf-4a31-9d7b-641bbca6fc95
source-git-commit: 5971b2210eaac8f8a75fd7a4aac5a9f7954d27ef
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 1%

---

# Conectar o Adobe Workfront Fusion ao Google Services usando um cliente OAuth personalizado

Você pode usar o Adobe Workfront Fusion para se conectar aos Serviços da Google usando um cliente OAuth personalizado. Esse procedimento requer uma conta existente do Google.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront 
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
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecione ou Prime Workfront Plan: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Você precisa de uma conta existente do Google para fazer essa conexão.

## Conectar o Fusion aos serviços da Google usando um cliente OAuth personalizado

Para criar essa conexão, você deve criar e configurar um projeto na plataforma Google Cloud e, em seguida, configurar a conexão no Fusion com base nesse projeto.

>[!NOTE]
>
>Este procedimento destina-se a:
>
>* Uso pessoal (`@gmail.com` e `@googlemail.com` usuários)
>* Uso interno (usuários do Google Workspace que preferem usar um cliente OAuth personalizado)

* [Criar um projeto na Google Cloud Platform](#create-a-project-on-google-cloud-platform)
* [Definir configurações de consentimento do OAuth](#configure-oauth-consent-settings)
* [Criar credenciais do OAuth](#create-oauth-credentials)
* [Conectar-se ao Google no Workfront Fusion](#connect-to-google-in-workfront-fusion)

### Criar um projeto na Google Cloud Platform

Para criar um projeto na Google Cloud Platform:

1. Comece a criar um projeto na Google Cloud Platform.

   Para obter instruções, consulte [Criar um projeto da Google Cloud](https://developers.google.com/workspace/guides/create-project) na documentação do Google.
1. Ao habilitar as APIs, você deve habilitar a API do Google Drive, bem como a API de todos os aplicativos Google que deseja usar (como a API do Google Sheets).
1. Conclua a criação do projeto.
1. Prossiga para a seção [Definir configurações de consentimento do OAuth](#configure-oauth-consent-settings) neste artigo.

### Definir configurações de consentimento do OAuth

1. Comece a configurar o OAuth para o seu projeto

   Para obter instruções, consulte [Configurar a tela de consentimento do OAuth e escolher escopos](https://developers.google.com/workspace/guides/configure-oauth-consent) na documentação do Google.
1. Selecione **Externo** e clique em **Criar**.

   >[!NOTE]
   >
   >Você não será cobrado ao selecionar essa opção. Para obter mais informações, consulte as informações da Google sobre exceções aos requisitos de verificação.

1. Preencha os campos obrigatórios da seguinte maneira:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Nome do aplicativo</p> </td> 
      <td> <p>Insira o nome do aplicativo que solicita consentimento.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span>Adobe Workfront Fusion </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Email de suporte ao usuário</td> 
      <td>Insira um endereço de email para que os usuários entrem em contato com você caso tenham dúvidas sobre o consentimento deles ao se conectarem a este aplicativo.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Endereços de email</td> 
      <td>Insira um ou mais endereços de email que a Google pode usar para notificá-lo sobre qualquer alteração no seu projeto.</td> 
     </tr> 
    </tbody> 
   </table>

1. Em Domínios autorizados, clique em **Adicionar domínio** e digite `workfrontfusion.com`.
1. Adicione os seguintes escopos:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Serviço/API</th> 
      <th>Escopos necessários</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td> <p>Gmail</p> </td> 
      <td> <p>https://mail.google.com/</p> <p>https://www.googleapis.com/auth/gmail.labels</p> <p>https://www.googleapis.com/auth/gmail.send</p> <p>https://www.googleapis.com/auth/gmail.readonly</p> <p>https://www.googleapis.com/auth/gmail.compose</p> <p>https://www.googleapis.com/auth/gmail.insert</p> <p>https://www.googleapis.com/auth/gmail.modify</p> <p>https://www.googleapis.com/auth/gmail.metadata</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Google Drive</p> </td> 
      <td> <p>https://www.googleapis.com/auth/drive</p> <p>https://www.googleapis.com/auth/drive.readonly</p> </td> 
     </tr> 
    </tbody> 
   </table>

   Talvez seja necessário expandir a lista ou ir para a próxima página da lista para ver todos eles.

1. (Opcional) Adicione usuários de teste ao projeto.
1. Examine suas informações para verificar a precisão e clique em **Voltar ao painel**.

   >[!NOTE]
   >
   >Você não precisa enviar sua tela de consentimento e seu aplicativo para verificação pela Google.

1. Continue em [Criar credenciais do OAuth](#create-oauth-credentials).

### Criar credenciais do OAuth

1. Comece a criar credenciais da ID do cliente OAuth.

   Para obter instruções, consulte [Criar credenciais de acesso](https://developers.google.com/workspace/guides/create-credentials) na documentação da Google.

   >[!NOTE]
   >
   >Se essa não for a primeira API ou serviço (Gmail ou Google Drive) habilitado, não será necessário criar novas credenciais.

1. Preencha os campos obrigatórios da seguinte maneira:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Tipo de aplicativo</td> 
      <td> <p> aplicação web</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Nome</td> 
      <td>Workfront Fusion </td> 
     </tr> 
    </tbody> 
   </table>

1. Em URIs de redirecionamento autorizados, insira **um** dos seguintes:

   * Para Gmail ou Google Drive: `https://app.workfrontfusion.com/oauth/cb/google-restricted`

   * Para outros aplicativos Google: `https://app.workfrontfusion.com/oauth/cb/google`

1. Clique em **Criar**.

   A ID do cliente e o Segredo do cliente são exibidos.

1. Copie a ID do cliente e o segredo do cliente para um local seguro. Você os usará para fazer uma conexão no Workfront Fusion.
1. Continue para [Conectar-se ao Google no Workfront Fusion](#connect-to-google-in-workfront-fusion).

### Conectar-se ao Google no Workfront Fusion

O processo de criação de uma conexão com o Google difere dependendo se você está usando um módulo de um serviço do Google (como Google Sheets ou Google Docs) ou se está se conectando ao Google por meio do módulo de solicitação HTTP >Criar um OAuth2.0.

* [Conexão com o Google em um serviço do Google](#connect-to-google-in-a-google-service)
* [Conecte-se ao Google no HTTP > Criar um módulo de solicitação OAuth2.0](#connect-to-google-in-the-http--make-an-oauth20-request-module)

#### Conexão com o Google em um serviço do Google

1. No Workfront Fusion, localize o módulo Google para o qual você precisa criar uma conexão.
1. Clique em **Criar uma conexão** e em **Mostrar configurações avançadas**.
1. Preencha os campos Nome da conexão, Ambiente e Tipo, conforme aplicável.
1. Insira a ID do cliente e o Segredo do cliente que você recuperou em [Criar credenciais do OAuth](#create-oauth-credentials) nos respectivos campos e clique em **Continuar**.

1. Faça logon com sua conta da Google.

   A janela **Este aplicativo não foi verificado** é exibida. Observe que o &quot;aplicativo&quot; mencionado no título da janela é o cliente OAuth criado acima.

1. Clique em **Avançado** e em **Ir para o Workfront Fusion (não seguro)** para permitir o acesso usando seu cliente OAuth personalizado.

1. Clique em **Permitir** para conceder permissão ao Workfront Fusion.
1. Na janela exibida, clique em **Permitir** novamente para confirmar suas escolhas.

   A conexão com o serviço Google desejado usando um cliente OAuth personalizado é estabelecida.

#### Conecte-se ao Google no HTTP > Criar um módulo de solicitação OAuth2.0 {#connect-to-google-in-the-http--make-an-oauth20-request-module}

Para obter instruções sobre como se conectar ao Google no HTTP > Criar um módulo de solicitação OAuth2.0, consulte [Instruções para criar uma conexão com o Google em HTTP > Criar um módulo de solicitação OAuth 2.0](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module) no artigo HTTP > Criar um módulo de solicitação OAuth 2.0.

## Possível mensagem de erro:[403 Acesso Não Configurado]

Se a mensagem de erro `403 Access Not Configured` for exibida, você deverá habilitar a API correspondente na Google Cloud Platform. Para habilitar a API, siga as etapas da seção [Criar um projeto na Google Cloud Platform](#create-a-project-on-google-cloud-platform) deste artigo.
