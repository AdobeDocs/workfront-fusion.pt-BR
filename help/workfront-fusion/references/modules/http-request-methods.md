---
title: métodos de solicitação HTTP
description: Ao configurar uma chamada de API em um módulo do, você deve selecionar o método de solicitação HTTP. Este artigo descreve os métodos disponíveis e por que você selecionaria cada um deles.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# métodos de solicitação HTTP

Ao configurar uma chamada de API em um módulo do, você deve selecionar o método de solicitação HTTP. Este artigo descreve os métodos disponíveis e por que você selecionaria cada um deles.

## Métodos HTTP

Use um dos seguintes métodos HTTP.

* **[!UICONTROL GET]**: Recupera dados de um servidor Web com base em seus parâmetros. [!UICONTROL GET] solicita uma representação do recurso especificado e, em caso de sucesso, recebe uma mensagem de resposta [!UICONTROL 200 OK] com o conteúdo solicitado.
* **[!UICONTROL POST]**: Envia dados para um servidor Web com base em seus parâmetros. [!UICONTROL POST] solicitações incluem ações como carregar um arquivo. Vários [!UICONTROL POST]s podem resultar em um resultado diferente de um único [!UICONTROL POST]. Portanto, tenha cuidado ao enviar vários [!UICONTROL POST]s involuntariamente. Se um [!UICONTROL POST] for bem-sucedido, você receberá uma mensagem de resposta [!UICONTROL 200 OK].
* **[!UICONTROL PUT]**: Envia dados para um local no servidor Web com base em seus parâmetros. [!UICONTROL PUT] solicitações incluem ações como carregar um arquivo. A diferença entre um [!UICONTROL PUT] e [!UICONTROL POST] é que o PUT é idempotente, o que significa que o resultado de um único [!UICONTROL PUT] bem-sucedido é o mesmo que muitos [!UICONTROL PUT]s idênticos. Se um PUT for bem-sucedido, você receberá uma mensagem de resposta 200 (geralmente 201 ou 204).
* **[!UICONTROL PATCH]**: (Não disponível para alguns módulos de chamada de API) Aplica modificações parciais a um recurso em um servidor Web com base em seus parâmetros. [!UICONTROL PATCH] não é idempotente, o que significa que o resultado de vários [!UICONTROL PATCH]&#39;s pode ter consequências não intencionais. Se um [!UICONTROL PATCH] for bem-sucedido, você receberá uma mensagem de resposta 200 (normalmente 204).
* **[!UICONTROL DELETE]**: exclui o recurso especificado do servidor Web com base em seus parâmetros (se o recurso existir). Se um [!UICONTROL DELETE] for bem-sucedido, você receberá uma mensagem de resposta 200 OK.
