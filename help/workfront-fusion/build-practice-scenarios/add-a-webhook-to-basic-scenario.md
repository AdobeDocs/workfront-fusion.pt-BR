---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Adicionar webhook a um cenário básico
description: Webhooks, também conhecidos como acionadores instantâneos, são um tipo específico de módulo de acionador que pode iniciar um cenário sempre que uma alteração for feita, em vez de em um determinado agendamento.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
TQID: https://experienceleague.adobe.com/V3cpVf8NzJdGjSZvPA0Hy0Uui-zSdd986plS1Us0oNI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 4cd8b43e9ce9a16aca16397ce140cdd2467bf7d4
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 13%
---
# Adicionar webhook a um cenário básico

Webhooks, também conhecidos como acionadores instantâneos, são um tipo específico de módulo de acionador que pode iniciar um cenário sempre que uma alteração for feita, em vez de em um determinado agendamento.

Neste exemplo, você adicionará um webhook para iniciar um cenário, assim que qualquer solicitação for enviada para uma fila de solicitações específica. O cenário converte essas solicitações em um projeto.

Este exemplo modifica o cenário criado em [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

>[!NOTE]
>
>O Workfront Fusion está fazendo a transição do editor de cenários para uma nova experiência. Durante essa transição, as experiências clássicas e novas estão disponíveis e você pode alternar entre elas a qualquer momento. Recomendamos usar a nova experiência. Para obter mais informações, consulte [Experiências novas e clássicas](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) no artigo Editor de cenários.

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

## Pré-requisitos

Você deve criar o cenário descrito em [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) antes de seguir este procedimento.

## Adicionar e configurar o webhook na nova experiência do (Recomendado)

* [Adicionar o módulo de webhook](#add-the-webhook-module)
* [Atualizar o segundo módulo](#update-the-second-module)
* [Testar e ativar](#test-and-activate)

### Adicionar o módulo de webhook

1. Abra o cenário no editor de cenários.
1. Clique com o botão direito no primeiro módulo e selecione **[!UICONTROL Excluir módulo]**.

   O módulo é excluído, deixando um espaço reservado em branco.

1. Clique no módulo em branco para abrir a lista de aplicativos e serviços.

   ![Seletor de aplicativos e serviços](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Selecione **Adobe Workfront**.
1. Selecione **Assistir Eventos**.
1. Clique em **Adicionar** ao lado do campo Webhook.
1. no campo Tipo de Registro, selecione **Problema**, para que o módulo acione alterações nos problemas.
1. No campo Estado, selecione **Novo estado**. Este é um campo obrigatório usado para o filtro, que este exemplo não cobre.
1. No campo Origem do Registro, selecione **Somente Novo Registro**. Isso permite que o cenário seja acionado quando um problema for adicionado, não quando um for atualizado ou excluído.
1. Clique em **Salvar** para salvar a configuração do módulo.

### Atualizar o segundo módulo

1. Abra o cenário.
1. Clique no módulo **Converter objeto** para abri-lo.
1. No campo ID do problema, exclua o bloco de ID preto. O bloco está preto porque o módulo do qual foi mapeado não está mais disponível.
1. Selecione o bloco de ID no primeiro módulo (Eventos de observação) para mapeá-lo para o segundo módulo.
1. Clique em **OK**.

### Testar e ativar

1. Clique no ícone **[!UICONTROL Executar uma vez]**.

   Executar uma vez é somente para ícones na nova experiência do. Passe o mouse sobre o ícone para ver a dica de ferramenta **[!UICONTROL Executar uma vez]**.

   ![botão executar cenário](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

   O cenário deve estar em execução para observar a nova solicitação.
1. Acesse o ambiente do Workfront ao qual o Fusion está se conectando e adicione um problema.

   O cenário deve ser executado.
1. Examine a saída para garantir que o cenário seja executado conforme esperado.
1. Quando estiver satisfeito com o funcionamento do cenário, clique no botão **Agendamento** para **Ligado**.

   Isso ativa o cenário.

   ![Alternância de agendamento](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. Clique no ícone **Salvar** ![Salvar ícone](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png) na área Controles para salvar seu progresso no cenário.

## Adicionar e configurar o webhook na experiência clássica

* [Adicionar o módulo de webhook (Clássico)](#add-the-webhook-module-classic)
* [Atualizar o segundo módulo (Clássico)](#update-the-second-module-classic)
* [Testar e ativar (Clássico)](#test-and-activate-classic)

### Adicionar o módulo de webhook (Clássico)

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

### Atualizar o segundo módulo (Clássico)

1. Abra o cenário.
1. Clique no módulo **Converter objeto** para abri-lo.
1. No campo ID do problema, exclua o bloco de ID preto. O bloco está preto porque o módulo do qual foi mapeado não está mais disponível.
1. Selecione o bloco de ID no primeiro módulo (Eventos de observação) para mapeá-lo para o segundo módulo.
1. Clique em **OK**.

### Testar e ativar (Clássico)

1. Clique em **[!UICONTROL Executar uma vez]** no canto inferior esquerdo do editor de cenários.

   O cenário deve estar em execução para observar a nova solicitação.
1. Acesse o ambiente do Workfront ao qual o Fusion está se conectando e adicione um problema.

   O cenário deve ser executado.
1. Examine a saída para garantir que o cenário seja executado conforme esperado.
1. Quando estiver satisfeito com o funcionamento do cenário, clique no botão de alternância **Agendamento** no canto inferior esquerdo da tela para **Ativado**.

   Isso ativa o cenário.
1. No Workfront Fusion, clique em **[!UICONTROL Salvar]** próximo ao canto inferior esquerdo para salvar seu progresso no cenário.
