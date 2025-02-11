---
title: HTTP > Criar um módulo de solicitação OAuth 2.0
description: Para fazer uma solicitação  [!DNL Adobe Workfront Fusion] HTTP(S) para servidores que exigem uma autorização OAuth 2.0, primeiro é necessário criar uma conexão OAuth. [!DNL Adobe Workfront Fusion] garante que todas as chamadas feitas com esta conexão tenham os cabeçalhos de autorização apropriados e atualizem automaticamente os tokens associados quando necessário.
author: Becky
feature: Workfront Fusion
exl-id: a302a1d4-fddf-4a71-adda-6b87ff7dba4b
source-git-commit: a7ee3e751b75523c4da62cea71e59a63f98b95e0
workflow-type: tm+mt
source-wordcount: '1978'
ht-degree: 0%

---

# Módulo [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]

>[!NOTE]
>
>[!DNL Adobe Workfront Fusion] requer uma licença [!DNL Adobe Workfront Fusion] além de uma licença [!DNL Adobe Workfront].

Para fazer uma solicitação HTTP(S) [!DNL Adobe Workfront Fusion] para servidores que exigem uma autorização OAuth 2.0, primeiro é necessário criar uma conexão OAuth. [!DNL Adobe Workfront Fusion] garante que todas as chamadas feitas com esta conexão tenham os cabeçalhos de autorização apropriados e atualizem automaticamente os tokens associados quando necessário.

[!DNL Workfront Fusion] oferece suporte aos seguintes fluxos de autenticação do OAuth 2.0:

* Fluxo de código de autorização
* Fluxo implícito

Outros fluxos, como Fluxo de Credenciais de Senha do Proprietário do Recurso e Fluxo de Credenciais do Cliente, não são automaticamente compatíveis por meio desse módulo.

