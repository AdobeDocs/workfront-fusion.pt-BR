---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Criar um cenário básico
description: Saiba como criar um cenário de automação simples com o Adobe Workfront Fusion. Cenários de automação automatizam processos do Workfront, incluindo manipulação e transformação de dados. Este exemplo orienta você no processo de criação de um cenário que procura uma tarefa  [!DNL Workfront]  no Workfront e a converte em um projeto.
author: Becky
feature: Workfront Fusion
exl-id: 5284dee1-e890-4357-a28d-29e09ac02822
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 1%

---

# Criar um cenário básico

O papel de [!DNL Adobe Workfront Fusion] é automatizar seus processos para que você possa se concentrar em novas tarefas em vez de repetir as mesmas tarefas repetidamente. Ele funciona vinculando ações em e entre aplicativos e serviços para criar um cenário que transfere e transforma seus dados automaticamente. O cenário que você cria observa dados em um aplicativo ou serviço e processa esses dados para fornecer o resultado desejado.

Esse exemplo orienta você pelo processo de criação de um cenário que pesquisa uma solicitação no Workfront e a converte em um projeto.

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
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++



## Criar um cenário de prática

### Começar a criar o cenário

1. Na área **Cenários**, clique em **Criar um novo cenário**.

   Para localizar a área Cenários, consulte [Navegar pelo Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/navigate-workfront-fusion.md).

   O editor de cenários é exibido, contendo um módulo vazio no centro.

