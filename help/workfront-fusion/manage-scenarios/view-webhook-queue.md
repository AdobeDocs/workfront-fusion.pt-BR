---
title: fila de k
description: Muitos serviços fornecem webhooks para fornecer notificações instantâneas sempre que uma determinada alteração ocorrer no serviço. Os acionadores instantâneos, também conhecidos como webhooks, podem usar esses eventos para iniciar cenários. Os eventos entram na fila do webhook enquanto aguardam o processamento, por exemplo, quando o cenário já está em execução. Você pode exibir a fila do webhook.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Exibir a fila de um webhook

Muitos serviços fornecem webhooks para fornecer notificações instantâneas sempre que uma determinada alteração ocorrer no serviço. Os acionadores instantâneos, também conhecidos como webhooks, podem usar esses eventos para iniciar cenários. Os eventos entram na fila do webhook enquanto aguardam o processamento, por exemplo, quando o cenário já está em execução. Você pode exibir a fila do webhook.

Os dados de entrada do webhook são sempre armazenados na fila, independentemente de como você definiu a opção Dados são confidenciais no painel de configurações do cenário. Depois que os dados forem processados em um cenário, eles serão excluídos permanentemente da fila.

Para obter mais informações sobre webhooks, consulte [Acionadores instantâneos (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote de Automação e Integração do Adobe Workfront</p><p>Workfront Ultimate</p><p>Workfront Prime e pacotes Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Standard</p><p>Trabalhar ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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
