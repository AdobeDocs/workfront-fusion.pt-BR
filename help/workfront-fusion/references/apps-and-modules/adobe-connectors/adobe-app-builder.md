---
title: Módulo App Builder do Adobe
description: O conector App Builder do Adobe permite usar funções personalizadas em seus cenários.
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: ac7190293e7c4b3bb9bfd48d73cd59ad687690e6
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 19%

---

# Módulo App Builder do Adobe

É possível criar funções personalizadas na área Funções do Fusion. Em seguida, adicione essas funções aos seus cenários na forma de um módulo do Adobe App Builder.

Como as funções personalizadas funcionam por meio do Adobe App Builder, sua organização deve ter uma licença do Adobe App Builder para usá-las.

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
   <td role="rowheader">Produto</td> 
   <td>
   <p><ul><li>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li><li>Você deve ter uma licença do Adobe App Builder para usar funções personalizadas.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Módulos do Adobe App Builder

### Executar um bloco de código personalizado

Esse módulo permite executar um bloco de código. Você configura o bloco de código ao configurar o módulo e ele é executado quando o módulo é executado durante uma execução de cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Selecione a conexão que contém a função personalizada que você deseja executar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bloco de código]</td> 
   <td>Insira o bloco de código que você deseja que o módulo execute.<p>Para formatar o código e facilitar sua leitura, clique no ícone <b>Formatar código</b>.</td> 
  </tr> 
   </tbody> 
</table>

### Executar uma função personalizada do pacote

Este módulo executa uma função de um pacote.

Para obter informações sobre pacotes, consulte [Usar pacotes de função personalizada](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Selecione a conexão que contém a função personalizada que você deseja executar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pacote]</td> 
   <td>Selecione o pacote que inclui a função que você deseja executar no cenário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variável] </td> 
   <td>Selecione a função que deseja executar no cenário.</p></td> 
  </tr> 
   </tbody> 
</table>

### Usar variável do pacote

Esse módulo traz uma variável configurada em um pacote para o seu cenário.

Para obter informações sobre pacotes, consulte [Usar pacotes de função personalizada](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Selecione a conexão que contém a função personalizada que você deseja executar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pacote]</td> 
   <td>Selecione o pacote que inclui a variável que você deseja trazer para o cenário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variável] </td> 
   <td>Selecione a variável que deseja trazer para o cenário.</p></td> 
  </tr> 
   </tbody> 
</table>

### Executar uma função personalizada ou um bloco de código

Esse módulo permite usar uma função personalizada do JavaScript configurada anteriormente armazenada na área Funções.

Para obter instruções sobre como configurar uma função personalizada, consulte [Mapear dados usando funções personalizadas](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Selecione a conexão que contém a função personalizada que você deseja executar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Selecione a função personalizada que deseja executar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parâmetros] </td> 
   <td>Insira os valores dos parâmetros da função. Os parâmetros disponíveis são baseados nos parâmetros configurados quando a função foi criada.<p>Se um parâmetro tiver um valor padrão, você não o verá no campo, mas poderá substituí-lo inserindo ou mapeando um valor no campo.</p></td> 
  </tr> 
   </tbody> 
</table>