Para obter mais informações sobre a autenticação OAuth 2.0, consulte [A Estrutura de Autorização OAuth 2.0](https://tools.ietf.org/html/rfc6749).

>[!NOTE]
>
>Se você estiver se conectando a um produto Adobe que não tem um conector dedicado no momento, recomendamos usar o módulo Adobe Authenticator.
>
>Para obter mais informações, consulte [módulo Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

## Criar uma conexão para uma solicitação [!DNL OAuth]

* [Instruções gerais para criar uma conexão no HTTP > Criar um módulo de solicitação OAuth 2.0](#general-instructions-for-creating-a-connection-in-the-http--make-an-oauth-20-request-module)
* [Instruções para criar uma conexão com o Google no http > [!UICONTROL Make] um módulo de solicitação OAuth 2.0](#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module)
* [Instruções para conexão com a API Graph do Microsoft por meio do HTTP > Criar um módulo de solicitação OAuth 2.0](#instructions-for-connecting-to-microsoft-graph-api-via-the-http--make-an-oauth-20-request-module)

### Instruções gerais para criar uma conexão no módulo [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]

1. Crie um cliente OAuth no serviço [!DNL target] com o qual você deseja que [!DNL Adobe Workfront Fusion] se comunique. Esta opção provavelmente foi encontrada na seção [!UICONTROL Developer] do serviço fornecido.

   1. Ao criar um cliente, insira a URL apropriada no campo `[!UICONTROL Redirect URL]` ou `[!UICONTROL Callback URL]`:

      | Américas / APAC | `https://app.workfrontfusion.com/oauth/cb/oauth2` |
      |---|---|
      | **EMEA** | `https://app-eu.workfrontfusion.com/oauth/cb/oauth2` |

   1. Após a criação do cliente, o serviço fornecido exibe duas chaves: `[!UICONTROL Client ID]` e `[!UICONTROL Client Secret]`. Alguns serviços chamam estes `[!UICONTROL App Key]` e `[!UICONTROL App Secret]`. Salve a chave e o segredo em um local seguro, para que você possa fornecê-los ao criar a conexão no Workfront Fusion.

1. Localize o `[!UICONTROL Authorize URI]` e `[!UICONTROL Token URI]` na documentação de API do serviço especificado. Esses são endereços de URL através dos quais [!DNL Workfront Fusion] se comunica com o serviço [!DNL target]. Os endereços são usados para autorização OAuth.

   >[!NOTE]
   >
   >Se o serviço usar o Fluxo implícito, você precisará somente do `[!UICONTROL Authorize URI]`.

1. (Condicional) Se o serviço de destino usa escopos (direitos de acesso), verifique como o serviço separa escopos individuais e certifique-se de definir o separador nas configurações avançadas adequadamente. Se o separador não estiver definido corretamente, [!DNL Workfront Fusion] falhará ao criar a conexão e você receberá um erro de escopo inválido.
1. Após concluir as etapas acima, você pode começar a criar a conexão OAuth em [!DNL Workfront Fusion]. Adicione o HTTP > Criar um módulo de solicitação OAuth 2 ao seu cenário.
1. No campo Conexão do módulo, clique em **[!UICONTROL Add]**.

1. Preencha os seguintes campos para criar uma conexão:

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>Insira o nome da conexão.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Environment] </td> 
      <td> <p>Selecione se você está usando um ambiente de produção ou não.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Type] </td> 
      <td> <p>Selecione se você está usando uma conta de serviço ou uma conta pessoal.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>Selecione o fluxo para obter tokens.</p> 
       <ul> 
        <li><strong>[!UICONTROL Authorization Code]</strong>: insira o <code>[!UICONTROL Authorize URI]</code> e <code>[!UICONTROL Token URI]</code> da documentação da API do serviço.</li> 
        <li><strong>[!UICONTROL Implicit]</strong>: insira o <code>[!UICONTROL Authorize URI]</code> na documentação da API do serviço.</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>Adicionar escopos individuais. Você pode encontrar essas informações na documentação do desenvolvedor (API) do serviço específico.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>Selecione os escopos inseridos acima que devem ser separados por. Você pode encontrar essas informações na documentação do desenvolvedor (API) do serviço específico.</p> <p>Aviso: se o separador não estiver definido corretamente, [!DNL Workfront Fusion] falhará ao criar a conexão e você receberá um erro de escopo inválido.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>Insira a ID do cliente. Você obteve a ID do cliente ao criar um cliente OAuth no serviço que deseja conectar.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p> Digite o segredo do cliente. Você obteve o Segredo do cliente ao criar um cliente OAuth no serviço que deseja conectar.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>Adicione os parâmetros que deseja incluir na chamada de autorização. Os seguintes parâmetros padrão são sempre incluídos automaticamente e não precisam ser adicionados.</p> <p>Parâmetros padrão:</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL response_type]</strong> </p> <p> <code>code </code>para [!UICONTROL Authorization Code flow] e <code>token </code>para [!UICONTROL Implicit flow]</p> </li> 
        <li> <p><strong>[!UICONTROL redirect_uri]</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">Américas / APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong> </p> <p> A ID do cliente recebida ao criar a conta</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Access token parameters]</p> </td> 
      <td> <p>Adicione os parâmetros que deseja incluir na chamada de token. Os seguintes parâmetros padrão são sempre incluídos automaticamente e não precisam ser adicionados.</p> <p>Parâmetros padrão:</p> 
       <ul> 
        <li><strong>[!UICONTROL grant_type]</strong>: <code>authorization_code</code></li> 
        <li> <p><strong>[!UICONTROL redirect_uri]:</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">Américas / APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li><strong>[!UICONTROL client_id]</strong>: a ID do cliente recebida ao criar a conta é incluída automaticamente no corpo da solicitação</li> 
        <li><strong>client_secret</strong>: o Segredo do Cliente recebido ao criar a conta é automaticamente incluído no corpo da solicitação</li> 
        <li><strong>código</strong>: o código retornado pela solicitação de autorização</li> 
       </ul> <p>Nota:  <p>O padrão OAuth 2.0 oferece suporte a pelo menos dois métodos de autenticação de cliente durante esta etapa (<code>[!UICONTROL client_secret_basic]</code> e <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] envia automaticamente a ID de cliente e a senha especificadas pelo método <code>[!UICONTROL client_secret_post]</code>. Portanto, esses parâmetros são incluídos automaticamente como parte do corpo da solicitação de token. </p> <p>Para obter mais informações sobre a autenticação OAuth 2.0, consulte <a href="https://tools.ietf.org/html/rfc6749">A Estrutura de Autorização OAuth 2.0</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Refresh token parameters]</p> </td> 
      <td> <p>Adicione os parâmetros que deseja incluir na chamada de token. Os seguintes parâmetros padrão são sempre incluídos automaticamente e não precisam ser adicionados.</p> <p>Parâmetros padrão:</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL grant_type]</strong>: <code>refresh_token</code></p> </li> 
        <li> <p><strong>[!UICONTROL refresh_token]</strong>: o token de atualização mais recente obtido pelo serviço ao qual você está se conectando</p> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong>: a ID do cliente recebida ao criar a conta é incluída automaticamente no corpo da solicitação</p> </li> 
        <li> <p><strong>[!UICONTROL client_secret]</strong>: o segredo do cliente recebido ao criar a conta é incluído automaticamente no corpo da solicitação</p> </li> 
       </ul> <p>Nota:  <p>O padrão OAuth 2.0 oferece suporte a pelo menos dois métodos de autenticação de cliente durante esta etapa (<code>[!UICONTROL client_secret_basic]</code> e <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] envia automaticamente a ID de cliente e a senha especificadas pelo método <code>[!UICONTROL client_secret_post]</code>. Portanto, esses parâmetros são incluídos automaticamente como parte do corpo da solicitação de token. </p> <p>Para obter mais informações sobre a autenticação OAuth 2.0, consulte <a href="https://tools.ietf.org/html/rfc6749">A Estrutura de Autorização OAuth 2.0</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Custom Headers]</p> </td> 
      <td> <p>Especifique quaisquer chaves e valores adicionais para incluir no cabeçalho das etapas [!UICONTROL Token] e R[!UICONTROL efresh Token].</p> <p>Nota:  <p>O padrão OAuth 2.0 oferece suporte a pelo menos dois métodos de autenticação de cliente durante esta etapa (<code>[!UICONTROL client_secret_basic]</code> e <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] não dá suporte automático ao método <code>[!UICONTROL client_secret_basic]</code>. Se o serviço ao qual você está se conectando espera que a ID do cliente e o Segredo do cliente sejam combinados em uma única cadeia de caracteres e, em seguida, codificada em base64 no cabeçalho de Autorização, adicione esse cabeçalho e o valor da chave aqui.</p> <p> Para obter mais informações sobre a autenticação OAuth 2.0, consulte <a href="https://tools.ietf.org/html/rfc6749">A Estrutura de Autorização OAuth 2.0</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Token placement]</p> </td> 
      <td> <p>Selecione se deseja enviar o token no [!UICONTROL header], [!UICONTROL query string] ou em ambos ao conectar-se à URL especificada.</p> <p>Os tokens são enviados com mais frequência no cabeçalho da solicitação.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Header token name] </td> 
      <td> <p>Insira o nome do token de autorização no cabeçalho. Padrão: <code>[!UICONTROL Bearer]</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Query string parameter name] </td> 
      <td> <p>Insira o nome do token de autorização na cadeia de caracteres de consulta. Padrão: <code>[!UICONTROL access_token]</code>.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continue]** para salvar a conexão e retornar ao módulo.
