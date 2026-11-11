---
title: Exibir e gerenciar funções de equipe
description: Cada equipe tem uma guia Funções, na qual você pode visualizar as funções da equipe, criar suas próprias funções, escolher as permissões que cada função inclui e atualizar ou excluir funções.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: a3a6922afd713cd002cdf472c7ef62c1855b80d9
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 10%
---
# Exibir e gerenciar funções de equipe

Você pode visualizar as funções disponíveis em uma equipe, criar suas próprias funções e escolher quais permissões cada função inclui. Também é possível atualizar e excluir funções.

As funções personalizadas oferecem os seguintes benefícios:

* Cada membro da equipe tem somente o acesso de que seu trabalho precisa, o que reduz o risco de alterações acidentais em cenários críticos.
* As funções personalizadas podem corresponder melhor ao funcionamento de sua organização, em vez de ajustar suas equipes às funções predefinidas.
* Você mesmo pode gerenciar o acesso sem entrar em contato com o suporte.

Para obter uma visão geral das organizações, equipes e funções predefinidas de equipe, consulte [Visão geral da organização e da equipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/org-and-team-overview.md). Para obter as permissões incluídas nas funções predefinidas, consulte [Funções de organização e equipe](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso</td> 
   <td> 
     <p>Você deve ter a permissão <b>[!UICONTROL Gerenciar membros]</b> na equipe. Nas funções predefinidas, essa permissão está incluída nas funções de Administrador de equipe e Proprietário da organização.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Quem pode gerenciar funções de equipe

Qualquer pessoa com a permissão **[!UICONTROL Gerenciar membros]** em uma equipe pode criar, atualizar, excluir e atribuir usuários a funções nessa equipe.

* Os Proprietários da organização podem criar e gerenciar funções em todas as equipes.
* Os Administradores da Organização podem gerenciar funções somente nas equipes das quais são membros e onde têm a permissão **[!UICONTROL Gerenciar membros]**.
* Os administradores de equipe podem gerenciar funções em suas equipes.

## Criar ou editar uma função

1. No Fusion, na navegação à esquerda, clique em **Visão geral da equipe**.
1. (Condicional) Se você não estiver na página da equipe para a qual deseja exibir funções, clique na lista suspensa **Equipe** próxima à parte superior da página e selecione a equipe correta.
1. Abra a guia **[!UICONTROL Funções]**.

   A guia lista as funções que estão disponíveis na equipe, incluindo as funções predefinidas. Para cada função, a lista mostra o nome da função e um resumo de suas permissões, como &quot;Sem permissões&quot;, &quot;Membro&quot; ou &quot;Personalizado · 19 permissões&quot;.

1. Para criar uma função, clique em **[!UICONTROL Criar função]**.

   Ou

   Para editar uma função, clique em **[!UICONTROL Editar]** na linha da função que deseja editar.

   <!-- BECKY CHECK ME: The Edit button is available for the predefined roles as well as custom roles. Confirm the title of the edit page, whether you can rename the predefined roles, and what happens to users who already have the role. -->

1. Insira um nome para a função no campo **[!UICONTROL Nome da função]**.
1. Na lista suspensa **[!UICONTROL Modelo de função]**, selecione o modelo a partir do qual deseja começar.

   O modelo define as permissões iniciais para a função. O modelo padrão é **[!UICONTROL Visualizador]**.

1. Na área **[!UICONTROL Permissões com escopo]**, selecione as permissões que você deseja que a função inclua.

   As permissões são agrupadas por área, como **[!UICONTROL Automações]**, **[!UICONTROL Conexões]** e **[!UICONTROL Equipe]**. Para cada área, você pode executar um dos seguintes procedimentos:

   * Para definir todas as permissões em uma área ao mesmo tempo, clique em **[!UICONTROL Sem acesso]**, **[!UICONTROL Somente exibição]** ou **[!UICONTROL Acesso completo]** ao lado do nome da área.
   * Para escolher permissões específicas, marque ou desmarque a caixa de seleção de cada permissão.

   Para obter uma lista das permissões, consulte [Permissões que você pode incluir em uma função](#permissions-that-you-can-include-in-a-role) neste artigo.

   <!-- BECKY CHECK ME: Confirm the options in the Role template dropdown and what each one selects. Confirm exactly what No access, View only, and Full access select in each area (in the screenshot, View only selects the view permissions). Confirm whether there is a Description field, and whether there are areas below Team on the page (the screenshots end at Team). -->

1. Clique em **[!UICONTROL Salvar]**. Para fechar a página sem salvar, clique em **[!UICONTROL Cancelar]**.
1. (Opcional) Para excluir uma função, clique em **[!UICONTROL Excluir]** na linha da função na guia **[!UICONTROL Funções]**.

   <!-- BECKY CHECK ME: Confirm why the Delete button is unavailable (dimmed) for some roles, such as Team Operator, Team Member, and Team Admin in the screenshot, whether there is a confirmation prompt, and what happens to users who have the role. Update this step and add a note, if needed. -->

Uma função que você cria está disponível na equipe. Você pode atribuí-lo a membros da equipe.

### Permissões que você pode incluir em uma função

<table style="table-layout:auto">
 <col>
 <col>
 <thead>
  <tr>
   <th>Área</th>
   <th>Permissões</th>
  </tr>
 </thead>
 <tbody>
 <tr>
   <td role="rowheader">[!UICONTROL Automações]</td>
   <td>Exibir lista, Exibir detalhes, Exibir histórico de execução, Gerenciar notificações, Redefinir estatísticas, Executar uma vez, Editar programação, Ativar, Desativar, Criar, Editar, Publicar, Excluir</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Execuções incompletas]</td>
   <td>Exibir, Gerenciar</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Webhooks]</td>
   <td>Exibir, Exibir fila, Criar, Editar, Gerenciar fila, Alterar prioridade, Excluir</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Connections]</td>
   <td>Exibir, Criar, Editar, Excluir</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Chaves]</td>
   <td>Exibir, Criar, Editar, Excluir</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Armazenamento de dados]</td>
   <td>Exibir lista, Procurar registros, Criar, Editar, Excluir</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Estruturas de dados]</td>
   <td>Exibir, Criar, Editar, Excluir</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Modelos]</td>
   <td>Exibir lista, Exibir detalhes, Criar, Editar, Excluir</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Team]</td>
   <td>Exibir equipe, Editar configurações da equipe, Gerenciar membros, Excluir equipe</td>
  </tr>
 </tbody>
