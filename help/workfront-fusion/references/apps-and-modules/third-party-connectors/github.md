---
title: Módulos do GitHub
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o GitHub, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: d9e6c26c-8770-40bc-a83a-8c05f86e4a3f
source-git-commit: 899fc717f5107433d6f1aea31c4d079243a85822
workflow-type: tm+mt
source-wordcount: '1850'
ht-degree: 0%

---

# [!DNL GitHub] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam o [!UICONTROL GitHub], bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!DNL GitHub], você deve ter uma conta [!DNL GitHub].

## Conectar [!DNL GitHub] a [!DNL Workfront Fusion]

Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL GitHub] módulos e seus campos.

Ao configurar módulos do [!DNL GitHub], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL GitHub] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)

### Acionadores

* [[!UICONTROL Assistir Comentários]](#watch-comments)
* [[!UICONTROL Bifurcações de Inspeção]](#watch-forks)
* [[!UICONTROL Assistir Problemas]](#watch-issues)
* [[!UICONTROL Observar Solicitações Pull]](#watch-pull-requests)
* [[!UICONTROL Observar repositórios]](#watch-repositories)

#### [!UICONTROL Assistir Comentários]

Esse módulo de acionamento inicia um cenário quando um novo comentário é adicionado ou um comentário existente é modificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que deseja observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de Problema]</td> 
   <td>Se quiser restringir a pesquisa apenas pesquisando novos comentários feitos em uma ocorrência específica, informe o número da ocorrência.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de problemas retornados]</td> 
   <td> <p> Defina o número máximo de comentários que [!DNL Workfront Fusion] retorna durante um ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Observar]</td> 
   <td>Selecione se deseja observar somente novos comentários ou comentários e todas as alterações.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Bifurcações de Inspeção]

Este módulo de acionamento inicia um cenário quando uma nova bifurcação é criada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que deseja observar por bifurcações.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de bifurcações retornadas]</td> 
    <td>Insira ou mapeie o número máximo de bifurcações que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assistir Problemas]

Esse módulo de acionamento inicia um cenário quando um novo problema é adicionado ou um problema existente é modificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL que eu quero assistir]</td> 
   <td>Selecione se deseja observar todos os repositórios associados a esta conta ou apenas um repositório.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Se você optou por observar problemas em apenas um repositório, selecione o repositório que deseja observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de problemas retornados]</td> 
   <td> <p> Defina o número máximo de problemas que [!DNL Workfront Fusion] retorna durante um ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Observar]</td> 
   <td>Selecione se deseja observar somente novos problemas ou novos problemas e todas as alterações.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Você pode filtrar os problemas que deseja observar pela maneira como está associado a eles.</p> 
    <ul> 
     <li>[!UICONTROL Todos os problemas]</li> 
     <li>[!UICONTROL Somente problemas atribuídos a mim]</li> 
     <li>[!UICONTROL Somente problemas criados por mim]</li> 
     <li>[!UICONTROL Somente problemas que me mencionam]</li> 
     <li>[!UICONTROL Somente problemas para os quais me inscrevi para receber atualizações]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estado]</td> 
   <td>Selecione se você deseja assistir somente a problemas abertos ou somente a problemas fechados. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rótulos]</td> 
   <td>Para cada marca que você deseja adicionar, clique em <b>Adicionar item</b> e insira a marca. O módulo observa problemas com essas tags.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar Solicitações Pull]

Este módulo dispara quando uma nova solicitação de pull é adicionada ou uma solicitação de pull existente é modificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que deseja observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de solicitações de pull retornadas]</td> 
   <td> <p> Defina o número máximo de solicitações de pull que [!DNL Workfront Fusion] retorna durante um ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estado]</td> 
   <td>Selecione se deseja observar solicitações [!UICONTROL somente abertura de pull], [!UICONTROL somente fechadas] ou todas as solicitações de pull. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Observar]</td> 
   <td>Selecione se deseja observar somente novas solicitações de baixa automática ou novas solicitações de baixa automática e todas as alterações.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar repositórios]

