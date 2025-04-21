---
title: Módulos CRM do HubSpot
description: Os  [!DNL Adobe Workfront Fusion] módulos CRM do HubSpot permitem que você monitore eventos, registros, contatos, compromissos, envios de arquivos e formulários ou crie, recupere, atualize e exclua registros, contatos, compromissos, eventos ou arquivos na sua conta [!DNL HubSpot CRM] do.
author: Becky
feature: Workfront Fusion
exl-id: b8a1bbcd-337e-4c92-a1a6-d6d4bab1f440
source-git-commit: 0e4986d0d66b98213efabd487e6701f8385161e3
workflow-type: tm+mt
source-wordcount: '7003'
ht-degree: 0%

---

# [!DNL HubSpot CRM] módulos

Os módulos do [!DNL Adobe Workfront Fusion] [!DNL HubSpot CRM] permitem que você monitore eventos, registros, contatos, compromissos, envios de arquivos e formulários ou crie, recupere, atualize e exclua registros, contatos, compromissos, eventos ou arquivos na sua conta do [!DNL HubSpot CRM].

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
  <!--* [Workflows]()-->
* [Assinaturas](#subscriptions)
  <!--* [Associations]()-->
* [Outro](#other)

### Objetos do CRM

+++ **[!UICONTROL Pesquisar Objetos do CRM]**

Este módulo de pesquisa procura objetos do CRM por propriedades personalizadas ou por consulta. Para pesquisar produtos ou itens de linha, use uma conexão especial com um escopo personalizado necessário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de itens que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Objeto para Pesquisa]</td> 
   <td>Selecione o tipo de objeto CRM do Hubspot que você deseja pesquisar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades de saída]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. Os campos disponíveis dependem do objeto selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtrar por] </td> 
   <td> <p>Selecione como deseja filtrar a pesquisa</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Consulta]</strong> </p> <p>Insira ou mapeie a consulta</p> </li> 
     <li> <p><strong>[!UICONTROL Propriedades]</strong> </p> <p>Insira os grupos ou filtros para sua pesquisa.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classificar por]</td> 
   <td> <p>Clique em para classificar os resultados. Se você optar por classificar os resultados, serão exibidos os seguintes campos. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome da Propriedade]</strong> </p> <p>Selecione a propriedade pela qual deseja classificar os resultados</p> </li> 
     <li> <p><strong>[!UICONTROL Direção]</strong> </p> <p>Escolha se deseja classificar os resultados em uma direção crescente ou decrescente.</p> </li> 
    </ul> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Iniciar deslocamento</td> 
    <td>Insira ou mapeie a ID do primeiro item para o qual deseja recuperar detalhes. Esse módulo retorna até 5000 resultados por vez. Definir um deslocamento de início permite recuperar itens diferentes dos primeiros 5000. Se o deslocamento de início for 5000, o módulo retornará os itens 5000-9999.</td> 
   </tr>
 </tbody> 
</table>

+++

+++ **Observar objetos do CRM**

Este módulo de acionador inicia um cenário quando um objeto do CRM é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de itens que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de objeto a ser pesquisado]</td> 
   <td> <p>Selecione o tipo de objeto que deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades de Saída]</td> 
   <td>Selecione as propriedades que deseja incluir na saída deste módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criado/Atualizado]</td> 
   <td>Selecione se deseja observar objetos criados (novos) ou atualizados (modificados).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtrar por]</td> 
   <td>Você pode adicionar um filtro para garantir que o cenário comece somente quando determinadas condições forem atendidas.<ul><li><b>Query</b><p>Insira a consulta pela qual deseja filtrar.</li><li><b>Propriedades</b><p>Para cada propriedade que você deseja usar para filtrar resultados, clique em <b>Adicionar item</b> e insira o nome da propriedade, o operador e o valor da propriedade.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Registros (Transações, Contatos e Empresas)

+++ **Criar um registro**

Este módulo de ação cria um contato, uma empresa ou uma negociação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Grupos de propriedades]</td> 
   <td>Para cada propriedade que você deseja adicionar ao criar o registro, selecione o grupo no qual a propriedade é encontrada. O grupo de propriedades será aberto e você poderá preencher o valor das propriedades. Os grupos de propriedades e as propriedades disponíveis dependem do tipo de registro que você deseja criar.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar um Registro (Herdado)]**

