---
title: Módulos de caixa
description: Em um [!DNL Adobe Workfront Fusion] cenário, você pode automatizar workflows que usam a Box, bem como conectá-la a vários aplicativos e serviços de terceiros. monitora uma pasta especificada para verificar se há alterações nos arquivos, modificar e excluir arquivos existentes ou para upload novos arquivos a uma pasta.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: 0ed33cbed2b8ed4ab2c89c86b7e8f37b2683ec75
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 1%

---

# Módulos de caixa

Em um [!DNL Adobe Workfront Fusion] cenário, é possível automatizar workflows que usam [!DNL Box], bem como conectá-lo a vários aplicativos e serviços de terceiros. monitora uma pasta especificada para verificar alterações em arquivos, modificar e excluir arquivos existentes ou fazer upload de novos arquivos para uma pasta.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Para obter informações sobre módulos, consulte os artigos em [Módulos: índice](/help/workfront-fusion/references/modules/modules-toc.md) do artigo.

## Requisitos de acesso

+++ Expanda para visualização requisitos de acesso do funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">pacote Adobe Systems workfront</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">licença da Adobe Systems Workfront</td> 
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
   <p>Novo:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote Ultimate Workfront: Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar Adobe Systems Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Os requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos [!DNL Box], você deve ter uma conta [!DNL Box].

## Informações da API de caixa

O conector Box usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] módulos e seus campos

Ao configurar módulos do [!DNL Box], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Box] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

* [[!UICONTROL Novo Evento de Arquivo]](#new-file-event)
* [Evento de nova pasta](#new-folder-event)
* [[!UICONTROL Observar arquivos]](#watch-files)

#### [!UICONTROL Novo Evento de Arquivo]

Esse módulo de acionador instantâneo inicia um cenário quando a ação selecionada ocorre em um arquivo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecione o webhook que deseja usar para assistir mensagens de saída ou adicione um webhook. </p><p>Para adicionar um webhook, clique em <strong>[!UICONTROL Adicionar]</strong> e digite o nome e a conexão do webhook, o arquivo que você deseja assistir e os acionadores que deseja observar.</p> <p> Para obter instruções sobre como conectar sua conta da [!UICONTROL Box] ao [!UICONTROL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Conectar-se a um serviço - Instruções básicas</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Evento de nova pasta

Esse módulo de acionamento instantâneo inicia um cenário quando a ação de seleção ocorre na pasta.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecione o webhook que deseja usar para assistir mensagens de saída ou adicione um webhook. </p><p>Para adicionar um webhook, clique <strong>em [! Adicionar UICONTROL]</strong> e inserir o nome e a conexão do webhook, a pasta que você deseja assistir e os acionadores que você deseja observar.</p> <p> Para obter instruções sobre como conectar seu [! Caixa UICONTROL] conta para [! UICONTROL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Conectar a um serviço - Instruções básicas</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assista arquivos]

Esse acionador módulo inicia um cenário quando um novo arquivo é adicionado ou um arquivo existente é atualizado em uma pasta sendo monitorada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Box] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Assista na pasta</td> 
   <td> <p>Selecione a pasta que deseja assistir. Um cenário pode observar uma única pasta.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Relógio</td> 
   <td> <p>Selecione o tipo de arquivos que deseja assistir.</p> 
    <ul> 
     <li> <p><strong>Somente arquivos novos</strong> </p> <p>O cenário start quando um novo arquivo é adicionado.</p> </li> 
     <li> <p><strong>arquivos de Novo e todas as alterações</strong> </p> <p>O cenário começa quando um arquivo é adicionado ou quando um arquivo conteúdo ou um atributo de arquivo (como seu nome) é modificado.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Número máximo de arquivos baixados</p> </td> 
   <td> <p>Insira o número mais alto de arquivos que deseja que a módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

<!--* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Upload] a file](#upload-a-file)-->
* [Criar uma pasta](#create-a-folder)
* [Obter uma pasta](#get-a-folder)
* [Obter metadados da pasta](#get-folder-metadata)
* [Fazer uma chamada de API](#make-an-api-call)
* [Atualizar metadados Pasta](#update-folder-metadata)

<!--#### [!UICONTROL Delete a file] 

This action module deletes a file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This action module downloads a file.

You specify the ID of the file.

>[!NOTE]
>
>This module is useful for providing files to subsequent modules.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to retrieve.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a file] 

This action module updates a file.

You specify the ID of the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file] 

This action module uploads a file.

You specify the file. You can also provide a new filename for the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder where you want to upload the file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If this module is not successful, consider the following:
>
>* The size of the file might exceed the maximum file size limit for your [!DNL Box] plan, or you may have used all of your [!DNL Box] account's storage quota. To get more storage space, delete existing files from [!DNL Box] or upgrade your [!DNL Box] account.
>* [!DNL Box] does not upload more than one files with the same name to a single folder. If the destination folder contains a file with the same name as the file being uploaded, the scenario run terminates with an error. To avoid this, rename the file. If you want to update the file, use the **[!UICONTROL Update a file]** module.-->

#### Criar uma Pasta

Essa ação módulo cria uma nova pasta vazia dentro da pasta pai especificada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! Conexão UICONTROL]</td> 
   <td> <p>Para obter instruções sobre como conectar suas [!DNL Box] conta, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] instruções básicas</a>[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Nome UICONTROL]</td> 
   <td> <p>Insira ou mapeie um nome para a nova pasta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta Pai]</td> 
   <td> <p>Selecione a pasta na qual deseja criar a nova pasta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta Carregar Acesso a Email]</td> 
   <td> <p>Quando esse parâmetro for definido, os usuários poderão enviar arquivos por email para o endereço de email que foi criado automaticamente para essa pasta. As opções de colaboradores permitem somente emails registrados de colaboradores.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estado de Sincronização]</td> 
   <td> <p>Especifica se uma pasta deve ser sincronizada com o dispositivo de um usuário ou não. Isto é usado pela Box Sync (descontinuado) e não é usado pela Box Drive.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obter uma pasta

