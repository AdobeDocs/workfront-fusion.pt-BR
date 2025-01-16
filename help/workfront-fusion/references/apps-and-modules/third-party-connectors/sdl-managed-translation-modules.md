---
title: Módulos de tradução gerenciados por SDL
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode conectar sua conta do SDL Managed Translation a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# [!DNL SDL Managed Translation] módulos

Em um cenário do [!DNL Adobe Workfront Fusion], você pode conectar sua conta do [!DNL SDL Managed Translation] a vários aplicativos e serviços de terceiros.

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano [!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Adobe Workfront], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Informações da API de tradução gerenciada por SDL

O conector de Conversão gerenciada SDL usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://languagecloud.sdl.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.4.26</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL SDL Managed Translation] Módulos

>[!NOTE]
>
>O tempo limite da operação para chamadas a [!DNL SDL Managed Translation] é de **120 segundos**.

### Arquivos

#### [!UICONTROL Download Translated File]

Este módulo recupera o conteúdo de um único arquivo traduzido, contido no projeto especificado. Se o arquivo solicitado ainda não estiver no status Downland, talvez o conteúdo do arquivo ainda não tenha sido totalmente traduzido. Se o arquivo estiver no status Download e você o tiver recuperado com êxito, certifique-se de marcar o arquivo como concluído usando o método `Cancel or Complete File`.

#### [!UICONTROL Upload a File]

Esse módulo permite uploads de arquivos para tradução ou para inclusão em um projeto de tradução como material de referência. Os carregamentos devem ser enviados usando várias partes/dados de formulário e podem conter mais de um arquivo. Você especifica o `ProjectOptionId` que deve ser usado para avaliar os arquivos carregados. Isso determina se cada arquivo carregado é um possível candidato para tradução ou deve ser tratado como material de referência. No caso de arquivos mortos (`zip `, `rar`, `7z`, `tar` arquivos), o aplicativo examina o conteúdo do arquivo morto e indica se o arquivo morto como um todo pode ser traduzido ou se contém uma mistura de arquivos traduzíveis e não traduzíveis.

>[!NOTE]
>
>O upload de mais de um arquivo por vez não é recomendado, pois pode aumentar o impacto de qualquer falha.

#### [!UICONTROL Add a Reference File]

Este módulo adiciona um arquivo de referência.

### Projetos

#### [!UICONTROL Create a project]

Este módulo cria o projeto especificado.

#### Cancelar ou concluir um projeto

Este módulo cancela ou conclui o projeto especificado. Se o projeto estiver aguardando o download, ele passará por todas as etapas finais do fluxo de trabalho e, eventualmente, será movido para a conclusão. Se o projeto estiver aguardando aprovação ou a seleção do fornecedor for cancelada. Se o projeto estiver em qualquer outro status, a solicitação falhará.

#### [!UICONTROL Download Project Zip]

Este módulo obtém o arquivo `zip` de arquivos traduzidos para o projeto especificado.

#### [!UICONTROL Read a Project]

Este módulo obtém o projeto especificado.

#### [!UICONTROL Get Projects at Status]

Este módulo obtém todos os projetos disponíveis no status especificado. Este método permite que os resultados sejam paginados, especificando `$top`, `$skip` e `$orderby` parâmetros de consulta.

#### [!UICONTROL Get Projects List]

Obtém uma lista simples de todos os projetos, fornecendo informações gerais sobre cada projeto. Este método permite que os resultados sejam páginas, especificando `$top`, `$skip` e `$orderby` parâmetros de consulta.

#### [!UICONTROL Search Project Creation Options]

Este módulo obtém Opções de Criação de Projeto.

### Outro

#### [!UICONTROL Make an API Call]

Esse módulo executa uma chamada de API autorizada arbitrária.
