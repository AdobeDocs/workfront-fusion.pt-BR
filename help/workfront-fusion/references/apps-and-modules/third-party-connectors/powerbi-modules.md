---
title: Módulos do Power BI
description: O Adobe Workfront Fusion exige uma licença do Adobe Workfront Fusion, além de uma licença do Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: 73eb70e1-3f3d-419d-9cde-3ec3cda224f8
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2494'
ht-degree: 0%

---

# [!DNL Power BI] Módulos

[!DNL Power BI] é um aplicativo que permite visualizar e apresentar dados aos seus participantes. Ele pode receber dados de várias fontes.

>[!NOTE]
>
>[!DNL Workfront Fusion] não é uma fonte de dados. Embora o [!DNL Workfront Fusion] possa criar e usar fontes de dados, ele não armazena seus dados.


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

## Informações da API do Microsoft Power BI

O conector do Microsoft Power BI usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.powerbi.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.0.2</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Power BI] módulos e seus campos

Quando você configura o [!DNL Power BI], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro no Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Painéis](#dashboards)
* [Relatórios](#reports)
* [Conjunto de dados](#dataset)
* [Aplicativos](#apps)
* [Outro](#other)

### Painéis

* [Criar um painel](#create-a-dashboard)
* [Obter um painel](#get-a-dashboard)
* [Obter um bloco do painel](#get-a-dashboard-tile)
* [Listar blocos do painel](#list-dashboard-tiles)
* [Listar Painéis de Controle](#list-dashboards)

#### [!UICONTROL Criar um painel]

Esse módulo de ação cria um novo painel.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome]</td>
      <td>Insira ou mapeie um nome para o Painel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do grupo que será o proprietário do novo painel.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Obter um Painel]

Esse módulo de ação recupera metadados de um painel especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir uma ID de Painel]</td>
      <td>
        <p>Selecione ou mapeie a opção para escolher o painel para o qual deseja recuperar metadados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID do Painel]</td>
      <td>
        <p>Insira ou mapeie a ID do painel para a qual você deseja recuperar metadados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que possui os painéis para o qual você deseja recuperar metadados.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Obter um Bloco de Painel]

Este módulo de ação recupera metadados de um bloco do painel especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir uma ID de Painel]</td>
      <td>
        <p>Selecione ou mapeie a opção para escolher os detalhes do painel que deseja recuperar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID do Painel]</td>
      <td>
        <p>Insira ou mapeie a ID do painel para a qual deseja recuperar detalhes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Bloco]</td>
      <td>Insira ou mapeie a ID do bloco [!DNL Power BI] para o qual você deseja recuperar detalhes.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que é proprietário do bloco que você deseja recuperar.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Listar Blocos do Painel]

Este módulo de pesquisa recupera uma lista de blocos de painéis.

<table>
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Inserir uma ID de Painel]</td>
    <td>
      <p>Selecione ou mapeie a opção para escolher o painel cujos blocos você deseja listar.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL ID do Painel]</td>
    <td>
      <p>Insira ou mapeie a ID do painel que contém os blocos que você deseja listar.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
    <td>Selecione ou mapeie a ID do Grupo que possui os painéis que contêm os blocos que você deseja listar.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limite]  </td>
    <td>
      <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
    </td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Listar Painéis]

Este módulo de pesquisa recupera uma lista de painéis.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>
        <p>Selecione ou mapeie a ID do grupo que possui os painéis que você deseja listar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limite]  </td>
      <td>
        <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
      </td>
    </tr>
  </tbody>
</table>

### Relatórios

* [Copiar um relatório](#copy-a-report)
* [Excluir um relatório](#delete-a-report)
* [Obter um relatório](#get-a-report)
* [Listar Relatórios](#list-reports)

#### [!UICONTROL Copiar um relatório]

Este módulo de ação copia um relatório existente.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir uma ID de Relatório]</td>
      <td>
        <p>Selecione ou mapeie a opção para escolher o relatório que deseja copiar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Relatório]</td>
      <td>
        <p>Informe ou mapeie a ID do relatório que deseja copiar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que é proprietário do relatório que você deseja copiar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Novo Nome de Relatório Copiado]</td>
      <td>Insira ou mapeie um nome para o novo relatório.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Excluir um relatório]

