---
title: Módulos do Jira Software
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Jira] Software, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 92cac080-d8f6-4770-a6a6-8934538c978b
source-git-commit: 017341e045a703f5d6e933a6df860f4fc8c0649d
workflow-type: tm+mt
source-wordcount: '2466'
ht-degree: 37%

---

# Módulos do [!DNL Jira Software]

>[!NOTE]
>
>Essas instruções se aplicam aos conectores herdados do Jira Cloud e do Jira Server. Para obter instruções sobre a nova versão do conector Jira, que é simplesmente rotulada como Jira, consulte [Módulos Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md).

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam [!DNL Jira Software], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Essas instruções se aplicam aos módulos Jira Cloud e Jira Server.

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

Para usar módulos do [!DNL Jira] é necessário ter uma conta do [!DNL Jira].

## Informações da API Jira

O conector Jira usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"></td> 
   <td> Jira Cloud</td> 
   <td> Servidor Jira</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersion</td> 
   <td> 2</td> 
   <td> 2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersionAgile</td> 
   <td> 1,0 </td> 
   <td> 1,0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>1.7.29</td> 
   <td>1.0.19</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL Jira Software] ao Workfront Fusion

O método de conexão é baseado no uso do [!DNL Jira Cloud] ou do [!DNL Jira Server].

