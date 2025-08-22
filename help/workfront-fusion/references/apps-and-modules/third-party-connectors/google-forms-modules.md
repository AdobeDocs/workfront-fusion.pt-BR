---
title: Módulos do Google Forms
description: Os  [!DNL Adobe Workfront Fusion Google Forms] módulos permitem monitorar, selecionar, adicionar, atualizar ou excluir respostas no Google Forms.
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1415'
ht-degree: 0%

---

# [!DNL Google Forms] módulos

Os módulos do Adobe Workfront Fusion [!DNL Google Forms] permitem monitorar, selecionar, adicionar, atualizar ou excluir respostas no [!DNL Google Forms].

Para usar o [!DNL Google Docs] com o Adobe Workfront Fusion, é necessário ter uma conta [!DNL Google]. Se você ainda não tiver uma conta [!DNL Google], crie uma na página de ajuda da Conta [!DNL Google].

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion</p>
   <p>Ou</p>
   <p>Herdados: Automação e integração do Workfront Fusion for Work </p>
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

Para trabalhar com as respostas do formulário, primeiro crie a planilha de respostas.

1. Abra o formulário.
1. Vá para a guia **[!UICONTROL Respostas]**.
1. Clique no ícone **[!UICONTROL Criar planilha]** ![Ícone de planilha](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png).

1. Selecione se deseja criar uma nova planilha ou uma planilha existente
1. Clique em **[!UICONTROL Criar]**.

## [!DNL Google Forms] módulos e seus campos

Ao configurar módulos do [!DNL Google Forms], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Google Forms] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

#### [!UICONTROL Assistir Respostas]

Verifica se há novas respostas no formulário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha]</td> 
   <td> <p>Selecione a planilha que contém as respostas do formulário a ser observado para novas respostas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha]</td> 
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Linha com cabeçalhos]</td> 
   <td>Especifique a linha de cabeçalho da tabela. Linha padrão <code>A1:Z1</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Opção de Renderização de Valor]</td> 
   <td> <p>Especifique como deseja que os valores sejam renderizados na saída.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Valor formatado]</strong> </p> <p>Os valores são calculados e formatados na resposta de acordo com a formatação da célula. A formatação se baseia no local da planilha, não no local do usuário solicitante. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>$1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Valor não formatado]</strong> </p> <p>Os valores são calculados, mas não formatados na resposta. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará o número <code>1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Fórmula]</strong> </p> <p>Os valores não são calculados. A resposta inclui as fórmulas. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Opção de renderização de data e hora]</td> 
   <td>Selecione como deseja que datas, horas e duração sejam representadas na saída. Este campo será ignorado se a [!UICONTROL Opção de Renderização de Valor] estiver definida como [!UICONTROL Valor Formatado].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p> Defina o número máximo de respostas com as quais o Workfront Fusion funciona durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Adicionar uma resposta]](#add-a-response)
* [[!UICONTROL Excluir uma resposta]](#delete-a-response)
* [[!UICONTROL Atualizar uma resposta]](#update-a-response)

#### [!UICONTROL Adicionar uma resposta]

Este módulo anexa uma nova resposta à parte inferior da planilha do formulário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha]</td> 
   <td> <p>Selecione a planilha que contém a planilha à qual deseja adicionar uma resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha]</td> 
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Valores]</p> </td> 
   <td> <p>Insira os valores desejados nas colunas da planilha. As colunas estão disponíveis com base na planilha.</p> <p>Na coluna [!UICONTROL Carimbo de data/hora], use o seguinte valor:</p><pre>formatDate(agora;DD/MM/AAAA HH:mm;UTC)</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Opção de entrada de valor]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Os valores inseridos pelo usuário não são analisados e são armazenados como estão. </p> </li> 
     <li> <p><strong>[!UICONTROL Usuário inserido]</strong></p> <p>Os valores são analisados como se o usuário os tivesse digitado na interface. Os números permanecem números, mas as cadeias de caracteres podem ser convertidas em números, datas ou outros formatos seguindo as mesmas regras aplicadas ao inserir texto em uma célula por meio da interface do usuário do [!DNL Google Sheets].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Inserir opção de dados]</td> 
   <td> <p>Especifique como os dados existentes serão alterados quando novos dados forem inseridos. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Substituir]</strong> </p> <p>Os novos dados substituem os dados existentes nas áreas em que são gravados. A adição de dados ao final da planilha insere novas linhas ou colunas para que os dados possam ser gravados.</p> </li> 
     <li> <p><strong>[!UICONTROL Inserir linhas]</strong></p> <p>São inseridas linhas para os novos dados.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma resposta]

