---
title: Proteções de Desempenho de Fusão
description: A automação de trabalho requer processamento rápido, de modo que o Adobe Workfront Fusion é projetado para alto desempenho. Como cenários de longa duração podem retardar o ritmo do seu trabalho, projetamos o Workfront Fusion com medidas de proteção que preservam o desempenho e limitam o tempo de execução, o tamanho dos dados e outros parâmetros de cenário. Os designers do Workfront Fusion devem estar cientes dessas medidas de proteção e incorporá-las às suas práticas de design.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
source-git-commit: 3a05e5df36bf9b1aacd0611fdad0240c8c52368d
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Medidas de proteção do desempenho de fusão

A automação de trabalho requer processamento rápido, de modo que o Adobe Workfront Fusion é projetado para alto desempenho. Como cenários de longa duração podem retardar o ritmo do seu trabalho, projetamos o Workfront Fusion com medidas de proteção que preservam o desempenho e limitam o tempo de execução, o tamanho dos dados e outros parâmetros de cenário. Os designers do Workfront Fusion devem estar cientes dessas medidas de proteção e incorporá-las às suas práticas de design.

## Navegadores

* O Workfront Fusion é compatível apenas com navegadores baseados em Chrome.

## Cenários

* O tempo limite de execução de cenário padrão é de **40 minutos**. Quando a execução atinge esse tempo limite, o Workfront Fusion interrompe a execução do cenário após o próximo ciclo ou operação, dependendo do cenário. Isso força o cenário a parar logo após o limite de 40 minutos ser atingido

  Os cenários de encadeamento não contam para o tempo limite de execução do cenário. Um cenário pai não acumula tempo enquanto aguarda a execução de um cenário filho.
* O tamanho máximo de um blueprint do cenário é **5 MB**, mas recomendamos manter o tamanho do cenário abaixo de **3 MB**.

  Os módulos do aplicativo que criam ou atualizam dados com um grande número de campos podem causar blueprints muito grandes.

   * Ao usar o aplicativo Workfront, selecione apenas os campos necessários para criar ou atualizar casos de uso.
   * Ao usar outros aplicativos, use módulos de API personalizados para interagir com qualquer tipo de registro que tenha um grande número de campos.

* Embora não haja limite para o número de módulos em um cenário, cenários com mais de 150 módulos afetam negativamente o desempenho do seu sistema Workfront Fusion. Por esse motivo, não recomendamos criar cenários com mais de 150 módulos.

## Operações

* O tempo limite da operação padrão geralmente é de **40 segundos**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## Arquivos

* A capacidade total de processamento do Fusion para arquivos é de **1 GB**. O limite se baseia em um custo total de memória. Cada operação contribui para esse custo. Se um único arquivo de 400 MB for baixado e carregado, o custo total da capacidade do arquivo será de 800 MB.
* As organizações no plano Workfront Ultimate têm acesso a um maior processamento de arquivos além de 1 GB. No entanto, há outros fatores que afetam a transferência de dados. O serviço ao qual o Fusion está se conectando pode limitar o tamanho do arquivo, o que afetaria quaisquer arquivos processados por esse serviço. Além disso, arquivos grandes podem afetar o tempo de execução do cenário. O Fusion processará os arquivos até que o limite de execução de 40 minutos seja atingido, momento em que a execução falhará.
* Se um arquivo for baixado usando um módulo que suporte arquivos grandes e, em seguida, for passado para um módulo que não suporta arquivos grandes, esse módulo não processará o arquivo com êxito. Arquivos grandes devem ser manipulados exclusivamente com módulos compatíveis durante todo o fluxo de trabalho.
* Os módulos que não oferecem suporte a arquivos grandes podem processar arquivos de até **200 MB**.

