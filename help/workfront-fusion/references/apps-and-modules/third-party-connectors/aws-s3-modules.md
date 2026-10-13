---
title: Módulos do AWS S3
description: Os módulos S3 [!DNL Adobe Workfront Fusion AWS] permitem executar operações em seus buckets S3.
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
TQID: 'https://experienceleague.adobe.com/FDkre6osF2kT7Kz-5VGradQLa7GPSJ6MHPH9-FgM-ag'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 7c25013f7a94000651e8331199ad985d40651ae3
workflow-type: tm+mt
source-wordcount: '2637'
ht-degree: 16%
---
# Módulos do AWS S3

Os módulos S3 [!DNL Adobe Workfront Fusion AWS] permitem executar operações em seus buckets S3.

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

Para usar os módulos do [!UICONTROL AWS S3], você deve ter uma conta [!DNL Amazon Web Service].

## Informações da API do AWS S3

O conector AWS S3 usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td><pre><code>https://s3.&#123;&#123;parameters.region&#125;&#125;.amazonaws.com</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL AWS] ao Workfront Fusion {#connect-aws-to-workfront-fusion}

* [Conectar o AWS ao Workfront Fusion usando uma conexão federada](#connect-aws-to-workfront-fusion-using-a-federated-connection)
* [Conectar o AWS ao Workfront Fusion usando um usuário da API](#connect-aws-to-workfront-fusion-using-an-api-user)

### Conectar o AWS ao Workfront Fusion usando uma conexão federada

+++ Expanda para exibir instruções desse tipo de conexão.

* [Pré-requisitos para conectar o AWS ao Workfront Fusion usando uma conexão federada](#prerequisites-to-connecting-aws-to-workfront-fusion-using-a-federated-connection)
* [Adicionar o Workfront Fusion como um provedor de identidade no AWS](#add-workfront-fusion-as-an-identity-provider-in-aws)
* [Criar a função IAM](#create-the-iam-role)
* [Criar a conexão no Workfront Fusion](#create-the-connection-in-workfront-fusion)
* [Adicionar a conexão à diretiva de confiança da função](#add-the-connection-to-the-roles-trust-policy)
* [Verifique a conexão](#verify-the-connection)
* [Solução de problemas](#troubleshooting)

Uma conexão federada permite que o Workfront Fusion acesse sua conta da AWS sem criar um usuário do IAM ou armazenar uma chave de acesso no Fusion.
Em vez disso, você registra o Workfront Fusion como um provedor de identidade confiável em sua conta do AWS e configura qual conexão única do Fusion tem permissão para usar uma função específica do IAM. Quando a conexão é executada, o Fusion apresenta uma prova de identidade de curta duração e o AWS retorna credenciais temporárias que expiram por conta própria. Nenhuma chave de vida longa é criada, armazenada ou girada.

>[!NOTE]
>
>A configuração dessa conexão leva duas visitas ao console do AWS. Primeiro, você cria a função, depois cria a conexão no Workfront Fusion e, em seguida, retorna ao AWS para concluir a diretiva de confiança. Isso ocorre porque parte da diretiva de confiança identifica uma conexão específica e esse identificador não existe até que a conexão seja criada.

#### Pré-requisitos para conectar o AWS ao Workfront Fusion usando uma conexão federada

Para criar essa conexão, você precisa do seguinte:

* Permissão no AWS IAM para criar um provedor de identidade e criar e editar funções. Isso geralmente significa a política ou equivalente. Se você não tiver esse acesso, pergunte a alguém na sua nuvem ou
para concluir as etapas do AWS para você.
* A capacidade de criar conexões no Workfront Fusion.


#### Adicionar o Workfront Fusion como um provedor de identidade no AWS

Essa etapa informa ao AWS que os tokens emitidos pelo Workfront Fusion podem ser confiáveis. Você faz isso uma vez por conta da AWS. Se alguém em sua organização já tiver adicionado esse provedor, pule para [Criar a função IAM](#create-the-iam-role).

1. Faça logon no console do AWS e acesse **IAM** > **Provedores de identidade**.
1. Selecione **Adicionar provedor**.
1. Para o tipo de Provedor, selecione **OpenID Connect**.
1. Na URL do Provedor, insira o seguinte e selecione **Obter impressão digital**:

   ```
   https://oidc.automations.adobe.com
   ```

1. Em Público-alvo, insira o seguinte:

   ```
   sts.amazonaws.com
   ```

1. Selecione **Adicionar provedor**.
1. Continue para [Criar a função IAM](#create-the-iam-role).

#### Criar a função IAM

A função define o que a conexão tem permissão para fazer em sua conta da AWS. Você cria uma atribuição por conexão, para que cada acesso da conexão possa ser concedido e revogado independentemente.

1. No IAM, vá para **Funções** e selecione **Criar função**.
1. Para o tipo de entidade Confiável, selecione **Identidade da Web**.
1. Em Provedor de identidade, selecione `oidc.automations.adobe.com`.
1. Em Público, selecione `sts.amazonaws.com`.
1. Selecione **Avançar** e anexe as políticas de permissões necessárias para esta conexão.
Conceda somente as permissões que a conexão realmente usa. Por exemplo, uma conexão que só lê de
um bucket não precisa de `AmazonS3FullAccess`.
1. Dê à função um nome claro e reconhecível. Por exemplo, `WorkfrontFusionFederatedConnection`.
1. Selecione **Criar função**.
1. Abra a função que acabou de criar e copie seu ARN da área Resumo. Ela tem a seguinte aparência: `arn:aws:iam::123456789012:role/WorkfrontFusionFederatedConnection`

1. Continue em [Criar a conexão no Workfront Fusion](#create-the-connection-in-workfront-fusion).

#### Criar a conexão no Workfront Fusion

1. Na tela de configuração de conexão do módulo, selecione o tipo de conexão federada.
1. Insira o ARN de Função que você copiou em [Criar a função IAM](#create-the-iam-role).
1. Selecione **Criar**.
O Workfront Fusion exibe três valores. Você as usa no próximo procedimento.

<table>
  <tr>
    <td>Central de Problemas</td>
    <td>Sempre <code>https://oidc.automations.adobe.com</code>. Corresponde ao provedor de identidade adicionado no AWS.</td>
  </tr>
  <tr>
    <td>Assunto</td>
    <td>Identifica esta conexão. Parece com <code>fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964</code>. É diferente para cada conexão criada.</td>
  </tr>
  <tr>
    <td>Público-alvo</td>
    <td>Sempre <code>sts.amazonaws.com</code>.</td>
  </tr>
</table>

1. Deixe esse painel aberto e copie o valor Subject.

   >[!NOTE]
   >
   >Não feche o painel nem selecione Cancelar. A conexão não será concluída até que você conclua os procedimentos restantes. Se fechar o painel, você deverá excluir a conexão e iniciar novamente, pois uma nova conexão recebe um novo Assunto.

1. Continue em [Adicionar a conexão à diretiva de confiança da função](#add-the-connection-to-the-roles-trust-policy).

#### Adicionar a conexão à diretiva de confiança da função

Até que você conclua esse procedimento, a função confia no Workfront Fusion em geral, mas ainda não permite que essa conexão específica a use.

1. Em uma nova guia do navegador, retorne ao console AWS e abra a função criada.
1. Selecione a guia **Relações de confiança** e selecione **Editar diretiva de confiança**.
1. Substitua a política pelo seguinte, substituindo seus próprios valores:

   * Substituir `123456789012` pela ID de conta da AWS
   * Substitua o valor `sub` pelo Assunto copiado do Workfront Fusion.


   ```
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow", 
         "Principal": {
           "Federated": "arn:aws:iam::123456789012:oidc-provider/oidc.automations.adobe.com"
       },
       "Action": "sts:AssumeRoleWithWebIdentity", "Condition": {
        "StringEquals": {
          "oidc.automations.adobe.com:sub": "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964", 
          "oidc.automations.adobe.com:aud": "sts.amazonaws.com"
        }
       }
      }
    ]
   }
   ```

1. Selecione **Atualizar política**.
1. Continue em [Verificar a conexão](#verify-the-connection).

>[!TIP]
>
>Para permitir que mais de uma conexão use a mesma função, liste os assuntos como uma matriz. O AWS permite que a função seja usada se o token corresponder a qualquer valor na lista:
>
>```
>"oidc.automations.adobe.com:sub": [ "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964", "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:29011"
>]
>```
>
>Não substitua o subvalor por um curinga. Isso permite que qualquer conexão em sua organização use a função, incluindo conexões criadas posteriormente por outras pessoas


#### Verifique a conexão

1. Retorne à guia do navegador Workfront Fusion, onde o painel de conexão ainda está aberto.
1. Clique em **Salvar**.

   O Workfront Fusion entra em contato com a AWS, que verifica a diretiva de confiança e retorna credenciais temporárias. Se tudo estiver configurado corretamente, a conexão será validada com êxito e você poderá continuar a configuração do módulo.
   Se a verificação falhar, o painel permanecerá aberto e exibirá o erro. Corrija o problema no AWS e selecione Salvar novamente. Não é necessário recriar a conexão, e o Assunto não é alterado.

A partir desse ponto, a conexão renova suas próprias credenciais. Não há chave para girar e nada expira que você precise manter.

#### Solução de problemas


<table>
  <tr>
    <th>Erro</th>
    <th>O que significa</th>
    <th>O que verificar</th>
  </tr>
  <tr>
    <td>InvalidIdentityToken</td>
    <td>O AWS não pôde corresponder o token a um provedor de identidade registrado.</td>
    <td>Verifique se você adicionou o provedor de identidade descrito em Adicionar o Workfront Fusion como um provedor de identidade no AWS e se o URL é exatamente https://oidc.automations.adobe.com, sem a barra à direita.</td>
  </tr>
  <tr>
    <td>Acesso Negado ao assumir a função</td>
    <td>O provedor de identidade está registrado, mas a diretiva de confiança não corresponde a esta conexão.</td>
    <td>Verifique se o subvalor na política de confiança é caractere por caractere idêntico ao Assunto mostrado no Workfront Fusion e se aud é sts.amazonaws.com. Um Assunto copiado de uma conexão diferente é a causa mais comum.</td>
  </tr>
  <tr>
    <td>A conexão funciona, e depois falha</td>
    <td> </td>
    <td>Verifique se as políticas de permissões da função foram alteradas ou se a função foi excluída e recriada. Recriar uma função não altera seu ARN, mas redefine sua diretiva de confiança.</td>
  </tr>
</table>

+++

### Conectar o AWS ao Workfront Fusion usando um usuário da API

+++ Expanda para exibir instruções desse tipo de conexão.

Para conectar o [!DNL AWS S3] ao Workfront Fusion, você deve conectar sua conta do [!DNL AWS] ao Workfront Fusion. Para fazer isso, primeiro será necessário criar um usuário de API no [!DNL AWS] [!UICONTROL IAM].

1. Entre na sua conta do [!DNL AWS] [!UICONTROL IAM].
1. Navegue até **[!UICONTROL Gerenciamento de Identidade e Acesso]** > **[!UICONTROL Gerenciamento de Acesso]** > **[!UICONTROL Usuários]**.

1. Clique em **[!UICONTROL Adicionar usuário]**.
1. Insira o nome do novo usuário e selecione a opção **[!UICONTROL Acesso programático]** na seção [!UICONTROL Tipo de acesso].
1. Clique em **[!UICONTROL Anexar diretivas existentes diretamente]** e procure por **[!UICONTROL AmazonS3FullAccess]** na barra de pesquisa. Clique nela quando ela aparecer, em seguida, clique em **[!UICONTROL Avançar]**.

1. Prossiga pelas outras telas de diálogo e clique em **[!UICONTROL Criar Usuário]**.
1. Copie a **[!UICONTROL ID da chave de acesso]** e a **[!UICONTROL chave de acesso secreta]** fornecidas.

1. Vá para o Workfront Fusion e abra a caixa de diálogo **[!UICONTROL Criar uma conexão]** do módulo [!DNL AWS S3].
1. Insira a [!UICONTROL ID da chave de acesso] e a [!UICONTROL chave de acesso secreta] da etapa 7 para os respectivos campos e clique em **[!UICONTROL Continuar]** para estabelecer a conexão.

A conexão foi estabelecida. Você pode prosseguir com a configuração do módulo.

+++

## Módulos do [!DNL AWS S3] e seus campos

* [Ações](#actions)
* [Pesquisas](#searches)

Ao configurar módulos do [!DNL AWS S3], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos do [!DNL AWS S3] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ações](#actions)
* [Pesquisas](#searches)

### Ações

* [[!UICONTROL Criar bloco]](#create-bucket)
* [[!UICONTROL Obter arquivo]](#get-file)
* [[!UICONTROL Fazer uma chamada de API]](#make-an-api-call)
* [[!UICONTROL Carregar arquivo]](#upload-file)

#### [!UICONTROL Criar bloco]

Esse módulo de ação cria um bucket no AWS.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL AWS] ao Workfront Fusion, consulte <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Conectar [!DNL AWS] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Informe o nome do novo período.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Região] </td> 
   <td> <p>Selecione seu ponto de extremidade regional. Para obter mais informações, consulte <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">pontos de extremidade regionais</a> na documentação do AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter arquivo]

Esse módulo de ação baixa um arquivo de um bucket.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL AWS] ao Workfront Fusion, consulte <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Conectar [!DNL AWS] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Região] </td> 
   <td> <p>Selecione seu ponto de extremidade regional. Para obter mais informações, consulte <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">pontos de extremidade regionais</a> na documentação [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compartimento] </td> 
   <td> <p>Selecione o bucket do qual deseja baixar o arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Path]</p> </td> 
   <td> <p>Insira o caminho para o arquivo. Exemplo: <code>/photos/2019/February/image023.jpg</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fazer uma chamada de API]

Esse módulo de ação faz uma chamada personalizada para a API do AWS S3.

Para obter uma discussão detalhada da API [!DNL Amazon S3], consulte a [[!DNL Amazon S3] [!UICONTROL Introdução à API REST]](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL AWS] ao Workfront Fusion, consulte <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Conectar [!DNL AWS] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Região] </td> 
   <td> <p>Selecione seu ponto de extremidade regional. Para obter mais informações, consulte <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">pontos de extremidade regionais</a> na documentação [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Insira um URL de host. O caminho deve ser relativo a <code> https://s3.&lt;selected-region>.amazonaws.com/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação [!UICONTROL HTTP] necessário para configurar a chamada à API. Para obter mais informações, consulte métodos de solicitação <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">[!UICONTROL HTTP] no Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Adicione um cabeçalho de solicitação. Para cada cabeçalho que deseja adicionar, clique em <b>Adicionar item</b> e insira o cabeçalho. Você pode usar os seguintes cabeçalhos de solicitação comuns. Para obter mais cabeçalhos de solicitação consulte a <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3] Documentação da API</a>.</p> <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>Nome do cabeçalho</th> 
       <th> <p> Descrição</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Tamanho do Conteúdo]</p> </td> 
       <td> <p>Comprimento da mensagem (sem os cabeçalhos) de acordo com RFC 2616. Este cabeçalho é necessário para [!UICONTROL PUT]s e operações que carregam XML, como log e ACLs.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Tipo de Conteúdo]</p> </td> 
       <td> <p>O tipo de conteúdo do recurso, caso o conteúdo da solicitação esteja no corpo. Exemplo: <code>text/plain</code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-MD5]</p> </td> 
       <td> <p>O digest MD5 de 128 bits codificado em base64 da mensagem (sem os cabeçalhos) de acordo com a RFC 1864. Esse cabeçalho pode ser usado como uma verificação de integridade da mensagem para verificar se os dados são os mesmos que foram enviados originalmente. Embora seja opcional, recomendamos usar o mecanismo [!UICONTROL Content-MD5] como uma verificação de integridade completa. Para obter mais informações sobre a autenticação de solicitação do [!UICONTROL REST], consulte <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821">Solicitações de autenticação e autenticação REST</a> na documentação do AWS.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Data]</p> </td> 
       <td> <p>A data e a hora atuais de acordo com o solicitante. Exemplo: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Ao especificar o cabeçalho <code>Authorization </code>, você deve especificar o cabeçalho <code>x-amz-date</code> ou <code>Date </code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Esperar]</p> </td> 
       <td> <p>Quando seu aplicativo usa [!UICONTROL 100-continue], ele não envia o corpo da solicitação até que receba uma confirmação. Se a mensagem for rejeitada com base nos cabeçalhos, o corpo da mensagem não será enviado. Esse cabeçalho só poderá ser usado se você estiver enviando um corpo.</p> <p>Valores Válidos: [!UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
       <td> <p>Para solicitações de estilo de caminho, o valor é <code>s3.amazonaws.com</code>. Para solicitações de estilo virtual, o valor é <code>BucketName.s3.amazonaws.com</code>. Para obter mais informações, consulte <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html">Hospedagem virtual</a> na documentação do AWS.</p> <p>Esse cabeçalho é necessário para HTTP 1.1 (a maioria dos kits de ferramentas adiciona esse cabeçalho automaticamente); opcional para solicitações HTTP/1.0.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>Ao usar a assinatura versão 4 para autenticar a solicitação, este cabeçalho fornece um hash da carga da solicitação. Ao carregar um objeto em partes, defina o valor como <code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code> para indicar que a assinatura cobre apenas cabeçalhos e que não há carga útil. Para obter mais informações, consulte <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html">Cálculos de assinatura para o cabeçalho de autorização</a> na documentação do AWS.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL data-x-amz]</p> </td> 
       <td> <p>A data e a hora atuais de acordo com o solicitante. Exemplo: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Ao especificar o cabeçalho <code>Authorization </code>, você deve especificar o cabeçalho <code>x-amz-date</code> ou <code>Date </code>. Se você especificar ambos, o valor especificado para o cabeçalho <code>x-amz-date</code> terá prioridade.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>Esse cabeçalho pode ser usado nos seguintes cenários:</p> 
        <ul> 
         <li>Forneça tokens de segurança para [!DNL Amazon DevPay] operações. Cada solicitação que usa [!DNL Amazon DevPay] requer dois cabeçalhos <code>x-amz-security-token</code>: um para o token do produto e um para o token do usuário. Quando [!DNL Amazon S3] recebe uma solicitação autenticada, ele compara a assinatura computada com a assinatura fornecida. Cabeçalhos multivalores formatados incorretamente usados para calcular uma assinatura podem causar problemas de autenticação.</li> 
         <li>Forneça um token de segurança ao usar credenciais de segurança temporárias. Ao fazer solicitações usando credenciais de segurança temporárias obtidas do IAM, você deve fornecer um token de segurança usando esse cabeçalho. Para saber mais sobre credenciais de segurança temporárias, acesse Fazer solicitações.</li> 
        </ul> <p>Este cabeçalho é necessário para solicitações que usam [!DNL Amazon DevPay] e solicitações que são assinadas usando credenciais de segurança temporárias.</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Adicione as cadeias de caracteres de consulta desejadas, como parâmetros ou campos de formulário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:   <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar arquivo]

Esse módulo de ação faz upload de um arquivo para um bucket do AWS S3.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL AWS] ao Workfront Fusion, consulte <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Conectar [!DNL AWS] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Região] </td> 
   <td> <p>Selecione seu ponto de extremidade regional. Para obter mais informações, consulte <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">pontos de extremidade regionais</a> na documentação [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Folder] </p> </td> 
   <td> <p>Especifique a pasta de destino para a qual você deseja fazer upload de um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Cabeçalhos] (opcional)</p> </td> 
   <td> <p> Para cada cabeçalho que você deseja adicionar, clique em <b>Adicionar item</b> e insira a chave e o valor do cabeçalho.</p><p> Para os cabeçalhos disponíveis, consulte <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a> na documentação do AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Listar Arquivos]](#list-files)
* [[!UICONTROL Listar pastas]](#list-folders)

#### [!UICONTROL Listar Arquivos]

Retorna uma lista de arquivos de um local especificado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL AWS] ao Workfront Fusion, consulte <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Conectar [!DNL AWS] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Região] </td> 
   <td> <p>Selecione seu ponto de extremidade regional. Para obter mais informações, consulte <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">pontos de extremidade regionais</a> na documentação [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compartimento] </td> 
   <td> <p>Selecione o bucket [!DNL Amazon S3] que você deseja pesquisar arquivos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefixo]</p> </td> 
   <td> <p> Insira um caminho para uma pasta na qual pesquisar arquivos, como <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar pastas]

Retorna uma lista de pastas de um local especificado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL AWS] ao Workfront Fusion, consulte <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Conectar [!DNL AWS] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Região] </td> 
   <td> <p>Selecione seu ponto de extremidade regional. Para obter mais informações, consulte <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">pontos de extremidade regionais</a> na documentação [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compartimento] </td> 
   <td> <p>Selecione o bucket [!DNL Amazon S3] que deseja pesquisar pastas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefixo] (opcional)</p> </td> 
   <td> <p> Caminho para uma pasta na qual pesquisar pastas, como <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
