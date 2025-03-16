---
title: Módulos do SharePoint
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Microsoft SharePoint Online, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '3124'
ht-degree: 0%

---

# Módulos do Microsoft SharePoint Online

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam o Microsoft SharePoint Online, bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Para usar os módulos do Microsoft SharePoint Online, você deve ter uma conta do Microsoft SharePoint Online.

## Informações da API do SharePoint

O conector do SharePoint usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.14.2</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion] {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [Conectar o Microsoft SharePoint Online ao  [!DNL Workfront Fusion] usando uma conta do  [!DNL Microsoft] ](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [Conectar o Microsoft SharePoint Online ao  [!DNL Workfront Fusion] usando configurações avançadas](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)

### Conectar o Microsoft SharePoint Online a [!DNL Workfront Fusion] usando uma conta [!DNL Microsoft]

Você pode usar sua conta do [!DNL Microsoft] para criar uma conexão com o Microsoft SharePoint Online. Para obter instruções sobre como conectar sua conta do [!DNL Sharepoint] ao [!DNL Workfront Fusion], consulte [Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion] usando configurações avançadas

Para conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion] sem uma conta [!DNL Microsoft], você precisa de uma ID de Cliente, Segredo do Cliente e ID do Locatário.

1. Clique em **[!UICONTROL Adicionar]** próximo à parte superior da caixa **Microsoft SharePoint Online** para abrir a caixa **[!UICONTROL Criar uma conexão]**.

1. (Opcional) Altere o **[!UICONTROL Nome da conexão]** padrão.
1. Clique em **[!UICONTROL Mostrar configurações avançadas]**.
1. Insira a **[!UICONTROL ID do Cliente]** e o **[!UICONTROL Segredo do Cliente]** do Microsoft SharePoint Online.

1. Clique em **[!UICONTROL Continuar]**.
1. Na janela de logon que é exibida, digite suas credenciais para fazer logon no aplicativo, se ainda não tiver feito.
1. (Condicional) Se um botão **[!UICONTROL Permitir]** for exibido, clique no botão para conectar o aplicativo a [!DNL Workfront Fusion].

## Módulos do Microsoft SharePoint Online e seus campos

Ao configurar módulos do Microsoft SharePoint Online, o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos adicionais do Microsoft SharePoint Online podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Item da unidade](#drive-item)
* [Item](#item)
* [Lista](#list)
* [Página (Beta)](#page-beta)
* [Site](#site)
* [Outro](#other)

### Item da unidade

* [Criar um arquivo](#create-a-file)
* [Criar uma pasta](#create-a-folder)
* [Obter um arquivo](#get-a-file)
* [Observar itens da pasta](#watch-folder-items)

#### Criar um arquivo

Este módulo retorna as alterações feitas no SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site, Unidade e IDs de Pasta]</td> 
   <td> <p>Selecione como você deseja identificar o local da pasta na qual deseja recuperar as alterações.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Unidade]</strong> e <strong>[!UICONTROL ID da Pasta]</strong> do local em que deseja criar o arquivo.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o local em que deseja criar o arquivo. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
      <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p>
  </tr>  </tbody> 
</table>

#### Criar uma pasta

Este módulo de ação cria uma nova pasta no SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site, Unidade e IDs de Pasta]</td> 
   <td> <p>Selecione como deseja identificar o local da pasta que deseja criar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Unidade]</strong> e <strong>[!UICONTROL ID da Pasta]</strong> do local em que deseja criar a pasta.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o local em que deseja criar a pasta. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome da pasta]</td> 
   <td>Insira ou mapeie um nome para a nova pasta.</td> 
  </tr>
  </tbody> 
</table>

#### Obter um arquivo

Este módulo de ação recupera o arquivo SharePoint especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site, Unidade e IDs de Pasta]</td> 
   <td> <p>Selecione como você deseja identificar o local do arquivo que deseja obter.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL ID do Arquivo]</strong> para o arquivo que você deseja recuperar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o local do arquivo. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Observar itens da pasta

Este módulo de acionamento inicia um cenário quando um item é atualizado em uma pasta selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site, Unidade e IDs de Pasta]</td> 
   <td> <p>Selecione como você deseja identificar o local do arquivo que deseja obter.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL ID da pasta]</strong> nos campos exibidos.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o local da pasta que deseja observar. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira o número máximo de itens que [!DNL Workfront Fusion] deve retornar durante um ciclo de execução de cenário.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Item

* [[!UICONTROL Copiar um item]](#copy-an-item)
* [[!UICONTROL Criar um item]](#create-an-item)
* [[!UICONTROL Excluir um item]](#delete-an-item)
* [[!UICONTROL Obter um Item]](#get-an-item)
* [[!UICONTROL Listar itens]](#list-items)
* [[!UICONTROL Mover Item]](#move-an-item)
* [[!UICONTROL Atualizar um item]](#update-an-item)
* [[!UICONTROL Itens de observação] (Agendados)](#watch-items-scheduled)


#### [!UICONTROL Copiar um Item]

Este módulo de ação copia um item existente em uma lista do SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Inserir IDs de site, unidade e pasta</td> 
   <td> <p>Selecione como você deseja identificar o site e a unidade que contêm o item que você deseja copiar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Unidade]</strong> e <strong>[!UICONTROL ID do Item]</strong> do item que você deseja copiar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>No campo Tipo de Item, selecione se deseja mover um campo ou uma pasta.  Selecione o site que contém o item que você deseja copiar, selecione a lista e selecione o item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Destino]</td> 
   <td> Insira ou mapeie a ID da pasta para a qual você deseja copiar o item. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Novo nome]</td> 
   <td>Insira ou mapeie um nome para a nova cópia do item. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar um item]

Este módulo de ação cria um novo item em uma lista do SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criar um Item]</td> 
   <td> <p>Selecione como você deseja identificar o site e a unidade em que deseja criar um item.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong> e <strong>[!UICONTROL ID da Lista]</strong> onde deseja criar o item.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém a lista onde você deseja criar um item e selecione-a. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos]</td> 
   <td>Para cada campo que você deseja definir para o novo item, clique em <b>Adicionar item</b> e insira a chave do campo (que identifica o campo) e o valor que você deseja que o novo item tenha para esse campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um item]

Este módulo de ação exclui um item existente em uma lista do SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Atualizar um Item]</td> 
   <td> <p>Selecione como você deseja identificar o site e a lista que contém o item que você deseja excluir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL ID do Item]</strong> do item que você deseja excluir.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém o item que você deseja excluir, selecione a lista e selecione o item. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um Item]

