---
title: Exibir e gerenciar versões de cenário
description: Você pode exibir, restaurar, renomear ou baixar blueprints de versões anteriores de um cenário.
author: Becky
feature: Workfront Fusion
exl-id: e7fd0351-b840-422c-b861-82ae110c703b
TQID: https://experienceleague.adobe.com/xVihxZH-fwPCIkryQAQEOWgeShtPTMXth4jEl5OLdbo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: eb4c1ed6991606928beccbb57a8a86182e58a9e7
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 14%

---

# Exibir e gerenciar versões de cenário

O Adobe Workfront Fusion salva uma versão do cenário sempre que ele é alterado.

Você pode exibir, restaurar, renomear ou baixar blueprints de versões anteriores de um cenário.

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

## Exibir e gerenciar o histórico de versões de um cenário

1. Clique em **[!UICONTROL Cenários]** ![Ícone de cenários](assets/scenarios-icon.png) no painel esquerdo e clique no cenário para abri-lo.
1. Clique no ícone [!UICONTROL Mais] ![Mais ícone](assets/more-icon.png) na parte inferior da tela e em **[!UICONTROL Versões Anteriores]**.

   Uma lista de versões anteriores é exibida.
1. (Opcional) Para renomear a versão, clique no menu Mais ![Mais menu](assets/more-icon-vertical.png) na linha dessa versão, selecione **Editar** e insira um nome no campo. Clique em **Salvar** para salvar o novo nome.

   Recomendamos dar um nome que descreva as alterações feitas nesta versão.
1. (Opcional) Para baixar o blueprint de uma versão anterior, clique no menu Mais ![Mais menu](assets/more-icon-vertical.png) na linha dessa versão e selecione **Baixar**.
1. (Opcional) Para comparar as alterações entre duas versões, clique em **Exibir alterações** dessa versão.

   Para obter detalhes e instruções sobre como comparar versões, consulte [Comparar versões de cenários](#compare-scenario-versions) neste artigo.
1. (Opcional) Para restaurar a versão, clique em **Restaurar** na linha dessa versão


   >[!NOTE]
   >
   >A versão restaurada do cenário não é salva automaticamente. Para salvar a versão restaurada do cenário, salve-a manualmente.



## Comparar versões de cenários

&#x200B;
A funcionalidade Exibir alterações mostra o que é diferente entre duas versões de cenário, lado a lado, para que você possa ver exatamente o que foi alterado antes de decidir restaurar uma mais antiga.

1. Clique em **[!UICONTROL Cenários]** ![Ícone de cenários](assets/scenarios-icon.png) no painel esquerdo e clique no cenário para abri-lo.
1. Clique no ícone [!UICONTROL Mais] ![Mais ícone](assets/more-icon.png) na parte inferior da tela e em **[!UICONTROL Versões Anteriores]**.

   Uma lista de versões anteriores é exibida.
&#x200B;
1. Clique em **Exibir alterações** para a versão do cenário que você deseja exibir.
1. A exibição **Revisar alterações** é aberta e compara essa versão com seu cenário atual.

   O painel Revisar alterações é aberto em uma exibição lado a lado de duas versões de cenário.

   * À esquerda, você verá a versão atual.
   * À direita, você verá a versão em que clicou. Essa é a versão que você pode restaurar.

   Para entender as alterações, consulte [Examinar alterações](#examine-changes) neste artigo.

1. Para selecionar outra versão para ambos os lados, clique na lista suspensa **Comparar de** ou **Comparar com** próxima à parte superior do painel e selecione outra versão de cenário.
1. Para trocar de lado, clique no botão **⇄** entre os cenários.
1. Para reverter para o cenário no lado direito, clique em **Reverter para a versão selecionada**

   As versões restauradas são salvas como novas versões e, portanto, podem ser revertidas no futuro.

   Para reverter para o cenário que está atualmente no lado esquerdo, troque de lado para que esteja à direita e clique em **Reverter para a versão selecionada**.


### Examinar alterações

&#x200B;
Cada alteração é mostrada no lado a que pertence e colorida pelo que a restauração faria
faça:

* Vermelho (esquerda): essa alteração não está na versão à direita e será removida se a versão for restaurada.
* Verde (direita): essa alteração está na versão à direita e será adicionada se a versão for restaurada.

Se algo foi alterado, em vez de removido ou adicionado, o valor é exibido em vermelho à esquerda e em verde à direita.
&#x200B;
As alterações são agrupadas em seções:
&#x200B;

* **Cenário**: nome, descrição e tipo.
* **Configurações de cenário**: opções de agendamento e processamento.
* **Módulos**: módulos adicionados, removidos, movidos ou reconfigurados.
* **Fluxos**: ramificações adicionadas, removidas ou reordenadas.
* **Rotas do roteador**: rotas e seu conteúdo.
* **Manipuladores de erros**: ramificações de tratamento de erros.
* **Grupos órfãos**: módulos desconectados na tela.
&#x200B;
Se as duas versões forem idênticas, a exibição mostrará a mensagem/ **Nenhuma diferença encontrada**.
&#x200B;


