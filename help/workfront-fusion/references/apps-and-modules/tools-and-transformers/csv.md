---
title: CSV
description: Os módulos CSV do Adobe Workfront Fusion permitem criar arquivos CSV e analisar o texto CSV de um valor de texto recebido ou de um arquivo.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 5971b2210eaac8f8a75fd7a4aac5a9f7954d27ef
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# CSV

Os módulos [!DNL Adobe Workfront Fusion] [!UICONTROL CSV] permitem que você crie arquivos CSV e analise textos CSV de um valor de texto recebido ou de um arquivo.

Como esse é um transformador, esses módulos não exigem uma conexão.

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

## [!UICONTROL Create CSV]

O Agregador [!UICONTROL Create CSV] permite criar um texto csv a partir de valores de texto recebidos.

Para obter mais informações sobre agregadores, consulte [Módulo agregador](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Selecione o módulo que gera os campos que você deseja usar para criar o CSV.</td>
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

Para obter mais informações sobre agregadores, consulte [Módulo agregador](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
        <td>Selecione o módulo que gera os campos que você deseja usar para criar o CSV.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Selecione a estrutura de dados para agregar os campos da maneira que desejar. Após definir a estrutura de dados, é possível mapear os itens para os campos correspondentes.</p> <p>Para obter mais informações, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Estruturas de dados</a>.</p> </td> 
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


>[!BEGINSHADEBOX]

**Exemplo**:

Este exemplo mostra como exportar contatos do Google para um arquivo CSV com duas colunas chamadas &quot;Nome completo&quot; e &quot;Email&quot;. O pacote de saída do módulo [!UICONTROL Google Contacts] > [!UICONTROL Get contacts from a group] tem a seguinte estrutura. Os endereços de email são armazenados no <code>[!UICONTROL Emails[]]</code> item, que é uma matriz de coleções, cada coleção contém dois itens: <code>Rótulo</code> e <code>Email</code>.
![Transformando](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

O módulo simples [!DNL Create CSV] oferece uma lista de caixas de seleção correspondentes aos itens de nível superior de um pacote. Se você tentar selecionar <code>Nome completo</code> e <code>Emails</code> itens, o módulo [!UICONTROL Create CSV] produz a seguinte saída, que pode não ser a desejada:

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

Porque o item <code>Nome completo</code> é do tipo simples Text, é exportado conforme esperado. O item <code>Emails</code>, que é de um tipo complexo Matriz de Coleções, é exportado como [objeto Objeto], que é a forma como as Coleções e as Matrizes são transformadas em texto por padrão.

Para obter mais informações, consulte [Tipos de dados de item](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).


Para exportar o conteúdo do email <code> </code>item da primeira coleção de <code>Emails[]</code> em vez disso, você deve usar o módulo [!UICONTROL Create CSV (advanced)]. Esse módulo permite definir colunas individuais do arquivo CSV e mapear itens para elas, incluindo as aninhadas.

1. Insira o módulo [!UICONTROL Create CSV (advanced)] em um cenário.
1. Clique no botão <strong>[!UICONTROL Add]</strong> ao lado do campo [!UICONTROL Data structure] para criar uma nova estrutura de dados.
1. Insira um nome para a estrutura de dados e clique em <strong>[!UICONTROL Add item]</strong> para adicionar as colunas individuais. Para exportar duas colunas: &quot;Nome completo&quot; e &quot;Email&quot;, a estrutura de dados resultante seria semelhante a:

   ![Saída de contatos do Google](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. Após definir a estrutura de dados, os campos correspondentes a cada coluna individual aparecem na configuração do módulo [!UICONTROL Create CSV (advanced)] para que você possa mapear os itens. Pegar o primeiro item de <code>[!UICONTROL Emails[]]</code> matriz e mapear seu item <code>Email </code>para o campo/coluna Email:

   ![Criar módulo CSV avançado](/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png)

1. Execute o cenário. Porque o item <code>Emails[1]: Email</code> mapeado para a coluna &quot;Email&quot; é do tipo simples Texto, ele é exportado corretamente.

```
"Full Name","Email"
"Shon Winer","Shon@Winer.com"
"Lizeth Fulmore","Lizeth@Fulmore.com"
"Hilario Gullatt","Hilario@Gullatt.com"
"Abby Eisenbarth","Abby@Eisenbarth.com"
```

>[!ENDSHADEBOX]

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
   <td>Insira ou mapeie o arquivo CSV que você deseja analisar.<p>Nota: <p>Se os dados vierem em formato binário (geralmente de um arquivo), você deverá usar a função "toString()" para converter os dados binários em [!UICONTROL String]:</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>
