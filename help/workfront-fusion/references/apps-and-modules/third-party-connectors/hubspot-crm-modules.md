---
title: Módulos CRM do HubSpot
description: Os  [!DNL Adobe Workfront Fusion] módulos CRM do HubSpot permitem que você monitore eventos, registros, contatos, compromissos, envios de arquivos e formulários ou crie, recupere, atualize e exclua registros, contatos, compromissos, eventos ou arquivos na sua conta [!DNL HubSpot CRM] do.
author: Becky
feature: Workfront Fusion
exl-id: b8a1bbcd-337e-4c92-a1a6-d6d4bab1f440
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '5661'
ht-degree: 0%

---

# [!DNL HubSpot CRM] módulos

Os módulos do [!DNL Adobe Workfront Fusion] [!DNL HubSpot CRM] permitem que você monitore eventos, registros, contatos, compromissos, envios de arquivos e formulários ou crie, recupere, atualize e exclua registros, contatos, compromissos, eventos ou arquivos na sua conta do [!DNL HubSpot CRM].

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

Para usar módulos [!DNL HubSpot CRM], você deve ter uma conta [!DNL HubSpot CRM].

## Informações da API CRM do HubSpot

O conector HubSpot CRM usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://api.hubapi.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2.0.14</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!DNL Adobe Workfront Fusion] a [!DNL HubSpot CRM]

Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte [Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Ao configurar uma conexão, selecione o tipo de conexão **HubSpot CRM**. O tipo HubSpot CRM (obsoleto) é compatível com conexões existentes, mas não recomendamos usá-lo para criar novas conexões.

## [!DNL HubSpot CRM] módulos e seus campos

Ao configurar módulos do [!DNL Hubspot CRM], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Hubspot CRM] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Objetos do CRM](#crm-objects)
* [Registros (Transações, Contatos e Empresas)](#records-deals-contacts-and-companies)
* [Contatos](#contacts)
* [Transações](#deals)
* [Empresas](#companies)
* [Envolvimentos](#engagements)
* [Eventos e notificações](#events-and-notifications)
* [Arquivos](#files)
* [Tarefas](#tasks)
* [Usuários](#users)
* [Tíquetes](#tickets)
* [Formulários](#forms)
* [Redes sociais (transmissão)](#social-media-broadcast)
* [Publicações do blog](#blog-posts)
  <!--* [Workflows]-->
* [Assinaturas](#subscriptions)
  <!--* [Associations](#associations)-->
* [Outro](#other)

+++**Objetos do CRM**

### Objetos do CRM

* [Pesquisar objetos do CRM](#search-for-crm-objects)
* [Observar objetos do CRM](#watch-crm-objects)

#### [!UICONTROL Search for CRM Objects]

Este módulo de pesquisa procura objetos do CRM por propriedades personalizadas ou por consulta. Para pesquisar produtos ou itens de linha, use uma conexão especial com um escopo personalizado necessário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de itens que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type to Search]</td> 
   <td>Selecione o tipo de objeto CRM do Hubspot que você deseja pesquisar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. Os campos disponíveis dependem do objeto selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by] </td> 
   <td> <p>Selecione como deseja filtrar a pesquisa</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Insira ou mapeie a consulta</p> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Insira os grupos ou filtros para sua pesquisa.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Clique em para classificar os resultados. Se você optar por classificar os resultados, serão exibidos os seguintes campos. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Property name]</strong> </p> <p>Selecione a propriedade pela qual deseja classificar os resultados</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>Escolha se deseja classificar os resultados em uma direção crescente ou decrescente.</p> </li> 
    </ul> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Iniciar deslocamento</td> 
    <td>Insira ou mapeie a ID do primeiro item para o qual deseja recuperar detalhes. Esse módulo retorna até 5000 resultados por vez. Definir um deslocamento de início permite recuperar itens diferentes dos primeiros 5000. Se o deslocamento de início for 5000, o módulo retornará os itens 5000-9999.</td> 
   </tr>
 </tbody> 
</table>

#### Observar objetos do CRM

Este módulo de acionador inicia um cenário quando um objeto do CRM é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de itens que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object type to search]</td> 
   <td> <p>Selecione o tipo de objeto que deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selecione as propriedades que deseja incluir na saída deste módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created/Updated]</td> 
   <td>Selecione se deseja observar objetos criados (novos) ou atualizados (modificados).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by]</td> 
   <td>Você pode adicionar um filtro para garantir que o cenário comece somente quando determinadas condições forem atendidas.<ul><li><b>Query</b><p>Insira a consulta pela qual deseja filtrar.</li><li><b>Propriedades</b><p>Para cada propriedade que você deseja usar para filtrar resultados, clique em <b>Adicionar item</b> e insira o nome da propriedade, o operador e o valor da propriedade.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Registros (Transações, Contatos e Empresas)**

### Registros (Transações, Contatos e Empresas)

* [Criar um registro](#create-a-record)
* [[!UICONTROL Create a Record (Legacy)]](#create-a-record-legacy)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Get a Record]](#get-a-record)
* [[!UICONTROL Get a Record Property]](#get-a-record-property)
* [Listar Registros](#list-records)
* [[!UICONTROL Update a Record]](#update-a-record)
* [[!UICONTROL Watch Records]](#watch-records)

#### Criar um registro

Este módulo de ação cria um contato, uma empresa ou uma negociação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Para cada propriedade que você deseja adicionar ao criar o registro, selecione o grupo no qual a propriedade é encontrada. O grupo de propriedades será aberto e você poderá preencher o valor das propriedades. Os grupos de propriedades e as propriedades disponíveis dependem do tipo de registro que você deseja criar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Record (Legacy)]

Este módulo de ação cria um contato, uma empresa ou uma negociação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Preencha quaisquer propriedades que deseja definir para o registro. Os campos disponíveis dependem do tipo de registro que você deseja criar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Record]

Este módulo de ação exclui um contato, uma empresa ou uma negociação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro que deseja deletar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira a ID do contato, empresa ou negócio que deseja excluir. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Record]

Este módulo de ação obtém detalhes de um contato, de uma empresa ou de uma transação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro.</p> 
    <ul> 
     <li>[!UICONTROL Contact]</li> 
     <li>[!UICONTROL Company] </li> 
     <li>[!UICONTROL Deal]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td>Se você estiver recebendo um contato, selecione se deseja identificá-lo por ID ou por endereço de email.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira a ID do contato, empresa ou negócio que você deseja recuperar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Insira o endereço de email do contato cujos detalhes você deseja recuperar. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Record Property]

Esse módulo de ação obtém metadados para uma propriedade de registro específica por seu nome (interno).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro que tem a propriedade para a qual você deseja recuperar metadados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property Name]</td> 
   <td>Selecione a propriedade para a qual deseja recuperar metadados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Option ID]</td> 
   <td> <p> Algumas propriedades têm um conjunto de opções disponíveis que um usuário pode selecionar como o valor da propriedade. Insira a ID da opção que representa o valor da propriedade que você deseja recuperar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Listar Registros

Este módulo de pesquisa retorna uma lista de contatos, empresas ou ofertas. A saída é limitada a 5.000 contatos, 12.500 empresas ou 12.500 ofertas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja retornar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selecione as propriedades que deseja incluir na saída deste módulo.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr>

</tbody> 
</table>

#### [!UICONTROL Update a Record]

Este módulo de ação atualiza um contato, uma empresa ou um negócio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td> <p>Se você estiver recebendo um contato, selecione como deseja identificar o registro:</p> 
    <ul> 
     <li> <p>[!UICONTROL ID]</p> </li> 
     <li> <p>[!UICONTROL Email]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira a ID do contato, empresa ou negócio que você deseja atualizar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Insira o endereço de email do contato cujos detalhes você deseja atualizar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Preencha quaisquer propriedades que deseja definir para o registro. Os campos disponíveis dependem do tipo de registro que você deseja criar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Records]

Este módulo de acionador inicia um cenário quando um contato, empresa ou negócio foi modificado ou criado nos últimos 30 dias. A saída é limitada a 10.000 registros.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro que tem a propriedade que você deseja observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Selecione se deseja observar registros modificados recentemente ou criados recentemente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selecione as propriedades que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Contatos**

### Contatos

* [[!UICONTROL Add Contacts to a List]](#add-contacts-to-a-list)
* [Criar/atualizar um contato](#createupdate-a-contact)
* [[!UICONTROL Create/Update a Contact (Legacy)]](#createupdate-a-contact-legacy)
* [[!UICONTROL Create/Update a Group of Contacts]](#createupdate-a-group-of-contacts)
* [[!UICONTROL List Contacts]](#list-contacts)
* [[!UICONTROL List Contacts of a Company]](#list-contacts-of-a-company)
* [[!UICONTROL Merge contacts]](#merge-contacts)
* [[!UICONTROL Remove a Contact from a List]](#remove-a-contact-from-a-list)
* [[!UICONTROL Search for Contacts]](#search-for-contacts)
* [Assistir Contatos Adicionados a uma Lista](#watch-contacts-added-to-a-list)

#### [!UICONTROL Add Contacts to a List]

Este módulo adiciona registros de contato que já foram criados no sistema a uma lista de contatos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Selecione a ID da lista à qual você deseja adicionar o contato. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs/Emails] </td> 
   <td> <p>Selecione como deseja identificar os contatos que deseja adicionar à lista:</p> 
    <ul> 
     <li> <p>[!UICONTROL IDs]</p> <p>Adicione as IDs dos contatos que deseja adicionar à lista.</p> </li> 
     <li> <p>[!UICONTROL Emails]</p> <p>Adicione os endereços de email dos contatos que deseja adicionar à lista.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Criar/atualizar um contato

Este módulo de ação cria um contato se ele não existir em um portal. Se o contato não existir no portal, este módulo o atualizará com os valores fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Para cada propriedade que você deseja adicionar ao criar o contato, selecione o grupo no qual a propriedade é encontrada. O grupo de propriedades será aberto e você poderá preencher os valores das propriedades.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Contact (Legacy)]

Cria um contato se ele ainda não existir em um portal ou o atualiza com os valores de propriedade mais recentes se ele existir em um portal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Preencha todas as propriedades que deseja definir ou atualizar para o contato. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Group of Contacts]

Cria um grupo de contatos ou os atualiza quando já existem. O desempenho é melhor quando o tamanho do lote é limitado a 100 contatos ou menos. As alterações feitas por meio desse endpoint são processadas de forma assíncrona, portanto, pode levar vários minutos para que as alterações sejam aplicadas a registros de contato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Batch of Contacts to Create/Update] </td> 
   <td> <p>Adicione o lote de contatos.</p> <p>Clique em <strong>[!UICONTROL Add item]</strong> para adicionar um novo contato. Na janela exibida, insira ou mapeie as seguintes informações:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search Type]</strong> </p> <p>Selecione como deseja identificar o contato:</p> 
      <ul> 
       <li> <p>[!UICONTROL ID]</p> <p>Insira a ID do contato que você deseja criar ou atualizar. </p> </li> 
       <li> <p>[!UICONTROL Email]</p> <p>Insira o endereço de email do contato que deseja criar ou atualizar. </p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Preencha todas as propriedades que deseja definir ou atualizar para o contato.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Contacts]

Retorna todos os contatos que foram criados no portal. A saída é limitada a 5000 contatos. Para listar contatos anteriores ou seguintes, você pode usar o parâmetro [!UICONTROL advanced] para deslocar a lista.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>O número máximo de contatos [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID de contato [deslocamento de início] </td> 
    <td>Insira ou mapeie a ID do usuário que deseja iniciar a lista. Por exemplo, definir a ID de contato como a ID do 101º contato permitirá que o módulo liste os contatos 101-5100 em vez de 1-5000. </td> 
   </tr>
 </tbody> 
</table>

#### [!UICONTROL List Contacts of a Company]

Recupera uma lista de contatos na empresa. A saída é limitada a 5000 contatos. Para listar contatos anteriores ou seguintes, você pode usar o parâmetro [!UICONTROL advanced] para deslocar a lista.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Informe a ID da empresa cujos contatos você deseja listar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>O número máximo de contatos [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID de contato [deslocamento de início] </td> 
    <td>Insira ou mapeie a ID do usuário que deseja iniciar a lista. Por exemplo, definir a ID de contato como a ID do 101º contato permitirá que o módulo liste os contatos 101-5100 em vez de 1-5000. </td> 
   </tr>
 </tbody> 
</table>

#### [!UICONTROL Merge contacts]

Este módulo de ação mescla contatos

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 1] </td> 
   <td>Digite a ID de um dos contatos que você deseja mesclar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 2] </td> 
   <td>Insira a ID do outro contato que você deseja mesclar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a Contact from a List]

Remove um contato de uma lista de contatos.

>[!NOTE]
>
>Não é possível remover contatos manualmente de uma lista dinâmica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Selecione a ID da lista da qual deseja remover o contato. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID] </td> 
   <td>Digite a ID do contato que você deseja remover da lista. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Contacts]

Recupera uma lista de contatos usando a consulta de pesquisa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Insira a consulta de pesquisa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Insira ou mapeie o número máximo de contatos que [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch contacts added to a list]

Este módulo de acionamento inicia um cenário quando um novo contato é adicionado a uma lista. Isso está disponível somente para usuários com uma conta de marketing paga.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Insira ou mapeie a ID da lista que contém os contatos que você deseja assistir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selecione as propriedades que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Ofertas**

### Transações

* [[!UICONTROL Get a Deal's CRM Pipeline]](#get-a-deals-crm-pipeline)
* [[!UICONTROL List Deal/Ticket Pipelines]](#list-dealticket-pipelines)

#### [!UICONTROL Get a Deal's CRM Pipeline]

Retorna um pipeline de negociação específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pipeline ID] </td> 
   <td>Insira ou mapeie a ID do pipeline do qual deseja recuperar detalhes. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stage ID] </td> 
   <td>Insira ou mapeie a ID do estágio para o qual deseja recuperar detalhes. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Deal/Ticket Pipelines]

Retorna todos os pipelines de negócios e tíquetes de um determinado portal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type] </td> 
   <td>Selecione se deseja listar ofertas ou tickets.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Empresas**

### Empresas

#### [!UICONTROL Search for Companies by domain]

Recupera uma lista de empresas com base em uma correspondência exata com a propriedade de domínio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Domain] </td> 
   <td>Insira o domínio das empresas que você deseja pesquisar, como <code>[!DNL hubspot].com</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>O número máximo de empresas [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Envolvimentos**

### Envolvimentos

* [Associar um compromisso a um objeto do CRM](#associate-an-engagement-with-a-crm-object)
* [Criar um compromisso](#create-an-engagement)
* [Excluir um Compromisso](#delete-an-engagement)
* [Observar envolvimentos](#watch-engagements)

#### Associar um compromisso a um objeto do CRM

Este módulo de ação associa um envolvimento a um contato, empresa ou negócio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selecione o tipo de registro do CRM ao qual você deseja associar um envolvimento. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Engagement ID]</td> 
  <td>Insira ou mapeie a ID do envolvimento que você deseja associar ao objeto.</td> 
   </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
  <td>Insira ou mapeie a ID do registro ao qual você deseja associar o envolvimento.</td> 
   </tr> 
 </tbody> 
</table>

#### Criar um compromisso

Este módulo de ação cria um envolvimento (como uma observação, tarefa ou atividade) com um objeto CRM no HubSpot. Envolvimentos são qualquer interação com um contato que deve ser registrado no CRM.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Is Active?]</td> 
   <td>Habilite esta opção se o novo engajamento estiver ativo quando for criado. Um envolvimento deve estar ativo para aparecer na linha do tempo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
  <td>Selecione o tipo de envolvimento que deseja criar.
  <ul>
  <li><b>Email</b><p></p>Continue para <a href="#email-metadata" class="MCXref xref" >Metadados de email</a>.</p></li>
  <li><b>Chame</b><p>Continue para <a href="#call-metadata" class="MCXref xref" >Chamar metadados</a>.</p></li>
  <li><b>Encontro</b><p>Continue para <a href="#meeting-fields" class="MCXref xref" >Campos de reunião</a>.</p></li>
  <li><b>Tarefa</b><p>Continue para <a href="#task-fields" class="MCXref xref" >Campos de tarefa</a>.</p></li>
  <li><b>Nota</b><p>No campo Corpo, informe o texto da nota.</p></li>
  </ul>
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Carimbo de data e hora</td> 
   <td>Insira ou mapeie um carimbo de data e hora para o envolvimento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do proprietário</td> 
   <td>Insira ou mapeie a ID do proprietário da pessoa à qual o compromisso será atribuído.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UID</td> 
   <td>Insira ou mapeie uma ID para o envolvimento, que pode ser usada entre tipos de objeto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do portal</td> 
   <td>Insira ou mapeie a ID do portal. Isso é útil se sua organização tiver vários portais.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Contatos Associados</td> 
   <td>Para cada contato ao qual você deseja associar este compromisso, clique em <b>Adicionar item</b> e insira a ID do Contato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Empresas associadas</td> 
   <td>Para cada empresa à qual você deseja associar este compromisso, clique em <b>Adicionar item</b> e insira a ID da Empresa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ofertas associadas</td> 
   <td>Para cada negócio ao qual você deseja associar este compromisso, clique em <b>Adicionar item</b> e insira a ID do Contrato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tíquetes associados</td> 
   <td>Para cada tíquete ao qual você deseja associar este compromisso, clique em <b>Adicionar item</b> e insira a ID do Tíquete.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anexos</td> 
   <td>Para cada anexo ao qual você deseja associar este compromisso, clique em <b>Adicionar item</b> e insira a ID do arquivo que você deseja anexar.</td> 
  </tr> 
 </tbody> 
</table>

##### Metadados de email

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL From > Email]</p> </td> 
   <td> <p>Insira ou mapeie o endereço de email do qual o email será enviado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First Name]</td> 
   <td>Insira ou mapeie o nome da pessoa da qual o email será enviado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Last Name]</td> 
  <td>Insira ou mapeie o sobrenome da pessoa da qual o email será enviado.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Até</td> 
   <td>Para cada endereço de email para o qual deseja enviar o email, clique em <b>Adicionar item</b> e insira ou mapeie o endereço de email.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cc</td> 
   <td>Para cada endereço de email para o qual você deseja Cc, clique em <b>Adicionar item</b> e insira ou mapeie o endereço de email.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cco</td> 
   <td>Para cada endereço de email para o qual você deseja Cco, clique em <b>Adicionar item</b> e insira ou mapeie o endereço de email.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Assunto</td> 
   <td>Inserir ou mapear o texto do assunto do email</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML</td> 
   <td>Para enviar um email formatado em HTML, insira ou mapeie o corpo do email, incluindo as tags HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Texto</td> 
   <td>Para enviar um email somente texto, insira ou mapeie o texto do corpo do email.</td> 
  </tr> 
 </tbody> 
</table>

##### Metadados da chamada

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL To Number]</p> </td> 
   <td> <p>Insira ou mapeie o número de telefone para o qual a chamada será feita.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From Number]</td> 
   <td>Insira ou mapeie o número de telefone a partir do qual a chamada será feita.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
  <td>Selecione o status da chamada.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td>Insira ou mapeie os detalhes ou as notas da chamada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID externa</td> 
   <td>Este campo representa a ID interna de uma chamada feita no HubSpot. Não requer nenhuma ação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Duração</td> 
   <td>Insira ou mapeie o comprimento da chamada em milissegundos</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da conta externa</td> 
   <td>Este campo representa a ID de conta interna de uma chamada feita no HubSpot. Não requer nenhuma ação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL de Gravação</td> 
   <td>Insira ou mapeie o URL do arquivo de gravação.</td> 
  </tr> 
 </tbody> 
</table>

##### Campos de reunião

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Title]</p> </td> 
   <td> <p>Insira ou mapeie o título ou o assunto da reunião.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Insira ou mapeie o texto da descrição ou dos detalhes da reunião.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Time]</td> 
  <td>Informe ou mapeie a hora de início da reunião como um timestamp UNIX.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Horário de término</td> 
   <td>Informe ou mapeie a hora de término da reunião como um timestamp UNIX.</td> 
  </tr> 
 </tbody> 
</table>

##### Campos de tarefa

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Subject]</p> </td> 
   <td> <p>Insira ou mapeie o título ou o assunto da tarefa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Insira ou mapeie o texto da descrição ou dos detalhes da tarefa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Status</td> 
   <td>Selecione o status da tarefa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL For Object Type]</td> 
  <td>Insira <code>CONTACT</code> ou <code>COMPANY</code>.
  </td> 
   </tr> 
 </tbody> 
</table>

#### Excluir um Compromisso

Este módulo de ação exclui um envolvimento por sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Insira ou mapeie a ID do compromisso que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Observar envolvimentos

Este módulo de acionamento inicia um cenário quando um novo envolvimento é criado em um portal. Esse módulo retorna apenas registros criados nos últimos 30 dias ou os 10.000 registros criados mais recentemente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>O número máximo de empresas [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>Insira ou mapeie a data mais antiga para a qual você deseja assistir aos eventos. Use o formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Eventos e notificações**

### Eventos e notificações

* [Criar/atualizar um evento de linha do tempo](#create--update-a-timeline-event)
* [Listar Tipos de Evento de Linha do Tempo](#list-timeline-event-types)
* [Assistir a eventos do calendário](#watch-calendar-events)
* [Observar notificações](#watch-notifications)

#### Criar/atualizar um evento de linha do tempo

Este módulo de ação cria ou atualiza um evento de linha do tempo. Este módulo pode ser usado somente com uma conexão de desenvolvedor que inclua seu identificador de usuário, sua chave da API HubSpot, a ID do cliente e o segredo do cliente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Insira ou mapeie a ID do aplicativo ao qual este evento pertence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>Insira ou mapeie uma ID para este evento. IDs de evento não são geradas pelo sistema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Type ID]</td> 
   <td>Insira ou mapeie a ID do tipo de evento deste evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Insira ou mapeie o endereço de email do contato para o qual você está criando o evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object ID]</td> 
   <td>Insira ou mapeie a ID do contato para o qual você está criando o evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp]</td> 
   <td>Insira ou mapeie o carimbo de data e hora desse evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom data]</td> 
   <td>Para cada item de dados personalizados que você deseja adicionar a este evento, clique em <b>Adicionar item</b> e insira o nome e o valor do item.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar Tipos de Evento de Linha do Tempo

Este módulo de pesquisa retorna uma lista de todos os eventos da linha do tempo de um aplicativo específico. Este módulo pode ser usado somente com uma conexão de desenvolvedor que inclua seu identificador de usuário, sua chave da API HubSpot, a ID do cliente e o segredo do cliente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Insira ou mapeie a ID do aplicativo ao qual esses eventos pertencem. </td> 
  </tr> 
 </tbody> 
</table>

#### Assistir a eventos do calendário

Este módulo de acionamento inicia um cenário quando um novo evento é adicionado a um calendário. Inclui até 500 tarefas no intervalo entre as datas de início e término. Este módulo pode ser usado somente com uma conexão de desenvolvedor que inclua seu identificador de usuário, sua chave da API HubSpot, a ID do cliente e o segredo do cliente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Events Type]</td> 
   <td>Selecione se deseja assistir a eventos sociais, de conteúdo ou a todos os eventos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Insira ou mapeie a data de início.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Insira ou mapeie a data final.</td> 
  </tr> 
 </tbody> 
</table>

#### Observar notificações

Este módulo de acionamento inicia um cenário quando uma nova notificação sobre alterações é enviada.  Inclui até 500 tarefas no intervalo entre as datas de início e término. Este módulo pode ser usado somente com uma conexão de desenvolvedor que inclua seu identificador de usuário, sua chave da API HubSpot, a ID do cliente e o segredo do cliente. Você pode ter apenas um URL de webhook por aplicativo de desenvolvedor no HubSpot.

Para criar um webhook para este módulo, clique em **Adicionar** ao lado do campo de webhook e preencha os seguintes campos:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Insira a ID do aplicativo que deseja usar para este webhook. Você pode encontrar a ID em seu portal do desenvolvedor HubSpot.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscriptions]</td> 
   <td> <p>Para cada tipo de notificação que você deseja observar, clique em <b>Adicionar item</b> e selecione o tipo de assinatura.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Force to Remove Old Subscriptions]</td> 
   <td>Habilite esta opção para desanexar ou excluir assinaturas antigas anexadas a este webhook.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Arquivos**

### Arquivos

* [[!UICONTROL Create a Folder]](#create-a-folder)
* [Excluir um arquivo](#delete-a-file)
* [[!UICONTROL Delete a Folder]](#delete-a-folder)
* [Listar arquivos](#list-files)
* [[!UICONTROL Move a File]](#move-a-file)
* [Carregar um arquivo](#upload-a-file)
* [Observar arquivos](#watch-files)

#### [!UICONTROL Create a Folder]

Este módulo cria uma pasta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Name] </td> 
   <td>Insira ou mapeie um nome para a nova pasta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID] </td> 
   <td>Selecione a ID da pasta principal da pasta que você está criando. </td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um arquivo

Esse módulo de ação exclui permanentemente um arquivo e todos os dados e miniaturas relacionados do gerenciador de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Insira ou mapeie a ID do arquivo que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Folder]

Marca uma pasta como excluída.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID da pasta que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar arquivos

Este módulo de pesquisa retorna uma lista de arquivos armazenados no gerenciador de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Insira ou mapeie a ID da pasta que contém os arquivos que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Para incluir somente arquivos que contenham caracteres específicos no nome do arquivo, insira ou mapeie os caracteres que deseja que o nome do arquivo inclua.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

Move um arquivo para outra pasta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID] </td> 
   <td>Insira ou mapeie a ID do arquivo que deseja mover. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Selecione a ID da pasta para onde deseja mover o arquivo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Insira um nome para o arquivo movido.</td> 
  </tr> 
 </tbody> 
</table>

#### Carregar um arquivo

Este módulo de ação faz upload de um arquivo para o gerenciador de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access type] </td> 
   <td>Selecione se você deseja que o arquivo seja privado, público, mas não indexável, ou público e indexável. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Selecione a ID da pasta na qual deseja fazer upload do arquivo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Ative essa opção para substituir o arquivo se ele já existir na pasta.</td> 
  </tr> 
 </tbody> 
</table>

### Observar arquivos

Este módulo de acionamento inicia um cenário quando um novo arquivo é salvo no gerenciador de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Insira ou mapeie a ID da pasta que contém os arquivos que você deseja observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Para incluir somente arquivos que contenham caracteres específicos no nome do arquivo, insira ou mapeie os caracteres que deseja que o nome do arquivo inclua.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tarefas**

### Tarefas

* [Criar uma tarefa de calendário](#create-a-calendar-task)
* [Excluir uma tarefa do calendário](#create-a-calendar-task)
* [Assistir a Eventos de Tarefas](#watch-task-events)

#### Criar uma tarefa do Calendário

Este módulo de ação cria uma nova tarefa para um calendário. A conexão usada neste módulo deve usar as credenciais de um usuário com uma conta de Marketing paga.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Insira ou mapeie um nome para a nova tarefa do calendário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Insira ou mapeie uma descrição para a nova tarefa do calendário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td>Insira ou mapeie a ID do proprietário do usuário atribuído a esta tarefa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Date]</td> 
   <td>Insira ou mapeie a data para esta tarefa.<p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Selecione o tipo de evento.<ul><li><b>Publicação do blog</b><p>Insira a ID do grupo de conteúdo. Esta é a ID da página do blog.</p></li><li><b>Email</b><p>Insira ou mapeie o caminho para o modelo de email que deseja usar.</li><li><b>Landing Page</b><p>Insira ou mapeie o caminho para o modelo de página de aterrissagem que deseja usar.</li><li><b>Personalizado</b></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Digite se o evento está no estado "Tarefa" ou "Concluída".</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign GUID]</td> 
   <td>Insira ou mapeie a ID do HubSpot interno da campanha da qual este evento faz parte.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir uma tarefa do calendário

Este módulo de ação exclui uma tarefa de calendário. A conexão usada neste módulo deve usar as credenciais de um usuário com uma conta de Marketing paga.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID da tarefa que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Assistir a Eventos de Tarefas

Este módulo de acionamento inicia um cenário quando há um novo evento de tarefa em um calendário. A conexão usada neste módulo deve usar as credenciais de um usuário com uma conta de Marketing paga. O módulo retorna até 500 eventos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Insira ou mapeie a data mais antiga para a qual você deseja assistir aos eventos. Use o formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Insira ou mapeie a data mais recente para a qual você deseja assistir aos eventos. Use o formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Usuários**

### Usuários

* [Obter um Proprietário](#get-an-owner)
* [Proprietários da lista](#list-owners)

#### Obter um Proprietário

Este módulo de ação retorna detalhes de um proprietário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td> <p>Insira ou mapeie a ID do proprietário para o qual deseja retornar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Proprietários da lista

Este módulo de pesquisa retorna uma lista de todos os proprietários em uma conta HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tíquetes**

### Tíquetes

<!--* [Create a Ticket]-->
* [Excluir um tíquete](#delete-a-ticket)
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->

<!-- Create a Ticket Need to find a working connection-->

#### [!UICONTROL Delete a Ticket]

Exclui um tíquete existente por sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Digite a ID do ticket que você deseja excluir. </td> 
  </tr> 
 </tbody> 
</table>

<!-- Get a Ticket  Need to find a working connection-->

<!-- List Tickets  Need to find a working connection-->

&lt;!— Atualizar um tíquete Necessidade de encontrar uma conexão operacional—>

<!-- Watch Tickets Need to find a working connection-->

+++

+++**Forms**

### Formulários

* [Obter um arquivo carregado por meio do formulário](#get-a-file-uploaded-via-form)
* [Listar Forms](#list-forms)
  <!--* [Submit Data to a Form]-->
  <!--* [Watch Submissions for a Form]-->

#### Obter um arquivo carregado por meio do formulário

Este módulo de ação retorna um arquivo que foi carregado por meio de um formulário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td>Insira ou mapeie o URL do arquivo que deseja recuperar. Isso pode ser encontrado nos metadados do formulário.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar Forms

Este módulo de ação retorna todos os formulários que foram criados na conta associada à conexão usada para este módulo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de formulários que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Submit Data to a Form Need to find a working connection-->



&lt;!—#### Assista aos envios para um formulário—É necessário encontrar uma conexão ativa>—>

+++

+++**Mídia social (Difusão)**

### Redes sociais (transmissão)

* [Cancelar uma mensagem de transmissão](#cancel-a-broadcast-message)
* [Criar uma mensagem de transmissão](#create-a-broadcast-message)
* [Assistir Mensagens de Difusão](#watch-broadcast-messages)

#### Cancelar uma mensagem de transmissão

Esse módulo de ação cancela uma transmissão agendada, como um tweet ou uma publicação do Facebook.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Insira ou mapeie a ID da transmissão que você deseja cancelar.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar uma mensagem de transmissão

Esse módulo de ação cria e publica imediatamente uma mensagem no canal de mídia social especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel ID]</td> 
   <td>Insira ou mapeie a ID do canal que deseja usar para esta transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Insira ou mapeie um título para esta transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Insira ou mapeie o texto da transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Photo URL]</td> 
   <td>Insira ou mapeie o URL de uma foto que você deseja incluir na transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thumbnail URL]</td> 
   <td>Insira ou mapeie o URL de uma miniatura que você deseja usar para esta transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trigger at]</td> 
   <td>Insira ou mapeie a data e a hora em que deseja que a transmissão seja enviada. Se isso for deixado em branco, a transmissão será enviada imediatamente.<p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Assistir Mensagens de Difusão

Esse módulo de acionador inicia um cenário quando uma mensagem é postada do HubSpot para o canal de rede social especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de itens que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Status]</td> 
   <td>Para iniciar o cenário somente quando a mensagem estiver em um status específico, selecione o status.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Channel]</td> 
   <td>Para iniciar o cenário somente quando a mensagem estiver em um canal específico, selecione o canal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Para iniciar o cenário somente quando a mensagem for em ou após uma data específica, insira ou mapeie a data no formato <code>MM/DD/YYYY</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Publicações do blog**

### Publicações no blog

<!--* [Create a Blog Post]-->
* [Excluir uma postagem do blog](#delete-a-blog-post)
  <!--* [List Blog Posts]-->
* [Publish/Cancelar publicação de uma postagem do blog](#publish--unpublish-a-blog-post)
  <!--* [Watch Blog Posts]-->

<!--
#### Create a Blog Post May need connection
-->


#### Excluir uma publicação do blog

Este módulo de ação exclui uma única publicação de blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID da publicação do blog que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### List Blog Posts May need connection

This search module retrieves posts from a HubSpot blog.-->

#### Publish / Desfazer a publicação de uma postagem de blog

Este módulo de ação agenda ou cancela a publicação de uma publicação de blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID da publicação do blog que você deseja agendar ou cancelar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Selecione se deseja agendar a postagem de blog ou cancelar uma postagem de blog agendada anteriormente.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Watch Blog PostsMay need connection-->

+++

<!--+++**Workflows**>

<!--### Workflows May need connection

#### Add a Contact to a Workflow


#### Remove a Contact from a Workflow

-->

<!--+++-->

+++**Assinaturas**

### Assinaturas

* [Atualizar assinatura de email](#update-email-subscription)
* [Assistir Linha do Tempo de Assinaturas de um Portal](#watch-subscriptions-timeline-for-a-portal)

#### Atualizar assinatura de email

Este módulo de ação atualiza uma assinatura de email no HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Insira ou mapeie o endereço de email da assinatura que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Statuses]</td> 
   <td>Para cada status para o qual você deseja atualizar a inscrição, clique em <b>Adicionar item</b> e insira a ID do status, e se o endereço de email será inscrito nesse status.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Status]</td> 
   <td>Para registrar a base legal desta assinatura para o GDPR, selecione o status legal desta assinatura.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Basis Explanation]</td> 
   <td>Para adicionar uma observação sobre a base legal desta assinatura do GDPR, insira ou mapeie o texto da observação.</td> 
  </tr> 
 </tbody> 
</table>

#### Assistir Linha do Tempo de Assinaturas de um Portal

Esse módulo de acionamento inicia um cenário quando uma nova assinatura de linha do tempo de email é adicionada ao portal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de itens que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Timestamp]</td> 
   <td>Para retornar resultados de em ou após uma data específica, insira a data no formato <code>MM/DD/YYYY.</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Timestamp]</td> 
   <td>Para retornar resultados de uma data específica ou antes dela, insira a data no formato <code>MM/DD/YYYY.</code></td> 
  </tr> 
 </tbody> 
</table>

+++

<!--+++**Associations**-->

<!--### Associations-->

<!--#### Associate CRM Objects  May need connection

This action module associates two CRM objects.-->

<!--#### Associate Multiple CRM Objects  May need connection-->



<!--#### Delete an Association May need connection-->



<!--#### Delete Multiple Associations between CRM Objects May need connection-->



<!--#### List Associations for a CRM Object May need connection-->

<!--+++-->

+++**Outros**

### Outro

#### [!UICONTROL Make an API Call]

Permite executar uma chamada de API personalizada.

>[!NOTE]
>
>Os seguintes endpoints foram descontinuados na API HubSpot em 31 de agosto de 2023 e não podem mais ser usados em módulos do Fusion.
>
>* Listar eventos de conteúdo
>* Listar eventos sociais
>* Listar eventos de tarefas do calendário
>* Listar todos os eventos do calendário
>* Criar tarefa de calendário
>* Obter tarefa de calendário por ID
>* Atualizar tarefa de calendário
>* Excluir uma tarefa de calendário

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo para https://api.hubapi.com/. Por exemplo, /contacts/v1/lists/all/contacts/all</p> <p>Para obter a lista de pontos de extremidade disponíveis, consulte a <a href="https://legacydocs.hubspot.com/docs/overview">[!DNL HubSpot] Documentação da API</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método HTTP que deseja usar:</p> <p>[!UICONTROL GET]</p> <p>para recuperar informações de uma entrada.</p> <p>[!UICONTROL POST]</p> <p>para criar uma nova entrada.</p> <p>[!UICONTROL PUT]</p> <p>para atualizar/substituir uma entrada existente.</p> <p>[!UICONTROL PATCH]</p> <p>para fazer uma atualização de entrada parcial.</p> <p>[!UICONTROL DELETE]</p> <p>para deletar uma entrada.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p> Insira os cabeçalhos de solicitação desejados. Não é necessário adicionar cabeçalhos de autorização; já fizemos isso para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Insira a string de consulta da solicitação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão. Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemplo:** a chamada de API a seguir retorna todos os contatos da sua conta [!DNL HubSpot]:
>
>**URL**: `/contacts/v1/lists/all/contacts/all`
>
>**Método**: `GET`
>
>![Configuração da API do Hubspot](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-config.png)
>
>Correspondências da pesquisa podem ser encontradas na Saída do módulo em [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL contacts].
>
>No nosso exemplo, 3 contatos foram retornados:
>
>![Saída da API do Hubspot](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-output.png)

+++

## Criar um novo aplicativo

1. Faça logon em sua conta de desenvolvedor do [!DNL HubSpot].
1. Selecione a opção **[!UICONTROL Create an App]**.
1. Insira o Nome do Aplicativo e [!UICONTROL Save] a caixa de diálogo.
1. Selecione os escopos necessários para o webhook.

   Por exemplo, adicione escopos de contatos para acionar o módulo quando um novo contato for criado ou excluído.

   O [!UICONTROL contacts scope] é tudo o que você precisa para receber webhooks de contatos, ofertas e eventos da empresa.

   >[!IMPORTANT]
   >
   >Não preencha o campo [!UICONTROL Redirect URL].