* [Conectar [!DNL Jira Cloud] ao Workfront Fusion](#connect-jira-cloud-to-workfront-fusion)
* [Conectar [!DNL Jira Server] ao Workfront Fusion](#connect-jira-server-to-workfront-fusion)

### Conectar o [!DNL Jira Cloud] ao Workfront Fusion

Conectar o [!DNL Jira Cloud] ao Workfront Fusion

Para conectar [!DNL Jira Software] ao Workfront Fusion, você deve criar um token de API e inseri-lo junto com a URL de Serviço e o Nome de Usuário no campo [!UICONTROL Criar uma conexão] no Workfront Fusion.

#### Criar um token de API em [!DNL Jira]

1. Crie um token de API no Jira.

   Para obter instruções, recomendamos pesquisar por &quot;Criar um token de API&quot; na documentação do Jira.
1. Depois de criar o token, copie-o em um local seguro.

   >[!IMPORTANT]
   >
   >Você não poderá exibir o token novamente depois de fechar esta caixa de diálogo.
1. Armazene o token gerado em um local seguro.
1. Continuar com [Configurar o token de API [!DNL Jira] no Workfront Fusion](#configure-the-jira-api-token-in-workfront-fusion).

#### Configurar o token de API [!DNL Jira] no Workfront Fusion

1. Em qualquer módulo [!DNL Jira Cloud] no Workfront Fusion, clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL conexão].
1. Especifique as seguintes informações:

   * **Ambiente**
   * **Tipo**
   * **[!UICONTROL URL do Serviço]:** Esta é a URL base que você usa para acessar sua conta Jira. Exemplo: `yourorganization.atlassian.net`
   * **[!UICONTROL Nome de usuário]**
   * **[!UICONTROL Token de API]:** Este é o token de API criado na seção [Criar um token de API [!DNL Jira]](#create-an-api-token-in-jira) deste artigo.

1. Clique em [!UICONTROL Continuar] para criar a conexão e retornar ao módulo.

### Conectar o [!DNL Jira Server] ao Workfront Fusion

Para autorizar uma conexão entre o Workfront Fusion e o [!DNL Jira Server], você precisa de sua Chave do Consumidor, Chave Privada e URL do Serviço. Talvez seja necessário contatar o administrador do [!DNL Jira] para obter essas informações.

* [Gerar chaves Públicas e Privadas para sua  [!DNL Jira] conexão](#generate-public-and-private-keys-for-your-jira-connection)
* [Configurar o aplicativo cliente como consumidor no  [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)
* [Criar uma conexão com o  [!DNL Jira] Server ou Jira Data Center no Workfront Fusion](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Gerar chaves públicas e privadas para sua conexão [!DNL Jira]

Para adquirir uma chave privada para sua conexão [!DNL Workfront Fusion Jira], você precisa gerar chaves públicas e privadas. Isso é feito no terminal do computador. Você pode localizar seu terminal procurando o terminal no menu Iniciar ou na barra de pesquisa do computador (não na barra de pesquisa do navegador).

1. No terminal, execute os seguintes comandos `openssl`.

   * `openssl genrsa -out jira_privatekey.pem 1024`

     Esse comando gera uma chave privada de 1024 bits.

   * `openssl req -newkey rsa:1024 -x509 -key jira_privatekey.pem -out jira_publickey.cer -days 365`

     Este comando cria um certificado X509.

   * `openssl pkcs8 -topk8 -nocrypt -in jira_privatekey.pem -out jira_privatekey.pcks8`

     Este comando extrai a chave privada (formato PKCS8) para o arquivo `jira_privatekey.pcks8`.

   * `openssl x509 -pubkey -noout -in jira_publickey.cer  > jira_publickey.pem`

     Este comando extrai a chave pública do certificado para o arquivo `jira_publickey.pem`.

     >[!NOTE]
     >
     >Se estiver usando o Windows, talvez seja necessário salvar manualmente a chave pública no arquivo `jira_publickey.pem`:
     >
     >1. No terminal, execute o seguinte comando:
     >   
     >   `openssl x509 -pubkey -noout -in jira_publickey.cer`
     >   
     >1. Copie a saída do terminal, incluindo `-------BEGIN PUBLIC KEY--------` e `-------END PUBLIC KEY--------`.
     >   
     >1. Cole a saída do terminal em um arquivo chamado `jira_publickey.pem`.


1. Prossiga para [Configurar o aplicativo cliente como consumidor em [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)

#### Configure o aplicativo cliente como um consumidor no [!DNL Jira]

1. Faça logon na instância do [!DNL Jira].
1. No painel de navegação esquerdo, clique em **[!UICONTROL [!DNL Jira]Configurações]** ![Ícone de configurações Jira](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **[!UICONTROL Aplicativos]**> **[!UICONTROL Links de aplicativos]**.
1. No campo **[!UICONTROL Insira a URL do aplicativo que deseja vincular]**, digite

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. Clique em **[!UICONTROL Criar novo link]**. Ignore a mensagem de erro &quot;Nenhuma resposta foi recebida do URL inserido&quot;.
1. Na janela **[!UICONTROL Vincular aplicativos]**, insira valores nos campos **[!UICONTROL Chave do consumidor]** e **[!UICONTROL Segredo compartilhado]**.

   Você pode escolher os valores desses campos.

1. Copie os valores dos campos **[!UICONTROL Chave do consumidor]** e **[!UICONTROL Segredo compartilhado]** para um local seguro.

   Esses valores serão necessários posteriormente no processo de configuração.

1. Preencha os campos URL da seguinte maneira:

   | Campo | Descrição |
   | --- | --- |
   | [!UICONTROL URL do token de solicitação] | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | [!UICONTROL URL de autorização] | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | [!UICONTROL URL do token de acesso] | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. Marque a caixa de seleção **[!UICONTROL Criar link de entrada]**.
1. Clique em **[!UICONTROL Continuar]**.
1. Na janela **[!UICONTROL Vincular aplicativos]**, preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col data-mc-conditions=""> 
    <col data-mc-conditions=""> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Chave do Consumidor]</p> </td> 
      <td> Cole a chave do consumidor que você copiou para um local seguro.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Nome do consumidor]</td> 
      <td>Insira um nome de sua escolha. Este nome é para sua própria referência.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Chave pública]</td> 
      <td>Cole a chave pública do arquivo <code>[!DNL jira_publickey.pem]</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continuar]**.
1. Continue para [Criar uma conexão com [!DNL Jira Server] ou [!DNL Jira Data Center] no Workfront Fusion](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Criar uma conexão com [!DNL Jira Server] ou [!DNL Jira Data Center] no Workfront Fusion

>[!NOTE]
>
>Use o aplicativo [!DNL Jira Server] para se conectar a [!DNL Jira Server] ou [!DNL Jira Data Center].

1. Em qualquer módulo [!DNL Jira Server] no Workfront Fusion, clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL conexão].
1. No painel [!UICONTROL Criar uma conexão], preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Insira um nome para a conexão.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td> <p>Selecione se você está usando um ambiente de produção ou não produção.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Type]</p> </td> 
      <td> <p>Selecione se você está usando uma conta de serviço ou uma conta pessoal.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Chave do Consumidor]</td> 
      <td>Cole a chave do consumidor que você copiou em um local seguro no <a href="#configure-the-client-app-as-a-consumer-in-jira" class="MCXref xref">Configure o aplicativo cliente como um consumidor no [!DNL Jira]</a></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Private Key]</td> 
      <td>Cole a chave privada do arquivo <code>[!DNL jira_privatekey.pcks8]</code> criado em <a href="#generate-public-and-private-keys-for-your-jira-connection" class="MCXref xref">Gerar chaves públicas e privadas para sua conexão [!DNL Jira]</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Service URL]</td> 
      <td>Insira a URL da instância do [!DNL Jira]. Exemplo: <code>yourorganization.atlassian.net</code></td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## Módulos do [!DNL Jira Software] e seus campos

