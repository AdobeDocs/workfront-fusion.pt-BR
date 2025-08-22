---
title: Visão geral do módulo
description: 'O Adobe Workfront Fusion distingue cinco tipos de módulos: módulos de ação, módulos de pesquisa, módulos de acionador, agregadores e iteradores. Agregadores e Iteradores são para cenários avançados.'
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 1%

---

# Visão geral do módulo

O Adobe Workfront Fusion distingue cinco tipos de módulos:

* Módulos de ação
* Pesquisar módulos
* Módulos acionadores
* Agregadores
* Iteradores

Agregadores e Iteradores são para cenários avançados.

## Módulos de ação

Os módulos de ação são o tipo mais comum de módulo. Um módulo de ação típico executa uma ação e retorna um único pacote, que então passa para o próximo módulo para processamento.

Diferentemente dos módulos de acionamento, os módulos de ação podem ser colocados no início, no meio ou no final de um cenário.

Os cenários podem conter um número ilimitado de módulos de ação, embora um grande número de módulos (mais de 150) possa afetar o desempenho.

>[!BEGINSHADEBOX]

**Exemplos:**

* **Workfront > [!UICONTROL Carregar um arquivo]** envia um arquivo à Workfront e retorna seu identificador.
* **[!UICONTROL Imagem] > [!UICONTROL Redimensionar]** recebe uma imagem, redimensiona-a para dimensões especificadas e passa a imagem redimensionada para a próxima ação.

>[!ENDSHADEBOX]

O tipo de ação tem quatro subtipos:

* Criar
* Ler
* Atualização
* Excluir

O subtipo Update inclui as três operações a seguir:

* **Apagar o conteúdo de um campo**. Essa operação ocorre quando o conteúdo do campo é avaliado para a palavra-chave `erase` (não deve ser confundido com `empty`).

  ![Apagar palavra-chave](assets/erase-content-of-field.png)

* **Deixe o conteúdo de um campo inalterado**. Essa operação ocorre quando o campo é deixado vazio ou o conteúdo do campo é avaliado como vazio (representado por meio de nulo no JSON).

  ![Pacote vazio](assets/leave-content-field-unchanged.png)

* **Substituir o conteúdo de um campo**. Esta operação ocorre em todos os outros casos que não os descritos acima.

>[!NOTE]
>
>* Se você não vir a palavra-chave `erase` no painel de mapeamento, o módulo não é um módulo de atualização ou não foi atualizado para as especificações mais recentes do aplicativo.
>* `Empty` não altera o conteúdo do campo. Se for necessário apagar o campo, você poderá usar a seguinte fórmula:
>
>   ![Se estiver vazio](assets/formula-ifempty-name-erase.png)
>
>* No momento, não há suporte para manter um campo inalterado quando seu conteúdo for avaliado como vazio.

## Pesquisar módulos

Os módulos de pesquisa retornam zero, um ou mais pacotes, que passam para o próximo módulo para processamento.

Você pode colocar módulos de Pesquisa no início, no meio ou no fim de um cenário.

Os cenários podem conter um número ilimitado de módulos de pesquisa, embora um grande número de módulos (mais de 150) possa afetar o desempenho.

>[!BEGINSHADEBOX]

**Exemplo:**

**Workfront > [!UICONTROL Ler Registros Relacionados]** lê registros que correspondem à consulta de pesquisa especificada em um determinado objeto pai.

>[!ENDSHADEBOX]

## Módulos acionadores

Os acionadores geram pacotes quando há uma alteração em um determinado serviço, como a criação ou atualização de um registro.

Os acionadores retornam zero, um ou mais pacotes, que passam para o próximo módulo para processamento.

Como os Acionadores fazem com que os cenários comecem a ser executados, eles só podem ser colocados no início de um cenário.

Cada cenário pode conter apenas um Acionador.

O Workfront Fusion usa dois tipos de acionadores: acionadores de pesquisa e acionadores instantâneos.

### Acionadores de sondagem

