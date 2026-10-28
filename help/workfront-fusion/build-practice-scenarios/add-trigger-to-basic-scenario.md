---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Adicionar um módulo de acionador a um cenário básico
description: Saiba como adicionar um módulo de acionamento para permitir que o cenário procure novas solicitações periodicamente e as converta em projetos.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
TQID: https://experienceleague.adobe.com/xepLecibr9U6FpQM0neDy15DbFGF55rR6gVYvo644H4
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 347280547bea92c0ee498da519495569a3cac661
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 11%
---
# Adicionar um módulo de acionador a um cenário básico

Os módulos de acionamento são colocados no início de um cenário. Esses módulos iniciam uma execução de cenário quando há uma alteração em um determinado serviço. A alteração pode ser uma criação de novos registros, exclusão de um registro, atualização de um registro e assim por diante. Você especifica os critérios para as alterações que iniciam o cenário.

Os módulos de sondagem verificam o serviço em um intervalo de tempo definido e retornam informações sobre as alterações ocorridas durante esse intervalo de tempo. Se não houver alterações, o acionador não executará o cenário.

Neste exemplo, você adicionará um módulo de acionador que é executado a cada 15 minutos e iniciará um cenário se alguma solicitação tiver sido enviada para uma fila específica. O cenário converte essas solicitações em um projeto.

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

## Adicionar e configurar o módulo de acionador na nova experiência do (recomendado)

* [Adicionar o módulo de acionamento](#add-the-trigger-module)
* [Agendar o módulo de acionamento](#schedule-the-trigger-module)
* [Atualizar o segundo módulo](#update-the-second-module)
* [Testar e ativar](#test-and-activate)

### Adicionar o módulo de acionamento

1. Abra o cenário no editor de cenários.
1. Clique com o botão direito do mouse no primeiro módulo (Pesquisa) e selecione **[!UICONTROL Excluir módulo]**.

   O módulo é excluído, deixando um espaço reservado em branco.

1. Clique no módulo em branco para abrir a lista de aplicativos e serviços.

   ![Seletor de aplicativos e serviços](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Selecione **Adobe Workfront**.
1. Selecione **Assistir Registro**.
1. Certifique-se de que o módulo usa a mesma conexão que o restante dos módulos no cenário.
1. No campo Tipo de Registro, selecione **Problema**.
1. No campo Filtro, selecione **Somente novos registros**.
1. Na caixa Saídas, selecione `ID`, `Name` e `Project ID`.
1. Clique em **OK** para salvar as configurações do módulo.

   A janela Escolha onde iniciar é exibida.

1. Selecione **De agora em diante**.

### Agendar o módulo de acionamento

1. Clique no ícone do relógio no módulo Observar registro.

   ![Ícone de relógio no módulo Observar Registro](assets/clock-icon-on-watch-record.png)

   A janela de configuração Programação é aberta.

1. No campo Executar cenário, selecione **Em intervalos regulares**.

1. Clique em **OK**.

### Atualizar o segundo módulo

Como o primeiro módulo foi substituído, o segundo módulo deve ser mapeado para o novo primeiro módulo.

1. Abra o módulo Converter objeto.
1. No campo ID do problema, exclua o bloco de ID preto. O bloco está preto porque o módulo do qual foi mapeado não está mais disponível.
1. Selecione o bloco de ID no primeiro módulo (Registro de observação) para mapeá-lo para o segundo módulo.
1. Clique em **OK**.

### Testar e ativar

1. Acesse o ambiente do Workfront ao qual o Fusion está se conectando e adicione um problema.
1. Clique no ícone **[!UICONTROL Executar uma vez]**.

   Executar uma vez é somente para ícones na nova experiência do. Passe o mouse sobre o ícone para ver a dica de ferramenta **[!UICONTROL Executar uma vez]**.

   ![botão executar cenário](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

1. Examine a saída para garantir que o cenário seja executado conforme esperado.
1. Quando estiver satisfeito com o funcionamento do cenário, clique no botão **Agendamento** para **Ligado**.

   Isso ativa o cenário.

   ![Alternância de agendamento](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. Clique no ícone **Salvar** ![Salvar ícone](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png) na área Controles para salvar seu progresso no cenário.

   >[!IMPORTANT]
   >
   >Salve com frequência à medida que você aprimora e testa um cenário.

## Adicionar e configurar o módulo de acionamento na experiência do Classic

* [Adicionar o módulo de acionamento (Clássico)](#add-the-trigger-module-classic)
* [Agendar o módulo de acionador (Clássico)](#schedule-the-trigger-module-classic)
* [Atualizar o segundo módulo (Clássico)](#update-the-second-module-classic)
* [Testar e ativar (Clássico)](#test-and-activate-classic)

### Adicionar o módulo de acionamento (Clássico)

1. Abra o cenário no editor de cenários.
1. Clique com o botão direito do mouse no primeiro módulo (Pesquisa) e selecione **Excluir módulo**.

   O módulo é excluído, deixando um espaço reservado em branco.

1. Clique no módulo em branco e selecione **Adobe Workfront** na lista de aplicativos.
1. Selecione **Assistir Registro**.
1. Certifique-se de que o módulo usa a mesma conexão que o restante dos módulos no cenário.
1. No campo Tipo de Registro, selecione **Problema**.
1. No campo Filtro, selecione **Somente novos registros**.
1. Na caixa Saídas, selecione `ID`, `Name` e `Project ID`.
1. Clique em **OK** para salvar as configurações do módulo.

   A janela Escolha onde iniciar é exibida.

1. Selecione **De agora em diante**.

### Agendar o módulo de acionador (Clássico)

1. Clique no relógio no módulo Watch Record.

   A janela de configuração Programação é aberta.

1. No campo Executar cenário, selecione **Em intervalos regulares**.

1. Clique em **OK**.

### Atualizar o segundo módulo (Clássico)

Como o primeiro módulo foi substituído, o segundo módulo deve ser mapeado para o novo primeiro módulo.

1. Abra o módulo Converter objeto.
1. No campo ID do problema, exclua o bloco de ID preto. O bloco está preto porque o módulo do qual foi mapeado não está mais disponível.
1. Selecione o bloco de ID no primeiro módulo (Registro de observação) para mapeá-lo para o segundo módulo.
1. Clique em **OK**.

### Testar e ativar (Clássico)

1. Acesse o ambiente do Workfront ao qual o Fusion está se conectando e adicione um problema.
1. Clique em **[!UICONTROL Executar uma vez]** no canto inferior esquerdo do editor de cenários.
1. Examine a saída para garantir que o cenário seja executado conforme esperado.
1. Quando estiver satisfeito com o funcionamento do cenário, clique no botão de alternância **Agendamento** no canto inferior esquerdo da tela para **Ativado**.

   Isso ativa o cenário.
1. No Workfront Fusion, clique em **[!UICONTROL Salvar]** próximo ao canto inferior esquerdo para salvar seu progresso no cenário.

   >[!IMPORTANT]
   >
   >Salve com frequência à medida que você aprimora e testa um cenário.

## Recursos

* Para obter mais informações sobre módulos de acionador, consulte [Módulos de acionador](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) no artigo Visão geral de módulos.
