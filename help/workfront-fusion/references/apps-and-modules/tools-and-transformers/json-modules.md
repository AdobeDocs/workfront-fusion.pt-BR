---
title: Módulos JSON
description: O aplicativo JSON do Adobe Workfront Fusion fornece módulos para processar dados no formato JSON, de modo que o Adobe Workfront Fusion possa trabalhar ainda mais com o conteúdo de dados ou criar novo conteúdo JSON.
author: Becky
feature: Workfront Fusion
exl-id: f8b281c5-bb63-4412-98c5-d82f45f8eafc
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '1229'
ht-degree: 1%

---

# [!UICONTROL JSON] módulos

O aplicativo Adobe Workfront Fusion [!UICONTROL JSON] fornece módulos para processar dados no formato JSON, de modo que o Adobe Workfront Fusion possa trabalhar ainda mais com o conteúdo de dados ou criar novo conteúdo JSON.

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



## Considerações ao analisar o JSON

* [Estrutura de dados](#data-structure)
* [Coleção versus array](#collection-vs-array)

### Estrutura de dados

A estrutura de dados descreve como os dados JSON são organizados e permite o mapeamento de itens JSON individuais para outros módulos em seu cenário. Se você não fornecer a estrutura de dados, poderá executar o módulo manualmente e o Workfront Fusion criará a estrutura do JSON fornecido:

1. Adicione o módulo [!UICONTROL Parse JSON] a um cenário.
1. No campo **[!UICONTROL Cadeia de Caracteres JSON]**, digite o JSON a partir do qual deseja criar uma estrutura de dados.
1. Não conecte outros módulos ao módulo [!UICONTROL Parse JSON] ainda. Como o Workfront Fusion ainda não conhece a estrutura dos dados JSON, ainda não é possível mapear dados do módulo [!UICONTROL Analisar JSON] para outros módulos em seu cenário.
1. Execute o cenário manualmente. Isso permite que o módulo [!UICONTROL Analisar JSON] identifique a estrutura JSON do JSON fornecido.
1. Agora você pode conectar os seguintes módulos. Os itens do módulo JSON de análise agora estão disponíveis para mapeamento.

Para obter mais informações, consulte [Estruturas de dados no [!UICONTROL Adobe Workfront Fusion]](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

### Coleção versus array

Se o campo de cadeia de caracteres JSON contiver uma coleção `{ ... }`, a saída será um único pacote contendo os itens da coleção.

>[!BEGINSHADEBOX]

**Exemplo:**

```
{
    "name" : "Peter",

    "ID" : 1>}
```


![Coleção JSON](/help/workfront-fusion/references/apps-and-modules/assets/json-collection.png)

>[!ENDSHADEBOX]

Se o campo de cadeia de caracteres JSON contiver uma matriz `[ ... ]`, a saída será uma série de pacotes. cada pacote contém um elemento da matriz.

>[!BEGINSHADEBOX]

**Exemplo:**

```
[
  {
    "name" : "Peter",
    "ID" : 1
  },

  {
    "name" : "Mike",
    "ID" : 2
  }
]
```

![Matriz JSON](/help/workfront-fusion/references/apps-and-modules/assets/json-array.png)

>[!ENDSHADEBOX]

## [!UICONTROL JSON] módulos e seus campos

Ao configurar módulos do [!DNL JSON], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos JSON adicionais podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Converter JSON em XML](#convert-json-to-xml)
* [Analisar JSON](#parse-json)
* [Criar JSON](#create-json)
* [Transformar JSON](#transform-json)

### Agregadores

#### [!UICONTROL Agregar para JSON]

Esse módulo agregador agrega a saída de um módulo anterior no JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL módulo Source] </td> 
   <td> <p>Selecione o módulo que gera os dados que você deseja agregar ao JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estrutura de dados]</td> 
   <td> <p>Selecione a estrutura de dados que deseja usar para criar JSON. A estrutura de dados determina quais outros campos estão disponíveis nesse módulo. Para obter mais informações, consulte <a href="#data-structure" class="MCXref xref">Estrutura de dados</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recuo]</td> 
   <td> <p> Selecione se deseja recuar o JSON usando tabulações, dois espaços ou quatro espaços.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agrupar por]</td> 
   <td>Defina uma expressão pela qual você deseja agrupar a saída agregada. Esta expressão pode conter um ou mais itens mapeados. Os dados agregados são, então, separados em grupos usando o valor dessa expressão. Cada grupo gera um pacote separado com uma chave (a expressão avaliada) e um valor (o texto agregado). Você pode usar a chave como um filtro nos módulos subsequentes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parar processamento após uma agregação vazia]</td> 
   <td>Habilite essa opção para interromper o cenário quando não houver resultados.</td> 
  </tr> 
 </tbody> 
</table>

### Transformadores

* [Converter JSON em XML](#convert-json-to-xml)
* [Criar JSON](#create-json)
* [Analisar JSON](#parse-json)
* [Transformar JSON](#transform-json)

#### [!UICONTROL Converter JSON em XML]

Esse módulo de ação converte uma sequência de caracteres JSON em XML.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL cadeia de caracteres JSON] </td> 
   <td> <p>Insira ou mapeie o JSON que você deseja converter em XML.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar JSON]

Esse módulo de ação cria o JSON a partir de uma estrutura de dados.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Estrutura de dados</td> 
   <td> <p>Selecione a estrutura de dados que deseja usar para criar JSON. Para obter mais informações, consulte <a href="#data-structure" class="MCXref xref">Estrutura de dados</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recuo</td> 
   <td> <p>Selecione o recuo que deseja usar para este JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Analisar JSON]

Esse módulo de ação analisa uma sequência JSON em uma estrutura de dados, que permite acessar os dados dentro da sequência JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estrutura de dados]</td> 
   <td> <p>Selecione a estrutura de dados que deseja usar para criar JSON. Para obter mais informações, consulte <a href="#data-structure" class="MCXref xref">Estrutura de dados</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL cadeia de caracteres JSON] </td> 
   <td> <p>Insira ou mapeie o JSON que deseja analisar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Transformar JSON]

