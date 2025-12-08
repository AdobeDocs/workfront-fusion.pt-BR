---
title: Visão geral da API
description: As APIs (Application Programming Interfaces, interfaces de programação de aplicativos) são uma maneira de aplicativos e serviços se comunicarem entre si. O Fusion usa APIs para se comunicar com o aplicativo ao qual você está se conectando. Cada aplicativo tem uma API separada.
author: Becky
feature: Workfront Fusion
source-git-commit: b30aac8040cc0b6bcad92914b1c0997a8ddebdd5
workflow-type: ht
source-wordcount: '431'
ht-degree: 100%

---

# Visão geral de APIs no Fusion

<!--Add me to TOCs-->

As APIs (Application Programming Interfaces, interfaces de programação de aplicativos) são uma maneira de aplicativos e serviços se comunicarem entre si. O Fusion usa APIs para se comunicar com os aplicativos aos quais você está se conectando.

As APIs são criadas e controladas pelos proprietários do aplicativo. Por exemplo, a API do Workfront é de propriedade da equipe do Workfront na Adobe, e a API do Microsoft Graph é de propriedade da Microsoft. O proprietário da API define quais ações estão disponíveis por meio dela.

## Considerações

O fato das APIs serem definidas por seus proprietários e não pelo Fusion leva a algumas considerações importantes:

* **Você pode usar o Fusion para se conectar a qualquer aplicativo ou serviço que tenha uma API pública**, independentemente de o Fusion oferecer ou não um conector dedicado para esse aplicativo ou serviço. Você pode usar os conectores universais do Fusion para trazer esses aplicativos ou serviços para seus cenários.

  Para obter uma lista de conectores universais, consulte [Conectores universais](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

* **As alterações feitas na API de um aplicativo pelo proprietário podem afetar a funcionalidade do Fusion.** Se as alterações forem graves o suficiente, o Fusion talvez precise atualizar módulos ou tipos de conexão ou, em casos extremos, criar um novo conector para o aplicativo.

  Para obter mais informações sobre essas situações extremas, conhecidas como &quot;alterações drásticas&quot;, consulte [Alterações drásticas](#breaking-changes) neste artigo.


## Alterações drásticas

Uma causa comum para alterações drásticas é a descontinuação, quando um proprietário de API torna parte ou toda a API indisponível. Quando isso ocorre, a equipe do Fusion se esforça para realinhar rapidamente a funcionalidade do Fusion com a nova versão da API do aplicativo. Isso geralmente assume a forma de novos módulos, tipos de conexão ou conectores.

Como os cenários do Fusion são configurados com seus dados específicos, talvez seja necessário você atualizar os cenários.

* Se as alterações foram relacionadas à autenticação ou autorização, talvez seja necessário você atualizar as conexões desse aplicativo.
* Se as alterações forem relacionadas a uma ação específica (ponto de acesso) na API, talvez seja necessário atualizar qualquer módulo relacionado a essa ação para uma nova versão do módulo.
* Se toda a versão da API usada pelo Fusion for descontinuada, talvez seja necessário atualizar todos os módulos desse conector para uma nova versão do conector.

Em muitos casos, você pode atualizar para a nova versão de um módulo sem precisar reconfigurá-lo.

Para obter informações e instruções sobre como atualizar um módulo, consulte [Atualizar um módulo para uma nova versão](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