Esse módulo de acionador inicia um cenário quando um repositório é criado ou modificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de repositórios retornados]</td> 
   <td> <p> Defina o número máximo de repositórios que [!DNL Workfront Fusion] retorna durante um ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Observar]</td> 
   <td>Selecione se deseja observar novos repositórios e todas as alterações ou somente novos repositórios.</td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Adicionar responsáveis]](#add-assignees)
* [[!UICONTROL Adicionar rótulos a um problema]](#add-labels-to-an-issue)
* [[!UICONTROL Criar um comentário]](#create-a-comment)
* [[!UICONTROL Criar um problema]](#create-an-issue)
* [[!UICONTROL Obter um problema]](#get-an-issue)
* [[!UICONTROL Listar comentários]](#list-comments)
* [[!UICONTROL Remover um rótulo de um problema]](#remove-a-label-from-an-issue)
* [[!UICONTROL Remover responsáveis]](#remove-assignees)
* [[!UICONTROL Procurar um problema]](#search-for-an-issue)
* [[!UICONTROL Atualizar um problema]](#update-an-issue)

#### [!UICONTROL Adicionar responsáveis]

Este módulo adiciona responsáveis ao problema especificado

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que contém o problema ao qual você deseja adicionar atribuídos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Atribuído]</td> 
   <td>Selecione as pessoas que você deseja atribuir à ocorrência. Os designados disponíveis incluem qualquer pessoa com permissões de gravação no repositório e membros da organização com permissões de leitura no repositório. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número]</td> 
   <td>Insira ou mapeie o número do problema ao qual você deseja adicionar atribuídos. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Adicionar rótulos a um problema]

Este módulo adiciona rótulos a um problema. Os rótulos são definidos no nível do repositório e só podem ser criados por alguém com acesso de gravação ao repositório.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que contém o problema ao qual deseja adicionar rótulos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rótulos]</td> 
   <td>Selecione os rótulos que deseja adicionar ao problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número]</td> 
   <td>Insira ou mapeie o número do problema ao qual deseja adicionar rótulos.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar um comentário]

Este módulo cria um comentário sobre o problema especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que contém o problema no qual deseja criar um comentário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número]</td> 
   <td>Insira ou mapeie o número do problema no qual deseja criar um comentário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td>Insira ou mapeie o conteúdo do comentário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar um problema]

Este módulo cria um novo problema no repositório selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório no qual deseja criar um problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Atribuído]</td> 
   <td>Selecione as pessoas que você deseja atribuir à ocorrência. Os designados disponíveis incluem qualquer pessoa com permissões de gravação no repositório e membros da organização com permissões de leitura no repositório. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etapa]</td> 
   <td>Selecione a etapa que você deseja associar à nova ocorrência. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rótulos]</td> 
   <td>Selecione os rótulos que deseja aplicar ao novo problema. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Título]</td> 
   <td>Insira ou mapeie um título para o novo problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td>Insira ou mapeie o corpo do problema, como uma descrição ou informações adicionais</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um problema]

Este módulo recupera detalhes sobre o problema especificado

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que contém o problema sobre o qual deseja recuperar detalhes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número]</td> 
   <td>Insira ou mapeie o número do problema sobre o qual você deseja recuperar detalhes. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar comentários]

Este módulo lista todos os comentários sobre o problema especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que contém o problema do qual deseja listar comentários.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número]</td> 
   <td>Insira ou mapeie o número da ocorrência da qual deseja listar comentários.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Desde]</td> 
   <td>O módulo retornará comentários criados após essa data. Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de comentários retornados]</td> 
   <td> <p> Defina o número máximo de comentários que [!DNL Workfront Fusion] retorna durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remover um rótulo de um problema]

Este módulo remove um único rótulo de um problema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que contém o problema do qual deseja remover um rótulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rótulos]</td> 
   <td>Selecione o rótulo que deseja remover do problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número]</td> 
   <td>Insira ou mapeie o número do problema do qual deseja remover um rótulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remover responsáveis]

Este módulo remove os atribuídos do problema especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório que contém o problema do qual você deseja remover os atribuídos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Atribuído]</td> 
   <td>Selecione as pessoas que você deseja remover do problema. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número]</td> 
   <td>Informe ou mapeie o número do problema do qual deseja remover os designados. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Procurar um problema]

Este módulo procura por problemas que correspondam aos seus critérios de busca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de problemas retornados]</td> 
   <td> <p> Defina o número máximo de problemas que [!DNL Workfront Fusion] retorna durante um ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classificar por]</td> 
   <td> <p>Selecione como deseja classificar os resultados da pesquisa.</p> 
    <ul> 
     <li> <p>[!UICONTROL Melhor correspondência] </p> </li> 
     <li>[!UICONTROL Data de criação]</li> 
     <li>[!UICONTROL Data de atualização]</li> 
     <li>[!UICONTROL Número de comentários]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Direção de classificação]</td> 
   <td> <p>Selecione crescente ou decrescente. </p> <p>Para datas, selecionar <strong>[!UICONTROL decrescente]</strong> retornará a data mais recente primeiro. </p> <p>Para [!UICONTROL número de comentários], selecionar <strong>[!UICONTROL descendente]</strong> retornará o problema com o maior número de comentários primeiro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Consulta]</td> 
   <td>Insira ou mapeie a consulta de pesquisa. Para obter uma descrição detalhada das opções de pesquisa, consulte <a href="https://docs.github.com/en/github/searching-for-information-on-github/searching-issues-and-pull-requests">Pesquisa de problemas e pull requests</a> no site de ajuda [!DNL GitHub].</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um problema]

Este módulo atualiza um problema [!DNL GitHub] existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL GitHub] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repositório]</td> 
   <td>Selecione o repositório no qual deseja atualizar um problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Atribuído]</td> 
   <td>Selecione as pessoas que você deseja atribuir à ocorrência. Os designados disponíveis incluem qualquer pessoa com permissões de gravação no repositório e membros da organização com permissões de leitura no repositório. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etapa]</td> 
   <td>Selecione a etapa que você deseja associar à ocorrência. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rótulos]</td> 
   <td>Selecione os rótulos que deseja aplicar ao problema. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número]</td> 
   <td>Insira ou mapeie o número do problema que você deseja atualizar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estado]</td> 
   <td>Selecione o estado para o qual você deseja atualizar o problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Título]</td> 
   <td>Insira ou mapeie um novo título para o problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td>Informe ou mapeie um novo corpo para a ocorrência, como uma descrição ou informações adicionais</td> 
  </tr> 
 </tbody> 
</table>