Esse módulo de ação recupera detalhes de uma pasta, incluindo as primeiras 100 entradas na pasta.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Box] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Pasta UICONTROL]</td> 
   <td> <p>Selecione a pasta para a qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obter metadados Pasta

Essa ação módulo recupera o metadados da pasta por ID da pasta.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! Conexão UICONTROL]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Box] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escopo]</td> 
   <td> <p>Selecione o escopo que deseja usar para essa recuperação de metadados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td> <p>Selecione a pasta para a qual deseja recuperar metadados.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Fazer uma chamada de API

Esse módulo de ação faz uma chamada personalizada para a API Box.



<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Bynder] ao [!DNL Workfront Fusion], consulte <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Bynder] ao [!DNL Workfront Fusion] </a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Insira um caminho relativo para <code>https://api.box.com</code>. <p>Exemplo: <code>/2.0/users/me</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos do solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! String de consulta UICONTROL]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar declarações condicionais como <code>if</code> no JSON, coloque as aspas fora da declaração condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar metadados Pasta

Essa ação módulo cria ou atualiza o metadados de uma pasta.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! Conexão UICONTROL]</td> 
   <td> <p>Para obter instruções sobre como conectar suas [!DNL Box] conta, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] instruções básicas</a>[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Escopo UICONTROL]</td> 
   <td> <p>Selecione as escopo que deseja usar para essa atualização metadados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Pasta UICONTROL]</td> 
   <td> <p>Selecione a pasta para a qual deseja atualizar os metadados.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Pesquisas

#### Pesquisar por conteúdo

Este módulo de pesquisa procura por itens que estejam disponíveis para o usuário ou para toda a empresa.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar suas [!DNL Box] conta, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] instruções básicas</a>[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Consulta UICONTROL]</td> 
   <td> <p>Insira ou mapeie a cadeia de caracteres para pesquisa. Essa query é comparada com nomes de itens, descrições, conteúdo de texto de arquivos e vários outros campos dos diferentes tipos de itens.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Escopo UICONTROL]</td> 
   <td> <p>Selecione se você está procurando por conteúdo associados ao usuário cujas credenciais são usadas para a conexão usada neste módulo ou procurando conteúdo associados a toda a empresa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td> <p>Selecione se você está procurando arquivos, pastas ou links da Web.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Classificação UICONTROL]</td> 
   <td> <p>Selecione se deseja classificar por relevância ou por data modificada.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Conteúdo de lixeira UICONTROL]</td> 
   <td> <p>Selecione se deseja pesquisa conteúdo ou conteúdo que não foram enviados para a lixeira.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! IDs de Pasta pai UICONTROL]</td> 
   <td> <p>Para pesquisar em uma pasta específica, para cada pasta que você deseja pesquisar, clique em <b>Adicionar item</b> e insira a ID da pasta. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criado A Partir De]</td> 
   <td> <p>Para pesquisar ativos criados em um determinado intervalo de datas, insira a data mais antiga no intervalo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criado para]</td> 
   <td> <p>Para pesquisar ativos criados em um determinado intervalo de datas, insira a última data no intervalo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL Atualizado de]</td> 
   <td> <p>Para pesquisa para ativos atualizados em determinado intervalo de datas, insira a data mais antiga no intervalo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL atualizado para]</td> 
   <td> <p>Para pesquisa for ativos atualizados em determinada intervalo de datas, insira a data mais recente no intervalo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Campos UICONTROL]</td> 
   <td> <p>Para cada atributo que você deseja retornar na resposta do módulo, clique em <b>Adicionar item</b> e insira o campo.</p><p>Isso pode ser usado para solicitar campos que normalmente não são retornados em uma resposta padrão. Esteja ciente de que a especificação desse parâmetro terá o efeito de que nenhum dos campos padrão será retornado na resposta, a menos que especificado explicitamente. </p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Extensões de Arquivo]</td> 
   <td> <p>Para limitar a pesquisa a extensões de arquivo específicas, digite uma lista separada por vírgulas de extensões de arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tamanho de]</td> 
   <td> <p>Para pesquisar ativos em um intervalo de tamanho específico, insira o final pequeno do intervalo, em bytes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dimensionar em]</td> 
   <td> <p>Para pesquisar ativos em um intervalo de tamanho específico, insira o fim do intervalo, em bytes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Usuário Proprietário]</td> 
   <td> <p>Para pesquisar ativos de propriedade de usuários específicos, insira uma lista separada por vírgulas de IDs de proprietários.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de resultados que você deseja que o módulo retorne em cada ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>


