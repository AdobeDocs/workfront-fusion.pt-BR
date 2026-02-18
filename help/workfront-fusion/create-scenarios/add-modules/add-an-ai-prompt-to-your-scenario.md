---
title: Adicionar um prompt de IA ao seu cenário
description: Você pode incluir um prompt de IA no seu cenário que se conecta ao seu
author: Becky
feature: Workfront Fusion
source-git-commit: 09e8ca28c12990a699816671d07f85288d973bc7
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Adicionar um prompt de IA ao seu cenário

Você pode incluir um prompt de IA em seu cenário usando o Protocolo de contexto de modelo (MCP) combinado com modelos de idioma grandes (LLMs). Ao configurá-los no módulo Agente MCP, você pode usar inteligência artificial para configurar workflows que sejam eficientes, seguros e flexíveis.

>[!NOTE]
>
>Essa funcionalidade é separada da capacidade de adicionar módulos a um cenário usando IA.
>
>Para obter informações sobre como adicionar módulos com IA, consulte [Gerar um segmento de cenário usando IA](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-with-ai.md).

## Visão Geral do Protocolo de Contexto do Modelo

O protocolo de contexto de modelo (MCP) é uma maneira de conectar com segurança modelos de idioma de IA a outros aplicativos. Você configura servidores MCP, que permitem que o modelo de IA acesse o aplicativo. Em seguida, você pode enviar um prompt para o modelo de IA, que pode retornar informações do aplicativo.

Por exemplo, você pode configurar um servidor MCP para conectar um modelo de IA ao Gmail. Quando você envia o prompt &quot;Me dê meus últimos 5 emails do Gmail&quot; para o modelo de idioma grande, ele analisa esse prompt e o envia para o servidor MPC do Gmail, que pode acessar seu Gmail e retornar os emails.

O módulo Agente MCP permite processar um prompt de usuário usando um modelo de idioma e servidores MCP.

## Benefícios do uso do MCP em seus cenários de Fusão

O uso do MCP em seus cenários oferece os seguintes benefícios:

* O uso do MCP em seu cenário reduz a necessidade de analisar todas as situações e possíveis variações de uma ação. Ao usar um prompt, você elimina a necessidade de usar dados de regex ou análise para levar em conta essas variações.
* Você pode fornecer contexto ao prompt usando elementos mapeados de módulos anteriores ou outras funções no painel de mapeamento.
* O uso de um prompt pode ser mais eficiente e flexível do que criar um cenário com módulos específicos, pois ele pode usar o raciocínio no prompt e selecionar o melhor curso de ação no contexto disponível.
* Como você configura os servidores MCP aos quais o módulo pode se conectar, você controla a segurança desse servidor e pode ter certeza de que a segurança se adapta às necessidades de sua organização.

>[!NOTE]
>
>A funcionalidade disponível depende das ferramentas disponíveis no servidor MCP e não é controlada pelo Fusion.

## Adicionar um prompt de IA ao seu cenário

Você pode adicionar um prompt de IA ao cenário usando o módulo Agente MCP.

Para obter instruções, consulte [Módulo do agente MCP](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).
