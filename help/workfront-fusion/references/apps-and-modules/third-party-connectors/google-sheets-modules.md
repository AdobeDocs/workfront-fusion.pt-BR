---
title: Módulos do Google Sheets
description: Para usar [!DNL Google Sheets] com [!DNL Adobe Workfront Fusion],you need the [!UICONTROL Workfront Fusion Google Sheets] extensão (opcional, mas necessário para acionadores instantâneos).
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 80965570-2937-4ac8-97c0-54f7a813ec50
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '3957'
ht-degree: 0%

---

# [!DNL Google Sheets] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Google Sheets], bem como conectá-los a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte [Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

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

## Pré-requisitos

Para usar os módulos do [!UICONTROL Google Sheets], você deve ter uma conta do [!UICONTROL Google].

## Informações da API do Google Sheets

O conector do Google Sheets usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://sheets.googleapis.com/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2.5.7</td> 
  </tr>
 </tbody> 
 </table>

## Módulos do Google Sheets e seus campos

Ao configurar módulos do [!DNL Google Forms], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Google Sheets] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Acionadores

#### [!UICONTROL Linhas de observação]

Recupera valores de linhas recém-adicionadas na planilha.

O módulo recupera somente novas linhas que não foram preenchidas anteriormente. O acionador não processa uma linha substituída.