1. Selecione o nome do espaço reservado **[!UICONTROL New scenario]** no canto superior esquerdo e digite um nome.
1. Continue com [Adicionar e configurar o primeiro módulo](#add-and-configure-the-first-module).

### Adicionar e configurar o primeiro módulo

1. Clique no módulo vazio para escolher o aplicativo do qual você selecionará um módulo.

   Uma lista de aplicativos é exibida à direita do módulo.

1. Selecione **[!DNL Adobe Workfront]**. Se não estiver visível, clique na barra de pesquisa na parte inferior da lista, digite &quot;Workfront&quot; e selecione-a quando ela aparecer na lista.

   A lista é alterada para exibir todos os módulos [!DNL Workfront] que você pode usar.

1. Clique no módulo **[!UICONTROL Search]**.

   A janela de configuração do módulo é aberta.

1. Na caixa [!UICONTROL Connection], selecione sua conexão com o Workfront.

   Se você não tiver uma conexão Workfront, consulte [Criar uma conexão](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)
1. Na caixa [!UICONTROL Record Type], selecione **[!UICONTROL Issue]**. Isso define o módulo para pesquisar somente problemas, que incluem solicitações.

   Você pode encontrar **[!UICONTROL Issue]** na lista se começar a digitar a palavra &quot;[!UICONTROL Issue]&quot;.

1. Na caixa **[!UICONTROL Result Set]**, selecione **[!UICONTROL First Matching Record]**.

   Isso define o módulo para retornar somente o primeiro registro encontrado que atenda aos critérios.
1. Na área **[!UICONTROL Search criteria]**, configure os critérios para retornar a tarefa específica.

   1. Na primeira caixa em [!UICONTROL Search Criteria], selecione o campo que deseja incluir na pesquisa. Para este exemplo, selecione **[!UICONTROL Name]**.

      Você pode encontrar **[!UICONTROL Name]** na lista se começar a digitar a palavra &quot;[!UICONTROL name]&quot;.
   1. Para o operador, clique na seta suspensa ao lado de **Existe** e altere para [!UICONTROL **Contém (não diferencia maiúsculas de minúsculas)**].

      Isso permite que o módulo encontre projetos com as palavras escolhidas em seu nome, mesmo se você não inserir o nome inteiro ou inserir o nome com a caixa incorreta (como todas em maiúsculas).
   1. No último campo em [!UICONTROL Search Criteria], digite uma palavra ou frase que você sabe que está no nome da tarefa que está procurando.

1. Na lista **[!UICONTROL Outputs]**, selecione os campos nos quais deseja que o módulo seja gerado. Para este exemplo, selecione os campos **[!UICONTROL ID]** e **[!UICONTROL Name]**.

   >[!TIP]
   >
   >Você pode usar **Cmd+F** (SO [!DNL Mac]) ou **Ctrl-F** (SO [!DNL Windows]) para localizar um campo rapidamente.

1. Clique em **[!UICONTROL OK]** para salvar a configuração do módulo.

1. Clique com o botão direito do mouse no módulo, clique em **[!UICONTROL Rename]**, em seguida, digite um nome que descreva o que você deseja que o módulo faça (como &quot;Pesquisar solicitações&quot;) e, em seguida, clique em **[!UICONTROL OK]**.

   O nome aparece logo abaixo do módulo. Abaixo disso, [!DNL Workfront Fusion] inclui uma breve descrição do tipo de ação executada pelo módulo.

   ![](assets/module-renamed-wf.png)

1. Continue com [Adicionar e configurar o segundo módulo](#add-and-configure-the-second-module).

## Adicionar e configurar o segundo módulo

1. Passe o mouse sobre o círculo parcial à direita do do módulo e clique em **[!UICONTROL Add another module]**.
1. Selecione [!DNL Adobe Workfront] na lista de aplicativos e escolha o módulo **[!UICONTROL Convert object]**.
1. No campo [!UICONTROL Connection], selecione a mesma conexão do Workfront usada no módulo anterior.
1. No campo **[!UICONTROL Record type]**, selecione **[!UICONTROL issue]**, pois o módulo converterá um problema.
1. No campo **[!UICONTROL Convert to]**, selecione **Projeto**.
1. Ao lado do campo ID de tarefa, clique no botão de alternância do mapa para ativá-lo.

   O botão fica azul quando é ativado. Isso permite mapear a ID da tarefa do módulo anterior.

   ![Alternância de mapa](assets/map-toggle.png)
1. Clique no campo **[!UICONTROL Task ID]**.

   É aberto um painel que permite selecionar o que será usado como a ID da tarefa que você deseja converter em um projeto. Como você ativou o mapeamento, o painel inclui a saída de qualquer módulo anterior. Você selecionou ID como uma saída do módulo anterior, de modo que ele agora está disponível no painel.

   Esse painel é chamado de painel de mapeamento. Para obter mais informações sobre o painel de mapeamento, consulte [Visão geral do mapeamento](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).
1. Selecione **ID** no painel de mapeamento.

   Um bloco ID é exibido no campo ID. Ela mostra o número do módulo do qual é mapeado e o campo que é mapeado.

   ![ID do mapa](assets/map-id.png)

1. Clique no campo **ID do Modelo**, comece digitando o nome do modelo do Workfront que deseja usar para este projeto e selecione-o quando ele aparecer na lista.
1. Clique em **[!UICONTROL OK]** para salvar a configuração do módulo.

1. Clique com o botão direito do mouse no módulo, clique em **[!UICONTROL Rename]**, digite um nome que descreva o que você deseja que o módulo faça (como &quot;Converter em projeto&quot;) e clique em **[!UICONTROL OK]**.

1. Continue para [Testar o cenário](#test-the-scenario).

## Testar o cenário

Antes de ativar o cenário, é importante testá-lo executando-o pelo menos uma vez e visualizando os resultados. Isso ajuda você a entender como os dados fluem pelo cenário e encontrar erros.

Para esse cenário, um teste bem-sucedido resultaria na localização da solicitação e na conversão dela em um projeto.

1. Clique em **[!UICONTROL Run once]** no canto inferior esquerdo do editor de cenários.
1. Depois que o cenário terminar de ser executado, clique no balão acima do primeiro módulo para exibir informações sobre o pacote de dados que o módulo processou, incluindo dados obtidos da solicitação que o módulo retornou.

1. Clique na bolha do inspetor de execução acima do segundo módulo para ver a entrada (a solicitação) e a saída (o projeto convertido).

   Para obter mais informações sobre os dados nas bolhas de inspeção, consulte:

   * Para obter informações gerais, consulte [Fluxo de execução do cenário](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Para obter informações sobre pacotes processados, consulte [Execução do cenário, ciclos e fases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. Em [!DNL Workfront Fusion], clique em **[!UICONTROL Save]** próximo ao canto inferior esquerdo para salvar seu progresso no cenário.

   >[!IMPORTANT]
   >
   >Salve com frequência à medida que você aprimora e testa um cenário.

>[!TIP]
>
>Recomendamos a prática opcional, mas útil, de adicionar observações sobre cada módulo.
>
>1. Clique com o botão direito em um módulo e selecione **[!UICONTROL Add a note]**.
>1. Na nota exibida, digite uma visão geral do módulo.
>
>    Você pode adicionar várias notas para um módulo.
>
>1. Feche a área **[!UICONTROL Notes]**.
>
>     Depois de adicionar uma observação a um cenário, um ponto laranja é exibido no ícone **[!UICONTROL Notes]** ![](assets/notes-icon-w-dot.png), na parte inferior do editor de cenários.
>
>1. Clique no ícone **[!UICONTROL Notes]** ![](assets/notes-icon-w-dot.png) para exibir suas anotações.
>

## Ativar o cenário

A última etapa na criação de um cenário é ativá-lo.

Como esse cenário está procurando por um problema específico, não há necessidade de ativá-lo. Ativar um cenário faz com que ele seja executado de acordo com um agendamento ou quando uma ação específica ocorre em um aplicativo. Após ativar um cenário, por padrão, ele é executado a cada 15 minutos. Você pode alterar isso definindo quando e com que frequência deseja que ele seja executado.

Para obter mais informações sobre como ativar cenários, consulte [Ativar ou desativar um cenário](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

Para obter informações sobre agendamentos, consulte [Agendar um cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Próximas etapas

* [Adicione um módulo de acionador](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) para permitir que o cenário procure novas solicitações periodicamente e as converta em projetos.
* [Adicione um webhook](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) para permitir que o cenário seja executado sempre que uma solicitação for inserida.
* [Adicione um filtro](/help/workfront-fusion/build-practice-scenarios/add-filter-basic-scenario.md) para garantir que somente determinadas solicitações sejam convertidas em projetos.
* [Adicione uma função](/help/workfront-fusion/build-practice-scenarios/use-function-to-build-practice-scenario.md) que personalize o nome do novo projeto.