Este módulo de ação cria um contato, uma empresa ou uma negociação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades]</td> 
   <td>Preencha quaisquer propriedades que deseja definir para o registro. Os campos disponíveis dependem do tipo de registro que você deseja criar.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Excluir um Registro]**

Este módulo de ação exclui um contato, uma empresa ou uma negociação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Registro]</td> 
   <td>Selecione o tipo de registro que deseja deletar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira a ID do contato, empresa ou negócio que deseja excluir. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ [!UICONTROL Obter um Registro]

Este módulo de ação obtém detalhes de um contato, de uma empresa ou de uma transação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro.</p> 
    <ul> 
     <li>[!UICONTROL Contato]</li> 
     <li>[!UICONTROL Empresa] </li> 
     <li>[!UICONTROL oferta]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Pesquisa]</td> 
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

+++

+++ **[!UICONTROL Obter uma Propriedade de Registro]**

Esse módulo de ação obtém metadados para uma propriedade de registro específica por seu nome (interno).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Registro]</td> 
   <td>Selecione o tipo de registro que tem a propriedade para a qual você deseja recuperar metadados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome da Propriedade]</td> 
   <td>Selecione a propriedade para a qual deseja recuperar metadados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Identificação de Opção]</td> 
   <td> <p> Algumas propriedades têm um conjunto de opções disponíveis que um usuário pode selecionar como o valor da propriedade. Insira a ID da opção que representa o valor da propriedade que você deseja recuperar.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Listar Registros**

Este módulo de pesquisa retorna uma lista de contatos, empresas ou ofertas. A saída é limitada a 5.000 contatos, 12.500 empresas ou 12.500 ofertas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td> <p>Selecione o tipo de registro que deseja retornar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades de Saída]</td> 
   <td>Selecione as propriedades que deseja incluir na saída deste módulo.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Atualizar um Registro]**

Este módulo de ação atualiza um contato, uma empresa ou um negócio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Registro]</td> 
   <td>Selecione o tipo de registro que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Pesquisa]</td> 
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
   <td role="rowheader">[!UICONTROL Propriedades]</td> 
   <td>Preencha quaisquer propriedades que deseja definir para o registro. Os campos disponíveis dependem do tipo de registro que você deseja criar.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Registros de Inspeção]**

Este módulo de acionador inicia um cenário quando um contato, empresa ou negócio foi modificado ou criado nos últimos 30 dias. A saída é limitada a 10.000 registros.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Registro]</td> 
   <td>Selecione o tipo de registro que tem a propriedade que você deseja observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pesquisar]</td> 
   <td>Selecione se deseja observar registros modificados recentemente ou criados recentemente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades de Saída]</td> 
   <td>Selecione as propriedades que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Contatos

+++ **[!UICONTROL Adicionar Contatos a uma Lista]**

Este módulo adiciona registros de contato que já foram criados no sistema a uma lista de contatos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Lista] </td> 
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

+++

+++ **Criar/Atualizar um Contato**

Este módulo de ação cria um contato se ele não existir em um portal. Se o contato não existir no portal, este módulo o atualizará com os valores fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Grupos de propriedades]</td> 
   <td>Para cada propriedade que você deseja adicionar ao criar o contato, selecione o grupo no qual a propriedade é encontrada. O grupo de propriedades será aberto e você poderá preencher os valores das propriedades.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar/Atualizar um Contato (Herdado)]**

Cria um contato se ele ainda não existir em um portal ou o atualiza com os valores de propriedade mais recentes se ele existir em um portal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades]</td> 
   <td>Preencha todas as propriedades que deseja definir ou atualizar para o contato. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar/Atualizar um Grupo de Contatos]**

Cria um grupo de contatos ou os atualiza quando já existem. O desempenho é melhor quando o tamanho do lote é limitado a 100 contatos ou menos. As alterações feitas por meio desse endpoint são processadas de forma assíncrona, portanto, pode levar vários minutos para que as alterações sejam aplicadas a registros de contato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lote de Contatos a ser criado/atualizado] </td> 
   <td> <p>Adicione o lote de contatos.</p> <p>Clique em <strong>[!UICONTROL Adicionar item]</strong> para adicionar um novo contato. Na janela exibida, insira ou mapeie as seguintes informações:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Tipo de Pesquisa]</strong> </p> <p>Selecione como deseja identificar o contato:</p> 
      <ul> 
       <li> <p>[!UICONTROL ID]</p> <p>Insira a ID do contato que você deseja criar ou atualizar. </p> </li> 
       <li> <p>[!UICONTROL Email]</p> <p>Insira o endereço de email do contato que deseja criar ou atualizar. </p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Propriedades]</strong> </p> <p>Preencha todas as propriedades que deseja definir ou atualizar para o contato.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar Contatos]**

