---
title: Encadear vários cenários em conjunto
description: É possível encadear cenários, permitindo que um cenário acione outro e retornando a saída de dados pelo segundo cenário para o primeiro.
author: Becky
feature: Workfront Fusion
exl-id: def8d4c1-fc20-4b93-b1fd-be2f60300464
source-git-commit: 0390bb875eb10278967d7d1c9cd61e5243e5f37e
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 12%

---

# Encadear vários cenários juntos

>[!NOTE]
>
>Este recurso atualmente está no Beta.

É possível encadear cenários, permitindo que um cenário acione outro e retornando a saída de dados pelo segundo cenário para o primeiro. Isso permite a criação de cenários mais modulares, em que você não precisa duplicar seções de cenário em vários cenários.

Você pode chamar vários cenários filho de um cenário pai e chamar um cenário filho de vários cenários pai. Você também pode aninhar cenários filhos, chamando um do outro.

Quando um cenário pai está aguardando que um cenário filho retorne dados, esse tempo não é contabilizado em relação ao tempo limite do cenário pai. Por exemplo, um cenário pai chama cinco cenários filhos, cada um leva 10 minutos para ser executado, para um total de 50 minutos. Os módulos no próprio cenário pai levam 15 minutos para serem executados. O cenário principal não atinge o tempo limite, mesmo que um total de 65 minutos tenha passado, o que está acima do tempo limite de 40 minutos.

Para obter mais informações sobre as medidas de proteção de desempenho do Fusion, incluindo tempos limite, consulte [Medidas de proteção de desempenho do Fusion](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md).

