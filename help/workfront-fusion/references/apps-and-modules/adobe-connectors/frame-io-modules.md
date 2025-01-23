---
title: Módulos do Frame.io
description: A conta  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] .
author: Becky
feature: Workfront Fusion
exl-id: 121b145c-d04d-44b9-b673-ea2928e2346d
source-git-commit: 7f25a8a118a3dba3de3d834497e047bd1aeabf0a
workflow-type: tm+mt
source-wordcount: '2128'
ht-degree: 0%

---

# [!DNL Frame.io] módulos

Os módulos do [!DNL Adobe Workfront Fusion] [!DNL Frame.io] permitem monitorar, criar, atualizar, recuperar ou excluir ativos e comentários em sua conta do [!DNL Frame.io].

Para obter uma introdução ao vídeo sobre o conector Frame.io, consulte:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
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

Para usar módulos [!DNL Frame.io], você deve ter uma conta [!DNL Frame.io]

## Informações da API do Frame.io

O conector Frame.io usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.frame.io/v2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!DNL Frame.io] a [!UICONTROL Adobe Workfront Fusion]

Você pode se conectar a [!DNL Frame.io] usando um token de API ou usando o OAuth 2.0.

[Conectar-se ao  [!DNL Frame.io] usando um token de API](#connect-to-frameio-using-an-api-token)

[Conectar-se ao  [!DNL Frame.io] usando o PKCE do OAuth 2.0](#connect-to-frameio-using-oauth-20-pkce)

### Conectar-se a [!DNL Frame.io] usando um token de API

Para conectar sua conta do [!DNL Frame.io] ao [!DNL Workfront Fusion] usando um token de API, você deve criar o token de API em sua conta do [!DNL Frame.io] e inseri-lo na caixa de diálogo [!DNL Workfront Fusion] [!DNL Frame.io] [!UICONTROL Create a connection].

1. Faça logon em sua conta do [!DNL Frame.io].
1. Vá para a página **[!UICONTROL Tokens]** no [!DNL Frame.io] Desenvolvedor.
1. Clique em **[!UICONTROL New]**.
1. Insira o nome do token, selecione os escopos que deseja usar e clique em **[!UICONTROL Create]**.
1. Copie o token fornecido.
1. Vá para [!DNL Workfront Fusion] e abra a caixa de diálogo **[!UICONTROL Create a connection]** do módulo [!DNL Frame.io].
1. No campo **[!UICONTROL Connection type]**, selecione **[!DNL Frame.io]**.
1. Insira o token copiado na etapa 5 para o campo **[!UICONTROL Your [!DNL Frame.io] API Key]**
1. Clique em **[!UICONTROL Continue]** para estabelecer a conexão e retornar ao módulo.

### Conectar a [!DNL Frame.io] usando o PKCE do OAuth 2.0

Você pode criar uma conexão com [!DNL Frame.io] usando o PKCE OAuth 2.0 com uma ID de cliente opcional. Para incluir uma ID do cliente em sua conexão, crie um aplicativo OAuth 2.0 na conta [!DNL Frame.io].

* [Conectar-se ao  [!DNL Frame.io] usando o PKCE do OAuth 2.0 (sem ID do cliente)](#connect-to-frameio-using-using-oauth-20-pkce-without-client-id)
* [Conecte-se ao  [!DNL Frame.io] usando o PKCE do OAuth 2.0 (com ID de cliente)](#connect-to-frameio-using-using-oauth-20-pkce-with-client-id)

#### Conecte-se a [!DNL Frame.io] usando o PKCE do OAuth 2.0 (sem ID do cliente)

1. Vá para [!DNL Workfront Fusion] e abra a caixa de diálogo **[!UICONTROL Create a connection]** do módulo [!DNL Frame.io].
1. No campo **[!UICONTROL Connection type]**, selecione **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]**.
1. Insira um nome para a nova conexão no campo **[!UICONTROL Connection name]**.
1. Clique em **[!UICONTROL Continue]** para estabelecer a conexão e retornar ao módulo.

#### Conecte-se a [!DNL Frame.io] usando o PKCE do OAuth 2.0 (com ID de Cliente)

1. Crie um aplicativo OAuth 2.0 em [!DNL Frame.io]. Para obter instruções, consulte a documentação do [!DNL Frame.io] em [!UICONTROL OAuth 2.0 Code Authorization Flow].

   >[!IMPORTANT]
   >
   >Ao criar o aplicativo OAuth 2.0 em [!DNL Frame.io]:
   >
   >* Insira o seguinte como o URI de redirecionamento:
   >   
   >     * **Américas/APAC**: `https://app.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >     * **EMEA**: `https://app-eu.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >* Ative a opção PCKE.


1. Copie o `client_id` fornecido.
1. Vá para [!DNL Workfront Fusion] e abra a caixa de diálogo **[!UICONTROL Create a connection]** do módulo [!DNL Frame.io].
1. No campo **[!UICONTROL Connection type]**, selecione **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]**.
1. Insira um nome para a nova conexão no campo **[!UICONTROL Connection name]**.
1. Clique em **[!UICONTROL Show advanced settings]**.
1. Insira o `client_id` que você copiou na etapa 2 para o campo **[!UICONTROL Client ID]**.
1. Clique em **[!UICONTROL Continue]** para estabelecer a conexão e retornar ao módulo.

## [!DNL Frame.io] módulos e seus campos

Ao configurar módulos do [!DNL Frame.io], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Frame.io] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ativos](#assets)
* [Comentários](#comments)
* [Projetos](#projects)
* [Outro](#other)

### Ativos

* [[!UICONTROL Create an Asset]](#create-an-asset)
* [[!UICONTROL Delete an Asset]](#delete-an-asset)
* [[!UICONTROL Get an Asset]](#get-an-asset)
* [[!UICONTROL List Assets]](#list-assets)
* [[!UICONTROL Update an Asset]](#update-an-asset)
* [[!UICONTROL Watch Asset Deleted]](#watch-asset-deleted)
* [[!UICONTROL Watch Asset Label Updated]](#watch-asset-label-updated)
* [[!UICONTROL Watch New Asset]](#watch-new-asset)

#### [!UICONTROL Create an Asset]

Este módulo de ação cria um novo ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto ou mapeie a ID do projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta ou mapeie a ID da pasta na qual deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Selecione se deseja criar uma pasta ou um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Insira o nome do novo arquivo ou pasta.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">File Type </td> 
    <td> <p>Select the type of file you want to upload.</p> </td> 
   </tr>
  --> <!--
   <tr> 
    <td role="rowheader">File Size </td> 
    <td> <p>The file size in bytes.</p> </td> 
   </tr>
  --> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Se estiver criando um arquivo, insira o URL do arquivo do qual deseja fazer upload.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Se estiver criando um arquivo, insira uma breve descrição do ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Label] </td> 
   <td> <p>Se estiver criando um arquivo, selecione se ele está em andamento, precisa de revisão ou se foi aprovado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Asset]

Esse módulo de ação exclui um ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe que possui o projeto que contém o ativo que você deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Selecione o projeto ou que contém o ativo que você deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta que contém o ativo que você deseja excluir</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecione ou mapeie o ativo que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Asset]

Este módulo de ação recupera detalhes do ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto que contém o ativo sobre o qual você deseja recuperar detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Selecione o projeto que contém o ativo do qual deseja recuperar detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta que contém o ativo do qual deseja recuperar detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecione o ativo ou mapeie a ID do ativo sobre o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Assets]

Este módulo de pesquisa recupera todos os ativos na pasta do projeto especificado.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto que contém a pasta da qual você deseja recuperar ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Selecione o projeto que contém a pasta da qual deseja recuperar ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta da qual deseja listar ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Insira ou mapeie o número máximo de ativos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an Asset]

Esse módulo de ação permite atualizar o nome, a descrição ou os campos personalizados de um ativo existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto para o qual você deseja atualizar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto ou mapeie a ID do projeto para o qual você deseja atualizar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta ou mapeie a ID da pasta na qual deseja atualizar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Insira ou mapeie a ID do ativo que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Insira o nome do arquivo atualizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Insira uma breve descrição do ativo atualizado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Deleted]

Este módulo de acionamento inicia um cenário quando um ativo pertencente ao grupo especificado é excluído.

Como esse é um acionador instantâneo, você deve selecionar ou criar um webhook para o módulo usar.

Se estiver adicionando um webhook, insira as informações a seguir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Insira um nome para o webhook, como "Ativo excluído".</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Label Updated]

Esse módulo de acionamento inicia um cenário quando um rótulo para um ativo de propriedade do grupo especificado é definido, alterado ou removido.

Como esse é um acionador instantâneo, você deve selecionar ou criar um webhook para o módulo usar.

Se estiver adicionando um webhook, insira as informações a seguir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Insira um nome para o webhook, como "Status do ativo atualizado".</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Asset]

Este módulo de acionamento inicia um cenário quando um novo ativo é criado para o grupo especificado.

Como esse é um acionador instantâneo, você deve selecionar ou criar um webhook para o módulo usar.

Se estiver adicionando um webhook, insira as informações a seguir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Insira um nome para o webhook, como "Ativo criado".</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Comentários

* [[!UICONTROL Create a Comment]](#create-a-comment)
* [[!UICONTROL Delete a Comment]](#delete-a-comment)
* [[!UICONTROL Get a Comment]](#get-a-comment)
* [[!UICONTROL List Comments]](#list-comments)
* [[!UICONTROL Update a Comment]](#update-a-comment)
* [[!UICONTROL Watch Comment Updated]](#watch-comment-updated)
* [[!UICONTROL Watch New Comment]](#watch-new-comment)

#### [!UICONTROL Create a Comment]

Esse módulo de ação adiciona um novo comentário ou resposta ao ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Selecione se deseja criar um comentário ou responder a um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto que contém o ativo ao qual você deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto ou mapeie a ID do projeto que contém o ativo ao qual você deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta ou mapeie a ID da pasta que contém o ativo ao qual você deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecione ou mapeie o ativo ao qual deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Selecione ou mapeie o comentário ao qual deseja adicionar uma resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Insira o conteúdo do texto do comentário ou da resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Insira o número do quadro no vídeo ao qual o comentário deve ser vinculado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Comment]

Este módulo de ação exclui um comentário existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID]</td> 
   <td> <p> Selecione ou mapeie a equipe proprietária do projeto que contém o ativo do qual você deseja excluir um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Selecione o projeto ou mapeie a ID do projeto que contém o ativo do qual você deseja excluir um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p> Selecione a pasta que contém o ativo do qual você deseja excluir um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Insira ou mapeie a ID do ativo que contém o comentário que você deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Insira ou mapeie a ID do comentário que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Comment]

Este módulo de ação recupera detalhes do comentário especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto que contém a pasta da qual você deseja recuperar ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto que contém a pasta da qual deseja recuperar ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta da qual deseja listar ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecione o ativo que contém o comentário que você deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Selecione o comentário sobre o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Comments]

Este módulo de pesquisa recupera todos os comentários do ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto que contém a pasta da qual você deseja recuperar comentários.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto que contém a pasta da qual deseja recuperar comentários.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta que contém o ativo do qual deseja listar comentários.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecione o ativo para o qual deseja listar comentários.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Insira ou mapeie o número máximo de comentários que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Comment]

Este módulo de ação edita um comentário existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto que contém o ativo no qual você deseja atualizar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto \ que contém o ativo no qual você deseja atualizar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecione a pasta que contém o ativo sobre o qual deseja atualizar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecione o ativo no qual deseja atualizar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Selecione o comentário que deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Insira o conteúdo do texto do comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Insira o número do quadro no vídeo ao qual o comentário está vinculado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comment Updated]

Este módulo de acionamento inicia um cenário quando um comentário é editado.

Como esse é um acionador instantâneo, você deve selecionar ou criar um webhook para o módulo usar.

Se estiver adicionando um webhook, insira as informações a seguir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Insira o nome do webhook, por exemplo, Comment Edited.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Comment]

Este módulo de acionamento inicia um cenário quando um novo comentário ou resposta é criado.

Como esse é um acionador instantâneo, você deve selecionar ou criar um webhook para o módulo usar.

Se estiver adicionando um webhook, insira as informações a seguir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Insira o nome do webhook, por exemplo Novo comentário.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projetos

#### [!UICONTROL List Projects]

Este módulo de pesquisa recupera todos os projetos da equipe especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecione ou mapeie a equipe para a qual deseja recuperar projetos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Insira ou mapeie o número máximo de projetos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outro

#### [!UICONTROL Make an API Call]

Este módulo permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo para <code>https://api.frame.io</code>. Exemplo: <code> /v2/teams</code></p> <p>Observação: para obter a lista de endpoints disponíveis, consulte a Referência de API [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Insira a string de consulta da solicitação. Para cada parâmetro que você deseja incluir na cadeia de caracteres de consulta, clique em <b>[!UICONTROL Add item]</b> e insira o nome do campo e o valor desejado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
