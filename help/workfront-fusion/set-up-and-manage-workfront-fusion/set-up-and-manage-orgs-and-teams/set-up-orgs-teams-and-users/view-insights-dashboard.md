---
title: Exibir o painel de Insights de uma organização
description: Os administradores do Fusion podem visualizar um painel que mostra as métricas de execução de uma organização.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: 'https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 45c755a2f6152b6e230864e4c840d0334705bd22
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 3%
---
# Exibir o painel de Insights de uma organização

O Painel do Fusion Insights permite ver rapidamente quais cenários estão sendo mais executados, onde os atrasos estão ocorrendo e com que eficiência seus pools de trabalhadores estão operando. Isso proporciona visibilidade em tempo real dos volumes de execução, profundidade da fila, utilização do pool e desempenho em nível de cenário.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Adobe Workfront Workflow Ultimate e Adobe Workfront Automation and Integration Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso</td> 
   <td> 
     <p>Você deve ser um administrador do Workfront Fusion para sua organização.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações desta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Componentes do painel do Insights

>[!NOTE]
>
>As métricas são mostradas pelo pool de trabalhadores. Para exibir um pool de trabalhadores diferente, clique no campo Pool próximo ao canto superior esquerdo do painel e selecione o pool para o qual deseja exibir métricas.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

No painel do Fusion Insights, é possível ver as seguintes métricas.

* **Logs de Execuções com Falha**
Essa tabela lista cada execução de cenário de falha ou aviso em sua organização para que você possa encontrar e solucionar problemas sem sair do painel.
* **Operações da Organização**
Este gráfico permite exibir o número de operações usadas em sua organização. Você pode selecionar equipes ou cenários específicos e exibir operações na última semana, mês ou ano.
* **Principais cenários por operações**
Este gráfico permite exibir quais cenários estão usando mais operações. Você pode selecionar equipes específicas ou exibir dados do último dia, semana ou mês.

<!--

* **Executions waiting to be processed**
   This chart shows the number of executions waiting to be processed (also known as the execution backlog) at a given point in time. 

   A high number of executions waiting to be processed may affect performance in your Fusion instance. You will receive a notification if your execution backlog reaches 5000 executions. We recommend identifying responsible scenarios and modifying or disabling them. If the high execution backlog persists, the Fusion team will protect the performance of your Fusion instance by disabling the responsible scenarios.
* **Pool Utilization**
   This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.

   If a pool is nearing 100% utilization, other resources that use the same pool may be delayed or disrupted. If this occurs, we recommend reassigning a high-usage scenario to another worker pool, or modifying existing scenarios to be less resource intensive.
* **Executions per scenario**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify which scenarios may be causing an execution backlog or high worker pool utilization. 
* **Duration of executions**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify scenarios that are taking longer than usual, including those affected by issues with a connected app or service.

-->

## Exibir o Painel do Fusion Insights

1. No Fusion, clique em **Insights** na navegação à esquerda.

   O Painel é aberto.

1. Para visualizar dados de um momento específico, passe o mouse sobre um painel e ajuste o cursor para estar sobre o momento que deseja visualizar.

   Uma linha aparece sobre esse ponto no tempo em todos os gráficos, e uma janela mostrando dados para esse tempo aparece em cada gráfico.
1. Para exibir dados de um cenário específico no gráfico Execuções por cenário ou no gráfico Duração de execuções, clique em uma barra da cor do cenário para o qual deseja exibir dados. Para retornar à visualização que mostra todos os cenários, clique no gráfico novamente.
1. Para ir para um cenário específico mostrado no gráfico Execuções por cenário ou no gráfico Duração de execuções, clique com o botão direito do mouse em uma barra da cor do cenário e selecione **Abrir cenário em nova guia**.
1. Para expandir um gráfico, clique no ícone **Expandir** ![Ícone Expandir](assets/expand-icon.png) no canto superior direito desse gráfico.
1. Para alterar o intervalo de tempo do painel, abra o campo Intervalo de tempo no canto superior direito do painel e selecione um novo intervalo de tempo. O período mais longo disponível é de 24 horas e o mais curto é de 15 minutos.
1. Para atualizar os gráficos, clique no ícone Atualizar próximo ao canto superior direito do painel.
1. Para exibir um pool de trabalhadores diferente, clique no campo Pool próximo ao canto superior esquerdo do painel e selecione o pool que deseja exibir.

## Personalizar o painel de Insights

Você pode escolher quais widgets serão exibidos no painel Insights e em que ordem.

### Adicionar, remover ou reordenar widgets

1. Na navegação à esquerda, clique em **Insights** ![Ícone de Insights](assets/insights-icon.png).
1. Clique em **[!UICONTROL Personalizar]** no cabeçalho do Insights.

   Um painel lateral se abre. Ele lista cada widget como um cartão que mostra uma visualização, o nome do widget e uma descrição.

1. Para mostrar ou ocultar um widget, clique no respectivo cartão ou clique no botão **[!UICONTROL Adicionar widget]** ou **[!UICONTROL Remover widget]** no cartão.

   Os widgets exibidos têm uma marca de seleção.
1. Para reordenar widgets, arraste um cartão de widget para uma nova posição no painel.

   Um espaço reservado tracejado e uma barra suspensa mostram onde o cartão será direcionado.

