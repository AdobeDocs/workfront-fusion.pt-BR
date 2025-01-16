---
title: Módulos de imagem
description: Os módulos do Adobe Workfront Fusion Image permitem obter informações sobre uma imagem específica (dimensões, tipo e assim por diante), converter uma imagem em outro formato de arquivo e alterar diretamente o tamanho da imagem.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Módulos de imagem

[!DNL Adobe Workfront Fusion] módulos do [!UICONTROL Image] permitem obter informações sobre uma imagem específica (dimensões, tipo e assim por diante), converter uma imagem em outro formato de arquivo e alterar diretamente o tamanho da imagem.

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho, [!UICONTROL [!DNL Workfront Fusion] para Automação do Trabalho</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano [!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Adobe Workfront], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## [!UICONTROL Image] módulos e seus campos

Ao configurar esse módulo, os campos a seguir são exibidos. Um título em negrito em um módulo indica um campo obrigatório.

* [[!UICONTROL Resize]](#resize)
* [[!UICONTROL Convert a format]](#convert-a-format)
* [[!UICONTROL Extract metadata]](#extract-metadata)

### [!UICONTROL Resize]

Esse módulo de transformador altera a altura e a largura de uma imagem de acordo com os critérios especificados.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione a origem da imagem que deseja converter. Você pode selecionar a saída de um módulo anterior ou mapear o arquivo de dados e o nome do arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>Mapeie o arquivo que deseja converter. Este campo estará disponível se você tiver selecionado [!UICONTROL Map] no campo [!UICONTROL Source file].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Insira um nome para o arquivo convertido. Este campo estará disponível se você tiver selecionado [!UICONTROL Map] no campo [!UICONTROL Source file].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to]</td> 
   <td>Selecione se deseja manter a proporção altura-largura ou alterar as dimensões para uma altura e largura especificadas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL According to]</td> 
   <td> <p>Selecione como deseja que o módulo determine o novo tamanho da imagem. Este campo será exibido se você tiver selecionado a opção para manter a proporção altura/largura no campo Desejo. Outros campos são exibidos com base na seleção deste campo.</p> 
    <ul> 
     <li> <p>[!UICONTROL Maximum width]</p> <p>Reduz uma imagem a uma largura especificada. A altura é calculada automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Maximum height]</p> <p>Reduz uma imagem a uma altura especificada. A largura é calculada automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Maximum height or width]</p> <p>Reduz uma imagem de forma que sua altura e largura não excedam os valores especificados. Como essa opção mantém a relação altura/largura, uma das dimensões pode ser menor do que o especificado. Por exemplo, se altura e largura forem especificadas como 40, uma imagem 400x300 será reduzida para 40X30.</p> </li> 
     <li> <p>[!UICONTROL Minimum width]</p> <p>Amplia uma imagem até a largura especificada. A altura é calculada automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Minimum height]</p> <p>Amplia uma imagem para uma altura especificada por você. A largura é calculada automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Minimum height or width]</p> <p>Amplia uma imagem de forma que sua altura e largura não sejam menores que os valores especificados. Como essa opção mantém a relação altura/largura, uma das dimensões pode ser maior do que o especificado. Por exemplo, se altura e largura forem especificadas como 300, uma imagem 40x30 será ampliada para 400X300.</p> </li> 
     <li> <p>[!UICONTROL Percent]</p> <p>Altera o tamanho da imagem em uma porcentagem com base no valor especificado. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Width]</td> 
   <td>Insira ou mapeie a largura desejada da imagem redimensionada em pixels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Height]</td> 
   <td>Insira ou mapeie a altura desejada da imagem redimensionada em pixels.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert a format]

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
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione a origem da imagem que deseja converter. Você pode selecionar a saída de um módulo anterior ou mapear o arquivo de dados e o nome do arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>Mapeie o arquivo que deseja converter. Este campo estará disponível se você tiver selecionado [!UICONTROL Map] no campo [!UICONTROL Source file].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Insira um nome para o arquivo convertido. Este campo estará disponível se você tiver selecionado [!UICONTROL Map] no campo [!UICONTROL Source file].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output format]</td> 
   <td>Selecione o formato para o qual você deseja que o módulo converta o arquivo de origem. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Extract metadata]

Este módulo de transformador retorna informações básicas sobre um módulo.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione a origem da imagem que deseja converter. Você pode selecionar a saída de um módulo anterior ou mapear o arquivo de dados e o nome do arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>Mapeie o arquivo que deseja converter. Este campo estará disponível se você tiver selecionado Mapear no campo [!UICONTROL Source file].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Insira um nome para o arquivo convertido. Este campo estará disponível se você tiver selecionado Mapear no campo [!UICONTROL Source file].</td> 
  </tr> 
 </tbody> 
</table>

## Possíveis problemas

### Ação encerrada com erro

Há três casos em que uma ação pode ser encerrada com um erro:

* Os dados recebidos não estavam no formato JPG/GIF/PNG/BMP
* O limite máximo de largura/altura foi excedido ao alterar as dimensões da imagem. O tamanho da imagem não deve exceder a largura e a altura de 3840 px
* O tamanho máximo permitido de uma imagem foi excedido durante a alteração das dimensões ou do formato da imagem.
