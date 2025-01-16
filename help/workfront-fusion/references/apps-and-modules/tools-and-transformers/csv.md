---
title: CSV
description: Os módulos CSV do Adobe Workfront Fusion permitem criar arquivos CSV e analisar o texto CSV de um valor de texto recebido ou de um arquivo.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 1%

---

# CSV

Os módulos [!DNL Adobe Workfront Fusion] [!UICONTROL CSV] permitem que você crie arquivos CSV e analise textos CSV de um valor de texto recebido ou de um arquivo.

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

## [!UICONTROL Create CSV]

O Agregador [!UICONTROL Create CSV] permite criar um texto csv a partir de valores de texto recebidos.

Para obter mais informações sobre agregadores, consulte [Módulo agregador](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Selecione o módulo que você está usando para agregar os campos necessários.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Aggregated Fields]</td>
        <td>Selecione os campos que deseja agregar na lista de campos disponíveis.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Include headers in the first row]</td>
        <td>Selecione essa opção para incluir os cabeçalhos no resultado.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Group by]</td>
        <td>Insira o filtro para agrupar os resultados. Por exemplo, insira uma data.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Stop processing after an empty aggregation]</td>
        <td>Selecione esta opção para interromper o cenário quando não houver resultados.</td>
    </tr>
</table>

## [!UICONTROL Create CSV (advanced)]

O Agregador [!UICONTROL Create CSV (advanced)] permite criar um texto CSV de valores de texto recebidos. Ele emprega uma estrutura de dados que define as colunas CSV no arquivo CSV resultante. Uma vez definidas, as colunas são exibidas como campos na configuração do módulo CSV e podem ser mapeadas para um módulo posterior no cenário.

Para obter mais informações sobre agregadores, consulte [Módulo agregador em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td>Selecione o módulo de aplicativo que você está usando para agregar os campos necessários.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Selecione a estrutura de dados para agregar os campos da maneira que desejar. Após definir a estrutura de dados, é possível mapear os itens para os campos correspondentes.</p> <p>Para obter mais informações, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Estruturas de dados em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include headers in the first row] </td> 
   <td>Selecione essa opção para incluir os cabeçalhos no resultado. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by] </td> 
   <td>Insira o filtro para agrupar os resultados. Por exemplo, insira uma data. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation] </td> 
   <td>Selecione esta opção para interromper o cenário quando não houver resultados. </td> 
  </tr> 
 </tbody> 
</table>


<p>Suponhamos que você deseje exportar seus contatos do Google para um arquivo CSV com duas colunas "Nome completo" e "Email". O pacote de saída do módulo [!UICONTROL Google Contacts] &gt;[!UICONTROL Get contacts from a group] tem a seguinte estrutura. Os endereços de email são armazenados dentro do item <code>[!UICONTROL Emails[]]</code>, que é uma matriz de coleções, cada coleção contendo dois itens: <code>Label</code> e <code>Email</code>.</p>
<p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png" style="width: 350;height: 546;"> </p>
<p>Se você usar o módulo simples [!DNL Create CSV], receberá uma lista de caixas de seleção correspondentes aos itens de nível superior de um pacote. Se você tentar marcar <code>Full name</code> e <code>Emails</code> itens, o módulo [!UICONTROL Create CSV] produzirá a seguinte saída, que provavelmente não é a que você deseja:</p>
<p>"emails","fullName"</p>
<p>"[object Object]","Shon Winer"</p>
<p>"[object Object]","Lizeth Fulmore"</p>
<p>"[object Object]","Hilario Gullatt"</p>
<p>"[object Object]","Abby Eisenbarth"</p>
<p>Como o item <code>Full Name</code> é do tipo Texto simples, ele é exportado sem problemas. Mas o item <code>Emails</code>, que é de um tipo complexo Matriz de Coleções, é exportado como [object Object], que é como Coleções e Matrizes são transformadas em texto por padrão. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipos de dados de item no Adobe Workfront Fusion</a>.</p>
<p>Para exportar o conteúdo do item <code>Email </code> da primeira coleção da matriz <code>Emails[]</code>, é necessário empregar o módulo [!UICONTROL Create CSV (advanced)]. O módulo permite definir colunas individuais do arquivo CSV e mapear itens para elas, incluindo as aninhadas.</p>
<ol>
<li value="1">Insira o módulo [!UICONTROL Create CSV (advanced)] em um cenário e abra sua configuração.</li>
<li value="2">Clique no botão <strong>[!UICONTROL Add]</strong> ao lado do campo [!UICONTROL Data structure] para criar uma nova Estrutura de dados.</li>
<li value="3"> <p>Escreva um nome para a estrutura de dados e clique no botão <strong>[!UICONTROL Add item]</strong> para adicionar as colunas individuais. Se você quiser exportar duas colunas: "Nome completo" e "Email", a estrutura de dados resultante será semelhante a:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png" style="width: 350;height: 524;"> </p> </li>
<li value="4"> <p>Depois de definir com êxito a Estrutura de dados, os campos correspondentes a cada coluna individual devem aparecer na configuração do módulo [!UICONTROL Create CSV (advanced)] para que você possa mapear os itens. Pegue o primeiro item da matriz <code>[!UICONTROL Emails[]]</code> e mapeie seu item <code>Email </code> para o campo/coluna Email:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png" style="width: 350;height: 308;"> </p> </li>
<li value="5"> <p>Execute o cenário. Como o item <code>Emails[1]: Email</code> mapeado para a coluna "Email" é do tipo simples Texto, ele é exportado corretamente agora:</p> <p>"Nome completo","Email"</p> <p>"Shon Winer","Shon@Winer.com"</p> <p>"Lizeth Fulmore","Lizeth@Fulmore.com"</p> <p>"Hilario Gullatt","Hilario@Gullatt.com"</p> <p>"Abby Eisenbarth","Abby@Eisenbarth.com"</p> </li>
</ol>
</div>

## [!UICONTROL Parse CSV]

O transformador [!UICONTROL Parse CSV] permite analisar o texto CSV de um valor de texto recebido ou de um arquivo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of columns]</td> 
   <td>Especifique o número de colunas no arquivo CSV.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV contains headers]</td> 
   <td> <p>Selecione essa opção se a primeira linha do texto CSV contiver cabeçalhos.</p> <p>Observação: o módulo não usa esses cabeçalhos para rotular as colunas na saída. Em vez disso, esse campo garante que os cabeçalhos não sejam incluídos nos dados de saída.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>Selecione o delimitador para o arquivo CSV. O delimitador é o caractere de texto que indica o limite entre valores ou campos separados.</p> 
    <ul> 
     <li>[!UICONTROL Comma]</li> 
     <li>[!UICONTROL Tab]</li> 
     <li> <p>[!UICONTROL Other]</p> <p>Se você selecionar [!UICONTROL Other], insira o caractere delimitador que o arquivo CSV está usando para separar valores. Digite exatamente um caractere.<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve quotes inside unquoted field]</td> 
   <td>Habilite esta opção para preservar as aspas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>Insira ou mapeie o arquivo CSV que você deseja analisar.<p>Nota: <p>Se os dados vierem em formato binário (geralmente de um arquivo), você deverá usar a função "toString()" para converter os dados binários em [!UICONTROL String]:</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png" style="width: 350;height: 123;"></p></p></td> 
  </tr> 
 </tbody> 
</table>
