---
title: Gerar um segmento de cenário usando IA
description: Você pode usar a IA para inserir um prompt de texto que descreve o que um segmento do seu cenário precisa fazer. O Fusion gera, em seguida, um ou mais módulos que executam essas ações, que podem ser usadas no seu cenário.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: 9d29abc82a3bb09affc4d17d7ea214d7bb850294
workflow-type: tm+mt
source-wordcount: '600'
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

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacote</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença</td> 
   <td> <p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou plano do [!UICONTROL Prime] [!DNL Workfront]: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plano: [!DNL Workfront Fusion] está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Sua organização deve atender aos seguintes pré-requisitos para usar essa funcionalidade:

* Sua organização deve ter participado do programa Workfront AI Assistant Beta.
* O Adobe deve ter um contrato de geração de IA de Adobe assinado no arquivo para sua organização.

  Para obter mais informações sobre como assinar o contrato, consulte [Assinar o contrato do Adobe Gen AI](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement) no artigo Visão geral do Assistente de IA na documentação da Workfront.

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

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
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
