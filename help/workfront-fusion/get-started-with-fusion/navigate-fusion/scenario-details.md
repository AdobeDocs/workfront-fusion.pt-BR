---
title: Visão geral dos detalhes do cenário
description: Detalhes do cenário em  [!DNL Adobe Workfront Fusion]
author: Becky
feature: Workfront Fusion
exl-id: a6d07ed9-aa55-4993-9f78-7e691aa61049
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 1%

---

# Visão geral dos detalhes do cenário

A página de detalhes do cenário é a página inicial de um cenário específico. Ele fornece acesso a informações específicas para o cenário representado na página.

Também fornece acesso ao editor de cenários, onde você pode editar o cenário.

Para obter informações sobre o Editor de cenários, consulte [O Editor de cenários](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md)

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

## Abra a página [!UICONTROL Scenario detail]:

1. Clique na guia **[!UICONTROL Scenario]** no painel esquerdo e, em seguida, clique no cenário sobre o qual deseja obter detalhes.

   Ou

   Se estiver trabalhando no cenário no editor de cenários, clique na seta para a esquerda ![](assets/exit-editing-arrow.png) próxima ao canto superior esquerdo da janela.

1. Na página exibida, é possível revisar os elementos listados na tabela abaixo:

   ![](assets/scenario-detail-350x207.png)

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Modules diagram] </td> 
      <td>Essa guia exibe a representação visual do cenário. O diagrama é o mesmo que você verá no editor de cenários.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Reports] guia </td> 
      <td> <p>Abra esta guia para ver um gráfico do número de operações executadas por este cenário nos últimos 30 dias.</p>  </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL History] guia </td> 
      <td> <p>Abra esta guia para ver um histórico do cenário, incluindo edições feitas no cenário. </p> <p>A guia [!UICONTROL History] também fornece o histórico de execução de cada execução de cenário, que inclui o seguinte:</p> 
       <ul> 
        <li>Status de cada execução (sucesso ou erro)</li> 
        <li>Duração da execução</li> 
        <li>Número de operações</li> 
        <li>Tamanho da transferência de dados</li> 
        <li>Link para informações detalhadas</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Incomplete executions]</td> 
      <td> <p>Essa guia fornece informações sobre qualquer execução incompleta do cenário. Ela inclui as seguintes informações para cada execução incompleta:</p> 
       <ul> 
        <li>Data de criação</li> 
        <li>Tamanho da transferência de dados</li> 
        <li>Tente novamente</li> 
        <li>Solucionado</li> 
        <li>Número de tentativas</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Activate scenario] (Botão Ligar/Desligar)</td> 
      <td>Depois que um cenário é criado, ele precisa ser ativado para ser executado de acordo com seu agendamento. Ao clicar no botão Ligar/Desligar próximo ao canto superior direito, você pode ativar ou desativar o cenário. Quando ativado, o cenário é executado de acordo com seu agendamento.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Edit]</td> 
      <td>Clique no diagrama de cenário para abrir o editor de cenário e fazer alterações no cenário.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Options]</td> 
      <td> <p>Esse menu fornece opções adicionais sem precisar abrir o editor de cenários. Isso inclui:</p> 
       <ul> 
        <li>[!UICONTROL Scheduling]</li> 
        <li>[!UICONTROL Rename]</li> 
        <li>[!UICONTROL Clone]</li> 
        <li>[!UICONTROL Delete]</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Currently running]</td> 
      <td>Esta área mostra informações relacionadas à execução atual.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL History] painel</p> <p> </p> </td> 
      <td> <p>Essa área mostra informações relacionadas às últimas execuções do cenário. Para cada execução exibida:</p> 
       <ul> 
        <li>Data de execução</li> 
        <li>Status (sucesso ou falha)</li> 
        <li>Duração da execução</li> 
        <li>Tamanho da transferência de dados</li> 
        <li>Link para informações detalhadas</li> 
       </ul> </td> 
     </tr> 
         <tr> 
      <td role="rowheader"> <p>[!UICONTROL Events] painel</p>  </td> 
      <td>Essa área mostra informações sobre eventos relacionados ao cenário.  </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Processing banner]</p>  </td>

   <td>Se o cenário foi executado recentemente, você poderá ver um banner com a seguinte redação:<p><code>Data is still being processed. Only partial scenario history will show until processing is complete.</code></p>Isso é exibido enquanto os detalhes da execução são gravados no armazenamento. O processamento ocorre imediatamente após a execução do cenário. e não deve durar mais do que alguns minutos. Os detalhes da execução do cenário podem não estar visíveis enquanto a execução estiver sendo processada.</td> 
     </tr> 
    </tbody> 
   </table>
