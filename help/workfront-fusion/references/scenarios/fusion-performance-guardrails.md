---
title: Medidas de proteção do desempenho do Fusion
description: A automação do trabalho requer processamento rápido, por isso o Adobe Workfront Fusion foi projetado para alto desempenho. Como cenários de longa duração podem diminuir o ritmo do trabalho, o Workfront Fusion foi projetado com medidas de proteção que preservam o desempenho e limitam o tempo de execução, o tamanho dos dados e outros parâmetros do cenário. Os designers do Workfront Fusion devem estar cientes dessas medidas de proteção e devem incorporá-las às suas práticas de design.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
source-git-commit: 441b192d50e928ce74e54d8bcc0d89f4af348bb5
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 96%

---

# Medidas de proteção do desempenho do Fusion

A automação do trabalho requer processamento rápido, por isso o Adobe Workfront Fusion foi projetado para alto desempenho. Como cenários de longa duração podem diminuir o ritmo do trabalho, o Workfront Fusion foi projetado com medidas de proteção que preservam o desempenho e limitam o tempo de execução, o tamanho dos dados e outros parâmetros do cenário. Os designers do Workfront Fusion devem estar cientes dessas medidas de proteção e devem incorporá-las às suas práticas de design.

## Navegadores

* O Workfront Fusion é compatível apenas com navegadores baseados no Chrome.

## Cenários

* O tempo-limite padrão de execução de cenário é **40 minutos**. Quando a execução atinge esse tempo-limite, o Workfront Fusion interrompe a execução do cenário após o próximo ciclo ou operação, dependendo do cenário. Isso força o cenário a parar logo depois que o limite de 40 minutos é atingido

  O encadeamento de cenários não conta no tempo-limite de execução do cenário. Um cenário pai não acumula tempo enquanto aguarda a execução de um cenário filho.
* O tamanho máximo de um blueprint do cenário é **5 MB**, mas recomendamos manter o tamanho do cenário abaixo de **3 MB**.

  Os módulos do aplicativo que criam ou atualizam dados com um número elevado de campos podem causar blueprints muito grandes.

   * Ao usar o aplicativo Workfront, selecione apenas os campos necessários para criar ou atualizar casos de uso.
   * Ao usar outros aplicativos, use módulos de API personalizados para interagir com qualquer tipo de registro que tenha um número elevado de campos.

* Embora não haja limite para o número de módulos em um cenário, cenários com mais de 150 módulos afetam negativamente o desempenho do sistema Workfront Fusion. Por esse motivo, não recomendamos criar cenários com mais de 150 módulos.

## Operações

* O tempo-limite padrão de operação geralmente é **40 segundos**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## Arquivos

* A capacidade total de processamento do Fusion para arquivos é **1 GB**. O limite se baseia em um custo total de memória. Cada operação contribui para esse custo. Se um único arquivo de 400 MB for baixado e enviado, o custo total para a capacidade do arquivo será de 800 MB.
* As organizações que utilizam o plano Workfront Ultimate têm acesso a um aumento na capacidade de processamento de arquivo maior que 1 GB. No entanto, há outros fatores que afetam a transferência de dados. O serviço ao qual o Fusion está se conectando pode limitar o tamanho do arquivo, o que afetaria quaisquer arquivos processados por esse serviço. Além disso, arquivos grandes podem afetar o tempo de execução do cenário. O Fusion processará os arquivos até que o limite de execução de 40 minutos seja atingido, momento em que a execução falhará.
* Se um arquivo for baixado usando um módulo compatível com arquivos grandes e, em seguida, for passado para um módulo que não é, esse módulo não processará o arquivo com êxito. Arquivos grandes devem ser manipulados exclusivamente com módulos compatíveis durante todo o fluxo de trabalho.
* Os módulos que não oferecem suporte a arquivos grandes podem processar arquivos de até **200 MB**.