Este módulo de ação exclui um relatório.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir uma ID de Relatório]</td>
      <td>
        <p>Selecione ou mapeie a opção para escolher o relatório que deseja excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Relatório]</td>
      <td>
        <p>Informe ou mapeie a ID do relatório que deseja deletar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que possui o relatório que você deseja excluir.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Obter um relatório]

Este módulo de ação recupera metadados de um relatório especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir uma ID de Relatório]</td>
      <td>
        <p>Selecione ou mapeie a opção para escolher o relatório para o qual deseja recuperar metadados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Relatório]</td>
      <td>
        <p>Insira ou mapeie a ID do relatório para o qual deseja recuperar metadados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que é proprietário do relatório para o qual você deseja recuperar metadados.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Listar Relatórios]

Este módulo de pesquisa recupera uma lista de relatórios.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>
        <p>Selecione ou mapeie a ID do Grupo que possui os relatórios que você deseja listar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limite]  </td>
      <td>
        <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
      </td>
    </tr>
  </tbody>
</table>


### Conjunto de dados

* [Adicionar/Excluir Linhas em uma Tabela de Conjunto de Dados](#add-or-delete-rows-in-a-dataset-table)
* [Criar um conjunto de dados](#create-a-dataset)
* [Excluir um conjunto de dados](#delete-a-dataset)
* [Obter um conjunto de dados](#get-a-dataset)
* [Listar conjuntos de dados](#list-datasets)
* [Atualizar um conjunto de dados](#refresh-a-dataset)

#### [!UICONTROL Adicionar ou Excluir Linhas em uma Tabela de Conjunto de Dados]

Esse módulo de ação adiciona ou exclui linhas de uma tabela de conjunto de dados de push especificada.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir uma tabela]</td>
      <td>Selecione ou mapeie a opção para selecionar o conjunto de dados que contém a tabela que você deseja ajustar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Conjunto de Dados]</td>
      <td>Insira ou mapeie a ID do conjunto de dados que contém as linhas que você deseja adicionar ou excluir.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome da Tabela]  </td>
      <td>
        <p>Insira ou mapeie o nome da tabela que contém as linhas que você deseja adicionar ou excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Insira ou mapeie a ID do grupo que é proprietário do conjunto de dados.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selecionar a Ação]</td>
      <td>
        <p>Selecione ou mapeie a ação que deseja executar.</p>
        <ul>
          <li>
            <p>[!UICONTROL Adicionar linhas]</p>
          </li>
          <li>
            <p>[!UICONTROL Excluir Todas as Linhas]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Linhas]</td>
      <td>
        <p>Adicione os campos de linha.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL chave]</b>
            </p>
            <p>Insira ou mapeie o nome da chave.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Tipo de Campo]</b>
            </p>
            <p>Selecione ou mapeie o tipo de campo:</p>
            <ul>
              <li>
                <p>Booleano</p>
              </li>
              <li>
                <p>Data</p>
              </li>
              <li>
                <p>Texto</p>
              </li>
              <li>
                <p>Número</p>
              </li>
            </ul>
          </li>
          <li>
            <p>[!UICONTROL Valor]</p>
            <p>Insira ou mapeie o valor da chave.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Criar um Conjunto de Dados]

