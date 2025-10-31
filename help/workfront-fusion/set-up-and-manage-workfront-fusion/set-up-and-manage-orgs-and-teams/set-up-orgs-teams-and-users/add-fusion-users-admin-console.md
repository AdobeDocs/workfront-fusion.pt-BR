---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Adicionar usuários ao Adobe Workfront Fusion por meio da Adobe Admin Console
description: Você pode adicionar um usuário ao Adobe Admin Console e atribuí-lo ao Adobe Workfront Fusion ou atribuir um usuário existente no Adobe Admin Console ao Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 1%

---

# Adicionar usuários ao Adobe Workfront Fusion por meio da Adobe Admin Console

Você pode adicionar um usuário ao [!DNL Adobe Admin Console] e atribuí-lo ao Adobe Workfront Fusion, ou atribuir um usuário existente no [!DNL Adobe Admin Console] ao Workfront Fusion.

Para assistir a um vídeo que descreve o Workfront Fusion no [!DNL Adobe Admin Console], incluindo como adicionar usuários, consulte [[!DNL Fusion] no Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso</td> 
   <td> 
     <p>Você deve ser um administrador do Workfront Fusion para sua organização.</p>
     <p>Você deve ser um administrador do Workfront Fusion para sua equipe.</p>
   </td> 
  </tr> 
  </tr>
   <tr> 
   <td role="rowheader">Configurações de nível de acesso</td> 
   <td>Você deve ser um Administrador de configuração de produtos da Adobe para sua organização.</td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Pré-requisitos

Antes de usar o [!DNL Admin Console] for Workfront, você deve receber um email convidando você para o console.

1. Se você é novo no [!DNL Adobe] e recebeu um email informando que agora tem direitos de administrador para gerenciar software e serviços do [!DNL Adobe] para sua organização, clique no botão no email para criar uma conta do [!DNL Adobe] e abrir o [!DNL Admin Console].

   Ou

   Se você já tiver uma conta do Adobe, vá para a [[!DNL Adobe Admin Console] página](https://adminconsole.adobe.com).


## Adicionar um novo usuário ao [!DNL Adobe Admin Console] e ao Workfront Fusion

1. Na [[!DNL Adobe Admin Console] página](https://adminconsole.adobe.com/), selecione a guia **[!UICONTROL Produtos]** na barra de navegação superior e, em seguida, selecione o bloco de produtos **Workfront Fusion**.

   ![Fusão no Admin Console](assets/fusion-product-admin-console.png)

1. Na lista exibida, selecione a organização à qual deseja adicionar um usuário.

   ![Instância do Fusion no Admin Console](assets/fusion-instances-admin-console.png)

1. Na lista exibida, com a guia **[!UICONTROL Perfis de Produto]** selecionada, clique no nome do link do [!UICONTROL Perfil de Produto] do Workfront Fusion.

   >[!IMPORTANT]
   >
   > Não faça alterações no próprio [!UICONTROL Perfil do Produto].

1. Com a guia **[!UICONTROL Usuários]** selecionada acima da lista, clique em **[!UICONTROL Adicionar usuário]**.

1. Na caixa **[!UICONTROL Adicionar usuários a este perfil de produto]**, digite o endereço de email ou o nome de um usuário que deseja adicionar e selecione o usuário na lista exibida.

1. Clique em **[!UICONTROL Salvar]**.

   O usuário é criado no Workfront Fusion.

1. (Opcional) Continue para [Alterar o nível de acesso de um usuário no Workfront Fusion](#change-a-users-access-level-in-workfront-fusion)

## Alterar o nível de acesso de um usuário no Workfront Fusion

* [Alterar a função de um usuário para Administrador](#change-a-users-role-to-admin)
* [Alterar a função de um usuário para Membro, Contador ou Desenvolvedor de aplicativos](#change-a-users-role-to-member-accountant-or-app-developer)

### Alterar a função de um usuário para Administrador

A atribuição de uma função de Administrador a um usuário deve ser feita no [!DNL Adobe Admin Console].

1. Na página [!UICONTROL Perfil de Produto] do Workfront Fusion em que você adicionou o usuário, selecione a guia **[!UICONTROL Administradores]**.

1. Clique em **[!UICONTROL Adicionar administrador]**.

1. Na caixa **[!UICONTROL Adicionar administradores de perfil de produto]**, digite o endereço de email ou o nome do usuário que deseja tornar-se um administrador e selecione-o na lista exibida.

1. Clique em **[!UICONTROL Salvar]**.

   O usuário agora é um Administrador no Workfront Fusion.

### Alterar a função de um usuário para Membro, Contador ou Desenvolvedor de aplicativos

As funções de Membro, Contador e Desenvolvedor de aplicativos são tratadas no Workfront Fusion.

Para obter instruções, consulte [Exibir ou editar funções de usuário](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md).

## Atribuir um usuário existente no [!DNL Adobe Admin Console] ao Workfront Fusion

É possível adicionar um usuário existente a uma equipe no Fusion. Isso é tratado no Fusion.

Para obter instruções, consulte [Adicionar um usuário a uma equipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md).
