---
title: Execute o especialista de pontuação de cenários
description: O especialista em pontuação de cenários pode ajudá-lo a garantir que seu cenário seja configurado de uma maneira que siga as práticas recomendadas. Ele verifica o cenário e fornece recomendações para sua estrutura e organização.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 1%

---

# Execute o especialista de pontuação de cenários

O especialista em pontuação de cenários pode ajudá-lo a garantir que seu cenário seja configurado de uma maneira que siga as práticas recomendadas. Ele verifica o cenário e fornece recomendações para sua estrutura e organização.

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

## Execute o especialista de pontuação de cenários

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário em que deseja executar o Especialista em Pontuação de Cenários.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no ícone Especialista em Pontuação de Cenário ![Especialista em pontuação de cenário](assets/scoring-expert-icon.png) próximo à parte inferior da tela.

   O painel Especialista em Pontuação de Cenário é aberto.
1. Clique em **Avaliar**.

O Especialista em Pontuação de Cenários retorna uma pontuação de 10 e mostra quais verificações foram bem-sucedidas ou falharam. Se uma verificação falhar, o especialista em pontuação de cenários dará recomendações sobre como garantir que o cenário atenda a essas verificações.

![Pontuação do cenário](assets/scenario-score.png)

## Verificações de pontuação de cenário

O especialista em pontuação de cenários usa as seguintes verificações:

* O cenário deve ser nomeado.
* Todos os módulos devem ser rotulados.
* O cenário deve ser executado em um cronograma definido.

  Para obter instruções, consulte [Agendar um cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* O tamanho do blueprint do cenário deve estar abaixo de 5 MB.

  Para obter mais informações, consulte [Medidas de proteção de desempenho do Fusion](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios).
* Se um módulo de acionador instantâneo do Workfront for usado, ele deverá ser filtrado.

  Para obter instruções, consulte [Filtros de assinatura de eventos no [!DNL Workfront] > [!UICONTROL Watch Events] módulo](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).