>[!IMPORTANT]
>
>Se a planilha contiver uma linha em branco, nenhuma linha após a linha em branco será processada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha que contém a planilha que você deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha que deseja observar para uma nova linha.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tabela contém cabeçalhos]</td> 
   <td> <p> Selecione se a planilha contém uma linha de cabeçalho.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Sim]</strong> </p> <p>O módulo não recupera a linha de cabeçalho como dados de saída. </p> <p>Os nomes das variáveis na saída são chamados pelos cabeçalhos.</p> </li> 
     <li> <p><strong>[!UICONTROL Não]</strong> </p> <p>O módulo também recupera a primeira linha da tabela</p> <p>Os nomes das variáveis na saída são chamados de A, B, C, D e assim por diante.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Linha com cabeçalhos] </td> 
   <td> <p>Informe a faixa da linha de cabeçalho. Por exemplo, <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Primeira linha de tabela]</td> 
   <td> <p>Insira o intervalo da primeira linha da tabela. Por exemplo, <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Opção de renderização de valor]</p> </td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Valor formatado]</p> <p>Os valores são calculados e formatados na resposta de acordo com a formatação da célula. A formatação se baseia no local da planilha, não no local do usuário solicitante. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>"$1.23"</code>.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Valor não formatado]</p> <p>Os valores são calculados, mas não formatados na resposta. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará o número <code>"1.23"</code>.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Fórmula]</p> <p>Os valores não são calculados. A resposta inclui as fórmulas. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>"=A1"</code>.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Opção de renderização de data e hora]</p> </td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Número de série]</p> <p>Os campos de data, hora, data e hora e duração são exibidos como duplos no formato "número de série", conforme popularizado pelo Lotus 1-2-3. A parte do número inteiro do valor (à esquerda do decimal) conta os dias desde 30 de dezembro de 1899. A parte fracional (à direita do decimal) conta o tempo como uma fração do dia. Por exemplo, 1º de janeiro de 1900 ao meio-dia seria 2,5, 2 porque é 2 dias depois de 30 de dezembro de 1899, e 0,5 porque o meio-dia é meio dia. 1 de fevereiro de 1900 às 15h seria 33.625. Isso considera corretamente o ano de 1900 como não um ano bissexto.</p> </li><li><p style="font-weight: bold;">[!UICONTROL Cadeia de caracteres formatada]</p> <p>Os campos de data, hora, data e hora e duração são gerados como strings em seu formato de número (que depende do local da planilha).</p></li><ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Defina o número máximo de resultados com os quais [!DNL Workfront Fusion] trabalhará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Adicionar uma linha]](#add-a-row)
* [[!UICONTROL Adicionar uma Planilha]](#add-a-sheet)
* [[!UICONTROL Limpar uma Célula]](#clear-a-cell)
* [[!UICONTROL Limpar uma Linha]](#clear-a-row)
* [[!UICONTROL Criar uma Planilha]](#create-a-spreadsheet)
* [[!UICONTROL Excluir uma Linha]](#delete-a-row)
* [[!UICONTROL Excluir uma Planilha]](#delete-a-sheet)
* [[!UICONTROL Obter uma Célula]](#get-a-cell)
* [[!UICONTROL Fazer uma chamada de API]](#make-an-api-call)
* [[!UICONTROL Atualizar uma Célula]](#update-a-cell)
* [[!UICONTROL Atualizar uma linha]](#update-a-row)

#### [!UICONTROL Adicionar uma linha]

Este módulo anexa adiciona uma linha a uma planilha.

Ao configurar módulos do [!DNL Google Sheets], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Google Sheets] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Modo]</td> 
   <td> <p>Selecione se deseja selecionar a planilha e a planilha manualmente ou por mapeamento.</p> <p>Observação: o mapeamento manual é útil, por exemplo, quando uma nova planilha é criada em um cenário [!DNL Workfront Fusion] e você deseja adicionar dados na planilha recém-criada diretamente no cenário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha à qual deseja adicionar uma linha.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Intervalo de Colunas]</td> 
   <td>Selecione o intervalo de colunas com o qual deseja trabalhar.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tabela contém cabeçalhos]</td> 
   <td> <p> Selecione se a planilha contém a linha de cabeçalho.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Sim]</strong> </p> <p>O módulo não recupera a linha de cabeçalho como dados de saída. </p> <p>Os nomes das variáveis na saída são chamados pelos cabeçalhos.</p> </li> 
     <li> <p><strong>[!UICONTROL Não]</strong> </p> <p>O módulo também recupera a primeira linha da tabela</p> <p>Os nomes das variáveis na saída são chamados de A, B, C, D e assim por diante.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Valores] </td> 
   <td> <p>Insira ou mapeie as células desejadas da linha que deseja adicionar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Opção de entrada de valor]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Usuário inserido]</strong></p> <p>Os valores são analisados como se o usuário os tivesse digitado na interface. Os números permanecem números, mas as cadeias de caracteres podem ser convertidas em números, datas ou outros formatos seguindo as mesmas regras aplicadas ao inserir texto em uma célula por meio da interface do usuário do [!DNL Google Sheets].</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Os valores inseridos pelo usuário não são analisados e são armazenados conforme foram inseridos. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Inserir opção de dados]</td> 
   <td> <p>Especifique como os dados existentes serão alterados quando novos dados forem inseridos. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir linhas]</strong></p> <p>São inseridas linhas para os novos dados.</p> </li> 
     <li> <p><strong>[!UICONTROL Substituir]</strong> </p> <p>Os novos dados substituem os dados existentes nas áreas em que são gravados. A adição de dados ao final da planilha insere novas linhas ou colunas para que os dados possam ser gravados.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Adicionar uma Planilha]

Cria uma nova planilha em uma planilha selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha do Google à qual deseja adicionar uma planilha.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Propriedades]</td> 
   <td> 
    <ul> 
     <li> <p style="font-weight: bold;">[!UICONTROL Título]</p> <p>Digite o nome da nova planilha.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Índice]</p> <p>Insira a posição da planilha. O padrão é 0 (que coloca a planilha no primeiro lugar).</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Limpar uma Célula]

Exclui um valor de uma célula especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha do Google que contém a planilha da qual você deseja limpar uma célula.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha da qual deseja limpar uma célula.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Célula] </td> 
   <td> <p>Insira ou mapeie a ID da célula que deseja limpar. Exemplo: <code>A5</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Limpar uma Linha]

