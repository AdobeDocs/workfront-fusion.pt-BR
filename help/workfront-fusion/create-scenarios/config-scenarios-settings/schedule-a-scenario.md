---
content-type: reference
title: Agendar um cenário
description: Por padrão, um cenário é executado a cada 15 minutos. Você pode alterar isso definindo quando e com que frequência um cenário ativado é executado. Os cenários de fusão podem ser agendados para execução com uma frequência de até 5 minutos.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Agendar um cenário

Por padrão, um cenário é executado a cada 15 minutos. Você pode alterar isso definindo quando e com que frequência um cenário ativado é executado. Os cenários de fusão podem ser agendados para execução com uma frequência de até 5 minutos.

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
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Workfront] Plano: Sua organização deve comprar [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plano: [!DNL Workfront Fusion] está incluído.</li></ul>
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

## Agendar um cenário

1. Clique na guia **Cenário** no painel esquerdo.
1. Selecione o cenário que deseja agendar.
1. No canto superior direito da página Detalhes do cenário, clique em **[!UICONTROL Options]** > **[!UICONTROL Scheduling]**

   Ou

   Clique no ícone **[!UICONTROL Scheduling]** (relógio) no módulo do acionador do cenário.

1. Insira informações nos seguintes campos:

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Run scenario]</td> 
      <td> <p>Selecione a frequência na qual deseja executar o cenário e selecione o intervalo.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL At regular intervals]</strong> </p> <p>Insira o número de minutos entre execuções. O valor padrão é 15 minutos.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>Insira a data e a hora em que deseja que o cenário seja executado. Use o formato <code>MM/DD/YYYY h:mm A</code>. Exemplo: <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Every day]</strong> </p> <p>Informe a hora em que deseja que o cenário seja executado. Use o formato <code>h:mm A</code>. Exemplo: <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Days of the week]</strong> </p> <p>Dias: Selecione os dias da semana em que deseja que o cenário seja executado. Você pode selecionar um ou mais dias.</p> <p>Hora: Informe a hora em que deseja que o cenário seja executado nos dias selecionados. Use o formato <code>h:mm A</code>. Exemplo: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Days of the month]</strong> </p> <p>Dias: Selecione os dias do mês em que deseja que o cenário seja executado. Você pode selecionar um ou mais dias.</p> <p>Hora: Informe a hora em que deseja que o cenário seja executado nos dias selecionados. Use o formato <code>h:mm A</code>. Exemplo: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Specified dates]</strong> </p> <p>Meses: Selecione os meses em que deseja executar o cenário. Você pode selecionar um ou mais meses.</p> <p>Dias: Selecione os dias do mês em que deseja que o cenário seja executado. Você pode selecionar um ou mais dias.</p> <p>Hora: Informe a hora em que deseja que o cenário seja executado nos dias selecionados. Use o formato <code>h:mm A</code>. Exemplo: <code>11:00 PM</code></p> </li> 
       </ul> <p>Nota: Uma data deve existir para que um cenário seja executado nessa data. Por exemplo, um cenário agendado para somente o dia 31 do mês não será executado em fevereiro, abril, junho, setembro ou novembro, pois esses meses não têm um dia 31.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Advanced scheduling]</td> 
      <td>Você pode definir intervalos de tempo específicos durante os quais seu cenário deve ser executado. Você pode especificar intervalos de hora do dia, dias da semana ou meses. Para cada intervalo, clique em <strong>[!UICONTROL Add]</strong> e preencha os campos conforme descrito no campo [!UICONTROL Run scenario].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Start]</td> 
      <td>Informe a data e a hora após as quais deseja que o cenário seja executado. Use o formato <code>MM/DD/YYYY h:mm A</code>. Exemplo: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL End]</td> 
      <td>Informe a data e a hora antes da qual deseja que o cenário seja executado. Use o formato <code>MM/DD/YYYY h:mm A</code>. Exemplo: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL OK]** para salvar as configurações do cronograma e retornar ao cenário.