Este módulo de ação retorna os dados de um item especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Obter um Item]</td> 
   <td> <p>Selecione como você deseja identificar o site e a lista que contém o item que você deseja obter.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL ID do Item]</strong> do item para o qual você deseja retornar dados.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém a lista da qual você deseja recuperar um item e selecione a lista e, em seguida, o item. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar itens]

Este módulo de ação recupera uma lista de todos os itens em uma lista especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listar Itens]</td> 
   <td> <p>Selecione como deseja identificar a lista da qual deseja recuperar os itens.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong> e <strong>[!UICONTROL ID da Lista]</strong> para a lista para a qual você deseja listar itens.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém a lista da qual deseja recuperar itens e selecione-a. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de itens que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mover um Item]

Este módulo de ação copia um item existente em uma lista do SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Inserir IDs de site, unidade e pasta</td> 
   <td> <p>Selecione como você deseja identificar o site e a lista que contém o item que você deseja mover.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL ID do Item]</strong> para o item que você deseja mover.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>No campo Tipo de Item, selecione se deseja mover um campo ou uma pasta. Selecione o site que contém o item que você deseja copiar, selecione a lista e selecione o item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Destino]</td> 
   <td> Insira ou mapeie a ID da pasta para onde deseja mover o item. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Novo nome]</td> 
   <td>Insira ou mapeie um nome para o item movido. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um item]

Este módulo de ação atualiza um item existente em uma lista do SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Atualizar um Item]</td> 
   <td> <p>Selecione como você deseja identificar o site e a lista que contém o item que você deseja atualizar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL ID do Item]</strong> do item que você deseja atualizar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém o item que você deseja atualizar, selecione a lista e selecione o item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos]</td> 
   <td>Para cada campo que você deseja atualizar para o novo item, clique em <b>Adicionar item</b> e insira a chave do campo (que identifica o campo) e o novo valor que você deseja que o item tenha para esse campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Itens de observação] (Agendados)

Esse módulo de acionamento inicia um cenário quando um item é criado ou modificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listas de Observação]</td> 
   <td>Selecione se deseja monitorar as listas por hora de criação (novos itens) ou por hora de modificação (itens atualizados).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site e ID de Lista]</td> 
   <td> <p>Selecione como deseja identificar o site e a lista que deseja observar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong> e a <strong>[!UICONTROL ID da Lista]</strong> que você deseja assistir.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o site que deseja observar e selecione a lista. Esses menus suspensos recuperam apenas os sites seguidos.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de itens que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Lista

