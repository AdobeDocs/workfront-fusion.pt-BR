---
title: Gerar um segmento de cenário usando IA
description: Você pode usar a IA para inserir um prompt de texto que descreve o que um segmento do seu cenário precisa fazer. O Fusion gera, em seguida, um ou mais módulos que executam essas ações, que podem ser usadas no seu cenário.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 1%

---

# Gerar um segmento de cenário usando IA

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

Você pode usar a IA para inserir um prompt de texto que descreve o que um segmento do seu cenário precisa fazer. O Fusion gera, em seguida, um ou mais módulos que executam essas ações, que podem ser usadas no seu cenário.

Os segmentos de cenário gerados contêm módulos para um único conector. Para gerar módulos para um conector diferente, crie um prompt separado e junte os segmentos do cenário no seu cenário.

Assim como em qualquer coisa gerada pela IA, recomendamos que você verifique e teste os módulos gerados para garantir que eles estejam funcionando conforme o esperado.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote de Automação e Integração do Adobe Workfront</p><p>Workfront Ultimate</p><p>Workfront Prime e pacotes Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Standard</p><p>Trabalhar ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++## Pré-requisitos

Sua organização deve atender aos seguintes pré-requisitos para usar essa funcionalidade:

* Sua organização deve ter participado do programa Workfront AI Assistant Beta.
* A Adobe deve ter um contrato Gen AI da Adobe assinado no arquivo para sua organização.

  Para obter mais informações sobre como assinar o contrato, consulte [Assinar o contrato da Adobe Gen AI](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement) no artigo Visão geral do Assistente de IA na documentação da Workfront.

## Aplicativos do módulo de IA compatíveis no momento

A Fusion AI pode atualmente gerar módulos que se conectam aos seguintes aplicativos:

* Adobe Firefly
* Azure OpenAI
* Gráfico do Microsoft
* Planejamento do Adobe Workfront
* Adobe Analytics
* Serviços da Adobe PDF
* Adobe Marketo
* Adobe Frame.io
* Dropbox
* NetSuite
* Calendário do Google
* Atlassian Jira
* GitLab
* Spotify
* Bitbucket
* OpenAI
* Slack

## Gerar módulos

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja adicionar um módulo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no ícone do **Assistente de IA** ![ícone do Assistente de IA](assets/ai-assistant-icon.png) próximo ao canto superior direito da tela.
1. Insira um prompt de texto no painel Assistente do AI.

   Para obter dicas sobre solicitações, consulte [Dicas para criar solicitações para segmentos de cenário](#tips-for-creating-prompts-for-scenario-segments) neste artigo.

   O Assistente de IA gera o módulo ou conjunto de módulos.
1. (Condicional) Se necessário, adicione seu token de API do aplicativo nos módulos.
1. Verifique os módulos para garantir que eles estejam configurados para o aplicativo e a ação apropriados.
1. (Condicional) Se a seção de cenário gerada não estiver anexada ao seu cenário, arraste-a para o lugar.

Recomendamos testar os módulos para garantir que eles estejam funcionando como esperado.

## Dicas para criar prompts para segmentos de cenário

Os prompts de texto devem incluir as seguintes informações no mínimo:

* O aplicativo ao qual você está se conectando
* A ação ou ações que você deseja executar

>[!IMPORTANT]
>
>Você pode gerar mais de um módulo por vez, mas só pode gerar módulos para um aplicativo por vez.

>[!BEGINSHADEBOX]

**Exemplos**:

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`
Isso inclui o aplicativo `Workfront Planning` e a ação `delete records`. Esse prompt cria três módulos, um para cada registro que será excluído.
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`
Isso inclui o aplicativo `Workfront Planning` e a ação `change campaign summary`.
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`
Isso inclui o aplicativo `Workfront Planning` e a ação `get field details`.

O exemplo a seguir NÃO está correto:

* `Generate an image in Adobe Firefly and upload it to Dropbox`

  Este exemplo está incorreto porque inclui mais de um aplicativo

>[!ENDSHADEBOX]

Considere o seguinte ao criar prompts de texto:

* Use linguagem simples e direta.
* Verifique e teste o segmento do cenário. Se o desempenho não for o esperado, refine o prompt e tente novamente.
