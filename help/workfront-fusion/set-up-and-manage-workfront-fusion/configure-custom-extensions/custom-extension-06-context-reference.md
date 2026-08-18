---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: A referência de contexto do Fusion
description: A referência de contexto do Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 757
ht-degree: 8%

---

# A referência de contexto do Fusion

>[!NOTE]
>
>Este artigo presume alguma familiaridade com ferramentas de desenvolvimento de software.

Quando sua interface chama `attach(...)`, o Fusion compartilha um objeto **context** que descreve a sessão atual. Essa página lista cada campo, o que significa e como os identificadores do Fusion e do Adobe IMS se relacionam.

## Como ler o contexto

* **Valores iniciais:** `connection.sharedContext.get("<key>")`
* **Atualizações:** Ouça o evento `contextchange`. O último objeto chega em `event.detail.context`.

Para obter o padrão de código completo, consulte [Criar a interface de extensão personalizada](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

```js
const organization = connection.sharedContext.get("organization");
const fusionOrgId  = organization?.id;        // Fusion's organization id
const imsOrgId     = connection.sharedContext.get("imsOrgId"); // Adobe IMS org id
```

## Chaves de nível superior

| Chave | Tipo | Descrição |
| ----- | ------ | ------------- |
| `imsToken` | sequência de caracteres | O **token de acesso IMS** do Adobe do usuário conectado. Use como um token `Bearer` para chamar APIs do Adobe ou Fusion em nome do usuário. **Por ser confidencial, nunca faça logon ou exiba.** |
| `imsOrgId` | sequência de caracteres | A **IMS organization id** da Adobe, no formato `XXXXXXXXXXXX@AdobeOrg`. |
| `imsUserId` | sequência de caracteres | A **ID de usuário IMS** do Adobe do usuário conectado. |
| `organization` | objeto | A **organização ativa completa do Fusion**. Para obter mais informações, consulte [`organization` campos](#organization-fields) neste artigo. |
| `team` | objeto \| indefinido | A **equipe completa ativa do Fusion**, quando uma está ativa (sempre relevante para `fusion/nav-team/1`). Para obter mais informações, consulte [`team` campos](#team-fields) neste artigo. |
| `user` | objeto | O **usuário Fusão totalmente conectado**. Para obter mais informações, consulte [`user` campos](#user-fields) neste artigo. |

### Fusion ID e IMS ID

Cada entidade tem uma **ID do Fusion** (usada pelas próprias APIs do Fusion) e, quando ela existe, uma **ID do Adobe IMS** (usada pelas APIs da plataforma Adobe):

| Entidade | ID da fusão | ID do Adobe IMS |
| -------- | ----------- | -------------- |
| Organização | `organization.id` | `imsOrgId` (também exposto como `organization.externalOrgId`) |
| Equipe | `team.id` | *(As equipes são somente Fusion; sem ID IMS)* |
| Usuário | `user.id` | `imsUserId` |

## `organization` campos

Esses campos são encontrados no registro ativo da organização. A maioria das extensões requer apenas `id`, `name` e os identificadores.

| Campo | Tipo | Descrição |
| ------- | ------ | ------------- |
| `id` | sequência de caracteres | ID da organização Fusion. |
| `name` | sequência de caracteres | Nome para exibição da organização |
| `externalOrgId` | sequência de caracteres | ID da organização IMS da Adobe (mesmo valor de `imsOrgId`). |
| `externalId` | sequência de caracteres | Identificador externo usado pelas integrações do Fusion |
| `countryId` | sequência de caracteres | ID de configuração do país. |
| `timezoneId` | sequência de caracteres | ID da configuração de fuso horário |
| `serviceName` | sequência de caracteres | Identificador de serviço/plano |
| `teamIds` | cadeia de caracteres[] | IDs de equipes nesta organização |
| `license` | objeto | Limites e direitos do plano, como operações, transferência de dados, vagas de usuário e sinalizadores de recursos |
| `scenariosCount` | número | Total de cenários na organização |
| `activeScenarios` | número | Cenários ativos no momento |
| `activeApps` | número | Número de aplicativos ou conexões ativos |
| `operations`, `operationsExt` | número | Contadores de uso de operações |
| `transfer`, `transferExt` | número | Contadores de uso da transferência de dados |
| `isPaused` | booleano | Se a organização está pausada |
| `isDeleted` | booleano | Se a organização está marcada como excluída |
| `imsEnabled` | booleano | Se a organização está vinculada ao Adobe IMS |
| `usersCount` | número | Número de usuários na organização |
| `nextReset` | string (data) | Na próxima redefinição dos contadores de uso. Ver [Datas](#dates) |

## `team` campos

Esses campos estão presentes quando uma equipe está ativa. Você deve fornecer um fallback caso a equipe seja `undefined` (por exemplo, em uma tela de nível de organização sem nenhuma equipe selecionada).

| Campo | Tipo | Descrição |
| ------- | ------ | ------------- |
| `id` | sequência de caracteres | ID da equipe de fusão. |
| `name` | sequência de caracteres | Nome para exibição da equipe. |
| `organizationId` | sequência de caracteres | ID de fusão da organização à qual esta equipe pertence. |
| `country` | sequência de caracteres | Configuração do país da equipe. |
| `timezone` | sequência de caracteres | Fuso horário da equipe. |
| `license` | objeto | Limites e direitos no nível da equipe. |
| `activeScenarios` | número | Cenários ativos na equipe. |
| `activeApps` | número | Aplicativos ou conexões ativos na equipe. |
| `scenarioDrafts` | booleano | Se os rascunhos de cenário estão habilitados. |
| `isDeleted` | booleano | Se a equipe está marcada como excluída. |
| `created` | string (data) | Quando a equipe foi criada. Consulte [Datas](#dates). |

## `user` campos

Esses campos se aplicam ao usuário do Fusion conectado.

| Campo | Tipo | Descrição |
| ------- | ------ | ------------- |
| `id` | sequência de caracteres | ID de usuário de fusão. |
| `name` | sequência de caracteres | Nome completo. |
| `email` | sequência de caracteres | Endereço de email. |
| `avatar` | sequência de caracteres | URL da imagem de avatar. |
| `locale` | sequência de caracteres | Local do usuário, como `en`. |
| `language` | sequência de caracteres | Idioma preferencial, quando definido. |
| `timezone` | sequência de caracteres | Nome do fuso horário. |
| `timezoneId` | sequência de caracteres | ID de configuração de fuso horário. |
| `countryId` | sequência de caracteres | ID de configuração do país. |
| `localeId` | sequência de caracteres | ID da configuração de localidade. |
| `features` | objeto | Sinalizadores de recursos por usuário (por exemplo, `allow_apps`, `public_templates`). |
| `usersAdminsRoleId` | sequência de caracteres | A ID da função de administrador do usuário, quando aplicável. |

>[!NOTE]
>
> O objeto `user` pode incluir campos internos adicionais. Você deve confiar somente nos campos documentados aqui. Outros campos podem ser alterados sem aviso prévio e alguns campos relacionados à autenticação nunca devem ser registrados ou exibidos.

## Datas

O contexto é serializado antes de atingir sua extensão, portanto, os campos de data **chegam como cadeias de caracteres** (ISO 8601, como `"2026-06-24T00:00:00.000Z"`), não como objetos `Date` do JavaScript. Você pode convertê-los se necessário:

```js
const resetDate = new Date(context.organization.nextReset);
```

## Atualizações de contexto

O Fusion reenvia todo o contexto (via `contextchange`) quando:

* o usuário **alterna a organização**,
* o usuário **alterna equipes** ou
* as informações **do** usuário conectado foram alteradas.

Sempre leia novamente todas as chaves que você usa dentro do seu manipulador `contextchange`, em vez de considerar que apenas um valor foi alterado.

## Práticas recomendadas de segurança

* **Nunca registrar, exibir ou persistir `imsToken`.** Trate-o como uma senha.
* Envie o token somente para endpoints confiáveis do Adobe/Fusion, via HTTPS, como um token `Bearer`.
* Não armazene dados pessoais do contexto além do que seu recurso precisa.

## Usar o token para chamar APIs

Para transformar `imsToken` (mais `organization.id` / `team.id`) em Workfront real ou
Dados de fusão, não é possível chamar essas APIs diretamente do navegador, pois o CORS bloqueia
o mesmo. Em vez disso, roteie a chamada por meio de uma pequena ação de tempo de execução do App Builder. Consulte
[Chamada de APIs do Workfront e Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


Para continuar o processo de criação de uma extensão personalizada, consulte [Publicar sua extensão](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
