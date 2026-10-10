---
title: HTTP > Criar um módulo de solicitação JWT
description: O módulo Adobe Workfront Fusion HTTP > Criar uma solicitação JWT envia uma solicitação HTTP(S) para um URL e a autoriza com um JSON Web Token que o Fusion assina automaticamente.
author: Becky
feature: Workfront Fusion
exl-id: 2f8c0b0d-085a-4b49-b350-4fd4cca1d0a7
TQID: 'https://experienceleague.adobe.com/pt-br'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 5e6403abee4e5767da9134529b9e88070bad5f44
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 11%
---
# [!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação JWT] para o módulo

O módulo [!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação JWT] do Adobe Workfront Fusion envia uma solicitação HTTP(S) para uma URL e a autoriza com um JSON Web Token (JWT) que o módulo assina para você em cada chamada. A resposta é processada da mesma forma que no módulo padrão [!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação].

Este módulo se comporta como o módulo padrão [!UICONTROL Fazer uma solicitação], com uma diferença principal: ele assina automaticamente um JWT das declarações fornecidas e o adiciona à solicitação, por padrão como `Authorization: Bearer <token>`.

Use este módulo para chamar qualquer API que espere um JWT assinado para autenticação, como serviços que exigem um token de portador de vida curta assinado com um segredo compartilhado (HMAC) ou uma chave privada (RSA/ECDSA), sem criar o token em uma etapa separada.

Se a API usar OAuth 2.0, autenticação básica, uma chave de API ou um certificado de cliente, use o módulo HTTP dedicado correspondente.

