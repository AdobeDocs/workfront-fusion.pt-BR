---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Atividade de lançamento do Workfront Fusion: semana de 7 de novembro de 2022'
description: Esta página descreve todos os aprimoramentos realizados no Adobe Workfront Fusion na semana de terça-feira, 7 de novembro de 2022.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 9d58abd0-1fe7-43c8-a1ea-2fadea738590
source-git-commit: 0e8f73afb2ab60bb1b601abf3c4f3d611e97d125
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 32%

---

# Atividade de lançamento do Workfront Fusion: semana de 7 de novembro de 2022

**Otimização da fila do Webhook**

A fila de webhook do Fusion foi otimizada com esta versão. O serviço que aceita webhooks agora está separado do enfileiramento e de outros processos. Essa alteração permite que o Fusion processe filas de webhook a uma taxa mais rápida e consistente.

Durante a implementação dessa alteração, foi possível entender melhor o tempo de processamento de log esperado para eventos de webhook na fila. Espera-se que a página do visualizador de webhook do Fusion não tenha mais de 1 minuto.

Para ver os eventos de webhook atualmente na fila, navegue até Webhooks, na navegação à esquerda. Os ícones de caminhão com um número no numerador indicam eventos de fila para esse webhook. Clique no ícone de caminhão para ver os eventos em fila.


**Os webhooks não utilizados agora serão desativados ou excluídos**

Fizemos algumas alterações no modo como o Workfront Fusion lida com webhooks não utilizados. Agora, os Webhooks são desativados automaticamente se qualquer uma das opções a seguir se aplicar:

* O webhook não foi conectado a nenhum cenário por mais de 5 dias.
* O webhook é usado somente em cenários inativos, que ficaram assim por mais de 30 dias.

Os webhooks desativados serão excluídos e removidos do registro automaticamente se não estiverem conectados a nenhum cenário e estiverem com o status desativado por mais de 30 dias.
