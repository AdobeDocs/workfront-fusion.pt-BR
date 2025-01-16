---
title: Configurar um webhook para um serviço da Web sem um conector
description: Se um serviço Web não tiver um conector dedicado no Workfront Fusion, mas tiver suporte para o envio de webhooks, você poderá adicionar o serviço a um cenário usando o módulo Webhook personalizado como um acionador instantâneo.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---

# Configurar um webhook para um serviço da Web sem um conector

Se um serviço Web não tiver um conector dedicado no Workfront Fusion, mas tiver suporte para o envio de webhooks, você poderá adicionar o serviço a um cenário usando o módulo Webhook personalizado como um acionador instantâneo. Esse processo é chamado de recebimento de um webhook e requer alguma configuração no lado do aplicativo ao qual você está se conectando.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença do Adobe Workfront</td> 
   <td> <p>Novo: Padrão</p><p>Ou</p><p>Atual: trabalho ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecione ou Prime Workfront Plan: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Receber um webhook

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
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
