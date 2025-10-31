---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Adicionar um módulo de acionamento a um cenário básico
description: Saiba como adicionar um módulo de acionamento para permitir que o cenário procure novas solicitações periodicamente e as converta em projetos.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
source-git-commit: 3a977d805c10fda7209b0634c6e32e818a980691
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 1%

---

# Adicionar um módulo de acionamento a um cenário básico

Os módulos de acionamento são colocados no início de um cenário. Esses módulos iniciam uma execução de cenário quando há uma alteração em um determinado serviço. A alteração pode ser uma criação de novos registros, exclusão de um registro, atualização de um registro e assim por diante. Você especifica os critérios para as alterações que iniciam o cenário.

Os módulos de sondagem verificam o serviço em um intervalo de tempo definido e retornam informações sobre as alterações ocorridas durante esse intervalo de tempo. Se não houver alterações, o acionador não executará o cenário.

Neste exemplo, você adicionará um módulo de acionador que é executado a cada 15 minutos e iniciará um cenário se alguma solicitação tiver sido enviada para uma fila específica. O cenário converte essas solicitações em um projeto.

Este exemplo modifica o cenário criado em [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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

## Pré-requisitos

Você deve criar o cenário descrito em [Criar um cenário básico](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) antes de seguir este procedimento.

## Adicionar e configurar o módulo acionador

### Adicionar o módulo de acionamento

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

### Agendar o módulo de acionamento

1. Clique no relógio do módulo Watch Records.

   A janela de configuração Programação é aberta.

1. No campo Executar cenário, selecione **Em intervalos regulares**.

1. Clique em **OK**.

### Atualizar o segundo módulo

Como o primeiro módulo foi substituído, o segundo módulo deve ser mapeado para o novo primeiro módulo.

1. Abra o módulo Converter objeto.
1. No campo ID do problema, exclua o bloco de ID preto. O bloco está preto porque o módulo do qual foi mapeado não está mais disponível.
1. Selecione o bloco de ID no primeiro módulo (Registros de observação) para mapeá-lo para o segundo módulo.
1. Clique em **OK**.

### Testar e ativar

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