>[!NOTE]
>
>Se você estiver se conectando a um produto Adobe que não tem um conector dedicado no momento, recomendamos usar o módulo Adobe Authenticator.
>
>Para obter mais informações, consulte [módulo Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Criar uma conexão JWT

O módulo requer uma conexão JWT. A conexão armazena o material de assinatura para que a chave secreta ou privada não precise aparecer no cenário.

### Criar uma conexão JWT no Fusion

1. Adicione o módulo [!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação JWT] ao seu cenário.
1. Clique em **[!UICONTROL Adicionar]** ao lado do campo **[!UICONTROL Conexão]**.
1. Configure os campos de conexão:

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader"><p>Nome da conexão</p></td>
      <td><p>Insira um nome para a conexão.</p></td>
     </tr>
     <tr>
      <td role="rowheader"><p>Algoritmo</p></td>
      <td>
       <p>Selecione o algoritmo de assinatura para a conexão.</p>
       <ul>
        <li><code>HS256</code></li>
        <li><code>HS384</code></li>
        <li><code>HS512</code></li>
        <li><code>RS256</code></li>
        <li><code>RS384</code></li>
        <li><code>RS512</code></li>
        <li><code>PS256</code></li>
        <li><code>PS384</code></li>
        <li><code>PS512</code></li>
        <li><code>ES256</code></li>
        <li><code>ES384</code></li>
        <li><code>ES512</code></li>
       </ul>
      </td>
     </tr>
     <tr>
      <td role="rowheader"><p>Segredo</p></td>
      <td>
       <p>Insira a chave de assinatura.</p>
       <ul>
        <li>Para algoritmos <code>HS*</code>, use a cadeia de caracteres de segredo compartilhado.</li>
        <li>Para os algoritmos <code>RS*</code>, <code>PS*</code> e <code>ES*</code>, use a chave privada codificada em PEM.</li>
       </ul>
      </td>
     </tr>
    </tbody>
   </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e retornar ao módulo.

>[!IMPORTANT]
>
>Uma conexão JWT assina com apenas um algoritmo. Se o cenário exigir mais de um algoritmo de assinatura, crie uma conexão separada para cada algoritmo. Isso corresponde ao comportamento do aplicativo JWT independente existente.

## [!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação JWT] para o módulo e seus campos

Ao configurar o módulo [!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação JWT], o Adobe Workfront Fusion exibe os campos listados abaixo na mesma ordem em que aparecem na interface do usuário do módulo. Um título em negrito em um módulo indica um campo obrigatório. Os campos marcados como avançados ficam ocultos, a menos que você selecione **[!UICONTROL Mostrar configurações avançadas]**.

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Connection]</p></td>
   <td><p>Selecione uma conexão JWT existente ou crie uma nova.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL URL]</p></td>
   <td><p>O URL de destino da solicitação.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Method]</p></td>
   <td><p>Método HTTP, como GET, POST, PUT, PATCH ou DELETE.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Headers]</p></td>
   <td><p>Cabeçalhos de solicitação personalizados em formato de chave/valor.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Query String]</p></td>
   <td><p>Parâmetros da sequência de consulta no formato chave/valor.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Tipo de corpo]</p></td>
   <td><p>Como o corpo da solicitação é codificado. As opções incluem Raw, application/x-www-form-urlencoded e multipart/form-data.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Analisar resposta]</p></td>
   <td><p>Quando ativado, o Fusion analisa o corpo da resposta com base no tipo de conteúdo da resposta.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Carga JWT (Declarações)]</p></td>
   <td><p>Pares de valor/chave incluídos como declarações na carga do JWT. As declarações reservadas <code>exp</code>, <code>iat</code> e <code>nbf</code> devem ser NumericDate — um número de segundos desde a época Unix. Os valores de reivindicação mantêm seu tipo JSON, para que os números permaneçam números e os booleanos permaneçam booleanos.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Tempo Limite] (avançado)</p></td>
   <td><p>Especifique o tempo limite da solicitação em segundos (1-300). O padrão é 40 segundos.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Repetir Contagem] (avançado)</p></td>
   <td><p>Especifique quantas vezes a solicitação deverá ser repetida se ela falhar devido a um erro com nova tentativa.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Códigos de Status de Novas Tentativas Adicionais] (avançado)</p></td>
   <td><p>Especifique códigos de status HTTP adicionais que devem ser tratados como repetíveis.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Compartilhar cookies com outros módulos HTTP] (avançado)</p></td>
   <td><p>Habilite essa opção para compartilhar cookies do servidor com todos os módulos HTTP em seu cenário.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Certificado autoassinado] (avançado)</p></td>
   <td><p>Faça upload do seu certificado se quiser usar o TLS usando seu certificado autoassinado.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Rejeitar conexões que estão usando certificados não verificados (autoassinados)] (avançado)</p></td>
   <td><p>Habilite esta opção para rejeitar conexões que estejam usando certificados TLS não verificados.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Seguir redirecionamento] (avançado)</p></td>
   <td><p>Ative essa opção para seguir os redirecionamentos de URL com respostas 3xx.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Desabilitar serialização de várias chaves de cadeia de caracteres de consulta como matrizes] (avançado)</p></td>
   <td><p>Por padrão, o Workfront Fusion lida com vários valores para a mesma chave de parâmetro de string de consulta de URL que os arrays. Por exemplo, <code>www.test.com?foo=bar&amp;foo=baz</code> será convertido em <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Ative esta opção para desativar este recurso.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Solicitar conteúdo compactado] (avançado)</p></td>
   <td><p>Habilite esta opção para solicitar uma versão compactada do site. Adiciona um cabeçalho <code>[!UICONTROL Accept-Encoding]</code> para solicitar conteúdo compactado.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Usar TLS Mútuo] (avançado)</p></td>
   <td><p>Habilite esta opção para usar o TLS mútuo na solicitação HTTP.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Opções de assinatura] (avançado)</p></td>
   <td><p>Para cada opção de assinatura que você deseja adicionar à solicitação, clique em <b>Adicionar item</b> e insira o nome e o valor do parâmetro.</p><p>Opções adicionais passadas ao signatário do JWT, como <code>expiresIn</code>, <code>issuer</code>, <code>audience</code>, <code>subject</code> e <code>keyid</code>. Valores de duração como <code>expiresIn</code> são interpretados pela biblioteca <code>jsonwebtoken</code>. Um número simples é tratado como milissegundos, portanto, use uma cadeia de caracteres de unidade como <code>"1h"</code> ou <code>"3600s"</code> para ser explícito. O algoritmo é retirado da conexão e não pode ser substituído aqui.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Nome do Cabeçalho] (avançado)</p></td>
   <td><p>Informe ou mapeie o nome do cabeçalho da solicitação que recebe o JWT assinado. Padrão: <code>Authorization</code>. O nome do cabeçalho não deve conter um ponto (<code>.</code>), pois os nomes pontilhados são rejeitados e não podem ser mascarados em logs de solicitação.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Tipo de Token] (avançado)</p></td>
   <td><p>Insira ou mapeie o esquema de autenticação colocado antes do token, como <code>Bearer</code>. Deixe em branco para enviar o token bruto sem um prefixo.</p></td>
  </tr>
 </tbody>
