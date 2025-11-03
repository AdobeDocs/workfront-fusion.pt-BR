---
title: Módulos do Excel para Microsoft Office 365
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o Microsoft 365 Excel, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 059bc82b-f1bc-4b92-a44b-51c1daf14f08
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2699'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Excel] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Microsoft 365 Excel], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (herdado): automação e integração do Workfront Fusion for Work </p>
   </td> 
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

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar o [!DNL Microsoft office 365 Excel], você deve ter uma conta da Microsoft.

## Informações da API do Excel do Microsoft Office 365

O conector do Microsoft Office 365 Excel usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2.0.16</td> 
  </tr>
 </tbody> 
 </table>



## Conectando o serviço [!DNL Office 365 Excel] ao Workfront Fusion

Para obter instruções sobre como conectar sua conta do [!DNL Office 365 Excel] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alguns aplicativos do Microsoft usam a mesma conexão, que está vinculada a permissões de usuário individuais. Portanto, ao criar uma conexão, a tela de consentimento de permissões exibe todas as permissões que foram concedidas anteriormente à conexão deste usuário, além de todas as novas permissões necessárias para o aplicativo atual.
>
>Por exemplo, se um usuário tiver permissões de &quot;Tabela de leitura&quot; concedidas por meio do conector do Excel e criar uma conexão no conector do Outlook para ler emails, a tela de consentimento de permissões mostrará a permissão &quot;Tabela de leitura&quot; já concedida e a permissão &quot;Gravar email&quot; recém-necessária.

## [!DNL Microsoft Office 365 Excel] módulos e seus campos

Ao configurar módulos do [!DNL Microsoft 365 Excel], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Microsoft 365 Excel] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Pasta de trabalho](#workbook)
* [Planilha](#worksheet)
* [Tabela](#table)
* [Outras](#other)

### Pasta de trabalho

* [Baixar uma Pasta de Trabalho](#download-a-workbook)
* [Pesquisar pastas de trabalho](#search-workbooks)
* [Assistir Pastas de Trabalho](#watch-workbooks)

#### [!UICONTROL Baixar uma Pasta de Trabalho]

Este módulo de ação baixa o conteúdo da pasta de trabalho do Excel especificada.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Baixar uma pasta de trabalho]</td> 
   <td> <p>Selecione como deseja identificar a pasta de trabalho para o módulo a ser baixado.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserindo uma ID manualmente]</strong> </p> <p>No campo [!UICONTROL Workbook ID], insira ou mapeie a ID da pasta de trabalho específica que você deseja que o módulo baixe.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionando no caminho]</strong> </p> <p>No campo [!UICONTROL Workbook], selecione a pasta de trabalho para baixar o módulo, incluindo seu caminho se ele não estiver na pasta raiz.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pastas de Trabalho de Pesquisa]

Este módulo de ação pesquisa por [!DNL Excel] pastas de trabalho.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td> <p>Selecione a pasta na qual deseja pesquisar pastas de trabalho.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filtro]</p> </td> 
   <td> <p>É possível definir um filtro para pesquisar apenas pastas de trabalho que atendam aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que deseja que o filtro avalie, o operador e o valor que deseja que o filtro permita. É possível usar mais de um filtro adicionando regras AND ou OR.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de planilhas que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Assistir Pastas de Trabalho]

Esse módulo de acionador inicia um cenário quando uma pasta de trabalho é criada.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td> <p>Selecione a pasta que deseja observar para novas pastas de trabalho.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filtro]</p> </td> 
   <td> <p>É possível definir um filtro para observar somente as pastas de trabalho que atendem aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que deseja que o filtro avalie, o operador e o valor que deseja que o filtro permita. É possível usar mais de um filtro adicionando regras AND ou OR.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de pastas de trabalho que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Planilha

* [[!UICONTROL Adicionar uma planilha]](#add-a-worksheet)
* [[!UICONTROL Adicionar uma Linha da Planilha]](#add-a-worksheet-row)
* [[!UICONTROL Excluir uma Linha da Planilha]](#delete-a-worksheet-row)
* [[!UICONTROL Listar Linhas da Planilha]](#list-worksheet-rows)
* [[!UICONTROL Listar Planilhas]](#list-worksheets)
* [[!UICONTROL Atualizar uma Linha da Planilha]](#update-a-worksheet-row)
* [[!UICONTROL Observar Linhas da Planilha]](#watch-worksheet-rows)

#### [!UICONTROL Adicionar uma planilha]

Esse módulo de ação cria uma nova planilha na pasta de trabalho selecionada.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho à qual deseja adicionar uma planilha, incluindo o caminho se a pasta de trabalho não estiver no diretório raiz.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Nome] </td>
   <td> <p>Insira ou mapeie um nome para a nova planilha.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Adicionar uma Linha da Planilha]

Este módulo de ação adiciona uma nova linha à planilha selecionada.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém a planilha à qual deseja adicionar uma linha, incluindo o caminho se a pasta de trabalho não estiver no diretório raiz.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Planilha] </td>
   <td> <p>Selecione a planilha à qual deseja adicionar uma linha.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo de valores que estão sendo inseridos]</p> </td> 
   <td> <p>Selecione o tipo de valor a ser inserido na planilha. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL fórmulas]</strong> </p> <p> O Excel tenta avaliar a expressão especificada. Os nomes das funções em uma fórmula estão em inglês. Exemplo: <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Fórmulas locais]</strong> </p> <p>O Excel tenta avaliar a expressão especificada. Os nomes das funções estão no idioma do aplicativo do Excel. Exemplo: <code>=SUM(A1, 1.5)</code> vs <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL Valor]</strong> </p> <p>O Excel não avalia o valor. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Linha]</td>
    <td>Para cada coluna, insira o valor que deseja que a coluna tenha na nova linha.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma Linha da Planilha]