1. Continue em [Configurar o módulo Criar uma solicitação OAuth 2.0](#configure-the-make-an-oauth-20-request-module).

### Instruções para criar uma conexão com [!DNL Google] em [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request module]

O exemplo a seguir mostra como usar o módulo de solicitação [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0] para se conectar a [!DNL Google].

1. Verifique se você criou um projeto, definiu as configurações de OAuth e gerou suas credenciais conforme descrito no artigo[Conectar [!DNL Adobe Workfront Fusion] a [!DNL Google Services] usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).
1. Abra o módulo [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request].
1. Clique em **[!UICONTROL Add]** ao lado da caixa de conexão.
1. Insira os seguintes valores:

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>Insira um nome para a conexão.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Environment] </td> 
      <td> <p>Selecione se você está usando um ambiente de produção ou não.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Type] </td> 
      <td> <p>Selecione se você está usando uma conta de serviço ou uma conta pessoal.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>[!UICONTROL Authorization Code]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Authorize URI]</td> 
      <td><code>https://accounts.google.com/o/oauth2/v2/auth</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Token URI]</td> 
      <td><code>https://www.googleapis.com/oauth2/v4/token</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>Adicionar escopos individuais. Para obter mais informações sobre escopos, consulte <a href="https://developers.google.com/identity/protocols/oauth2/scopes">Escopos do OAuth 2.O para [!DNL Google] APIs</a> na documentação do [!DNL Google].</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>[!UICONTROL SPACE]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>Insira sua ID de cliente do [!DNL Google]. </p> <p>Para criar uma ID de cliente, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create-oauth-credentials" class="MCXref xref">Criar credenciais OAuth</a> no artigo [!DNL Connect Adobe Workfront Fusion] para [!DNL Google Services] usando um cliente OAuth personalizado</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p>Insira seu Segredo do Cliente do [!DNL Google]. </p> <p>Para criar um segredo de cliente, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create-oauth-credentials" class="MCXref xref">Criar credenciais OAuth</a> no artigo [!DNL Connect Adobe Workfront Fusion] para [!DNL Google] Serviços usando um cliente OAuth personalizado</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>Adicionar <code>[!UICONTROL access_type]</code> - <code>[!UICONTROL offline] </code>par de valor-chave.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-authentication-http.png"> </p> <p>Observação: se você tiver problemas de autenticação, por exemplo, com a atualização de token, tente adicionar o par de valores-chave <code>[!UICONTROL prompt] </code>- <code>[!UICONTROL consent] </code>.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continue]** para salvar as configurações de conexão.
