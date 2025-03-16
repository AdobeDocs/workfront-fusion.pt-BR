---
title: Criar conexões
description: Uma conexão deve atender aos requisitos definidos pela API do aplicativo ou serviço Web ao qual ela se conecta. Por esse motivo, as instruções para configurar uma conexão variam com base no aplicativo ou serviço da Web. Este artigo pode ajudá-lo a identificar e localizar as instruções para conectar o [!DNL Adobe Workfront Fusion] ao aplicativo ou serviço Web escolhido.
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Criar conexões

Uma conexão deve atender aos requisitos definidos pela API do aplicativo ou serviço Web ao qual ela se conecta. Por esse motivo, as instruções para configurar uma conexão variam com base no aplicativo ou serviço da Web. Este artigo pode ajudá-lo a identificar e localizar as instruções para conectar o [!DNL Adobe Workfront Fusion] ao aplicativo ou serviço Web escolhido.

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion</p>
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

## Conexão com um aplicativo ou serviço Web que não requer configuração

Na maioria dos casos, você pode usar o módulo para criar uma conexão com pouca ou nenhuma informação extra. [!DNL Workfront Fusion] manipula a autenticação automaticamente.

Para obter instruções sobre como criar uma conexão sem considerações especiais, consulte [Criar uma conexão - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

## Conectar-se a um aplicativo ou serviço do Adobe

Para se conectar a um aplicativo ou serviço da Adobe, talvez você precise de informações da Adobe Admin Console, como a ID da organização ou a ID de conta técnica.

Você também pode usar o módulo Adobe Authenticator para se conectar a qualquer API do Adobe, usando uma única conexão. Isso permite que você se conecte mais facilmente a produtos da Adobe que ainda não têm um conector Fusion dedicado.

Para obter instruções específicas, consulte [o artigo sobre o conector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products).

## Conectar a um aplicativo ou serviço Web [!DNL Microsoft]

A maioria dos aplicativos [!DNL Microsoft] em [!DNL Workfront Fusion] permite que você crie uma conexão sem informações adicionais.

As seguintes circunstâncias exigem etapas adicionais na criação de uma conexão:

* Uso de módulos do Microsoft Dynamics 365.

  Para obter instruções, consulte [módulos do Microsoft Dynamics 365](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).

* Conexão com a API do Microsoft Graph usando um módulo HTTP

  Para obter instruções, consulte [Chamar a API REST do MS Graph](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).

## Conectar a um aplicativo ou serviço Web [!DNL Google]

O processo de conexão com os aplicativos do [!DNL Google] pode ser diferente de acordo com o tipo de conta do [!DNL Google] que você está usando. Além disso, as medidas de segurança do [!DNL Google] podem exigir configuração extra quando você estiver se conectando ao [!DNL Workfront Fusion].

Para obter mais informações, consulte:

* [Conectar o Adobe Workfront Fusion ao Google Services usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [Conectar o Adobe Workfront Fusion aos Serviços da Google com medidas de segurança atualizadas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## Outros aplicativos que exigem configuração adicional

Alguns aplicativos e serviços não seguem a configuração básica para conexões [!DNL Workfront Fusion]. Você pode encontrar instruções para conectar esses aplicativos no artigo desse aplicativo.

Para obter instruções específicas, consulte [o artigo sobre o conector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications).