Ao configurar módulos do [!DNL Jira Software], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos do [!DNL Jira Software] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

#### [!UICONTROL Observar registros]

Este módulo de acionamento inicia um cenário quando um registro é adicionado, atualizado ou excluído.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecione o webhook que deseja usar para observar registros. </p> <p>Para adicionar um novo webhook:</p> 
    <ol> 
     <li value="1">Clique em <strong>[!UICONTROL Adicionar]</strong></li> 
     <li value="2">Insira um nome para o webhook.</li> 
     <li value="3"> <p>Selecione a conexão que deseja usar com seu webhook. </p> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </li> 
     <li value="4"> <p>Selecione o tipo de registro que você deseja que o software assista:</p> 
      <ul> 
       <li>[!UICONTROL Comentário] </li> 
       <li>[!UICONTROL Problema]</li> 
       <li>[!UICONTROL Projeto] </li> 
       <li>[!UICONTROL Sprint]</li> 
      </ul> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Adicionar problema ao sprint]](#add-issue-to-sprint)
* [[!UICONTROL Criar um Registro]](#create-a-record)
* [[!UICONTROL Chamada de API personalizada]](#custom-api-call)
* [[!UICONTROL Excluir um registro]](#delete-a-record)
* [[!UICONTROL Baixar um anexo]](#download-an-attachment)
* [[!UICONTROL Ler um registro]](#read-a-record)
* [[!UICONTROL Atualizar um registro]](#update-a-record)

#### [!UICONTROL Adicionar problema ao sprint]

Este módulo de ação adiciona um ou mais problemas a um sprint.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID Sprint]</td> 
   <td>Insira ou mapeie a ID de velocidade da velocidade à qual você deseja adicionar um problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Identificação de Problema ou Chaves]</td> 
   <td>Para cada problema ou chave que você deseja ver a experiência, clique em <b>[!UICONTROL Adicionar item]</b> e insira a ID ou chave do problema. Você pode inserir até 50 em um módulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar um Registro]

Este módulo de ação cria um novo registro no Jira.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo crie e preencha os outros campos específicos desse tipo de registro que aparecem no módulo.</p> 
    <ul> 
     <li>[!UICONTROL Anexo]</li> 
     <li>[!UICONTROL Comentário]</li> 
     <li>[!UICONTROL Problema]</li> 
     <li>[!UICONTROL Projeto]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Log de Trabalho]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API do [!DNL Jira Software]. Use este módulo para criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos [!DNL Jira Software].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo a<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta para a chamada de API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um registro]

Este módulo de ação exclui o registro especificado.

Especifique a ID do registro.

O módulo retorna a ID do registro e todos os campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo exclua. </p> 
    <ul> 
     <li>[!UICONTROL Anexo]</li> 
     <li>[!UICONTROL Comentário]</li> 
     <li>[!UICONTROL Problema]</li> 
     <li>[!UICONTROL Projeto]</li> 
     <li>[!UICONTROL Sprint] </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID ou Chave]</td> 
   <td>Insira ou mapeie a ID ou a Chave do registro que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Baixar um anexo]

Este módulo de ação baixa um anexo específico.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID do anexo que deseja baixar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler um registro]

Este módulo de ação lê dados de um único registro em [!DNL Jira Software].

