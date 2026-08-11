---
title: Definir Opções de Notificação
description: As opções de notificação por email são definidas no nível da equipe.
author: Becky
feature: Workfront Fusion
exl-id: 570a09fc-01a9-4952-8a2b-8bfdd86d0bd8
TQID: https://experienceleague.adobe.com/-HytP4gfrhiiSn-dg5ndg1YC6NTMC-NURYzSFgO5kIo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 90a58033e240271b88d01b9daef9763f38264056
workflow-type: tm+mt
source-wordcount: 665
ht-degree: 13%

---

# Definir opções de notificação

Na sua organização do que usa o Unified Shell da Adobe, você recebe notificações por meio da área Notificações da Adobe.

Se sua organização não tiver sido migrada para o Adobe Unified Shell, você poderá escolher as notificações que uma equipe receberá. As notificações são definidas no nível da equipe.

Você pode controlar para quais situações as notificações são enviadas:

* Notificar em aviso: o Fusion envia uma notificação quando uma execução de cenário registra um aviso.
* Notificar em caso de erro: o Fusion envia uma notificação quando a execução de um cenário falha.
* Notificar quando o cenário está desativado: o Fusion envia uma notificação quando um cenário é desativado automaticamente, por exemplo, após muitos erros consecutivos.

Você pode definir notificações no nível da equipe ou do cenário. As notificações no nível do cenário substituem as notificações definidas no nível da equipe. Isto é, se um cenário contradiz diretamente um cenário do grupo, o cenário é seguido. As configurações de notificação do grupo mostram se há substituições para esta configuração.

Por padrão, todos os tipos de notificações são ativados no Workfront Fusion.

>[!IMPORTANT]
>
>Para receber notificações do Workfront Fusion, você deve ter as notificações do Fusion ativadas nas configurações de notificação do Adobe CX Enterprise. Você pode acessar essas configurações clicando no sino de notificação no canto superior direito da tela e clicando no ícone de configurações.

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
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Função</td> 
   <td> 
     <p>Você deve ser membro da organização e da equipe do Fusion para a qual está ajustando as configurações de notificação.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Exibir e gerenciar configurações de notificação no nível da equipe

1. No Workfront Fusion, clique em **Visão geral da equipe** na navegação à esquerda.
1. Clique na guia **Opções de notificação**.

   A lista de opções de Notificação é aberta. Se houver sobreposições, o número de sobreposições aparecerá ao lado dessa configuração.

1. (Condicional) Se houver substituições, para ver quais cenários substituem a configuração de notificação do grupo, clique no menu de três pontos dessa configuração.

   Você pode clicar em um cenário neste menu para ir diretamente para esse cenário.

   ![Substituir menu de cenários](assets/view-notification-override.png)

1. Para restaurar as configurações padrão de um tipo de notificação, consulte [Restaurar padrões de notificação](#restore-notification-defaults) neste artigo.

As alterações feitas na lista de opções de Notificações são salvas automaticamente.

## Definir configurações de notificação em nível de cenário

As configurações de notificação para cenários individuais são definidas no painel Configurações do cenário.

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário ao qual deseja adicionar um filtro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no ícone [!UICONTROL Configurações de cenário] ícone ![Configurações de cenário](assets/scenario-settings-icon.png) na parte inferior do cenário.
1. No painel Configurações do cenário, clique em **Mostrar configurações avançadas** na parte inferior do painel.
1. Ajuste as configurações **Notificar sobre aviso**, **Notificar sobre erro** e **Notificar quando o cenário estiver desabilitado**, conforme desejado.
1. Clique em **OK** para salvar e sair das configurações do cenário.

## Restaurar padrões de notificação

Você pode restaurar a configuração padrão de notificação de um grupo na guia Opções de notificação. Isso define a opção de notificação como ativada e remove todas as sobreposições de notificação de cenário desse tipo de notificação.

Se o tipo de notificação estiver definido como padrão no momento, o ícone **Restaurar para padrão** não estará visível.

1. No Workfront Fusion, clique em **Visão geral da equipe** na navegação à esquerda.
1. Clique na guia **Opções de notificação**.

   A lista de opções de Notificação é aberta. Se um tipo de notificação não estiver definido atualmente como padrão, o ícone Restaurar para padrão ficará visível para esse tipo de notificação.

   ![Restaurar para o padrão visível](assets/restore-notification-defaults.png)

1. Para restaurar as configurações padrão desse tipo de notificação, incluindo qualquer substituição de cenário, clique no ícone **Redefinir para padrão** ![Redefinir para padrão](assets/restore-default-icon.png) desse tipo de notificação.

As alterações feitas na lista de opções de Notificações são salvas automaticamente.

<!--

## Set notification options

If your organization is not on the Adobe Unified Shell, you can set notification settings directly in Fusion.

Email notification options are set on the team level.

1. In the left navigation panel, click **[!UICONTROL Team]**
1. Select the **[!UICONTROL Notification Options]** tab.
1. Enable the notifications that you want the team to receive.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">'[!UICONTROL Warning in scenario run]'</td> 
      <td> <p>Receive an email when there is a warning in a scenario run</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Errors in scenario run]</td> 
      <td>Receive an email when there is an error in a scenario run.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Scenario deactivation]</p> </td> 
      <td><p>Receive an email when a scenario deactivates.</p><p>In some cases, a scenario might be deactivated by the Workfront Fusion engineering team because the scenario is causing performance or other issues. In these cases, you do not receive notifications in Workfront Fusion. </p></td>

</tr>
</tbody>
</table>

Changes to notification options save automatically.

-->