Retorna todos os contatos que foram criados no portal. A saída é limitada a 5000 contatos. Para listar os contatos anteriores ou seguintes, você pode usar o parâmetro [!UICONTROL avançado] para deslocar a lista.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>O número máximo de contatos [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades de saída]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID de contato [deslocamento de início] </td> 
    <td>Insira ou mapeie a ID do usuário que deseja iniciar a lista. Por exemplo, definir a ID de contato como a ID do 101º contato permitirá que o módulo liste os contatos 101-5100 em vez de 1-5000. </td> 
   </tr>
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar Contatos de uma Empresa]**

Recupera uma lista de contatos na empresa. A saída é limitada a 5000 contatos. Para listar os contatos anteriores ou seguintes, você pode usar o parâmetro [!UICONTROL avançado] para deslocar a lista.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Informe a ID da empresa cujos contatos você deseja listar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>O número máximo de contatos [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID de contato [deslocamento de início] </td> 
    <td>Insira ou mapeie a ID do usuário que deseja iniciar a lista. Por exemplo, definir a ID de contato como a ID do 101º contato permitirá que o módulo liste os contatos 101-5100 em vez de 1-5000. </td> 
   </tr>
 </tbody> 
</table>

+++

+++ **[!UICONTROL Mesclar contatos]**

Este módulo de ação mescla contatos

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
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

+++

+++ **[!UICONTROL Remover um Contato de uma Lista]**

Remove um contato de uma lista de contatos.

>[!NOTE]
>
>Não é possível remover contatos manualmente de uma lista dinâmica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Lista] </td> 
   <td>Selecione a ID da lista da qual deseja remover o contato. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Contato] </td> 
   <td>Digite a ID do contato que você deseja remover da lista. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Procurar Contatos]**

Recupera uma lista de contatos usando a consulta de pesquisa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Consulta]</td> 
   <td>Insira a consulta de pesquisa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td>Insira ou mapeie o número máximo de contatos que [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assista a contatos adicionados a uma lista]**

Este módulo de acionamento inicia um cenário quando um novo contato é adicionado a uma lista. Isso está disponível somente para usuários com uma conta de marketing paga.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Lista]</td> 
   <td>Insira ou mapeie a ID da lista que contém os contatos que você deseja assistir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades de Saída]</td> 
   <td>Selecione as propriedades que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Transações

+++ **[!UICONTROL Obter um pipeline de CRM do contrato]**

Retorna um pipeline de negociação específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Pipeline] </td> 
   <td>Insira ou mapeie a ID do pipeline do qual deseja recuperar detalhes. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Estágio] </td> 
   <td>Insira ou mapeie a ID do estágio para o qual deseja recuperar detalhes. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar pipelines de contrato/tíquete]**

Retorna todos os pipelines de negócios e tíquetes de um determinado portal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Objeto] </td> 
   <td>Selecione se deseja listar ofertas ou tickets.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Empresas

+++ **[!UICONTROL Procurar Empresas por domínio]**

Recupera uma lista de empresas com base em uma correspondência exata com a propriedade de domínio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Domínio] </td> 
   <td>Insira o domínio das empresas que você deseja pesquisar, como <code>[!DNL hubspot].com</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>O número máximo de empresas [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Propriedades de saída]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. </td> 
  </tr> 
 </tbody> 
</table>

+++

### Envolvimentos

+++ **Associar um Compromisso a um objeto do CRM**

Este módulo de ação associa um envolvimento a um contato, empresa ou negócio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td>Selecione o tipo de registro do CRM ao qual você deseja associar um envolvimento. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Compromisso]</td> 
  <td>Insira ou mapeie a ID do envolvimento que você deseja associar ao objeto.</td> 
   </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Registro]</td> 
  <td>Insira ou mapeie a ID do registro ao qual você deseja associar o envolvimento.</td> 
   </tr> 
 </tbody> 
</table>

+++

+++ **Criar um Compromisso**

Este módulo de ação cria um envolvimento (como uma observação, tarefa ou atividade) com um objeto CRM no HubSpot. Envolvimentos são qualquer interação com um contato que deve ser registrado no CRM.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Está Ativo?]</td> 
   <td>Habilite esta opção se o novo engajamento estiver ativo quando for criado. Um envolvimento deve estar ativo para aparecer na linha do tempo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
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

