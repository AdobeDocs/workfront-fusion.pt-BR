---
title: Módulos do SharePoint
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Microsoft SharePoint Online, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
TQID: 'https://experienceleague.adobe.com/WmECfdPt-a3l2-WT9LMX2HB-7-p-BLIO4F2i3OAc7D0'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: c9bf5c68e4977027944114c35414fa5f46ea8751
workflow-type: tm+mt
source-wordcount: '5853'
ht-degree: 10%
---
# Módulos do Microsoft SharePoint Online

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Microsoft SharePoint Online, bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Baseado em operação: disponível para organizações com licenças baseadas em operação</p>
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

Para usar os módulos do Microsoft SharePoint Online, você deve ter uma conta do Microsoft SharePoint Online.

## Informações da API do SharePoint

O conector do SharePoint usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
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

## Conectar o Microsoft SharePoint Online ao Workfront Fusion {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [Conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma conta  [!DNL Microsoft] &#x200B;](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [Conectar o Microsoft SharePoint Online ao Workfront Fusion usando configurações avançadas](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)
* [Conectar o Microsoft SharePoint Online ao Workfront Fusion usando a autorização de certificado](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-certificate-authorization)
* [Conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma entidade de serviço](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-service-principal)

### Conecte o Microsoft SharePoint Online ao Workfront Fusion usando uma conta [!DNL Microsoft]

+++ Expanda para exibir instruções para conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma conta do Microsoft.

Você pode usar sua conta do [!DNL Microsoft] para criar uma conexão com o Microsoft SharePoint Online. Para obter instruções sobre como conectar sua conta do [!DNL Sharepoint] ao Workfront Fusion, consulte [Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

+++

### Conectar o Microsoft SharePoint Online ao Workfront Fusion usando configurações avançadas

+++ Expanda para exibir instruções para conectar o Microsoft SharePoint Online ao Workfront Fusion usando configurações avançadas.

Para incluir credenciais na conexão, habilite a opção Mostrar configurações avançadas. Para esse tipo de conexão, você precisa de uma ID do cliente, um Segredo do cliente e uma ID do locatário.

1. Em qualquer módulo do SharePoint, clique em **[!UICONTROL Adicionar]** próximo ao campo Conexão para abrir a caixa **[!UICONTROL Criar uma conexão]**.
1. Clique em **[!UICONTROL Mostrar configurações avançadas]**.
1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection type]</p> </td> 
      <td>Para usar as credenciais do cliente, selecione <b>Email do Microsoft 365</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Insira um nome para a conexão.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client ID]</p> </td> 
      <td>Insira a ID do cliente do aplicativo SharePoint ao qual você está se conectando. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Segredo do cliente]</p> </td> 
      <td>Insira o segredo do cliente para o aplicativo SharePoint ao qual você está se conectando.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL ID de Locatário]</p> </td> 
      <td>Insira a ID do locatário do aplicativo SharePoint ao qual você está se conectando.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **Continuar** para salvar a conexão e retornar ao módulo.

+++

### Conectar o Microsoft SharePoint Online ao Workfront Fusion usando a autorização de certificado

+++ Expanda para exibir instruções para conectar o Microsoft SharePoint Online ao Workfront Fusion usando a autorização de certificado.

Você pode usar a autorização de certificado para se conectar ao SharePoint.

>[!IMPORTANT]
>
>Para usar a autorização do certificado, primeiro você deve criar um aplicativo no Microsoft Entra e carregar o certificado lá.
>
>Para obter instruções, consulte [Como configurar autoridades de certificação para autenticação baseada em certificado do Microsoft Entra](https://learn.microsoft.com/en-us/entra/identity/authentication/how-to-configure-certificate-authorities) na documentação do Microsoft.

1. Em qualquer módulo do SharePoint, clique em **[!UICONTROL Adicionar]** próximo ao campo Conexão para abrir a caixa **[!UICONTROL Criar uma conexão]**.
1. Clique em **[!UICONTROL Mostrar configurações avançadas]**.
1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection type]</p> </td> 
      <td>Para usar autorização de certificado, selecione <b>Microsoft SharePoint Online (Autenticação do Certificado)</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Insira um nome para a conexão.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client ID]</p> </td> 
      <td>Insira a ID do cliente do aplicativo SharePoint ao qual você está se conectando. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Impressão Digital]</p> </td> 
      <td>Insira a impressão digital do aplicativo SharePoint ao qual você está se conectando.</td> 
     </tr> 
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Insira o certificado ou a chave privada que foi gerada quando suas credenciais foram criadas no Microsoft. </p>
          <p>Para extrair a chave privada ou o certificado:</p>
          <ol>
            <li>
              <p>Clique em <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li>
            <p>Selecione se você está extraindo um certificado ou uma chave privada.</li>
            <li>
              <p>Selecione o tipo de arquivo que você está extraindo.</p>
            </li>
            <li>
              <p>Selecione o arquivo que contém a chave privada ou o certificado.</p>
            </li>
            <li>
              <p>Insira a senha do arquivo.</p>
            </li>
            <li>
              <p>Clique em <b>[!UICONTROL Save]</b> para extrair o arquivo e retornar à configuração de conexão.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody> 
   </table>

