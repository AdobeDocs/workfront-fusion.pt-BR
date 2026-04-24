---
title: Módulos Frame.io (Legacy)
description: A conta do  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] .
author: Becky
feature: Workfront Fusion
exl-id: 121b145c-d04d-44b9-b673-ea2928e2346d
source-git-commit: 72abd9b5aa73d54edd73dc16f7695d2b01cc8624
workflow-type: tm+mt
source-wordcount: '2663'
ht-degree: 44%

---

# [!DNL Frame.io] módulos herdados

>[!IMPORTANT]
>
>Este artigo descreve a versão herdada do conector Frame.io. Esse conector é usado para estabelecer conexão com o Frame.io versão 3.
>
>Para obter instruções sobre a nova versão (beta) do conector Frame.io, consulte [Conector Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules-new.md).

Os módulos do [!DNL Frame.io] do Adobe Workfront Fusion permitem monitorar, criar, atualizar, recuperar ou excluir ativos e comentários da conta do [!DNL Frame.io].

O Workfront oferece dois conectores do Frame.io, com base na versão do Frame.io à qual você está se conectando.

| Conector | Versão do Frame.io |
|---|---|
| Frame.io | V4 |
| Frame.io (legado) | V3 |

Para obter instruções sobre a nova versão do conector Frame.io, consulte [Conector Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules-new.md).

Para obter um vídeo de introdução ao conector do Frame.io, consulte:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote do Adobe Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Os pacotes Workfront Prime e Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p><p>Trabalho ou maior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos do [!DNL Frame.io], você deve ter uma conta do [!DNL Frame.io]

## Informações da API do Frame.io

O conector do Frame.io usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
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

## Conectar o [!DNL Frame.io] ao [!UICONTROL Adobe Workfront Fusion]

Você pode se conectar a [!DNL Frame.io] usando um token de API ou usando o OAuth 2.0.