#### Metadados de email

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL De &gt; Email]</p> </td> 
   <td> <p>Insira ou mapeie o endereço de email do qual o email será enviado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td>Insira ou mapeie o nome da pessoa da qual o email será enviado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sobrenome]</td> 
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
   <td>Para enviar um email formatado pela HTML, insira ou mapeie o corpo do email, incluindo as tags da HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Texto</td> 
   <td>Para enviar um email somente texto, insira ou mapeie o texto do corpo do email.</td> 
  </tr> 
 </tbody> 
</table>

#### Metadados da chamada

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Para Número]</p> </td> 
   <td> <p>Insira ou mapeie o número de telefone para o qual a chamada será feita.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do Número]</td> 
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

#### Campos de reunião

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Título]</p> </td> 
   <td> <p>Insira ou mapeie o título ou o assunto da reunião.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td>Insira ou mapeie o texto da descrição ou dos detalhes da reunião.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hora de Início]</td> 
  <td>Informe ou mapeie a hora de início da reunião como um timestamp UNIX.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Horário de término</td> 
   <td>Informe ou mapeie a hora de término da reunião como um timestamp UNIX.</td> 
  </tr> 
 </tbody> 
</table>

#### Campos de tarefa

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Assunto]</p> </td> 
   <td> <p>Insira ou mapeie o título ou o assunto da tarefa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td>Insira ou mapeie o texto da descrição ou dos detalhes da tarefa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Status</td> 
   <td>Selecione o status da tarefa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Para Tipo De Objeto]</td> 
  <td>Insira <code>CONTACT</code> ou <code>COMPANY</code>.
  </td> 
   </tr> 
 </tbody> 
</table>

+++

+++ **Excluir um Compromisso**

Este módulo de ação exclui um envolvimento por sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td>Insira ou mapeie a ID do compromisso que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Assistir aos Compromissos**

Este módulo de acionamento inicia um cenário quando um novo envolvimento é criado em um portal. Esse módulo retorna apenas registros criados nos últimos 30 dias ou os 10.000 registros criados mais recentemente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>O número máximo de empresas [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Desde]</td> 
   <td>Insira ou mapeie a data mais antiga para a qual você deseja assistir aos eventos. Use o formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Eventos e notificações

+++ **Criar/Atualizar um Evento de Linha do Tempo**

Este módulo de ação cria ou atualiza um evento de linha do tempo. Este módulo pode ser usado somente com uma conexão de desenvolvedor que inclua seu identificador de usuário, sua chave da API HubSpot, a ID do cliente e o segredo do cliente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Aplicativo]</td> 
   <td>Insira ou mapeie a ID do aplicativo ao qual este evento pertence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Evento]</td> 
   <td>Insira ou mapeie uma ID para este evento. IDs de evento não são geradas pelo sistema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Tipo de Evento]</td> 
   <td>Insira ou mapeie a ID do tipo de evento deste evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Insira ou mapeie o endereço de email do contato para o qual você está criando o evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Objeto]</td> 
   <td>Insira ou mapeie a ID do contato para o qual você está criando o evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carimbo de Data/Hora]</td> 
   <td>Insira ou mapeie o carimbo de data e hora desse evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dados personalizados]</td> 
   <td>Para cada item de dados personalizados que você deseja adicionar a este evento, clique em <b>Adicionar item</b> e insira o nome e o valor do item.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Listar Tipos de Eventos de Linha do Tempo**

Este módulo de pesquisa retorna uma lista de todos os eventos da linha do tempo de um aplicativo específico. Este módulo pode ser usado somente com uma conexão de desenvolvedor que inclua seu identificador de usuário, sua chave da API HubSpot, a ID do cliente e o segredo do cliente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Aplicativo]</td> 
   <td>Insira ou mapeie a ID do aplicativo ao qual esses eventos pertencem. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Assistir a Eventos de Calendário**

Este módulo de acionamento inicia um cenário quando um novo evento é adicionado a um calendário. Inclui até 500 tarefas no intervalo entre as datas de início e término. Este módulo pode ser usado somente com uma conexão de desenvolvedor que inclua seu identificador de usuário, sua chave da API HubSpot, a ID do cliente e o segredo do cliente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Eventos]</td> 
   <td>Selecione se deseja assistir a eventos sociais, de conteúdo ou a todos os eventos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data de Início]</td> 
   <td>Insira ou mapeie a data de início.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data de Término]</td> 
   <td>Insira ou mapeie a data final.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Assistir Notificações**

