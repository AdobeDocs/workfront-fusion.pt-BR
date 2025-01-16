---
content-type: reference
title: Aprovar ou desaprovar modelos
description: Este artigo descreve como aprovar ou desaprovar modelos do Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: dafecd8b-96e5-46da-9ab6-15f0bc9b52a4
source-git-commit: 23e9f383b25c7b3789c413e557b94418e48a636b
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 1%

---

# Aprovar ou desaprovar modelos para a guia Público

Os modelos do Adobe Workfront Fusion são cenários pré-criados projetados para automatizar e simplificar vários workflows. Esses modelos podem ajudar os usuários a configurar rapidamente integrações e automações sem precisar criar tudo do zero.

Se você for um administrador, poderá escolher se determinados modelos devem ou não ser compartilhados com toda a organização na guia Public templates.

Os usuários podem enviar modelos criados para aprovação para serem compartilhados na página Modelos públicos. <!--do the have to be requested or can an admin just choose to approve?-->

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plano</td>
      <td><p>Qualquer</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">[!DNL Adobe Workfront] licença</td>
      <td><p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td>
      <td>
        <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
        <p>Ou</p>
        <p>Herdados: Qualquer um</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produto</td>
      <td>
        <p>Novo:</p>
        <ul>
          <li>[!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Workfront] Plano: Sua organização deve comprar [!DNL Adobe Workfront Fusion].</li>
          <li>[!UICONTROL Ultimate] [!DNL Workfront] Plano: [!DNL Workfront Fusion] está incluído.</li>
        </ul>
        <p>Ou</p>
        <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->

+++

## Aprovar ou desaprovar [!DNL Workfront Fusion] modelos

A aprovação de um modelo o torna visível na guia [!UICONTROL Public templates] e disponível a todos os usuários.

Desaprovar um modelo o remove da guia [!UICONTROL Public templates] e o disponibiliza somente para a equipe que o criou.

1. Clique em **[!UICONTROL Administration]** no painel de navegação esquerdo para abrir a área [!UICONTROL Administration].
1. Clique em **[!UICONTROL Templates]** no painel de navegação esquerdo.
1. Se quiser aprovar um modelo, clique em **[!UICONTROL Approve]** à direita do modelo.
1. Se quiser desaprovar um modelo, clique em **[!UICONTROL Disapprove]** à direita do modelo.

>[!NOTE]
>
>Se você estiver aprovando o modelo que foi aprovado anteriormente e editado, sua segunda aprovação substituirá o modelo original.


## Status dos modelos

Você pode verificar o status na página de modelo sob o nome do modelo.

Os seguintes status estão disponíveis:

* **[!UICONTROL Private]**: este modelo é visível apenas para o autor do modelo e sua equipe.
* **[!UICONTROL Published]**: este modelo é visível apenas para o autor do modelo e sua equipe. Depois de publicado, é possível enviar o modelo para aprovação, se desejado. Também é possível copiar um link compartilhável.
* **[!UICONTROL Approved]**: Esse modelo está visível para todos os usuários do Workfront Fusion na guia [!UICONTROL Public templates]. Você também pode copiar um link compartilhável clicando em [!UICONTROL Options] no canto superior direito da tela.

Você também pode verificar o status na guia [!UICONTROL Team templates]. Se um modelo for publicado, ele terá um ícone à direita do nome do modelo.

* **Ícone de olho**: o modelo foi publicado, está visível somente para a equipe e uma solicitação de aprovação não foi enviada.
* **Ícone de marca de seleção amarelo**: o modelo é publicado, está visível somente para a equipe e aguarda aprovação para ser adicionado à guia Modelos públicos.
* **Ícone de marca de seleção verde**: o modelo está disponível na guia Modelos públicos e está visível para qualquer usuário do Workfront Fusion. Ela também ainda está visível na guia [!UICONTROL Team templates]. O autor do modelo ou o membro da equipe ainda pode editá-lo.

Modelos sem ícones têm status [!UICONTROL Private]. Eles não são publicados e são visíveis apenas para a equipe do.


<!--

## Questions about how this works

Editing

1. If an admin edits a template, do they have to publish again? ... Do they have to approve again?
1. What does publishing actually do?
1. Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
1. What is the admin approving? Does a user have to submit it for approval? 



What does "Publishing" mean?
What does "Approving" mean?
If an admin edits a template, do they have to publish again? ... Do they have to approve again?
Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
What is the admin approving? Does a user have to submit it for approval?

-->
