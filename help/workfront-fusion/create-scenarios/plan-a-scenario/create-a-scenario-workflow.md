---
title: Fluxo de trabalho para criar um cenário
description: Siga este fluxo de trabalho geral para criar um cenário
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

---

# Fluxo de trabalho para criar um cenário

Os cenários são criados para atender às necessidades de sua organização, com aplicativos e módulos que atendem aos seus casos de uso. No entanto, a criação de um cenário segue o mesmo fluxo de trabalho básico, independentemente do caso de uso. Este artigo descreve o processo básico de criação de um cenário.


* [Criar e nomear o cenário](#create-and-name-the-scenario)
* [Adicionar e configurar o primeiro módulo](#configure-the-first-module)
* [Criar conexões](#create-connections)
* [Adicionar e configurar módulos adicionais](#add-and-configure-additional-modules)
* [Mapear dados entre módulos](#map-data-between-modules)
* [Configurar roteamento](#configure-routing)
* [Configurar tratamento de erros](#configure-error-handling)
* [Definir configurações de cenário](#onfigure-scenario-settings)
* [Teste e revisão](#test-and-revise)
* [Ativar o cenário](#activate-the-scenario)
* [Atalhos de teclado do cenário do Workfront Fusion](#workfront-fusion-scenario-keyboard-shortcuts)

Atalhos de teclado



## Criar e nomear o cenário

1. Faça logon em sua conta do Workfront Fusion.
1. Clique em **[!UICONTROL Cenários]** ![Ícone de cenários](assets/scenarios-icon.png) no painel esquerdo.

   >[!NOTE]
   >
   >Se você não vir o painel de navegação esquerdo ou seus ícones, clique no ícone Menu ![Menu](assets/main-menu-icon-left-nav.png).

1. (Opcional) No painel [!UICONTROL **Pastas**], clique no ícone **[!UICONTROL Adicionar pasta]** ![Ícone Adicionar pasta](assets/add-folder-icon.png) e digite um nome como &quot;Cenários de prática&quot; para a sua primeira pasta.

1. (Opcional) Abra a pasta e clique em **[!UICONTROL Criar um novo cenário]** no canto superior direito da página.

1. Selecione o nome do espaço reservado **[!UICONTROL Novo cenário]** no canto superior esquerdo e digite um nome como &quot;Praticar cenário 1&quot;.

   ![Nomear o cenário](assets/name-the-scenario.png)

1. Continue com [Conecte o primeiro módulo](#2-connect-the-first-module) abaixo.

## Adicionar e configurar o primeiro módulo

O primeiro módulo para o cenário é um módulo acionador, que iniciará o cenário quando determinadas condições forem atendidas.

Para obter instruções sobre como adicionar o primeiro módulo a um cenário, consulte [Adicionar o primeiro módulo a um cenário](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario) no artigo Adicionar um módulo a um cenário.

Para obter instruções sobre como configurar um módulo, consulte [Configurar um módulo](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)

## Criar conexões

Ao configurar um módulo, você deve inserir ou criar uma conexão. O módulo usa essa conexão e as permissões que ela contém para acessar a data no aplicativo.

Para obter instruções básicas sobre como criar uma conexão, consulte [Criar uma conexão - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

Para casos de uso específicos envolvendo Google, Microsoft ou aplicativos sem conectores dedicados, consulte os outros artigos em [Conectar a aplicativos: índice do artigo](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-apps-toc.md).

## Adicionar e configurar módulos adicionais

Continue adicionando e configurando módulos adicionais.

Para obter instruções sobre como adicionar módulos, consulte os artigos listados em [Adicionar módulos: índice do artigo](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

## Mapear dados entre módulos

Você pode usar a saída dos módulos anteriores como entrada nos módulos subsequentes. Por exemplo, você pode criar um projeto Workfront em um módulo e fazer upload de um documento para esse módulo em um módulo subsequente.

Para obter instruções, consulte os artigos em [Mapear dados: índice do artigo](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

## Configurar roteamento

O roteamento permite que o cenário execute ações diferentes com base nos valores de dados.

Para obter instruções, consulte [Adicionar um módulo de roteador e configurar rotas](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Configurar tratamento de erros

A manipulação de erros permite que o cenário se recupere de erros. Você pode selecionar como deseja que o cenário reaja em diferentes situações de erro.

Para obter instruções, consulte [Adicionar tratamento de erros](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).

## Definir configurações de cenário

É possível definir configurações para o cenário como um todo, como agendar um cenário, fazer observações ou determinar como os dados são armazenados.

Para obter instruções, consulte os artigos em [Definir configurações de cenário: índice do artigo](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md).

## Teste e revisão

Testar o cenário permite determinar se ele está funcionando como esperado. Você pode revisar o cenário com base nos resultados e testar novamente.

1. Clique em **[!UICONTROL Executar uma vez]** no canto inferior esquerdo do editor de cenários.
1. Depois que o cenário terminar de ser executado, clique na bolha do inspetor de execução acima de cada módulo para ver a entrada de informações e a saída desse módulo.

   * Para obter informações gerais sobre a leitura de informações de execução do cenário, consulte [Fluxo de execução do cenário](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Para obter informações sobre pacotes processados, consulte [Execução de cenário, ciclos e fases no Adobe Workfront Fusion](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. No Workfront Fusion, clique em **[!UICONTROL Salvar]** ![Ícone Salvar](assets/save-icon.png) próximo ao canto inferior esquerdo para salvar seu progresso no cenário.

   >[!IMPORTANT]
   >
   >Salve com frequência à medida que você aprimora e testa um cenário.

## Ativar o cenário

Este cenário de exemplo não tem um módulo acionador. Se esse fosse um cenário usado para dados reais, ele começaria com um módulo de acionamento e a última coisa que você faria é ativá-lo. Após ativar um cenário, por padrão, ele é executado a cada 15 minutos. Você pode alterar isso definindo quando e com que frequência deseja que ele seja executado.

Para obter mais informações sobre como ativar cenários, consulte [Ativar ou desativar um cenário](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

Para obter informações sobre agendamentos, consulte [Agendar um cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Atalhos de teclado do cenário do Workfront Fusion

Você pode usar os seguintes atalhos de teclado ao criar ou editar um cenário:

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <thead> 
  <tr> 
   <th> <p>Ação</p> </th> 
   <th>[!DNL Windows]</th> 
   <th> <p>[!DNL MacOS]</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Salvar] </td> 
   <td>Ctrl+Shift+S</td> 
   <td>Cmd+Shift+S</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Executar Uma Vez]</td> 
   <td>Ctrl+Shift+Enter</td> 
   <td>Cmd+Shift+Enter</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abrir DevTool]</td> 
   <td>F12</td> 
   <td>Ctrl+Fn+F12</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar vários módulos]</td> 
   <td>Shift+Arrastar</td> 
   <td>Shift+Arrastar</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copiar]</td> 
   <td>Ctrl+C</td> 
   <td>Cmd+C</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Colar]</td> 
   <td>Ctrl+V</td> 
   <td>Cmd+V</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cole o cURL no cenário para criar o módulo HTTP</td> 
   <td colspan="2">Copie o cURL e cole em qualquer lugar no editor de cenários.<p>Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/add-modules/use-curl-create-http.md">Usar cURL para adicionar um módulo HTTP</a>.</td> 
  </tr> 
 </tbody> 
</table>





