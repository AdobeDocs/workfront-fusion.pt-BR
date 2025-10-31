---
title: Copiar módulos ou cenários
description: Você pode copiar módulos, grupos de módulos ou cenários inteiros no Adobe Workfront Fusion. Essa capacidade permite reutilizar cenários ou partes de cenários sem precisar criá-los novamente.
author: Becky
feature: Workfront Fusion
exl-id: 5cece7d4-b2c7-4276-8a6f-f65bad799c7a
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# Copiar módulos ou cenários

Você pode copiar módulos, grupos de módulos ou cenários inteiros no Adobe Workfront Fusion. Essa capacidade permite reutilizar cenários ou partes de cenários sem precisar criá-los novamente.

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

Os módulos devem existir em um cenário antes que você possa copiá-los.

## Copiar um módulo ou um grupo de módulos

Ao copiar um módulo, a cópia retém todos os valores de campo e configurações do módulo original.

Você pode colar o módulo ou os módulos em outra área do mesmo cenário ou em um cenário diferente.

Considere o seguinte ao colar módulos em um cenário diferente:

* Quaisquer valores de campo que extraem informações de outro módulo que você não copiou não poderão mais acessar essas informações. Você deve definir esses campos para obter informações do novo cenário.
* Se você colar os módulos em um cenário de propriedade de outra equipe ou organização, todas as conexões deverão ser atualizadas para conexões de propriedade da equipe ou organização que possui o novo cenário.

### Copiar módulos

Copiar um grupo de módulos é semelhante a copiar um único módulo.

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja copiar um módulo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique com o botão direito do mouse no módulo que deseja copiar.

   >[!NOTE]
   >
   >Você pode selecionar mais de um módulo, mantendo pressionado o [!UICONTROL shift] e clicando nos módulos que deseja copiar. Copiar um grupo de módulos também copia quaisquer linhas de conexão, filtros ou lógica de roteamento entre eles.

1. Selecione **[!UICONTROL Copiar módulo]**.
1. Mova o cursor para a área do cenário em que deseja copiar o cenário.
1. Clique com o botão direito e selecione **[!UICONTROL Colar]**.
1. Conecte os módulos colados ao cenário arrastando-os para o local apropriado no cenário.

   Você também pode usar atalhos de teclado para copiar e colar.

## Copiar um cenário por clonagem

A clonagem de um cenário cria uma cópia do cenário, que pode ser editada.

1. Abra a página de detalhes do cenário:

   1. Clique na guia **[!UICONTROL Cenário]** no painel esquerdo e, em seguida, clique no cenário sobre o qual deseja obter detalhes.

      Ou

      Se você estiver trabalhando no cenário no editor de cenários, clique na seta para a esquerda ![Seta para edição de saída](assets/exit-editing-arrow.png) próxima ao canto superior esquerdo da janela.

1. Clique com o botão direito do mouse em **[!UICONTROL Opções]** no canto superior direito da página.
1. Selecione **[!UICONTROL Clone]**.
1. (Opcional) Insira um nome para o novo cenário.
1. (Opcional) Habilite **[!UICONTROL Manter os estados de qualquer módulo novo iguais aos que estão sendo duplicados]** para garantir que o cenário copiado também inclua informações sobre os registros mais recentes processados pelo cenário original.
1. Clique em **[!UICONTROL Salvar]** para criar o cenário.

## Copiar um cenário usando blueprints

Os blueprints de cenário representam a organização, o mapeamento e os valores de campo de um determinado cenário em um determinado momento. Você pode exportar um blueprint de cenário para um arquivo JSON em seu computador e, em seguida, importá-lo ao criar um novo cenário. Os cenários importados de um blueprint de cenário podem ser editados.

Um blueprint de cenário representa todo o cenário. Para copiar apenas determinados módulos de um cenário, consulte [Copiar um módulo ou um grupo de módulos](#copy-a-module-or-a-group-of-modules) neste artigo.

### Exportar um blueprint de cenário

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja exportar um blueprint.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. No cenário, clique no menu **[!UICONTROL Mais]** na área de configurações de cenário.
1. Clique em **[!UICONTROL Exportar blueprint]**.

   Um arquivo JSON é criado e baixado no computador. Você pode localizar este arquivo na pasta [!DNL Downloads].

>[!NOTE]
>
>Para exportar o blueprint de uma versão anterior de um cenário, consulte [Exibir e gerenciar versões de cenário](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md).

### Importar um blueprint

>[!IMPORTANT]
>
>Se você importar um blueprint para um cenário existente, o blueprint do cenário substituirá o existente. Não é possível anexar um blueprint a um cenário existente.

1. Comece a criar um novo cenário.
1. No cenário, clique no menu **[!UICONTROL Mais]** na área de configurações de cenário.
1. Clique em **[!UICONTROL Importar blueprint]**.
1. Na caixa de diálogo exibida, clique em **[!UICONTROL Procurar]**
1. Navegue até o blueprint que você deseja importar e clique em **[!UICONTROL Abrir]**.
1. Clique em **[!UICONTROL Salvar]**.

   Um arquivo JSON é criado e baixado no computador. Você pode localizar este arquivo na pasta [!UICONTROL Downloads].

## Copiar e reutilizar cenários usando modelos

É possível criar modelos como ponto de partida para seus cenários do Workfront Fusion. Ao criar um cenário a partir de um modelo, você pode modificar o cenário sem modificar o modelo. Os valores de campo não são salvos em modelos.

Para obter mais informações sobre como criar um cenário usando um modelo, consulte [Criar cenários com modelos](/help/workfront-fusion/create-scenarios/add-modules/create-scenarios-with-fusion-templates.md).

## Solução de problemas

Se você estiver copiando e colando módulos conforme descrito em [Copiar um módulo ou um grupo de módulos](#copy-a-module-or-a-group-of-modules) e nada aparecer ao colar, verifique as configurações do site do navegador para garantir que a colagem da área de transferência seja permitida.
