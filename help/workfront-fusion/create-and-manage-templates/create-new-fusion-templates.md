---
title: Criar novos modelos
description: Você pode criar novos modelos de cenário no  [!DNL Adobe] Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
source-git-commit: 7acc27ab2ce80b964b7f9fbb302816aa75964ab5
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%

---

# Criar novos modelos

Você pode criar novos modelos de cenário no [!DNL Adobe] Workfront Fusion.

>[!TIP]
>
>Antes de criar um novo modelo, verifique a guia [!UICONTROL Public templates] para garantir que o modelo que você deseja criar ainda não está disponível.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacote</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença</td> 
   <td> <p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou plano do [!UICONTROL Prime] [!DNL Workfront]: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plano: [!DNL Workfront Fusion] está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Criar um novo modelo

Você pode criar um modelo em um processo semelhante à criação de um cenário. Os administradores do Fusion também podem criar modelos a partir de cenários existentes.

* [Criar um modelo](#build-a-template)
* [Criar um modelo a partir de um cenário](#create-a-template-from-a-scenario)

### Criar um modelo

1. Clique em **[!UICONTROL Templates]** ![](assets/templates-icon.png) no painel de navegação esquerdo.
1. Clique em **[!UICONTROL Create a new template]** no canto superior direito.
1. (Opcional) Renomeie o modelo substituindo o padrão **[!UICONTROL New template name]** no canto superior esquerdo.
1. (Opcional) Para alterar o idioma do modelo, clique em **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) e selecione o idioma no menu suspenso Idioma.

   >[!IMPORTANT]
   >
   >A seleção Languages corresponde aos idiomas disponíveis nas configurações do sistema e aborda apenas o nome do template público e sua descrição. Não é possível alterar um idioma de modelo depois que o modelo é salvo.

1. (Opcional) Para inserir uma descrição do modelo, clique em **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) e insira a descrição.
1. Adicionar aplicativos, módulos e ferramentas, usando os mesmos processos que adicionar módulos a um cenário.

   Para obter instruções, consulte os artigos em [Adicionar módulos](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Para adicionar ajuda contextual aos módulos, consulte [Configurar funcionalidade do Assistente](#set-up-wizard-functionality) neste artigo.

   Para obter mais informações sobre como criar um cenário, consulte [Fluxo de trabalho para criar um cenário](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md).

   >[!NOTE]
   >
   >Se o modelo incluir módulos que exigem a adição da conexão, das credenciais ou de outras informações confidenciais de privacidade, essas informações não serão compartilhadas com os usuários do modelo.

1. (Opcional) Clique em **[!UICONTROL Run once]** para testar seu modelo.
1. Clique no ícone **[!UICONTROL Save]** ![](assets/save-icon.png) para salvar o modelo.

Ao salvar o modelo, ele fica visível para os membros da equipe. Se quiser que o modelo seja acessível fora da equipe, envie uma solicitação para que ele seja aprovado e publicado. A solicitação é enviada à equipe do Adobe Workfront Fusion para aprovação. Depois de aprovado, o modelo pode ser acessado por outras pessoas fora da equipe.

Para obter informações sobre a publicação de modelos, consulte [Publish e compartilhar [!DNL Adobe Workfront Fusion] modelos](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

### Criar um modelo a partir de um cenário

>[!NOTE]
>
>Você deve ser um administrador do Fusion para criar um modelo a partir de um cenário.

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário a partir do qual deseja criar um modelo.
1. Clique no menu suspenso **Admin** próximo ao canto superior direito da página.
1. Selecione **Clonar como modelo**.

   O cenário é copiado em uma página Novo modelo.
1. (Opcional) Renomeie o modelo substituindo o padrão **[!UICONTROL New template name]** no canto superior esquerdo.
1. (Opcional) Para alterar o idioma do modelo, clique em **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) e selecione o idioma no menu suspenso Idioma.

   >[!IMPORTANT]
   >
   >A seleção Languages corresponde aos idiomas disponíveis nas configurações do sistema e aborda apenas o nome do template público e sua descrição. Não é possível alterar um idioma de modelo depois que o modelo é salvo.

1. (Opcional) Para inserir uma descrição do modelo, clique em **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) e insira a descrição.
1. Edite aplicativos, módulos e ferramentas conforme desejado, usando os mesmos processos que adiciona módulos a um cenário.

   Para obter instruções, consulte os artigos em [Adicionar módulos](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Para adicionar ajuda contextual aos módulos, consulte [Configurar a funcionalidade [!UICONTROL Wizard]](#set-up-wizard-functionality) neste artigo.

   >[!NOTE]
   >
   >Se o modelo incluir módulos que exigem a adição da conexão, das credenciais ou de outras informações confidenciais de privacidade, essas informações não serão compartilhadas com os usuários do modelo.

1. (Opcional) Clique em **[!UICONTROL Run once]** para testar seu modelo.
1. Clique no ícone **[!UICONTROL Save]** ![](assets/save-icon.png).

## Configurar a funcionalidade [!UICONTROL Wizard] {#set-up-wizard-functionality}

O [!DNL Workfront Fusion template] [!UICONTROL Wizard] permite que você forneça aos futuros usuários do seu modelo instruções ou informações relacionadas aos campos específicos usados nos módulos.

1. Ao criar um modelo, clique em um módulo adicionado ao modelo para ver os campos do módulo.
1. Localize o campo onde deseja adicionar informações de [!UICONTROL Wizard] e habilite **[!UICONTROL Use in Wizard]** para esse campo.
1. Insira as informações que você deseja tornar visíveis para usuários no campo [!UICONTROL Help].
1. (Opcional) Para permitir que os usuários vejam este texto ao usar o modelo, habilite **[!UICONTROL Use as default value]**.
1. Repita as etapas 2 a 4 para cada campo para o qual deseja fornecer informações.
1. Clique em **[!UICONTROL OK]** para salvar as alterações e fechar o módulo.
