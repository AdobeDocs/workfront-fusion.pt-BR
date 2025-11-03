---
title: Módulo Adobe Authenticator
description: Com o módulo Adobe Authenticator, você pode se conectar a qualquer produto da Adobe com uma API, usando uma única conexão.
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 1%

---

# Módulos do Adobe Authenticator

O módulo Adobe Authenticator permite se conectar a qualquer API do Adobe, usando uma única conexão. Isso permite que você se conecte mais facilmente a produtos da Adobe que ainda não têm um conector Fusion dedicado.

A vantagem sobre os módulos HTTP é que você pode criar uma conexão, como em um aplicativo dedicado.

Para ver uma lista de APIs do Adobe disponíveis, consulte [APIs do Adobe](https://developer.adobe.com/apis). Você pode usar somente as APIs às quais está atribuído.

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

* Você deve ter acesso ao produto Adobe ao qual deseja que o módulo se conecte.
* Você deve ter acesso à Adobe Developer Console.
* Você deve ter um projeto no Adobe Developer Console que inclua a API à qual deseja que o módulo se conecte. É possível:

   * Crie um novo projeto com a API.

     Ou
   * Adicionar a API a um projeto existente.

  Para obter informações sobre como criar ou adicionar uma API a um projeto no Adobe Developer Console, consulte [Criar um projeto](https://developer.adobe.com/dep/guides/dev-console/create-project/) na documentação do Adobe.

## Informações da API do Adobe Authenticator

O conector do Adobe Authenticator usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão

Uma conexão do Adobe Authenticator se conecta a um único projeto na Adobe Developer Console. Para usar a mesma conexão para mais de uma API do Adobe, adicione as APIs ao mesmo projeto e crie uma conexão com esse projeto.

Você pode criar conexões separadas para projetos separados, mas não pode usar uma conexão para acessar uma API que não esteja no projeto especificado nessa conexão.

>[!IMPORTANT]
>
>Com o conector do Adobe Authenticator, você tem a opção de fazer uma conexão servidor a servidor do OAuth ou uma conexão de conta de serviço (JWT). O Adobe substituiu as credenciais do JWT, que deixarão de funcionar após 1º de janeiro de 2025. **Portanto, é altamente recomendável criar conexões OAuth.**
>
>Para obter mais informações sobre esses tipos de conexões, consulte [Autenticação de Servidor para Servidor](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/) na documentação do Adobe

Para criar uma conexão:

1. Em qualquer módulo do Adobe Authenticator, clique em **Adicionar** ao lado do campo Conexão.
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
          <p>Selecione se deseja criar uma conexão de servidor para servidor OAuth ou uma conexão de conta de serviço (JWT). Recomendamos criar conexões OAuth.</p>
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
        <td>Insira sua ID de cliente do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira seu Segredo do Cliente do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Escopos]</td>
        <td>Se você selecionou uma conexão OAuth, insira os escopos necessários para essa conexão.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID da conta técnica]</td>
        <td>Se você selecionou uma conexão JWT, digite sua ID de conta técnica do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID da Organização]</td>
        <td>Se você selecionou uma conexão JWT, insira sua ID da organização [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Escopos do Meta]</td>
        <td>Se você selecionou uma conexão JWT, insira os metaescopos necessários para essa conexão. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Chave privada]</td>
        <td>
          <p>Se você selecionou uma conexão JWT, insira a chave privada que foi gerada quando suas credenciais foram criadas no [!DNL Adobe Developer Console]. </p>
          <p>Para extrair sua chave privada ou certificado:</p>
          <ol>
            <li value="1">
              <p>Clique em <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selecione o tipo de arquivo que você está extraindo.</p>
            </li>
            <li value="3">
              <p>Selecione o arquivo que contém a chave privada ou o certificado.</p>
            </li>
            <li value="4">
              <p>Digite a senha do arquivo.</p>
            </li>
            <li value="5">
              <p>Clique em <b>[!UICONTROL Salvar]</b> para extrair o arquivo e retornar à configuração de conexão.</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL URLs Base]</td>
        <td>Você deve adicionar os URLs de base que este autenticador deve permitir. Ao usar o módulo Fazer uma chamada de API personalizada posteriormente no cenário, você adicionará um caminho relativo ao URL escolhido. Ao inserir URLs aqui, você pode controlar a que o módulo Fazer uma chamada de API personalizada pode se conectar, o que aumenta a segurança.<p>Para cada URL base que você deseja adicionar ao autenticador, clique em <b>Adicionar item</b> e insira a URL base.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL URL de Autenticação]</td>
        <td>Deixe em branco para usar a URL de autenticação padrão do Adobe IMS de <code>https://ims-na1.adobelogin.com</code>. Se você não usar o Adobe IMS para autenticação, insira o URL a ser usado para autenticação.</td>
      </tr>
    </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## Módulos

* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Fazer uma chamada de API personalizada (herdado)](#make-a-custom-api-call-legacy)

### Fazer uma chamada de API personalizada

Esse módulo de ação permite fazer uma chamada para qualquer API do Adobe. Ele suporta arquivos grandes, em vez de corpos somente texto.

Esse módulo foi disponibilizado em 14 de novembro de 2024. Qualquer chamada de Adobe Authenticator > Fazer uma API personalizada configurada antes dessa data não lida com arquivos grandes e agora é considerada o módulo Fazer uma chamada de API personalizada (Herdado).

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Conexão]</td>
     <td>Para obter instruções sobre como criar uma conexão com o módulo Adobe Authenticator, consulte <a href="#create-a-connection" class="MCXref xref" >Criar uma conexão</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL Base]</p>
      </td>
      <td>
        <p>Insira o URL de base do ponto de API ao qual você deseja se conectar.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Insira o caminho relativo ao URL de base.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Método]</p>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cabeçalhos]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cadeia de Consulta]  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de Corpo]</td>
   <td> Selecione o tipo de corpo para esta solicitação de API:
   <ul>
   <li>Brutos</li>
   <li>application/x-www-form-urlencoded</li>
   <li>multipart/form-data</li>
   </ul>
      </td>
      </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de Saída]  </td>
      <td>
        <p>Selecione o tipo de dados que você deseja que o módulo produza. Se você não selecionar um tipo, o módulo selecionará um tipo automaticamente.</p>
      </td>
    </tr>
  </tbody>
</table>

### Fazer uma chamada de API personalizada (herdado)

Esse módulo de ação permite fazer uma chamada para qualquer API do Adobe.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Conexão]</td>
     <td>Para obter instruções sobre como criar uma conexão com o módulo Adobe Authenticator, consulte <a href="#create-a-connection" class="MCXref xref" >Criar uma conexão</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL Base]</p>
      </td>
      <td>
        <p>Insira o URL de base do ponto de API ao qual você deseja se conectar.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Insira o caminho relativo ao URL de base.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Método]</p>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cabeçalhos]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cadeia de Consulta]  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
