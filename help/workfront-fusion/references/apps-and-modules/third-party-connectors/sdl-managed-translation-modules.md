---
title: Módulos do SDL Managed Translation
description: Em um cenário do Adobe Workfront Fusion, é possível conectar sua conta do SDL Managed Translation a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
TQID: https://experienceleague.adobe.com/J6v5bxEi3MzcrkaiQQFOpToDzon0K-BhpmuJQe8sdgY
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 567
ht-degree: 24%

---

# Módulos do [!DNL SDL Managed Translation]

Em um cenário do Adobe Workfront Fusion, é possível conectar a conta do [!DNL SDL Managed Translation] a vários aplicativos e serviços de terceiros.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote do Adobe Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Os pacotes Workfront Prime e Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p><p>Trabalho ou maior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

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

#### [!UICONTROL Fazer upload de um arquivo]

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
