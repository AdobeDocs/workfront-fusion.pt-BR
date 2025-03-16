---
title: HTTP > Outros módulos
description: O aplicativo HTTP [!DNL Adobe Workfront Fusion] fornece vários módulos para comunicação com base no protocolo HTTP. HTTP é a base da comunicação de dados para a World Wide Web. Você pode usar os módulos do para baixar páginas e arquivos da Web, chamar webhooks e endpoints de API e assim por diante.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# HTTP > Outros módulos

O aplicativo [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] fornece vários módulos para comunicação com base no protocolo HTTP. HTTP é a base da comunicação de dados para a World Wide Web. Você pode usar os módulos do para baixar páginas e arquivos da Web, chamar webhooks e endpoints de API e assim por diante.

A escolha correta do módulo depende do mecanismo de autenticação/ autorização que o recurso que você deseja acessar emprega. Veja a seguir exemplos de módulos

* **Fazer uma solicitação**: destinada principalmente a recursos que não usam nenhum tipo de autenticação ou autorização
* **Fazer uma solicitação de Autenticação Básica**: Para recursos que usam a [!DNL HTTP] Autenticação Básica (BA)
* **Fazer uma solicitação OAuth 2.0**: para recursos que usam o protocolo de autorização OAuth 2.0
* **Fazer uma solicitação de Autenticação de Certificado de Cliente**: Para recursos que utilizam protocolo de autorização que exigem um certificado do lado do cliente
* **Fazer uma solicitação de autorização de Chave de API**: Para recursos que utilizam Chaves de API para autorização

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

## Módulos de solicitação

Consulte os seguintes artigos para obter instruções específicas do módulo de solicitação:

* [[!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação] para o módulo](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Criar um módulo de solicitação de Autorização Básica]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação OAuth 2.0] para o módulo](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação de Autorização de Certificado de Cliente] módulo](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação de autorização de Chave de API]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Outros módulos de ação

* [[!UICONTROL Obter um Arquivo]](#get-a-file)
* [[!UICONTROL Resolver uma URL de destino]](#resolve-a-target-url)

### [!UICONTROL Obter um Arquivo]

Este módulo de ação baixa um arquivo do URL especificado. Depois que o arquivo for baixado, você poderá processar ainda mais o arquivo (mapear os dados do arquivo) usando outros módulos no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Avaliar todos os estados como erros (exceto para 2xx e 3xx )] </td> 
   <td> <p>Use esta opção para configurar o tratamento de erros.</p> <p>Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Tratamento de erros em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Insira ou mapeie o URL do arquivo que deseja baixar. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compartilhar cookies com outros módulos HTTP] </td> 
   <td> <p>Ative esta opção se quiser que os cookies deste site estejam disponíveis para outros módulos. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resolver uma URL de destino]

Este módulo de ação resolve uma cadeia de redirecionamentos HTTP e retorna um URL de destino.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Insira ou mapeie a URL que você deseja resolver, como uma URL [!DNL bit.ly].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método] </td> 
   <td> <p>Selecione se você deseja usar o método [!UICONTROL HEAD] ou o método [!UICONTROL GET].</p> </td> 
  </tr> 
 </tbody> 
</table>

## Módulos iteradores

### [!UICONTROL Recuperar cabeçalhos]

Esse módulo retorna cada cabeçalho (nome e valor) do módulo HTTP especificado em um pacote separado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Módulo Source]</td> 
   <td> <p> Selecione o módulo do qual deseja recuperar cabeçalhos.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Geração de tokens da Web JSON (JWT)

É possível gerar um token JWT com a ajuda de funções integradas:

Cabeçalho

![Cabeçalho JWT](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

Código para copiar e colar:

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Carga:

![carga JWT](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

Código para copiar e colar:

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Token:

![Token JWT](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

Código para copiar e colar:

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