1. Continue em [Configurar o módulo Criar uma solicitação OAuth 2.0](#configure-the-make-an-oauth-20-request-module).

## Configurar o módulo Criar uma solicitação do OAuth 2.0

Depois de estabelecer uma conexão OAuth 2.0, continue configurando o módulo conforme desejado. Todos os tokens de autorização são incluídos automaticamente nessa solicitação e em qualquer outra solicitação que use a mesma conexão.

Ao configurar o módulo [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto">  
 <col> 
 <col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter informações sobre como configurar uma conexão, consulte <a href="#create-a-connection-for-an-oauth-request" class="MCXref xref">Criar uma conexão para uma solicitação OAuth</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx)] </td> 
   <td> <p>Use esta opção para configurar o tratamento de erros.</p> <p>Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Tratamento de erros</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Insira o URL para o qual você deseja enviar uma solicitação, como um endpoint de API, site etc.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Por exemplo, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Insira os pares de valor-chave da consulta desejados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>O Corpo HTTP são os bytes de dados transmitidos em uma mensagem de transação HTTP imediatamente após os cabeçalhos, se houver algum a ser usado.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>O tipo de corpo bruto geralmente é adequado para a maioria das solicitações de corpo HTTP, mesmo em situações em que a documentação do desenvolvedor não especifica os dados a serem enviados.</p> <p>Especifique um formulário de análise de dados no campo [!UICONTROL Content type].</p> <p>Apesar do tipo de conteúdo selecionado, os dados são inseridos em qualquer formato estipulado ou exigido pela documentação do desenvolvedor.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>Este tipo de corpo é para POSTAR dados usando <code>[!UICONTROL application/x-www-form-urlencoded]</code>.</p> <p>Para <code>[!UICONTROL application/x-www-form-urlencoded]</code>, o corpo da mensagem HTTP enviada ao servidor é essencialmente uma cadeia de caracteres de consulta. As chaves e os valores são codificados em pares de valores chave separados por <code>&amp;</code> e por um <code>=</code> entre a chave e o valor. </p> <p>Para dados binários, <code>use [!UICONTROL multipart/form-data]</code> em vez disso.</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>Exemplo: </b></span></span> 
       <p>Exemplo do formato de solicitação HTTP resultante:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>O [!UICONTROL Multipart/form-data] é uma solicitação HTTP de várias partes usada para enviar arquivos e dados. Normalmente, é usado para carregar arquivos no servidor.</p> <p>Adicione campos a serem enviados na solicitação. Cada campo deve conter um par de valores chave.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>Informe a chave e o valor a serem enviados dentro do corpo da solicitação.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Informe a chave e especifique o arquivo de origem que deseja enviar no corpo da solicitação.</p> <p>Mapeie o arquivo que você deseja carregar do módulo anterior (como [!UICONTROL HTTP] &gt; [!UICONTROL Get a File]) ou insira o nome do arquivo e os dados do arquivo manualmente.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Habilite esta opção para analisar respostas automaticamente e converter respostas JSON e XML para que você não precise usar os módulos [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON] ou [!UICONTROL XML] &gt; [!UICONTROL Parse XML].</p> <p>Antes de usar o conteúdo JSON ou XML analisado, execute o módulo uma vez manualmente para que o módulo possa reconhecer o conteúdo da resposta e permitir que você o mapeie em módulos subsequentes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>Insira o tempo limite da solicitação em segundos (1-300). O padrão é 40 segundos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> Habilite essa opção para compartilhar cookies do servidor com todos os módulos HTTP em seu cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p>Para usar um certificado autoassinado ou uma chave privada para TLS, clique em <b>Extrair</b> e forneça o arquivo e a senha do certificado ou da chave privada.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>Habilite esta opção para rejeitar conexões que estejam usando certificados TLS não verificados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> Ative essa opção para seguir os redirecionamentos de URL com respostas 3xx.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>Ative essa opção para seguir os redirecionamentos de URL com todos os códigos de resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>Por padrão, [!DNL Workfront Fusion] manipula vários valores para a mesma chave de parâmetro da cadeia de caracteres de consulta da URL que as matrizes. Por exemplo, <code>www.test.com?foo=bar&amp;foo=baz</code> será convertido em <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Ative esta opção para desativar este recurso. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> Habilite esta opção para solicitar uma versão compactada do site.</p> <p>Isso adiciona um cabeçalho <code>[!UICONTROL Accept-Encoding]</code> para solicitar conteúdo compactado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>Habilite esta opção para usar o TLS mútuo na solicitação HTTP.</p> <p>Para obter mais informações sobre TLS Mútuo, consulte <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">Usar TLS Mútuo em módulos HTTP em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
