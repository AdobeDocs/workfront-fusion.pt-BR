---
title: Métodos de solicitação HTTP
description: Ao configurar uma chamada de API em um módulo do, você deve selecionar o método de solicitação HTTP. Este artigo descreve os métodos disponíveis e por que você selecionaria cada um deles.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
TQID: https://experienceleague.adobe.com/Z11y3dk6PtoN11Gja8S2ZyJlTJZNZfXfcPPrNJWvbRk
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 303
ht-degree: 1%

---

# Métodos de solicitação HTTP

Ao configurar uma chamada de API em um módulo do, você deve selecionar o método de solicitação HTTP. Este artigo descreve os métodos disponíveis e por que você selecionaria cada um deles.

## Métodos HTTP

Use um dos seguintes métodos HTTP.

* **[!UICONTROL GET]**: recupera dados de um servidor Web com base em seus parâmetros. [!UICONTROL GET] solicita uma representação do recurso especificado e recebe uma mensagem de resposta [!UICONTROL 200 OK] com o conteúdo solicitado se for bem-sucedido.
* **[!UICONTROL POST]**: envia dados para um servidor Web com base em seus parâmetros. As solicitações [!UICONTROL POST] incluem ações como carregar um arquivo. Várias [!UICONTROL PUBLICAÇÕES]s podem resultar em um resultado diferente de uma única [!UICONTROL PUBLICAÇÃO]. Portanto, tenha cuidado ao enviar várias [!UICONTROL PUBLICAÇÕES]s involuntariamente. Se uma [!UICONTROL POSTAGEM] for bem-sucedida, você receberá uma mensagem de resposta [!UICONTROL 200 OK].
* **[!UICONTROL PUT]**: envia dados para um local no servidor Web com base em seus parâmetros. As solicitações [!UICONTROL PUT] incluem ações como carregar um arquivo. A diferença entre um [!UICONTROL PUT] e [!UICONTROL POST] é que PUT é idempotente, o que significa que o resultado de um único [!UICONTROL PUT] bem-sucedido é o mesmo que muitos [!UICONTROL PUT]s idênticos. Se um PUT for bem-sucedido, você receberá uma mensagem de resposta 200 (geralmente 201 ou 204).
* **[!UICONTROL PATCH]**: (não disponível para alguns módulos de chamada de API) Aplica modificações parciais a um recurso em um servidor Web com base em seus parâmetros. [!UICONTROL PATCH] não é idempotente, o que significa que o resultado de vários [!UICONTROL PATCH]&#39;s pode ter consequências não intencionais. Se um [!UICONTROL PATCH] for bem-sucedido, você receberá uma mensagem de resposta 200 (normalmente 204).
* **[!UICONTROL DELETE]**: exclui o recurso especificado do servidor Web com base em seus parâmetros (se o recurso existir). Se um [!UICONTROL DELETE] for bem-sucedido, você receberá uma mensagem de resposta 200 OK.
