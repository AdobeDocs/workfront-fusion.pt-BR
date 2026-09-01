---
title: Fazer upload de arquivos para armazenamento
description: Você pode fazer upload de arquivos diretamente para uma pasta no Armazenamento ou criar um cenário de automação para lidar com o upload.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 196
ht-degree: 2%

---

# Fazer upload de arquivos para armazenamento

Você pode fazer upload de um arquivo para o Adobe Cloud Storage de dentro do Workfront Fusion usando a área Armazenamento.

O upload está disponível ao navegar dentro de uma pasta (não na lista de pastas de nível superior).

* Para obter uma visão geral do Armazenamento, consulte [Visão geral do Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).
* Para obter instruções sobre como criar um cenário de carregamento, consulte [Criar cenários do Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md).


## Fazer upload de um arquivo

1. No Workfront Fusion, clique em **Armazenamento** na navegação à esquerda.
1. Navegue até o repositório e a pasta em que deseja fazer upload de um arquivo.
1. Clique no botão suspenso **&quot;Carregar Arquivo&quot;**.
1. Selecione **&quot;Carregar Arquivo&quot;** para carregar diretamente.

   Um seletor de arquivos é aberto.
1. Selecione o arquivo a ser carregado.

   Um **banner de progresso** aparece no canto superior direito mostrando:

   * Nome do arquivo
   * Porcentagem de progresso do upload
   * Bytes transferidos
   * Um botão **Cancelar** para interromper o carregamento

Após o upload, o arquivo é exibido na lista de pastas. A coluna **Size** pode mostrar temporariamente *&quot;Processing...&quot;* enquanto o Adobe Storage processa o arquivo no back-end. O tamanho real do arquivo é exibido após a conclusão do processamento. Isso pode ser verificado atualizando a página.

## Limites de upload

* Tamanho máximo do arquivo: **5 GB**.

