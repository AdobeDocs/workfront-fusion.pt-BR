---
title: Exibir e gerenciar fusos horários
description: Saiba como exibir e gerenciar configurações de fuso horário no Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9910d9b4-5a7a-4f4a-9e66-8600d3b6c785
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 39c34b17e766678e187837e07c90b67f365a4f1d
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 17%
---
# Exibir e gerenciar fusos horários

O Adobe Workfront Fusion inclui controles para fusos horários na organização e no nível do usuário.

* Fusos horários da organização: os cenários usam fusos horários da organização para determinar quando um evento agendado ocorre.

* Fusos horários do usuário: os fusos horários do usuário determinam o horário que é exibido a um usuário.

>[!BEGINSHADEBOX]

Exemplo:

Uma organização tem sede em Nova York e a hora da organização está definida como UTC-5 (América/Nova York). O cenário A pertence a essa organização e está programado para ser executado às 9h todos os dias. O cenário é executado às 9h no fuso horário de Nova York.

Um usuário nesta organização mora em Los Angeles e seu fuso horário de usuário está definido como UTC-8 (América/Los Angeles). Quando esse usuário visualiza o histórico de execução do cenário A, ele vê que o cenário foi executado às 6h. Embora o cenário seja executado de acordo com a hora em Nova York, o usuário vê a hora como convertida em seu próprio fuso horário.

>[!ENDSHADEBOX]



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
  <tr> 
   <td role="rowheader">Nível de acesso</td> 
   <td> Você deve ser um proprietário ou um administrador de uma organização para editar o fuso horário dessa organização. </td>
   </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Exibir e gerenciar o fuso horário do usuário

1. No Fusion, clique no ícone do Perfil do Adobe na parte superior direita extrema da tela.
1. No menu que é aberto, selecione **Perfil do Fusion**.
1. Selecione a guia **Opções de Fuso Horário**. As guias estão localizadas diretamente sob seu nome.
A lista Opções de fuso horário é aberta.
1. Na área Web da lista Opções de Fuso Horário, localize seu nome.

   Sua configuração atual de fuso horário do usuário é exibida à direita do seu nome.
1. Para editar o fuso horário, clique em Editar ![Editar fuso horário](assets/edit-timezone-icon.png) ao lado do fuso horário.
1. Na janela Alterar detalhes, no campo **Fuso horário**, selecione o fuso horário que deseja definir para você mesmo.
1. Clique em **Salvar**.


## Exibir e gerenciar o fuso horário de sua organização

>[!NOTE]
>
>Você deve ser um proprietário ou um administrador de uma organização para editar o fuso horário dessa organização.

1. No Fusion, clique no ícone do Perfil do Adobe na parte superior direita extrema da tela.
1. No menu que é aberto, selecione **Perfil do Fusion**.
1. Selecione a guia **Opções de Fuso Horário**. As guias estão localizadas diretamente sob seu nome.
A lista Opções de fuso horário é aberta.
1. Na área Cenários da lista Opções de Fuso Horário, localize a organização que deseja exibir ou gerenciar o fuso horário.

   A configuração de fuso horário atual da organização é exibida à direita do nome da organização.
1. Para editar o fuso horário, clique em Editar ![Editar fuso horário](assets/edit-timezone-icon.png) ao lado do fuso horário.
1. Na janela Alterar detalhes, no campo **Fuso horário**, selecione o fuso horário que deseja definir para sua organização.
1. Clique em **Salvar**.