Especifique a ID do registro.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro [!DNL Jira] que deseja que o módulo leia.</p> 
    <ul> 
     <li>[!UICONTROL Anexo]</li> 
     <li>[!UICONTROL Problema]</li> 
     <li>[!UICONTROL Projeto]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Usuário]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione as saídas que deseja receber. As opções de saída estão disponíveis com base no tipo de registro selecionado no campo "[!UICONTROL Tipo de registro]".</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Insira ou mapeie a ID [!DNL Jira Software] exclusiva do registro que você deseja que o módulo leia.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um registro]

Esse módulo de ação atualiza um registro existente, como um problema ou projeto,.

Especifique a ID do registro.

O módulo retorna a ID do registro e todos os campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo atualize. Quando você seleciona um tipo de registro, outros campos específicos desse tipo de registro aparecem no módulo.</p> 
    <ul> 
     <li>[!UICONTROL Comentário]</li> 
     <li>[!UICONTROL Problema]</li> 
     <li>[!UICONTROL Projeto]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Problema de transição]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID ou Chave]</td> 
   <td>Insira ou mapeie a ID ou a Chave do registro que deseja atualizar e, em seguida, preencha os outros campos específicos desse tipo de registro que aparecem no módulo.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Listar registros]](#list-records)
* [[!UICONTROL Pesquisar registros]](#search-for-records)

>[!IMPORTANT]
>
>O módulo de pesquisa usado pelo conector Jira herdado pode resultar no seguinte erro:
>
>`[410] The requested API has been removed. Please migrate to the /rest/api/3/search/jql API. A full migration guideline is available at https://developer.atlassian.com/changelog/#CHANGE-2046`
>
>Isso se deve a uma descontinuação no lado de Jira.
>
>Se encontrar esse erro, você poderá substituir o módulo de pesquisa do conector Jira herdado pelo módulo de pesquisa do novo conector. Observe que o novo conector permite selecionar a versão da API usada. Certifique-se de selecionar V3 ao criar a conexão.
>
> ![Opção de versão da API no novo conector Jira](/help/workfront-fusion/references/apps-and-modules/assets/jira-version-option.png)
>
>Observe que:
>
>* Somente o módulo de Pesquisa é afetado. No momento, outros endpoints da API Jira usados pelo conector Fusion não são afetados por essa desativação.
>
>* A implantação geográfica pode causar inconsistências. A Atlassian está lançando essa alteração regionalmente, o que significa que algumas instâncias do Jira Cloud ainda podem oferecer suporte temporário a endpoints mais antigos. Isso pode levar a um comportamento inconsistente entre ambientes.

#### [!UICONTROL Listar registros]

Este módulo de pesquisa recupera todos os itens de um tipo específico que correspondam à sua consulta de pesquisa

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo liste. Quando você seleciona um tipo de registro, outros campos específicos desse tipo de registro aparecem no módulo.</p> 
    <ul> 
     <li>[!UICONTROL Comentário]</li> 
     <li>[!UICONTROL Problema]</li> 
     <li>[!UICONTROL Projeto]</li> 
     <li>[!UICONTROL Problema de Sprint]</li> 
     <li>[!UICONTROL Log de Trabalho]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Máximo de Resultados]</p> </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que você deseja que o módulo recupere durante cada ciclo de execução de cenário.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Enter or map the ID of the first item you want to retrieve details for. This is a way to paginate the records. If you enter the 5000th item as the offset, the module would return items 5000-9999.</td> 
   </tr>
  --> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar registros]

Este módulo de pesquisa procura registros em um objeto em [!DNL Jira Software] que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Jira Software] ao Workfront Fusion, consulte <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Conectar [!DNL Jira Software] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja que o módulo procure. Quando você seleciona um tipo de registro, outros campos específicos desse tipo de registro aparecem no módulo.</p> 
    <ul> 
     <li>[!UICONTROL Issues]</li> 
     <li> <p>[!UICONTROL Problemas por JQL (Jira Query Language)] </p> <p>Para obter mais informações sobre JQL, consulte <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> no site de ajuda da Atlassian. </p> </li> 
     <li>[!UICONTROL Projeto]</li> 
     <li>[!UICONTROL Projeto por problema]</li> 
     <li>[!UICONTROL Usuário]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
