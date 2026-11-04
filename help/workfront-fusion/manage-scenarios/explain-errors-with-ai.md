---
title: Explicar um erro de cenário com a IA
description: Quando uma execução de cenário falhar, você pode clicar em Explicar ao lado do erro para obter uma descrição curta e em linguagem simples do que deu errado e como corrigi-lo.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 565302f1d994819607051014d18779ccfb2645cb
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 15%
---
# Explicar um erro de cenário com a IA

Quando uma execução de cenário falha, a IA pode fornecer uma descrição curta e em linguagem simples do que deu errado e como corrigi-lo. A explicação aparece ao lado do erro original, para que você possa ler ambos juntos.

Você pode explicar erros nas seguintes áreas do Workfront Fusion:

* Os detalhes de erro do módulo no designer de cenários
* Os detalhes da execução no histórico de execução de um cenário
* A tabela [!UICONTROL Logs de Execuções com Falha] na página Insights

>[!NOTE]
>
>O botão **[!UICONTROL Explicar]** está disponível somente no novo designer de cenários. Não está disponível no designer de cenário herdado.
>
>Sua organização deve ter uma licença de IA para usar esse recurso.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote do Adobe Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Os pacotes Workfront Prime e Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p><p>Trabalho ou maior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Explicar um erro nos detalhes de saída do módulo

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja explicar um erro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Execute o cenário conforme agendado ou clicando em **Executar uma vez**.
1. Quando um módulo falhar, abra os detalhes de erro do módulo.
1. Clique em **[!UICONTROL Explicar]**.

   O botão está com erro.

   ![Explicar erro na saída do módulo](assets/explain-in-module-output.png)

A explicação aparece abaixo do erro.

>[!NOTE]
>
> * Enquanto a IA gera a explicação, um estado de carregamento é exibido.
> * Se a explicação não for gerada, clique em **[!UICONTROL Tentar novamente]**.
> * Se a organização atingir o limite de uso de IA, uma mensagem de limite de uso será exibida, em vez de uma explicação.

## Explicar um erro no histórico de execução de um cenário

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo e, em seguida, clique no cenário.
1. Clique em **[!UICONTROL Histórico]** próximo ao nome do cenário.
1. Clique na execução com falha que deseja exibir.

   Cada erro nos detalhes da execução tem um botão **[!UICONTROL Explicar]**.

1. Clique em **[!UICONTROL Explicar]** sob o erro que você deseja explicar.

   Se vários módulos falharem na execução, você poderá explicar cada erro por conta própria.

   ![Explicar no histórico de execução](assets/explain-in-execution-details.png)

Para obter mais informações sobre a exibição de uma execução, consulte [Exibir o histórico de execução de um cenário](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md) e [Exibir a execução de um cenário específico](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).

>[!NOTE]
>
> * Enquanto a IA gera a explicação, um estado de carregamento é exibido.
> * Se a explicação não for gerada, clique em **[!UICONTROL Tentar novamente]**.
> * Se a organização atingir o limite de uso de IA, uma mensagem de limite de uso será exibida, em vez de uma explicação.

## Explicar um erro na página de Insights

1. No Fusion, clique em **[!UICONTROL Insights]** na navegação à esquerda.
1. Na tabela [!UICONTROL Execuções com falha], passe o mouse sobre a linha com falha que deseja exibir.

   Um botão **[!UICONTROL Explicar]** é exibido.

1. Clique em **[!UICONTROL Explicar]**.

   ![Explicar na página de insights](assets/explain-failed-execution-log.png)

   Um pop-up é aberto mostrando o erro e a explicação da IA.

Para obter mais informações sobre a página Insights, consulte [Exibir o painel Insights de uma organização](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/view-insights-dashboard.md).

>[!NOTE]
>
> * Enquanto a IA gera a explicação, um estado de carregamento é exibido.
> * Se a explicação não for gerada, clique em **[!UICONTROL Tentar novamente]**.
> * Se a organização atingir o limite de uso de IA, uma mensagem de limite de uso será exibida, em vez de uma explicação.
