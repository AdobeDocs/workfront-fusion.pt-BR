---
title: Utilização do TLS mútuo em módulos HTTP no Adobe Workfront Fusion
description: Você pode usar o TLS mútuo nos módulos HTTP do Adobe Workfront Fusion, permitindo que ambos os lados da transação de informações verifiquem a identidade do outro.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Usar TLS mútuo em módulos HTTP em [!DNL Adobe Workfront Fusion]

>[!NOTE]
>
>O Adobe Workfront Fusion requer uma licença [!DNL Adobe Workfront Fusion], além de uma licença da Adobe Workfront.

## Visão geral do TLS mútuo

Ao enviar dados pela Internet, é importante garantir que eles cheguem ao local correto ou sejam originados dele e que somente o recipient pretendido possa lê-los. Com o TLS ativado, o cliente (computador solicitando informações) usa certificados para verificar a identidade do servidor (computador fornecendo informações). Isso faz conexões HTTP seguras.

O TLS mútuo permite que essa confirmação de identidade siga ambos os caminhos. Quando o servidor envia seu certificado para verificar sua identidade para o cliente, ele também solicita o certificado do cliente. Isso garante que o servidor não envie informações para um site ou usuário que as usaria incorretamente.

>[!INFO]
>
>**Exemplo:**
>
>* **TLS**: quando uma pessoa digita &quot;MyGreatBank.com&quot; em um navegador, ela quer ter certeza de que está indo para o My Great Bank, não para um site que pode usar incorretamente ou vender suas informações bancárias. Eles também querem ter certeza de que as informações de sua conta bancária estão criptografadas.
>
>   Quando o navegador (o cliente) se conecta ao MyGreatBank.com (o servidor), o TLS requer um certificado do MyGreatBank.com para verificar sua identidade. O certificado é fornecido por uma autoridade de certificação como [!DNL DigiCert] ou [!DNL Thawte]. Como o navegador confia na autoridade de certificação, ele permite a conexão.
>
>* **TLS mútuo**: MySoftware.com é um cliente de software que precisa de informações da API MyGreatBank.com. MyGreatBank permite que apenas clientes confiáveis se conectem aos seus servidores. Portanto, além do TLS normal verificar a identidade do MyGreatBank.com, o processo da autoridade de certificação/TLS também verifica a solicitação do MySoftware.com.

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

&#42;Para saber qual plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

&#42;&#42;Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Fornecendo seu certificado público [!DNL Workfront Fusion]


Quando você se conecta a um serviço Web com uma solicitação HTTP, o serviço Web geralmente requer um certificado público [!DNL Workfront Fusion] para verificação. Isso permite que o serviço da Web compare o certificado apresentado na solicitação HTTP com o do arquivo, como uma maneira de garantir que o certificado esteja na inclui na lista de permissões do serviço da Web.

Para obter instruções sobre como carregar o certificado público [!DNL Adobe Workfront Fusion] para um serviço Web, consulte a documentação do serviço Web.

>[!NOTE]
>
>Talvez seja necessário fornecer outras informações além do certificado. Para obter informações sobre o que um serviço Web exige, consulte a documentação da API do serviço Web.

Você pode usar os seguintes links para baixar os certificados públicos do Workfront Fusion:

### Certificados para 23 de abril de 2023 a 7 de maio de 2024

>[!IMPORTANT]
>
>* Esses [!DNL Workfront Fusion] certificados públicos expiram em 7 de maio de 2025. Depois que o seu expirar, será necessário carregar um novo certificado no serviço da Web. Recomendamos:
>
>   * Anote a data de expiração e defina um lembrete para você fazer upload do certificado para o seu serviço da Web.
>   * Adicione esta página aos favoritos para encontrar facilmente os novos certificados.
>
>* Esses são certificados mTLS não curingas.

* [Baixar [!DNL Workfront Fusion] Certificado 2023](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem)
* [Baixar [!DNL Workfront Fusion] Certificado UE 2023](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem)

  Para utilização na UE

<!--

### Certificates for November 14, 2022 - July 15, 2023

>[!IMPORTANT]
>
>* These [!DNL Workfront Fusion] public certificates expire on July 15, 2023.
>* These are wildcard mTLS certificates.

* [Download [!DNL Workfront Fusion] Certificate 2023](https://cdn.experience.workfront.com/Documentation/Workfront+Fusion+2.0+public+certificates/app_workfrontfusion_com-jul-15-2023+updated.cer)
* [Download [!DNL Workfront Fusion] EU Certificate 2023](https://cdn.experience.workfront.com/Documentation/Workfront+Fusion/app-eu_workfrontfusion_com-jul-15-2023.cer)

   For use in the EU 

   -->

## Habilitando o TLS mútuo em módulos HTTP [!DNL Workfront Fusion]

Todos os módulos de solicitação [!DNL Workfront Fusion] [!UICONTROL HTTP] têm a opção de habilitar o TLS Mútuo.

Para habilitar o TLS Mútuo em um módulo de solicitação [!UICONTROL HTTP]:

1. Adicione um módulo de solicitação [!UICONTROL HTTP] ao seu cenário.
1. Comece a configurar o módulo.

   <!--For instructions on configuring an [!UICONTROL HTTP] request module, see the appropriate article under [[!UICONTROL Universal connectors] modules](/help/workfront-fusion/references/apps-and-modules/universal-connectors/).-->

1. Habilite **[!UICONTROL Show advanced settings]** próximo à parte inferior do módulo.
1. Habilitar **[!UICONTROL Use Mutual TLS]**.
