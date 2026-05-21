---
title: Criar conexões
description: Uma conexão deve atender aos requisitos definidos pela API do aplicativo ou serviço Web ao qual ela se conecta. Por esse motivo, as instruções para configurar uma conexão variam com base no aplicativo ou serviço da Web. Este artigo pode ajudá-lo a identificar e localizar as instruções para conectar o Adobe Workfront Fusion ao aplicativo ou serviço da Web escolhido.
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
TQID: https://experienceleague.adobe.com/qjxlwSzWy6FmnASQrhjVKe8A4VyBpw0aBHkNwgQpo3A
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 563
ht-degree: 24%

---

# Criar conexões

Uma conexão deve atender aos requisitos definidos pela API do aplicativo ou serviço Web ao qual ela se conecta. Por esse motivo, as instruções para configurar uma conexão variam com base no aplicativo ou serviço da Web. Este artigo pode ajudá-lo a identificar e localizar as instruções para conectar o Adobe Workfront Fusion ao aplicativo ou serviço da Web escolhido.

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
   <p>Baseado em conector (herdado): para se conectar a aplicativos fora da família de produtos Workfront, é necessário ter a Automação e Integração do Workfront Fusion for Work </p>
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

## Conexão com um aplicativo ou serviço Web que não requer configuração

Na maioria dos casos, você pode usar o módulo para criar uma conexão com pouca ou nenhuma informação extra. O Workfront Fusion lida com a autenticação automaticamente.

Para obter instruções sobre como criar uma conexão sem considerações especiais, consulte [Criar uma conexão - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

## Conectar-se a um aplicativo ou serviço do Adobe

Para se conectar a um aplicativo ou serviço da Adobe, talvez você precise de informações da Adobe Admin Console, como a ID da organização ou a ID de conta técnica.

Você também pode usar o módulo Adobe Authenticator para se conectar a qualquer API do Adobe, usando uma única conexão. Isso permite que você se conecte mais facilmente a produtos da Adobe que ainda não têm um conector Fusion dedicado.

Para obter instruções específicas, consulte [o artigo sobre o conector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products).

## Conectar a um aplicativo ou serviço Web [!DNL Microsoft]

A maioria dos aplicativos [!DNL Microsoft] no Workfront Fusion permite criar uma conexão sem informações adicionais.

As seguintes circunstâncias exigem etapas adicionais na criação de uma conexão:

* Uso de módulos do Microsoft Dynamics 365.

  Para obter instruções, consulte [módulos do Microsoft Dynamics 365](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).

* Conexão com a API do Microsoft Graph usando um módulo HTTP

  Para obter instruções, consulte [Chamar a API REST do MS Graph](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).

## Conectar a um aplicativo ou serviço Web [!DNL Google]

O processo de conexão com os aplicativos do [!DNL Google] pode ser diferente de acordo com o tipo de conta do [!DNL Google] que você está usando. Além disso, as medidas de segurança do [!DNL Google] podem exigir configuração adicional quando você estiver se conectando ao Workfront Fusion.

Para obter mais informações, consulte:

* [Conectar o Adobe Workfront Fusion ao Serviços do Google usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [Conectar o Adobe Workfront Fusion aos Serviços do Google com medidas de segurança atualizadas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## Outros aplicativos que exigem configuração adicional

Alguns aplicativos e serviços não seguem a configuração básica das conexões do Workfront Fusion. Você pode encontrar instruções para conectar esses aplicativos no artigo desse aplicativo.

Para obter instruções específicas, consulte [o artigo sobre o conector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications).