</table>

## Como o token é criado

1. O módulo coleta as declarações no campo [!UICONTROL Carga JWT (Declarações)].
1. Declarações reservadas, como <code>exp</code>, <code>iat</code>, e <code>nbf</code> são convertidos em valores NumericDate.
1. O módulo aplica as [!UICONTROL Opções de assinatura] e assina o token usando o algoritmo da conexão.
1. O token assinado é colocado no cabeçalho da solicitação definido por [!UICONTROL Nome do Cabeçalho].
1. Se [!UICONTROL Tipo de token] estiver definido, o módulo adicionará o prefixo antes do token. Por exemplo, <code>Bearer KeyJ...</code>.
1. A solicitação é enviada e a resposta é processada da mesma forma que o módulo padrão [!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação].

O token assinado é mascarado automaticamente nos logs de depuração e erro para que nunca seja exposto.

## Exemplo

### Conexão

- Algoritmo: `HS256`
- Segredo: `my-shared-secret`

### Configurações do módulo

- URL: `https://api.example.com/v1/orders`
- Método: `GET`
- Carga JWT (solicitações):
  - `sub` = `service-account-42`
  - `iss` = `make-integration`
- Opções de assinatura:
  - `expiresIn` = `1h`
- Nome do Cabeçalho: `Authorization`
- Tipo de token: `Bearer`

### Resultado

O módulo envia a solicitação com um cabeçalho semelhante a:

```text
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

## Perguntas frequentes/armadilhas

### Por que meu token expirou tão rapidamente?

Você provavelmente inseriu um número vazio para `expiresIn`, como `3600`. A biblioteca `jsonwebtoken` interpreta números sem formatação como milissegundos. Em vez disso, use uma cadeia de caracteres de unidade como `"1h"` ou `"3600s"`.

### Quando o token é criado?

O módulo assina um JWT novo sempre que o módulo é executado, não quando você cria a conexão. A conexão armazena somente o material e o algoritmo de assinatura, portanto, declarações como `iat` e `exp` refletem o momento da execução desse módulo.

Se a solicitação tentar novamente dentro da mesma execução do módulo, o Fusion reutiliza o mesmo token assinado para essas tentativas, em vez de assinar um novo token para cada tentativa. Por causa disso, um valor `expiresIn` muito curto pode expirar antes que ocorra uma nova tentativa e fazer com que uma nova tentativa envie um token já expirado. Para evitar isso, use uma cadeia de caracteres de unidade limpa, como `"1h"` ou `"3600s"`, e evite tempos de vida de token muito curtos.

### Posso alterar o algoritmo por solicitação?

Não. O algoritmo é corrigido pela conexão. Se você precisar de um algoritmo diferente, crie uma conexão JWT diferente.

### Posso enviar o token em um cabeçalho personalizado?

Sim. Defina o campo [!UICONTROL Nome do Cabeçalho] com um nome personalizado, mas ele não pode conter um ponto (`.`).

### Posso enviar o token bruto sem `Bearer`?

Sim. Deixe [!UICONTROL Tipo de token] vazio.

### O token está visível nos logs?

Não. O token assinado é mascarado automaticamente nos logs de depuração e erro.


>[!NOTE]
>
>Observação técnica: a assinatura usa a biblioteca `jsonwebtoken` e espelha o comportamento de assinatura do aplicativo JWT independente, para que as mesmas entradas produzam o mesmo token que o aplicativo JWT independente.
