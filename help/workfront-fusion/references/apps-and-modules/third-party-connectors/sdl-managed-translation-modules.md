---
title: Módulos de tradução gerenciados por SDL
description: Em um cenário do Adobe Workfront Fusion, é possível conectar sua conta do SDL Managed Translation a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 1%

---

# [!DNL SDL Managed Translation] módulos

Em um cenário do Adobe Workfront Fusion, é possível conectar a conta do [!DNL SDL Managed Translation] a vários aplicativos e serviços de terceiros.

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">plano do Adobe Workfront*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença da Adobe Workfront*</td>
   <td> <p>[!UICONTROL Plano], [!UICONTROL Trabalho]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Requisito de licença herdado: [!UICONTROL Workfront Fusion para Automação e Integração do Trabalho] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano do Adobe Workfront [!UICONTROL Select] ou [!UICONTROL Prime], sua organização deve comprar o Adobe Workfront Fusion, bem como o Adobe Workfront, para usar a funcionalidade descrita neste artigo. O Workfront Fusion está incluído no plano do Workfront da [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o Adobe Workfront Fusion e o Adobe Workfront para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para descobrir seu plano, tipo de licença ou acesso, entre em contato com o administrador do Workfront.

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Informações da API de tradução gerenciada por SDL

O conector de Conversão gerenciada SDL usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
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

#### [!UICONTROL Baixar Arquivo Traduzido]

Este módulo recupera o conteúdo de um único arquivo traduzido, contido no projeto especificado. Se o arquivo solicitado ainda não estiver no status Downland, talvez o conteúdo do arquivo ainda não tenha sido totalmente traduzido. Se o arquivo estiver no status Download e você o tiver recuperado com êxito, certifique-se de marcar o arquivo como concluído usando o método `Cancel or Complete File`.

#### [!UICONTROL Carregar um arquivo]

Esse módulo permite uploads de arquivos para tradução ou para inclusão em um projeto de tradução como material de referência. Os carregamentos devem ser enviados usando várias partes/dados de formulário e podem conter mais de um arquivo. Você especifica o `ProjectOptionId` que deve ser usado para avaliar os arquivos carregados. Isso determina se cada arquivo carregado é um possível candidato para tradução ou deve ser tratado como material de referência. No caso de arquivos mortos (`zip `, `rar`, `7z`, `tar` arquivos), o aplicativo examina o conteúdo do arquivo morto e indica se o arquivo morto como um todo pode ser traduzido ou se contém uma mistura de arquivos traduzíveis e não traduzíveis.

>[!NOTE]
>
>O upload de mais de um arquivo por vez não é recomendado, pois pode aumentar o impacto de qualquer falha.

#### [!UICONTROL Adicionar um Arquivo de Referência]

Este módulo adiciona um arquivo de referência.

### Projetos

#### [!UICONTROL Criar um projeto]

Este módulo cria o projeto especificado.

#### Cancelar ou concluir um projeto

Este módulo cancela ou conclui o projeto especificado. Se o projeto estiver aguardando o download, ele passará por todas as etapas finais do fluxo de trabalho e, eventualmente, será movido para a conclusão. Se o projeto estiver aguardando aprovação ou a seleção do fornecedor for cancelada. Se o projeto estiver em qualquer outro status, a solicitação falhará.

#### [!UICONTROL Baixar o Zip do Projeto]

Este módulo obtém o arquivo `zip` de arquivos traduzidos para o projeto especificado.

#### [!UICONTROL Ler um projeto]

Este módulo obtém o projeto especificado.

#### [!UICONTROL Obter Projetos no Status]

Este módulo obtém todos os projetos disponíveis no status especificado. Este método permite que os resultados sejam paginados, especificando `$top`, `$skip` e `$orderby` parâmetros de consulta.

#### [!UICONTROL Obter Lista de Projetos]

Obtém uma lista simples de todos os projetos, fornecendo informações gerais sobre cada projeto. Este método permite que os resultados sejam páginas, especificando `$top`, `$skip` e `$orderby` parâmetros de consulta.

#### [!UICONTROL Pesquisar Opções de Criação de Projeto]

Este módulo obtém Opções de Criação de Projeto.

### Outras

#### [!UICONTROL Fazer uma chamada de API]

Esse módulo executa uma chamada de API autorizada arbitrária.
