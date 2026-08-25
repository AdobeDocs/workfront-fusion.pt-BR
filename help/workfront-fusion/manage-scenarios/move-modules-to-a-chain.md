---
title: Mover módulos para uma cadeia
description: Você pode selecionar um grupo de módulos em um cenário e movê-los para um novo cenário encadeado, sem recriar manualmente mapeamentos ou estruturas de dados.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: f1a80f64edc410ae76bfbba1280df7232e2d09c5
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 17%

---

# Mover módulos para uma cadeia

>[!IMPORTANT]
>
>Esse recurso está no Beta e não é recomendado para fluxos de trabalho de produção de missão crítica. Como um recurso do Beta, o comportamento pode mudar e os casos de borda podem não ser totalmente tratados.

Você pode selecionar um grupo de módulos em um cenário e movê-los para um novo cenário encadeado, sem recriar manualmente mapeamentos ou estruturas de dados. Isso fornece uma maneira fácil de modular grandes cenários.

Quando você move um grupo de módulos em uma cadeia, o Workfront Fusion:

* Move os módulos selecionados para um cenário recém-criado.
* Abre o novo cenário em uma janela separada do navegador.
* Substitui os módulos selecionados no cenário original por um módulo de cenário Cadeia > Chamar um secundário.
* Cria automaticamente as estruturas de dados de entrada e saída necessárias para o novo cenário filho.
* Preserva o comportamento do cenário existente, de modo que o cenário continua a ser executado da mesma forma que antes dos módulos serem movidos.
* Atualiza os mapeamentos automaticamente:
  * Os módulos movidos para o cenário filho recebem dados por meio de Cadeia > Receber dados das entradas do módulo pai.
  * As saídas do cenário filho são expostas automaticamente de volta ao cenário pai.
  * Os mapeamentos existentes no blueprint são ajustados para corresponder à nova estrutura.

Para obter informações sobre o planejamento de cenários encadeados, consulte [Encadear vários cenários juntos](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

Para obter instruções sobre como configurar módulos de Cadeia, consulte [Módulos de Cadeia](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

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

Os módulos que você deseja mover para uma cadeia já devem existir em um cenário e você deve selecionar mais de um módulo.

## Limitações

Não é possível mover uma seleção de módulos para uma cadeia nas seguintes situações:

* Os módulos selecionados não fazem parte de um fluxo único ininterrupto. Por exemplo, não é possível selecionar módulos de duas rotas diferentes não conectadas ao mesmo tempo.
* A seleção inclui um módulo de webhook.
* A seleção inclui outro módulo de Cadeia.
* A seleção inclui um módulo de roteador e você não selecionou todas as rotas desse roteador.
* Um módulo selecionado tem uma rota de manipulador de erros, e você também não selecionou essa rota.

## Mover módulos para uma cadeia

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário que contém os módulos que você deseja mover.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Selecione os módulos que você deseja mover em uma cadeia, segurando o [!UICONTROL Shift] e clicando nos módulos que deseja mover.
1. Clique com o botão direito do mouse em um dos módulos selecionados.
1. Selecione **[!UICONTROL Mover para a Cadeia]**.
