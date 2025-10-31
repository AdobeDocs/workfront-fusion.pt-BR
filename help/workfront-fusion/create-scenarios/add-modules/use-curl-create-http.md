---
title: Usar cURL para adicionar um módulo HTTP
description: Você pode colar uma solicitação cURL no seu cenário e o Fusion cria um módulo HTTP configurado a partir da solicitação cURL.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---

# Usar cURL para adicionar um módulo HTTP

Você pode colar uma solicitação cURL no seu cenário e o Fusion cria um módulo HTTP configurado a partir da solicitação cURL.

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

## Criar um módulo HTTP a partir de uma solicitação cURL


Para criar um módulo HTTP usando cURL:

1. Crie o texto da solicitação cURL fora do Fusion, como em um editor de texto.
1. Copie a solicitação cURL para a área de transferência.
1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja criar o módulo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique com o botão direito do mouse em qualquer espaço em branco no editor de cenários e selecione **Colar**.

   Ou

   Pressione Ctrl + V (Windows) ou Cmd + V (Mac).


   Um módulo HTML é criado.
1. Arraste o módulo para conectá-lo ao seu cenário.

## Solução de problemas

Se o cURL não estiver colando no seu cenário, verifique as configurações do navegador para garantir que a colagem da área de transferência esteja ativada.
