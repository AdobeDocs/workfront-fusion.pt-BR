---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Visão geral de extensibilidade da interface do usuário
description: Extensões personalizadas no Workfront Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 835
ht-degree: 0%

---

# Visão geral de extensibilidade da interface do usuário

A Extensibilidade da interface do usuário permite trazer sua lógica personalizada e a interface do usuário (interface do usuário) para o Adobe Workfront Fusion. Ao usar o Adobe App Builder, você pode modificar a experiência do Workfront Fusion da sua organização para atender melhor às necessidades da organização, enquanto ainda depende da funcionalidade principal do Fusion.

Este artigo fornece uma visão geral da Extensibilidade da interface e como sua extensão personalizada se comunica com o Workfront Fusion.

## Estrutura da extensão

* [Hosts e convidados](#hosts-and-guests)
* [A tecnologia subjacente](#the-technology-underneath)

### Hosts e convidados

O Fusion pode exibir a interface do usuário que não foi criada pela equipe do Workfront Fusion. Para garantir que essas alterações na interface do usuário não afetem a funcionalidade principal do Fusion, a interface do usuário é executada em seu próprio quadro isolado do navegador (um `<iframe>`), completamente separado do código do Fusion.

* **Host**: o aplicativo que *contém* a extensão. Aqui, isto é **Fusion**. O host decide onde as extensões podem aparecer e quais dados serão compartilhados com ele.
* **Convidado**: *Sua* extensão. É um pequeno aplicativo da Web que o host carrega em um iframe.

Ao criar uma Extensão de interface do usuário, você não modifica o Fusion. Você cria e publica um convidado, que o Fusion pode usar após a publicação do convidado.

### A tecnologia subjacente

Seu convidado é construído com duas tecnologias Adobe:

* **Adobe App Builder**: uma plataforma gratuita de hospedagem e ferramentas para pequenos aplicativos Web e ações sem servidor. Sua extensão é um aplicativo App Builder. O App Builder fornece um local para hospedar sua interface do usuário (na rede de entrega de conteúdo `*.adobeio-static.net` da Adobe) e uma ferramenta de linha de comando chamada `aio` para criá-la, compilá-la e publicá-la.
* **Adobe UI Extensibility SDK (UIX)**: As bibliotecas que permitem que o host e o convidado conversem. Você usará um pacote, `@adobe/uix-guest`, do seu lado. O Fusion usa o pacote `@adobe/uix-host` correspondente em seu lado.

<!--

```
   ┌────────── Browser ─────────────────────────────┐
   │                                                                   │
   │   Fusion (Host)                      Your extension (Guest)       │
   │   ────────────                       ─────────────────────        │
   │   @adobe/uix-host   ◀── messages ──▶  @adobe/uix-guest            │
   │        │                                    │                     │
   │   renders an iframe ───────────────▶  your React/HTML UI          │
   │                                                                   │
   └───────────────────────────────────────────────────────────────────┘

   Your UI files are hosted by Adobe App Builder at
   https://<your-app>.adobeio-static.net
```

-->

## Pontos de extensão

Um ponto de extensão é um &quot;slot&quot; nomeado no host em que um convidado pode aparecer. O Fusion define seus slots e você escolhe qual deles o convidado usará.

Um nome de ponto de extensão tem três partes: `service/name/version`.

O Fusion oferece os seguintes pontos de extensão:

| Ponto de extensão | Onde sua interface do usuário aparece no Fusion | Quando usá-lo |
| --- | --- | ---- |
| `fusion/nav-organization/1` | Na seção **Organização** da navegação à esquerda. | Sua ferramenta trata de toda a organização. |
| `fusion/nav-team/1` | Na seção **Equipe** da navegação à esquerda (exibida quando uma equipe é selecionada). | A ferramenta tem aproximadamente uma equipe específica. |

* `fusion` é o **serviço** (o produto, Fusion).
* `nav-organization` / `nav-team` é o **nome** (o slot específico).
* `1` é a **versão**.

Uma extensão pode implementar um ou ambos os pontos de extensão. A maioria das extensões usa um ponto.

Com base no ponto de extensão selecionado, o Fusion adiciona um botão com o título da extensão à seção de navegação correspondente. Clicar nela abre uma página dedicada na área de conteúdo principal do Fusion e carrega sua interface de usuário lá.

## Quadros incluídos em uma extensão da interface do usuário

>[!IMPORTANT]
>
>Esta seção discute um aspecto das extensões da interface do usuário que pode causar confusão. Recomendamos lê-lo com cuidado.

Quando o Fusion carrega seu convidado, sua extensão é executada em **dois** quadros:

1. **O quadro de registro (invisível).** É executado primeiro, em segundo plano. O quadro de registro informa ao Fusion o que sua extensão oferece. Por exemplo, ele pode indicar que tem um widget de painel e enviar o título do widget e o URL de sua interface do usuário. O quadro de registro faz isso chamando `register(...)`. Ela não renderiza nenhuma interface do usuário visível.
1. **O quadro da interface do usuário (visível).** Esta é a página que o Fusion mostra ao usuário. Ele deve se anunciar ao host, chamando `attach(...)`. Se ele nunca chamar `attach`, o Fusion aguardará e eventualmente expirará com um erro.

>[!BEGINSHADEBOX]

Este exemplo mostra o fluxo quando um usuário clica no botão de extensão.

1. O botão é clicado.
1. O Fusion carrega o quadro REGISTRATION (oculto).

   ```
   register({ methods: { dashboard: { getWidget() {...} } } })
   ```

   `getWidget()` retorna a URL da interface visível
1. O Fusion carrega o quadro da interface do usuário (visível) nesse URL.

   ```
   attach({ id }) 
   ```

   Isso é necessário ou o Fusion atinge o tempo limite
1. O Fusion envia contexto e a interface do usuário é renderizada.

>[!ENDSHADEBOX]

Ambos os quadros são gravados quando você constrói a interface do usuário. O importante é lembrar que a página visível **deve** chama `attach`.

Para obter mais informações sobre como criar a interface, consulte [Criar a interface de extensão personalizada](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

## Contexto do Fusion

Depois que a extensão é anexada, o Fusion compartilha um objeto `context` com o convidado. Ele contém:

* **Usuário**: o perfil Fusion do usuário conectado e a ID de usuário do Adobe IMS.
* **Organização**: o registro completo da organização do Fusion da ativa e a ID da organização do Adobe IMS.
* **Equipe**: a equipe ativa, quando aplicável.
* **Token de acesso do Adobe IMS**: chama as APIs do Adobe ou Fusion em nome do usuário, se necessário.

O Fusion também envia atualizações. Por exemplo, se o usuário alternar entre organização ou equipe enquanto sua interface do usuário estiver aberta, o Fusion enviará o novo contexto para que sua interface do usuário possa reagir instantaneamente.

Para obter a lista completa dos campos de contexto, consulte [A referência de contexto do Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Criação de uma extensão da interface do usuário

Para criar uma extensão de interface do usuário, siga estas etapas:

1. [Instale as ferramentas e crie um projeto do Adobe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
1. [Gere um projeto App Builder em branco, aponte-o para um ponto de extensão Fusion e registre seu widget](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).
1. [Crie a interface do usuário e conecte-se ao Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
1. [Usar os envios de Fusão de contexto](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
1. [Publique para que o Fusion possa encontrá-lo](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. (Opcional) [Chame APIs do Workfront/Fusion para obter dados reais sem o CORS](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).

Para iniciar o processo, vá para [Configurar suas ferramentas e a conta da Adobe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


