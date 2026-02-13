---
title: Escolher onde um módulo de acionador é iniciado
description: Alguns módulos de acionamento permitem selecionar o primeiro pacote a partir do qual deseja que a recuperação de pacotes seja iniciada.
author: Becky
feature: Workfront Fusion
exl-id: 83628fa5-82e2-4f67-bfed-70a4c3c19f7f
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 33%

---

# Escolher onde um módulo de acionador é iniciado

Alguns módulos de acionamento permitem selecionar o primeiro pacote a partir do qual deseja que a recuperação de pacotes seja iniciada.

Você também pode especificar se deseja recuperar todos os pacotes ou apenas os pacotes de após uma data específica.

Para obter mais informações sobre módulos de acionador, consulte a seção [Módulos de acionador](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) no artigo Visão geral do módulo.

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
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Escolher onde um módulo de acionador é iniciado

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja escolher o início do acionador.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Configure e salve um módulo de acionador.

   Ou

   Clique com o botão direito do mouse no ícone do módulo de acionador e selecione **Escolher onde começar**.

   ![Escolher onde começar](assets/choose-where-to-start.png)

1. Na caixa **[!UICONTROL Escolher onde começar]**, selecione uma opção.

   As opções exibidas dependem das possibilidades de um determinado serviço. Elas podem incluir o seguinte:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody>
    <tr>
    <td>[!UICONTROL De agora em diante] (padrão)</td>
    <td>Recupera todos os pacotes adicionados ou atualizados (dependendo das configurações) depois que esta opção for selecionada</td>
    </tr>
     <tr>
    <td>[!UICONTROL Desde a data específica]</td>
    <td>Recupera todos os pacotes adicionados ou atualizados (dependendo das configurações) após uma data e hora especificadas</td>
      </tr>
      <tr>
    <td>[!UICONTROL Tudo]</td>
    <td>Recupera todos os pacotes disponíveis</td>
     </tr>
      <tr>
    <td>[!UICONTROL Escolher manualmente]</td>
    <td>Permite selecionar o primeiro pacote a partir do qual a recuperação de pacotes deve começar</td>
     </tr>
     </tbody>
   </table>
