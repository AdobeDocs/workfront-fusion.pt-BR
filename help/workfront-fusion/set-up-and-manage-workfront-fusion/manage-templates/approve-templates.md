---
content-type: reference
title: Aprovar ou desaprovar modelos
description: Este artigo descreve como aprovar ou desaprovar modelos do Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: dafecd8b-96e5-46da-9ab6-15f0bc9b52a4
TQID: https://experienceleague.adobe.com/YxbvSHbDGHOsRUv8UJ8aDUct1daxudv2IGAqG3dkGZU
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: d968a1bc-9a90-4926-a531-bcf272c32aadid: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 526
ht-degree: 5%

---

# Aprovar ou desaprovar modelos para a guia Público

Os modelos do Adobe Workfront Fusion são cenários pré-criados projetados para automatizar e simplificar vários workflows. Esses modelos podem ajudar os usuários a configurar rapidamente integrações e automações sem precisar criar tudo do zero.

Se você for um administrador, poderá escolher se determinados modelos devem ou não ser compartilhados com toda a organização na guia Public templates.

Os usuários podem enviar modelos criados para aprovação para serem compartilhados na página Modelos públicos. <!--do the have to be requested or can an admin just choose to approve?-->

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">Plano Adobe Workfront</td>
      <td><p>Qualquer</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">Licença do Adobe Workfront</td>
      <td><p>Novo: padrão</p><p>Ou</p><p>Atual: [!UICONTROL Trabalho] ou superior</p></td>
    </tr>
    <tr>
      <td role="rowheader">Licença do Adobe Workfront Fusion**</td>
      <td>
        <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
        <p>Ou</p>
        <p>Herdados: Qualquer um</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produto</td>
      <td>
        <p>Novo menu:</p>
        <ul>
          <li>Plano do Workfront para [!UICONTROL Select] ou [!UICONTROL Prime]: sua organização deve comprar o Adobe Workfront Fusion.</li>
          <li>Plano do Workfront do [!UICONTROL Ultimate]: o Workfront Fusion está incluído.</li>
        </ul>
        <p>Ou</p>
        <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).
-->

+++

## Aprovar ou desaprovar modelos do Workfront Fusion

A aprovação de um modelo o torna visível na guia [!UICONTROL Modelos públicos] e disponível para todos os usuários.

Desaprovar um modelo o remove da guia [!UICONTROL Modelos públicos] e o disponibiliza somente para a equipe que o criou.

1. Clique em **[!UICONTROL Administração]** no painel de navegação esquerdo para abrir a área [!UICONTROL Administração].
1. Clique em **[!UICONTROL Modelos]** no painel de navegação esquerdo.
1. Se quiser aprovar um modelo, clique em **[!UICONTROL Aprovar]** à direita do modelo.
1. Se quiser desaprovar um modelo, clique em **[!UICONTROL Desaprovar]** à direita do modelo.

>[!NOTE]
>
>Se você estiver aprovando o modelo que foi aprovado anteriormente e editado, sua segunda aprovação substituirá o modelo original.


## Status dos modelos

Você pode verificar o status na página de modelo sob o nome do modelo.

Os seguintes status estão disponíveis:

* **[!UICONTROL Particular]**: este modelo é visível somente para o autor do modelo e sua equipe.
* **[!UICONTROL Publicado]**: este modelo é visível somente para o autor do modelo e sua equipe. Depois de publicado, é possível enviar o modelo para aprovação, se desejado. Também é possível copiar um link compartilhável.
* **[!UICONTROL Aprovado]**: este modelo está visível para todos os usuários do Workfront Fusion na guia [!UICONTROL Modelos públicos]. Você também pode copiar um link compartilhável clicando em [!UICONTROL Opções] no canto superior direito da tela.

Você também pode verificar o status na guia [!UICONTROL Modelos de equipe]. Se um modelo for publicado, ele terá um ícone à direita do nome do modelo.

* **Ícone de olho**: o modelo foi publicado, está visível somente para a equipe e uma solicitação de aprovação não foi enviada.
* **Ícone de marca de seleção amarelo**: o modelo é publicado, está visível somente para a equipe e aguarda aprovação para ser adicionado à guia Modelos públicos.
* **Ícone de marca de seleção verde**: o modelo está disponível na guia Modelos públicos e está visível para qualquer usuário do Workfront Fusion. Ele também ainda está visível na guia [!UICONTROL Modelos de equipe]. O autor do modelo ou o membro da equipe ainda pode editá-lo.

Modelos sem ícones têm status [!UICONTROL Particular]. Eles não são publicados e são visíveis apenas para a equipe do.


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
