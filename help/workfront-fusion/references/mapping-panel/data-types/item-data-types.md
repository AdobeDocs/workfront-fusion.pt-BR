---
title: Tipos de dados de item
description: Seus  [!DNL Adobe Workfront Fusion] cenários podem conter os tipos de itens listados abaixo em um pacote.
author: Becky
feature: Workfront Fusion
exl-id: 3ad65959-5c19-4727-bc9d-4ff1d238ad8b
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Tipos de dados de item

Você pode conter os tipos de itens listados abaixo em um pacote.

Para obter informações sobre quais tipos de itens [!DNL Workfront Fusion] permitem a conversão entre si, consulte [Coerção de tipo](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Texto</p> </td> 
   <td> <p>O tipo de item mais comum. Para alguns itens de texto, o [!DNL Adobe Workfront Fusion] verifica se o comprimento máximo ou mínimo permitido foi atingido ou se o item executa a validação de formato (email, URL ou nome de arquivo).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Número</p> </td> 
   <td> <p>Para alguns itens numéricos, [!DNL Workfront Fusion] pode validar a entrada para um intervalo especificado (o valor mínimo ou máximo permitido).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Booleano (Sim/Não)</p> </td> 
   <td> <p>Esse tipo é usado para itens com apenas dois valores possíveis: verdadeiro ou falso. </p> <p>Ao definir módulos, o tipo Booleano pode aparecer de duas formas diferentes:</p> 
    <ul> 
     <li> <p>A caixa de seleção obrigatória é exibida caso o campo seja obrigatório e deva ser preenchido.</p> <p> <img src="assets/boolean-checkbox-350x158.jpg" style="width: 350;height: 158;"> </p> </li> 
     <li> <p>Campos opcionais que podem ser deixados em branco são exibidos como uma caixa de seleção, permitindo a seleção entre três valores: <code>Yes</code>, <code>No</code> e <code>Not defined</code> (padrão).</p> <p> <img src="assets/boolean-convert-file-350x129.jpg" style="width: 350;height: 129;"> </p> </li> 
    </ul> <p>Você pode clicar em <strong>[!UICONTROL Map]</strong> se precisar mapear o valor para um item de outro módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data</p> </td> 
   <td> <p>As datas são inseridas no formato de data ISO 8601, por exemplo, <code>2015-09-18T11:58Z</code>. Você pode alterar o fuso horário nas configurações do perfil. </p> <p>Se você clicar em um campo que requer uma data, um calendário pop-up será exibido nas configurações do módulo. O tempo não é necessário para alguns itens.</p> <p>Os valores dos itens de Data são formatados usando o fuso horário local e da Web selecionado no seu perfil. É possível exibir a versão ISO 8601 do valor de um item de data, passando o mouse sobre o item.</p> <p>Observação: se o valor ISO não for exibido, o item provavelmente é um texto, não uma data.</p> <p>A hora é inserida no formato <code>hours:minutes:seconds</code>, por exemplo, <code>14:03:52</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Buffer (dados binários)</p> </td> 
   <td> <p>O conteúdo do arquivo geralmente é enviado como conteúdo do tipo Buffer (conteúdo de imagem, arquivo de vídeo e outros). Em alguns casos, dados de texto são incluídos nesse tipo (por exemplo, um arquivo de texto). O [!DNL Workfront Fusion] pode converter automaticamente dados de texto em código binário em texto e texto em dados de texto em código binário. Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/map-data/map-files.md" class="MCXref xref">Arquivos de mapa</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Coleção</p> </td> 
   <td> <p>Uma coleção é um item que consiste em vários subitens. O item Remetente em uma mensagem de email é um exemplo de uma coleção: ele contém o nome do remetente (tipo de texto) e o endereço de email do remetente (tipo de texto).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Selecionar (menu)</p> </td> 
   <td> <p>Ao definir as configurações do módulo, é possível selecionar entre vários itens do mesmo tipo. Um exemplo é o menu de seleção de pasta nas configurações dos módulos [!DNL Dropbox]. </p> <p>Ao configurar módulos, o menu de seleção pode aparecer de duas formas:</p> <p> <p>Se for possível fazer várias seleções, vários itens com caixas de seleção serão exibidos.</p> <p> <img src="assets/image-kb-type-list-multi-350x232.jpg" style="width: 350;height: 232;"> </p> </p> <p>Se apenas uma opção for possível, um menu suspenso será exibido.</p> <p> <img src="assets/select-menu-dropdown-350x130.jpg" style="width: 350;height: 130;"> </p> <p>Se você precisar mapear um item de outro módulo, use o botão <strong>Mapear</strong>. Esse botão abre um campo de texto em vez do menu de seleção. Para obter mais informações sobre mapeamento, consulte <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md" class="MCXref xref">Visão geral do mapeamento</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Matriz</p> </td> 
   <td> <p>Você pode usar o tipo de matriz para trabalhar com vários valores do mesmo tipo, incluindo coleções. Um exemplo são os módulos [!UICONTROL Email]: eles retornam uma matriz de anexos e cada anexo contém nome, conteúdo, tamanho e assim por diante. Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/map-data/map-an-array.md" class="MCXref xref">Mapear uma matriz ou elemento de matriz</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Validação</p> </td> 
   <td> <p>[!DNL Workfront Fusion] executar a validação em cada tipo de item. Se um item não passar na validação, o módulo parará de ser processado devido a um erro de dados. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/errors/error-processing.md" class="MCXref xref">Tipos de erro </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