Suas escolhas são salvas por navegador. Os widgets adicionados em versões posteriores aparecem automaticamente no painel.

Se você remover todos os widgets, a página exibirá a mensagem &quot;Nenhum widget nesta página&quot;.

## Atualizar o painel de Insights

Para recarregar os dados de cada widget, clique em **[!UICONTROL Atualizar]** ao lado de **[!UICONTROL Personalizar]**.

* Cada widget mantém seus filtros.
* O botão **[!UICONTROL Atualizar]** mostra um estado pendente até que todos os widgets terminem de ser carregados.
* Os gráficos mantêm o gráfico anterior sob um controle giratório de carregamento, e o Log de execuções esmaece sua tabela sob um controle giratório enquanto os dados são recarregados.
* Se uma atualização falhar, os widgets manterão seus últimos dados bons.

## Faça o tour do Insights

Na primeira vez que você abrir o painel Insights, uma caixa de diálogo de boas-vindas oferecerá a opção de iniciar um tour ou ignorá-lo.

O tour destaca cada widget, em sua ordem salva, bem como o botão e painel **[!UICONTROL Personalizar]**, o botão **[!UICONTROL Atualizar]** e o botão **[!UICONTROL Repetir tour]** na barra de título.

Para reiniciar o tour a qualquer momento, clique no ícone de informações do tour ![ícone de informações](assets/insights-tour-information.png) na barra de título.

O tour não começa quando você abre o painel de Insights a partir de um link em um cenário. Para obter mais informações, consulte [Abrir o painel de Insights de um cenário](#open-the-insights-dashboard-from-a-scenario) neste artigo.

## Pesquisar cenários e equipes por ID

Nos widgets **[!UICONTROL Operações da Organização]** e **[!UICONTROL Principais Cenários por Operações]**, os campos **[!UICONTROL Cenário]** e **[!UICONTROL Equipe]** correspondem na ID e no nome. Cada opção mostra sua ID sob o nome, por exemplo &quot;ID 123&quot;.

* As listas carregam os primeiros 500 cenários e as primeiras 200 equipes. Se você inserir uma ID que não esteja na lista carregada, o Fusion a pesquisará automaticamente após um pequeno atraso.
* Se você limpar um cenário, a equipe que foi preenchida automaticamente para esse cenário também é limpa.

>[!NOTE]
>
>O filtro de cenário no Log de Execuções não corresponde na ID.

## Abrir o painel de Insights em um cenário

Você pode abrir o painel de Insights com o widget **[!UICONTROL Operações da Organização]** filtrado para um cenário e uma equipe específicos.

Para acessar a página de Insights a partir de um cenário:

1. Abra a página de detalhes do cenário:

   1. Clique na guia **[!UICONTROL Cenário]** no painel esquerdo e, em seguida, clique no cenário sobre o qual deseja obter detalhes.

      Ou

      Se você estiver trabalhando no cenário no editor de cenários, clique na seta para a esquerda ![Seta para edição de saída](assets/exit-editing-arrow.png) próxima ao canto superior esquerdo da janela.
      1. Clique na guia **Relatórios** próxima à parte superior da página.

* O widget **[!UICONTROL Operações da Organização]** abre filtrado para esse cenário e equipe, e a página rola até o widget.
* Se você tiver removido o widget da página, será exibido um aviso com o botão **[!UICONTROL Adicionar widget]**.

## Usar modo escuro

O painel Insights e seus widgets seguem automaticamente sua configuração de modo escuro. Quando você altera a configuração, a página é atualizada imediatamente, sem recarregar, e mantém seu estado atual. O modo de luz não é alterado.

## Acesso ao widget de desempenho

O widget **[!UICONTROL Desempenho]** é mostrado apenas para usuários que têm uma das seguintes permissões:

* Organização Editar na organização ativa
* Exibição da organização na página de administração

O widget está oculto na página e no painel **[!UICONTROL Personalizar]** para outros usuários. Se um usuário receber acesso posteriormente, o widget retornará em sua posição salva. Abrir o URL do Insights diretamente não ignora essa verificação.

## Filtrar e filtrar execuções no Log de execução

Use o Log de execução para localizar execuções de cenário que falharam ou retornaram um aviso em sua organização e reativar todos os cenários que foram desativados automaticamente após falhas repetidas.

1. No Log de execução, filtre as execuções por qualquer um dos seguintes itens:

   * [!UICONTROL Equipe]
   * [!UICONTROL Cenário]
   * [!UICONTROL Tipo de execução]
   * [!UICONTROL Intervalo de datas]
   * [!UICONTROL Estado de desativação]
   * [!UICONTROL Mensagem de erro]

   Para a maioria dos filtros, é possível optar por corresponder apenas aos valores selecionados ou a tudo, exceto eles.

1. Clique em uma execução para exibir mais detalhes sobre o erro.
1. Para reativar um ou mais cenários que foram desativados automaticamente após falhas repetidas, selecione as execuções e clique em **Ativar**.

   >[!NOTE]
   >
   >Antes de reativar um cenário, investigue a causa das falhas, como credenciais expiradas ou um problema de conector, para que o cenário não falhe imediatamente novamente.
