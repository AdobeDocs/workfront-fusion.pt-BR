---
title: Módulos Airtable
description: O Adobe Workfront Fusion exige uma licença do Adobe Workfront Fusion, além de uma licença do Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: 3b445b50-5812-4ded-9788-f467991e0b52
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1923'
ht-degree: 2%

---

# Módulos Airtable


Com o conector [!DNL Airtable] para Adobe Workfront Fusion, você pode iniciar um cenário com base em eventos na sua conta do [!DNL Airtable], criar, carregar e atualizar registros, registros de pesquisa e fazer chamadas de API personalizadas para a API do Airtable.

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

Você deve ter uma conta Airtable para usar a funcionalidade deste artigo.

<!--
<p>For more information, see the tutorial .</p>
-->

## Informações da API Airtable

O conector Airtable usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td>https://api.airtable.com/v0</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v3.3.28</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o Airtable ao Workfront Fusion {#connect-airtable-to-workfront-fusion}

<!--

1. Log in to your Airtable account.
1. Open your account overview and generate the API key.
-->
1. Abra o Workfront Fusion e a caixa de diálogo **Criar uma conexão** do módulo desejado.
1. Insira um nome para a conexão.
1. (Opcional) Clique em Mostrar configurações avançadas e digite a ID do cliente do Airtable e o Segredo do cliente.
1. Clique no botão **Continuar** para criar a conexão e retornar ao módulo.

## Módulos dirigíveis e seus campos

### Registros