Exclui valores de uma linha especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google] que contém a planilha da qual você deseja limpar uma linha.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p> Selecione a planilha cujos dados você deseja limpar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número de linha]</td> 
   <td> <p>Insira o número da linha da qual deseja limpar dados. Exemplo: <code> 23</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar uma Planilha]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Título] </td> 
   <td> <p>Insira o nome de uma nova planilha.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Localidade]</td> 
   <td> <p>Informe o local da planilha em um dos seguintes formatos:</p> 
    <ul> 
     <li>um código de idioma ISO 639-1, como <code>en</code></li> 
     <li>um código de idioma ISO 639-2, como <code>haw</code>, se não existir um código 639-1</li> 
     <li>uma combinação do código ISO de idioma e do código do país, como <code>en_US</code></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Intervalo de recálculo]</td> 
   <td> <p>O tempo de espera antes que as funções voláteis sejam recalculadas:</p> <ul><li><p style="font-weight: bold;">[!UICONTROL Na alteração]</p> <p>Funções voláteis são atualizadas a cada mudança.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Em alteração e a cada minuto]</p> <p>Funções voláteis são atualizadas a cada mudança e a cada minuto.</p></li> <li><p style="font-weight: bold;">[!UICONTROL Em alteração e a cada hora]</p> <p>As funções voláteis são atualizadas a cada mudança e a cada hora.</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Fuso horário]</td> 
   <td> <p> Selecione o fuso horário da planilha.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Formato de número]</td> 
   <td> <p>Selecione o formato padrão de todas as células da planilha.</p> <p><strong>[!UICONTROL Texto]</strong>: formatação de texto. Exemplo: <code>1000. 12</code></p> <p><strong>[!UICONTROL Number]</strong>: Formatação de número. Exemplo: <code>1,000.12</code></p> <p><strong>[!UICONTROL Percent]</strong>: formatação de porcentagem. Exemplo: <code>10. 12%</code></p> <p><strong>[!UICONTROL Moeda]</strong>: Formatação de moeda. Exemplo: <code>$1,000.12</code></p> <p><strong>[!UICONTROL Data]</strong>: formatação de data. Exemplo: <code>9/26/2008</code></p> <p><strong>[!UICONTROL Time]</strong>: formatação de hora. Exemplo: <code>3:59:00 PM</code></p> <p><strong>[!UICONTROL Data hora]</strong>: formatação de data e hora. Exemplo: <code>9/26/08 15:59:00</code> </p> <p><strong>[!UICONTROL Scientific]</strong>: formatação de número científico. Exemplo: <code>1. 01E+03</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilhas] </td> 
   <td> <p>Para cada planilha que você deseja adicionar à planilha, clique em <strong>[!UICONTROL Adicionar item]</strong> e insira ou mapeie um título para a planilha e o índice da planilha. Um índice de 0 representa a primeira planilha.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma Linha]

Exclui uma linha especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha do Google que contém a planilha da qual deseja excluir uma linha.</p> </td> 
  </tr> 
  <tr> 
   <td>Planilha </td> 
   <td> <p>Selecione a planilha da qual deseja excluir uma linha.</p> </td> 
  </tr> 
  <tr> 
   <td>Número da linha</td> 
   <td> <p>Informe o número da linha que deseja deletar. Exemplo: <code>23</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma Planilha]

Exclui uma planilha específica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma Célula]

Recupera um valor de uma célula selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha que contém a célula da qual deseja recuperar dados.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Célula] </td> 
   <td> <p>Insira a ID da célula da qual deseja recuperar dados. Exemplo: <code>A6</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Opção de renderização de valor]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Valor formatado]</p> <p>Os valores são calculados e formatados na resposta de acordo com a formatação da célula. A formatação se baseia no local da planilha, não no local do usuário solicitante. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>"$1.23"</code>.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Valor não formatado]</p> <p>Os valores são calculados, mas não formatados na resposta. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará o número <code>"1.23"</code>.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Fórmula]</p> <p>Os valores não são calculados. A resposta inclui as fórmulas. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>"=A1"</code>.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!DNL Date and time render option]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!DNL Serial number]</p> <p>Os campos de data, hora, data e hora e duração são exibidos como duplos no formato "número de série", conforme popularizado pelo Lotus 1-2-3. A parte do número inteiro do valor (à esquerda do decimal) conta os dias desde 30 de dezembro de 1899. A parte fracional (à direita do decimal) conta o tempo como uma fração do dia. Por exemplo, 1º de janeiro de 1900 ao meio-dia seria 2,5, 2 porque é 2 dias depois de 30 de dezembro de 1899, e 0,5 porque o meio-dia é meio dia. 1 de fevereiro de 1900 às 15h seria 33.625. Isso considera corretamente o ano de 1900 como não um ano bissexto.</p></li><li> <p style="font-weight: bold;">[!DNL Formatted string]</p> <p>Os campos de data, hora, data e hora e duração são gerados como strings em seu formato de número (que depende do local da planilha).</p> </li><ul></td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fazer uma chamada de API]

