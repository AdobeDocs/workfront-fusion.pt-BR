---
content-type: reference
title: 'Configurar e gerenciar organizações e equipes: índice de artigos'
description: Esta seção contém artigos relacionados à configuração e ao gerenciamento de organizações e equipes no Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 1%

---

# Excluir usuários por meio do [!DNL Adobe Admin Console]

Você pode remover um usuário somente do Adobe Workfront Fusion, deixando acesso a qualquer outro perfil de produto do [!DNL Adobe], ou pode remover o usuário totalmente do [!DNL Adobe Admin Console].

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
     <p>Você deve ser um administrador [!DNL Adobe Admin Console] da sua organização.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