Este módulo de acionamento inicia um cenário quando uma nova notificação sobre alterações é enviada.  Inclui até 500 tarefas no intervalo entre as datas de início e término. Este módulo pode ser usado somente com uma conexão de desenvolvedor que inclua seu identificador de usuário, sua chave da API HubSpot, a ID do cliente e o segredo do cliente. Você pode ter apenas um URL de webhook por aplicativo de desenvolvedor no HubSpot.

Para criar um webhook para este módulo, clique em **Adicionar** ao lado do campo de webhook e preencha os seguintes campos:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Aplicativo]</td> 
   <td>Insira a ID do aplicativo que deseja usar para este webhook. Você pode encontrar a ID em seu portal do desenvolvedor HubSpot.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assinaturas]</td> 
   <td> <p>Para cada tipo de notificação que você deseja observar, clique em <b>Adicionar item</b> e selecione o tipo de assinatura.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Força a Remoção de Assinaturas Antigas]</td> 
   <td>Habilite esta opção para desanexar ou excluir assinaturas antigas anexadas a este webhook.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Arquivos

+++ **[!UICONTROL Criar uma Pasta]**

Este módulo cria uma pasta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome da Pasta] </td> 
   <td>Insira ou mapeie um nome para a nova pasta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Pasta Pai] </td> 
   <td>Selecione a ID da pasta principal da pasta que você está criando. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Excluir um arquivo**

Esse módulo de ação exclui permanentemente um arquivo e todos os dados e miniaturas relacionados do gerenciador de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td>Insira ou mapeie a ID do arquivo que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Excluir uma pasta]**

Marca uma pasta como excluída.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID da pasta que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Listar Arquivos**

Este módulo de pesquisa retorna uma lista de arquivos armazenados no gerenciador de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Pasta]</td> 
   <td>Insira ou mapeie a ID da pasta que contém os arquivos que deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td>Para incluir somente arquivos que contenham caracteres específicos no nome do arquivo, insira ou mapeie os caracteres que deseja que o nome do arquivo inclua.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Mover um Arquivo]**

Move um arquivo para outra pasta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo] </td> 
   <td>Insira ou mapeie a ID do arquivo que deseja mover. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Pasta] </td> 
   <td>Selecione a ID da pasta para onde deseja mover o arquivo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td>Insira um nome para o arquivo movido.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Carregar um arquivo**

Este módulo de ação faz upload de um arquivo para o gerenciador de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de acesso] </td> 
   <td>Selecione se você deseja que o arquivo seja privado, público, mas não indexável, ou público e indexável. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Pasta] </td> 
   <td>Selecione a ID da pasta na qual deseja fazer upload do arquivo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Substituir]</td> 
   <td>Ative essa opção para substituir o arquivo se ele já existir na pasta.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Observar arquivos**

Este módulo de acionamento inicia um cenário quando um novo arquivo é salvo no gerenciador de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Pasta]</td> 
   <td>Insira ou mapeie a ID da pasta que contém os arquivos que você deseja observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td>Para incluir somente arquivos que contenham caracteres específicos no nome do arquivo, insira ou mapeie os caracteres que deseja que o nome do arquivo inclua.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Tarefas

+++ **Criar uma tarefa de Calendário**

Este módulo de ação cria uma nova tarefa para um calendário. A conexão usada neste módulo deve usar as credenciais de um usuário com uma conta de Marketing paga.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td>Insira ou mapeie um nome para a nova tarefa do calendário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td>Insira ou mapeie uma descrição para a nova tarefa do calendário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Proprietário]</td> 
   <td>Insira ou mapeie a ID do proprietário do usuário atribuído a esta tarefa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data do Evento]</td> 
   <td>Insira ou mapeie a data para esta tarefa.<p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Categoria]</td> 
   <td>Selecione o tipo de evento.<ul><li><b>Publicação do blog</b><p>Insira a ID do grupo de conteúdo. Esta é a ID da página do blog.</p></li><li><b>Email</b><p>Insira ou mapeie o caminho para o modelo de email que deseja usar.</li><li><b>Landing Page</b><p>Insira ou mapeie o caminho para o modelo de página de aterrissagem que deseja usar.</li><li><b>Personalizado</b></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estado]</td> 
   <td>Digite se o evento está no estado "Tarefa" ou "Concluída".</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL GUID de Campanha]</td> 
   <td>Insira ou mapeie a ID do HubSpot interno da campanha da qual este evento faz parte.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Excluir uma tarefa do calendário**

