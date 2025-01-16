---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gerenciar cenários bloqueados
description: Gerenciar cenários bloqueados em  [!DNL Adobe Workfront Fusion]
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# Gerenciar cenários bloqueados

Em alguns casos, um cenário pode estar temporariamente bloqueado em [!DNL Workfront Fusion]. Os cenários bloqueados serão automaticamente desbloqueados em 2 a 4 horas. É possível desbloquear cenários manualmente, mas isso geralmente não é recomendado.

Os cenários podem ser bloqueados por vários motivos:

* O Workfront Fusion não oferece suporte ao processamento paralelo de cenários agendados. Esses cenários são bloqueados no início da execução do cenário e desbloqueados quando ele é concluído. Se a execução for interrompida, o cenário pode não ser desbloqueado. Isso pode ocorrer quando um usuário força manualmente o cenário ou quando há um problema no sistema.

* A equipe de engenharia do Workfront Fusion pode bloquear um cenário porque ele está causando desempenho ou outros problemas.

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


## Desbloquear um cenário bloqueado

Cenários bloqueados serão desbloqueados de 2 a 4 horas a partir do momento em que foram bloqueados. É possível desbloquear um cenário manualmente antes de seu desbloqueio automático ser agendado.

>[!WARNING]
>
>Desbloquear um cenário manualmente pode causar erros nas execuções de um cenário. Recomendamos desbloquear manualmente os cenários somente quando um cenário está bloqueado devido à execução e interrupção de execuções como parte do design do cenário. Em outras circunstâncias, recomendamos que você aguarde até que o cenário seja desbloqueado automaticamente.


Para desbloquear manualmente um cenário bloqueado:

1. Vá para a página Detalhes do cenário do cenário bloqueado.
1. Clique em **[!UICONTROL Options]** no canto superior direito da tela.
1. Selecione **[!UICONTROL Unlock execution]**.
1. Clique em **[!UICONTROL Unlock]**.
   ![](assets/unlock-scenario.png)
