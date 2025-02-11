---
title: Chamar a API REST do MS Graph
description: Chamar a API REST do MS Graph por meio do Adobe Workfront Fusion HTTP &> Criar um módulo de solicitação OAuth 2.0
author: Becky
feature: Workfront Fusion
exl-id: f411c807-955d-44fe-98b1-3ebba3fe0861
source-git-commit: a7ee3e751b75523c4da62cea71e59a63f98b95e0
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 2%

---

# Chamar a API REST do MS Graph

Muitos serviços da Web do Microsoft são acessados por meio da API do Microsoft Graph. É possível criar uma conexão com a API do Graph do Microsoft, usando o módulo de solicitação Workfront Fusion HTTP > Make an OAuth 2.0.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront 
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
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecione ou Prime Workfront Plan: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Registrar o Workfront Fusion no Portal de Registro de Aplicativos do Microsoft

Para criar uma conexão com a API REST do Microsoft Graph, primeiro registre o Adobe Workfront Fusion.

1. Comece a registrar um novo aplicativo conforme descrito em [Registre um aplicativo com a Microsoft identity platform](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) na documentação do Microsoft.

   Como parte do registro, o Microsoft exige as seguintes informações:

   <table style="table-layout:auto">
      <tr>
        <td>Nome do aplicativo</td>
        <td>Insira um nome para o aplicativo, como "Meu aplicativo do Workfront Fusion".</td>
      </tr>
      <tr>
        <td>Redirecionar URL</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/oauth2</code></td>
      </tr>
    </table>

1. Após concluir o registro do aplicativo, anote a ID do aplicativo.

   >[!IMPORTANT]
   >
   >Você precisará da ID do aplicativo para configurar sua conexão no Workfront Fusion.

1. Gerar um Segredo do Cliente. Anote este segredo.

   Para obter instruções, consulte [Registrar um aplicativo com a Microsoft identity platform](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) na documentação do Microsoft.

   >[!IMPORTANT]
   >
   >Você precisará do Segredo do cliente para configurar sua conexão no Workfront Fusion.

1. Configure as permissões para seu aplicativo.

   Para obter informações específicas sobre como localizar e configurar esses campos, consulte a seção &quot;Configurar permissões para o Gráfico do Microsoft&quot; em [Obter acesso sem um usuário](https://docs.microsoft.com/en-us/graph/auth-v2-service) na documentação do Microsoft.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Que tipo de permissões seu aplicativo requer?</td> 
      <td>Selecione <code>Delegated permissions</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Selecionar permissões</td> 
      <td> <p>Selecione as seguintes permissões:</p> 
       <ul> 
        <li> <p><code>offline_access</code> </p> </li> 
        <li> <p><code>openid</code> </p> </li> 
        <li> <p>Quaisquer outras permissões necessárias às suas integrações (Exemplo: <code>User.Read</code>)</p> </li> 
       </ul> <p><b>Importante</b>: você precisará das permissões selecionadas para configurar sua conexão no Workfront Fusion.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Continue em [Configurar sua conexão com a API do MS Graph no Workfront Fusion](#configure-your-ms-graph-api-connection-in-workfront-fusion).

## Configurar sua conexão da API do MS Graph no Workfront Fusion

Depois de registrar o Workfront Fusion como discutido em [Registrar o Workfront Fusion no Portal de Registro de Aplicativos do Microsoft](#register-workfront-fusion-in-the-microsoft-application-registration-portal), você pode configurar sua conexão no módulo de solicitação HTTP > Criar um Oauth 2.0.

1. Adicione um HTTP > Faça um módulo de chamada OAuth 2.0 ao seu cenário.
1. Clique em **Adicionar** ao lado do campo de conexão.
1. Configure os campos de conexão da seguinte maneira:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Nome da conexão</td> 
      <td>Insira um nome para a conexão.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Ambiente</p> </td> 
      <td>Selecione se você está se conectando a uma conta de produção ou não produção. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Tipo</p> </td> 
      <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Tipo de fluxo</p> </td> 
      <td>Selecione <code>Authorization Code</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Autorizar URI</td> 
      <td>Digite <code>https://login.microsoftonline.com/common/oauth2/v2.0/authorize</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">URI do token</td> 
      <td>Digite <code>https://login.microsoftonline.com/common/oauth2/v2.0/token</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Escopo</td> 
      <td> <p>Insira as permissões que você selecionou ao se registrar, conforme discutido em <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registrar o Workfront Fusion no Portal de Registro de Aplicativos do Microsoft</a>.</p> <p>Para cada escopo, clique em <b>Adicionar</b> e digite a permissão.</p> <p>Exemplo: <code>offline_access</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Separador de escopo</td> 
      <td>Selecione <code>SPACE</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">ID do cliente</td> 
      <td>Insira a ID do Aplicativo da etapa 2 em <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registrar o Workfront Fusion no Portal de Registro de Aplicativos do Microsoft</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Segredo do cliente</td> 
      <td>Insira o Segredo do Cliente gerado na etapa 3 em <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registrar o Workfront Fusion no Portal de Registro de Aplicativos do Microsoft</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Autorizar parâmetros</td> 
      <td> <p>Adicione os seguintes parâmetros Authorize. Para cada parâmetro que você está adicionando, clique em <b>Adicionar item</b> e insira o seguinte: </p> 
       <ul> 
        <li> <p>Chave:<code> response_mode</code> Valor: <code>query</code></p> </li> 
        <li> <p>Chave: <code>prompt </code>Valor: <code>consent</code></p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Parâmetros de token de acesso</td> 
      <td>Não é necessário inserir nada nesse campo.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Atualizar parâmetros de token</td> 
      <td> 
       <ol> 
        <li value="1"> <p>Clique em <b>Adicionar item</b>.</p> </li> 
        <li value="2"> <p>No campo <b>Chave</b>, digite <code>scope</code>.</p> </li> 
        <li value="3"> <p>No campo <b>Valor</b>, insira todos os escopos inseridos no campo de escopo, separados por espaços.</p> <p>Exemplo: <code>offline_access openid User.Read</code></p> </li> 
       </ol> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Cabeçalhos personalizados</td> 
      <td>Não é necessário inserir nada nesse campo.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Posicionamento do token</td> 
      <td><code>In the header</code> </td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **Continuar**.
1. Na janela exibida, clique em **Aceitar** para concluir a conexão e retornar ao módulo.