1. Clique em **Continuar** para salvar a conexão e retornar ao módulo.

+++

### Conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma entidade de serviço

+++ Expanda para exibir instruções para conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma entidade de serviço.

Você pode criar uma conexão que use uma entidade de serviço (uma conexão da API do aplicativo) em vez de uma conta pessoal. Isso é útil quando você deseja que a conexão seja executada como uma identidade de aplicativo ou serviço, em vez de uma pessoa específica — por exemplo, para que a integração não seja interrompida se essa pessoa sair da empresa ou alterar sua senha.

>[!IMPORTANT]
>
>Este tipo de conexão está disponível somente para o módulo [Fazer uma Chamada de API](#make-an-api-call). Outros módulos do SharePoint exigem um dos outros tipos de conexão descritos neste artigo.

* [Pré-requisitos para conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma entidade de serviço](#prerequisites-to-connecting-microsoft-sharepoint-online-to-workfront-fusion-using-a-service-principal)
* [Criar o registro do aplicativo na Microsoft Entra ID](#create-the-app-registration-in-microsoft-entra-id)
* [Criar um segredo do cliente](#create-a-client-secret)
* [Conceder permissões de API](#grant-api-permissions)
* [Coletar detalhes da conexão](#collect-your-connection-details)
* [Criar a conexão](#create-the-connection)

#### Pré-requisitos para conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma entidade de serviço

Você precisa de acesso de **Administrador Global**, **Administrador de Aplicativos** ou **Administrador de Função Privilegiada** à Microsoft Entra ID para registrar o aplicativo e conceder permissões. Se você não tiver esse acesso, peça a alguém da sua equipe de TI ou de identidade que conclua essas etapas para você.

Prossiga para [Criar o registro do aplicativo na Microsoft Entra ID](#create-the-app-registration-in-microsoft-entra-id).

#### Criar o registro do aplicativo na Microsoft Entra ID (Entidade de serviço)

1. Entre no centro de administração [!DNL Microsoft Entra].
1. Ir para **[!UICONTROL Registros de aplicativo]** > **[!UICONTROL Novo registro]**.
1. Dê ao aplicativo um nome claro e reconhecível. Por exemplo, `Make - SharePoint Integration`.
1. Deixe **[!UICONTROL URI de redirecionamento]** em branco. Essa conexão não envolve ninguém que faça logon por meio de um navegador.
1. Selecione **[!UICONTROL Registrar]**.
1. Continue em [Criar um segredo de cliente](#create-a-client-secret).

#### Criar um segredo do cliente (Entidade de serviço)

1. No novo registro do aplicativo, acesse **[!UICONTROL Certificados e segredos]**.
1. Selecione **[!UICONTROL Novo segredo do cliente]**, adicione uma descrição e escolha um período de expiração.
1. Selecione **[!UICONTROL Adicionar]**.
1. Copie o **[!UICONTROL Valor]** do segredo imediatamente. É exibido apenas uma vez. Se você navegar para fora antes de copiá-lo, deverá criar um novo.
1. Continue em [Conceder permissões de API](#grant-api-permissions).

#### Conceder permissões de API (Entidade de serviço)

>[!IMPORTANT]
>
>BECKY CHECK ME: diferente do Azure DevOps, o Microsoft Graph oferece suporte às permissões de aplicativo diretamente nesta etapa. Confirme as permissões exatas que o módulo Fazer uma chamada de API precisa (por exemplo, um escopo de permissão Sites) antes de publicar esta seção e atualize as etapas abaixo de acordo.

1. No registro do seu aplicativo, acesse **[!UICONTROL Permissões de API]**.
1. Selecione **[!UICONTROL Adicionar uma permissão]** e **[!UICONTROL Gráfico do Microsoft]**.
1. Selecione **[!UICONTROL Permissões do aplicativo]**.
1. Selecione a(s) permissão(ões) necessária(s) para suas chamadas de API e **[!UICONTROL Adicionar permissões]**.
1. Selecione **[!UICONTROL Conceder consentimento administrativo]** à sua organização e, em seguida, confirme.
1. Prossiga para [Coletar detalhes da conexão](#collect-your-connection-details).

#### Coletar seus detalhes de conexão (Entidade de serviço)

Na página **[!UICONTROL Visão geral]** do registro do aplicativo, observe os seguintes valores. Você os insere ao criar a conexão no módulo.

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader">[!UICONTROL ID de Locatário]</td>
   <td>Na página Visão Geral, rotulada <b>ID do Diretório (locatário)</b>.</td>
  </tr>
  <tr>
   <td role="rowheader">[!UICONTROL Client ID]</td>
   <td>Na página Visão Geral, rotulada <b>ID do Aplicativo (cliente)</b>.</td>
  </tr>
  <tr>
   <td role="rowheader">[!UICONTROL Client Secret]</td>
   <td>O valor copiado em <a href="#create-a-client-secret" class="MCXref xref">Criar um segredo de cliente</a>.</td>
  </tr>
 </tbody>
</table>

Continue em [Criar a conexão](#create-the-connection).

#### Criar a conexão (Entidade de serviço)

1. No módulo [!UICONTROL Fazer uma Chamada de API], clique em **[!UICONTROL Adicionar]** próximo ao campo Conexão para abrir a caixa **[!UICONTROL Criar uma conexão]**.
1. Clique em **[!UICONTROL Mostrar configurações avançadas]**.
1. No campo [!UICONTROL Tipo de conexão], selecione **[!UICONTROL Entidade de Serviço]**.
1. Insira o seguinte:

   * [!UICONTROL ID do inquilino]
   * [!UICONTROL ID do cliente]
   * [!UICONTROL Segredo do cliente]

1. Clique em **Continuar** para salvar a conexão e retornar ao módulo.

   Se tudo estiver configurado corretamente, a conexão será validada com êxito.

+++

### Conectar o Microsoft SharePoint Online ao Adobe Workfront Fusion usando uma conexão federada

+++ Expanda para exibir instruções para conectar o Microsoft SharePoint Online ao Adobe Workfront Fusion usando uma conexão federada.

Uma conexão federada funciona como a conexão principal de serviço, exceto por não usar um segredo de cliente.
Em vez de armazenar um segredo, você informa ao Microsoft Entra ID para confiar em tokens que o Workfront Fusion emite para uma conexão específica. Quando a conexão é executada, o Fusion apresenta uma prova de identidade de curta duração e o Microsoft Entra ID retorna um token de acesso. Como não há segredo do cliente, não há nada que expire e nenhum segredo para girar ou armazenar.

>[!NOTE]
>
>A configuração dessa conexão leva duas visitas ao centro de administração do Microsoft Entra. Registre o aplicativo primeiro, crie a conexão no Workfront Fusion e retorne ao Microsoft Entra ID para adicionar a credencial federada. Isso ocorre porque a credencial federada identifica uma conexão específica e esse identificador não existe até que a conexão seja criada.

* [Pré-requisitos para conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma conexão federada](#prerequisites-to-connecting-microsoft-sharepoint-online-to-workfront-fusion-using-a-federated-connection)
* [Criar o registro do aplicativo na Microsoft Entra ID (Federated connection)](#create-the-app-registration-in-microsoft-entra-id-federated-connection)
* [Conceder permissões de API (conexão Federada)](#grant-api-permissions-federated-connection)
* [Coletar detalhes da conexão (Conexão federada)](#collect-your-connection-details-federated-connection)
* [Criar a conexão no Workfront Fusion (conexão Federada)](#create-the-connection-in-workfront-fusion-federated-connection)
* [Adicionar a credencial federada na Microsoft Entra ID (conexão Federada)](#add-the-federated-credential-in-microsoft-entra-id-federated-connection)
* [Verificar a conexão (Conexão federada)](#verify-the-connection-federated-connection)
* [Solução de problemas](#troubleshooting)

#### Pré-requisitos para conectar o Microsoft SharePoint Online ao Workfront Fusion usando uma conexão federada

Você precisa de acesso de Administrador Global, Administrador de Aplicativos ou Administrador de Função Privilegiada no Microsoft Entra ID para registrar o aplicativo, conceder permissões e adicionar a credencial federada. Se você não tiver esse acesso, peça a alguém da sua equipe de TI ou de identidade que conclua essas etapas para você.

#### Criar o registro do aplicativo na Microsoft Entra ID (Federated connection)

1. Faça logon no centro de administração do Microsoft Entra.
1. Acesse Registros do aplicativo > Novo registro.
1. Dê ao aplicativo um nome claro e reconhecível. Por exemplo, `Workfront Fusion SharePoint Integration`.
1. Deixe o URL de redirecionamento em branco. Essa conexão não envolve ninguém que faça logon por meio de um navegador.
1. Selecione **Registrar**.
Não crie um segredo de cliente. Uma conexão federada não usa uma.
1. Continue para Conceder permissões de API.


#### Conceder permissões de API (conexão Federada)

1. No registro do seu aplicativo, acesse **Permissões de API**.
1. Selecione **Adicionar uma permissão** e **Gráfico do Microsoft**.
1. Selecione **Permissões do aplicativo**.
1. Selecione a(s) permissão(ões) necessária(s) para suas chamadas de API e **Adicionar permissões**.
1. Selecione **Dar consentimento administrativo** para sua organização e confirme.
1. Prossiga para [Coletar detalhes da conexão](#collect-your-connection-details-federated-connection).


#### Coletar detalhes da conexão (Conexão federada)

1. Na página Visão geral do registro do aplicativo, observe os seguintes valores. Você os insere ao criar a conexão no módulo.

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL ID de Locatário]</td>
      <td>Na página Visão Geral, rotulada <b>ID do Diretório (locatário)</b>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Client ID]</td>
      <td>Na página Visão Geral, rotulada <b>ID do Aplicativo (cliente)</b>.</td>
     </tr>
    </tbody>
   </table>

1. Continue em [Criar a conexão no Workfront Fusion](#create-the-connection-in-workfront-fusion-federated-connection).

#### Criar a conexão no Workfront Fusion (conexão Federada)

1. No módulo Fazer uma chamada de API, clique em b próximo ao campo Conexão para abrir a caixa Criar uma conexão.
1. Clique em (Federated connection).
1. No campo Tipo de conexão, selecione o tipo de conexão federada.
1. Insira o seguinte:

   * ID do inquilino
   * ID do cliente

1. Selecione **Criar**.
O Workfront Fusion exibe três valores. Você as usa no próximo procedimento.

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL Emissor]</td>
      <td>Sempre <code>https://oidc.automations.adobe.com</code>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Assunto]</td>
      <td>Identifica esta conexão. Parece com <code>fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964</code>. É diferente para cada conexão criada.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Público-alvo]</td>
      <td>Sempre <code>api://AzureADTokenExchange</code>.</td>
     </tr>
    </tbody>
   </table>


1. Deixe este painel aberto e copie o valor de **Assunto**.

   >[!NOTE]
   >
   >Não feche o painel nem selecione Cancelar. A conexão não será concluída até que você conclua os procedimentos restantes. Se fechar o painel, você deverá excluir a conexão e iniciar novamente, pois uma nova conexão recebe um novo Assunto.


1. Continue para [Adicionar a credencial federada na Microsoft Entra ID](#add-the-federated-credential-in-microsoft-entra-id-federated-connection).

#### Adicionar a credencial federada na Microsoft Entra ID (conexão Federada)

Esse procedimento substitui o segredo do cliente. Ele instrui o Microsoft Entra ID a aceitar tokens que o Workfront Fusion emite para essa conexão única.

1. Em uma nova guia do navegador, retorne ao centro de administração do Microsoft Entra e abra o registro do aplicativo.
1. Vá para **Certificados e segredos** > **Credenciais federadas**.
1. Selecione **Adicionar credencial**.
1. Em Cenário de credencial federada, selecione **Outro emissor**.
1. Insira o seguinte:

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL Emissor]</td>
      <td><code>https://oidc.automations.adobe.com</code>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Identificador de Assunto]</td>
      <td>O Assunto copiado do Workfront Fusion. Cole exatamente, sem espaços adicionados.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Um nome que identifica esta conexão, para que você possa localizá-la posteriormente. Por exemplo, <code>workfront-fusion-connection-28964</code>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Público-alvo]</td>
      <td><code>api://AzureADTokenExchange</code>. Isso geralmente é preenchido para você. Deixe o valor padrão.</td>
     </tr>
    </tbody>
   </table>

1. Selecione **Adicionar**.
1. Continue em [Verificar a conexão](#verify-the-connection-federated-connection).


#### Verificar a conexão (Conexão federada)

1. Retorne à guia do navegador Workfront Fusion, onde o painel de conexão ainda está aberto.
2. Selecione **Salvar**.

   * Se tudo estiver configurado corretamente, a conexão será validada com êxito e você poderá continuar a configuração do módulo.
   * Se a verificação falhar, o painel permanecerá aberto e exibirá o erro. Corrija o problema na Microsoft Entra ID e selecione Salvar novamente. Não é necessário recriar a conexão, e o Assunto não é alterado.


#### Solução de problemas


<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader">Falha na verificação da conexão com um cliente inválido ou erro de solicitação inválido</td>
   <td>A Microsoft Entra ID não pôde corresponder o token a uma credencial federada. Verifique se o Emissor é exatamente <code>https://oidc.automations.adobe.com</code> sem barra à direita e se o identificador de Assunto é idêntico caractere por caractere ao Assunto mostrado no Workfront Fusion. Um Assunto copiado de uma conexão diferente é a causa mais comum.</td>
  </tr>
  <tr>
   <td role="rowheader">A conexão é verificada, mas as chamadas de API retornam 403</td>
   <td>A identidade é confiável, mas o aplicativo não tem as permissões do Gráfico do Microsoft necessárias para sua chamada. Retorne para Conceder permissões de API, adicionar a permissão de aplicativo necessária e conceder consentimento administrativo.</td>
  </tr>
  <tr>
   <td role="rowheader">Não é possível adicionar outra credencial federada</td>
   <td>Você atingiu o limite de 20 credenciais federadas para esse registro de aplicativo. Registre um aplicativo adicional e crie outras conexões com ele.</td>
  </tr>
 </tbody>
</table>

+++

## Módulos do Microsoft SharePoint e seus campos

Ao configurar módulos do Microsoft SharePoint Online, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Microsoft SharePoint Online podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Item da unidade](#drive-item)
* [Item](#item)
* [Lista](#list)
* [Página (Beta)](#page-beta)
* [Site](#site)
* [Outras](#other)

### Item da unidade

* [Criar um arquivo](#create-a-file)
* [Criar um arquivo (herdado)](#create-a-file-legacy)
* [Criar uma pasta](#create-a-folder)
* [Obter um arquivo](#get-a-file)
* [Obter uma pasta](#get-a-folder)
* [Atualizar uma pasta ou um arquivo](#update-a-folder-or-a-file)
* [Observar itens da pasta](#watch-folder-items)

#### Criar um arquivo

Esse módulo retorna cria um arquivo no SharePoint. Este módulo tem melhor desempenho do que o módulo Criar um arquivo (Herdado).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Source file] </td>
      <td><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p></td>
  </tr>  </tbody> 
</table>



#### Criar um arquivo (herdado)

Este módulo cria um arquivo no SharePoint.

Para obter um melhor desempenho, recomendamos usar o módulo [Criar um arquivo](#create-a-file).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Source file]</td> 
      <td><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p></td>
  </tr>  </tbody> 
</table>

#### Criar uma pasta

Este módulo de ação cria uma nova pasta no SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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

#### Obter uma pasta

Este módulo recuperou detalhes sobre a pasta especificada

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site, Unidade e IDs de Arquivo]</td> 
   <td> <p>Selecione como você deseja identificar o local do arquivo que deseja obter.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL Caminho da Pasta]</strong> para a pasta que você deseja recuperar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o local da pasta. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Atualizar uma pasta ou um arquivo

Este módulo de ação atualiza os metadados de uma pasta ou arquivo

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site, Unidade e IDs de Arquivo]</td> 
   <td> <p>Selecione como você deseja identificar o local do arquivo que deseja obter.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL ID de Pasta ou item]</strong> para a pasta ou arquivo que você deseja recuperar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o local da pasta. </p> </li> 
    </ul> </td> 
  </tr> 
  </tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Para cada campo de metadados que você deseja atualizar, clique em <b>Adicionar item</b> e insira o caminho e o valor do campo.</td> 
  <tr>
</tbody> 
</table>

#### Observar itens da pasta

Este módulo de acionamento inicia um cenário quando um item é atualizado em uma pasta selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir Site, Unidade e IDs de Pasta]</td> 
   <td> <p>Selecione como você deseja identificar o local do arquivo que deseja obter.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>, <strong>[!UICONTROL ID da Lista]</strong> e <strong>[!UICONTROL ID da pasta]</strong> nos campos exibidos.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o local da pasta que deseja observar. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira o número máximo de itens que o Workfront Fusion deve retornar durante um ciclo de execução de cenário.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Item

* [[!UICONTROL Copiar um Item]](#copy-an-item)
* [[!UICONTROL Criar um item]](#create-an-item)
* [[!UICONTROL Excluir um item]](#delete-an-item)
* [[!UICONTROL Obter um Item]](#get-an-item)
* [Obter detalhes](#get-details)
* [[!UICONTROL Listar itens]](#list-items)
* [[!UICONTROL Mover um Item]](#move-an-item)
* [[!UICONTROL Atualizar um item]](#update-an-item)
* [[!UICONTROL Itens de observação] (Agendados)](#watch-items-scheduled)


#### [!UICONTROL Copiar um Item]

Este módulo de ação copia um item existente em uma lista do SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Fields]</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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

#### Obter detalhes

Esse módulo obtém detalhes do item do URL especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL da Web</td> 
   <td> Insira ou mapeie o URL do item para o qual deseja recuperar detalhes. </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Limit]</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Fields]</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Limit]</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Description]</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Limit]</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de listas que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Página (Beta)

>[!NOTE]
>
>As APIs na versão `beta` em [!DNL Microsoft Graph] estão sujeitas a alterações. O uso dessas APIs em aplicativos de produção não é compatível.

* [Obter uma página](#get-a-page)
* [Listar páginas](#list-pages)
* [Publicar uma página](#publish-a-page)
* [Assistir páginas](#watch-pages)

#### [!UICONTROL Obter uma página]

Este módulo de ação retorna os dados de uma página especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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

#### Listar páginas

Este módulo recupera uma lista de todas as páginas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listar Páginas]</td> 
   <td> <p>Selecione como você deseja identificar as páginas que deseja listar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong> do site que contém as páginas que você deseja listar.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém as páginas que você deseja listar.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de páginas que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Publicar uma página

Esse módulo de ação publica a versão mais recente da página selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Publicar uma página]</td> 
   <td> <p>Selecione como você deseja identificar a página que deseja publicar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID do Site]</strong>e <strong>[!UICONTROL ID da Página]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o site que contém a página que você deseja publicar e selecione a página.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Assistir páginas

Esse módulo de acionador inicia um cenário quando uma página é modificada no site especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID do Site]</td> 
   <td> <p>Selecione como você deseja identificar as páginas que deseja listar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL ID do Site]</strong> do site que contém as páginas que você deseja assistir.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista que você segue]</strong> </p> <p>Selecione o site que contém as páginas que você deseja visualizar.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de páginas que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Palavra-chave do Nome para Exibição]</td> 
   <td> <p>Insira ou mapeie o termo de pesquisa que você deseja pesquisar nos sites.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de sites que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outras

* [Obter alterações](#get-changes)
* [Fazer uma chamada de API](#make-an-api-call)
* [Monitorar eventos](#watch-events)

#### Obter alterações

Este módulo recupera adições, atualizações e exclusões feitas na pasta do SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft SharePoint Online ao Workfront Fusion, consulte <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar o Microsoft SharePoint Online ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo a <code>https://graph.microsoft.com</code>. Exemplo:<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Por exemplo, <code>{"Content-type":"application/json"}</code>. O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Adicione a consulta para a chamada de API na forma de um objeto JSON padrão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selecione o tipo de dados que deseja enviar na chamada de API.</td> 
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

#### Monitorar eventos

Esse módulo de acionador instantâneo inicia um cenário quando um item é adicionado, atualizado ou excluído no SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to Workfront Fusion, see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecione um webhook existente ou clique em Adicionar e insira a conexão para criar um novo webhook.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
