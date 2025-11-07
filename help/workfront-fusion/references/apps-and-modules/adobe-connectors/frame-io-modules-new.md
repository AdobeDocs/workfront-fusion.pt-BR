---
title: Módulos do Frame.io
description: A conta  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] .
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 52dbf75ebb65a1de1a7a86619af4c7633e0cbe03
workflow-type: tm+mt
source-wordcount: '4399'
ht-degree: 1%

---

# [!DNL Frame.io] módulos V4

>[!IMPORTANT]
>
>Este artigo descreve a nova versão do conector Frame.io. Esse conector é usado para conectar ao Frame.io versão 4.
>
>Para obter instruções sobre a versão herdada do conector Frame.io, consulte [Conector herdado Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

Os módulos do Adobe Workfront Fusion [!DNL Frame.io] permitem monitorar, criar, atualizar, recuperar ou excluir ativos e comentários em sua conta do [!DNL Frame.io].

O Workfront oferece dois conectores Frame.io, com base na versão do Frame.io à qual você está se conectando.

| Conector  | Versão do Frame.io |
|---|---|
| Frame.io | V4 |
| Frame.io (Herdado) | V3 |

Para obter instruções sobre a versão herdada do conector Frame.io, consulte [Conector herdado Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


Para obter uma introdução ao vídeo sobre o conector Frame.io, consulte:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

Para usar módulos [!DNL Frame.io], você deve ter uma conta [!DNL Frame.io]

## Informações da API do Frame.io

O conector Frame.io usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td> https://api.frame.io/v4</td> 
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

## Conectar [!DNL Frame.io] ao [!UICONTROL Adobe Workfront Fusion]

Você pode se conectar automaticamente com credenciais de usuário, criar manualmente uma conexão de credencial de usuário ou criar uma conexão de servidor para servidor.

* [Conectar-se automaticamente com credenciais de usuário](#connect-automatically-with-user-credentials#)
* [Criar uma conexão de credenciais do usuário manualmente](#create-a-user-credentials-connection-manually)
* [Criar uma conexão de servidor para servidor](#create-a-server-to-server-connection)

### Conectar-se automaticamente com credenciais de usuário

Este método cria uma conexão automaticamente se você estiver conectado ao Frame.io ou conecta você à página de logon do Frame.io para que você possa fazer logon.

1. Em qualquer módulo Frame.io, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.
1. Insira um nome para a conexão.
1. Clique em **Continuar**.
1. Se for solicitado que você faça logon em sua conta Frame.io, faça isso.
1. Se você fizer parte de mais de uma organização Frame.io, selecione a organização que deseja usar para essa conexão.

A conexão é criada.

### Criar uma conexão de credenciais do usuário manualmente

Você pode criar uma conexão de credenciais do usuário fazendo logon no Frame.io ou fornecendo uma ID do cliente ou um Segredo do cliente.

Para criar uma conexão servidor a servidor, primeiro você deve configurar um aplicativo no Adobe Developer Console.

* [Criar credenciais de usuário na Adobe Developer Console](#create-user-credentials-in-the-adobe-developer-console)
* [Configurar uma conexão de autenticação de usuário](#configure-a-user-authentication-connection)

#### Criar credenciais de usuário na Adobe Developer Console

Se você ainda não tiver credenciais de servidor para servidor em um projeto do Adobe Developer Console, poderá criá-las.

1. Abra o [Adobe Developer Console](https://developer.adobe.com/).
1. Selecione um projeto existente no Adobe Developer Console para usar nesta conexão

   Ou

   Crie um novo projeto na Adobe Developer Console. Para obter instruções, consulte [Criar um projeto vazio](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Na página Visão geral do projeto ou na página Introdução ao novo projeto, clique em **Adicionar API**.
1. Na página que abre, localize e clique em **API Frame.io**.
1. Na página Selecionar tipo de autenticação, selecione **Autenticação de Usuário** e clique em **Avançar**.
1. Na página Adicionar uma credencial de autenticação de usuário, selecione **OAuth Web App** e clique em **Avançar**.
1. Na página Configurar credencial do aplicativo web OAuth, digite o seguinte:   <table style="table-layout:auto">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL URI de redirecionamento padrão]</td>
          <td>
            <p><code>https://oauth.app.workfrontfusion.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Padrão de URI de redirecionamento]</td>
          <td>
            <p><code>https://oauth\.app\.workfrontfusion\.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
       </tbody>
    </table>
1. Clique em **Avançar**.
1. Clique em **Salvar API configurada**.
1. Na página do produto, clique no cartão das credenciais que você acabou de criar.

   Aqui, você pode encontrar sua ID do cliente e o Segredo do cliente.

>[!NOTE]
>
> Recomendamos deixar essa janela aberta quando você começar a configurar sua conexão no Adobe Workfront Fusion. Você pode copiar a ID do cliente, recuperar e copiar o Segredo do cliente desta página para colar nos campos de conexão.


#### Configurar uma conexão de autenticação de usuário

1. Em qualquer módulo Frame.io, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.
1. Na caixa Criar uma conexão, clique em **Mostrar configurações avançadas**.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Tipo de conexão]</td>
          <td>
            <p>Selecione <b>Autenticação de usuário do IMS</b>.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Nome da Conexão]</td>
          <td>
            <p>Insira um nome para esta conexão.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID do Cliente]</td>
          <td>Insira sua [!DNL Adobe] [!UICONTROL ID do Cliente]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como criar credenciais, consulte <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Criar credenciais de usuário no Adobe Developer Console</a> neste artigo.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Segredo do Cliente]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como criar credenciais, consulte <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Criar credenciais de usuário no Adobe Developer Console</a> neste artigo.</p>
        </tr>
       </tbody>
    </table>
1. Se for solicitado que você faça logon em sua conta Frame.io, faça isso.
1. Se você fizer parte de mais de uma organização Frame.io, selecione a organização que deseja usar para essa conexão.

A conexão é criada.


### Criar uma conexão de servidor para servidor

Para criar uma conexão servidor a servidor, primeiro você deve configurar um aplicativo no Adobe Developer Console.

* [Criar credenciais de servidor para servidor no Adobe Developer Console](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [Configurar uma conexão servidor a servidor](#configure-a-server-to-server-connection)

#### Criar credenciais de servidor para servidor no Adobe Developer Console

Se você ainda não tiver credenciais de servidor para servidor em um projeto do Adobe Developer Console, poderá criá-las.

1. Abra o [Adobe Developer Console](https://developer.adobe.com/).
1. Selecione um projeto existente no Adobe Developer Console para usar nesta conexão

   Ou

   Crie um novo projeto na Adobe Developer Console. Para obter instruções, consulte [Criar um projeto vazio](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Na página Visão geral do projeto ou na página Introdução ao novo projeto, clique em **Adicionar API**.
1. Na página que abre, localize e clique em **API Frame.io**.
1. Na página Selecionar tipo de autenticação, selecione **Autenticação de Servidor para Servidor** e clique em **Avançar**.
1. Insira um nome para as credenciais. Isso permite identificar as credenciais posteriormente na área Credenciais da API do Adobe Admin Console.
1. Clique em **Avançar**.
1. Na página Selecionar perfis de produto, selecione o perfil de produto que inclui a conta Frame.io à qual você deseja se conectar.
1. Clique em **Salvar API configurada**.
1. Na página do produto, clique no cartão das credenciais que você acabou de criar.

   Aqui, você pode encontrar sua ID do cliente e o Segredo do cliente.

>[!NOTE]
>
> Recomendamos deixar essa janela aberta quando você começar a configurar sua conexão no Adobe Workfront Fusion. Você pode copiar a ID do cliente, recuperar e copiar o Segredo do cliente desta página para colar nos campos de conexão.


#### Configurar uma conexão servidor a servidor

1. Em qualquer módulo Frame.io, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Tipo de conexão]</td>
          <td>
            <p>Selecione <b>Servidor IMS para Servidor</b>.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Nome da Conexão]</td>
          <td>
            <p>Insira um nome para esta conexão.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID do Cliente]</td>
          <td>Insira sua [!DNL Adobe] [!UICONTROL ID do Cliente]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como criar credenciais, consulte <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Criar credenciais de servidor para servidor no Adobe Developer Console</a> neste artigo.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Segredo do Cliente]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como criar credenciais, consulte <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Criar credenciais de servidor para servidor no Adobe Developer Console</a> neste artigo.</p>
        </tr>
       </tbody>
    </table>
1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.




## [!DNL Frame.io] módulos e seus campos

Ao configurar módulos do [!DNL Frame.io], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Frame.io] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ativos](#assets)
* [Comentários](#comments)
* [Pastas](#folders)
* [Projetos](#projects)
* [Compartilhamento](#shares)
* [Espaços de trabalho](#workspaces)
* [Metadados](#metadata)
* [Outras](#other)

### Ativos

* [[!UICONTROL Criar um ativo]](#create-an-asset)
* [[!UICONTROL Excluir um ativo]](#delete-an-asset)
* [[!UICONTROL Obter um ativo]](#get-an-asset)
* [[!UICONTROL Listar ativos]](#list-assets)
* [Inspecionar ativo excluído](#watch-asset-deleted)
* [Observar novo ativo](#watch-new-asset)

#### [!UICONTROL Criar um ativo] <!--different for v4-->

Este módulo de ação cria um novo ativo. Você pode fazer upload de um arquivo local ou fornecer o URL de um arquivo remoto do qual criar o ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que contém o projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione o espaço de trabalho ou mapeie a ID do espaço de trabalho que contém o projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Projeto] </td> 
   <td> <p>Selecione o projeto ou mapeie a ID do projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Caminho] </td> 
   <td> <p>Selecione o caminho onde deseja criar um ativo.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Enter the name of the file that you want to use for this asset.</p> </td> 
  </tr> -->
    <tr> 
    <td role="rowheader">Tipo de upload </td> 
    <td> <p>Selecione se você está criando um ativo de um arquivo local ou de uma vida remota.</p> </td> 
   </tr>
    <tr> 
    <td role="rowheader">Tamanho do arquivo </td> 
    <td> <p>Se você estiver fazendo upload de um arquivo local, insira ou mapeie o tamanho do arquivo em bytes.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL URL DO Source] </td> 
   <td> <p>Se estiver criando o ativo a partir de um arquivo remoto, insira o URL do arquivo do qual deseja fazer upload.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de origem.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Select the media type for this asset.</p> </td> 
  </tr> -->
  </tbody> 
</table>

#### [!UICONTROL Criar um ativo (Herdado)] <!--different for v4-->

Este módulo de ação cria um novo ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que contém o projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione o espaço de trabalho ou mapeie a ID do espaço de trabalho que contém o projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Projeto] </td> 
   <td> <p>Selecione o projeto ou mapeie a ID do projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Caminho] </td> 
   <td> <p>Selecione o caminho onde deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Arquivo] </td> 
   <td> <p>Insira o nome do arquivo que deseja usar para este ativo.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Tamanho do arquivo </td> 
    <td> <p>Insira ou mapeie o tamanho do arquivo em bytes.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL URL DO Source] </td> 
   <td> <p>Se estiver criando um arquivo, insira o URL do arquivo do qual deseja fazer upload.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de mídia] </td> 
   <td> <p>Selecione o tipo de mídia para este ativo.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL Excluir um ativo]

Esse módulo de ação exclui um ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que contém o ativo que você deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Ativo] </td> 
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
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que contém o ativo que você deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Ativo] </td> 
   <td> <p>Selecione ou mapeie o ativo que deseja recuperar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar ativos]

Este módulo de pesquisa recupera todos os ativos na pasta do projeto especificado.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que contém os ativos que você deseja listar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de ativos retornados] </td> 
   <td> <p>Insira ou mapeie o número máximo de ativos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Inspecionar ativo excluído

Este módulo de acionamento inicia um cenário quando um ativo é excluído.

Selecione o webhook que deseja usar para esse módulo ou clique em Adicionar ao lado do campo Webhook e insira as seguintes informações:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Webhook] </td> 
   <td> <p>Insira um nome para o novo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que deseja observar para ativos excluídos.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Observar novo ativo

Esse módulo de acionador inicia um cenário quando um novo ativo é criado.

Selecione o webhook que deseja usar para esse módulo ou clique em Adicionar ao lado do campo Webhook e insira as seguintes informações:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Webhook] </td> 
   <td> <p>Insira um nome para o novo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que você deseja observar para novos ativos.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Comentários

* [[!UICONTROL Criar um comentário]](#create-a-comment)
* [[!UICONTROL Excluir um comentário]](#delete-a-comment)
* [[!UICONTROL Obter um comentário]](#get-a-comment)
* [[!UICONTROL Listar comentários]](#list-comments)
* [[!UICONTROL Atualizar um comentário]](#update-a-comment)
* [Assista ao comentário atualizado](#watch-comment-updated)
* [Assista ao novo comentário](#watch-new-comment)

#### [!UICONTROL Criar um comentário]

Esse módulo de ação adiciona um novo comentário ou resposta ao ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que contém o ativo ao qual você deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione a conta ou mapeie a ID do espaço de trabalho que contém o ativo ao qual você deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Projeto] </td> 
   <td> <p>Selecione o projeto ou mapeie a ID do projeto que contém o ativo ao qual você deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Caminho] </td> 
   <td> <p>Selecione o caminho para o ativo ao qual deseja adicionar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Texto]</td> 
   <td> <p> Insira o conteúdo do texto do comentário ou da resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carimbo de Data/Hora] </td> 
   <td> <p>Insira o número do quadro no vídeo ao qual o comentário deve ser vinculado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Página] </td> 
   <td> <p>Se o ativo for uma PDF, insira ou mapeie a página à qual o comentário deve ser anexado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um comentário]

Este módulo de ação exclui um comentário existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que contém o comentário que você deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Comentário] </td> 
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
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que contém o comentário sobre o qual você deseja recuperar detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Comentário] </td> 
   <td> <p>Selecione o comentário sobre o qual deseja recuperar detalhes.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém o ativo do qual deseja recuperar comentários.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione ou mapeie o espaço de trabalho que contém o ativo do qual deseja recuperar comentários.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Projeto] </td> 
   <td> <p>Selecione o projeto que contém o ativo do qual deseja recuperar comentários.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Caminho] </td> 
   <td> <p>Selecione o caminho que leva ao ativo do qual deseja listar comentários.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de comentários retornados] </td> 
   <td> <p>Insira ou mapeie o número máximo de comentários que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um comentário]

