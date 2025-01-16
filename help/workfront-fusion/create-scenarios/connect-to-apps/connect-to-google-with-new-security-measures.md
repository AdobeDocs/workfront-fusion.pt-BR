---
title: Conectar o Adobe Workfront Fusion aos Serviços da Google com medidas de segurança atualizadas
description: A Google introduziu restrições sobre como os usuários podem usar a API. Este artigo descreve como conectar o Adobe Workfront Fusion ao Google, levando em conta essas medidas de segurança de atualização.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: 362952ec85b0df2306ba117ba530e95201330cca
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Conectar o Adobe Workfront Fusion aos Serviços da Google com medidas de segurança atualizadas

A Google introduziu restrições sobre como os usuários podem usar a API. Este artigo descreve como conectar o Adobe Workfront Fusion ao Google, levando em conta essas medidas de segurança de atualização.

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

Os usuários do Google Workspace que preferem usar seu próprio cliente OAuth em vez de usar o cliente OAuth do Workfront Fusion podem se conectar aos Serviços da Google por meio da abordagem de uso interno. Essa opção destina-se a usuários avançados. Para obter instruções, consulte [Conectar o Adobe Workfront Fusion ao Google Services usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

### @gmail.com e @googlemail.com {#gmailcom-and-googlemailcom}

Os usuários que acessam os Serviços da Google por meio de @gmail.com ou @googlemail.com podem se conectar aos Serviços da Google por meio da abordagem de Uso pessoal. Essa opção destina-se a usuários avançados. Para obter instruções, consulte [Conectar o Adobe Workfront Fusion ao Google Services usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## Perguntas frequentes

* [Quais aplicativos no Adobe Workfront Fusion são afetados?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Eu tenho uma conta do Google Workspace?](#do-i-have-a-g-suite-account)
* [O que devo fazer se sou um usuário @gmail.com ou @googlemail.com?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [O que devo fazer se sou um usuário do Google Workspace?](#what-should-i-do-if-im-a-g-suite-user)

### Quais aplicativos no Adobe Workfront Fusion são afetados? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive, Gmail e Email (conectado à conta do Gmail).

### Eu tenho uma conta do Google Workspace? {#do-i-have-a-g-suite-account}

Se o seu endereço de email termina com @gmail.com ou @googlemail.com, sua conta não é uma conta do Google Workspace. Se sua conta do Google terminar com um domínio personalizado, como @my-company.com, ela será uma conta do Google Workspace.

### O que devo fazer se for um usuário @gmail.com ou @googlemail.com? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

Essas novas restrições só se aplicam se você estiver integrando o Google Drive ou o Gmail. Se quiser se conectar ao Google Drive ou Gmail, você poderá

* Alternar para o Google Workspace

  ou

* Crie um cliente OAuth personalizado. Essa opção destina-se a usuários avançados.

  Para obter instruções, consulte [Conectar o Adobe Workfront Fusion ao Google Services usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Se você quiser integrar qualquer serviço diferente do Google Drive ou Gmail, essas restrições não se aplicam.

### O que devo fazer se sou um usuário do Google Workspace? {#what-should-i-do-if-im-a-g-suite-user}

Não há nenhuma ação necessária.
