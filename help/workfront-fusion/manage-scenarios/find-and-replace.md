---
title: Localizar e substituir variáveis, fontes e conexões em um cenário
description: Use Localizar e substituir para substituir uma variável mapeada, remapear referências de um módulo de origem para outro ou copiar uma conexão para outros módulos em seu cenário.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 15%
---

# Localizar e substituir variáveis, fontes e conexões em um cenário

>[!NOTE]
>
>Essa funcionalidade está disponível somente na nova experiência do editor de cenários. Para obter mais informações, consulte [Experiências novas e clássicas](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) no artigo Editor de cenários.

Localizar e substituir permite que você faça a mesma alteração em vários módulos de uma só vez. É possível:

* Substitua uma variável mapeada em todo o cenário ou em um módulo.
* Remapeie as referências de um módulo de origem para outro.
* Copie uma conexão para um ou todos os módulos compatíveis do mesmo aplicativo.

Antes de fazer uma alteração, Localizar e substituir mostra uma pré-visualização dos módulos que serão afetados.

Na experiência clássica, você pode usar as ferramentas de conexão Trocar variável, Remapear origem e Trocar na DevTool para executar essas tarefas. Para obter mais informações, consulte [Depurar um cenário](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md).

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
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Abrir Localizar e substituir

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja fazer alterações.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no ícone **Localizar e substituir** ![Localizar e substituir](assets/find-replace-icon.png) na área Controles.

   Talvez seja necessário clicar no ícone de três pontos na área Controles para ver o ícone Localizar e substituir.

Localize e substitua as aberturas no painel no lado direito da tela de desenho.

## Substituir uma variável

Use a guia **Variável** para substituir uma variável mapeada.

1. Abra Localizar e substituir e clique na guia **Variável**.
1. No campo Variável a ser encontrada, cole na variável que deseja substituir.
1. No campo Substituir por, cole na variável que substituirá a variável anterior.
1. No campo Módulo, escolha o módulo ao qual a alteração será aplicada ou selecione **Cenário completo** para aplicar a alteração a todos os módulos afetados no cenário.
1. Clique em **Substituir**
1. Revise a visualização dos módulos que serão afetados. Para ir para um módulo na tela de desenho, selecione a linha correspondente na visualização.
1. Clique em **Aplicar**.

## Remapear uma origem

Use a guia **Source** para alterar a qual módulo os mapeamentos em outros módulos se referem.

1. Abra Localizar e substituir e clique na guia **Source**.
1. No campo Módulo do Source, selecione o módulo de origem ao qual os mapeamentos se referem atualmente.
1. Nos campos do módulo de Direcionamento, selecione o módulo ao qual eles devem se referir.
1. No campo Módulo, escolha o módulo ao qual a alteração será aplicada ou selecione **Cenário completo** para aplicar a alteração a todos os módulos afetados no cenário.
1. Clique em **Substituir**
1. Revise a visualização dos módulos que serão afetados. Para ir para um módulo na tela de desenho, selecione a linha correspondente na visualização.
1. Clique em **Aplicar**.

## Copiar uma conexão para outros módulos

Use a guia **Conexão** para usar a mesma conexão em mais de um módulo do mesmo aplicativo.

1. Abra Localizar e substituir e clique na guia **Conexão**.
1. No campo Conexão de, selecione um módulo que atualmente tenha a conexão que você deseja usar para outros módulos.
1. No campo Aplicar a, escolha o módulo ao qual a alteração será aplicada ou se ela será aplicada a todos os módulos compatíveis no cenário.
1. Clique em **Aplicar**.