Esse módulo de ação permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Google Sheets ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão ao [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td>Insira um caminho relativo para <code>https://sheets.googleapis.com/v4/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Método]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Por exemplo, <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p> Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:   <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar uma Célula]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha na qual deseja atualizar uma célula.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Célula] </td> 
   <td> <p>Insira a ID da célula que deseja atualizar. Exemplo: <code>A5</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Valor]</td> 
   <td> <p>Insira o novo valor para a célula.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Opção de entrada de valor]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Usuário inserido]</strong></p> <p>Os valores são analisados como se o usuário os tivesse digitado na interface. Os números permanecem números, mas as cadeias de caracteres podem ser convertidas em números, datas ou outros formatos seguindo as mesmas regras aplicadas ao inserir texto em uma célula por meio da interface do usuário do [!DNL Google Sheets].</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Os valores inseridos pelo usuário não são analisados e são armazenados conforme foram inseridos. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar uma linha]

Esse módulo permite alterar o conteúdo da célula em uma linha selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Modo]</td> 
   <td> <p>Selecione se deseja selecionar a planilha e a planilha manualmente ou por mapeamento.</p> <p>Observação: o mapeamento manual é útil, por exemplo, quando uma nova planilha é criada no cenário do [!UICONTROL Workfront Fusion] e você deseja adicionar dados à planilha recém-criada diretamente no cenário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha na qual deseja atualizar uma linha.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número de linha]</td> 
   <td> <p> Informe o número da linha que deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tabela contém cabeçalhos]</td> 
   <td> <p> Selecione se a planilha contém a linha de cabeçalho.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Sim]</strong> </p> <p>O módulo não recupera a linha de cabeçalho como dados de saída. </p> <p>Os nomes das variáveis na saída são chamados pelos cabeçalhos.</p> </li> 
     <li> <p><strong>[!UICONTROL Não]</strong> </p> <p>O módulo também recupera a primeira linha da tabela</p> <p>Os nomes das variáveis na saída são chamados de A, B, C, D e assim por diante.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Valores] </td> 
   <td> <p>Insira ou mapeie os valores para as células desejadas da linha que você deseja alterar (atualizar).</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Opção de entrada de valor]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Usuário inserido]</strong></p> <p>Os valores são analisados como se o usuário os tivesse digitado na interface. Os números permanecem números, mas as cadeias de caracteres podem ser convertidas em números, datas ou outros formatos seguindo as mesmas regras aplicadas ao inserir texto em uma célula por meio da interface do usuário do [!DNL Google Sheets].</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Os valores inseridos pelo usuário não são analisados e são armazenados conforme foram inseridos. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Obter Valores de Intervalo]](#get-range-values)
* [[!UICONTROL Listar planilhas]](#list-sheets)
* [[!UICONTROL Pesquisar Linhas]](#search-rows)
* [[!UICONTROL Pesquisar Linhas (Avançado)]](#search-rows-advanced)

#### [!UICONTROL Obter Valores de Intervalo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha da qual deseja obter o conteúdo do intervalo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Intervalo] </td> 
   <td> <p>Insira o intervalo que deseja obter. Exemplo: <code>A1:D25</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tabela contém cabeçalhos]</td> 
   <td> <p>Marque esta caixa se a planilha tiver uma linha de cabeçalho</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Linha com cabeçalhos]</td> 
   <td>Insira o intervalo dos cabeçalhos da tabela. Exemplo <code>A1:F1</code>. Se você deixar o campo vazio, [!DNL Workfront Fusion] tratará a primeira linha do intervalo especificado como o cabeçalho.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Opção de renderização de valor]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Valor formatado]</p> <p>Os valores são calculados e formatados na resposta de acordo com a formatação da célula. A formatação se baseia no local da planilha, não no local do usuário solicitante. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>"$1.23"</code>.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Valor não formatado]</p> <p>Os valores são calculados, mas não formatados na resposta. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará o número <code>"1.23"</code>.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Fórmula]</p> <p>Os valores não são calculados. A resposta inclui as fórmulas. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>"=A1"</code>.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Opção de renderização de data e hora]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Número de série]</p> <p>Os campos de data, hora, data e hora e duração são exibidos como duplos no formato "número de série", conforme popularizado pelo Lotus 1-2-3. A parte do número inteiro do valor (à esquerda do decimal) conta os dias desde 30 de dezembro de 1899. A parte fracional (à direita do decimal) conta o tempo como uma fração do dia. Por exemplo, 1º de janeiro de 1900 ao meio-dia seria 2,5, 2 porque é 2 dias depois de 30 de dezembro de 1899, e 0,5 porque o meio-dia é meio dia. 1 de fevereiro de 1900 às 15h seria 33.625. Isso considera corretamente o ano de 1900 como não um ano bissexto.</p> </li><li><p style="font-weight: bold;">[!UICONTROL Cadeia de caracteres formatada]</p> <p>Os campos de data, hora, data e hora e duração são gerados como strings em seu formato de número (que depende do local da planilha).</p></li><ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar planilhas]

