---
title: Módulos do Google Forms
description: Os  [!DNL Adobe Workfront Fusion Google Forms] módulos permitem monitorar, selecionar, adicionar, atualizar ou excluir respostas no Google Forms.
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 0%

---

# [!DNL Google Forms] módulos

Os módulos do [!DNL Adobe Workfront Fusion] [!DNL Google Forms] permitem monitorar, selecionar, adicionar, atualizar ou excluir respostas no [!DNL Google Forms].

Para usar [!DNL Google Docs] com [!DNL Adobe Workfront Fusion], é necessário ter uma conta [!DNL Google]. Se você ainda não tiver uma conta [!DNL Google], crie uma na página de ajuda da Conta [!DNL Google].

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho] </p>
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

## Pré-requisitos

Para usar módulos [!DNL Google Forms], você deve ter uma conta [!DNL Google].

## Informações da API do Google Forms

O conector do Google Forms usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Criação de uma planilha a partir do formulário

Para trabalhar com as respostas do formulário, a planilha de suas respostas deve ser criada.

1. Abra o formulário.
1. Vá para a guia **[!UICONTROL Responses]**.
1. Clique no ícone **[!UICONTROL Create Spreadsheet]** ![Ícone de Planilha](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png).

1. Selecione se deseja criar uma nova planilha ou uma planilha existente
1. Clique em **[!UICONTROL Create]**.

## [!DNL Google Forms] módulos e seus campos

Ao configurar módulos do [!DNL Google Forms], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Google Forms] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

#### [!UICONTROL Watch Responses]

Verifica se há novas respostas no formulário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selecione a planilha que contém as respostas do formulário a ser observado para novas respostas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers]</td> 
   <td>Especifique a linha de cabeçalho da tabela. Linha padrão <code>A1:Z1</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Especifique como deseja que os valores sejam renderizados na saída.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong> </p> <p>Os valores são calculados e formatados na resposta de acordo com a formatação da célula. A formatação se baseia no local da planilha, não no local do usuário solicitante. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>$1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Os valores são calculados, mas não formatados na resposta. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará o número <code>1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>Os valores não são calculados. A resposta inclui as fórmulas. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date and time render option]</td> 
   <td>Selecione como deseja que datas, horas e duração sejam representadas na saída. Este campo será ignorado se [!UICONTROL Value Render Option] estiver definido como [!UICONTROL Formatted Value].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p> Defina o número máximo de respostas com as quais [!DNL Workfront Fusion] funciona durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Add a Response]](#add-a-response)
* [[!UICONTROL Update a Response]](#update-a-response)
* [[!UICONTROL Delete a Response]](#delete-a-response)

#### [!UICONTROL Add a Response]

Este módulo anexa uma nova resposta à parte inferior da planilha do formulário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selecione a planilha que contém a planilha à qual deseja adicionar uma resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Insira os valores desejados nas colunas da planilha.</p> <p>Para a coluna [!UICONTROL Timestamp] no formato correto, use o seguinte valor:</p><pre>formatDate(agora;DD/MM/AAAA HH:mm;UTC)</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Os valores inseridos pelo usuário não são analisados e são armazenados como estão. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>Os valores são analisados como se o usuário os tivesse digitado na interface. Os números permanecem números, mas as cadeias de caracteres podem ser convertidas em números, datas ou outros formatos seguindo as mesmas regras aplicadas ao inserir texto em uma célula por meio da interface do usuário do [!DNL Google Sheets].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Insert data option]</td> 
   <td> <p>Especifique como os dados existentes serão alterados quando novos dados forem inseridos. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>Os novos dados substituem os dados existentes nas áreas em que são gravados. A adição de dados ao final da planilha insere novas linhas ou colunas para que os dados possam ser gravados.</p> </li> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>São inseridas linhas para os novos dados.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Response]

Este módulo atualiza a resposta selecionada.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selecione a planilha que contém a planilha na qual você deseja atualizar uma resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Informe ou mapeie o número da linha que deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Insira os novos valores nas colunas desejadas.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Os valores inseridos pelo usuário não são analisados e são armazenados como estão. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>Os valores são analisados como se o usuário os tivesse digitado na interface. Os números permanecem números, mas as cadeias de caracteres podem ser convertidas em números, datas ou outros formatos seguindo as mesmas regras aplicadas ao inserir texto em uma célula por meio da interface do usuário do [!DNL Google Sheets].</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Response]

Este módulo exclui uma resposta selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selecione a planilha que contém a planilha da qual deseja excluir uma resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Informe ou mapeie o número da linha que deseja deletar.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Search Responses]](#search-responses)
* [[!UICONTROL Search Responses (Advanced])](#search-responses-advanced)

#### [!UICONTROL Search Responses]

Este módulo retorna respostas que correspondem aos critérios fornecidos.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>Conexão</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Selecione o formulário que deseja pesquisar.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Sheet] </td>
   <td> <p>Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Column range]</td>
   <td> <p> Selecione o intervalo de colunas que deseja pesquisar.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Defina o filtro pelo qual deseja pesquisar respostas de respostas.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Sort Order] </td>
   <td> <p>Selecione se as respostas retornadas devem ser classificadas em ordem crescente ou decrescente.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Order By]</td>
   <td> <p> Selecione a coluna pela qual deseja ordenar as respostas retornadas.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Especifique como deseja que os valores sejam renderizados na saída.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong></p> <p>Os valores são calculados e formatados na resposta de acordo com a formatação da célula. A formatação se baseia no local da planilha, não no local do usuário solicitante. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>$1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Os valores são calculados, mas não formatados na resposta. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará o número <code>1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>Os valores não são calculados. A resposta inclui as fórmulas. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Date and time render option]</td>
    <td>Selecione como deseja que datas, horas e duração sejam representadas na saída. Este campo será ignorado se a Opção [!UICONTROL Value Render] estiver definida como Valor Formatado. </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Maximum number of returned responses]</td>
   <td> <p> Defina o número máximo de respostas que [!DNL Workfront Fusion] retorna durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Responses (Advanced)]

Este módulo executa uma pesquisa usando o [[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage). Este módulo não retorna um número de linha.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Selecione a planilha que contém a planilha que você deseja pesquisar.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Sheet]</td>
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Defina a consulta de pesquisa usando o <a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a>.</p> <p>Exemplo: <code>select * where C = "John"</code> recupera todos os valores da linha em que a coluna C é "John".</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Maximum number of returned rows]</td>
   <td> <p> Defina o número máximo de respostas que [!DNL Workfront Fusion] retorna durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>