Para obter instruções sobre como configurar módulos de Cadeia, consulte [Módulos de Cadeia](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Cenários pai e filho

* O cenário **pai** chama outro cenário, usando o módulo **Cadeia** > **Chamar um cenário filho**. Ele recebe a saída do cenário filho, que pode ser processada em módulos de cenário posteriores.
* O cenário **filho** é chamado pelo cenário pai. Seu módulo de acionamento recebe dados do cenário principal e retorna a saída para o cenário principal.

O cenário pai requer uma resposta do cenário filho. No momento, não há suporte para cenários secundários que não retornam dados.

## Estruturas de dados em cenários encadeados

O Workfront Fusion usa estruturas de dados para transferir informações do cenário principal para o cenário secundário. A estrutura de dados é configurada no cenário filho. Quando o cenário filho é selecionado no cenário pai, os campos da estrutura de dados usada como entrada do cenário filho aparecem no cenário pai. Você pode mapear valores para esses campos, que são passados para o cenário filho quando ele é acionado.

Para obter informações sobre os módulos a serem configurados nos cenários pai e filho, consulte [Módulos de cadeia](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

Para obter informações sobre estruturas de dados, consulte [Estruturas de dados](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

## Fluxo de dados

1. Os dados fluem pelo cenário principal.
1. Os dados atingem o módulo Chamar um cenário filho. Os dados são mapeados para os campos no módulo Chamar um cenário filho, que correspondem aos campos na estrutura de dados usada no módulo de acionador do cenário filho.
1. Os dados do cenário Chamar um filho são passados para o cenário filho.
1. O cenário filho processa dados e executa ações.
1. O cenário filho termina com a resposta de Retorno ao módulo pai.
1. A saída da resposta de Retorno para o módulo pai é passada para o cenário pai.
1. A saída do cenário Chamar um filho é a saída do cenário filho. Essa saída pode ser processada posteriormente no cenário principal.

## Casos de uso

Considere os seguintes exemplos de casos de uso para cenários de encadeamento:

* **Lógica reutilizável**: você pode encadear cenários para ações repetidas usadas em vários cenários. Por exemplo, se houver vários cenários que arquivam conteúdo, você poderá criar um único cenário filho chamado &quot;Arquivar conteúdo&quot;, que poderá ser usado como um cenário filho para qualquer fluxo de trabalho que arquive conteúdo.

* **Tratamento de erros**: é comum que as organizações tenham as mesmas ações de tratamento de erros em vários cenários, como uma rota de tratamento de erros que envia um log de erros para um armazenamento de dados e cria uma notificação do Slack. Você pode criar um cenário filho com essas ações e encadear esse cenário nas rotas de tratamento de erros em vários cenários.

* **Tempo de extensão**: você pode usar o encadeamento para operações em lotes grandes com ações de longa execução, como quando exportar e importar arquivos. Essa operação leva algum tempo se houver muitos arquivos. Como os cenários filho não contam com o tempo limite do cenário pai, você pode exceder o tempo de execução usando vários cenários filho para exportar ou importar os arquivos.

* **Substituir iteradores** Substituir iteradores por cenários filho pode reduzir o uso de memória, como em operações complexas em uma iteração que causa erro de falta de memória. Você pode criar um cenário separado para a operação complexa e substituir o iterador por um módulo de cenário Chamar um filho

* **Procurar e criar um registro**: por exemplo, você pode criar um cenário que procure um usuário. Se existirem, o cenário os adicionará como aprovador com acesso que eles precisam revisar e aprovar. Se não existirem, o cenário criará uma solicitação para o administrador integrar um novo usuário.

## Viewing execution history for chained scenarios

You can view execution history for chained scenarios by viewing the history of each scenario included in the chain. For example, the parent scenario&#39;s execution history would include information about modules and data processed directly in the parent scenario. To view execution history for modules and data processed in a child scenario, open the child scenario and view the execution history there.

We recommend using the **Go to the child scenario** button in the Call a child scenario module to quickly go to the child scenario, where you can view its execution history. The child scenario opens in another browser window, allowing you to see parent and child scenarios at the same time.

![Go to the child scenario button](assets/go-to-the-child-button.png)

## Errors and incomplete executions

### Tratamento de erros

If the child scenario errors out, that may affect getting data back to your parent.

We recommend configuring error handling in the child scenario to ensure that if something goes wrong in the child scenario, the parent scenario is not stuck waiting for the response from the child scenario.

## Práticas recomendadas

Consider the following best practices when chaining a scenario.

### Avoid recursion when chaining scenarios

A recursão ocorre quando um cenário aciona uma nova execução de si mesmo, que aciona uma nova execução, e assim por diante em um loop infinito.

A recursão pode causar problemas de desempenho tanto para a organização responsável pelo cenário recursivo quanto para outras organizações.

When chaining scenarios, follow these practices to avoid recursion:

* Ensure that **child scenarios cannot trigger the parent scenario**. For example, if a parent scenario is triggered when a request is created, ensure that the child scenarios do not create requests.
* Ensure that **child scenarios do not call each other**. For example, If child scenario A calls child scenario B, ensure that child scenario B does not call child scenario A.
* Ensure that **a scenario cannot call itself**. Por exemplo, um cenário é acionado quando uma tarefa é criada e esse cenário cria duas tarefas. As tarefas recém-criadas acionam o cenário novamente, criando quatro novas tarefas. Toda vez que uma tarefa é criada, o cenário é acionado, e toda vez que o cenário é executado, o número de tarefas dobra. O número de tarefas aumenta exponencialmente.

>[!IMPORTANT]
>
>* **Quando um cenário está causando recursão, ele é desativado pela equipe de engenharia do Fusion para evitar mais problemas de desempenho.**
>* Como a recursão é resultado do próprio design do cenário, é preciso projetar os cenários de forma que eles não incluam ações que acionem o próprio cenário.
>* You can view a diagram of the relationships between parent and child scenarios.
>   For instructions, see [View chained scenario relationships](/help/workfront-fusion/manage-scenarios/view-chained-scenario-relationships.md).

### Use error handling to ensure a response

Because the parent scenario is waiting for a response from the child scenario before it can continue, you must ensure that the child scenario is built so that it will provide a response even if it encounters an error.
