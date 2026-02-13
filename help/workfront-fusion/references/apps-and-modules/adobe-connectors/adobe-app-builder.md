---
title: Módulo App Builder do Adobe
description: O conector App Builder do Adobe permite usar funções personalizadas em seus cenários.
author: Becky
feature: Workfront Fusion
source-git-commit: 8250d4fdad8ed7ffe63cd003f6e0cb325cbbfa8d
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 31%

---

# Módulo App Builder do Adobe

É possível criar funções personalizadas na área Funções do Fusion. Em seguida, adicione essas funções aos seus cenários na forma de um módulo do Adobe App Builder.

Como as funções personalizadas funcionam por meio do Adobe App Builder, sua organização deve ter uma licença do Adobe App Builder para usá-las.

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
   <p><ul><li>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li><li>Você deve ter uma licença do Adobe App Builder para usar funções personalizadas.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Módulo App Builder do Adobe

O único módulo do Adobe App Builder disponível no momento é Executar uma ação, que permite usar uma função personalizada do JavaScript configurada anteriormente.

Para obter instruções sobre como configurar uma função personalizada, consulte [Mapear dados usando funções personalizadas](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

### Executar uma ação

Este módulo executa uma função personalizada configurada anteriormente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Selecione a conexão que contém a função personalizada que você deseja executar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Selecione a função personalizada que deseja executar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parâmetros] </td> 
   <td>Insira os valores dos parâmetros da função. Os parâmetros disponíveis são baseados nos parâmetros configurados quando a função foi criada.<p>Se um parâmetro tiver um valor padrão, você não o verá no campo, mas poderá substituí-lo inserindo ou mapeando um valor no campo.</p></td> 
  </tr> 
   </tbody> 
</table>


