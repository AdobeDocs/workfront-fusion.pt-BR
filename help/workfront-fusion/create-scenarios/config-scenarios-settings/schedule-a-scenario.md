---
content-type: reference
title: Agendar um cenário
description: Por padrão, um cenário é executado a cada 15 minutos. Você pode alterar isso definindo quando e com que frequência um cenário ativado é executado. Os cenários de fusão podem ser agendados para execução com uma frequência de até 5 minutos.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---

# Agendar um cenário

Por padrão, um cenário é executado a cada 15 minutos. Você pode alterar isso definindo quando e com que frequência um cenário ativado é executado. Os cenários de fusão podem ser agendados para execução com uma frequência de até 5 minutos.

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

+++

## Agendar um cenário

1. Clique na guia **Cenário** no painel esquerdo.
1. Selecione o cenário que deseja agendar.
1. No canto superior direito da página Detalhes do cenário, clique em **[!UICONTROL Opções]** > **[!UICONTROL Agendamento]**

   Ou

   Clique no ícone (relógio) **[!UICONTROL Agendamento]** no módulo de gatilho do cenário.

1. Insira informações nos seguintes campos:

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Executar cenário]</td> 
      <td> <p>Selecione a frequência na qual deseja executar o cenário e selecione o intervalo.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL Em intervalos regulares]</strong> </p> <p>Insira o número de minutos entre execuções. O valor padrão é 15 minutos.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>Insira a data e a hora em que deseja que o cenário seja executado. Use o formato <code>MM/DD/YYYY h:mm A</code>. Exemplo: <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Todo dia]</strong> </p> <p>Informe a hora em que deseja que o cenário seja executado. Use o formato <code>h:mm A</code>. Exemplo: <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong></strong>&lbrace;UICONTROL Dias da semana </p> <p>Dias: Selecione os dias da semana em que deseja que o cenário seja executado. Você pode selecionar um ou mais dias.</p> <p>Hora: Informe a hora em que deseja que o cenário seja executado nos dias selecionados. Use o formato <code>h:mm A</code>. Exemplo: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Dias do mês]</strong> </p> <p>Dias: Selecione os dias do mês em que deseja que o cenário seja executado. Você pode selecionar um ou mais dias.</p> <p>Hora: Informe a hora em que deseja que o cenário seja executado nos dias selecionados. Use o formato <code>h:mm A</code>. Exemplo: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Datas Especificadas]</strong> </p> <p>Meses: Selecione os meses em que deseja executar o cenário. Você pode selecionar um ou mais meses.</p> <p>Dias: Selecione os dias do mês em que deseja que o cenário seja executado. Você pode selecionar um ou mais dias.</p> <p>Hora: Informe a hora em que deseja que o cenário seja executado nos dias selecionados. Use o formato <code>h:mm A</code>. Exemplo: <code>11:00 PM</code></p> </li> 
       </ul> <p>Nota: Uma data deve existir para que um cenário seja executado nessa data. Por exemplo, um cenário agendado para somente o dia 31 do mês não será executado em fevereiro, abril, junho, setembro ou novembro, pois esses meses não têm um dia 31.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Agendamento avançado]</td> 
      <td>Você pode definir intervalos de tempo específicos durante os quais seu cenário deve ser executado. Você pode especificar intervalos de hora do dia, dias da semana ou meses. Para cada intervalo, clique em <strong>[!UICONTROL Adicionar]</strong> e preencha os campos conforme descrito no campo [!UICONTROL Executar cenário].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Iniciar]</td> 
      <td>Informe a data e a hora após as quais deseja que o cenário seja executado. Use o formato <code>MM/DD/YYYY h:mm A</code>. Exemplo: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Fim]</td> 
      <td>Informe a data e a hora antes da qual deseja que o cenário seja executado. Use o formato <code>MM/DD/YYYY h:mm A</code>. Exemplo: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL OK]** para salvar as configurações do agendamento e retornar ao cenário.
