---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Adicionar um webhook a um cenário básico
description: Webhooks, também conhecidos como acionadores instantâneos, são um tipo específico de módulo de acionador que pode iniciar um cenário sempre que uma alteração for feita, em vez de em um determinado agendamento.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Adicionar um webhook a um cenário básico

Webhooks, também conhecidos como acionadores instantâneos, são um tipo específico de módulo de acionador que pode iniciar um cenário sempre que uma alteração for feita, em vez de em um determinado agendamento.

Neste exemplo, você adicionará um webhook para iniciar um cenário, assim que qualquer solicitação for enviada para uma fila de solicitações específica. O cenário converte essas solicitações em um projeto.

Este exemplo modifica o cenário criado em [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote que inclua Automação e integração do Workfront</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Nenhum requisito de licença do Workfront Fusion.</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>É necessário ter uma conta para qualquer aplicativo ou serviço ao qual você se conecta com o Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Você deve criar o cenário descrito em [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) antes de seguir este procedimento.

## Adicionar e configurar o webhook


### Adicionar o módulo de webhook

1. Abra o cenário no editor de cenários.
1. Clique com o botão direito no primeiro módulo e selecione **Excluir módulo**.

   O módulo é excluído, deixando um espaço reservado em branco.

1. Clique no módulo em branco e selecione **Adobe Workfront** na lista de aplicativos.
1. Selecione **Assistir Eventos**.
1. Clique em **Adicionar** ao lado do campo Webhook.
1. no campo Tipo de Registro, selecione **Problema**, para que o módulo acione alterações nos problemas.
1. No campo Estado, selecione **Novo estado**. Este é um campo obrigatório usado para o filtro, que este exemplo não cobre.
1. No campo Origem do Registro, selecione **Somente Novo Registro**. Isso permite que o cenário seja acionado quando um problema for adicionado, não quando um for atualizado ou excluído.
1. Clique em **Salvar** para salvar a configuração do módulo.

## Atualizar o segundo módulo

1. Abra o cenário.
1. Clique no módulo **Converter objeto** para abri-lo.
1. No campo ID do problema, exclua o bloco de ID preto. O bloco está preto porque o módulo do qual foi mapeado não está mais disponível.
1. Selecione o bloco de ID no primeiro módulo (Eventos de observação) para mapeá-lo para o segundo módulo.
1. Clique em **OK**.



### Testar e ativar

1. Clique em **[!UICONTROL Executar uma vez]** no canto inferior esquerdo do editor de cenários.

   O cenário deve estar em execução para observar a nova solicitação.
1. Acesse o ambiente do Workfront ao qual o Fusion está se conectando e adicione um problema.

   O cenário deve ser executado.
1. Examine a saída para garantir que o cenário seja executado conforme esperado.
1. Quando estiver satisfeito com o funcionamento do cenário, clique no botão de alternância **Agendamento** no canto inferior esquerdo da tela para **Ativado**.

   Isso ativa o cenário.
1. No Workfront Fusion, clique em **[!UICONTROL Salvar]** próximo ao canto inferior esquerdo para salvar seu progresso no cenário.