O polling aciona regularmente a pesquisa de um determinado serviço, mesmo se não houver alterações desde a execução do cenário anterior. Recomendamos que você agende um cenário contendo um acionador de sondagem para ser executado em intervalos regulares. Se houver uma alteração que corresponda à configuração do acionador, ele retornará pacotes contendo informações sobre a alteração. Se não houver alteração que corresponda à configuração, o acionador não gerará nenhum pacote.

Para obter instruções sobre como agendar um cenário, consulte [Agendar um cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Os acionadores de pesquisa permitem selecionar o primeiro pacote que devem ser gerados por meio de um painel que é exibido automaticamente depois que você salva um acionador ou altera as configurações dele. Essa seleção afeta apenas a primeira execução do módulo. Depois que o módulo for executado uma vez, as execuções subsequentes observarão apenas as alterações que ocorrerem após a execução mais recente.

Para obter mais informações, consulte [Escolher onde um módulo de acionador inicia](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md).

>[!BEGINSHADEBOX]

**Exemplos:**

* **Workfront > [!UICONTROL Registros de observação]** retorna registros que foram adicionados recentemente após a última vez que o cenário foi executado.

* **[!DNL Google Sheets]> [!UICONTROL Linhas de Observação]** retorna novas linhas adicionadas após a última vez que o cenário foi executado.

>[!ENDSHADEBOX]

### Acionadores instantâneos

Os acionadores instantâneos permitem que um serviço notifique o Workfront Fusion sobre uma alteração imediatamente após ela ocorrer. Recomendamos que você agende um cenário contendo um acionador instantâneo para ser executado imediatamente.

Para obter instruções, consulte [Agendar um cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Para obter detalhes sobre como os dados de entrada são tratados por um acionador instantâneo, consulte [Acionadores instantâneos (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

>[!BEGINSHADEBOX]

**Exemplos:**

* **Workfront > [!UICONTROL Assistir Eventos]** retorna informações quando um determinado tipo de evento ocorre no Workfront, como a criação de uma tarefa.
* **[!DNL Google Sheets]> [!UICONTROL Observar Alterações]** retorna informações sempre que uma célula é atualizada.

>[!ENDSHADEBOX]

## Agregadores

Um módulo Agregador acumula vários pacotes em um único pacote.

Os agregadores retornam apenas um pacote, que passa para o próximo módulo para processamento adicional.

Você pode colocar Agregadores somente no meio de um cenário.

Os cenários podem conter um número ilimitado de agregadores, embora um grande número de módulos (mais de 150) possa afetar o desempenho.

>[!BEGINSHADEBOX]

**Exemplos:**

* **[!UICONTROL Arquivar] > [!UICONTROL Criar um arquivo]** compacta vários arquivos em um arquivo zip.
* **[!UICONTROL CSV] > [!UICONTROL Agregar em CSV]** mescla várias cadeias de caracteres de um arquivo CSV em uma única linha.
* **[!UICONTROL Ferramentas] > [!UICONTROL Agregador de texto]** combina várias cadeias de caracteres em uma única cadeia.

>[!ENDSHADEBOX]

Para obter mais informações, consulte [Módulo agregador](/help/workfront-fusion/references/modules/aggregator-module.md).

## Iteradores

Um Iterador é um tipo de módulo que divide matrizes em pacotes separados.

Os iteradores retornam um ou mais pacotes, que passam para o próximo módulo para processamento.

É possível colocar iteradores somente no meio de um cenário.

Os cenários podem conter um número ilimitado de iteradores, embora um grande número de módulos (150+) possa afetar o desempenho.

>[!BEGINSHADEBOX]

**Exemplo:**

**[!UICONTROL Email] > [!UICONTROL Recuperar anexos]** quebra uma matriz de anexos em conjuntos separados.

>[!ENDSHADEBOX]

Para obter mais informações, consulte [Módulo Iterador](/help/workfront-fusion/references/modules/iterator-module.md) e [Mapear uma matriz](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