Este módulo de ação edita um comentário existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém o projeto que contém o ativo no qual você deseja atualizar um comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Comentário] </td> 
   <td> <p>Selecione o comentário que deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Texto]</td> 
   <td> <p> Insira o conteúdo do texto do comentário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carimbo de Data/Hora] </td> 
   <td> <p>Insira o número do quadro no vídeo ao qual o comentário está vinculado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Página] </td> 
   <td> <p>Se o ativo for uma PDF, insira ou mapeie a página à qual o comentário está anexado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Assista ao comentário atualizado

Este módulo de acionamento inicia um cenário quando um comentário é atualizado.

Selecione o webhook que deseja usar para esse módulo ou clique em Adicionar ao lado do campo Webhook e insira as seguintes informações:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Webhook] </td> 
   <td> <p>Insira um nome para o novo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que deseja observar para ver comentários atualizados.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Assista ao novo comentário

Este módulo de acionamento inicia um cenário quando um comentário é criado.

Selecione o webhook que deseja usar para esse módulo ou clique em Adicionar ao lado do campo Webhook e insira as seguintes informações:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Webhook] </td> 
   <td> <p>Insira um nome para o novo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que deseja observar para novos comentários.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pastas

#### Criar uma pasta

Este módulo de ação cria uma nova pasta no Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta na qual deseja criar uma pasta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione ou mapeie o espaço de trabalho em que deseja criar uma pasta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Projeto] </td> 
   <td> <p>Selecione a onde deseja criar uma pasta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Caminho] </td> 
   <td> <p>Selecione o caminho no qual deseja criar uma pasta.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Insira ou mapeie um nome para a nova pasta.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projetos

