---
title: Módulos do Qualtrics
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Qualtrics, bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 80b441b7-c808-4c4f-b9ff-d614650dbb73
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 1%

---

# Módulos do Qualtrics

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Qualtrics], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (herdado): automação e integração do Workfront Fusion for Work </p>
   </td> 
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

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos do [!DNL Qualtrics], você deve ter uma conta do [!UICONTROL Qualtrics].

## Informações da API do Qualtrics

O conector Qualtrics usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td> https://{{connection.dataCenterCode}}.qualtrics.com/API/v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.1.1</td> 
  </tr>
 </tbody> 
 </table>

## Conectando o [!DNL Qualtrics] ao Workfront Fusion

Você pode criar uma conexão com sua conta do [!DNL Qualtrics] diretamente de dentro de um módulo do [!UICONTROL Qualtrics].

1. Em qualquer módulo do [!UICONTROL Qualtrics], clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. Insira as seguintes informações:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Nome da Conexão]</p> </td> 
      <td> <p>Insira um nome para a nova conexão.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL ID do Centro de Dados] </td> 
      <td>Use o formato <code>&lt;Data Center ID>.qualtrics.com</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Chave de API]</td> 
      <td>Para localizar sua chave de API, consulte a documentação do [!DNL Qualtrics].</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## [!DNL Qualtrics] módulos e seus campos

Os seguintes módulos estão disponíveis para o conector [!DNL Qualtrics]:

* [!UICONTROL Assista à nova resposta da pesquisa]
* [!UICONTROL Criar um Contato de Diretório]
* [!UICONTROL Excluir um Contato do Diretório]
* [!UICONTROL Obter um Contato do Diretório]
* [!UICONTROL Atualizar um Contato do Diretório]
* [!UICONTROL Criar uma Nova Distribuição de Pesquisa via SMS]
* [!UICONTROL Distribuir uma Pesquisa por Email]
* [!UICONTROL Fazer uma chamada de API]
* [!UICONTROL Listar Contatos do Diretório]
