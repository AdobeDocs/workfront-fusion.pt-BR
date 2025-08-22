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
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 2%

---

# Adicionar usuários ao Adobe Workfront Fusion por meio da Adobe Admin Console

Você pode adicionar um usuário ao [!DNL Adobe Admin Console] e atribuí-lo ao Adobe Workfront Fusion, ou atribuir um usuário existente no [!DNL Adobe Admin Console] ao Workfront Fusion.

Para assistir a um vídeo que descreve o Workfront Fusion no [!DNL Adobe Admin Console], incluindo como adicionar usuários, consulte [[!DNL Fusion] no Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.



Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">plano do Adobe Workfront*</td> 
   <td> <p>[!UICONTROL Pro] ou superior</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença da Adobe Workfront*</td> 
   <td> <p>[!UICONTROL Plano], [!UICONTROL Trabalho]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Requisito de licença herdado: [!UICONTROL Workfront Fusion para Automação e Integração do Trabalho] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o plano do [!UICONTROL Select] ou do [!UICONTROL Prime] para Adobe Workfront, sua organização deve comprar o Adobe Workfront Fusion e o Adobe Workfront para usar a funcionalidade descrita neste artigo. O Workfront Fusion está incluído no plano do Workfront da [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o Adobe Workfront Fusion e o Adobe Workfront para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] direitos de administrador</td> 
   <td>Você deve ser um [!UICONTROL Administrador de Configuração de Produto] de [!DNL Adobe] produtos para sua organização.</td> 
  </tr>
  </tbody> 
</table>

&#42;Para saber qual plano, tipo de licença ou acesso você tem, contate o administrador do Workfront.

&#42;&#42;Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença do Adobe Workfront</td> 
   <td> <p>Novo: Padrão</p><p>Ou</p><p>Atual: [!UICONTROL Trabalho] ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo menu:</p> <ul><li>Plano do Workfront para [!UICONTROL Select] ou [!UICONTROL Prime]: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Workfront do [!UICONTROL Ultimate]: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso*</td> 
   <td> 
     <p>Você deve ser um administrador do Workfront Fusion para sua organização.</p>
     <p>Você deve ser um administrador do Workfront Fusion para sua equipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
