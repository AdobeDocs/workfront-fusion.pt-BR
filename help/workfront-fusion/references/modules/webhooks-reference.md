---
title: Acionadores instantâneos (webhooks)
description: Muitos serviços fornecem webhooks para fornecer notificações instantâneas sempre que uma determinada alteração ocorrer no serviço. Para processar essas notificações, recomendamos que você use acionadores instantâneos. Este artigo descreve o uso e a funcionalidade de acionadores instantâneos no Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 5bfda2b2-dc1c-4ff6-9236-b480bfda2e58
source-git-commit: 45efeecd1758e302f57498bab842594800a84c1d
workflow-type: tm+mt
source-wordcount: '1272'
ht-degree: 10%

---

# Acionadores instantâneos (webhooks)

Muitos serviços fornecem webhooks para fornecer notificações instantâneas sempre que determinada alteração (evento) ocorrer no serviço. Para processar esses eventos, recomendamos que você use acionadores instantâneos. Os disparadores instantâneos exibem a marca `Instant` na lista de módulos de um determinado conector.

![Instantâneo](assets/instant.png)

>[!TIP]
>
>Você pode verificar a lista de módulos em um conector para ver se ele tem um acionador instantâneo ou pode verificar essa documentação do conector em [Aplicativos Fusion e suas referências de módulos](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
>
>Para obter a documentação do acionador instantâneo do Adobe Workfront, consulte [Acionadores](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#triggers) no artigo Módulos do Workfront.

Se um conector não incluir um webhook, você poderá executar um dos seguintes procedimentos:

* Crie um webhook personalizado usando o módulo Webhook.
Para obter mais informações, consulte [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).
* Use acionadores de pesquisa para pesquisar o serviço periodicamente.
Para obter mais informações, consulte [Agendar um cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)

Para obter uma introdução em vídeo a webhooks no Workfront Fusion, consulte:

* [Introdução aos Webhooks](https://video.tv.adobe.com/v/3427025/){target=_blank}
* [Webhooks intermediários](https://video.tv.adobe.com/v/3427030/){target=_blank}

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

## Exibir detalhes do webhook

É possível exibir uma lista de webhooks na área Webhooks.

1. Para abrir a área Webhooks, clique no ícone Webhooks ![Webhooks](assets/webhooks-icon.png) na navegação à esquerda.

   Aqui você pode ver uma lista de webhooks.

   ![Lista de Webhook](assets/list-of-webhooks.png)

1. Para procurar um webhook específico, digite o termo de pesquisa na caixa Pesquisar.
1. Para copiar um webhook, clique no ícone Copiar ![ícone de webhook Copiar](assets/copy-webhook-icon.png) próximo à URL na linha desse webhook.
1. Para definir a prioridade de um webhook, clique na lista suspensa na coluna Prioridade e selecione a nova prioridade.

   Webhooks com maior prioridade serão tratados primeiro, o que pode ser benéfico se um pool de trabalhadores tiver muitas automações competindo por recursos.
1. Para desativar ou ativar um webhook, desative ou ative a alternância na coluna Status na linha desse webhook.
1. Para ver se uma fila de webhooks está cheia, verifique a coluna Fila cheia. O número nesta coluna é o número de itens atualmente na fila.
1. Para exibir operações tratadas por um webhook, clique em **Operações** na coluna Fila Completa desse webhook.
1. Para ver se um webhook expirou, verifique a coluna Expirado. Os webhooks expirados não são anexados a nenhum cenário ou não receberam nenhum evento por 120 horas.
1. Para exibir o cenário em que um webhook é usado, clique no botão **Cenário** na coluna Cenário desse webhook.
1. Para exibir a conexão usada para este webhook, clique no botão **Conexão** na coluna Conexão para esse webhook.
1. Para ocultar colunas ou mostrar colunas ocultas anteriormente, clique no ícone **Colunas** ícone ![Colunas](assets/glist-column.png) e marque ou desmarque nomes de colunas.
1. Para exibir assinaturas de evento associadas a um webhook do Workfront, marque a caixa ao lado do webhook e selecione **Mostrar Detalhes** na parte inferior da página.

   >[!NOTE]
   >
   > Os detalhes de assinatura do evento estão disponíveis somente para webhooks do Workfront criados no novo conector do Workfront. Os detalhes do Webhook não estão disponíveis no momento para outros conectores.


## Agendar acionadores instantâneos

Ao configurar um acionador instantâneo, você será solicitado a selecionar quando ele for executado.

![Configuração de agendamento](assets/schedule-setting.png)

Selecione `Immediately` para executar o cenário imediatamente quando o Workfront Fusion receber novos eventos do serviço. Esses eventos são enviados imediatamente para uma fila e processados no cenário, um de cada vez, na mesma ordem em que os dados são recebidos.

Quando o cenário é executado, a quantidade total de eventos pendentes em espera na fila é contada e o cenário executa quantos ciclos houver de eventos pendentes, processando um evento por ciclo.

Para obter mais informações sobre ciclos, consulte [Execução do cenário, ciclos e fases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

>[!NOTE]
>
>* Um ciclo não é o mesmo que uma execução de cenário. Pode haver vários ciclos em uma execução de cenário.
>* Quando você executa um cenário com um gatilho instantâneo agendado para execução `Immediately`, as seguintes exceções se aplicam:
>
>     * O intervalo entre duas execuções não está sujeito ao intervalo mínimo de acordo com o plano de precificação.
>
>       Por exemplo, uma vez concluída a execução do cenário, a fila do webhook será verificada novamente. Se houver webhooks pendentes, o cenário será executado imediatamente novamente e todos os webhooks pendentes serão processados novamente.
>   
>     * A configuração de cenário Número máximo de ciclos é ignorada e definida como 100, o que significa que não mais de 100 webhooks pendentes serão processados durante uma única execução de cenário (na taxa de 1 evento por ciclo).
>


Se você usar qualquer outra configuração de agendamento que não [!UICONTROL Imediatamente], o cenário será executado nos intervalos especificados. Como vários webhooks podem ser coletados na fila durante o intervalo, recomendamos definir a opção [!UICONTROL Número máximo de ciclos] com um valor maior que o padrão 1 para processar mais webhooks em uma execução de cenário:

1. Clique no ícone [!UICONTROL Configurações de cenário] ícone ![Configurações de cenário](assets/scenario-settings-icon.png) na parte inferior do cenário.
1. No painel **[!UICONTROL Configurações de cenário]** exibido, insira um número no campo **[!UICONTROL Número máximo de ciclos]** para indicar o número de eventos da fila que você deseja executar sempre que executar o cenário.

Os eventos restantes na fila serão processados na próxima vez que o cenário for executado, até o número definido no campo Número máximo de ciclos.

## Medidas de proteção de Webhook

Para garantir um bom desempenho, o Workfront Fusion tem as seguintes medidas de proteção em vigor para webhooks.

### Limites de taxa

O limite de taxa atual é de 5 webhooks por segundo. Se o limite for excedido, um código de status `429` será retornado.

### Expiração de webhooks inativos

Um webhook que não foi atribuído a nenhum cenário por mais de 120 horas é removido.

### Cargas do Webhook

O Workfront Fusion armazena conteúdo do webhook por 30 dias. Acessar uma carga de webhook mais de 30 dias após sua criação resulta no erro [!UICONTROL `Failed to read file from storage.`]

### Tratamento de erros

Quando há um erro no seu cenário com um acionador instantâneo, o cenário:

* Para imediatamente quando o cenário está definido para execução [!UICONTROL Imediatamente].
* Interrompe após 3 tentativas malsucedidas (3 erros) quando o cenário está definido para ser executado como programado.

Se ocorrer um erro durante a execução do cenário, o evento será colocado de volta na fila durante a fase de reversão do acionador instantâneo. Nessa situação, você pode corrigir o cenário e executá-lo novamente.

Para obter mais informações, consulte [Reversão](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) no artigo Execução de cenário, ciclos e fases.

Se houver um módulo de resposta do Webhook em seu cenário, o erro será enviado para a resposta do Webhook. O módulo de resposta do Webhook é sempre executado por último (quando a opção [!UICONTROL Confirmação automática] nas configurações de Cenário não está habilitada).

Para obter mais informações, consulte [Responding to webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md#responding-to-webhooks) no artigo Webhooks.

### Desativação do Webhook

Os webhooks são desativados automaticamente se qualquer uma das seguintes situações se aplicar:

* O webhook não foi conectado a nenhum cenário por mais de 5 dias.
* O webhook é usado somente em cenários inativos, que ficaram assim por mais de 30 dias.

Os webhooks desativados são excluídos e não registrados automaticamente se não estiverem conectados a nenhum cenário e estiverem com o status desativado por mais de 30 dias.

## Webhooks personalizados

Você pode criar seus próprios webhooks. Para obter mais informações, consulte [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

## Recursos

Para obter mais informações sobre ciclos, consulte [Execução do cenário, ciclos e fases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).
