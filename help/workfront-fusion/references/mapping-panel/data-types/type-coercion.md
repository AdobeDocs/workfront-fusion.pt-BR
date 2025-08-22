---
title: Coerção de tipo
description: Este documento descreve como o Adobe Workfront Fusion se comporta em situações em que recebe valores em formatos de dados esperados e inesperados.
author: Becky
feature: Workfront Fusion
exl-id: a8bdd36d-c01f-4019-a3ea-fb185101500e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 5%

---

# Coerção de tipo

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">plano do Adobe Workfront*</td> 
   <td> <p>[!DNL Pro] ou superior</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença da Adobe Workfront*</td> 
   <td> <p>[!UICONTROL Plano], [!UICONTROL Trabalho]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença [!UICONTROL Adobe Workfront Fusion]**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Requisito de licença herdado: [!UICONTROL Workfront Fusion para Automação e Integração do Trabalho] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o plano do [!UICONTROL Select] ou do [!UICONTROL Prime] para Adobe Workfront, sua organização deve comprar o Adobe Workfront Fusion e o Adobe Workfront para usar a funcionalidade descrita neste artigo. O Workfront Fusion está incluído no plano do Workfront da [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o Adobe Workfront Fusion e o Adobe Workfront para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para descobrir seu plano, tipo de licença ou acesso, entre em contato com o administrador do Workfront.

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

### Coerção de tipo

Este documento descreve como o Adobe Workfront Fusion se comporta em situações em que recebe valores em formatos de dados esperados e inesperados.

<table style="table-layout:auto">
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Esperado</th> 
   <th>Recebido</th> 
   <th> <p>Descrição</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>matriz </td> 
   <td>matriz </td> 
   <td> <p>O valor é entregue inalterado.</p> </td> 
  </tr> 
  <tr> 
   <td>matriz </td> 
   <td>outro </td> 
   <td> <p>Se o valor recebido não for do tipo de matriz, o Workfront Fusion criará uma matriz e o primeiro (e único) elemento será o valor recebido.</p> </td> 
  </tr> 
  <tr> 
   <td>booleano </td> 
   <td>booleano </td> 
   <td> <p>O valor é entregue inalterado.</p> </td> 
  </tr> 
  <tr> 
   <td>booleano </td> 
   <td>número </td> 
   <td> <p>O valor é convertido em Sim lógico, mesmo se o valor for 0.</p> </td> 
  </tr> 
  <tr> 
   <td>booleano </td> 
   <td>texto </td> 
   <td> <p>Se o valor for igual a false ou o valor estiver vazio, ele será convertido para o Nº lógico. Caso contrário, será convertido em Sim lógico.</p> </td> 
  </tr> 
  <tr> 
   <td>booleano </td> 
   <td>outro </td> 
   <td> <p>O valor é convertido em Sim lógico sempre que o valor recebido existe (não é nulo).</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>buffer </td> 
   <td> <p>O valor é entregue inalterado somente se a página de código for a esperada. Se a página de código for diferente, o Workfront Fusion tentará converter o valor recebido na página de código solicitada. Se essa conversão não for suportada, o Workfront Fusion retornará um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>booleano </td> 
   <td> <p>O valor é convertido em texto (true/false) e em dados binários seguindo as etapas mencionadas acima para a conversão em texto.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>data </td> 
   <td> <p>O valor é convertido em texto ISO 8601 e em dados binários seguindo as etapas mencionadas para a conversão em texto.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>número </td> 
   <td> <p>O valor é convertido em texto e, em seguida, em dados binários seguindo as etapas mencionadas acima para converter em texto.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>texto </td> 
   <td> <p>O valor é convertido em dados binários e codificado conforme esperado. Se a codificação esperada não for especificada, a codificação utf8 será usada.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>outro </td> 
   <td> <p>O Workfront Fusion retorna um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>coleção </td> 
   <td>coleção </td> 
   <td> <p>O valor é entregue inalterado.</p> </td> 
  </tr> 
  <tr> 
   <td>coleção </td> 
   <td>outro </td> 
   <td> <p>O Workfront Fusion retorna um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>data </td> 
   <td>data </td> 
   <td> <p>O valor é entregue inalterado.</p> </td> 
  </tr> 
  <tr> 
   <td>data </td> 
   <td>texto </td> 
   <td> <p>O Workfront Fusion tentará converter o texto em uma data. Se a conversão falhar, retornará um erro de validação. A data deve conter dia, mês e ano. A data pode conter a hora e o fuso horário. O fuso horário padrão é baseado em suas configurações. Exemplos:</p> <p><code>2016-06-20T17:26:44.356Z</code> </p> <p><code>2016-06-20 19:26:44 GMT+02:00</code> </p> <p><code>2016-06-20 19:26+0200</code> </p> <p><code>2016-06-20 17:26:44</code> </p> <p><code>2016-06-20</code> </p> <p><code>2016/06/20 17:26:44</code> </p> <p><code>2016/06/20 19:26:44+02:00</code> </p> <p><code>2016/06/20 17:26</code> </p> <p><code>2016/06/20 5:26 PM</code> </p> <p><code>2016/06/20</code> </p> <p><code>06/20/2016 17:26:44</code> </p> <p><code>06/20/2016 19:26:44+02:00</code> </p> <p><code>06/20/2016 17:26</code> </p> <p><code>06/20/2016 5:26 PM</code> </p> <p><code>06/20/2016</code> </p> <p><code>20.6.2016 17:26:44</code> </p> <p><code>20.6.2016 19:26:44+02:00</code> </p> <p><code>20.6.2016 17:26</code> </p> <p><code>20.6.2016</code> </p> </td> 
  </tr> 
  <tr> 
   <td>data </td> 
   <td>outro </td> 
   <td> <p>O Workfront Fusion retorna um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>número </td> 
   <td>número </td> 
   <td> <p>O valor é entregue inalterado.</p> </td> 
  </tr> 
  <tr> 
   <td>número </td> 
   <td>texto </td> 
   <td> <p>O Workfront Fusion tentará converter o texto em um número. Se a conversão falhar, retornará um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>número </td> 
   <td>outro </td> 
   <td> <p>O Workfront Fusion retorna um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>texto </td> 
   <td>texto </td> 
   <td> <p>O valor é entregue inalterado.</p> </td> 
  </tr> 
  <tr> 
   <td>texto </td> 
   <td>matriz </td> 
   <td> <p>Se a matriz fornecida suportar conversão para texto, o valor será convertido. Caso contrário, o Workfront Fusion retornará um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>texto </td> 
   <td>booleano </td> 
   <td> <p>O valor é convertido em texto (true/false).</p> </td> 
  </tr> 
  <tr> 
   <td>texto </td> 
   <td>buffer </td> 
   <td> <p>Se a codificação de texto for especificada para dados binários, o valor será convertido em texto. Caso contrário, o Workfront Fusion retornará um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>texto </td> 
   <td>data </td> 
   <td> <p>O valor é convertido em texto ISO 8601.</p> </td> 
  </tr> 
  <tr> 
   <td>texto </td> 
   <td>número </td> 
   <td> <p>O valor é convertido em texto.</p> </td> 
  </tr> 
  <tr> 
   <td>texto </td> 
   <td>outro </td> 
   <td> <p>O Workfront Fusion retorna um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>hora </td> 
   <td>hora </td> 
   <td> <p>O valor é entregue inalterado.</p> </td> 
  </tr> 
  <tr> 
   <td>hora </td> 
   <td>texto </td> 
   <td> <p>O Workfront Fusion tentará converter o tempo para o formato <code>hours:minutes:seconds</code>. Se a conversão falhar, retornará um erro de validação.</p> </td> 
  </tr> 
  <tr> 
   <td>hora </td> 
   <td>outro </td> 
   <td> <p>O Workfront Fusion retorna um erro de validação.</p> </td> 
  </tr> 
 </tbody> 
</table>
