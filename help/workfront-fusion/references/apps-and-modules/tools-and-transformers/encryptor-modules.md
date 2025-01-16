---
title: Criptografador
description: Os módulos do Adobe Workfront Fusion Encryptor permitem criptografar quaisquer dados de texto. Atualmente, eles suportam criptografia de mensagens via AES256 e PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---

# Criptografador

[!DNL Adobe Workfront Fusion] módulos do [!UICONTROL Encryptor] permitem que você criptografe dados de texto. Atualmente, eles oferecem suporte à criptografia de mensagens via AES256 e PGP ([!UICONTROL OpenPGP]).

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
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho, [!UICONTROL [!DNL Workfront Fusion] para Automação do Trabalho</p>
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

## Criptografia e descriptografia de mensagens usando PGP

Ao criptografar e descriptografar via PGP, é necessário usar um chaveiro e criar uma chave privada ou pública (ou ambas).

Para obter mais informações sobre chaves públicas e privadas, consulte o [glossário do Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md). <!--For more information on keychains, see [Keys in [!DNL Adobe Workfront Fusion]]().-->

## [!UICONTROL Encryptor] módulos e seus campos

Ao configurar módulos do [!UICONTROL Encryptor], os campos a seguir são exibidos. Um título em negrito em um módulo indica um campo obrigatório.

### Criptografar uma mensagem PGP

Esse módulo permite criptografar uma mensagem usando chaves públicas e privadas.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Insira a chave privada do remetente. Isso pode autenticar a identidade do remetente.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Insira a chave pública do recipient.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Informe a mensagem que deseja criptografar.</td>
    </tr>

### Descriptografar uma mensagem PGP

Este módulo permite descriptografar uma mensagem usando chaves públicas e privadas.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Insira a chave privada do recipient.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Insira a chave pública do recipient. Isso pode autenticar a identidade do remetente.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Mapeie a mensagem que deseja descriptografar.</td>
    </tr>
</table>
