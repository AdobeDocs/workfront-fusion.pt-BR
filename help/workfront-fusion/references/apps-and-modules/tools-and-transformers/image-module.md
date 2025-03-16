---
title: Módulos de imagem
description: Os módulos do Adobe Workfront Fusion Image permitem obter informações sobre uma imagem específica (dimensões, tipo e assim por diante), converter uma imagem em outro formato de arquivo e alterar diretamente o tamanho da imagem.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---

# Módulos de imagem

Os módulos [!DNL Adobe Workfront Fusion] [!UICONTROL Image] permitem obter informações sobre uma imagem específica (dimensões, tipo e assim por diante), converter uma imagem em outro formato de arquivo e alterar diretamente o tamanho da imagem.

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
   <p>Novo:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Módulos [!UICONTROL Image] e seus campos

Ao configurar esse módulo, os campos a seguir são exibidos. Um título em negrito em um módulo indica um campo obrigatório.

* [[!UICONTROL Converter um formato]](#convert-a-format)
* [[!UICONTROL Extrair metadados]](#extract-metadata)
* [[!UICONTROL Redimensionar]](#resize)

### [!UICONTROL Converter um formato]

Esse módulo de transformador altera o formato de um arquivo de imagem. Este módulo é compatível com os seguintes formatos:

* Imagem PNG
* JPG
* GIF
* BMP

O arquivo de origem e a saída devem estar em um desses formatos. Por exemplo, o módulo [!UICONTROL Image] >[!UICONTROL Convert a format] pode transformar um arquivo PNG em um arquivo BMP ou um BMP em um JPG.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de saída]</td> 
   <td>Selecione o formato para o qual você deseja que o módulo converta o arquivo de origem. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Extrair metadados]

Este módulo de transformador retorna informações básicas sobre um módulo.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Redimensionar]

Esse módulo de transformador altera a altura e a largura de uma imagem de acordo com os critérios especificados.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL que eu desejo]</td> 
   <td>Selecione se deseja manter a proporção altura-largura ou alterar as dimensões para uma altura e largura especificadas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL De acordo com]</td> 
   <td> <p>Selecione como deseja que o módulo determine o novo tamanho da imagem. Este campo será exibido se você tiver selecionado a opção para manter a proporção altura/largura no campo Desejo. Outros campos são exibidos com base na seleção deste campo.</p> 
    <ul> 
     <li> <p>[!UICONTROL Largura máxima]</p> <p>Reduz uma imagem a uma largura especificada. A altura é calculada automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Altura máxima]</p> <p>Reduz uma imagem a uma altura especificada. A largura é calculada automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Altura ou largura máxima]</p> <p>Reduz uma imagem de forma que sua altura e largura não excedam os valores especificados. Como essa opção mantém a relação altura/largura, uma das dimensões pode ser menor do que o especificado. Por exemplo, se altura e largura forem especificadas como 40, uma imagem 400x300 será reduzida para 40X30.</p> </li> 
     <li> <p>[!UICONTROL Largura mínima]</p> <p>Amplia uma imagem até a largura especificada. A altura é calculada automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Altura mínima]</p> <p>Amplia uma imagem para uma altura especificada por você. A largura é calculada automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Altura ou largura mínima]</p> <p>Amplia uma imagem de forma que sua altura e largura não sejam menores que os valores especificados. Como essa opção mantém a relação altura/largura, uma das dimensões pode ser maior do que o especificado. Por exemplo, se altura e largura forem especificadas como 300, uma imagem 40x30 será ampliada para 400X300.</p> </li> 
     <li> <p>[!UICONTROL Porcentagem]</p> <p>Altera o tamanho da imagem em uma porcentagem com base no valor especificado. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Largura]</td> 
   <td>Insira ou mapeie a largura desejada da imagem redimensionada em pixels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Altura]</td> 
   <td>Insira ou mapeie a altura desejada da imagem redimensionada em pixels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Alteração por porcentagem]</td> 
   <td>Se você optou por alterar a imagem por porcentagem, insira ou mapeie a porcentagem desejada para alterar a imagem.</td> 
  </tr> 
 </tbody> 
</table>

## Solução de problemas

### Ação encerrada com erro

uma ação pode ser finalizada com um erro devido a uma das seguintes causas:

* Os dados recebidos não estão no formato JPG/GIF/PNG/BMP
* O limite máximo de largura/altura foi excedido ao alterar as dimensões da imagem. O tamanho da imagem não deve exceder a largura e a altura de 3840 px
* O tamanho máximo permitido de uma imagem foi excedido durante a alteração das dimensões ou do formato da imagem.
