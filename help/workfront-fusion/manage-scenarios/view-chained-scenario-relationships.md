---
title: Exibir relacionamentos de cenário encadeados
description: Você pode criar um mapa dos relacionamentos entre cenários pai e filho.
author: Becky
feature: Workfront Fusion
exl-id: 0782c6b1-42a5-48de-bfa0-3ced6ed2bf7f
source-git-commit: aee2b35919e240cce5346df6d94a610c34b26e88
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 18%

---

# Exibir e gerenciar relacionamentos de cenário encadeados

Você pode criar um mapa dos relacionamentos entre cenários pai e filho. Você também pode usar o mapa para saltar para diferentes cenários na cadeia.

Para obter mais informações sobre cenários encadeados, consulte [Encadear vários cenários juntos](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

Para obter informações sobre como configurar cenários encadeados, consulte [Módulos de cadeia](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)

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

## Exibir um mapa de relacionamentos encadeados

Você pode exibir um mapa do cenário atual e seus cenários pai ou filho. O mapa exibe um diagrama do fluxo de dados nos cenários encadeados.

![Relacionamentos de cenário encadeados](assets/chained-scenario-relationships-2.png)

<!--get a better picture-->

Para exibir o mapa de relacionamento de um cenário encadeado:

1. Clique na guia **[!UICONTROL Cenário]** no painel esquerdo e clique no cenário.

   Ou

   Se você estiver trabalhando no cenário no Editor de cenários, clique na seta para a esquerda ![Sair da seta de edição](assets/exit-editing-arrow.png) próximo ao canto superior esquerdo da janela.

1. Clique na guia **Relações**.

   ![Guia Relações](assets/relations-tab.png)

1. Para obter detalhes gerais sobre cada cenário encadeado, verifique as tags.

   Cada cenário tem uma ou mais das seguintes tags:

   * Raiz: o cenário é o início da cadeia e não tem um cenário pai.
   * Pai: o cenário é um cenário pai.
   * Filho: o cenário é um cenário filho. Um cenário pode ser pai e filho.
   * Atual: esse é o cenário que o usuário está visualizando no momento. Em outras palavras, esse é o cenário do qual o usuário abriu o mapa de relações.

   ![Marcas de cenário no mapa de relações](assets/chained-scenario-maps-tag.png)
1. (Opcional) Para visualizar um pequeno diagrama de um cenário, passe o mouse sobre o cenário.
1. (Opcional) para ir diretamente para outro cenário no mapa, clique no cenário.

   O cenário clicado é aberto em outra janela.
1. (Opcional) Para alternar entre as exibições horizontal e vertical do mapa, clique em **Horizontal** ou **Vertical** próximo ao canto superior direito da página Detalhes do Cenário.
1. (Opcional) Para ver uma exibição simplificada do mapa, verifique o canto inferior direito da página.

   Isso pode ser conveniente se o mapa de cadeia for grande ou complexo.

   * Se você estiver visualizando apenas uma parte do mapa, essa parte será mais escura no mapa simplificado.
   * O cenário atual está marcado em azul no mapa simplificado.
1. Para exibir o histórico de execução da cadeia, clique na guia Histórico próximo à parte superior da exibição.

   Você pode clicar em um histórico para exibir os dados específicos transmitidos entre os cenários encadeados.
