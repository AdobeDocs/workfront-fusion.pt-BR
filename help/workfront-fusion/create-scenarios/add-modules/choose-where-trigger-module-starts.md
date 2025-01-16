---
title: Escolher onde um módulo de acionador é iniciado
description: Alguns módulos de acionamento permitem selecionar o primeiro pacote a partir do qual deseja que a recuperação de pacotes seja iniciada.
author: Becky
feature: Workfront Fusion
exl-id: 83628fa5-82e2-4f67-bfed-70a4c3c19f7f
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# Escolher onde um módulo de acionador é iniciado

Alguns módulos de acionamento permitem selecionar o primeiro pacote a partir do qual deseja que a recuperação de pacotes seja iniciada.

Você também pode especificar se deseja recuperar todos os pacotes ou apenas os pacotes de após uma data específica.

Para obter mais informações sobre módulos de acionador, consulte a seção [Módulos de acionador](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) no artigo Visão geral do módulo.

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
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Escolher onde um módulo de acionador é iniciado

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário em que deseja escolher o início do acionador.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Configure e salve um módulo de acionador.

   Ou

   Clique com o botão direito do mouse no ícone do módulo de acionador e selecione **Escolher onde começar**.

   ![](assets/choose-where-to-start.png)

1. Selecione uma opção na caixa **[!UICONTROL Choose where to start]** que aparece.

   As opções exibidas dependem das possibilidades de um determinado serviço. Elas podem incluir o seguinte:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody>
    <tr>
    <td>[!UICONTROL From now on] (padrão)</td>
    <td>Recupera todos os pacotes adicionados ou atualizados (dependendo das configurações) depois que esta opção for selecionada</td>
    </tr>
     <tr>
    <td>[!UICONTROL Since specific date]</td>
    <td>Recupera todos os pacotes adicionados ou atualizados (dependendo das configurações) após uma data e hora especificadas</td>
      </tr>
      <tr>
    <td>[!UICONTROL All]</td>
    <td>Recupera todos os pacotes disponíveis</td>
     </tr>
      <tr>
    <td>[!UICONTROL Choose manually]</td>
    <td>Permite selecionar o primeiro pacote a partir do qual a recuperação de pacotes deve começar</td>
     </tr>
     </tbody>
   </table>



   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Digite um nome para a nova conexão [!DNL DocuSign]</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>Selecione se a conta à qual deseja se conectar é uma conta de produção ou uma conta de demonstração.</td> 
     </tr> 
    </tbody> 
   </table>

   <!--Markdown 0032 placeholder-->