* [Criar um Registro](#create-a-record)
* [Excluir um Registro](#delete-a-record)
* [Obter um registro](#get-a-record)
* [Pesquisar Registros](#search-records)
* [Atualizar um Registro](#update-a-record)
* [Inserir um Registro](#upsert-a-record)
* [Observar registros](#watch-records)
* [Assistir Respostas](#watch-responses)
* [Fazer uma chamada de API](#make-an-api-call)

#### Criar um registro {#create-a-record}

Este módulo de ação cria um novo registro.

Especifique os dados que deseja no registro e onde deseja que ele seja armazenado.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Airtable ao Workfront Fusion, consulte <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Conectar o Airtable ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selecione a base à qual pertencerá o novo registro.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabela </td> 
   <td> <p>Selecione a tabela à qual o novo registro pertencerá.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Registro</p> </td> 
   <td> <p>Insira os valores para o novo registro. Os campos disponíveis são baseados na tabela selecionada.</p> <!--<p>For more information on field types, search for "Supported field types" in the Airtable documentation.</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>Multiple lines of text, which may contain "mention tokens", for example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong> : Add the attachment. Airtable will download the file from the provided <code>url</code> and keep its own copy of it. If the File name field is left empty, Airtable generates the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05 (ISO 8601 formatted date)</li> 
     <li>Phone number:</li> 
     <li><strong>Emails</strong>: A valid email address.</li> 
     <li><strong>URL</strong>: A valid URL (for example, airtable.com or https://airtable.com/universe).</li> 
     <li><strong>Number</strong>: Enter a number.</li> 
     <li><strong>Currency</strong>: Currency value.</li> 
     <li><strong>Percent</strong>: A percentage value. Must be higher than or equal to 0.</li> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation. </li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs will be reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Links inteligentes</td> 
   <td> <p>Ative essa opção para inserir nomes em vez de IDs de registro em campos que se vinculam a outra tabela. O registro é criado automaticamente na tabela vinculada se não houver correspondência.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um Registro {#delete-a-record}

Esse módulo de ação exclui um registro específico.

Especifique a ID e os locais do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Airtable ao Workfront Fusion, consulte <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Conectar o Airtable ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selecione a base que contém o registro que você deseja deletar.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabela </td> 
   <td> <p>Selecione a tabela que contém o registro que deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td>ID do registro</td> 
   <td> <p>Insira ou mapeie o ID exclusivo do Airtable do registro que você deseja que o módulo exclua. Você pode recuperar a ID, por exemplo, usando o módulo Pesquisar registros.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obter um registro {#get-a-record}

Este módulo de ação recupera detalhes do registro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Airtable ao Workfront Fusion, consulte <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Conectar o Airtable ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selecione a base que contém a tabela com o registro que você deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabela</td> 
   <td> <p> Selecione a tabela que contém o registro para o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td>ID do registro</td> 
   <td> <p> Insira ou mapeie a ID do registro para o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Pesquisar Registros {#search-records}

Esse módulo de pesquisa procura registros em um objeto no Airtable que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Airtable ao Workfront Fusion, consulte <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Conectar o Airtable ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selecione a base na qual deseja pesquisar registros.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabela </td> 
   <td> <p>Selecione a tabela que deseja pesquisar registros.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fórmula</p> </td> 
   <td> <p>Uma fórmula usada para filtrar registros. A fórmula é avaliada para cada registro e, se o resultado não for <code>0</code>, <code>false</code>, <code>""</code>, <code>NaN</code>, <code>[]</code> ou <code>#Error!</code>, o registro será incluído na resposta.</p> <p>Se combinado com o <code>view</code>, somente os registros nessa exibição que satisfazem a fórmula serão retornados.</p> <p>Por exemplo, para incluir apenas registros em que Nome não esteja vazio, transmita em:<code> NOT({Name} = '')</code></p> <p>Para saber mais, procure informações sobre referências de campo de fórmula na documentação de suporte do Airtable.</p> </td> 
  </tr> 
  <tr> 
   <td>Ordenar </td> 
   <td> <p>Selecione a direção da classificação e o campo pelo qual deseja classificar os resultados.</p> </td> 
  </tr> 
  <tr> 
   <td>Exibir </td> 
   <td> <p>Selecione a exibição na qual deseja pesquisar registros.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um Registro {#update-a-record}

Esse módulo de ação atualiza um registro específico.

Especifique a ID do registro e os novos dados que deseja que ele contenha.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Airtable ao Workfront Fusion, consulte <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Conectar o Airtable ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selecione a base que contém o registro que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabela </td> 
   <td> <p>Selecione a tabela que contém o registro que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td>ID do registro </td> 
   <td> <p>Insira ou mapeie o ID exclusivo do Airtable do registro que você deseja que o módulo atualize. Você pode recuperar a ID, por exemplo, usando o módulo Pesquisar registros.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Registro</p> </td> 
   <td> <p>Insira os valores para o novo registro. Os campos disponíveis dependem da tabela selecionada.</p> <!--<p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Links inteligentes</td> 
   <td> <p>Insira nomes em vez de IDs de registro para campos que se vinculam a outra tabela. O registro é criado automaticamente na tabela vinculada se não houver correspondência.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Inserir um registro

Esse módulo de ação atualiza ou insere um registro específico.

Especifique a ID do registro e os novos dados que deseja que ele contenha.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Airtable ao Workfront Fusion, consulte <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Conectar o Airtable ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selecione a base que contém o registro que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabela </td> 
   <td> <p>Selecione a tabela que contém o registro que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td>ID do registro </td> 
   <td> <p>Se você estiver atualizando um registro, informe ou mapeie o ID do Airtable exclusivo do registro que deseja que o módulo atualize. Você pode recuperar a ID, por exemplo, usando o módulo Pesquisar registros.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Registro</p> </td> 
   <td> <p>Insira os valores para o novo registro. Os campos disponíveis dependem da tabela selecionada.</p> <!-- <p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Links inteligentes</td> 
   <td> <p>Insira nomes em vez de IDs de registro para campos que se vinculam a outra tabela. O registro é criado automaticamente na tabela vinculada se não houver correspondência.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Observar registros {#watch-records}

Esse módulo de acionamento inicia um cenário quando um registro é criado ou atualizado na tabela especificada.

>[!NOTE]
>
>Para usar esse módulo, o campo Hora de criação ou Hora da última modificação deve ser criado na tabela.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Airtable ao Workfront Fusion, consulte <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Conectar o Airtable ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selecione a base que deseja observar para novos registros.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabela </td> 
   <td> <p>Selecione a tabela que deseja observar para novos registros.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Configuração do acionador</p> </td> 
   <td> <p>Campo de acionamento</p> <p>Um campo <code>Created Time</code> ou <code>Last Modified Time</code> que é usado para classificar registros. Se você não tiver um campo <code>Created Time</code> ou <code>Last Modified Time</code> no esquema, será necessário criar um. </p> <p>Campo de rótulo</p> <p>Um campo usado como rótulo para um registro, por exemplo, na caixa de diálogo Escolher onde iniciar.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que você deseja que o módulo assista durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td>Exibir</td> 
   <td> <p>Selecione a exibição que deseja usar.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fórmula</p> </td> 
   <td> <p>Uma fórmula usada para filtrar registros. A fórmula é avaliada para cada registro e, se o resultado não for <code>0</code>, <code>false</code>, <code>""</code>, <code>NaN</code>, <code>[]</code> ou <code>#Error!</code>, o registro será incluído na resposta.</p> <p>Se combinado com o <code>view</code>, somente os registros nessa exibição que satisfazem a fórmula serão retornados.</p> <p>Por exemplo, para incluir apenas registros em que Nome não esteja vazio, transmita em:<code> NOT({Name} = '')</code></p> <p>Para saber mais, consulte as informações sobre referências de campo de fórmula na documentação de suporte do Airtable.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Assistir Respostas

Este módulo acionador inicia um cenário quando um formulário é enviado.

>[!NOTE]
>
>Essa funcionalidade está disponível somente para o Airtable Pro Plan pago.

O URL do webhook precisa ser gerado no Workfront Fusion e adicionado para configuração de formulário no Airtable.

1. Adicione o módulo Observar novas respostas ao seu cenário do Workfront Fusion.
1. Gere e copie o URL do webhook.

   <!--For instructions, see [ (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->

1. Faça logon em sua conta do Airtable.
1. Abra a Base e a tabela que deseja usar para o formulário e crie uma exibição de Formulário.
1. Defina o formulário conforme necessário, role para baixo no formulário e ative a opção Redirecionar para URL após o formulário ser enviado.
1. Insira a URL do Webhook gerada na etapa 2 para a caixa de diálogo exibida e adicione ?record_id={record_id} logo após a URL do webhook para incluir a ID do Registro na saída do módulo e, em seguida, clique em Salvar. O URL resultante será, por exemplo, semelhante a:
1. Volte para o cenário do Workfront Fusion e execute o módulo Watch Responses somente para carregar campos do Airtable e poder mapear esses campos para os outros módulos.
1. Envie o formulário no Airtable onde a opção Redirecionar para URL após o envio do formulário está habilitada e a URL do Webhook adicionada (etapa 6 acima).

   O módulo Watch Responses é acionado e os dados desejados são carregados.

1. Adicione o módulo Airtable > Get a Record logo após o módulo Airtable > Watch Responses e mapeie o record_id para o campo Record ID.

Agora, sempre que o formulário for enviado, o módulo Observar respostas no cenário do Workfront Fusion será acionado e o módulo Obter um registro retornará os detalhes do formulário enviado.

#### Fazer uma chamada de API

#### Chamada de API personalizada

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Airtable]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Airtable].

A ação é baseada no tipo de entidade (tipo de objeto Alocadia) especificado.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Conexão</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Airtable ao Workfront Fusion, consulte <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Conectar o Airtable ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Insira um caminho relativo para <code>https://api.airtable.com/</code>. Exemplo: <code>v0/{base}/{table}</code> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Método</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cabeçalhos</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sequência de consulta</td> 
   <td> <p>Adicione a consulta para a chamada da API no formato de uma Chave e Valor</p> </td> 
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
