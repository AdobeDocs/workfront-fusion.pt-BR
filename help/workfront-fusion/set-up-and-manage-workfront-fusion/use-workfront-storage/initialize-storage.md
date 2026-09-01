---
title: Inicializar armazenamento
description: Quando um usuário navega para o Armazenamento pela primeira vez, ele vê uma tela de inicialização que cria uma conexão segura com o Adobe Storage em nome da equipe.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 0%

---

# Inicializar Armazenamento no Workfront Fusion

A área do Fusion Storage deve ser inicializada para que você possa visualizar repositórios, pastas e arquivos no armazenamento em nuvem do Adobe.

Para obter uma visão geral do Armazenamento, consulte [Visão geral do Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

## Inicializar armazenamento

1. No Workfront Fusion, clique em **Armazenamento** na navegação à esquerda.
1. Clique em **Inicializar Armazenamento**.

O Fusion cria automaticamente uma conexão segura com o Adobe Storage em nome da equipe.

Depois que a conexão é estabelecida, o Fusion carrega os repositórios de armazenamento da equipe.

## Solução de problemas de inicialização

| Mensagem | Motivo | O que o usuário deve fazer |
| -------- | -------- | ------------------------ |
| **Acesso Restrito** | A organização não está integrada ao Adobe IMS. | Entre em contato com o administrador da organização para concluir a integração do IMS. |
| **Incompatibilidade de Organização** | O usuário está conectado a uma organização da Adobe diferente da selecionada no Fusion. | Saia e entre novamente com a organização correta do Adobe IMS. |
| **Acesso negado** | A conta do usuário não tem as permissões necessárias ou o Adobe Storage não está disponível para a organização. | Verifique as permissões da conta com o administrador da organização. Após resolver, clique em **Repetir**. |
| **Nenhum Armazenamento Encontrado** | A conexão foi estabelecida, mas nenhum repositório foi encontrado. | Verificar se o armazenamento da Adobe está provisionado para a organização. Depois de verificar, clique em **Carregar Armazenamento** para tentar novamente. |