Este módulo de ação exclui uma tarefa de calendário. A conexão usada neste módulo deve usar as credenciais de um usuário com uma conta de Marketing paga.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID da tarefa que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Assistir a Eventos de Tarefas**

Este módulo de acionamento inicia um cenário quando há um novo evento de tarefa em um calendário. A conexão usada neste módulo deve usar as credenciais de um usuário com uma conta de Marketing paga. O módulo retorna até 500 eventos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data de Início]</td> 
   <td>Insira ou mapeie a data mais antiga para a qual você deseja assistir aos eventos. Use o formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data de Término]</td> 
   <td>Insira ou mapeie a data mais recente para a qual você deseja assistir aos eventos. Use o formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Usuários

+++ **Obter um Proprietário**

Este módulo de ação retorna detalhes de um proprietário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Proprietário]</td> 
   <td> <p>Insira ou mapeie a ID do proprietário para o qual deseja retornar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Proprietários da Lista**

Este módulo de pesquisa retorna uma lista de todos os proprietários em uma conta HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Tíquetes

<!-- Create a Ticket Need to find a working connection-->

+++ **[!UICONTROL Excluir um tíquete]**

Exclui um tíquete existente por sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Digite a ID do ticket que você deseja excluir. </td> 
  </tr> 
 </tbody> 
</table>

+++

<!-- Get a Ticket  Need to find a working connection-->

<!-- List Tickets  Need to find a working connection-->

&lt;!— Atualizar um tíquete Necessidade de encontrar uma conexão operacional—>

<!-- Watch Tickets Need to find a working connection-->

### Formulários

+++ **Obter um Arquivo Carregado via Formulário**

Este módulo de ação retorna um arquivo que foi carregado por meio de um formulário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL do Arquivo]</td> 
   <td>Insira ou mapeie o URL do arquivo que deseja recuperar. Isso pode ser encontrado nos metadados do formulário.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Listar Forms**

Este módulo de ação retorna todos os formulários que foram criados na conta associada à conexão usada para este módulo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de formulários que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--#### Submit Data to a Form Need to find a working connection-->



&lt;!—#### Assista aos envios para um formulário—É necessário encontrar uma conexão ativa>—>

### Redes sociais (transmissão)

+++ **Cancelar uma Mensagem de Difusão**

Esse módulo de ação cancela uma transmissão agendada, como um tweet ou uma publicação do Facebook.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Difusão]</td> 
   <td>Insira ou mapeie a ID da transmissão que você deseja cancelar.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Criar uma Mensagem de Difusão**

Esse módulo de ação cria e publica imediatamente uma mensagem no canal de mídia social especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Canal]</td> 
   <td>Insira ou mapeie a ID do canal que deseja usar para esta transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Título]</td> 
   <td>Insira ou mapeie um título para esta transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td>Insira ou mapeie o texto da transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL da Foto]</td> 
   <td>Insira ou mapeie o URL de uma foto que você deseja incluir na transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL da Miniatura]</td> 
   <td>Insira ou mapeie o URL de uma miniatura que você deseja usar para esta transmissão.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Acionar em]</td> 
   <td>Insira ou mapeie a data e a hora em que deseja que a transmissão seja enviada. Se isso for deixado em branco, a transmissão será enviada imediatamente.<p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Assistir Mensagens de Difusão**

Esse módulo de acionador inicia um cenário quando uma mensagem é postada do HubSpot para o canal de rede social especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de itens que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtrar por Status]</td> 
   <td>Para iniciar o cenário somente quando a mensagem estiver em um status específico, selecione o status.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtrar por Canal]</td> 
   <td>Para iniciar o cenário somente quando a mensagem estiver em um canal específico, selecione o canal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Difusão]</td> 
   <td>Para iniciar o cenário somente quando a mensagem for em ou após uma data específica, insira ou mapeie a data no formato <code>MM/DD/YYYY</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Publicações no blog

+++ **Criar uma postagem de blog**