Esse módulo de ação transforma um objeto em uma sequência de caracteres json.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Recuo</td> 
   <td> <p>Selecione o recuo que deseja usar para este JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objeto]</td> 
   <td> <p>Insira ou mapeie o objeto que deseja transformar em JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Transformação de registros de dados em JSON

>[!BEGINSHADEBOX]

**Exemplo:** o exemplo a seguir mostra como transformar registros de dados de [!DNL Google Sheets] para o formato JSON:

1. Coloque o módulo [!DNL Google Sheets] > [!UICONTROL Selecionar linhas] no cenário para buscar os dados. Configure o módulo para recuperar linhas da planilha [!DNL Google]. Defina o&#x200B;**[!UICONTROL Número máximo de linhas retornadas]** para um número pequeno, porém maior que um para fins de teste (Exemplo, três). Execute o módulo [!DNL Google Sheets] clicando com o botão direito do mouse nele e escolhendo &quot;**[!UICONTROL Executar este módulo somente]**.&quot; Verifique a saída do módulo.

1. Conecte o módulo [!UICONTROL Agregador de Matriz] após o módulo [!DNL Google Sheets]. Na configuração do módulo, escolha o módulo [!DNL Google Sheets] no campo **[!UICONTROL nó do Source]**. Deixe os outros campos como estão para o momento.

1. Conecte o [!UICONTROL JSON] > [!UICONTROL Criar módulo JSON] após o módulo [!UICONTROL Agregador de Matriz]. A configuração do módulo requer uma estrutura de dados que descreva o formato JSON. Clique em **[!UICONTROL Adicionar]** para abrir a configuração da estrutura de dados. A maneira mais fácil de criar essa estrutura de dados é gerá-la automaticamente a partir de uma amostra JSON. Clique em **[!UICONTROL Gerador]** e cole sua amostra JSON no campo **[!UICONTROL Dados de amostra]**:

   **Exemplo:**

   ```
   {
   "books": [
   {
   "id": "ID",
   "title": "Title",
   "author": "Author"
   }
   ]
   }
   ```

1. Clique em **[!UICONTROL Salvar]**. O campo [!UICONTROL Especificação] na estrutura de dados agora contém a estrutura gerada.
1. Altere o nome da estrutura de dados para algo mais específico e clique em **[!UICONTROL Salvar]**. Um campo correspondente ao atributo de matriz raiz aparece como um campo mapeável na configuração do módulo JSON.

1. Clique no botão **[!UICONTROL Mapear]** ao lado do campo e mapeie o item `Array[]` da saída do agregador de matriz para ele.

1. Clique em **[!UICONTROL OK]** para fechar a configuração do módulo [!UICONTROL JSON].

1. Abra a configuração do módulo [!UICONTROL Agregador de Matrizes]. Altere a **[!UICONTROL Estrutura de destino]** de [!UICONTROL Personalizada] para o campo do módulo [!UICONTROL JSON] correspondente ao atributo de matriz raiz. Mapeie itens do módulo [!DNL Google Sheets] para os campos apropriados.

1. Clique em **[!UICONTROL OK]** para fechar a configuração do módulo [!UICONTROL Agregador de Matriz].

1. Execute o cenário.

   O módulo [!UICONTROL JSON] gera o formato JSON correto.

1. Abra a configuração do módulo [!DNL Google Sheets] e aumente o número [!UICONTROL Máximo de linhas retornadas] para um número maior que o número de linhas em sua planilha para processar todos os dados.

>[!ENDSHADEBOX]

## Solução de problemas

### Não é possível mapear dados do módulo [!UICONTROL Parse JSON]

Verifique se o conteúdo JSON está mapeado corretamente no módulo [!UICONTROL Analisar JSON] e se a estrutura de dados está definida corretamente. Para obter mais informações, consulte [Transformando registros de dados em JSON](#transforming-data-records-to-json) neste artigo.

### O módulo falha ao usar declarações condicionais em JSON

Ao usar instruções condicionais como `if` em seu JSON, coloque as aspas fora da instrução condicional.

>[!BEGINSHADEBOX]

**Exemplo:**

![Cotas em JSON](/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png)

>[!ENDSHADEBOX]
