---
title: Execute o especialista de pontuação de cenários
description: O especialista em pontuação de cenários pode ajudá-lo a garantir que seu cenário seja configurado de uma maneira que siga as práticas recomendadas. Ele verifica o cenário e fornece recomendações para sua estrutura e organização.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Execute o especialista de pontuação de cenários

>[!IMPORTANT]
>
>O Especialista em Pontuação de Cenários foi desabilitado temporariamente.

O especialista em pontuação de cenários pode ajudá-lo a garantir que seu cenário seja configurado de uma maneira que siga as práticas recomendadas. Ele verifica o cenário e fornece recomendações para sua estrutura e organização.

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

## Execute o especialista de pontuação de cenários

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
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

  Para obter instruções, consulte [Filtros de assinatura de evento no módulo Workfront > [!UICONTROL Eventos de observação]](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).
