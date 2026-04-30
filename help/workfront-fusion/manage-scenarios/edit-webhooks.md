---
title: Editar Webhooks
description: É possível editar webhooks existentes para os conectores do Workfront e do Workfront Planning.
author: Becky
feature: Workfront Fusion
source-git-commit: 2561c911b9b542a7b143fae745baf4e1de45be38
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 4%

---

# Editar webhooks

É possível editar webhooks existentes. Os cenários que usam esses webhooks usarão a nova configuração a partir de agora, o que elimina a necessidade de criar um novo webhook e atribuí-lo manualmente a todos os cenários afetados.

Os webhooks podem ser editados somente para os seguintes conectores:

* Workfront
* Workfront Planning

>[!IMPORTANT]
>
>Considere o seguinte ao atualizar um webhook:
>
>* O webhook editado é tratado pelas assinaturas de evento do Workfront como uma nova assinatura. O histórico de assinaturas do evento não é preservado para a configuração de webhook anterior, pois essa é considerada uma assinatura de evento separada.
>* A alternância da assinatura de evento antiga para a nova pode não estar perfeitamente sincronizada. Portanto, é possível receber um evento duas vezes (se a nova assinatura começar a ser executada antes da antiga) ou perder um evento (se a assinatura antiga for interrompida antes da nova começar a ser executada).

## Editar um webhook

É possível editar webhooks a partir de um cenário ou da lista Webhooks.

### Editar um webhook em um cenário

>[!NOTE]
>
>Essa funcionalidade só está disponível para cenários que têm um módulo de acionador instantâneo do Workfront ou do Workfront Planning.

1. Vá para o cenário que inclui o webhook que deseja editar.
1. No módulo do acionador do cenário, clique na lista suspensa ao lado do campo Webhook e selecione **Editar item**.

   A janela de configuração do webhook é aberta, preenchida com a configuração existente.

1. Faça as edições desejadas no webhook.
1. Clique em **Salvar** para salvar o webhook e retornar ao módulo.

### Editar um webhook na lista Webhooks

1. Na navegação à esquerda, selecione **Webhooks** ![ícone de Webhooks](assets/webhooks-icon.png).
1. Clique na caixa de seleção ao lado do webhook que deseja editar.
1. No banner azul na parte inferior da tela, clique em **Editar**.
1. Faça as edições desejadas no webhook.
1. Clique em **Salvar** para salvar o webhook e retornar à lista de Webhooks.

