---
content-type: reference
title: Editar modelos
description: Este artigo descreve como editar modelos do Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: 86b0d7b16a4ed7e15888f6ee1a58f0279e96fb70
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Editar modelos

Os modelos do Adobe Workfront Fusion são cenários pré-criados projetados para automatizar e simplificar vários workflows. Esses modelos podem ajudar você a configurar rapidamente integrações e automações sem precisar criar tudo do zero.

Se você for um administrador, terá permissão para exibir, modificar, renomear, publicar, aprovar e excluir modelos criados por outros.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plano</td>
      <td><p>Qualquer</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">[!DNL Adobe Workfront] licença</td>
      <td><p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td>
      <td>
        <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
        <p>Ou</p>
        <p>Herdados: Qualquer um</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produto</td>
      <td>
        <p>Novo:</p>
        <ul>
          <li>[!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Workfront] Plano: Sua organização deve comprar [!DNL Adobe Workfront Fusion].</li>
          <li>[!UICONTROL Ultimate] [!DNL Workfront] Plano: [!DNL Workfront Fusion] está incluído.</li>
        </ul>
        <p>Ou</p>
        <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## Editar modelos de [!DNL Workfront Fusion] como administrador

1. Clique em **[!UICONTROL Administration]** no painel de navegação esquerdo para abrir a área [!UICONTROL Administration].
1. Clique em **[!UICONTROL All Templates]** no painel de navegação esquerdo.
1. Clique em **[!UICONTROL Detail]** à direita do modelo que deseja editar.
1. (Opcional) Renomeie o modelo clicando em **Opções** no canto superior direito e selecionando **Renomear**.
1. (Opcional) Para alterar o idioma do modelo, clique em **[!UICONTROL Create a new template]** ![](assets/fusion-scenario-settings-icon.png) e selecione o idioma no menu suspenso Idioma.

   >[!IMPORTANT]
   >
   >A seleção Languages corresponde aos idiomas disponíveis nas configurações do sistema e aborda apenas o nome do template público e sua descrição. Não é possível alterar um idioma de modelo depois que o modelo é salvo.

1. (Opcional) Para editar a descrição do modelo, clique em **[!UICONTROL Set up a template]** ![](assets/fusion-scenario-settings-icon.png) e insira a descrição.
1. Adicione ou edite aplicativos, módulos e ferramentas da mesma forma que faria ao criar um cenário padrão.

   Para adicionar ajuda contextual aos módulos, consulte [Configurar a funcionalidade [!UICONTROL Wizard]](#set-up-wizard-functionality) neste artigo.

   <!--For more information on building a scenario, see [Create a scenario in [!DNL Adobe Workfront Fusion]](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >Se o modelo incluir módulos que exigem a adição da conexão, das credenciais ou de outras informações confidenciais de privacidade, essas informações não serão compartilhadas com os usuários do modelo.

1. (Opcional) Clique em **[!UICONTROL Run once]** para testar o modelo.
1. Clique no ícone **[!UICONTROL Save]** ![](assets/save-icon.png).


## Configurar a funcionalidade [!UICONTROL Wizard]

O [!DNL Workfront Fusion template] [!UICONTROL Wizard] permite que você forneça aos futuros usuários do seu modelo instruções ou informações relacionadas aos campos específicos usados nos módulos.

1. Clique no módulo adicionado ao modelo para ver os campos do módulo.
1. Localize o campo onde deseja adicionar informações de [!UICONTROL Wizard] e habilite **[!UICONTROL Use in Wizard]** abaixo dele.
1. Insira as informações que você deseja tornar visíveis para usuários no campo [!UICONTROL Help].
1. (Opcional) Para permitir que os usuários vejam este texto ao usar o modelo, habilite **[!UICONTROL Use as default value]**.
1. Repita as etapas 2 a 4 para cada campo para o qual deseja fornecer informações.
1. Clique em **[!UICONTROL OK]** para salvar as alterações e fechar o módulo.

O processo de publicação é o mesmo que no caso de um usuário padrão. Para obter informações, consulte a seção [Publish e modelos de compartilhamento](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md) para obter mais detalhes.

## Status dos modelos

Você pode verificar o status na página de modelo sob o nome do modelo.

Os seguintes status estão disponíveis:

* **[!UICONTROL Private]**: este modelo é visível apenas para o autor do modelo e sua equipe.
* **[!UICONTROL Published]**: este modelo é visível apenas para o autor do modelo e sua equipe. Depois de publicado, é possível enviar o modelo para aprovação, se desejado. Também é possível copiar um link compartilhável.
* **[!UICONTROL Approved]**: Esse modelo está visível para todos os usuários do Workfront Fusion na guia [!UICONTROL Public templates]. Você também pode copiar um link compartilhável clicando em [!UICONTROL Options] no canto superior direito da tela.

Você também pode verificar o status na guia [!UICONTROL Team templates]. Se um modelo for publicado, ele terá um ícone à direita do nome do modelo.

* **Ícone de olho**: o modelo está publicado; ele está visível para a equipe.
* **Ícone de marca de seleção amarelo**: o modelo é publicado, está visível somente para a equipe e aguarda aprovação para ser adicionado à guia Modelos públicos.
* **Ícone de marca de seleção verde**: o modelo está disponível na guia Modelos públicos e está visível para qualquer usuário do Workfront Fusion. Ela também ainda está visível na guia [!UICONTROL Team templates]. O autor do modelo ou o membro da equipe ainda pode editá-lo.

Modelos sem ícones têm status [!UICONTROL Private]. Eles não são publicados e são visíveis apenas para a equipe do.

## Localizar informações de SVG de um modelo

1. Clique em **[!UICONTROL Administration]** no painel de navegação esquerdo para abrir a área [!UICONTROL Administration].
1. Clique em **[!UICONTROL Templates]** no painel de navegação esquerdo.
1. Clique no modelo para o qual deseja localizar informações.
1. Clique em **Opções** no canto superior direito.
1. Selecione *Diagrama SVG*.

Aqui você pode ver o diagrama de SVG e o código de SVG.
