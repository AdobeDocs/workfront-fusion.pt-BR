---
content-type: reference
title: Diretivas para tratamento de erros
description: Este artigo descreve as diretivas que podem ser usadas para a manipulação de erros nos cenários do Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 32%

---

# Diretivas para tratamento de erros

As diretivas de manipulação de erros permitem escolher o que ocorre quando um cenário encontra um erro.

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
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Diretivas para tratamento de erros

As seguintes diretivas de manipulação de erros estão disponíveis no Workfront Fusion.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Reversão</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>A execução do cenário é interrompida imediatamente.</li><li>Uma fase de reversão é iniciada em todos os módulos, em uma tentativa de reverter todos para o estado inicial. </li><li>Os módulos subsequentes não são processados.</p></li><li> <p>Na maioria dos casos, o cenário é desativado após o número de erros consecutivos especificados em Configurações do cenário. Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors" class="MCXref xref">Número de erros consecutivos</a>.</p> </li><li><p>O status de execução do cenário é marcado como "Erro".</p></li></ul> <p><b>Observação</b>: este é o comportamento padrão se nenhuma rota de manipulador de erros estiver anexada ao módulo e se a opção <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions" class="MCXref xref">Permitir o armazenamento de execuções incompletas</a>Permitir o armazenamento de execuções incompletas nas [!UICONTROL Configurações de cenário] não estiver marcada.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Confirmar</p> <p> <img src="assets/commit.png"> </p> </td> 
   <td> <ul><li><p>A execução do cenário é interrompida imediatamente.</li><li>Uma fase de confirmação é iniciada em todos os módulos. </li><li>Os módulos subsequentes não são processados.</p></li><li> <p>Todos os pacotes não processados são ignorados.</p> </li><li><p>O status de execução do cenário é marcado como “sucesso”. </p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Retomar</p> <p> <img src="assets/resume.png"> </p> </td> 
   <td> <ul><li><p>Uma saída substituta é especificada e fornecida ao módulo que encontra um erro.</p> </li><li><p>Os módulos subsequentes são processados.</p></li><li> <p>O status de execução do cenário é marcado como “sucesso”.</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ignorar</p> <p> <img src="assets/ignore.png"> </p> </td> 
   <td><ul><li> <p>O erro é ignorado.</li><li> Os módulos subsequentes não são processados.</p> </li><li><p>Se houver pacotes não processados, a execução do cenário continuará normalmente.</p> </li><li><p>O status de execução do cenário é marcado como “sucesso”.</p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Interrupção</p> <p> <img src="assets/break.png"> </p> </td> 
   <td><ul><li> <p>O estado de execução do cenário é armazenado na fila de execuções incompletas, onde o erro pode ser resolvido manualmente. Para obter mais informações, consulte <a href="/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref">Exibir e resolver execuções incompletas</a>.</p> <p>Há, no entanto, algumas exceções. Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow" class="MCXref xref">Permitir o armazenamento de execuções incompletas</a> no artigo Definir configurações de cenário</a>.</p></li><li> <p>Os módulos subsequentes não são processados.</p></li><li> <p>Se houver pacotes não processados, a execução do cenário continuará normalmente.</p> </li><li><p>O status de execução do cenário é marcado como "aviso" quando a opção [!UICONTROL Concluir execução automaticamente] está desabilitada.</p></li></ul> <p>Para obter mais informações, consulte a seção <a href="#break" class="MCXref xref">[!UICONTROL Break]</a> neste artigo</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tente novamente</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>Em alguns casos, pode ser útil executar novamente um módulo com falha quando houver uma chance de o motivo da falha passar do tempo.</p> <p>Atualmente, o Workfront Fusion não oferece a diretiva Repetir, embora várias soluções alternativas possam ser empregadas para mimetizar sua funcionalidade. Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/config-error-handling/retry.md" class="MCXref xref">Repetir tratamento de erros</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* As diretivas de tratamento de erros não podem ser usadas fora de uma rota de tratamento de erros.
>* Atualmente, o Workfront Fusion não oferece um módulo de Lançamento que permitiria gerar facilmente erros condicionalmente (lançamentos), embora uma solução alternativa possa ser empregada para simular sua funcionalidade.
>
>  Para obter mais informações, consulte [Configurar a solução alternativa de erro `throw`](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md).

## Recursos

* Para obter informações sobre a reversão e a fase de reversão, consulte [Reversão](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) no artigo Execução de cenário, ciclos e fases.
* Para obter informações sobre a fase de Confirmação, consulte [Confirmar](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit) no artigo Execução de cenário, ciclos e fases.