Este módulo de ação cria uma nova publicação de blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Insira ou mapeie o título da publicação (o nome interno da publicação).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo da publicação</td> 
   <td>Insira ou mapeie o corpo principal da publicação no formato HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Resumo da publicação</td> 
   <td>Insira ou mapeie um resumo da publicação. Esse resumo é exibido na página da lista principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do autor do blog</td> 
   <td>Insira ou mapeie a ID do autor associado à publicação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do grupo de conteúdo</td> 
   <td>Insira ou mapeie a ID do blog ao qual esta publicação pertence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML de rodapé</td> 
   <td>Insira ou mapeie a HTML para códigos incorporados ou javascript que devem ser colocados antes da tag da página.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Head HTML</td> 
   <td>Insira ou mapeie a HTML para códigos incorporados ou javascript que devem ser colocados na parte superior.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da campanha</td> 
   <td>Insira ou mapeie a ID da campanha à qual esta publicação está associada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Imagem em destaque</td> 
   <td>Insira ou mapeie o URL da imagem que esta publicação usará como a imagem em destaque.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Palavra-chave</td> 
   <td>Para cada palavra-chave que você deseja adicionar a esta postagem, clique em <b>Adicionar item</b> e insira a palavra-chave e a GUID da palavra-chave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Metadescrição</td> 
   <td>Insira ou mapeie o texto da marca <code>meta</code> na página.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Data de publicação</td> 
   <td>Insira ou mapeie a data em que a publicação do blog deve ser publicada. <p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Habilite esta opção para publicar a publicação do blog imediatamente quando for criada. Se definida como Sim, essa opção ignorará o campo Data de publicação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Slug</td> 
   <td>Insira ou mapeie a descrição da publicação. A descrição é anexada ao final do domínio para formar o URL da publicação do blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">IDs de tópico</td> 
   <td>Para cada tópico que você deseja adicionar à publicação, clique em <b>Adicionar item</b> e insira a ID do tópico.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usar imagem em destaque</td> 
   <td>Habilite esta opção para usar a imagem em destaque para a publicação do blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dispositivos</td> 
   <td>Insira ou mapeie uma estrutura de dados contendo a data de todos os módulos desta publicação de blog. Isso se refere aos módulos da publicação do blog, não aos módulos do Fusion.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Excluir uma postagem do blog**

Este módulo de ação exclui uma única publicação de blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID da publicação do blog que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Listar postagens de blog**

Este módulo de pesquisa recupera publicações de um blog HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limite</td> 
   <td>Insira ou mapeie o número máximo de postagens de blog a serem retornadas em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Arquivado</td> 
   <td>Habilite esta opção para incluir publicações arquivadas em seus resultados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do autor do blog</td> 
   <td>Insira ou mapeie a ID de um autor para retornar postagens associadas a ele.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da campanha</td> 
   <td>Insira ou mapeie a ID de uma campanha para retornar postagens associadas a ela.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do grupo de conteúdo</td> 
   <td>Insira ou mapeie a ID de um blog para retornar postagens associadas a ele.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Digite um nome de publicação para retornar somente publicações com esse nome.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtrar por criado</td> 
   <td>Selecione Filtrar para retornar as publicações pelo valor de tempo criado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtrar por atualizado</td> 
   <td>Selecione Filtrar para retornar publicações pelo valor de tempo atualizado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtrar por excluído</td> 
   <td>Selecione Filtrar para retornar publicações pelo valor de tempo excluído.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Slug</td> 
   <td>Insira ou mapeie uma descrição para retornar publicações que correspondam à descrição. A descrição é anexada ao final do domínio para formar o URL da publicação do blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Estado</td> 
   <td>Selecione um estado (Rascunho, Publicado ou Agendado) para incluir apenas os resultados nesse estado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordenar por data de publicação</td> 
   <td>Selecione se os resultados devem ser classificados em ordem crescente ou decrescente por data de publicação.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Publicar/Desfazer a publicação de uma postagem do blog**

Este módulo de ação agenda ou cancela a publicação de uma publicação de blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID da publicação do blog que você deseja agendar ou cancelar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ação]</td> 
   <td>Selecione se deseja agendar a postagem de blog ou cancelar uma postagem de blog agendada anteriormente.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Assista a postagens no blog**

Esse módulo de acionamento inicia um cenário quando uma publicação de blog que corresponde aos critérios definidos é criada, atualizada ou excluída.