Esse módulo de ação cria um novo conjunto de dados.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome]</td>
      <td>Insira ou mapeie um nome para o conjunto de dados.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que será o proprietário do novo conjunto de dados.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Modo Padrão]</td>
      <td>
        <p>Selecione ou mapeie o modo padrão do conjunto de dados:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Como Azure]</b>: Um conjunto de dados com uma conexão ativa com [!DNL Azure Analysis Service]</p>
          </li>
          <li>
            <p><b>[!UICONTROL Como no Local]</b>: Um conjunto de dados com uma conexão ativa com o Serviço [!DNL On-premise Analysis]</p>
          </li>
          <li>
            <p><b>[!DNL Push]</b>: um conjunto de dados que permite acesso programático para enviar dados para o [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Push Streaming]</b>: um conjunto de dados que suporta transmissão de dados e permite acesso programático para enviar dados para o [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Streaming]</b>: um conjunto de dados que suporta transmissão de dados</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tabelas]</td>
      <td>Adicione tabelas ao conjunto de dados. Para campos, consulte <a href="#Table" class="MCXref_0">Campos de tabela</a></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Data sources]</td>
      <td>Adicione as fontes de dados. Para campos, consulte <a href="#Data" class="MCXref_0">Campos de fontes de dados</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Default Retention Policy]  </td>
      <td>
        <p>Selecione ou mapeie a política intencional para o conjunto de dados:</p>
        <ul>
          <li>
            <p>[!UICONTROL Nenhum]</p>
          </li>
          <li>
            <p>[!UICONTROL FIFO Básico]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Campos de tabela

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Nome]</td>
      <td>
        <p>  Insira ou mapeie um nome para a tabela.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Colunas]</td>
      <td>
        <p>Adicione as colunas:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Nome]</b>
            </p>
            <p>Insira (mapeie) um nome de coluna.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Tipo de Dados]</b>
            </p>
            <p>Selecione ou mapeie o tipo de dados:</p>
            <ul>
              <li>
                <p>[!UICONTROL Cadeia de Caracteres]</p>
              </li>
              <li>
                <p>[!UICONTROL Inteiro]</p>
              </li>
              <li>
                <p>[!UICONTROL Booleano]</p>
              </li>
              <li>
                <p>[!UICONTROL Data Hora]</p>
              </li>
            </ul>
          </li>
          <li>
            <p><b>[!UICONTROL Formatar Cadeia de Caracteres]</b>
            </p>
            <p>Insira (mapeie) a string de formato.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Linhas]</td>
      <td>Informe ou mapeie detalhes da linha.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Medidas]</td>
      <td>Adicione a medida para as tabelas.</td>
    </tr>
  </tbody>
</table>

##### Campos de fontes de dados

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Banco de Dados]  </td>
      <td>
        <p>Insira ou mapeie o banco de dados que deseja usar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Server]  </td>
      <td>
        <p>Insira ou mapeie o nome do servidor que deseja usar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]  </td>
      <td>
        <p>Insira ou mapeie o URL que deseja usar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID da fonte de dados]</td>
      <td>
        <p>  Insira ou mapeie a ID da fonte de dados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de fonte de dados]  </td>
      <td>
        <p>Selecione ou mapeie o tipo de fonte de dados. Exemplo: SQL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID do Gateway]  </td>
      <td>Insira ou mapeie a ID do gateway que deseja usar.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Excluir um conjunto de dados]

Esse módulo de ação exclui um conjunto de dados.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir uma ID de Relatório]</td>
      <td>
        <p>Selecione ou mapeie a opção para escolher o conjunto de dados que deseja excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Relatório]</td>
      <td>
        <p>Insira ou mapeie a ID do conjunto de dados que você deseja excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que possui o conjunto de dados que você deseja excluir.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Obter um Conjunto de Dados]

Esse módulo de ação recupera metadados de um conjunto de dados especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir uma ID de Relatório]</td>
      <td>
        <p>Selecione ou mapeie a opção para escolher o relatório para o qual deseja recuperar metadados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Relatório]</td>
      <td>
        <p>Insira ou mapeie a ID do conjunto de dados para o qual você deseja recuperar metadados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que possui o conjunto de dados para o qual você deseja recuperar metadados.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Listar conjuntos de dados]

Este módulo de pesquisa recupera uma lista de conjuntos de dados.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Selecione ou mapeie a ID do Grupo que é proprietário do relatório para o qual você deseja recuperar metadados.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limite]</td>
      <td>
        <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Atualizar um conjunto de dados]

