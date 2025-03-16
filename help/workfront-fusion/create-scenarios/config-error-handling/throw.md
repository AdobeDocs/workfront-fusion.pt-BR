---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: errors
title: Configurar solução alternativa para o erro de lançamento
description: Em alguns casos, você pode querer interromper de forma forçada a execução do cenário seguida pela fase Reverter ou Confirmar, ou interromper o processamento de uma rota e, opcionalmente, armazená-la na fila de Exibir e resolver execuções incompletas no Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 4bf2a6c7-16b2-4545-9adf-be3947a7017d
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---

# Configurar solução alternativa de erro do `throw`

Em alguns casos, você pode querer interromper de forma forçada a execução do cenário seguida da fase Reverter ou Confirmar, ou interromper o processamento de uma rota e, opcionalmente, armazená-la na fila de execuções incompletas.

Atualmente, as diretivas de manipulação de erros não podem ser usadas fora do escopo de uma rota de manipulador de erros, e o Adobe Workfront Fusion não oferece um módulo que permitiria gerar (lançar) erros condicionalmente facilmente.

Você pode usar a solução alternativa a seguir para imitar a funcionalidade de erro do `throw`.

Para obter informações sobre execuções incompletas, consulte [Exibir e resolver execuções incompletas no Adobe Workfront Fusion](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Para obter informações sobre diretivas de tratamento de erros, consulte [Diretivas para tratamento de erros em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença do Adobe Workfront</td> 
   <td> <p>Novo: Padrão</p><p>Ou</p><p>Atual: trabalho ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Atual: nenhum requisito de licença do Workfront Fusion</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecione ou Prime Workfront Plan: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Solução alternativa para `throw`

Para emitir um erro condicionalmente, você pode configurar um módulo para que ele falhe propositalmente durante sua operação. Uma possibilidade é empregar o módulo [!UICONTROL JSON] > [!UICONTROL Parse JSON], configurado para emitir opcionalmente um erro (`BundleValidationError` neste caso):

![Erro de JSON](assets/json-parse-json.png)

Em seguida, você pode anexar uma das diretivas de tratamento de erros à rota de tratamento de erros:

* **Reversão**: forçar a execução do cenário para parar e executar a fase de reversão.
* **Confirmar**: forçar a execução do cenário para parar e executar a fase de confirmação.
* **Ignorar**: parar o processamento de uma rota.
* **Intervalo**: interrompe o processamento de uma rota e armazena-a na fila da pasta de execuções incompletas.

O exemplo a seguir mostra o uso da diretiva [!DNL Rollback]:

![Diretiva de reversão](assets/rollback-directive.png)