* [Criar um projeto](#create-a-project)
* [Convidar usuários para o projeto Frame.io](#invite-users-to-frameio-project)
* [Listar projetos](#list-projects)

#### Criar um projeto

Este módulo de ação cria um novo projeto no Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta na qual deseja criar um projeto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione ou mapeie o espaço de trabalho em que deseja criar um projeto.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Insira ou mapeie um nome para o novo projeto.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Convidar usuários para o projeto Frame.io

Este módulo de ação convida os usuários para o projeto Frame.io especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém o projeto para o qual você deseja convidar um usuário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione ou mapeie o espaço de trabalho que contém o projeto para o qual você deseja convidar um usuário.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID do projeto </td> 
   <td> <p>Selecione ou mapeie o projeto para o qual você deseja convidar um usuário.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de usuário </td> 
   <td> <p>Selecione ou mapeie o usuário que deseja convidar para o projeto.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar Projetos]

Este módulo de pesquisa recupera todos os projetos da equipe especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém o ativo do qual deseja recuperar projetos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione ou mapeie o espaço de trabalho que contém o ativo do qual deseja recuperar projetos.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de projetos retornados] </td> 
   <td> <p>Inserir ou mapear o número máximo de projetos
   você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Compartilhamento

* [Adicionar um ativo a um link de compartilhamento](#add-an-asset-to-a-share-link)
* [Criar um link de compartilhamento](#create-a-share-link)

#### Adicionar um ativo a um link de compartilhamento

Esses módulos de ação adicionam um ativo a um link de compartilhamento no Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém o link de compartilhamento ao qual você deseja adicionar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compartilhar ID de link] </td> 
   <td> <p>Selecione ou mapeie o link de compartilhamento ao qual você deseja adicionar um ativo.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL ID de Ativo] </td> 
   <td> <p>Insira ou mapeie a ID do ativo que deseja adicionar ao link de compartilhamento.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Criar um link de compartilhamento

Este módulo de ação cria um novo link de compartilhamento no Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta na qual deseja criar um link de compartilhamento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione ou mapeie o espaço de trabalho em que deseja criar um link de compartilhamento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Projeto] </td> 
   <td> <p>Selecione ou mapeie o projeto no qual deseja criar um link de compartilhamento.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Acesso </td> 
   <td> <p>Selecione se este link tem acesso público ou restrito.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Ativos </td> 
   <td> <p>Para cada ativo que você deseja adicionar ao link de compartilhamento, clique em <b>Adicionar item</b> e insira a ID do ativo.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Descrição </td> 
   <td> <p>Insira ou mapeie uma descrição para o link de compartilhamento.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Insira ou mapeie a data de expiração do link de compartilhamento.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Insira ou mapeie um nome para o novo link de compartilhamento.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Insira ou mapeie uma senha para o link de compartilhamento.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Espaços de trabalho