Este módulo de pesquisa recupera publicações de um blog HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limite</td> 
   <td>Insira ou mapeie o número máximo de postagens de blog a serem retornadas em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Arquivado</td> 
   <td>Habilite esta opção para incluir publicações arquivadas em seus resultados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do autor do blog</td> 
   <td>Insira ou mapeie a ID de um autor para retornar postagens associadas a ele.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da campanha</td> 
   <td>Insira ou mapeie a ID de uma campanha para retornar postagens associadas a ela.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do grupo de conteúdo</td> 
   <td>Insira ou mapeie a ID de um blog para retornar postagens associadas a ele.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Digite um nome de publicação para retornar somente publicações com esse nome.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtrar por criado</td> 
   <td>Selecione Filtrar para retornar as publicações pelo valor de tempo criado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtrar por atualizado</td> 
   <td>Selecione Filtrar para retornar publicações pelo valor de tempo atualizado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtrar por excluído</td> 
   <td>Selecione Filtrar para retornar publicações pelo valor de tempo excluído.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Slug</td> 
   <td>Insira ou mapeie uma descrição para retornar publicações que correspondam à descrição. A descrição é anexada ao final do domínio para formar o URL da publicação do blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Estado</td> 
   <td>Selecione um estado (Rascunho, Publicado ou Agendado) para incluir apenas os resultados nesse estado.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--+++**Workflows**>

<!--### Workflows May need connection

#### Add a Contact to a Workflow


#### Remove a Contact from a Workflow

-->

<!--+++-->

### Assinaturas

+++ **Atualizar Assinatura de Email**

Este módulo de ação atualiza uma assinatura de email no HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Insira ou mapeie o endereço de email da assinatura que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
   <td>Para cada status para o qual você deseja atualizar a inscrição, clique em <b>Adicionar item</b> e insira a ID do status, e se o endereço de email será inscrito nesse status.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status Legal de Assinatura do Portal]</td> 
   <td>Para registrar a base legal desta assinatura para o GDPR, selecione o status legal desta assinatura.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Explicação da Base Jurídica de Assinatura do Portal]</td> 
   <td>Para adicionar uma observação sobre a base legal desta assinatura do GDPR, insira ou mapeie o texto da observação.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Assistir Linha do Tempo de Assinaturas de um Portal**

Esse módulo de acionamento inicia um cenário quando uma nova assinatura de linha do tempo de email é adicionada ao portal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de itens que o módulo retornará em um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carimbo de Data/Hora de Início]</td> 
   <td>Para retornar resultados de em ou após uma data específica, insira a data no formato <code>MM/DD/YYYY.</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carimbo de Data/Hora Final]</td> 
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

### Outro

+++ **[!UICONTROL Fazer uma chamada de API]**

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
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL HubSpot CRM] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo para https://api.hubapi.com/. Por exemplo, /contacts/v1/lists/all/contacts/all</p> <p>Para obter a lista de pontos de extremidade disponíveis, consulte a <a href="https://legacydocs.hubspot.com/docs/overview">[!DNL HubSpot] Documentação da API</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Método]</p> </td> 
   <td> <p>Selecione o método HTTP que deseja usar:</p> <p>[!UICONTROL GET]</p> <p>para recuperar informações de uma entrada.</p> <p>[!UICONTROL POST]</p> <p>para criar uma nova entrada.</p> <p>[!UICONTROL PUT]</p> <p>para atualizar/substituir uma entrada existente.</p> <p>[!UICONTROL PATCH]</p> <p>para fazer uma atualização de entrada parcial.</p> <p>[!UICONTROL DELETE]</p> <p>para deletar uma entrada.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p> Insira os cabeçalhos de solicitação desejados. Não é necessário adicionar cabeçalhos de autorização; já fizemos isso para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p> Insira a string de consulta da solicitação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
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
>Correspondências da pesquisa podem ser encontradas na Saída do módulo em [!UICONTROL Pacote] > [!UICONTROL Corpo] > [!UICONTROL contatos].
>
>No nosso exemplo, 3 contatos foram retornados:
>
>![Saída da API do Hubspot](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-output.png)

+++

## Criar um novo aplicativo

1. Faça logon em sua conta de desenvolvedor do [!DNL HubSpot].
1. Selecione a opção **[!UICONTROL Criar um aplicativo]**.
1. Insira o Nome do aplicativo e [!UICONTROL Salve] a caixa de diálogo.
1. Selecione os escopos necessários para o webhook.

   Por exemplo, adicione escopos de contatos para acionar o módulo quando um novo contato for criado ou excluído.

   O [!UICONTROL escopo de contatos] é tudo que você precisa para receber webhooks de contatos, ofertas e eventos da empresa.

   >[!IMPORTANT]
   >
   >Não preencha o campo [!UICONTROL URL de redirecionamento].
