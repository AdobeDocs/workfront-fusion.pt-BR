---
title: Módulos do Veeva Vault
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Veeva Vault, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
source-git-commit: 4f5a4cf8691e5bb47eec6f6b2842369c5c6fbad8
workflow-type: tm+mt
source-wordcount: '1516'
ht-degree: 3%

---

# Módulos do Veeva Vault

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Veeva Vault, bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Para usar os módulos do Veeva Vault, você deve ter uma conta do Veeva Vault.

## Módulos do Veeva Vault e seus campos

Ao configurar os módulos do Veeva Vault, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Veeva Vault podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Documento

* [Criar um único documento](#create-a-single-document)
* [Criar vários documentos](#create-multiple-documents)
* [Excluir um único documento](#delete-a-single-document)
* [Exportar documentos](#export-documents)
* [Obter um único documento](#get-a-single-document)
* [Iniciar ação do usuário](#initiate-user-action)
* [Listar documentos](#list-documents)
* [Recuperar resultados da exportação de documentos](#retrieve-document-export-results)
* [Atualizar vários documentos](#update-multiple-documents)
* [Atualizar um único documento](#update-a-single-document)

#### Criar um único documento

Este módulo cria um único documento, binder ou modelo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar um documento, um binder ou um modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Selecionar campos</p> </td> 
   <td> <p>Selecione os campos para os quais deseja inserir dados e, em seguida, insira os dados nesses campos.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar vários documentos

Este módulo cria vários documentos ou modelos usando um arquivo CSV.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar modelos ou documentos</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dados do arquivo</p> </td> 
   <td> <p>Mapeie o arquivo CSV que será usado para criar os documentos.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um único documento

Este módulo exclui um único documento, binder ou modelo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja excluir um documento, um binder ou um modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID do documento / ID do associador / Nome do modelo</p> </td> 
   <td> <p>Selecione os campos que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Exportar documentos

Este módulo exporta documentos que você especificar, incluindo origens, representações e texto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja excluir um documento, um binder ou um modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Fonte</p> </td> 
   <td> <p>Habilite essa opção para incluir arquivos de origem na exportação.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Representações</p> </td> 
   <td> <p>Habilite essa opção para incluir arquivos de representação na exportação.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Todas as versões</p> </td> 
   <td> <p>Habilite esta opção para incluir todas as versões dos arquivos de documento na exportação.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Texto</p> </td> 
   <td> <p>Habilite esta opção para incluir o texto do documento de origem na exportação.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Obter um único documento

Este módulo recupera metadados para um único documento, binder ou modelo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja recuperar dados de um documento, binder ou modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID do documento / ID do associador / Nome do modelo</p> </td> 
   <td> <p>Selecione os campos para os quais deseja recuperar dados.</td> 
  </tr> 
 </tbody> 
</table>

#### Iniciar ação do usuário

Este módulo inicia ações em documentos e binders, como enviar um documento para revisão ou alterar seu estado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se você deseja executar uma ação em um documento ou um binder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Documento / Fichário</p> </td> 
   <td> <p>Selecione o documento ou o binder no qual deseja executar a ação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versão do documento/Versão do fichário</p> </td> 
   <td> <p>Selecione o documento ou o binder no qual deseja executar a ação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Ação</p> </td> 
   <td> <p>Selecione a ação a ser executada no documento ou binder.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar documentos

Este módulo lista todos os documentos do tipo selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja listar documentos, binders ou modelos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### Recuperar resultados da exportação de documentos

Este módulo retorna os resultados de uma exportação de documento solicitada anteriormente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID da tarefa</p> </td> 
   <td> <p>Insira ou mapeie a ID do trabalho para o qual deseja retornar resultados. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Atualizar vários documentos

Este módulo atualiza vários documentos ou modelos usando um arquivo CSV.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar modelos ou documentos</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dados do arquivo</p> </td> 
   <td> <p>Mapeie o arquivo CSV que será usado para criar os documentos.</td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um único documento

Este módulo atualiza um único documento, binder ou modelo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar um documento, uma versão do documento, um binder ou um modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID / Nome</p> </td> 
   <td> <p>Se você estiver atualizando um modelo, digite um novo nome para ele.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Nome do novo modelo</p> </td> 
   <td> <p>Insira ou mapeie a ID ou o nome do objeto que você deseja atualizar.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Selecionar campos</p> </td> 
   <td> <p>Selecione os campos para os quais deseja inserir dados e, em seguida, insira os dados nesses campos.</td> 
  </tr> 
 </tbody> 
</table>

### Objeto



#### Listar objetos

Este módulo recupera todos os objetos do Vault no Vault autenticado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Recuperar rótulos localizados</p> </td> 
   <td> <p>Selecione Sim para recuperar strings localizadas (traduzidas) para os campos label e label_plural.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

### Outras

* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Criar uma consulta VQL](#make-a-vql-query)
* [Ler logs](#read-logs)

#### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada personalizada para a API do Veeva Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Insira um caminho relativo para <code>baseurl/api/v</code>.  Por exemplo: <code>/objects/documents</code>. Não inclua <code>baseurl/api/v/</code>, pois ele já está incluído.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Método</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cabeçalhos</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sequência de consulta</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Criar uma consulta VQL

Esse módulo faz uma consulta usando o VQL (Vault Query Language).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar modelos ou documentos</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dados do arquivo</p> </td> 
   <td> <p>Mapeie o arquivo CSV que será usado para criar os documentos.</td> 
  </tr> 
 </tbody> 
</table>

#### Ler logs

Este módulo retorna dados de trilhas de auditoria

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo de auditoria</p> </td> 
   <td> <p>Selecione o tipo de auditoria para o qual deseja recuperar dados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data inicial</p> </td> 
   <td> <p>Informe ou mapeie a data inicial das auditorias que deseja recuperar.</p><p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data final</p> </td> 
   <td> <p>Informe ou mapeie a data final das auditorias que deseja recuperar.</p><p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL de resultado </p> </td> 
   <td> <p>Selecione CSV se desejar obter o URL para baixar um CSV do resultado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>


