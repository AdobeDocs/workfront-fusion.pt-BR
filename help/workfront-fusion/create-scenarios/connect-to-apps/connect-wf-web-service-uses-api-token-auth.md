---
title: Conectar o Adobe Workfront Fusion a um serviço Web que usa a autorização do token de API
description: Alguns serviços não permitem que soluções de integração, como o Adobe Workfront Fusion, criem um aplicativo que pode ser usado facilmente em seu cenário.
author: Becky
feature: Workfront Fusion
exl-id: 4a8ac816-52de-41e8-96d7-1c8cde2ebe32
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 1%

---

# Conectar o Adobe Workfront Fusion a um serviço Web que usa a autorização do token de API

Alguns serviços não permitem que soluções de integração, como o Adobe Workfront Fusion, criem um aplicativo que pode ser usado facilmente em seu cenário.

A solução alternativa para essa situação é conectar o serviço (aplicativo) desejado ao Workfront Fusion usando o módulo HTTP > Fazer uma solicitação.

Este artigo explica como conectar quase qualquer serviço Web ao Workfront Fusion usando uma chave de API/token de API.

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion</p>
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

## Conexão com um serviço Web que usa um token de API

O procedimento de conexão do serviço por meio de um token de API é semelhante para a maioria dos serviços da Web.

1. Crie um aplicativo no site do serviço Web, conforme explicado na seção [Crie um novo aplicativo e obtenha o token de API](#create-a-new-application-and-obtain-the-api-token) neste artigo.
1. Obtenha a chave de API ou o token de API.
1. Adicione o módulo HTTP do Workfront Fusion > Fazer uma solicitação ao seu cenário.
1. Configure o módulo de acordo com a documentação da API do serviço Web e execute o cenário, conforme explicado na seção [Configurar o módulo HTTP](#set-up-the-http-module) deste artigo.

>[!NOTE]
>
>Este exemplo se conecta ao serviço de notificação Pushover.

## Crie um novo aplicativo e obtenha o token da API

>[!NOTE]
>
>Há várias maneiras diferentes pelas quais os serviços da Web criam e distribuem chaves de API ou tokens de API. Para obter instruções sobre como obter uma chave de API e um token para o serviço da Web desejado, vá para o site do serviço e pesquise por &quot;Chave de API&quot; ou &quot;Token de API&quot;.
>
>Estamos incluindo instruções para obter uma chave de API Pushover somente como exemplo do que você pode encontrar.

1. Faça logon na sua conta Pushover.
1. Clique em **Criar um token de aplicativo/API** na parte inferior da página.
1. Preencha as Informações do Aplicativo e clique em **Criar um Aplicativo**.
1. Armazene o token de API fornecido em um local seguro. Você precisará dele para o módulo Workfront Fusion HTTP > Fazer uma solicitação para se conectar ao serviço Web desejado (Pushover, neste caso).

## Configurar o módulo HTTP

Para conectar um serviço Web ao seu cenário do Workfront Fusion, é necessário usar o módulo HTTP > Fazer uma solicitação no cenário e configurar o módulo de acordo com a documentação da API do serviço Web.

1. Adicione o módulo HTTP > Fazer uma solicitação ao seu cenário.
1. Para enviar uma mensagem usando o Workfront Fusion, configure o módulo HTTP da seguinte maneira.

   >[!NOTE]
   >
   >Essas configurações do módulo correspondem à documentação da API do serviço Web Pushover. As configurações podem ser diferentes para outros serviços da Web. Por exemplo, o token da API pode ser inserido no cabeçalho e não no campo Corpo.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> URL</td> 
      <td> <p><code>https://api.pushover.net/1/messages.json</code> </p> <p>O campo URL contém o endpoint que pode ser encontrado na documentação da API do serviço Web.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> Método</td> 
      <td> <p><code>POST</code> </p> <p>O método usado depende do endpoint correspondente. O endpoint de push para mensagens de push usa o método POST.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Cabeçalhos</p> </td> 
      <td> <p>Alguns serviços da Web podem usar Cabeçalhos para especificar a autenticação do token de API ou outros parâmetros. Esse não é o caso em nosso exemplo, pois o endpoint do Pushover para enviar mensagens usa Corpo (veja abaixo) para todos os tipos de solicitação.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Sequência de consulta</p> </td> 
      <td> <p>Alguns serviços da Web podem usar uma sequência de consulta para especificar outros parâmetros. Esse não é o caso em nosso exemplo, pois o serviço Web Pushover usa Corpo (veja abaixo) para todos os tipos de solicitação.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Tipo de corpo</p> </td> 
      <td> <p><code>Raw</code> </p> <p>Essa configuração permite selecionar o tipo de conteúdo JSON no campo Tipo de conteúdo abaixo.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Tipo de conteúdo</p> </td> 
      <td> <p><code>JSON (application/json)</code> </p> <p>JSON é o tipo de conteúdo necessário para o aplicativo Pushover. Isso pode diferir de outros serviços da Web.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Solicitar conteúdo</p> </td> 
      <td> <p>Insira o conteúdo da solicitação de corpo no formato JSON. Você pode usar o módulo JSON &gt; Criar JSON, conforme explicado em <a href="#map-the-json-body-using-the-json--create-json-module" class="MCXref xref">Mapear o corpo JSON usando JSON &gt; Criar módulo JSON</a> neste artigo. Ou você pode inserir o conteúdo JSON manualmente, como explicado em <a href="#enter-the-json-body-manually" class="MCXref xref">Inserir o corpo JSON manualmente</a> neste artigo.</p> <p>Consulte a documentação da API do serviço Web para obter os parâmetros necessários para esse serviço Web.</p> </td>

   </tr> 
    </tbody> 
   </table>

## Insira o corpo JSON manualmente

Especifique parâmetros e valores no formato JSON.

>[!BEGINSHADEBOX]

**Exemplo:**

```
{"user":"12345c2ecu1hq42ypqzhswbyam34",
"token":"123459evz8aepwtxydndydgyumbfx",
"message":"Hello World!",
"title":"The Push Notification"}
```

>[!ENDSHADEBOX]

Este exemplo inclui as seguintes informações.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p> usuário</p> </td> 
   <td> <p>Sua USER_KEY. Isso pode ser encontrado no seu painel Pushover.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> token </td> 
   <td> <p>O token de API/Chave de API gerado criou seu aplicativo Pushover.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> mensagem </td> 
   <td> <p>O conteúdo de texto da notificação por push enviada para o(s) dispositivo(s).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> título </td> 
   <td> <p>(Opcional) O título da sua mensagem. Se nenhum valor for inserido, o nome do aplicativo será usado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Mapeie o corpo JSON usando o módulo JSON > Criar JSON

O módulo Criar JSON facilita a especificação do JSON. Ela também oferece a possibilidade de definir valores dinamicamente.

Para obter mais informações sobre os módulos JSON, consulte [módulos JSON](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/json-modules.md).

1. Insira ou mapeie os valores a partir dos quais deseja criar JSON.

   ![Valores de JSON](/help/workfront-fusion/create-scenarios/connect-to-apps/assets/json-values-350x288.png)

1. Conecte o JSON > Criar módulo JSON ao HTTP > Fazer um módulo de solicitação.
1. Mapeie a string JSON do módulo Criar JSON para o campo Solicitar conteúdo no módulo HTTP > Fazer uma solicitação.

Quando você executa o cenário, a notificação por push é enviada para o dispositivo que foi registrado na sua conta Pushover.