* [[!UICONTROL Criar uma Lista]](#create-a-list)
* [[!UICONTROL Obter uma Lista]](#get-a-list)
* [[!UICONTROL Listar listas]](#list-lists)
* [[!UICONTROL Listas de Interesse]](#watch-lists)

#### [!UICONTROL Criar uma Lista]

Este módulo de ação cria uma nova lista no SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de Site]</td> 
   <td> <p>Selecione como deseja identificar o site em que deseja criar uma lista.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong> onde deseja criar uma lista.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site no qual deseja criar uma lista. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome para Exibição]</td> 
   <td>Insira ou mapeie um nome para a nova lista.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td>Insira ou mapeie uma descrição para a nova lista.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adicionar Colunas]</td> 
   <td>Para cada coluna que você deseja definir para a nova lista, clique em <b>Adicionar item </b>, insira um <strong>[!UICONTROL Name]</strong> para o campo e selecione o <strong>[!UICONTROL Type]</strong> do valor que você deseja que a nova coluna tenha.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma Lista]

Este módulo de ação retorna os dados de uma lista especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Obter uma Lista]</td> 
   <td> <p>Selecione como você deseja identificar o site e a lista que contém o item que você deseja obter.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong> e a <strong>ID da Lista</strong> que você deseja retornar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém a lista que você deseja recuperar e, em seguida, selecione a lista. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar listas]

Este módulo de ação recupera uma lista de todos os itens em um site especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listas de Listas]</td> 
   <td> <p>Selecione como você deseja identificar o site do qual deseja recuperar listas.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong> que contém as listas que você deseja retornar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém as listas que você deseja recuperar. O menu suspenso recupera apenas os sites que você segue.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de listas que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listas de Interesse]

Esse módulo de acionador inicia um cenário quando uma lista é criada ou modificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listas de Observação]</td> 
   <td>Selecione se deseja monitorar as listas por hora de criação (novos itens) ou por hora de modificação (itens atualizados).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID do Site]</td> 
   <td> <p>Selecione como você deseja identificar o site que deseja observar as listas.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong> onde deseja ver listas.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o site que deseja assistir. O menu suspenso recupera apenas o site que você segue.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de listas que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Página (Beta)

>[!NOTE]
>
>As APIs na versão `beta` em [!DNL Microsoft Graph] estão sujeitas a alterações. O uso dessas APIs em aplicativos de produção não é compatível.

#### [!UICONTROL Obter uma página]

Este módulo de ação retorna os dados de uma página especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Obter uma Página]</td> 
   <td> <p>Selecione como você deseja identificar a página que deseja recuperar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>e <strong>[!UICONTROL ID da Página]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém a página que você deseja recuperar e selecione a página.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Site

* [[!UICONTROL Obter um site]](#get-a-site)
* [[!UICONTROL Pesquisar Sites]](#search-sites)

#### [!UICONTROL Obter um site]

Este módulo de ação retorna os dados de um site especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Obter um Site]</td> 
   <td> <p>Selecione como você deseja identificar a página que deseja recuperar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que deseja recuperar.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar Sites]

Esse módulo de ação pesquisa sites por um parâmetro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Palavra-chave do Nome para Exibição]</td> 
   <td> <p>Insira ou mapeie o termo de pesquisa que você deseja pesquisar nos sites.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de sites que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outro

* [Obter alterações](#get-changes)
* [Fazer uma chamada de API](#make-an-api-call)
* [Assistir a eventos](#watch-events)

#### Obter alterações

Este módulo recupera adições, atualizações e exclusões feitas na pasta do SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site, Unidade e IDs de Pasta]</td> 
   <td> <p>Selecione como você deseja identificar o site e a unidade que contêm o item que você deseja atualizar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Unidade]</strong> e <strong>[!UICONTROL ID da Pasta]</strong> nos campos exibidos.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém o item que você deseja atualizar, selecione a unidade e selecione a pasta. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> O token identifica a partir de que ponto o módulo deve começar a recuperar as alterações.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fazer uma chamada de API]

Este módulo permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao [!DNL Workfront Fusion], consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo para <code>https://graph.microsoft.com</code>. Exemplo:<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Método]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td>Selecione o tipo de dados que deseja enviar na chamada de API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Assistir a eventos

Esse módulo de acionador instantâneo inicia um cenário quando um item é adicionado, atualizado ou excluído no SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecione um webhook existente ou clique em Adicionar e insira a conexão para criar um novo webhook.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
