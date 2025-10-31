---
title: Configurar um webhook para um serviço da Web sem um conector
description: Se um serviço Web não tiver um conector dedicado no Workfront Fusion, mas tiver suporte para o envio de webhooks, você poderá adicionar o serviço a um cenário usando o módulo Webhook personalizado como um acionador instantâneo.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---

# Configurar um webhook para um serviço da Web sem um conector

Se um serviço Web não tiver um conector dedicado no Workfront Fusion, mas tiver suporte para o envio de webhooks, você poderá adicionar o serviço a um cenário usando o módulo Webhook personalizado como um acionador instantâneo. Esse processo é chamado de recebimento de um webhook e requer alguma configuração no lado do aplicativo ao qual você está se conectando.

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

## Receber um webhook

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja adicionar um webhook.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Adicione o módulo **Webhooks > Webhook personalizado** para iniciar o cenário.
1. Clique em **Adicionar** ao lado do campo Webhook.
1. Digite um **nome do Webhook** na caixa que exibe
1. (Opcional) configure o webhook.

   Para obter instruções, consulte [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

1. Clique em **Salvar**.

1. Clique em **Copiar endereço para a área de transferência** e em **OK**.

1. Faça logon no serviço da Web e faça o seguinte:

   1. Na área Configurações do serviço Web, crie um webhook.

      Instruções específicas dependem do aplicativo. Recomendamos pesquisar a documentação do aplicativo para &quot;Criar um webhook&quot;.
   1. Cole o endereço copiado para a área de transferência na etapa 3.
   1. Selecione o evento que acionará o webhook.

1. Execute o cenário.

   Quando o evento ou eventos ocorrem, o módulo Webhook personalizado é acionado e o cenário é executado.
