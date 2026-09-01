---
title: Criar cenários do Armazenamento
description: O armazenamento integra-se ao criador de cenários do Fusion, para que você possa criar cenários pré-configurados diretamente da página Armazenamento para baixar ou fazer upload de arquivos.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: aef1685cb25c0cdcb0dcdf9b0c73fb482d392e5f
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# Criar cenários do Armazenamento

Para obter uma visão geral do Armazenamento, consulte [Visão geral do Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

O armazenamento integra-se ao construtor de cenários do Fusion. Na página Armazenamento, os usuários podem criar um cenário que fará o download do arquivo selecionado.

## Baixar em Cenário

1. No Workfront Fusion, clique em **Armazenamento** na navegação à esquerda.
1. Navegue até o repositório que contém o arquivo que você deseja baixar em um cenário.
1. Selecione um arquivo e clique em **&quot;Baixar no Cenário&quot;** na barra de ações.

O Fusion cria um novo cenário chamado **&quot;Download {fileName}&quot;**. Esse cenário é aberto em uma guia do navegador separada.

O cenário é pré-configurado com:

* A conexão ativa.
* O repositório, pasta e arquivo pré-selecionados.
* Um módulo para gerar um URL de download pré-assinado.
* Um módulo HTTP para buscar o arquivo desse URL.
* Um intervalo de agendamento padrão de 15 minutos.

## Fazer upload de arquivo no cenário

1. No Workfront Fusion, clique em **Armazenamento** na navegação à esquerda.
1. Navegue até o repositório e a pasta que contém o arquivo que você deseja baixar em um cenário.
1. Ao navegar dentro de uma pasta, clique na lista suspensa **&quot;Carregar Arquivo&quot;**.
1. Selecione **&quot;Carregar Arquivo no Cenário&quot;**.

O Fusion cria um novo cenário chamado **&quot;Carregar para {folderName}&quot;**. Esse cenário é aberto em uma nova guia do navegador. Você deve adicionar módulos para fornecer o arquivo que deseja fazer upload, como o módulo Workfront > Baixar documento.

O cenário é pré-configurado com:

* A conexão ativa.
* O repositório e a pasta pré-selecionados.
* Um módulo para gerar um URL de upload pré-assinado com um nome de arquivo de espaço reservado.
* Um intervalo de agendamento padrão de 15 minutos.

