---
title: fila de k
description: Muitos serviços fornecem webhooks para fornecer notificações instantâneas sempre que uma determinada alteração ocorrer no serviço. Os acionadores instantâneos, também conhecidos como webhooks, podem usar esses eventos para iniciar cenários. Os eventos entram na fila do webhook enquanto aguardam o processamento, por exemplo, quando o cenário já está em execução. Você pode exibir a fila do webhook.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---

# Exibir a fila de um webhook

Muitos serviços fornecem webhooks para fornecer notificações instantâneas sempre que uma determinada alteração ocorrer no serviço. Os acionadores instantâneos, também conhecidos como webhooks, podem usar esses eventos para iniciar cenários. Os eventos entram na fila do webhook enquanto aguardam o processamento, por exemplo, quando o cenário já está em execução. Você pode exibir a fila do webhook.

Os dados de entrada do webhook são sempre armazenados na fila, independentemente de como você definiu a opção Dados são confidenciais no painel de configurações do cenário. Depois que os dados forem processados em um cenário, eles serão excluídos permanentemente da fila.

Para obter mais informações sobre webhooks, consulte [Acionadores instantâneos (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacote</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença</td> 
   <td> <p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou plano do [!UICONTROL Prime] [!DNL Workfront]: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plano: [!DNL Workfront Fusion] está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Exibir a fila de um webhook

Todas as mensagens de webhooks recebidos são armazenadas na fila do webhook.

Se um cenário tiver uma fila no momento, um banner será exibido nesse cenário:

![Banner da fila](assets/queue-banner.png)

Para exibir a fila de um webhook:

1. Clique em **[!UICONTROL Webhooks]** no menu à esquerda.
1. Localize o Webhook no qual deseja exibir a fila.
1. Localize o número de eventos no botão Events received.

   ![Fila do Webhook](assets/webhook-queue.png)

1. Clique no botão para exibir detalhes sobre eventos na fila.
