---
title: Conectar o Adobe Workfront Fusion aos Serviços do Google com medidas de segurança atualizadas
description: A Google introduziu restrições sobre como os usuários podem usar a API. Este artigo descreve como conectar o Adobe Workfront Fusion ao Google, levando em conta essas medidas de segurança de atualização.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: bbd1ec27e52127c8814188612a1e8d5cfab0cd25
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 18%

---

# Conectar o Adobe Workfront Fusion aos Serviços do Google com medidas de segurança atualizadas

A Google introduziu restrições sobre como os usuários podem usar a API. Este artigo descreve como conectar o Adobe Workfront Fusion ao Google, levando em conta essas medidas de segurança de atualização.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote do Adobe Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Os pacotes Workfront Prime e Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p><p>Trabalho ou maior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Restrições aos serviços da Google

A Google introduziu restrições sobre como os usuários podem usar sua API a partir de 1º de junho de 2020. Essas medidas de segurança protegem os usuários do Google contra vazamento ou uso indevido de seus dados pessoais no Google.

Essas restrições estão relacionadas aos aplicativos Gmail e Google Drive.

Para obter mais informações sobre essas restrições, consulte &quot;Requisitos adicionais para escopos de API específicos&quot; na [Política de dados do usuário dos Serviços de API da Google](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)

Para acessar escopos restritos, o serviço conectado (Adobe Workfront Fusion ou qualquer outro serviço que acesse os dados do usuário por meio da API) deve ser verificado e deve ter uma Carta de Avaliação para provar que o serviço é seguro e transparente sobre como os dados são usados. O Workfront Fusion está em conformidade com todos os requisitos da Google para acessar escopos restritos. No entanto, a maioria dos serviços conectados de terceiros no Workfront Fusion não tem a Carta de Avaliação e, portanto, não está em conformidade com os termos do Google. Por causa disso, o Workfront Fusion não tem permissão para enviar dados para esses serviços.

## Exceções às restrições dos Serviços da Google

Há algumas exceções que permitem enviar dados a um serviço de terceiros não aprovado que não tenha a Carta de Avaliação sem violar nenhuma das novas restrições. Elas diferem com base no Google Workspace com o cliente OAuth do Workfront Fusion, Google Workspace com outro cliente OAuth ou @gmail.com e @googlemail.com.

* [Google Workspace com cliente OAuth do Workfront Fusion](#google-workspace-with-workfront-fusion-oauth-client)
* [Google Workspace com outro cliente OAuth](#google-workspace-with-another-oauth-client)
* [@gmail.com e @googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace com cliente OAuth do Workfront Fusion

O Workfront Fusion usa a exceção de Instalação em todo o domínio. A instalação em todo o domínio é adequada para usuários do Google Workspace e permite que os usuários integrem serviços não aprovados sem limitações. Se você for um usuário do Google Workspace, não será necessário executar etapas adicionais e poderá se conectar diretamente a serviços não aprovados.

### Google Workspace com outro cliente OAuth

Google Workspace users that prefer to use their own OAuth client instead of using the Workfront Fusion OAuth client can connect to Google Services through the Internal Use approach. This option is intended for advanced users. For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

### @gmail.com e @googlemail.com {#gmailcom-and-googlemailcom}

Users that access Google Services through @gmail.com or @googlemail.com can connect to Google Services through the Personal Use approach. This option is intended for advanced users. For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## Perguntas frequentes

* [What apps in Adobe Workfront Fusion are affected?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Do I have a Google Workspace account?](#do-i-have-a-g-suite-account)
* [What should I do if I&#39;m a @gmail.com or @googlemail.com user?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [What should I do if I&#39;m a Google Workspace user?](#what-should-i-do-if-im-a-g-suite-user)

### What apps in Adobe Workfront Fusion are affected? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive, Gmail, and Email (connected to Gmail account).

### Do I have a Google Workspace account? {#do-i-have-a-g-suite-account}

If your email address ends with @gmail.com or @googlemail.com, your account is not a Google Workspace account. If your Google account ends with a custom domain such as @my-company.com, then it is a Google Workspace account.

### What should I do if I&#39;m @gmail.com or @googlemail.com user? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

These new restrictions only apply if you are integrating Google Drive or Gmail. If you want to connect to Google Drive or Gmail, you can

* Switch to Google Workspace.

  ou

* Create a custom OAuth client. This option is intended for advanced users.

  For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

If you want to integrate any other service than Google Drive or Gmail, these restrictions do not apply.

### What should I do if I&#39;m a Google Workspace user? {#what-should-i-do-if-im-a-g-suite-user}

Não há nenhuma ação necessária.