Este módulo retorna uma lista de todas as planilhas em uma planilha.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google] que contém as planilhas que você deseja listar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar Linhas]

Pesquisa linhas usando as opções de filtro.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Google Sheets ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão ao [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha na qual deseja pesquisar as linhas.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tabela contém cabeçalhos]</td> 
   <td> <p> Selecione se a planilha contém a linha de cabeçalho. Se a opção [!UICONTROL Sim] estiver selecionada, o módulo não recuperará a linha de cabeçalho, pois os dados de saída e os nomes de variáveis na saída são chamados pelos cabeçalhos. Se a opção [!UICONTROL Não] estiver selecionada, o módulo também recuperará a primeira linha da tabela e os nomes de variáveis na saída serão chamados apenas de A, B, C, D e assim por diante.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Intervalo de colunas]</td> 
   <td>Selecione o intervalo de colunas com o qual trabalhar. Exemplo: <code>A-F</code></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filtro]</td> 
   <td> <p>Defina o filtro que deseja usar para pesquisar linhas.</p> <!--<p>For more information about filters, see <a href="/help/workfront-fusion/create-scenarios/add-modules/" class="MCXref xref">Add a filter to a scenario in [!UICONTROL Adobe Workfront Fusion]</a>.</p>--> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordem de classificação]</td> 
   <td>Selecione se deseja classificar em ordem crescente ou decrescente.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordenar por]</td> 
   <td>Escolha a coluna pela qual deseja classificar.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Opção de renderização de valor]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Valor formatado]</p> <p>Os valores são calculados e formatados na resposta de acordo com a formatação da célula. A formatação se baseia no local da planilha, não no local do usuário solicitante. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>"$1.23"</code>.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Valor não formatado]</p> <p>Os valores são calculados, mas não formatados na resposta. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará o número <code>"1.23"</code>.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Fórmula]</p> <p>Os valores não são calculados. A resposta inclui as fórmulas. Por exemplo, se <code>A1</code> for <code>1.23</code> e <code>A2</code> for <code>=A1</code> e formatado como moeda, <code>A2</code> retornará <code>"=A1"</code>.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Opção de renderização de data e hora]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Número de série]</p> <p>Os campos de data, hora, data e hora e duração são exibidos como duplos no formato "número de série", conforme popularizado pelo Lotus 1-2-3. A parte do número inteiro do valor (à esquerda do decimal) conta os dias desde 30 de dezembro de 1899. A parte fracional (à direita do decimal) conta o tempo como uma fração do dia. Por exemplo, 1º de janeiro de 1900 ao meio-dia seria 2,5, 2 porque é 2 dias depois de 30 de dezembro de 1899, e 0,5 porque o meio-dia é meio dia. 1 de fevereiro de 1900 às 15h seria 33.625. Isso considera corretamente o ano de 1900 como não um ano bissexto.</p> </li><li><p style="font-weight: bold;">[!UICONTROL Cadeia de caracteres formatada]</p> <p>Os campos de data, hora, data e hora e duração são gerados como strings em seu formato de número (que depende do local da planilha).</p></li><ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de linhas retornadas]</td> 
   <td>Defina o número máximo de linhas que [!DNL Workfront Fusion] retornará durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar Linhas (Avançado)]

