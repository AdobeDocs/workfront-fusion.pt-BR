---
title: Usar trilha dinâmica para revisar uma execução de cenário
description: O Live Trail mostra um cenário de execução à medida que ocorre, combinando solicitações de módulo e atividade de execução em uma lista. Você pode abrir os detalhes da solicitação e da resposta para qualquer operação.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 17%
---

# Usar trilha dinâmica para revisar uma execução de cenário

A Trilha ao vivo mostra um cenário que é executado à medida que ocorre. Ele combina solicitações de módulo e atividade de execução em uma lista cronológica, para que você possa seguir uma execução no editor de cenários e ver o que deu errado sem sair da tela.

>[!NOTE]
>
>Essa funcionalidade está disponível somente na nova experiência do editor de cenários. Para obter mais informações, consulte [Experiências novas e clássicas](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) no artigo Editor de cenários.

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
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Abrir trilha ao vivo

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário que deseja revisar.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Inicie uma execução do cenário, por exemplo, clicando em **Executar uma vez**.



O Live Trail é aberto no painel no lado direito da tela. Se fechar o painel durante uma execução, uma pequena guia à direita da tela permitirá abri-lo novamente sem perder os eventos capturados.

## Revisar eventos na trilha ao vivo

A Trilha dinâmica lista as solicitações do módulo e a atividade de execução na ordem em que ocorrem. É possível:

* Pesquise na lista.
* Filtrar a lista por status.
* Siga o evento mais recente enquanto a execução continua.
* Limpar a trilha atual.

## Exibir detalhes da solicitação e da resposta

1. No Live Trail, clique na solicitação para a qual deseja exibir detalhes.

   O módulo que fez a solicitação é revelado na tela e os detalhes da solicitação e da resposta são abertos no painel.

1. Revise os detalhes. A visualização detalhada inclui:

   * Navegação entre as operações do módulo
   * Cabeçalhos e corpo da solicitação
   * Cabeçalhos e corpo da resposta

1. (Opcional) Copie os detalhes para usá-los em outro lugar clicando em **Copiar bruto** ou **Copiar cURL**:

   * Copie um relatório bruto da solicitação e da resposta.
   * Copie um comando cURL para a solicitação.

1. Para retornar à lista, clique na seta para trás na parte superior esquerda do painel.

## Verifique se os detalhes da solicitação e da resposta estão disponíveis

Os detalhes da solicitação e da resposta não são mantidos para cada execução programada ou acionada, pois ocupam muito espaço de armazenamento.

* Executar uma vez sempre mantém os detalhes da solicitação e da resposta.
* Para execuções regulares de um cenário, ative Logs de depuração temporários nas configurações do cenário antes das execuções que deseja inspecionar. Para obter mais informações, consulte [Logs de depuração temporários](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs) no artigo Definir configurações de cenário.

Se você abrir uma execução do histórico de execução e o painel solicitação e resposta não tiver dados, o painel direcionará você para a configuração Registros de depuração temporários.
