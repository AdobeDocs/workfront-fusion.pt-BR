---
title: Módulos do Frame.io (Beta)
description: A conta  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] .
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: bf3e35a287c3beb2310a7b8d2c21c65aebfb9076
workflow-type: tm+mt
source-wordcount: '2168'
ht-degree: 1%

---

# [!DNL Frame.io] módulos do Beta (V4)

>[!IMPORTANT]
>
>Este artigo descreve a nova versão (beta) do conector Frame.io. Esse conector é usado para conectar ao Frame.io versão 4.
>
>Para obter instruções sobre a versão herdada do conector Frame.io, consulte [Conector herdado Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

Os módulos do [!DNL Adobe Workfront Fusion] [!DNL Frame.io] permitem monitorar, criar, atualizar, recuperar ou excluir ativos e comentários em sua conta do [!DNL Frame.io].

O Workfront oferece dois conectores Frame.io, com base na versão do Frame.io à qual você está se conectando.

| Conector | Versão do Frame.io |
|---|---|
| Frame.io (Beta) | V4 |
| Frame.io (Herdado) | V3 |

Para obter instruções sobre a versão herdada do conector Frame.io, consulte [Conector herdado Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


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

Para usar módulos [!DNL Frame.io], você deve ter uma conta [!DNL Frame.io]

## Informações da API do Frame.io

O conector Frame.io usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
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

O processo de conexão é diferente se você estiver usando o conector Legacy Frame.io ou o conector Beta Frame.io.

1. Em qualquer módulo Frame.io do Beta, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

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
            <p>Selecione se deseja criar uma conexão de autenticação de usuário IMD ou uma conexão de Servidor IMS para Servidor.</p>
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
          <td>Insira sua [!DNL Adobe] [!UICONTROL ID do Cliente]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor do Adobe.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Segredo do Cliente]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor do Adobe.</p>
        </tr>
       </tbody>
    </table>
1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## [!DNL Frame.io] módulos e seus campos

Ao configurar módulos do [!DNL Frame.io], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Frame.io] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ativos](#assets)
* [Comentários](#comments)
* [Pastas](#folders)
* [Projetos](#projects)
* [Compartilhamento](#shares)
* [Espaços de trabalho](#workspaces)
* [Outro](#other)

### Ativos

* [[!UICONTROL Criar um ativo]](#create-an-asset)
* [[!UICONTROL Excluir um ativo]](#delete-an-asset)
* [[!UICONTROL Obter um ativo]](#get-an-asset)
* [[!UICONTROL Listar ativos]](#list-assets)
* [[!UICONTROL Atualizar um ativo]](#update-an-asset)

#### [!UICONTROL Criar um ativo] <!--different for v4-->

Este módulo de ação cria um novo ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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

### Comentários

* [[!UICONTROL Criar um comentário]](#create-a-comment)
* [[!UICONTROL Excluir um comentário]](#delete-a-comment)
* [[!UICONTROL Obter um comentário]](#get-a-comment)
* [[!UICONTROL Listar comentários]](#list-comments)
* [[!UICONTROL Atualizar um comentário]](#update-a-comment)

#### [!UICONTROL Criar um comentário]

Esse módulo de ação adiciona um novo comentário ou resposta ao ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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

### Pastas

#### Criar uma pasta

Este módulo de ação cria uma nova pasta no Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
* [Listar projetos](#list-projects)

#### Criar um projeto

Este módulo de ação cria um novo projeto no Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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

#### [!UICONTROL Listar Projetos]

Este módulo de pesquisa recupera todos os projetos da equipe especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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

### Outro

#### [!UICONTROL Fazer uma chamada de API personalizada]

Este módulo permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Frame.io], consulte <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Conectar [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> neste artigo.</td> 
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
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de consulta] </td> 
   <td> <p>Insira a string de consulta da solicitação. Para cada parâmetro que você deseja incluir na cadeia de caracteres de consulta, clique em <b>[!UICONTROL Adicionar item]</b> e insira o nome do campo e o valor desejado.</p> </td> 
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


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
