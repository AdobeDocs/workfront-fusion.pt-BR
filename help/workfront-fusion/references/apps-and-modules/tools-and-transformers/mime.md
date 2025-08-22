---
title: Módulos MIME
description: Você pode usar tipos MIME no Adobe Workfront Fusion. Os tipos MIME (Multipurpose Internet Mail Extension) são rótulos que permitem que o software identifique diferentes tipos de dados compartilhados na Internet. Servidores da Web e navegadores usam o tipo MIME para determinar o que deve ser feito com um arquivo. Por exemplo, um arquivo com o tipo MIME text/html será processado em um navegador de forma diferente de um arquivo com o tipo MIME image/jpeg. Os tipos MIME funcionam independentemente do sistema operacional e do hardware.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# Módulos [!UICONTROL MIME]

Você pode usar tipos MIME no Adobe Workfront Fusion. Os tipos MIME (Multipurpose Internet Mail Extension) são rótulos que permitem que o software identifique diferentes tipos de dados compartilhados na Internet. Servidores da Web e navegadores usam o tipo MIME para determinar o que deve ser feito com um arquivo. Por exemplo, um arquivo com o tipo MIME `text/html` será processado em um navegador de forma diferente de um arquivo com o tipo MIME `image/jpeg`. Os tipos MIME funcionam independentemente do sistema operacional e do hardware.

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
   <td> <p>Novo: Padrão</p><p>Ou</p><p>Atual: trabalho ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Nenhum requisito de licença do Workfront Fusion</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo menu:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Módulos [!UICONTROL MIME] e seus campos

* [Obter uma extensão de arquivo](#get-a-file-extension)
* [Obter um tipo MIME](#get-a-mime-type)

### [!UICONTROL Obter uma extensão de arquivo]

Este módulo de transformador retorna a extensão de arquivo original para um determinado tipo de MIME.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL tipo MIME]</td> 
   <td> <p>Insira ou mapeie o tipo MIME para o qual você deseja determinar a extensão de arquivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Obter um tipo MIME]

Esse módulo de transformador retorna o tipo MIME associado a um determinado nome de arquivo, caminho ou extensão.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivo]</td> 
   <td> <p>Insira ou mapeie o arquivo para o qual você deseja determinar o tipo de MIME. </p> <p>Você pode inserir o arquivo usando:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Caminho do Arquivo]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL Nome do Arquivo]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL Extensão de Arquivo]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