Para obter mais informações, consulte [Trabalhando com arquivos grandes](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Uso de Memória do Servidor

* O uso de memória do servidor para uma única execução é limitado a **1 GB**.

  Muitos fatores, como arquivos grandes ou módulos complexos, podem afetar o uso da memória do servidor de maneiras difíceis de prever ou controlar. Por esse motivo, a execução do cenário pode exceder o limite de memória de 1 GB, mesmo que o cenário siga todas as outras medidas de proteção de desempenho. Exceder o limite de memória causa falha na execução.

## Webhooks

* O tamanho máximo padrão de uma carga é **5 MB**.
* Os webhooks estão limitados a **100 solicitações por segundo**. Quando esse limite é atingido, o Workfront Fusion envia um status 429 ([!UICONTROL Muitas solicitações]).
* O Workfront Fusion armazena cargas de webhook por 30 dias. O acesso a uma carga de webhook por mais de 30 dias após seu recebimento resulta no erro &quot;[!UICONTROL Falha ao ler o arquivo do armazenamento.]&quot;
* Os webhooks são desativados automaticamente se qualquer uma das seguintes situações se aplicar:

   * O webhook não foi conectado a nenhum cenário por mais de 5 dias
   * O webhook é usado somente em cenários inativos, que ficaram inativos por mais de 30 dias.

* Os webhooks desativados são excluídos e não registrados automaticamente se não estiverem conectados a nenhum cenário e estiverem com o status desativado por mais de 30 dias.
* O tempo limite para uma resposta de webhook é de 5 minutos.

## Histórico de execução

* Os logs do histórico de execução são limitados ao tamanho de **100 MB**. Se o histórico de execução exceder esse tamanho, somente os primeiros 100 MB serão exibidos.
* Se um cenário tiver várias execuções simultâneas, apenas 5 execuções serão exibidas na área Execuções da página de detalhes do cenário. Isso é verdade mesmo quando mais de 5 execuções estão em andamento.

## Execuções incompletas

* As execuções incompletas estão limitadas a um tamanho total de **10 MB** por cenário. Se o limite de 10 MB for atingido, não serão armazenadas mais execuções incompletas para esse cenário.
* As execuções incompletas estão limitadas a um tamanho total de **500 MB** por equipe. Se o limite de 500 MB for atingido, não serão armazenadas mais execuções incompletas para essa equipe.
* O Workfront Fusion permite até 5 falhas por minuto.

## Tentativas

* Ao usar o módulo Break e especificar a diretiva Retry, se um cenário falhar consecutivamente 10 vezes em um período de 2 minutos, o cenário será desativado automaticamente.

## Recursão

A recursão ocorre quando um cenário aciona uma nova execução de si mesmo, que aciona uma nova execução e assim por diante em um loop infinito.

Por exemplo, um cenário é acionado quando uma tarefa é criada e esse cenário cria duas tarefas. As tarefas recém-criadas acionam o cenário novamente, o que cria quatro novas tarefas. Toda vez que uma tarefa é criada, o cenário é acionado e toda vez que o cenário é executado, o número de tarefas dobra. O número de tarefas aumenta exponencialmente.

A recursão pode causar problemas de desempenho para a organização proprietária do cenário recursivo e para outras organizações.

Considere o seguinte em relação à recursão:

* **Quando um cenário está causando recursão, ele é desativado pela equipe de engenharia do Fusion para evitar mais problemas de desempenho.**
* Como a recursão é um resultado do design do cenário, você deve projetar seus cenários de forma a garantir que o cenário não inclua ações que acionem o cenário.

## TLS

* O Fusion atualmente é compatível com a versão 1.2 do TLS por padrão.
* O Fusion pode usar o TLS 1.3 para solicitações HTTPS de saída se o TLS 1.3 estiver habilitado para o serviço de destino.
* O Fusion é compatível com TLS 1.2 e TLS 1.3 para solicitações HTTPS de entrada para Webhooks.
* As organizações podem solicitar que a versão 1.3 do TLS seja habilitada para sua instância do Fusion.

>[!NOTE]
>
> Se você estiver se conectando ao Workfront, saiba que essa funcionalidade TLS está habilitada no Workfront para chamadas a domínios que têm o formato `https://<domain>.my.workfront.com`.
