---
title: Módulos JSON
description: O aplicativo JSON do Adobe Workfront Fusion fornece módulos para processar dados no formato JSON, de modo que o Adobe Workfront Fusion possa trabalhar ainda mais com o conteúdo de dados ou criar novo conteúdo JSON.
author: Becky
feature: Workfront Fusion
exl-id: f8b281c5-bb63-4412-98c5-d82f45f8eafc
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# [!UICONTROL JSON] módulos

O aplicativo [!DNL Adobe Workfront Fusion] [!UICONTROL JSON] fornece módulos para processar dados no formato JSON, de modo que [!DNL Adobe Workfront Fusion] possa trabalhar mais com o conteúdo de dados ou criar novo conteúdo JSON.

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

## Analisar JSON

* [Estrutura de dados](#data-structure)
* [Coleção versus array](#collection-vs-array)

### Estrutura de dados

A estrutura de dados descreve como os dados JSON são organizados e permite o mapeamento de itens JSON individuais para outros módulos em seu cenário. Se você não fornecer a estrutura de Dados, poderá executar o módulo manualmente e o [!DNL Workfront Fusion] criará a estrutura do JSON fornecido:

1. Adicione o módulo [!UICONTROL Parse JSON] a um cenário.
1. No campo **[!UICONTROL JSON String]**, insira o JSON do qual deseja criar uma estrutura de dados.
1. Não conecte outros módulos ao módulo [!UICONTROL Parse JSON] ainda. Como [!DNL Workfront Fusion] ainda não sabe a estrutura dos dados JSON, ainda não é possível mapear dados do módulo [!UICONTROL Parse JSON] para outros módulos em seu cenário.
1. Execute o cenário manualmente. Isso permite que o módulo [!UICONTROL Parse JSON] identifique a estrutura JSON do JSON fornecido.
1. Agora você pode conectar os seguintes módulos. Os itens do módulo JSON de análise agora estão disponíveis para mapeamento.

Para obter mais informações, consulte [Estruturas de dados em [!UICONTROL Adobe Workfront Fusion]](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

### Coleção versus array

Se o campo de cadeia de caracteres JSON contiver uma coleção `{ ... }`, a saída será um único pacote contendo os itens da coleção.

>[!INFO]
>
>**Exemplo:**
>
>```
>{
>    "name" : "Peter",
>
>    "ID" : 1
>}
>```
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/json-collection.png)

Se o campo de cadeia de caracteres JSON contiver uma matriz `[ ... ]`, a saída será uma série de pacotes. cada pacote contém um elemento da matriz.

>[!INFO]
>
>**Exemplo:**
>
>```
>[
>  {
>    "name" : "Peter",
>    "ID" : 1
>  },
>
>  {
>    "name" : "Mike",
>    "ID" : 2
>  }
>]
>```
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/json-array.png)

## [!UICONTROL JSON] módulos e seus campos

Ao configurar módulos do [!DNL JSON], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos JSON adicionais podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Converter JSON em XML](#convert-json-to-xml)
* [Analisar JSON](#parse-json)
* [Criar JSON](#create-json)
* [Transformar JSON](#transform-json)

### Agregadores

#### [!UICONTROL Aggregate to JSON]

Esse módulo agregador agrega a saída de um módulo anterior no JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module] </td> 
   <td> <p>Selecione o módulo que gera os dados que você deseja agregar ao JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>Selecione a estrutura de dados que deseja usar para criar JSON. A estrutura de dados determina quais outros campos estão disponíveis nesse módulo. Para obter mais informações, consulte <a href="#data-structure" class="MCXref xref">Estrutura de dados</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Indentation]</td> 
   <td> <p> Selecione se deseja recuar o JSON usando tabulações, dois espaços ou quatro espaços.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by]</td> 
   <td>Defina uma expressão pela qual você deseja agrupar a saída agregada. Esta expressão pode conter um ou mais itens mapeados. Os dados agregados são, então, separados em grupos usando o valor dessa expressão. Cada grupo gera um pacote separado com uma chave (a expressão avaliada) e um valor (o texto agregado). Você pode usar a chave como um filtro nos módulos subsequentes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Habilite essa opção para interromper o cenário quando não houver resultados.</td> 
  </tr> 
 </tbody> 
</table>

### Transformadores

* [Converter JSON em XML](#convert-json-to-xml)
* [Criar JSON](#create-json)
* [Analisar JSON](#parse-json)
* [Transformar JSON](#transform-json)

#### [!UICONTROL Convert JSON to XML]

Esse módulo de ação converte uma sequência de caracteres JSON em XML.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>Insira ou mapeie o JSON que você deseja converter em XML.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create JSON]

Esse módulo de ação cria o JSON a partir de uma estrutura de dados.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Estrutura de dados</td> 
   <td> <p>Selecione a estrutura de dados que deseja usar para criar JSON. Para obter mais informações, consulte <a href="#data-structure" class="MCXref xref">Estrutura de dados</a> neste artigo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Parse JSON]

Esse módulo de ação analisa uma sequência JSON em uma estrutura de dados, que permite acessar os dados dentro da sequência JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>Selecione a estrutura de dados que deseja usar para criar JSON. Para obter mais informações, consulte <a href="#data-structure" class="MCXref xref">Estrutura de dados</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>Insira ou mapeie o JSON que deseja analisar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Transform JSON]

Esse módulo de ação transforma um objeto em uma sequência de caracteres json.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object]</td> 
   <td> <p>Insira ou mapeie o objeto que deseja transformar em JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Transformação de registros de dados em JSON

>[!INFO]
>
>**Exemplo:** o exemplo a seguir mostra como transformar registros de dados de [!DNL Google Sheets] para o formato JSON:
>
>1. Coloque o módulo [!DNL Google Sheets] > [!UICONTROL Select rows] no seu cenário para buscar os dados. Configure o módulo para recuperar linhas da planilha [!DNL Google]. Defina o&#x200B;**[!UICONTROL Maximum number of returned rows]** como um número pequeno, mas maior que um para fins de teste (Exemplo, três). Execute o módulo [!DNL Google Sheets] clicando com o botão direito do mouse nele e escolhendo &quot;**[!UICONTROL Run this module only]**&quot;. Verifique a saída do módulo.
>
>1. Conecte o módulo [!UICONTROL Array Aggregator] após o módulo [!DNL Google Sheets]. Na configuração do módulo, escolha o módulo [!DNL Google Sheets] no campo **[!UICONTROL Source node]**. Deixe os outros campos como estão para o momento.
>
>1. Conecte o módulo [!UICONTROL JSON] > [!UICONTROL Create JSON] após o módulo [!UICONTROL Array Aggregator]. A configuração do módulo requer uma estrutura de dados que descreva o formato JSON. Clique em **[!UICONTROL Add]** para abrir a configuração da estrutura de dados. A maneira mais fácil de criar essa estrutura de dados é gerá-la automaticamente a partir de uma amostra JSON. Clique em **[!UICONTROL Generator]** e cole sua amostra JSON no campo **[!UICONTROL Sample data]**:
>
>     **Exemplo:**
>
>     ```
>     {
>     
>     "books": [
>     
>     {
>     
>     "id": "ID",
>     
>     "title": "Title",
>     
>     "author": "Author"
>     
>     }
>     
>     ]
>     
>     }
>     
>     ```
>
>1. Clique em **[!UICONTROL Save]**. O campo [!UICONTROL Specification] na estrutura de dados agora contém a estrutura gerada.
>1. Altere o nome da estrutura de Dados para algo mais específico e clique em **[!UICONTROL Save]**. Um campo correspondente ao atributo de matriz raiz aparece como um campo mapeável na configuração do módulo JSON.
>
>1. Clique no botão **[!UICONTROL Map]** ao lado do campo e mapeie o item `Array[]` da saída do agregador de matriz para ele.
>
>1. Clique em **[!UICONTROL OK]** para fechar a configuração do módulo [!UICONTROL JSON].
>
>1. Abra a configuração do módulo [!UICONTROL Array Aggregator]. Altere o **[!UICONTROL Target structure]** de [!UICONTROL Custom] para o campo do módulo [!UICONTROL JSON] correspondente ao atributo de matriz raiz. Mapeie itens do módulo [!DNL Google Sheets] para os campos apropriados.
>
>1. Clique em **[!UICONTROL OK]** para fechar a configuração do módulo [!UICONTROL Array Aggregator].
>
>1. Execute o cenário.
>
>O módulo [!UICONTROL JSON] gera o formato JSON correto.
>
>1. Abra a configuração do módulo [!DNL Google Sheets] e aumente o número [!UICONTROL Maximum number of returned rows] para que seja maior que o número de linhas na planilha para processar todos os dados.

## Solução de problemas

### Não é possível mapear dados do módulo [!UICONTROL Parse JSON]

Verifique se o conteúdo JSON está mapeado corretamente no módulo [!UICONTROL Parse JSON] e se a estrutura de dados está definida corretamente. Para obter mais informações, consulte [Transformando registros de dados em JSON](#transforming-data-records-to-json) neste artigo.

### O módulo falha ao usar declarações condicionais em JSON

Ao usar instruções condicionais como `if` em seu JSON, coloque as aspas fora da instrução condicional.

>[!INFO]
>
>**Exemplo:**
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png)