Este módulo de ação exclui uma linha de uma planilha.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém a planilha que inclui a linha que você deseja excluir.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Planilha]</td>
   <td> <p> Selecione a planilha que contém a linha que deseja deletar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL ID de Linha]</td>
   <td>Informe ou mapeie a ID da linha que deseja deletar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar Linhas da Planilha]

Este módulo de ação recupera uma lista de linhas na planilha especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém a planilha que inclui as linhas que você deseja listar, incluindo o caminho se a pasta de trabalho não estiver no diretório raiz.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Planilha] </td>
   <td> <p>Selecione a planilha que contém as linhas que deseja listar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limite]</td>
   <td> <p>Insira ou mapeie o número máximo de linhas da planilha que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar Planilhas]

Este módulo de ação recupera uma lista de planilhas na pasta de trabalho especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém as planilhas que você deseja que o módulo liste.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limite]</td>
   <td> <p>Insira ou mapeie o número máximo de planilhas que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar uma Linha da Planilha]

Este módulo de ação atualiza uma linha de planilha existente.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém a planilha que inclui a linha que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Planilha] </td>
   <td> <p>Selecione a planilha que contém a linha que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo de valores que estão sendo inseridos]</p> </td> 
   <td> <p>Selecione o tipo de valor a ser inserido na planilha. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL fórmulas]</strong> </p> <p> O Excel tenta avaliar a expressão especificada. Os nomes das funções em uma fórmula estão em inglês. Exemplo: <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Fórmulas locais]</strong> </p> <p>O Excel tenta avaliar a expressão especificada. Os nomes das funções estão no idioma do aplicativo do Excel. Exemplo: <code>=SUM(A1, 1.5)</code> vs <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL Valor]</strong> </p> <p>O Excel não avalia o valor. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Linha]</td> 
   <td>Selecione o número da linha a ser atualizada.</td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Linha]</td>
    <td>Para cada coluna, insira o valor que deseja que a coluna tenha na nova linha.</td>
    </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar Linhas da Planilha]

Esse módulo de acionamento inicia um cenário quando uma nova linha é adicionada à planilha.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém a planilha que você deseja observar para novas linhas.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Planilha] </td>
   <td> <p>Selecione a planilha do Excel que deseja observar para novas linhas.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Ignorar Linhas Vazias] </td>
   <td> <p>Habilite esta opção para não retornar pacotes para linhas vazias na planilha.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limite]</td>
   <td> <p>Insira ou mapeie o número máximo de linhas da planilha que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Tabela

* [[!UICONTROL Adicionar uma tabela]](#add-a-table)
* [[!UICONTROL Adicionar uma linha de tabela]](#add-a-table-row)
* [[!UICONTROL Excluir uma tabela]](#delete-a-table)
* [[!UICONTROL Obter uma Tabela]](#get-a-table)
* [[!UICONTROL Listar linhas da tabela]](#list-table-rows)
* [[!UICONTROL Listar tabelas]](#list-tables)
* [[!UICONTROL Atualizar uma tabela]](#update-a-table)
* [[!UICONTROL Observar linhas da tabela]](#watch-table-rows)

#### [!UICONTROL Adicionar uma tabela]

Esse módulo de ação cria um elemento de tabela na planilha do Excel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta de Trabalho] </td> 
   <td> <p>Selecione a pasta de trabalho que contém a planilha à qual deseja adicionar uma tabela.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha à qual deseja adicionar uma tabela.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tem cabeçalhos]</td> 
   <td> <p>Ative essa opção para definir a primeira linha como cabeçalhos da tabela.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Endereço]</p> </td> 
   <td> <p>Defina o tamanho da tabela indicando as células superior esquerda e inferior direita. Exemplo: <code>A1:C10</code> cria uma tabela com 3 colunas e 10 linhas.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Adicionar uma linha de tabela]

Este módulo de ação modifica uma tabela existente.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém a tabela à qual deseja adicionar uma linha.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Planilha] </td>
   <td> <p>Selecione a planilha que contém a tabela à qual deseja adicionar uma linha.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Tabela]</td>
   <td>Selecione a tabela à qual deseja adicionar uma linha.</td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Linha]</td>
    <td>Para cada coluna, insira o valor que deseja que a coluna tenha na nova linha.</td>
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Linha]</p> </td> 
   <td> <p>Para adicionar uma linha em um local específico na tabela, insira ou mapeie um número de linha. O módulo insere a nova linha após essa linha.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma tabela]