</table>

<!-- BECKY CHECK ME: Confirm that this list is complete, and add a description of what each permission allows, if needed. The list is taken from the Create role page, which may have more areas below Team. -->

## Clonar funções para outra equipe

Você pode copiar as funções de uma equipe para outra equipe, de modo que não seja necessário recriar as mesmas funções em cada equipe.

1. Abra a guia **[!UICONTROL Funções]** da equipe, conforme descrito em [Criar ou editar uma função](#create-or-edit-a-role) neste artigo.
1. Clique em **[!UICONTROL Clonar para a equipe]**.

   A página **[!UICONTROL Clonar funções para outra equipe]** é aberta.

1. Na lista suspensa **[!UICONTROL Equipe de destino]**, selecione a equipe para a qual deseja clonar as funções.

   Aparece uma tabela com as funções da equipe atual.

1. Para cada função na tabela, revise e defina o seguinte:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL função Source]</td> 
      <td> <p>A função na equipe atual, com um resumo de suas permissões.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Action]</td> 
      <td> <p>O que fazer com a função. Por exemplo, <b>[!UICONTROL Copiar na função existente]</b> copia as permissões da função de origem para uma função que já existe na equipe de destino.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Destino]</td> 
      <td> <p>A função na equipe de destino para a qual a função de origem é copiada.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Alterações]</td> 
      <td> <p>Se a função de destino é diferente da função de origem. Por exemplo, <b>[!UICONTROL Já sincronizado]</b> significa que a função de destino já tem as mesmas permissões que a função de origem.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Users]</td> 
      <td> <p>Informações sobre usuários que possuem a função. Por exemplo, <b>[!UICONTROL Sem usuários correspondentes]</b> significa que não há usuários a serem incluídos.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Status]</td> 
      <td> <p>O resultado para a função após a clonagem.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Clonar]**. Para fechar a página sem clonagem, clique em **[!UICONTROL Cancelar]**.

<!-- BECKY CHECK ME: The screenshot shows the Clone roles to another team page after a target team is selected. Confirm the options in the Action dropdown (for example, whether you can create a new role in the target team), the options in the Target dropdown, what the checkbox in the Users column does (for example, whether it also assigns the role to matching users in the target team) and what "matching users" means, what the Changes column shows when the roles differ, and what the Status column shows before and after you clone. -->

<!-- BECKY CHECK ME: Confirm whether the Target team dropdown lists all teams or only the teams that you can manage, and whether the Clone to team button is visible to everyone who can manage roles. -->

## Atribuir uma função a um usuário

Você atribui uma função personalizada da mesma forma que atribui uma função predefinida. Para obter instruções, consulte [Adicionar um usuário a uma equipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md) e [Exibir ou editar funções de usuário](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md#view-or-edit-user-roles-for-a-team).

<!-- BECKY CHECK ME: Confirm that custom roles appear in the role dropdowns in both of these procedures. -->

## Considerações

* Permissões da organização em cascata. Para conceder acesso a alguém para executar uma ação em todas as equipes, atribua uma função de organização em vez de criar uma função de equipe. Para obter mais informações, consulte [Organização e funções de equipe](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).
* As funções que você cria pertencem a uma equipe.

<!-- BECKY CHECK ME: The Slack thread says that defining a role that is available in all teams was out of scope for the initial release. Confirm that a role belongs to a single team, and that you clone it to use it in another team. -->
