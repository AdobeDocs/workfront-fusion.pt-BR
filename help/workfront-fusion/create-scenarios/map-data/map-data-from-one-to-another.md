---
title: Mapear informações de um módulo para outro
description: O mapeamento é o processo de atribuir as saídas de um módulo, estruturadas em itens, aos campos de entrada de outro módulo.
author: Becky
feature: Workfront Fusion
exl-id: 1e3f7729-f48e-451e-a90b-d680c9e3bcbc
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Mapear informações de um módulo para outro

Mapeamento é o processo de atribuir as saídas de um módulo aos campos de entrada de outro módulo.

O painel de mapeamento é exibido ao clicar em um campo, onde é possível inserir um valor emitido de um módulo anterior em um cenário.

Também é possível criar uma fórmula usando qualquer combinação de funções e itens mapeados do painel de mapeamento com texto estático digitado. Esses elementos podem ser aninhados um dentro do outro.

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

## Mapear um item

Depois de criar uma sequência de módulos vinculando dois ou mais deles, cada módulo pode processar valores de itens gerados pelos módulos que o precedem.

Para atribuir itens de saída aos campos de entrada de um módulo:

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário em que deseja mapear dados.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no módulo que deve processar a saída dos módulos anteriores.
1. No painel Configurações do módulo que é exibido, clique em um campo onde você deseja usar o valor de um item emitido de um módulo anterior.

   O painel de mapeamento é aberto.

1. (Opcional) Para pesquisar um campo específico no painel de mapeamento, clique na barra de pesquisa do painel de mapeamento e digite o termo que deseja pesquisar. Clique no campo quando ele aparecer na lista.

   Os resultados da pesquisa contêm o termo de pesquisa e não diferenciam maiúsculas de minúsculas.
1. Para selecionar um valor que seja um elemento de uma coleção, clique na seta ao lado dessa coleção e selecione o elemento quando ele for exibido.

   ![Elemento de coleção](assets/collection-dropdown.png)

1. Clique em um item no painel de mapeamento para inseri-lo no campo.

Para obter mais informações, consulte [Configurar um módulo](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).


## Solução de problemas

### Problema: itens ausentes no painel de mapeamento

O painel de mapeamento exibe itens de saída de módulos anteriores. Ocasionalmente, alguns itens podem estar ausentes nesse painel. Você pode executar o módulo cuja saída está ausente no editor de cenários, e o painel de mapeamento pode então incluir esses itens em módulos posteriores. O procedimento exato difere dependendo do tipo do módulo

* [Acionador instantâneo](#instant-trigger)
* [Acionador de sondagem](#polling-trigger)
* [Outros módulos](#other-modules)

#### Acionador instantâneo

1. Clique com o botão direito do mouse no módulo e, em seguida, clique em **[!UICONTROL Run this module only]** no menu exibido.

   Como esse é um acionador instantâneo, ele começa a observar eventos.

1. Crie o evento que o módulo está assistindo.

   Por exemplo, se o módulo for um módulo Workfront > Eventos de observação que esteja observando atribuições de tarefas, faça logon no Workfront (como um usuário diferente daquele que a conexão do Fusion está usando) e atribua uma tarefa.

1. Quando o módulo terminar de ser executado, clique no balão acima do módulo para explorar sua saída completa.

   O painel de mapeamento para módulos posteriores agora contém todos os itens na saída do módulo.

#### Acionador de sondagem

1. Clique com o botão direito do mouse no módulo e, em seguida, clique em **[!UICONTROL Run this module only]** no menu exibido.
1. Se não houver saída, clique em **[!UICONTROL Choose where to start]** e ajuste as configurações.
1. (Condicional) Se não houver um evento a ser processado, crie o evento que o módulo observará e repita a etapa 2.

   Por exemplo, se o módulo for um módulo Workfront > Observar registros que esteja observando atribuições de tarefas, faça logon no Workfront (como um usuário que não é o usuário que a conexão Fusion está usando) e atribua uma tarefa, em seguida, execute o módulo novamente.

1. Quando o módulo terminar de ser executado, clique no balão acima do módulo para explorar sua saída completa.

   O painel de mapeamento para módulos posteriores agora contém todos os itens na saída do módulo.

#### Outros módulos

Você pode optar por executar:

* O cenário inteiro (ou apenas a parte que contém o módulo)
* O módulo único

Para executar o módulo único:

1. Clique com o botão direito do mouse no módulo e clique em **[!UICONTROL Run this module only]** no menu que é exibido.
1. Forneça valores de exemplo para os itens de entrada, em seguida, clique em **[!UICONTROL OK]**.
1. Quando o módulo terminar de ser executado, clique no balão acima do módulo para explorar sua saída completa.

   O painel de mapeamento para módulos posteriores agora contém todos os itens na saída do módulo.
