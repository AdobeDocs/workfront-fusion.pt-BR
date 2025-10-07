---
title: Visão geral da API
description: As APIs (Application Programming Interfaces, interfaces de programação de aplicativos) são uma maneira de os aplicativos e os serviços se comunicarem entre si. O Fusion usa APIs para se comunicar com o aplicativo ao qual você está se conectando. Cada aplicativo tem uma API separada.
author: Becky
feature: Workfront Fusion
source-git-commit: 1ee32ad1faa8c105142f85e83f1b522548fc7f93
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Visão geral das APIs no Fusion

<!--Add me to TOCs-->

As APIs (Application Programming Interfaces, interfaces de programação de aplicativos) são uma maneira de os aplicativos e os serviços se comunicarem entre si. O Fusion usa APIs para se comunicar com os aplicativos aos quais você está se conectando.

As APIs são criadas e controladas pelos proprietários do aplicativo. Por exemplo, a API do Workfront é de propriedade da equipe do Workfront na Adobe, e a API do Microsoft Graph é de propriedade da Microsoft. O proprietário da API define quais ações estão disponíveis por meio da API.

## Considerações

O fato de as APIs serem definidas pelos seus proprietários e não pelo Fusion leva a algumas considerações importantes:

* **Você pode usar o Fusion para se conectar a qualquer aplicativo ou serviço que tenha uma API pública**, independentemente de o Fusion oferecer ou não um conector dedicado para esse aplicativo ou serviço. Você pode usar os conectores universais do Fusion para trazer esses aplicativos ou serviços para seus cenários.

  Para obter uma lista de conectores universais, consulte [Conectores universais](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

* **As alterações feitas na API de um aplicativo pelo proprietário podem afetar a funcionalidade do Fusion.** Se as alterações forem graves o suficiente, o Fusion talvez precise atualizar módulos ou tipos de conexão ou, em casos extremos, pode criar um novo conector para o aplicativo.

  Para obter mais informações sobre essas situações extremas, conhecidas como &quot;mudanças interruptivas&quot;, consulte [Quebra de alterações](#breaking-changes) neste artigo.


## Quebra de alterações

Uma causa comum para alterações importantes é a desativação, quando um proprietário de API remove parte ou toda a API da disponibilidade. Quando isso ocorre, a equipe do Fusion se esforça para realinhar rapidamente a funcionalidade do Fusion com a nova versão da API do aplicativo. Isso geralmente assume a forma de novos módulos, tipos de conexão ou conectores.

Como os cenários do Fusion são configurados com seus dados específicos, talvez seja necessário atualizar os cenários.

* Se as alterações foram relacionadas à autenticação ou autorização, talvez seja necessário atualizar as conexões desse aplicativo.
* Se as alterações estavam relacionadas a uma ação específica (endpoint) na API, talvez seja necessário atualizar os módulos relacionados a essa ação para uma nova versão do módulo.
* Se toda a versão da API usada pelo Fusion for descontinuada, talvez seja necessário atualizar todos os módulos desse conector para uma nova versão de um conector.

Em muitos casos, é possível atualizar para a nova versão de um módulo sem precisar reconfigurar esse módulo.

Para obter informações e instruções sobre como atualizar um módulo, consulte [Atualizar um módulo para uma nova versão](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
