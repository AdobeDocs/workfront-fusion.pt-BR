---
title: Visão geral da conexão
description: Para a maioria dos aplicativos, é necessário criar uma conexão, por meio da qual o Adobe Workfront Fusion pode se comunicar com o serviço de terceiros fornecido, de acordo com as configurações do cenário específico.
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Visão geral da conexão

O Workfront Fusion requer uma conexão para a maioria dos aplicativos.  Ele usa essa conexão para se comunicar com o serviço de terceiros fornecido.

Por exemplo, se você quiser criar um cenário que recupere informações do Workfront, deverá conceder permissão para que o Workfront Fusion acesse sua conta do Workfront.

Uma conexão representa a autorização e as permissões que o Fusion usa para acessar o aplicativo. É possível criar uma ou mais conexões para cada aplicativo usado em seus cenários e usar a mesma conexão em vários módulos ou cenários.

A maioria das conexões é usada somente para um único aplicativo. Por exemplo, uma conexão Workfront não pode ser usada em um módulo [!UICONTROL Salesforce]. Alguns aplicativos do [!DNL Adobe] podem compartilhar conexões. Para obter detalhes, consulte os artigos desses aplicativos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

As conexões são de propriedade de equipes. Todos os membros de uma equipe têm acesso às conexões da equipe e os usuários fora de uma equipe não têm acesso às conexões da equipe.

## Direitos de acesso

Para cada conexão, o Workfront Fusion requer somente os direitos de acesso necessários para concluir com êxito um determinado cenário. Por exemplo, se você criar um cenário para baixar um documento do Workfront, o Workfront Fusion não solicitará permissão para criar um novo projeto. Posteriormente, se você descobrir que precisa criar um projeto, poderá atualizar a conexão ou criar uma nova que possa criar projetos.

Nem todos os serviços permitem limitar o acesso a tarefas específicas. Nesses casos, o Workfront Fusion deve exigir direitos de acesso completos. Para obter mais informações sobre como restringir o acesso do Workfront Fusion à sua conta registrada para esses serviços, consulte a documentação específica do aplicativo listada nas [referências de aplicativos do Fusion e seus módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
