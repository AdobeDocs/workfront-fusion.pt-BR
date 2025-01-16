---
title: Adicionar um filtro a um cenário
description: Em alguns cenários, é necessário trabalhar somente com pacotes que atendam a critérios específicos. Os filtros permitem selecionar esses pacotes.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: 839f6edf93df8a935b2c5d0a520bdc125fe60288
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# Adicionar um filtro a um cenário

Em alguns cenários, é necessário trabalhar somente com pacotes que atendam a critérios específicos. Os filtros permitem selecionar esses pacotes.

Por exemplo, você pode criar um cenário com o acionador [!UICONTROL Watch records] para [!DNL Workfront] para capturar somente tarefas atribuídas a um usuário específico.

Você pode adicionar um filtro entre dois módulos e verificar se os pacotes recebidos dos módulos anteriores atendem a condições de filtro específicas:

* Se isso acontecer, os pacotes serão transmitidos para o próximo módulo no cenário.
* Caso contrário, o processamento dos pacotes será encerrado.

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

Você deve adicionar ambos os módulos a um cenário antes de poder adicionar um filtro entre eles.

## Adicione um filtro entre dois módulos:

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário ao qual deseja adicionar um filtro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no ícone de chave inglesa ![Ícone de chave inglesa](assets/wrench-icon.png) entre os módulos aos quais deseja adicionar um filtro e selecione **Configurar um filtro**.
1. Na caixa que é exibida, insira um **[!UICONTROL Label]** para o filtro.
1. Defina o filtro **[!UICONTROL Condition]**.

   Insira o campo pelo qual você deseja filtrar no primeiro campo, o operador e (se necessário) o valor ao qual você deseja comparar o campo.

   >[!TIP]
   >
   >É possível inserir valores em campos de filtro no painel de mapeamento
   >Para obter mais informações sobre mapeamento, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Por exemplo, se você deseja que o filtro passe os arquivos em [!DNL Adobe Workfront] terminando com XML, digite **[!UICONTROL File name]** na primeira caixa e .**[!UICONTROL xml]** na segunda caixa. No menu suspenso entre elas, você selecionaria **[!UICONTROL Ends with (case insensitive)]**. Esse filtro se aplicaria aos pacotes recebidos do primeiro módulo (Workfront). Somente pacotes contendo arquivos XML passariam para o módulo seguinte.

   ![](assets/set-up-filter-box.png)

1. Clique em **[!DNL OK]**.

## Copiar um filtro

Atualmente, o editor de cenários inclui um recurso para copiar um filtro.

>[!NOTE]
>
>Se você copiar os módulos em ambos os lados do filtro, o filtro também será copiado.
>
>Para obter mais informações sobre como copiar módulos, consulte [Copiar módulos ou cenários em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

Para copiar um filtro sem copiar módulos, é possível usar a Ferramenta de Desenvolvimento Fusion

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário ao qual deseja adicionar um filtro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Abra o Fusion DevTool clicando no ícone DevTool ![ícone DevTool](assets/debugger-icon.png) próximo à parte inferior da tela.

   Se você não vir o ícone DevTool, consulte [Depurar um cenário](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) para obter instruções sobre como abrir a DevTool.

1. Clique no ícone **[!UICONTROL Tools]** ![](assets/devtools-tools-icon.png) na barra lateral esquerda.

1. Clique em **[!UICONTROL Copy Filter]** e configure a ferramenta **[!UICONTROL Copy Filter]** no painel direito:

   1. Defina **[!UICONTROL Source Module]** como o módulo diretamente após o filtro que você deseja copiar.
   1. Defina **[!UICONTROL Target Module]** como o módulo após o qual você deseja colocar o filtro.

1. Clique em **[!UICONTROL Run]**.
