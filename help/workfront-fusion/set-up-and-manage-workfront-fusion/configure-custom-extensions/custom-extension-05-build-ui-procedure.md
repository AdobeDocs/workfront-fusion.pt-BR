---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Criar a interface de extensão personalizada
description: Criar a interface de extensão personalizada
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
source-wordcount: 440
ht-degree: 0%

---


# Criar a interface de extensão personalizada

>[!NOTE]
>
>Este artigo presume alguma familiaridade com ferramentas de desenvolvimento de software.

Este procedimento descreve como criar a tela que os usuários realmente veem e concluir a **conexão (&quot;handshake&quot;)** com o Fusion.

Durante esse processo, é importante lembrar que sua extensão é executada em dois quadros: o quadro oculto **registro** e o quadro visível **interface**.

Para obter informações sobre quadros em relação a extensões personalizadas, consulte [Quadros incluídos em uma Extensão de Interface do Usuário](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

Para obter instruções sobre como criar o quadro de registro, consulte [Criar um projeto para Extensibilidade da Interface do Usuário](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

## Rota entre os dois quadros

Ambos os quadros carregam o mesmo `index.html`; um pequeno roteador front-end decide qual componente mostrar com base no URL.

1. Configurar as rotas em `web-src/src/components/App.js`. A parte essencial é:

   ```jsx
   import { HashRouter as Router, Routes, Route } from "react-router-dom";
   import ExtensionRegistration from "./ExtensionRegistration";
   import DashboardWidget from "./DashboardWidget";
   
   export default function App() {
     return (
       <Router>
         <Routes>
           {/* Background frame: registers the extension with Fusion */}
           <Route index element={<ExtensionRegistration />} />
           <Route path="index.html" element={<ExtensionRegistration />} />
   
           {/* Visible frame: the URL you returned from getWidget() */}
           <Route path="my-widget" element={<DashboardWidget />} />
         </Routes>
       </Router>
     );
   }
   ```

   Essas rotas são mapeadas para a configuração anterior da seguinte maneira:

   * A rota padrão (`index`) renderiza **`ExtensionRegistration`**, o quadro oculto que chama `register(...)`.
   * A rota `my-widget` renderiza **`DashboardWidget`**, sua interface do usuário visível. Isto corresponde à `url: "/index.html#/my-widget"` que você retornou de `getWidget()` em [a página anterior](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

   >[!NOTE]
   >
   > **As rotas e a URL `getWidget` devem estar de acordo.** Se você alterar o nome da rota, altere o `url` também, ou o Fusion carregará uma página em branco.

1. Continue para [Concluir o handshake com `attach`](#complete-the-handshake-with-attach).

## Conclua o handshake com `attach`

Esta é a única linha mais importante na interface do usuário visível. Quando o Fusion abre o quadro da interface do usuário, ele aguarda o quadro &quot;fazer check-in&quot;. Seu código é verificado chamando `attach({ id })`.

**Se isso for omitido, o Fusion expirará** com um erro como *&quot;aguardando mensagem inicial do iframe de destino.&quot;*

1. Adicionar o seguinte a `web-src/src/components/DashboardWidget.js`:

   ```jsx
   import { useEffect, useState } from "react";
   import { attach } from "@adobe/uix-guest";
   import { extensionId } from "./Constants";
   
   export default function DashboardWidget() {
     const [connection, setConnection] = useState(null);
   
     useEffect(() => {
       // Tell Fusion this UI frame is ready. Required.
       attach({ id: extensionId })
         .then(setConnection)
         .catch((e) => console.error("attach failed", e));
     }, []);
   
     if (!connection) {
       return <p>Connecting to Fusion...</p>;
     }
   
     return <h2>Hello from my Fusion extension!</h2>;
   }
   ```

   Esse código faz o seguinte:

   * `attach({ id })` retorna um **objeto de conexão** assim que Fusion responde. Recomendamos salvar, pois você o usará na próxima etapa para ler o contexto que o Fusion envia.
   * Até que a conexão seja resolvida, um curto &quot;Conectando...&quot; é exibida.
   * Usa o **mesmo`extensionId`** definido em `Constants.js`.

   Neste ponto, você tem uma extensão de trabalho: ela registra, anexa e mostra uma mensagem. Tudo depois disso é sobre usar os dados que a Fusão oferece.

1. Continue para [Ler os compartilhamentos de Fusão de contexto](#read-the-context-fusion-shares).

## Ler o contexto Compartilhamentos do Fusion

Depois de anexada, a conexão expõe um **contexto compartilhado** com informações sobre o usuário, a organização e a equipe atuais. Você pode ler valores individuais com `connection.sharedContext.get("<key>")`:

```jsx
const orgId = connection.sharedContext.get("imsOrgId");
const organization = connection.sharedContext.get("organization"); // full Fusion org
const user = connection.sharedContext.get("user");                 // full Fusion user
```

Este exemplo mostra um exemplo completo e reativo que também é atualizado quando o usuário alterna entre organização ou equipe:

```jsx
import { useEffect, useState } from "react";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

function readContext(source) {
  // sharedContext behaves like a Map (.get); the change event gives a plain object.
  const get =
    typeof source.get === "function" ? (k) => source.get(k) : (k) => source[k];
  return Object.fromEntries(KEYS.map((k) => [k, get(k)]));
}

export default function DashboardWidget() {
  const [context, setContext] = useState(null);

  useEffect(() => {
    let cleanup = () => {};
    attach({ id: extensionId })
      .then((connection) => {
        // 1) initial values
        setContext(readContext(connection.sharedContext));

        // 2) react to org/team/user changes pushed by Fusion
        const onChange = (event) =>
          setContext(readContext(event?.detail?.context ?? connection.sharedContext));
        connection.addEventListener("contextchange", onChange);
        cleanup = () => connection.removeEventListener?.("contextchange", onChange);
      })
      .catch((e) => console.error("attach failed", e));
    return () => cleanup();
  }, []);

  if (!context) return <p>Connecting to Fusion...</p>;

  return (
    <div>
      <h2>{context.organization?.name ?? "No organization"}</h2>
      <p>Signed in as {context.user?.name} ({context.user?.email})</p>
      <p>IMS org: {context.imsOrgId}</p>
    </div>
  );
}
```

Lembre-se do seguinte:

* **Ler valores iniciais** de `connection.sharedContext.get(key)` logo após `attach`.
* **Inscreva-se em`contextchange`** para permanecer sincronizado. O Fusion aciona esse evento sempre que a organização, a equipe ou o usuário ativos são alterados. Os novos valores chegam em `event.detail.context`.

Para obter a lista completa de chaves e o que cada uma contém, consulte a [Referência de contexto do Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

Para continuar o processo de configuração da extensão personalizada, vá para [A referência de contexto do Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
