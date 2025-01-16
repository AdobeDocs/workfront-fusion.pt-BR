---
title: Licenças do Adobe Workfront Fusion
description: O Adobe Workfront Fusion oferece duas licenças diferentes que determinam a funcionalidade que você pode acessar. Sua organização escolheu uma dessas licenças ao comprar o Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6e2df1a0-c1f9-4833-b1c2-65efb3be9657
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 1%

---

# Licenças do Adobe Workfront Fusion

O Workfront Fusion tem dois modelos de licenciamento, um novo modelo baseado em operações e um modelo herdado baseado em conector.

## Modelo de licenciamento baseado em operações (Novo)

O novo modelo de licenciamento do Workfront Fusion é baseado no número de operações que sua organização usa. Nesse modelo, todas as organizações têm acesso à mesma funcionalidade.

Se sua organização tiver um plano do Workfront Ultimate, sua instância do Fusion será incluída em seu plano e permitirá um número ilimitado de operações do Fusion por mês. Se sua organização tiver um plano Workfront Prime ou Select, o Fusion poderá ser comprado e o preço será baseado no número de operações realizadas em um mês.

Para obter informações sobre o que conta como uma operação no novo modelo de licenciamento, consulte [Operações](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

## Modelo de licenciamento baseado em conector (herdado)

No modelo de licenciamento herdado do Adobe Workfront Fusion, o Fusion oferece duas licenças diferentes que determinam a funcionalidade que você pode acessar. Sua organização escolheu uma dessas licenças ao comprar o Workfront Fusion.

* [Automação do Workfront Fusion for Work](#workfront-fusion-for-work-automation)
* [Automação e integração do Workfront Fusion for Work](#workfront-fusion-for-work-automation-and-integration)

Para descobrir que tipo de licença do Workfront Fusion sua organização tem, entre em contato com o administrador do Workfront Fusion.

### Automação do Workfront Fusion for Work

* [Benefícios da automação do Workfront Fusion for Work](#benefits-of-workfront-fusion-for-work-automation)
* [Conectores e módulos disponíveis para a Automação de Trabalho do Workfront Fusion for](#connectors-and-modules-available-for-workfront-fusion-for-work-automation)
* [Exemplo de Workfront Fusion para Automação de Trabalho](#example-of-workfront-fusion-for-work-automation)

#### Benefícios da automação do Workfront Fusion for Work

Uma licença do Workfront Fusion for Work Automation permite automatizar os fluxos de trabalho do [!DNL Workfront]. Ao usar o Workfront Fusion for Work Automation, é possível criar cenários para automatizar os processos de trabalho exclusivos de sua organização.

Os benefícios da automatização dos processos do [!DNL Workfront] incluem:

* A automação é mais rápida e menos propensa a erros.
* Fluxos de trabalho que não exigem nenhuma decisão ou que têm decisões são baseados em lógica simples, como se/então, são bons candidatos para automação.
* A automação pode atender a necessidades específicas em workflows usados pela sua organização que não são abordados diretamente no produto do Workfront.

#### Conectores e módulos disponíveis para a Automação de Trabalho do Workfront Fusion for

Com a licença do Workfront Fusion for Work Automation, você tem acesso ao seguinte:

* Adobe Workfront
* Prova do Workfront
* Webhooks
* Módulos de ferramentas e transformadores, como:

   * Arquivo
   * CSV
   * Armazenamentos de dados
   * Imagem
   * JSON
   * Matemática
   * MIME
   * XML

#### Exemplo de Workfront Fusion para Automação de Trabalho

O exemplo a seguir mostra um workflow que:

1. Verifica uma alteração de campo
1. Obtém informações sobre o objeto ao qual o campo está anexado, incluindo a quem o objeto está atribuído
1. Envia uma notificação sobre a alteração do campo para o usuário ao qual o objeto está atribuído

![Exemplo de automação](assets/fusion-template-example.png)

### Automação e integração do Workfront Fusion for Work

* [Benefícios da Automação e Integração do Workfront Fusion for Work](#benefits-of-workfront-fusion-for-work-automation-and-integration)
* [Conectores e módulos disponíveis para Automação e Integração do Workfront Fusion for Work](#connectors-and-modules-available-for-workfront-fusion-for-work-automation-and-integration)
* [Exemplo de automação e integração do Workfront Fusion for Work](#example-of-workfront-fusion-for-work-automation-and-integration)

#### Benefícios da Automação e Integração do Workfront Fusion for Work {#benefits-of-workfront-fusion-for-work-automation-and-integration}

Uma licença do Workfront Fusion for Work Automation and Integration permite acessar todas as funcionalidades da licença do Workfront Fusion for Work Automation. Além disso, essa licença permite usar outros aplicativos e serviços em seus cenários. Por exemplo, você pode usar o Workfront Fusion para automatizar um processo que importa tíquetes Jira e, em seguida, os transforma em tarefas no Workfront. Você também pode usar os conectores HTTP ou SFTP para se conectar a quase qualquer serviço da Web, mesmo se o Workfront Fusion não tiver um conector dedicado para ele.

Os benefícios de uma licença de Automação e Integração do Workfront Fusion for Work incluem:

* A Automação e Integração do Workfront Fusion for Work inclui todos os benefícios associados à Automação do Workfront Fusion for Work
* A integração reduz a necessidade de entrar e sair de vários aplicativos ao concluir um fluxo de trabalho.
* A automatização da transferência de dados entre aplicativos é mais rápida e menos propensa a erros do que a transferência manual de dados

#### Conectores e módulos disponíveis para Automação e Integração do Workfront Fusion for Work

Para obter uma lista de conectores dedicados disponíveis, consulte [Referências de aplicativos Fusion e seus módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!IMPORTANT]
>
>O Workfront Fusion pode se conectar a quase qualquer serviço da Web. Se o aplicativo com o qual você deseja trabalhar não tiver um conector dedicado, você poderá usar os conectores do [!UICONTROL HTTP], [!UICONTROL SFTP] ou [!UICONTROL JSON] para se conectar diretamente ao serviço Web.

#### Exemplo de automação e integração do Workfront Fusion for Work

O exemplo a seguir mostra um workflow que:

1. Observa uma planilha para novos usuários
1. Verifica se o usuário existe em [!DNL Workfront]
1. Cria o usuário em [!DNL Workfront] se ele não existir
1. Carrega a ID de usuário [!DNL Workfront] de volta para a planilha.

![Exemplo de cenário de automação](assets/fusion-integration-example.png)
