---
content-type: reference
title: 'Configurar e gerenciar organizações e equipes: índice de artigos'
description: Esta seção contém artigos relacionados à configuração e ao gerenciamento de organizações e equipes no Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Excluir usuários por meio do [!DNL Adobe Admin Console]

Você pode remover um usuário somente do Adobe Workfront Fusion, deixando acesso a qualquer outro perfil de produto do [!DNL Adobe], ou pode remover o usuário totalmente do [!DNL Adobe Admin Console].

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
     <p>Você deve ser um administrador do Adobe Admin Console para sua organização.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Remover um usuário somente do Adobe Workfront Fusion

Você pode remover um usuário do Workfront Fusion enquanto deixa as outras permissões de produto do Adobe intactas.

Para obter instruções, consulte &quot;Remover usuários e grupos de usuários de um produto&quot; no artigo [Gerenciar produtos no Admin Console](https://helpx.adobe.com/br/enterprise/using/manage-products.html).

## Desativar um usuário em todos os produtos no [!DNL Adobe Admin Console]

Para excluir um usuário, você deve desativá-lo por meio do [!DNL Adobe Admin Console].

Um usuário é desativado de [!DNL Adobe Admin Console] quando uma das seguintes situações se aplicar:

* O usuário é movido de um produto ou perfil de produto e não está atribuído a nenhum outro produto ou perfil de produto.
* O usuário é removido de um grupo vinculado a um perfil de produto e não está incluído em nenhum outro grupo vinculado a um perfil de produto.
* O usuário é removido de um perfil de produto e não está atribuído a outro perfil de produto.
* O usuário é excluído ou desativado na organização que inclui o Workfront Fusion.

  Para obter instruções, consulte a seção &quot;Remover usuários&quot; em [Gerenciar usuários individualmente](https://helpx.adobe.com/br/enterprise/using/manage-users-individually.html).

No Workfront Fusion, a desativação afeta o usuário de uma das seguintes maneiras:

* Se o usuário estiver em apenas uma organização, ele será desativado.
* Se o usuário estiver em mais de uma organização, ele será removido da organização em que o usuário foi modificado no [!DNL Adobe Admin Console].
* Leve em consideração o seguinte ao excluir um usuário.

### Considerações ao excluir um usuário no Workfront Fusion

Leve em consideração o seguinte ao excluir um usuário.

* Quando um usuário é excluído, as conexões, as chaves e os webhooks do usuário são removidos.
* Quaisquer cenários pertencentes ao usuário são transferidos para o Proprietário da organização. As conexões nesses cenários devem ser atualizadas, pois as conexões pertencentes ao usuário não são mais válidas.
* Se o usuário excluído possuir quaisquer aplicativos ou modelos públicos, os aplicativos ou modelos públicos serão transferidos para o Proprietário da organização. Se não houver um Proprietário da organização, os aplicativos ou modelos públicos serão transferidos para outro usuário.