Retorna resultados que correspondem aos critérios fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Sheets] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha do Google que contém a planilha que você deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Planilha] </td> 
   <td> <p>Selecione a planilha que contém as linhas que você deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Consulta]</td> 
   <td> <p>Use o [!DNL Google Charts Query Language]. Exemplo: <code>select * where B = "John"</code></p> <p>Para obter mais informações sobre [!DNL Google Charts Query Language], consulte <a href="https://developers.google.com/chart/interactive/docs/querylanguage">Referência da linguagem de consulta</a> na documentação [!DNL Google].</p> </td> 
  </tr> 
 </tbody> 
</table>

## Limites de uso

Se o erro `429: RESOURCE_EXHAUSTED` ocorrer, você excedeu o limite de taxa da API.

A API [!DNL Google Sheets] tem um limite de 500 solicitações por 100 segundos por projeto e 100 solicitações por 100 segundos por usuário. Os limites para leituras e gravações são rastreados separadamente. Não há limite de uso diário.

Veja mais detalhes em [developers.google.com/sheets/api/limits](https://developers.google.com/sheets/api/limits).

## Dicas e truques

* [Obter células vazias de uma  [!DNL Google] Planilha](#get-empty-cells-from-a-google-sheet)
* [Adicionar um botão em uma planilha para executar um cenário](#add-a-button-in-a-sheet-to-run-a-scenario)

### Obter células vazias de um [!DNL Google Sheet]

Para obter células vazias, você pode usar o módulo [!UICONTROL Linhas de Pesquisa (Avançadas)]. Use esta fórmula para obter as colunas que estão vazias.

```
select * where E is null
```

Aqui, &quot;E&quot; é a coluna e &quot;é nulo&quot; é a condição. Você pode criar uma consulta mais avançada usando a linguagem de consulta do Google. Para obter mais informações, consulte [Google Query Lang](https://developers.google.com/chart/interactive/docs/querylanguage) na documentação do Google.

### Adicionar um botão em uma planilha para executar um cenário

1. Em [!DNL Workfront Fusion], insira o módulo **[!UICONTROL Webhook]** > **[!UICONTROL Webhooks personalizados]** no cenário e configure-o. Para obter instruções, consulte [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

1. Copie o URL do webhook.
1. Execute o cenário.
1. No Google Sheets, escolha **[!UICONTROL Inserir]** > **[!UICONTROL Desenho]**... na barra de menu principal.

1. Na janela [!UICONTROL Desenho], clique no ícone [Caixa de texto ]&#x200B;**&#x200B;**![[!UICONTROL &#x200B; Caixa de texto]](/help/workfront-fusion/references/apps-and-modules/assets/text-box.png) próximo à parte superior da janela.
1. Crie um botão e clique no botão **[!UICONTROL Salvar e Fechar]** no canto superior direito:
1. O botão é colocado em sua planilha. Clique nos três pontos verticais no canto superior direito do botão:
1. Escolha **[!UICONTROL Atribuir script..].** no menu.
1. Insira o nome do seu script (função), ex.: `runScenario` e clique em **[!UICONTROL OK]**:
1. Escolha **[!UICONTROL Ferramentas]** > **[!UICONTROL Editor de scripts]** na barra de menu principal.

1. Insira o seguinte código:

   * O nome da função deve corresponder ao nome especificado na etapa 9.
   * Substitua o URL pelo URL do webhook copiado na etapa 2.

     ```
     function runScenario() {
     UrlFetchApp.fetch("&lt;webhook you copied>");
     }
     ```

1. Pressione **[!UICONTROL Ctrl+S]** para salvar o arquivo de script, digite um nome de projeto e clique em **[!UICONTROL OK]**.

1. Volte para [!DNL Google Sheets] e clique no novo botão.
1. Conceda a autorização necessária para o script:
1. Em [!DNL Workfront Fusion], verifique se o cenário foi executado com êxito.

## Armazenamento de datas em uma planilha

Se você armazenar um valor Date em uma planilha sem qualquer formatação, ele aparecerá na planilha como texto no formato ISO 8601. No entanto, [!DNL Google Sheets] fórmulas ou funções que funcionam com datas que não compreendem esse texto (Exemplo: fórmula `=A1+10`) exibem o seguinte erro:

![Erro](/help/workfront-fusion/references/apps-and-modules/assets/mceclip6-350x87.png)

Para ajudar [!DNL Google Sheets] a entender a data, formate-a com a função `formatDate`. O formato correto passado para a função como o segundo argumento depende das configurações de localidade da planilha.

Para obter mais informações sobre esta função, consulte [[!UICONTROL formatDate] (date; format; [timezone])](/help/workfront-fusion/references/mapping-panel/functions/date-and-time-functions.md#formatdate-date-format-timezone) no artigo Funções de data e hora.

Para determinar o formato correto:

1. No Google Sheets, escolha **[!UICONTROL Arquivo]** > **[!UICONTROL Planilha]** configurações no menu principal para verificar e definir a localidade.

1. Depois de verificar ou definir a localidade apropriada, determine o formato de data e hora correspondente, escolhendo **[!UICONTROL Formato]** > **[!UICONTROL Número]** no menu principal. O formato é exibido ao lado do item de menu Data e hora:

1. Para compor o formato correto que deve ser passado para a função [!UICONTROL formatDate()], consulte a lista de [tokens para a formatação de data e hora](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md).

>[!BEGINSHADEBOX]

**Exemplo:**

Para o formato `MM/DD/YYYY HH:mm:ss` (para a localidade dos Estados Unidos):

![Fórmula de hora local](/help/workfront-fusion/references/apps-and-modules/assets/locale-time-350x83.png)

>[!ENDSHADEBOX]

## Explorando funções [!DNL Google Sheets]

Para usar uma função integrada do Google Sheets, você pode explorá-la. Para obter mais informações, consulte [Usar [!DNL Google Sheets] funções](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md#use-google-sheets-functions) no artigo Mapear um item usando funções.

## Impedir [!DNL Google Sheets] de transformar números em datas

Se uma sequência de números que você está usando como texto estiver sendo interpretada como uma data em uma planilha [!DNL Google], você poderá pré-formatar o número como texto simples para evitar isso. Por exemplo, se você digitar 1-2019, com a intenção de usá-lo como texto, o Google poderá interpretá-lo como uma data.

1. Em [!DNL Google Sheets], realce a coluna ou célula que contém o número ou os números.
1. Clique em **[!UICONTROL Formatar]** > **[!UICONTROL Número]** > **[!UICONTROL Texto sem formatação]**.

Outra solução alternativa em [!DNL Workfront Fusion] é digitar um apóstrofo (&#39;) antes de um número, por exemplo, &#39;1-2019 ou &#39;1/47. O apóstrofo não é exibido na célula após os dados serem enviados de [!DNL Workfront Fusion].
