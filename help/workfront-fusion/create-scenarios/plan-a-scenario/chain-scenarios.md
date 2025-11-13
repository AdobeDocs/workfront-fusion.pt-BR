---
title: Encadear vários cenários em conjunto
description: É possível encadear cenários, permitindo que um cenário acione outro e retornando a saída de dados pelo segundo cenário para o primeiro.
author: Becky
feature: Workfront Fusion
exl-id: def8d4c1-fc20-4b93-b1fd-be2f60300464
source-git-commit: 7f73007e219714c38dd0cf29d2a1e3a4c8f6f3cc
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# Encadear vários cenários em conjunto

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

## Exibição do histórico de execução para cenários encadeados

Você pode exibir o histórico de execução de cenários encadeados ao exibir o histórico de cada cenário incluído na cadeia. Por exemplo, o histórico de execução do cenário principal incluiria informações sobre módulos e dados processados diretamente no cenário principal. Para exibir o histórico de execução de módulos e dados processados em um cenário filho, abra o cenário filho e exiba o histórico de execução.

Recomendamos usar o botão **Ir para o cenário filho** no módulo Chamar um cenário filho para ir rapidamente para o cenário filho, onde você pode visualizar seu histórico de execução. O cenário filho é aberto em outra janela do navegador, permitindo que você veja cenários pai e filho ao mesmo tempo.

![Ir para o botão de cenário filho](assets/go-to-the-child-button.png)

## Erros e execuções incompletas

### Tratamento de erros

Se ocorrer um erro no cenário filho, isso poderá afetar a transferência de dados de volta para o pai.

Recomendamos configurar o tratamento de erros no cenário filho para garantir que, se algo der errado, o cenário pai não fique parado aguardando a resposta do cenário filho.

## Práticas recomendadas

Considere as práticas recomendadas a seguir ao encadear um cenário.

### Evitar recursão ao encadear cenários

A recursão ocorre quando um cenário aciona uma nova execução de si mesmo, que aciona uma nova execução e assim por diante em um loop infinito.

A recursão pode causar problemas de desempenho para a organização proprietária do cenário recursivo e para outras organizações.

Ao encadear cenários, siga estas práticas para evitar recursão:

* Verifique se **os cenários filho não podem disparar o cenário pai**. Por exemplo, se um cenário principal for acionado quando uma solicitação for criada, verifique se os cenários secundários não criam solicitações.
* Certifique-se de que **os cenários filho não façam chamadas entre si**. Por exemplo, se o cenário-filho A chamar o cenário-filho B, certifique-se de que o cenário-filho B não chame o cenário-filho A.
* Verifique se **um cenário não pode chamar a si mesmo**. Por exemplo, um cenário é acionado quando uma tarefa é criada e esse cenário cria duas tarefas. As tarefas recém-criadas acionam o cenário novamente, o que cria quatro novas tarefas. Toda vez que uma tarefa é criada, o cenário é acionado e toda vez que o cenário é executado, o número de tarefas dobra. O número de tarefas aumenta exponencialmente.

>[!IMPORTANT]
>
>* **Quando um cenário está causando recursão, ele é desativado pela equipe de engenharia do Fusion para evitar mais problemas de desempenho.**
>* Como a recursão é um resultado do design do cenário, você deve projetar seus cenários de forma a garantir que o cenário não inclua ações que acionem o cenário.

### Use o tratamento de erros para garantir uma resposta

Como o cenário pai está aguardando uma resposta do cenário filho antes de poder continuar, você deve garantir que o cenário filho seja criado para que ele forneça uma resposta mesmo se encontrar um erro.
