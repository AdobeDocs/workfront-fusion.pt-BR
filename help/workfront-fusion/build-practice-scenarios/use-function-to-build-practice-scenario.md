---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Usar uma função para atualizar um projeto em um cenário básico
description: Saiba como adicionar uma função para atualizar um item de trabalho no Workfront.
author: Becky
feature: Workfront Fusion
exl-id: aa082ac8-48e8-4569-880e-024dd77feaa1
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---

# Usar uma função para atualizar um projeto em um cenário básico

Atualizar um item de trabalho do Workfront é um caso de uso comum para o Workfront Fusion. Neste exemplo, você usará uma função para alterar o nome de um projeto para ficar em letras maiúsculas.

O Fusion inclui muitos tipos de funções que permitem transformar e executar lógica condicional em seus dados. Para obter mais informações sobre o uso de funções, consulte [Visão geral da função](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

Este exemplo modifica o cenário criado em [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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

## Pré-requisitos

Você deve criar o cenário descrito em [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) antes de seguir este procedimento.

## Usar uma função para atualizar um projeto

### Adicionar o módulo Atualizar Registro ao seu cenário

1. Abra o cenário no editor de cenários.
1. Passe o mouse sobre o círculo parcial à direita do do segundo módulo e clique em **[!UICONTROL Add another module]**.
1. Selecione [!DNL Adobe Workfront] na lista de aplicativos e escolha o módulo **[!UICONTROL Update Record]**.
1. No campo ID, selecione o bloco de ID que está sob o módulo de objeto Converter. Esta é a ID do projeto emitido por esse módulo.

   ![ID do objeto Convert](assets/id-convert-object.png)

1. No campo Tipo de registro, selecione Projeto, pois o objeto a ser atualizado é um projeto.
1. Na área Selecionar campos a serem mapeados, selecione Nome.

   Um campo Nome será aberto.
1. Continue para [Mapear a função para a atualização de nome](#map-the-function-for-the-name-update).

### Mapear a função para a atualização de nome

Quando esse cenário converte uma solicitação em um projeto, o nome do projeto é igual ao da solicitação. A função aqui pega esse nome e coloca todas as letras em maiúsculas nele.

1. Clique no campo **Nome**.

   O painel de mapeamento é aberto.
1. No painel de mapeamento, clique no ícone **Funções binárias e de texto**. ![Ícone de funções de texto](assets/toolbar-icon-text&binary-functions.png)
1. Selecione a função **upper**.

   A função aparece no campo Nome, incluindo a formatação da entrada esperada.

   A entrada para este exemplo é o nome do problema do qual o projeto foi convertido.

1. Mova o cursor entre os parênteses, porque é para onde a entrada irá.
1. No painel de mapeamento, clique no ícone **Saída do módulo**. ![Ícone de saída do módulo](assets/toolbar-icon-functions-you-map-from-other-modules.png)
1. Selecione o bloco de nome que foi emitido pelo primeiro módulo.

   O bloco de nome aparece na função.

   ![Bloco de nome na função](assets/map-name.png)

1. Clique em **OK** para salvar as configurações do módulo.

### Testar e ativar

1. Teste o cenário clicando em **Executar uma vez** no canto inferior esquerdo da tela.
1. Examine a saída para garantir que o cenário seja executado conforme esperado.
1. Quando estiver satisfeito com o funcionamento do cenário, clique no botão de alternância **Agendamento** no canto inferior esquerdo da tela para **Ativado**.

   Isso ativa o cenário. Cenários ativos são executados de acordo com o agendamento definido no módulo do acionador.
1. Em [!DNL Workfront Fusion], clique em **[!UICONTROL Save]** próximo ao canto inferior esquerdo para salvar seu progresso no cenário.

   >[!IMPORTANT]
   >
   >Salve com frequência à medida que você aprimora e testa um cenário.

## Recursos

* [Mapear itens usando funções](/help//workfront-fusion/create-scenarios/map-data/map-using-functions.md)