Este módulo de ação exclui a tabela especificada de uma planilha [!DNL Excel].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Excluir uma tabela]</td> 
   <td> <p>Selecione como você deseja identificar a tabela que deseja deletar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a ID da pasta de trabalho que contém a tabela que você deseja excluir e, em seguida, insira ou mapeie a ID da planilha que contém a tabela.</p> <p>No campo [!UICONTROL Nome da Tabela], digite ou mapeie o nome da tabela que deseja excluir.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione a pasta de trabalho e a planilha que contêm a tabela que você deseja excluir e selecione a tabela.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma Tabela]

Este módulo de ação recupera metadados para a tabela especificada.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> 
     <p >[!UICONTROL Conexão]</p>
   </td> 
   <td> 
     <p>Para obter instruções sobre como conectar sua conta do Office 365 ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p>
    --&gt; </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Obter uma tabela]</td> 
   <td> <p>Selecione como você deseja identificar a tabela que você deseja recuperar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a ID da pasta de trabalho que contém a tabela que você deseja recuperar e, em seguida, insira ou mapeie a ID da planilha que contém a tabela.</p> <p>No campo [!UICONTROL Nome da Tabela], digite ou mapeie o nome da tabela que deseja recuperar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione a pasta de trabalho e a planilha que contêm a tabela que você deseja recuperar e selecione a tabela.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar linhas da tabela]

Este módulo de pesquisa recupera uma lista de todas as linhas de tabela em uma pasta de trabalho.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém a tabela que inclui as linhas que você deseja listar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Planilha] </td>
   <td> <p>Selecione a planilha que contém a tabela que inclui as linhas que você deseja listar</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Tabela] </td>
   <td> <p>Selecione a tabela que contém as linhas que você deseja listar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limite]</td>
   <td> <p>Insira ou mapeie o número máximo de linhas de tabela que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar tabelas]

Este módulo de pesquisa recupera uma lista de todos os objetos de tabela.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Pasta de Trabalho] </td>
   <td> <p>Selecione a pasta de trabalho que contém as tabelas que você deseja listar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Planilha] </td>
   <td> <p>Selecione a planilha que contém as tabelas que deseja listar</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limite]</td>
   <td> <p>Insira ou mapeie o número máximo de tabelas que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar uma tabela]

Este módulo de ação atualiza uma tabela existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Atualizar uma tabela]</td> 
   <td> <p>Selecione como você deseja identificar a tabela que deseja atualizar.</p> 
    <ul> 
     <li> <p><strong>Inserir manualmente</strong> </p> <p>No campo [!UICONTROL ID da Pasta de Trabalho], insira ou mapeie a ID da pasta de trabalho que contém a tabela que você deseja atualizar.</p> <p>No campo [!UICONTROL Nome da Tabela], digite ou mapeie o nome da tabela que deseja atualizar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione a pasta de trabalho e a planilha que contêm a tabela que você deseja atualizar e selecione a tabela.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td> <p>Se quiser renomear a tabela, insira ou mapeie um novo nome para ela.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostrar Cabeçalhos]</td> 
   <td> <p>Ative esta opção para mostrar os cabeçalhos da tabela atualizada.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostrar totais]</td> 
   <td>Ative esta opção para mostrar os valores totais da tabela.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estilo]</td> 
   <td>Escolha um estilo para a nova tabela.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar linhas da tabela]

Esse acionador inicia um cenário quando uma nova linha é adicionada a uma tabela.

>[!NOTE]
>
>A tabela aqui se refere ao elemento de tabela incorporado na Pasta de trabalho. Não a tabela inteira (pasta/planilha).

![Tabela inserida](/help/workfront-fusion/references/apps-and-modules/assets/embedded-table-350x420.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Pasta de Trabalho]</p> </td> 
   <td> <p>Selecione a pasta de trabalho que contém a tabela que você deseja observar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Planilha] </td>
   <td> <p> Selecione a planilha que contém a tabela que você deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tabela]</p> </td> 
   <td> <p>Selecione a tabela que deseja observar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limite]</td>
   <td> <p>Insira ou mapeie o número máximo de linhas que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outras

* [[!UICONTROL Fazer uma chamada de API]](#make-an-api-call)
* [[!UICONTROL Recuperar dados]](#retrieve-data)

#### [!UICONTROL Fazer uma chamada de API]

Esse módulo de ação permite fazer uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://graph.microsoft.com</code>. Exemplo:<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:   <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Recuperar dados]

Esta ação recupera dados do intervalo de planilhas definido e retorna um conjunto para cada linha.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta de Trabalho] </td> 
   <td> <p>Selecione a pasta de trabalho que contém os dados que você deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha que contém os dados que você deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intervalo] </td> 
   <td> <p>Especifique a área da planilha da qual deseja recuperar dados indicando as células superior esquerda e inferior direita. Exemplo: <code>A1:D10</code></p> </td> 
  </tr> 
 </tbody> 
</table>
