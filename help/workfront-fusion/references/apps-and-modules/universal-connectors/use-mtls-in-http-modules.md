---
title: Utilização do TLS mútuo em módulos HTTP no Adobe Workfront Fusion
description: Você pode usar o TLS mútuo nos módulos HTTP do Adobe Workfront Fusion, permitindo que ambos os lados da transação de informações verifiquem a identidade do outro.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 1fa1ef68267d971a2769400a031b333de2f684ce
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Usar TLS mútuo em módulos HTTP em [!DNL Adobe Workfront Fusion]

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

## Fornecendo seu certificado público [!DNL Workfront Fusion]

Quando você se conecta a um serviço Web com uma solicitação HTTP, o serviço Web geralmente requer um certificado público [!DNL Workfront Fusion] para verificação. Isso permite que o serviço da Web compare o certificado apresentado na solicitação HTTP com o do arquivo, como uma maneira de garantir que o certificado esteja na inclui na lista de permissões do serviço da Web.

Para obter instruções sobre como carregar o certificado público [!DNL Adobe Workfront Fusion] para um serviço Web, consulte a documentação do serviço Web.

>[!NOTE]
>
>Talvez seja necessário fornecer outras informações além do certificado. Para obter informações sobre o que um serviço Web exige, consulte a documentação da API do serviço Web.

Você pode usar os seguintes links para baixar os certificados públicos do Workfront Fusion:

### Certificados para 23 de abril de 2024 a 7 de maio de 2025

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


## Habilitando o TLS mútuo em módulos HTTP [!DNL Workfront Fusion]

Todos os módulos de solicitação [!DNL Workfront Fusion] [!UICONTROL HTTP] têm a opção de habilitar o TLS Mútuo.

Para habilitar o TLS Mútuo em um módulo de solicitação [!UICONTROL HTTP]:

1. Adicione um módulo de solicitação [!UICONTROL HTTP] ao seu cenário.
1. Comece a configurar o módulo.

   Para obter instruções sobre como configurar um módulo de solicitação [!UICONTROL HTTP], consulte o artigo apropriado em [Conectores universais](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

1. Habilitar **[!UICONTROL Mostrar configurações avançadas]** próximo à parte inferior do módulo.
1. Habilitar **[!UICONTROL Usar TLS Mútuo]**.