#### Criar um espaço de trabalho

Este módulo de ação cria um novo espaço de trabalho no Frame.io

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta na qual deseja criar um espaço de trabalho.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome] </td> 
   <td> <p>Insira ou mapeie um novo nome para o espaço de trabalho.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Listar espaços de trabalho

Este módulo lista todos os espaços de trabalho em uma conta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém o ativo do qual você deseja recuperar espaços de trabalho.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de espaços de trabalho retornados] </td> 
   <td> <p>Insira ou mapeie o número máximo de espaços de trabalho
   você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Metadados

* [Criar um campo de nível de conta](#create-an-account-level-field)
* [Excluir um campo de nível de conta](#delete-an-account-level-field)
* [Obter metadados](#get-metadata)
* [Listar campos de nível de conta](#list-account-level-fields)
* [Atualizar uma definição de campo de nível de conta](#update-an-account-level-field-definition)
* [Atualizar metadados em vários arquivos](#update-metadata-across-multiple-files)

#### Criar um campo de nível de conta

Esse módulo de ação cria e configura um novo campo de metadados no nível da conta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta na qual deseja criar os metadados.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Tipo de campo </td> 
   <td> <p>Selecione o tipo de campo de metadados que deseja criar e configure as opções desse campo.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Insira ou mapeie um nome para o novo campo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um campo de nível de conta

Esse módulo de ação exclui um único campo de metadados de nível de conta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém o campo de metadados que você deseja excluir.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de definição de campo </td> 
   <td> <p>Insira ou mapeie a ID do campo que deseja excluir. Você pode encontrar IDs de campo com o módulo List account level fields.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obter metadados

Este módulo de ação recupera os metadados de um arquivo no Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém o arquivo para o qual deseja recuperar metadados.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID do arquivo </td> 
   <td> <p>Insira ou mapeie a ID do arquivo para o qual deseja recuperar metadados.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Mostrar nulo </td> 
   <td> <p>Ative essa opção para incluir campos com um valor nulo na saída.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Listar campos de nível de conta

Este módulo recupera uma lista de campos de metadados no nível da conta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta da qual deseja listar campos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de contratos retornados]</td> 
   <td> <p>Insira ou mapeie o número máximo de campos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar uma definição de campo de nível de conta

Esse módulo atualiza a definição de um único campo de metadados existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta na qual deseja criar os metadados.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de definição de campo </td> 
   <td> <p>Insira ou mapeie a ID do campo que você deseja atualizar. Você pode encontrar IDs de campo com o módulo List account level fields.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Tipo de campo </td> 
   <td> <p>Se desejar alterar o tipo de campo do campo, selecione o tipo de campo de metadados que deseja criar e configure as opções desse campo.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Insira ou mapeie um novo nome para o campo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar metadados em vários arquivos

Esse módulo atualiza campos de metadados em um ou mais arquivos com valores especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione ou mapeie a conta que contém os arquivos para os quais deseja atualizar os metadados.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecione o espaço de trabalho ou mapeie a ID do espaço de trabalho que contém o projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Projeto] </td> 
   <td> <p>Selecione o projeto ou mapeie a ID do projeto para o qual você deseja criar um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs de Arquivo] </td> 
   <td> <p>Para cada arquivo para o qual deseja atualizar os metadados, clique em <b>Adicionar item</b> e insira ou mapeie a ID do arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valores] </td> 
   <td> <p>Para cada campo para o qual deseja atualizar os metadados, clique em <b>Adicionar item</b> e insira ou mapeie a ID da definição do campo e o valor que deseja colocar nesse campo. Todos os arquivos especificados no campo IDs de arquivo são atualizados com esse valor de campo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outras

* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Observar valor de metadados atualizado](#watch-metadata-value-updated)


#### [!UICONTROL Fazer uma chamada de API personalizada]

Este módulo permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo para <code>https://api.frame.io</code>. Exemplo: <code> /v4/me</code></p> <p>Observação: para obter a lista de endpoints disponíveis, consulte a Referência de API [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Método]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de consulta] </td> 
   <td> <p>Insira a string de consulta da solicitação. Para cada parâmetro que você deseja incluir na cadeia de caracteres de consulta, clique em <b>[!UICONTROL Adicionar item]</b> e insira o nome do campo e o valor desejado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Observar valor de metadados atualizado

Este módulo de acionamento inicia um cenário quando um comentário é atualizado.

Selecione o webhook que deseja usar para esse módulo ou clique em Adicionar ao lado do campo Webhook e insira as seguintes informações:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Webhook] </td> 
   <td> <p>Insira um nome para o novo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar o [!DNL Frame.io] ao Adobe Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Conta] </td> 
   <td> <p>Selecione a conta ou mapeie a ID da conta que deseja observar para valores de metadados atualizados.</p> </td> 
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
