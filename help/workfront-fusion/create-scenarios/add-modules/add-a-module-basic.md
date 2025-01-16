---
title: Adicionar um módulo a um cenário
description: Este artigo descreve o processo básico de adicionar um módulo a um cenário.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# Adicionar um módulo a um cenário

Um cenário é composto de uma série de módulos que indicam como os dados devem ser transformados em um aplicativo ou transferidos entre aplicativos e serviços da Web. Você constrói um módulo adicionando e configurando módulos.

Este artigo descreve o processo básico de adicionar um módulo a um cenário. Para obter instruções mais específicas sobre como adicionar um cenário, consulte os outros artigos em [Adicionar módulos: índice do artigo](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

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

## Adicionar o primeiro módulo a um cenário

O primeiro módulo de um cenário geralmente é um módulo acionador.

Para obter mais informações sobre módulos de acionador, consulte [Módulos de acionador](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) no artigo Visão geral do módulo.

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Comece a criar um cenário clicando em **Criar um novo cenário** no canto superior direito da tela.

   O editor de cenários é aberto, com um módulo de espaço reservado (ponto de interrogação) e a lista de conectores disponíveis.

   ![Módulo de espaço reservado](assets/placeholder-module.png)

1. Selecione o conector ou webhook que iniciará esse cenário. Você pode digitar o nome do conector na barra de pesquisa da lista para filtrar a lista.
1. Configure o módulo.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Se você removeu o primeiro módulo de um cenário e deseja substituí-lo, clique no módulo de espaço reservado (ponto de interrogação) para abrir a lista de conectores.

## Adicionar outro módulo a um cenário

1. Se você não estiver no editor de cenários do cenário ao qual deseja adicionar um módulo, clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário em que deseja exportar um blueprint.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Para adicionar um módulo a outro módulo, passe o mouse sobre a alça direita do módulo após a qual deseja adicionar um módulo, em seguida, clique em **Adicionar outro módulo** quando ele aparecer.

   A lista de conectores é aberta, mostrando todos os conectores já usados no cenário.

1. (Opcional) Para selecionar outro conector, clique em **Adicionar outro módulo** na lista e selecione o conector. Você pode digitar o nome do conector na barra de pesquisa da lista para filtrar a lista.
1. Configure o módulo.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Inserir um módulo entre módulos existentes em um cenário

1. Se você não estiver no editor de cenários do cenário ao qual deseja adicionar um módulo, clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário em que deseja exportar um blueprint.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no caminho pontilhado entre os módulos em que deseja inserir um módulo.
1. No menu exibido, selecione **Adicionar um módulo**.

A lista de conectores é aberta, mostrando todos os conectores já usados no cenário.

1. (Opcional) Para selecionar outro conector, clique em **Adicionar outro módulo** na lista e selecione o conector. Você pode digitar o nome do conector na barra de pesquisa da lista para filtrar a lista.
1. Configure o módulo.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