Este módulo de ação atualiza um conjunto de dados especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inserir um conjunto de dados]</td>
      <td>Selecione ou mapeie a opção para selecionar o conjunto de dados que deseja atualizar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Conjunto de Dados]</td>
      <td>Insira ou mapeie a ID do conjunto de dados que você deseja atualizar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome da Tabela]  </td>
      <td>
        <p>Insira ou mapeie o nome da tabela que contém as linhas que você deseja adicionar ou excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Grupo]  </td>
      <td>Insira ou mapeie a ID do grupo que é proprietário do conjunto de dados.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Opção de Notificação]  </td>
      <td>
        <p>Selecione ou mapeie a opção para notificar:</p>
        <ul>
          <li>
            <p>[!UICONTROL Email ao Concluir]</p>
          </li>
          <li>
            <p>[!UICONTROL Email em Falha]</p>
          </li>
          <li>
            <p>[!UICONTROL Sem Notificação]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Aplicativos

* [Obter um aplicativo](#get-an-app)
* [Obter o painel de um aplicativo](#get-an-apps-dashboard)
* [Obter um relatório do aplicativo](#get-an-apps-report)
* [Listar painéis do aplicativo](#list-apps-dashboards)
* [Listar relatórios do aplicativo](#list-apps-reports)
* [Listar aplicativos](#list-apps)
* [Assistir Aplicativos](#watch-apps)

#### [!UICONTROL Obter um aplicativo]

Este módulo de ação recupera metadados de um aplicativo especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID do Aplicativo]  </td>
      <td>
        <p>Selecione ou mapeie a ID do aplicativo que deseja recuperar.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Obter o Painel de um Aplicativo]

Este módulo de ação recupera metadados do painel de um aplicativo especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID do Aplicativo]  </td>
      <td>
        <p>Selecione ou mapeie a ID do aplicativo que contém o painel que você deseja recuperar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Relatório]</td>
      <td>
        <p>  Selecione ou mapeie a ID do painel que deseja recuperar.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Obter relatório de um aplicativo]

Este módulo de ação recupera os metadados do relatório de um aplicativo especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID do Aplicativo]  </td>
      <td>
        <p>Selecione ou mapeie a ID do aplicativo que contém o relatório que você deseja recuperar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Relatório]</td>
      <td>
        <p>  Selecione ou mapeie a ID do relatório que deseja recuperar.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Listar Aplicativos]

Este módulo de pesquisa recupera uma lista de todos os aplicativos instalados.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limite]  </td>
      <td>
        <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Listar painéis do aplicativo]

Este módulo de pesquisa recupera uma lista de painéis de um aplicativo especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID do Aplicativo]</td>
      <td>Selecione ou mapeie a ID do aplicativo do qual deseja listar painéis.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limite]  </td>
      <td>
        <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Listar relatórios do aplicativo]

Este módulo de pesquisa recupera uma lista de todos os relatórios do aplicativo especificado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID do Aplicativo]</td>
      <td>Selecione ou mapeie a ID do aplicativo do qual deseja listar relatórios.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limite]  </td>
      <td>
        <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Assistir Aplicativos]

Este módulo de acionamento inicia um cenário quando um aplicativo é atualizado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limite]  </td>
      <td>
        <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
      </td>
    </tr>
  </tbody>
</table>

### Outro

#### [!UICONTROL Fazer uma chamada de API]

Este módulo de ação executa uma chamada à API [!DNL Power BI].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Power BI] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Caminho]</p>
      </td>
      <td>
        <p>Insira um caminho relativo para <code>https://api.powerbi.com</code>. Exemplo: <code>/v1.0/myorg/datasets</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Método]</p>
      </td>
      <td>
        <p>Selecione o método de solicitação [!UICONTROL HTTP] necessário para configurar a chamada à API. Para obter mais informações, consulte [!UICONTROL HTTP] métodos de solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cabeçalhos]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização e cabeçalhos x-api-key automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cadeia de Consulta]  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