[Conectar-se ao  [!DNL Frame.io] usando um token de API](#connect-to-frameio-using-an-api-token)

[Conectar-se ao  [!DNL Frame.io] usando o PKCE do OAuth 2.0](#connect-to-frameio-using-oauth-20-pkce)

### Conectar-se a [!DNL Frame.io] usando um token de API

Para conectar sua conta do [!DNL Frame.io] ao Workfront Fusion usando um token de API, você deve criar o token de API em sua conta do [!DNL Frame.io] e inseri-lo na caixa de diálogo [!DNL Frame.io]Criar uma conexão[!UICONTROL &#x200B; do Workfront Fusion &#x200B;].

1. Faça logon em sua conta do [!DNL Frame.io].
1. Vá para a página **[!UICONTROL Tokens]** no [!DNL Frame.io] Developer.
1. Clique em **[!UICONTROL Novo]**.
1. Insira o nome do token, selecione os escopos que deseja usar e clique em **[!UICONTROL Criar]**.
1. Copie o token fornecido.
1. Vá para o Workfront Fusion e abra a caixa de diálogo [!DNL Frame.io]Criar uma conexão **[!UICONTROL do módulo]**.
1. No campo **[!UICONTROL Tipo de conexão]**, selecione **[!DNL Frame.io]**.
1. Insira o token copiado na etapa 5 para o campo **[!UICONTROL Sua [!DNL Frame.io] Chave de API]**
1. Clique em **[!UICONTROL Continuar]** para estabelecer a conexão e retornar ao módulo.

### Conectar a [!DNL Frame.io] usando o PKCE do OAuth 2.0

Você pode criar uma conexão com [!DNL Frame.io] usando o PKCE OAuth 2.0 com uma ID de cliente opcional. Para incluir uma ID do cliente em sua conexão, crie um aplicativo OAuth 2.0 na conta [!DNL Frame.io].

* [Conectar-se ao  [!DNL Frame.io] usando o PKCE do OAuth 2.0 (sem ID do cliente)](#connect-to-frameio-using-using-oauth-20-pkce-without-client-id)
* [Conecte-se ao  [!DNL Frame.io] usando o PKCE do OAuth 2.0 (com ID de cliente)](#connect-to-frameio-using-using-oauth-20-pkce-with-client-id)

#### Conecte-se a [!DNL Frame.io] usando o PKCE do OAuth 2.0 (sem ID do cliente)

1. Vá para o Workfront Fusion e abra a caixa de diálogo [!DNL Frame.io]Criar uma conexão **[!UICONTROL do módulo]**.
1. No campo **[!UICONTROL Tipo de conexão]**, selecione **[!UICONTROL [!DNL Frame.io]PKCE OAuth 2.0]**.
1. Insira um nome para a nova conexão no campo **[!UICONTROL Nome da conexão]**.
1. Clique em **[!UICONTROL Continuar]** para estabelecer a conexão e retornar ao módulo.

#### Conecte-se a [!DNL Frame.io] usando o PKCE do OAuth 2.0 (com ID de Cliente)

1. Crie um aplicativo OAuth 2.0 em [!DNL Frame.io]. Para obter instruções, consulte a documentação do [!DNL Frame.io] em [!UICONTROL Fluxo de Autorização de Código do OAuth 2.0].

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
1. Vá para o Workfront Fusion e abra a caixa de diálogo [!DNL Frame.io]Criar uma conexão **[!UICONTROL do módulo]**.
1. No campo **[!UICONTROL Tipo de conexão]**, selecione **[!UICONTROL [!DNL Frame.io]PKCE OAuth 2.0]**.
1. Insira um nome para a nova conexão no campo **[!UICONTROL Nome da conexão]**.
1. Clique em **[!UICONTROL Mostrar configurações avançadas]**.
1. Insira o `client_id` copiado na etapa 2 para o campo **[!UICONTROL ID do cliente]**.
1. Clique em **[!UICONTROL Continuar]** para estabelecer a conexão e retornar ao módulo.

## Módulos do [!DNL Frame.io] e seus campos

Ao configurar módulos do [!DNL Frame.io], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos do [!DNL Frame.io] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ativos](#assets)
* [Comentários](#comments)
* [Projetos](#projects)
* [Outras](#other)

### Ativos

* [[!UICONTROL Criar um ativo]](#create-an-asset)
* [[!UICONTROL Excluir um ativo]](#delete-an-asset)
* [[!UICONTROL Obter um ativo]](#get-an-asset)
* [[!UICONTROL Listar Assets]](#list-assets)
* [[!UICONTROL Atualizar um ativo]](#update-an-asset)
* [[!UICONTROL Ativo de observação excluído]](#watch-asset-deleted)
* [[!UICONTROL Rótulo do ativo de observação atualizado]](#watch-asset-label-updated)
* [[!UICONTROL Assista ao novo ativo]](#watch-new-asset)

#### [!UICONTROL Criar um ativo]

Este módulo de ação cria um novo ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto para o qual você deseja criar um ativo, ou mapeie sua ID.</p> </td> 
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
  </tr> 
  <!--
   <tr> 
    <td role="rowheader">File Type </td> 
    <td> <p>Select the type of file you want to upload.</p> </td> 
   </tr>
   <tr> 
    <td role="rowheader">File Size </td> 
    <td> <p>The file size in bytes.</p> </td> 
   </tr>
  --> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Se estiver criando um arquivo, insira o URL do arquivo que você deseja fazer upload.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Se estiver criando um arquivo, insira uma breve descrição do ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rótulo] </td> 
   <td> <p>Se estiver criando um arquivo, selecione se ele está em andamento, precisa de revisão ou se foi aprovado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um ativo]

Este módulo de ação exclui um ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
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

#### [!UICONTROL Obter um ativo]

Este módulo de ação recupera detalhes do ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
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

#### [!UICONTROL Listar Assets]

Este módulo de pesquisa recupera todos os ativos contidos na pasta do projeto especificado.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
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

#### [!UICONTROL Atualizar um ativo]

Esse módulo de ação permite atualizar o nome, a descrição ou os campos personalizados de um ativo existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
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

#### [!UICONTROL Ativo de observação excluído]

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
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rótulo do ativo de observação atualizado]

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
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assista ao novo ativo]

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
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Comentários

* [[!UICONTROL Criar um comentário]](#create-a-comment)
* [[!UICONTROL Excluir um comentário]](#delete-a-comment)
* [[!UICONTROL Obter um comentário]](#get-a-comment)
* [[!UICONTROL Listar comentários]](#list-comments)
* [[!UICONTROL Atualizar um comentário]](#update-a-comment)
* [[!UICONTROL Assista ao comentário atualizado]](#watch-comment-updated)
* [[!UICONTROL Assistir ao Novo Comentário]](#watch-new-comment)

#### [!UICONTROL Criar um comentário]

Este módulo de ação adiciona um novo comentário ou uma resposta ao ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Selecione se deseja criar um comentário ou responder a um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto que contém o ativo ao qual você deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto que contém o ativo ao qual você deseja adicionar um comentário, ou mapeie sua ID.</p> </td> 
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
   <td> <p> Insira o conteúdo de texto do comentário ou da resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Insira o número do quadro no vídeo ao qual o comentário deve ser vinculado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um comentário]

Este módulo de ação exclui um comentário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe]</td> 
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

#### [!UICONTROL Obter um comentário]

Este módulo de ação recupera detalhes do comentário especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
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
   <td> <p>Selecione o comentário sobre o qual você deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar comentários]

Este módulo de pesquisa recupera todos os comentários do ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
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

#### [!UICONTROL Atualizar um comentário]

Este módulo de ação edita um comentário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione ou mapeie a equipe proprietária do projeto que contém o ativo no qual você deseja atualizar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecione o projeto que contém o ativo no qual você deseja atualizar um comentário.</p> </td> 
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
   <td> <p> Insira o conteúdo de texto do comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Insira o número do quadro no vídeo ao qual o comentário está vinculado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assista ao comentário atualizado]

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
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assistir ao Novo Comentário]

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
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione a equipe para a qual este webhook foi criado.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projetos

#### [!UICONTROL Listar projetos]

Este módulo de pesquisa recupera todos os projetos da equipe especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Equipe] </td> 
   <td> <p>Selecione ou mapeie a equipe para a qual deseja recuperar projetos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Insira ou mapeie o número máximo de projetos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outras

#### [!UICONTROL Fazer uma chamada de API]

Este módulo permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo a <code>https://api.frame.io</code>. Exemplo: <code> /v2/teams</code></p> <p>Observação: para obter a lista de pontos de acesso disponíveis, consulte a Referência de API do [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Insira a string de consulta da solicitação. Para cada parâmetro que você deseja incluir na string de consulta, clique em <b>[!UICONTROL Add item]</b> e insira o nome do campo e o valor desejado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
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

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