Este módulo exclui uma resposta selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha]</td> 
   <td> <p>Selecione a planilha que contém a planilha da qual deseja excluir uma resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha]</td> 
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Número de linha]</p> </td> 
   <td> <p>Informe ou mapeie o número da linha que deseja deletar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar uma resposta]

Este módulo atualiza a resposta selecionada.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha]</td> 
   <td> <p>Selecione a planilha que contém a planilha na qual você deseja atualizar uma resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha]</td> 
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Número de linha]</p> </td> 
   <td> <p>Informe ou mapeie o número da linha que deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Valores]</p> </td> 
   <td> <p>Insira os novos valores para as colunas desejadas. As colunas estão disponíveis com base na planilha.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Opção de entrada de valor]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Os valores inseridos pelo usuário não são analisados e são armazenados como estão. </p> </li> 
     <li> <p><strong>[!UICONTROL Usuário inserido]</strong></p> <p>Os valores são analisados como se o usuário os tivesse digitado na interface. Os números permanecem números, mas as cadeias de caracteres podem ser convertidas em números, datas ou outros formatos seguindo as mesmas regras aplicadas ao inserir texto em uma célula por meio da interface do usuário do [!DNL Google Sheets].</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Pesquisar Respostas]](#search-responses)
* [[!UICONTROL Pesquisar Respostas (Avançado])](#search-responses-advanced)

#### [!UICONTROL Pesquisar Respostas]

Este módulo retorna respostas que correspondem aos critérios fornecidos.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>Conexão</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Planilha]</td>
   <td> <p>Selecione o formulário que deseja pesquisar.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Planilha] </td>
   <td> <p>Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Intervalo de colunas]</td>
   <td> <p> Selecione o intervalo de colunas que deseja pesquisar.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Defina o filtro pelo qual deseja pesquisar respostas de respostas.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Ordem de Classificação] </td>
   <td> <p>Selecione se as respostas retornadas devem ser classificadas em ordem crescente ou decrescente.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Ordenar por]</td>
   <td> <p> Selecione a coluna pela qual deseja ordenar as respostas retornadas.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Opção de Renderização de Valor]</td> 
   <td> <p>Especifique como deseja que os valores sejam renderizados na saída.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Valor formatado]</strong></p> <p>Os valores são calculados e formatados na resposta de acordo com a formatação da célula. A formatação se baseia no local da planilha, não no local do usuário solicitante. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>$1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Valor não formatado]</strong> </p> <p>Os valores são calculados, mas não formatados na resposta. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará o número <code>1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Fórmula]</strong> </p> <p>Os valores não são calculados. A resposta inclui as fórmulas. Por exemplo, se <code>A1</code> for <code>1. 23</code> e <code>A2 </code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Opção de renderização de data e hora]</td>
    <td>Selecione como deseja que datas, horas e duração sejam representadas na saída. Este campo será ignorado se a Opção [!UICONTROL Value Render] estiver definida como Valor Formatado. </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Número máximo de respostas retornadas]</td>
   <td> <p> Defina o número máximo de respostas que o Workfront Fusion retorna durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Respostas de Pesquisa (Avançadas)]

Este módulo executa uma pesquisa usando o [[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage). Este módulo não retorna um número de linha.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Planilha]</td>
   <td> <p>Selecione a planilha que contém a planilha que você deseja pesquisar.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Planilha]</td>
   <td> <p> Selecione a planilha que contém as respostas do formulário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Consulta]</td> 
   <td> <p>Defina a consulta de pesquisa usando o <a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a>.</p> <p>Exemplo: <code>select * where C = "John"</code> recupera todos os valores da linha em que a coluna C é "John".</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Número máximo de linhas retornadas]</td>
   <td> <p> Defina o número máximo de respostas que o Workfront Fusion retorna durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>
