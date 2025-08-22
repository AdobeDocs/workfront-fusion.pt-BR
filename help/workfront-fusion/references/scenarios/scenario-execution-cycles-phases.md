---
title: Execução de cenários, ciclos e fases
description: Este artigo descreve os eventos que ocorrem enquanto um cenário do Adobe Workfront Fusion está em execução, como inicialização, operações, confirmações e reversões.
author: Becky
feature: Workfront Fusion
exl-id: abf41be5-df32-4eaf-b3f4-93ddf005bfe3
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 1%

---

# Execução de cenário, ciclos e fases

Cada execução de cenário começa com a fase de inicialização, continua com pelo menos um ciclo composto pelas fases de operação e confirmação/reversão e termina com a fase de finalização

* Inicialização
* Ciclo #1
   * Operação (leitura ou gravação)
   * Confirmar ou reverter
* Ciclo #2
   * Operação (leitura ou gravação)
   * Confirmar ou reverter
* ..
* Ciclo #n
   * Operação (leitura ou gravação)
   * Confirmar ou reverter
* Finalização

Em uma escala menor, cada módulo também segue essas fases. As informações sobre as fases do módulo podem ser encontradas nas informações do pacote processado, encontradas na bolha numerada na parte superior direita de cada módulo após a execução do cenário. Para obter mais informações sobre a localização de informações de pacotes processados, consulte [Informações sobre pacotes processados](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md#information-about-processed-bundles) no artigo Fluxo de execução de cenário.

Informações sobre as fases do cenário maior podem ser encontradas nos detalhes de execução.

## Fases de execução do cenário

### Inicialização

Durante a fase de inicialização, todas as conexões necessárias (conexão com um banco de dados, serviço de email e assim por diante) são criadas e verificadas para garantir que o módulo seja capaz de executar as operações desejadas.

### Ciclos

Cada ciclo representa uma unidade indivisível de trabalho composta por uma série de operações, cada uma com uma confirmação ou reversão.

Você pode definir o número máximo de ciclos no painel [!UICONTROL configurações de cenário]. O número padrão é 1.

* [Operação](#operation)
* [Confirmar](#commit)
* [Reversão](#rollback)

#### Operação

Durante a fase de operação, uma operação de leitura ou gravação é executada:

* Uma operação de leitura consiste em obter dados de um serviço que é processado por outros módulos de acordo com um cenário predefinido. Por exemplo, o módulo [!UICONTROL Workfront] >[!UICONTROL Watch records] retorna novos conjuntos (registros) criados desde a última execução do cenário.
* Uma operação de gravação consiste em enviar dados para um determinado serviço para processamento adicional. Por exemplo, o módulo Workfront >[!UICONTROL Carregar documento] carrega um arquivo no Workfront.

#### Confirmar

Se a fase de operação for bem-sucedida, a fase de confirmação será iniciada durante a qual todas as operações executadas pelos módulos serão confirmadas. Isso significa que o Workfront Fusion envia informações sobre seu sucesso para todos os serviços envolvidos na fase de operação.

### Reversão

Se ocorrer um erro durante a operação ou a fase de confirmação em qualquer módulo, a fase será abortada e a fase de reversão será iniciada, anulando todas as operações durante o ciclo fornecido.

>[!IMPORTANT]
>
>Todos os módulos do Workfront Fusion que oferecem suporte à reversão (também conhecida como transacionalidade) são marcados com a tag ACID.
>
>![Módulos Acid](assets/acid-modules.png)
>
>Os módulos não marcados com essa tag não podem ser revertidos para seu estado inicial quando ocorrem erros em outros módulos. Um exemplo típico de um módulo não ACID é a ação [!UICONTROL Email] >[!UICONTROL Enviar um Email]. Depois que o email é enviado, não é possível desfazer o envio.

### Finalização

Durante a fase de finalização, as conexões abertas (por exemplo, conexões FTP, conexões de banco de dados e assim por diante) são fechadas e o cenário é concluído.

## Recursos

Para obter mais informações, consulte [Definir configurações de cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).
