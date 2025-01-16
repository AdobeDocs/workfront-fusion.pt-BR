---
title: Exibir e resolver execuções incompletas
description: A pasta [!UICONTROL Incomplete executions] armazena execuções de cenário que não foram concluídas com êxito devido a um erro. Cada execução incompleta armazenada pode ser resolvida manual ou automaticamente.
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---

# Exibir o histórico de execução de um cenário

Você pode exibir informações sobre os eventos ou execuções de um cenário ou pesquisar todas as execuções do cenário por dados específicos.

A execução de um cenário representa uma única execução do cenário.

Um evento de cenário é uma modificação no cenário, como edição, ativação ou desativação.

>[!NOTE]
>
>O histórico de um cenário exibe todos os eventos e execuções de um cenário nos últimos 30 dias.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacote</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença</td> 
   <td> <p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou plano do [!UICONTROL Prime] [!DNL Workfront]: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plano: [!DNL Workfront Fusion] está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso*</td> 
   <td> 
     <p>Você deve ser um administrador do [!DNL Workfront Fusion] para sua organização.</p>
     <p>Você deve ser um administrador [!DNL Workfront Fusion] para sua equipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Exibir histórico de cenários


### Exibir o histórico do cenário na guia Histórico

A guia [!UICONTROL History] mostra mais detalhes do que o disponível na página [!UICONTROL Scenario detail]. Você também pode filtrar e classificar as execuções na guia [!UICONTROL History].

1. Clique na guia **[!UICONTROL Scenario]** no painel esquerdo e clique no cenário.

   Ou

   Se estiver trabalhando no cenário no Editor de cenários, clique na seta para a esquerda ![](assets/exit-editing-arrow.png) próxima ao canto superior esquerdo da janela.

1. Clique em **Histórico** próximo ao nome do cenário.
   ![guia Histórico](assets/history-tab.png)

   Os detalhes a seguir são listados para cada execução do cenário:

   * Data em que a execução foi **[!UICONTROL Started]**
   * ID de execução
   * **[!UICONTROL Status]** (com êxito ou com falha)
   * Executar **[!UICONTROL Duration]**
   * Número de **[!UICONTROL Operations]**
   * Tamanho de **[!UICONTROL Data Transfer]**

   >[!NOTE]
   >
   >O histórico de cenários exibe um selo **Processando** ao lado dos cenários que foram executados recentemente, enquanto os detalhes da execução são gravados no armazenamento. O processamento ocorre imediatamente após a execução do cenário. e não deve durar mais do que alguns minutos. Os detalhes da execução do cenário podem não estar visíveis enquanto a execução estiver sendo processada.

1. Para exibir detalhes da execução de um cenário específico, clique em **Detalhes** na extremidade direita. O link [!UICONTROL details] estará visível somente se a execução tiver detalhes disponíveis.
1. Para exibir eventos, alterne **Mostrar eventos** em.


### Exibir o histórico do cenário na página Detalhes do Cenário


1. Clique na guia **[!UICONTROL Scenario]** no painel esquerdo e clique no cenário.

   Ou

   Se estiver trabalhando no cenário no Editor de cenários, clique na seta para a esquerda ![](assets/exit-editing-arrow.png) próxima ao canto superior esquerdo da janela.

1. Clique na guia **[!UICONTROL History]** no painel direito.
1. (Opcional) Para obter informações detalhadas sobre uma execução de cenário selecionada, clique na execução no painel direito.

   Para obter mais informações sobre o processamento de pacotes, consulte [Fluxo de execução de cenário](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* O histórico de cenários exibe um selo **Histórico de processamento** ao lado dos cenários que foram executados recentemente, enquanto os detalhes de execução são gravados no armazenamento. O processamento ocorre imediatamente após a execução do cenário. e não deve durar mais do que alguns minutos. Os detalhes da execução do cenário podem não estar visíveis enquanto a execução estiver sendo processada.

1. Para exibir eventos, clique na guia **Eventos**.

## Filtrar o histórico de execução do cenário

Você pode filtrar o histórico de execução para exibir somente execuções com os valores especificados.

1. Abra o histórico de página inteira para um cenário conforme descrito em [Exibir o histórico de execução de cenário na guia [!UICONTROL History]](#view-scenario-history-on-the-history-tab) deste artigo.
1. Clique no ícone [!UICONTROL filter] ![](assets/fusion-scenario-filter-icon.png) no cabeçalho da coluna pela qual você deseja filtrar.
1. Na caixa de diálogo [!UICONTROL filter], insira os valores pelos quais deseja filtrar.
1. Clique em **[!UICONTROL Save]**.

O ícone de filtro está laranja em colunas com um filtro ativo.

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## Pesquisar todas as execuções de um cenário

1. Abra o histórico de página inteira para um cenário conforme descrito em [Exibir o histórico de execução de cenário na guia [!UICONTROL History]](#view-scenario-history-on-the-history-tab) deste artigo.
1. Clique em **[!UICONTROL Fulltext search]** na parte superior da lista de execuções.

   Ou

   Digite **Ctrl+Shift+F** (Windows) ou **Cmd+Shift+F** (Mac)
A janela [!UICONTROL Search in history] é aberta.

1. (Opcional) Para procurar execuções que contenham texto específico, insira o texto na barra de pesquisa da janela **[!UICONTROL Search in history]**.

   Para procurar um texto exato, coloque o texto entre aspas duplas (&quot;exemplo&quot;).

   >[!INFO]
   >
   >**Exemplo:** Se quiser encontrar a execução que criou um projeto específico, insira a ID do projeto na barra [!UICONTROL Fulltext search].
   >
   >&quot;625ef2ef0006036bd1794b6e52d737c5&quot;

1. (Opcional) Para limitar sua pesquisa por intervalo de datas, selecione as datas de início e término da pesquisa desejada na área [!UICONTROL By date range].

   >[!NOTE]
   >
   >* As execuções estão disponíveis somente para os últimos 30 dias.
   >
   >* O [!DNL Workfront Fusion] armazena cargas de webhook por 30 dias. Acessar uma carga de webhook mais de 30 dias após sua criação resulta no erro &quot;[!UICONTROL Failed to read file from storage.]&quot;


1. (Opcional) Para limitar sua pesquisa por status, selecione o status desejado na lista suspensa **[!UICONTROL By status]**.


   Os status disponíveis são:

   * [!UICONTROL All]

   * [!UICONTROL Error]

   * [!UICONTROL Warning]

   * [!UICONTROL Success]

1. (Opcional) Altere a ordem de exibição dos resultados na lista suspensa **[!UICONTROL Sort by dates]**.

1. (Opcional) Para copiar uma ID de execução de cenário, clique no ícone **[!UICONTROL Copy execution ID]** <img src="assets/copy-fusion-execution-id-icon.png"> na linha da execução desejada.

1. (Opcional) Clique em um resultado de [!UICONTROL Fulltext search] para examinar o pacote de saída do módulo de cenário que contém as informações.
