---
title: Visão geral de armazenamento
description: Armazenamento é uma página no Workfront Fusion que fornece às equipes acesso direto aos repositórios do Adobe Enterprise Storage Management (ESM), permitindo que os usuários naveguem em pastas, façam upload e download de arquivos, visualizem o histórico de versões e criem cenários de automação.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: d5568479d43bd5518adae5b66b132b4075e7f356
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 2%

---

# Visão geral de armazenamento

<!--Add to navigation articles once this goes to production-->

A área de armazenamento no Workfront Fusion fornece às equipes acesso direto aos repositórios ESM (Enterprise Storage Management, gerenciamento de armazenamento corporativo) da Adobe. Os usuários podem procurar pastas, carregar e baixar arquivos, visualizar o histórico de versões e criar cenários de automação, tudo sem sair do Fusion.

O armazenamento pertence a equipes e exige que a organização seja integrada ao Adobe Identity Management System (IMS) com acesso ao Adobe Storage.

Os arquivos no Fusion Storage são espelhados em Adobe Files (adobe.com/files), de modo que qualquer arquivo que possa ser acessado em Adobe Files pode ser acessado no Fusion Storage.

Para obter instruções sobre como usar o Armazenamento, consulte:

* [Inicializar armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md)
* [Exibir e gerenciar armazenamento no Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-and-manage-storage-in-workfront-fusion.md)
* [Fazer upload de arquivos para armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/upload-files-to-storage.md)
* [Baixar arquivos do Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/download-files-from-storage.md)
* [Excluir arquivos do Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/delete-files-from-storage.md)
* [Exibir histórico de versões do arquivo no Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-storage-file-version-history.md)
* [Criar cenários do Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md)

## Pré-requisitos de armazenamento

Para usar a área do Workfront Fusion Storage, o seguinte deve ser verdadeiro:

* A organização foi integrada ao **Adobe Identity Management System (IMS)**
* A organização tem o **Adobe Storage** disponível
* O usuário está conectado à **organização correta do Adobe IMS** (aquela que corresponde à organização selecionada do Fusion)
* A conta do usuário tem **acesso ao Adobe Storage**

## Glossário

Ao usar

| Termo | Definição |
| ------ | ----------- |
| **Repositório** | Um contêiner de armazenamento de nível superior no Adobe ESM, normalmente mapeado para um projeto ou espaço de trabalho |
| **Conexão** | Um link seguro entre o Fusion e o Adobe Storage, criado automaticamente durante a inicialização. Usa a autenticação do Adobe IMS com atualização automática de token |
| **ESM** | Gerenciamento de armazenamento corporativo, serviço de armazenamento de arquivos em nuvem da Adobe |
| **IMS** | Sistema Adobe Identity Management, plataforma de autenticação e identidade da Adobe |

<!--

## UI Reference — Key Screens

### 1. Initialization Screen

* Cloud icon with **"Adobe Storage"** heading
* Description text explaining the feature
* **"Initialize Storage"** button (primary action)
* Error variants for access restriction, org mismatch, access denied, no storage found

### 2. Repository List

* Table with **Name** and **Region** columns
* **"Open"** action button per row

### 3. File Browser

* Breadcrumb navigation bar
* **"Upload File"** dropdown button (with "Upload File" and "Upload File in Scenario" options)
* File/folder table with **Name**, **Type**, **Size**, **Created** columns
* Floating action bar on file selection with: **Download**, **Download in Scenario**, **Versions**, **Delete**
* Upload/download progress banners (top-right corner)

### 4. Version History Panel

* Right-side slide-out panel
* Version list with date, version badge, and download button per entry
* **"current"** label on the latest version

-->
