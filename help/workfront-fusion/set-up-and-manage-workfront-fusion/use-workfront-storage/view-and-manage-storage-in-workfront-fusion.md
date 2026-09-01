---
title: Exibir e gerenciar armazenamento no Workfront Fusion
description: A área de Armazenamento lista os repositórios disponíveis e permite que você navegue em pastas e arquivos.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 1%

---

# Exibir e gerenciar armazenamento no Workfront Fusion

A área de Armazenamento no Workfront Fusion permite visualizar e interagir com repositórios no armazenamento na nuvem do Adobe.

Para obter uma visão geral do Armazenamento, consulte [Visão geral do Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

>[!TIP]
>
>O armazenamento deve ser inicializado antes que você possa ver os repositórios. Para obter instruções, consulte [Inicializar Armazenamento](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md).

## Exibir repositórios, pastas e arquivos

1. No Workfront Fusion, clique em **Armazenamento** na navegação à esquerda.
Uma lista de repositórios é aberta.

   Se houver apenas um repositório disponível, ele será aberto diretamente.

1. Clique em **Abrir** em qualquer repositório para procurar seu conteúdo.

   A abertura de um repositório mostra Pastas no repositório.
1. Clique em uma pasta para abri-la e exibir seus Arquivos.
1. Para navegar de volta pela estrutura de pastas, clique na navegação estrutural.


>[!NOTE]
>
>Uma pasta vazia exibe a mensagem: *&quot;Esta pasta está vazia&quot;*

## Gerenciar várias conexões de armazenamento

Uma equipe pode ter várias conexões de armazenamento Adobe.

1. No Workfront Fusion, clique em **Armazenamento** na navegação à esquerda.
Quando houver várias conexões, as guias serão exibidas na parte superior da página Armazenamento, rotuladas com o nome de cada conexão.
1. Para alternar para os repositórios de uma conexão diferente, clique na guia dessa conexão.

Se uma conexão se tornar inválida, como se o token expirasse e não pudesse ser atualizado, ela seria automaticamente filtrada e não apareceria como uma guia. A atualização programada do token do Fusion mantém as conexões válidas automaticamente.

## Informações do arquivo

Cada arquivo na tabela mostra:

| Coluna | Descrição |
| -------- | ------------- |
| **Nome** | Nome de arquivo com um ícone de documento. |
| **Tipo** | Selo de extensão de arquivo, como PNG, PDF ou JPG. |
| **Tamanho** | Tamanho do arquivo. Mostra *&quot;Processando...&quot;* se o arquivo foi carregado recentemente e o back-end ainda o está processando. |
| **Criado** | Data de criação. |

Os arquivos também mostram um **selo de versão** (por exemplo, `v2`, `v3`) quando existem várias versões.

## Controles de tabela

* **Pesquisar/filtrar**: filtre arquivos por nome usando a barra de pesquisa global.
* **Classificação**: clique nos cabeçalhos da coluna para classificar.
* **Paginação**: escolha 10, 25, 50 ou 100 itens por página. O padrão é 25.