Para obter mais informações, consulte [Como trabalhar com arquivos grandes](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Uso de memória do servidor

* O uso de memória do servidor para uma única execução é limitado a **1 GB**.

  Muitos fatores, como arquivos grandes ou módulos complexos, podem afetar o uso da memória do servidor de maneiras difíceis de prever ou controlar. Por esse motivo, a execução do cenário pode exceder o limite de memória de 1 GB, mesmo que o cenário siga todas as outras medidas de proteção de desempenho. Exceder o limite de memória causa falha na execução.

## Webhooks

* O tamanho máximo padrão de um conteúdo é **5 MB**.
* Os webhooks são limitados a **100 solicitações por segundo**. Quando esse limite é atingido, o Workfront Fusion envia um status 429 ([!UICONTROL Solicitações demais]).
* O Workfront Fusion armazena conteúdo do webhook por 30 dias. O acesso a um conteúdo de webhook por mais de 30 dias após seu recebimento resulta no erro &quot;[!UICONTROL Falha ao ler o arquivo do armazenamento]&quot;.
* Os webhooks são desativados automaticamente se qualquer uma das seguintes situações se aplicar:

   * O webhook não foi conectado a nenhum cenário por mais de 5 dias
   * O webhook é usado somente em cenários inativos, que ficaram assim por mais de 30 dias.

* Os webhooks desativados serão excluídos e removidos do registro automaticamente se não estiverem conectados a nenhum cenário e estiverem com o status desativado por mais de 30 dias.
* O tempo-limite para uma resposta do webhook é 5 minutos.

## Histórico de execução

* Os logs do histórico de execução são limitados ao tamanho de **100 MB**. Se o histórico de execução exceder esse tamanho, somente os primeiros 100 MB serão exibidos.
* Se um cenário tiver várias execuções simultâneas, apenas 5 delas serão exibidas na área Execuções da página de detalhes do cenário. Essa é a realidade mesmo quando mais de 5 execuções estão em andamento.

## Execuções incompletas

* As execuções incompletas são limitadas a um tamanho total de **11 GB** ou **100 execuções incompletas** por cenário, o limite que for atingido primeiro. Se um limite for atingido, não serão armazenadas mais execuções incompletas para esse cenário.
* O Workfront Fusion permite até 5 falhas por minuto.

## Tentativas

* Ao usar o módulo Quebra e especificar a diretiva Tentativa, se um cenário falhar consecutivamente 10 vezes em um período de 2 minutos, o cenário será desativado automaticamente.

## Recursão

A recursão ocorre quando um cenário aciona uma nova execução de si mesmo, que aciona uma nova execução, e assim por diante em um loop infinito.

Por exemplo, um cenário é acionado quando uma tarefa é criada e esse cenário cria duas tarefas. As tarefas recém-criadas acionam o cenário novamente, criando quatro novas tarefas. Toda vez que uma tarefa é criada, o cenário é acionado, e toda vez que o cenário é executado, o número de tarefas dobra. O número de tarefas aumenta exponencialmente.

A recursão pode causar problemas de desempenho tanto para a organização responsável pelo cenário recursivo quanto para outras organizações.

Considere o seguinte em relação à recursão:

* **Quando um cenário está causando recursão, ele é desativado pela equipe de engenharia do Fusion para evitar mais problemas de desempenho.**
* Como a recursão é resultado do próprio design do cenário, é preciso projetar os cenários de forma que eles não incluam ações que acionem o próprio cenário.

## TLS

* Atualmente, o Fusion é compatível com o TLS versão 1.2 por padrão.
* O Fusion poderá usar o TLS 1.3 para solicitações HTTPS de saída se o TLS 1.3 estiver habilitado para o serviço de destino.
* O Fusion é compatível com TLS 1.2 e TLS 1.3 para solicitações HTTPS de entrada para Webhooks.
* As organizações podem solicitar que o TLS versão 1.3 seja habilitado para sua instância do Fusion.

>[!NOTE]
>
> Se você estiver se conectando ao Workfront, esteja ciente de que essa funcionalidade TLS está habilitada no Workfront para chamadas a domínios que têm o formato `https://<domain>.my.workfront.com`.
