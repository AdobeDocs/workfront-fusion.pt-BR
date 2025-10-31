---
title: Adicionar um módulo a um cenário
description: Este artigo descreve o processo básico de adicionar um módulo a um cenário.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Adicionar um módulo a um cenário

Um cenário é composto de uma série de módulos que indicam como os dados devem ser transformados em um aplicativo ou transferidos entre aplicativos e serviços da Web. Você constrói um módulo adicionando e configurando módulos.

Este artigo descreve o processo básico de adicionar um módulo a um cenário. Para obter instruções mais específicas sobre como adicionar um cenário, consulte os outros artigos em [Adicionar módulos: índice do artigo](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote de Automação e Integração do Adobe Workfront</p><p>Workfront Ultimate</p><p>Workfront Prime e pacotes Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Standard</p><p>Trabalhar ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++## Adicionar o primeiro módulo a um cenário

O primeiro módulo de um cenário geralmente é um módulo acionador.

Para obter mais informações sobre módulos de acionador, consulte [Módulos de acionador](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) no artigo Visão geral do módulo.

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
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

1. Se você não estiver no editor de cenários do cenário ao qual deseja adicionar um módulo, clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Para adicionar um módulo a outro módulo, passe o mouse sobre a alça direita do módulo após a qual deseja adicionar um módulo, em seguida, clique em **Adicionar outro módulo** quando ele aparecer.

   A lista de conectores é aberta, mostrando todos os conectores já usados no cenário.

1. (Opcional) Para selecionar outro conector, clique em **Adicionar outro módulo** na lista e selecione o conector. Você pode digitar o nome do conector na barra de pesquisa da lista para filtrar a lista.
1. Configure o módulo.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Inserir um módulo entre módulos existentes em um cenário

1. Se você não estiver no editor de cenários do cenário ao qual deseja adicionar um módulo, clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no caminho pontilhado entre os módulos em que deseja inserir um módulo.
1. No menu exibido, selecione **Adicionar um módulo**.

A lista de conectores é aberta, mostrando todos os conectores já usados no cenário.

1. (Opcional) Para selecionar outro conector, clique em **Adicionar outro módulo** na lista e selecione o conector. Você pode digitar o nome do conector na barra de pesquisa da lista para filtrar a lista.
1. Configure o módulo.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Para criar um link para um módulo específico, adicione `?moduleId=<module-id>` à URL ao visualizar as seguintes páginas:
>
>* Página de edição do cenário (URL termina em `/edit`)
>* Uma execução de cenário específica (a URL termina em `/logs/<log-id>`)
>
>`<module-id>` refere-se ao número ao lado do rótulo do módulo ao visualizar o cenário.
>
>Isso pode ser útil ao depurar cenários ou copiar a configuração do módulo.
