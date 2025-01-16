---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Atividade de lançamento do Workfront Fusion: semana de 16 de novembro de 2020'
description: Esta página descreve todas as melhorias feitas no Adobe Workfront Fusion na semana de 16 de novembro de 2020.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 69e4a458-fd32-4dcd-be43-19a9467cf678
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Atividade de lançamento do Workfront Fusion: semana de 16 de novembro de 2020

Esta página descreve todas as melhorias feitas no Adobe Workfront Fusion na semana de 16 de novembro de 2020.

Para obter uma lista de todas as alterações recentes, consulte [atividade de versão do Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Para obter uma lista de correções de erros recentes no Workfront Fusion, consulte a página [Atualizações de Manutenção do Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) e verifique se há atualizações rotuladas como Atualização de Manutenção do Workfront Fusion.

## Atualizações do conector do Jira Cloud

Para expandir as maneiras de usar o conector Jira Cloud, adicionamos três novos módulos:

* Adicionar problema ao sprint
* Listar Registros
* Procurar Registros

Também atualizamos módulos existentes para oferecer suporte ao tipo de objeto &quot;Sprint&quot;. Anteriormente, o objeto &quot;Sprint&quot; só podia ser acessado por meio do módulo Chamada de API personalizada.

## A ID de execução agora está disponível para mapeamento em cenários

A ID de execução de um cenário agora está disponível no painel de mapeamento. Essa ID representa uma execução específica do cenário e pode ser usada como metadados. Por exemplo, a ID de execução pode ser salva com um registro que o Fusion cria, para que você possa determinar posteriormente qual execução do Fusion criou o registro. Você pode encontrar a ID de execução no painel de mapeamento em Funções gerais.

## Atalhos de teclado para cenários do Workfront Fusion 2.0

Para tornar a criação de cenários mais conveniente, adicionamos alguns atalhos de teclado:

* Ctrl/Cmd+Shift+Enter: executar um cenário uma vez
* Ctrl/Cmd + Shift + S: salvar um cenário

## Atualizações do conector para Office 365 Excel

Para expandir as maneiras de usar o conector do Excel do Office 365, adicionamos alguns novos módulos. Agora é possível:

* Acionar um módulo de alterações em pastas de trabalho
* Pesquisar ou baixar pastas de trabalho
* Listar planilhas, linhas de planilha, tabelas ou linhas de tabela
* Atualizar uma tabela ou linha de planilha
* Excluir uma linha de tabela ou planilha
* Recuperar metadados de uma tabela
* Fazer uma chamada de API personalizada

Os módulos disponíveis anteriormente ainda estão presentes no aplicativo.


## Usar o OAuth 2.0 em suas conexões com o aplicativo Workfront

Atualizamos o conector do Workfront para usar o OAuth 2.0. Essa atualização significa que é mais fácil fazer alterações nas conexões do aplicativo Workfront. Por exemplo, se algo sobre sua conexão for alterado (como uma senha), você não precisará mais atualizar cada conexão individual em seus cenários. Além disso, o OAuth2 oferece outros benefícios, como a segurança aprimorada e a capacidade de usar o Logon único (SSO).

As conexões existentes não exigem alterações no momento. No entanto, você pode reautorizar conexões existentes se quiser aproveitar os benefícios do OAuth 2.0.
