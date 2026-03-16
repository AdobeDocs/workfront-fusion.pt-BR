---
title: Gerenciar usuários do Adobe Workfront Fusion na sua organização
description: Gerenciar usuários do Adobe Workfront Fusion na sua organização
author: Becky
feature: Workfront Fusion
exl-id: 32c221fa-856b-4921-9fa6-5e60f2aa08cd
source-git-commit: 3f9390d8947ef2666336c1a4cc6eab8d174849d5
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 18%

---

# Exibir ou editar funções de usuário

Os administradores do Adobe Workfront Fusion podem gerenciar funções de usuário no Workfront Fusion.


>[!NOTE]
>
>Se sua organização estiver migrando para a Adobe Admin Console, não será possível gerenciar usuários na Workfront (adicionar ou excluir usuários). Você poderá executar essas ações no Adobe Admin Console após a conclusão da migração.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso</td> 
   <td> 
     <p>Você deve ser um administrador do Workfront Fusion para sua organização.</p>
     <p>Você deve ser um administrador do Workfront Fusion para sua equipe.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações desta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Exibir ou editar funções de usuário para uma organização

Os administradores do Adobe Workfront Fusion podem exibir e atualizar funções de usuário de uma organização.

1. Enquanto estiver conectado como administrador do Workfront Fusion, selecione **[!UICONTROL Todos os usuários]** na navegação à esquerda.
1. Clique em **[!UICONTROL Detalhes]** na linha do usuário que você deseja exibir.
1. (Opcional) Para atualizar a função do usuário em uma organização, clique na lista suspensa na coluna **[!DNL Role]** na linha da organização em que deseja alterar a função do usuário e selecione a nova função.

### Considerações ao adicionar ou alterar Proprietários da organização

Sua organização pode ter mais de um proprietário.

Ao atribuir um usuário para ou a partir de uma função de Proprietário, considere o seguinte.

* Somente um Proprietário pode atribuir a função Proprietário ou atribuir outra função a um Proprietário atual.
* Somente Administradores podem ser atualizados para Proprietário.
* Se houver apenas um Proprietário, a função de Proprietário não poderá ser alterada ou removida.
* Se houver apenas um Proprietário, esse Proprietário não poderá ser excluído se houver outros usuários na organização.
* Quando uma função de Proprietário é atribuída a um Administrador, ele automaticamente se torna Administrador em todas as equipes da organização.
* Quando um Proprietário é atribuído a outra função, esse usuário se torna automaticamente um Membro da equipe em todas as equipes.
* Quando uma nova equipe é criada, todos os Proprietários são automaticamente atribuídos como Administradores da equipe.

## Exibir ou editar funções de usuário para uma equipe

Os administradores do Adobe Workfront Fusion e os administradores de equipe podem exibir e atualizar funções de usuário.

1. Enquanto estiver conectado como administrador do Workfront Fusion, selecione **[!UICONTROL Todos os usuários]** na navegação à esquerda.
1. Clique em **[!UICONTROL Detalhes]** na linha do usuário que você deseja exibir.
1. Clique no ícone Equipes na coluna **[!DNL Role]** na linha da organização que contém a equipe na qual você deseja exibir ou editar a função do usuário.
1. (Opcional) Para atualizar a função do usuário em uma equipe, clique na lista suspensa na coluna **[!DNL Role]** na linha da equipe em que você deseja alterar a função do usuário e, em seguida, selecione a nova função.
