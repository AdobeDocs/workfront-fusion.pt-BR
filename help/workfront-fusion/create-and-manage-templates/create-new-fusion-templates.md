---
title: Criar novos modelos
description: Você pode criar novos modelos de cenário no  [!DNL Adobe] Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
source-git-commit: 3a977d805c10fda7209b0634c6e32e818a980691
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

---

# Criar novos modelos

Você pode criar novos modelos de cenário no [!DNL Adobe] Workfront Fusion.

>[!TIP]
>
>Antes de criar um novo modelo, você pode verificar a guia [!UICONTROL Modelos públicos] para garantir que o modelo que você deseja criar ainda não está disponível.

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

## Criar um novo modelo

Você pode criar um modelo em um processo semelhante à criação de um cenário. Os administradores do Fusion também podem criar modelos a partir de cenários existentes.

* [Criar um modelo](#build-a-template)
* [Criar um modelo a partir de um cenário](#create-a-template-from-a-scenario)

### Criar um modelo

1. Clique em **[!UICONTROL Modelos]** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Clique em **[!UICONTROL Criar um novo modelo]** no canto superior direito.
1. (Opcional) Renomeie o modelo substituindo o padrão **[!UICONTROL Novo nome do modelo]** no canto superior esquerdo.
1. (Opcional) Para alterar o idioma do modelo, clique em **[!UICONTROL Configurar um modelo]** ![Ícone de configurações do cenário](assets/scenario-settings-icon.png) e selecione o idioma no menu suspenso Idioma.

   >[!IMPORTANT]
   >
   >A seleção Languages corresponde aos idiomas disponíveis nas configurações do sistema e aborda apenas o nome do template público e sua descrição. Não é possível alterar um idioma de modelo depois que o modelo é salvo.

1. (Opcional) Para inserir uma descrição do modelo, clique em **[!UICONTROL Configurar um modelo]** ![Ícone de configurações de cenário](assets/scenario-settings-icon.png) e insira a descrição.
1. Adicionar aplicativos, módulos e ferramentas, usando os mesmos processos que adicionar módulos a um cenário.

   Para obter instruções, consulte os artigos em [Adicionar módulos](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Para adicionar ajuda contextual aos módulos, consulte [Configurar funcionalidade do Assistente](#set-up-wizard-functionality) neste artigo.

   Para obter mais informações sobre como criar um cenário, consulte [Fluxo de trabalho para criar um cenário](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md).

   >[!NOTE]
   >
   >Se o modelo incluir módulos que exigem a adição da conexão, das credenciais ou de outras informações confidenciais de privacidade, essas informações não serão compartilhadas com os usuários do modelo.

1. (Opcional) Clique em **[!UICONTROL Executar uma vez]** para testar seu modelo.
1. Clique no ícone **[!UICONTROL Salvar]** ![Ícone Salvar](assets/save-icon.png) para salvar o modelo.

Ao salvar o modelo, ele fica visível para os membros da equipe. Se quiser que o modelo seja acessível fora da equipe, envie uma solicitação para que ele seja aprovado e publicado. A solicitação é enviada à equipe do Adobe Workfront Fusion para aprovação. Depois de aprovado, o modelo pode ser acessado por outras pessoas fora da equipe.

Para obter informações sobre a publicação de modelos, consulte [Publicar e compartilhar modelos do Adobe Workfront Fusion](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

### Criar um modelo a partir de um cenário

>[!NOTE]
>
>Você deve ser um administrador do Fusion para criar um modelo a partir de um cenário.

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário a partir do qual deseja criar um modelo.
1. Clique no menu suspenso **Admin** próximo ao canto superior direito da página.
1. Selecione **Clonar como modelo**.

   O cenário é copiado em uma página Novo modelo.
1. (Opcional) Renomeie o modelo substituindo o padrão **[!UICONTROL Novo nome do modelo]** no canto superior esquerdo.
1. (Opcional) Para alterar o idioma do modelo, clique em **[!UICONTROL Configurar um modelo]** ![Ícone de configurações do cenário](assets/scenario-settings-icon.png) e selecione o idioma no menu suspenso Idioma.

   >[!IMPORTANT]
   >
   >A seleção Languages corresponde aos idiomas disponíveis nas configurações do sistema e aborda apenas o nome do template público e sua descrição. Não é possível alterar um idioma de modelo depois que o modelo é salvo.

1. (Opcional) Para inserir uma descrição do modelo, clique em **[!UICONTROL Configurar um modelo]** ![Ícone de configurações de cenário](assets/scenario-settings-icon.png) e insira a descrição.
1. Edite aplicativos, módulos e ferramentas conforme desejado, usando os mesmos processos que adiciona módulos a um cenário.

   Para obter instruções, consulte os artigos em [Adicionar módulos](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Para adicionar ajuda contextual aos módulos, consulte [Configurar a funcionalidade [!UICONTROL Assistente]](#set-up-wizard-functionality) neste artigo.

   >[!NOTE]
   >
   >Se o modelo incluir módulos que exigem a adição da conexão, das credenciais ou de outras informações confidenciais de privacidade, essas informações não serão compartilhadas com os usuários do modelo.

1. (Opcional) Clique em **[!UICONTROL Executar uma vez]** para testar seu modelo.
1. Clique no ícone **[!UICONTROL Salvar]** ![Ícone Salvar](assets/save-icon.png).

## Configurar a funcionalidade [!UICONTROL Assistente] {#set-up-wizard-functionality}

O [!DNL Workfront Fusion template] [!UICONTROL Assistente] permite que você forneça aos futuros usuários do seu modelo instruções ou informações relacionadas aos campos específicos usados nos módulos.

1. Ao criar um modelo, clique em um módulo adicionado ao modelo para ver os campos do módulo.
1. Localize o campo no qual você deseja adicionar informações do [!UICONTROL Assistente] e habilitar o **[!UICONTROL Uso do Assistente]** para esse campo.
1. Digite as informações que você deseja tornar visíveis para usuários no campo [!UICONTROL Ajuda].
1. (Opcional) Para permitir que os usuários vejam este texto ao usar o modelo, habilite **[!UICONTROL Usar como valor padrão]**.
1. Repita as etapas 2 a 4 para cada campo para o qual deseja fornecer informações.
1. Clique em **[!UICONTROL OK]** para salvar as alterações e fechar o módulo.
