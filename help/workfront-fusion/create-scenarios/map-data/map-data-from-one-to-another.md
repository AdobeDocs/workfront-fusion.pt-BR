---
title: Mapear informações de um módulo para outro
description: Mapeamento é o processo de atribuir as saídas de um módulo, estruturadas em itens, aos campos de entrada de outro módulo.
author: Becky
feature: Workfront Fusion
exl-id: 1e3f7729-f48e-451e-a90b-d680c9e3bcbc
source-git-commit: 8de3e365ff7ff91f4b29fb8a298f3b846de0a980
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 17%

---

# Mapear informações de um módulo para outro

Mapeamento é o processo de atribuir as saídas de um módulo aos campos de entrada de outro módulo.

The mapping panel displays when you click a field where you can insert a value outputted from a preceding module in a scenario.

You can also create a formula using any combination of functions and mapped items from the mapping panel with static text that you type. These elements can be nested inside each other.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote do Adobe Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Os pacotes Workfront Prime e Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p><p>Trabalho ou maior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Map an item

After you have created a sequence of modules by linking two or more of them, each module can process values of items outputted by the modules that precede it.

To assign output items to a module&#39;s input fields:

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja mapear dados.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Click on the module that should process the output of the preceding module or modules.
1. In the Module settings panel that displays, click a field where you want to use the value of an item outputted from a preceding module.

   O painel de mapeamento é aberto.

1. (Optional) To search for a particular field in the mapping panel, click the mapping panel search bar and type in the term you want to search for. Click the field when it appears in the list.

   Search results contain the search term and are not case sensitive.
1. To select a value that is an element of a collection, click the arrow next to that collection, then select the element when it appears.

   ![Collection element](assets/collection-dropdown.png)

1. Click an item from the mapping panel to insert it into the field.

For more information, see [Configure a module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).


## Solução de problemas

### Problem: Missing items in the mapping panel

The mapping panel displays output items from previous modules. Occasionally, some items might be missing from this panel. You can run the module that is missing output in the scenario editor, and the mapping panel can then include those items in later modules. The exact procedure differs depending on the module&#39;s type.

* [Instant trigger](#instant-trigger)
* [Acionador de sondagem](#polling-trigger)
* [Outros módulos](#other-modules)

#### Acionador instantâneo

1. Clique com o botão direito do mouse no módulo e clique em **[!UICONTROL Executar este módulo somente]** no menu exibido.

   Como esse é um acionador instantâneo, ele começa a observar eventos.

1. Crie o evento que o módulo está assistindo.

   Por exemplo, se o módulo for um módulo Workfront > Eventos de observação que esteja observando atribuições de tarefas, faça logon no Workfront (como um usuário diferente daquele que a conexão do Fusion está usando) e atribua uma tarefa.

1. Quando o módulo terminar de ser executado, clique no balão acima do módulo para explorar sua saída completa.

   O painel de mapeamento para módulos posteriores agora contém todos os itens na saída do módulo.

#### Acionador de sondagem

1. Clique com o botão direito do mouse no módulo e clique em **[!UICONTROL Executar este módulo somente]** no menu exibido.
1. Se não houver saída, clique em **[!UICONTROL Escolher onde começar]** e ajuste as configurações.
1. (Condicional) Se não houver um evento a ser processado, crie o evento que o módulo observará e repita a etapa 2.

   Por exemplo, se o módulo for um módulo Workfront > Observar registros que esteja observando atribuições de tarefas, faça logon no Workfront (como um usuário que não é o usuário que a conexão Fusion está usando) e atribua uma tarefa, em seguida, execute o módulo novamente.

1. Quando o módulo terminar de ser executado, clique no balão acima do módulo para explorar sua saída completa.

   O painel de mapeamento para módulos posteriores agora contém todos os itens na saída do módulo.

#### Outros módulos

Você pode optar por executar:

* O cenário inteiro (ou apenas a parte que contém o módulo)
* O módulo único

Para executar o módulo único:

1. Clique com o botão direito do mouse no módulo e clique em **[!UICONTROL Executar este módulo somente]** no menu exibido.
1. Forneça valores de exemplo para os itens de entrada, em seguida, clique em **[!UICONTROL OK]**.
1. Quando o módulo terminar de ser executado, clique no balão acima do módulo para explorar sua saída completa.

   O painel de mapeamento para módulos posteriores agora contém todos os itens na saída do módulo.
