---
title: Módulos do Slack
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Slack, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: bb1cd0c54ae2c81c601d463cdc281d6ae7b8c434
workflow-type: tm+mt
source-wordcount: '4560'
ht-degree: 0%

---

# [!DNL Slack] módulos

>[!IMPORTANT]
>
>Este artigo descreve os módulos disponíveis no novo conector do Slack, lançado em 14 de novembro de 2025.
>
>Para obter informações sobre o conector herdado do Slack, consulte [[!DNL Slack] módulos (herdados)](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/slack-modules.md).

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Slack], bem como conectá-los a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!DNL Slack], você deve ter uma conta [!DNL Slack].

## Informações da API do Slack

O conector do Slack usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td>{{ifempty(parameters.domain, 'https://slack.com/api/')}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack] módulos e seus campos

Ao configurar módulos do [!DNL Slack], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Slack] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Mensagens](#messages)
* [Arquivos](#files)
* [Canais](#channels)
* [Reações](#reactions)
* [Estrelas](#stars)
* [Itens salvos](#saved-items)
* [Pins](#pins)
* [Usuários](#users)
* [Lembretes](#reminders)
* [Eventos](#events)
* [Perfil](#profile)
* [Outras](#other)

### Mensagens

+++ **[!UICONTROL Criar uma Mensagem]**

Este módulo de ação cria uma nova mensagem.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserir ID ou nome de canal]</p> </td> 
   <td> <p>Escolha como deseja selecionar o canal no qual deseja criar uma mensagem.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Canal ou nome]</strong>, insira ou mapeie a ID do Canal ou o nome do canal em que deseja postar a mensagem.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o tipo de canal e, em seguida, selecione o canal.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Texto]</p> </td> 
   <td> <p>Insira o conteúdo do texto da mensagem que deseja criar.</p> <p>Observação: para obter informações detalhadas sobre a formatação de texto, consulte <a href="https://api.slack.com/reference/surfaces/formatting">Formatação de texto para superfícies do aplicativo</a> na documentação de [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blocos]</td> 
   <td>Os blocos são componentes reutilizáveis que podem ser usados para personalizar e organizar suas mensagens. Para obter mais informações sobre blocos, consulte <a href="https://api.slack.com/block-kit">Kit de Bloqueios</a> na documentação do [!DNL Slack].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem de Thread (carimbo de data/hora)]</td> 
   <td>Se a nova mensagem for uma resposta, digite o carimbo de data e hora da mensagem à qual deseja responder. Não insira o carimbo de data e hora de uma mensagem que já seja uma resposta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Difusão de resposta]</td> 
   <td> <p>Selecione <strong>[!UICONTROL Sim]</strong> se ambas as condições a seguir se aplicarem:</p> 
    <ul> 
     <li> <p>A nova mensagem é uma resposta para outra mensagem</p> </li> 
     <li> <p>Você deseja que a nova mensagem seja visível para todos no canal</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nomes de links]</p> </td> 
   <td> <p>Habilite esta opção para permitir que nomes e canais usem o formato <code>@username</code> ou <code>#channel</code>. </p> <p>Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies do aplicativo</a> na documentação de [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Analisar texto da mensagem]</p> </td> 
   <td> <p>Ative esta opção para permitir a análise automática. </p> <p>Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies do aplicativo</a> na documentação de [!DNL Slack].</p> <p>Observação: se você usou as opções [!UICONTROL Link names] ou [!UICONTROL Parse message text] na mensagem original, deverá especificá-las ao executar o módulo [!UICONTROL Update a Message] também.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Usar markdown]</p> </td> 
   <td> <p>Habilite esta opção para permitir que [!DNL Slack] use a marcação no texto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Desfazer conteúdo baseado principalmente em texto]</p> </td> 
   <td> <p>Habilite essa opção para permitir o descarregamento de conteúdo baseado principalmente em texto. </p> <p>Para obter mais informações sobre descarregamento em [!DNL Slack], consulte <a href="https://api.slack.com/reference/messaging/link-unfurling">Descarregamento de links em mensagens</a> na documentação [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Desfazer carregamento de conteúdo de mídia]</p> </td> 
   <td> <p>Ative essa opção para permitir o descarregamento do conteúdo de mídia. </p> <p>Para obter mais informações sobre descarregamento em [!DNL Slack], consulte <a href="https://api.slack.com/reference/messaging/link-unfurling">Descarregamento de links em mensagens</a> na documentação [!DNL Slack].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Excluir uma Mensagem]**

Este módulo de ação exclui uma mensagem especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira ou mapeie a ID do canal.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Mensagem (carimbo de data/hora)]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem que deseja excluir.</p> <p>Observação: O carimbo de data e hora pode ser recuperado usando outro módulo, como o Watch Private Channel Module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obter uma Mensagem de Canal Privado]**

Este módulo de ação recupera os detalhes de uma mensagem de um canal selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Canal]</p> </td> 
   <td> <p>Selecione o canal que contém a mensagem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID da Mensagem (Carimbo de data/hora)]</p> </td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem sobre a qual deseja recuperar informações.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obter uma Mensagem de Canal Público]**

Este módulo de ação retorna uma mensagem com uma determinada ID de um canal público especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Selecione o canal que contém a mensagem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem (Carimbo de data/hora)]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem sobre a qual deseja recuperar informações.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar respostas]**

Este módulo de ação recupera um thread de mensagens postadas em uma conversa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal que contém a mensagem para a qual deseja recuperar respostas e selecione o canal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da mensagem pai (carimbo de data/hora)]</td> 
   <td> <p> Informe ou mapeie o timestamp da mensagem para a qual você deseja recuperar respostas.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de respostas que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Procurar Mensagem]**

Este módulo de pesquisa retorna mensagens correspondentes a uma consulta de pesquisa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Consulta]</td> 
   <td> <p>Informe a consulta pela qual deseja pesquisar. </p> <p>Para obter informações sobre como criar fórmulas no painel de mapeamento, consulte <a href="/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md" class="MCXref xref">Mapear itens usando funções em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira o número máximo de registros que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classificar por] </td> 
   <td> <p>Selecione se deseja classificar as mensagens retornadas por sua pontuação ou carimbo de data e hora.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Selecione se deseja classificar mensagens em ordem crescente ou decrescente.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Atualizar uma Mensagem]**

Este módulo de ação permite editar uma mensagem existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserir ID ou nome de canal]</p> </td> 
   <td> <p>Escolha como você deseja selecionar a mensagem.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Canal ou nome]</strong>, digite ou mapeie a ID do Canal ou do canal que contém a mensagem e, em seguida, digite o <strong>[!UICONTROL Carimbo de Data/Hora (ID da Mensagem)]</strong> da mensagem. .</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione o tipo de canal, o canal e a mensagem.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Texto]</p> </td> 
   <td> <p>Insira o novo conteúdo de texto da mensagem que deseja atualizar.</p> <p>Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies do aplicativo</a> na documentação de [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blocos]</td> 
   <td>Os blocos são componentes reutilizáveis que podem ser usados para personalizar e organizar suas mensagens. Para obter mais informações sobre blocos, consulte <a href="https://api.slack.com/block-kit">Kit de Bloqueios</a> na documentação do [!DNL Slack].</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nomes de links]</p> </td> 
   <td> <p>Habilite esta opção para permitir que nomes e canais usem o formato <code>@username</code> ou <code>#channel</code>. </p> <p>Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies do aplicativo</a> na documentação de [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Analisar texto da mensagem]</p> </td> 
   <td> <p>Ative esta opção para permitir a análise automática. </p> <p> Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies do aplicativo</a> na documentação de [!DNL Slack].</p> <p>Observação: se você usou as opções [!UICONTROL Link names] ou [!UICONTROL Parse message text] na mensagem original, você também deve especificá-las ao executar o módulo Atualizar uma Mensagem.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assistir Mensagens Diretas]**

Esse módulo de acionamento inicia o cenário quando uma nova mensagem é adicionada a uma mensagem direta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canal] </td> 
   <td> <p>Selecione a conversa de mensagem direta que deseja assistir para novas mensagens.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira o número máximo de mensagens que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assistir a Mensagens Diretas de Vários Participantes]**

Esse módulo de acionamento inicia o cenário quando uma nova mensagem é adicionada a um canal de mensagem direta multiparte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canal] </td> 
   <td> <p>Selecione a conversa de mensagem direta que deseja assistir para novas mensagens.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira o número máximo de mensagens que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Assistir Mensagens de Canal Privado]**

Esse módulo de acionamento inicia o cenário quando uma nova mensagem é adicionada a um canal privado (grupo).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canal] </td> 
   <td> <p>Selecione o canal privado que deseja observar para novas mensagens.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira o número máximo de mensagens que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Assistir a Mensagens de Canal Público]**

Esse módulo de acionamento inicia o cenário quando uma nova mensagem é adicionada a um canal público.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canal] </td> 
   <td> <p>Selecione o canal público que deseja assistir para novas mensagens.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira o número máximo de mensagens que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Arquivos

+++ **[!UICONTROL Excluir um arquivo]**

Este módulo de ação retorna a exclusão do arquivo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td> <p>Insira ou mapeie a ID do arquivo que deseja excluir. </p> <p>Observação: a ID do arquivo pode ser recuperada usando outro módulo, como o Módulo [!DNL Watch Files].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obter um Arquivo]**

Este módulo de ação retorna detalhes sobre o arquivo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td> <p>Insira ou mapeie a ID do arquivo que você deseja recuperar. </p> <p>Observação: a ID do arquivo pode ser recuperada usando outro módulo, como o Módulo [!DNL Watch Files].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar Arquivos]**

Este módulo de ação retorna uma lista de arquivos com base no filtro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo] </td> 
   <td> <p>Selecione os tipos de arquivos que deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo de canal]</p> </td> 
   <td> <p>Selecione o tipo de canal que representa o canal do qual deseja listar arquivos e selecione o canal.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criado por]</td> 
   <td> <p>Selecione um usuário para retornar somente os arquivos criados pelo usuário especificado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data de]</td> 
   <td>Insira a data a partir da qual você deseja retornar os arquivos. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data para]</td> 
   <td>Insira a última data a partir da qual você deseja retornar os arquivos. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Download a File]**

This action module downloads a file from a URL. It must follow the [!UICONTROL Slack] >[!UICONTROL Get a File] module in a scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL private download]</td> 
   <td> <p>Map the <b>[!UICONTROL URL Private download]</b> value from the [!DNL Slack] >[!UICONTROL Get a File] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL Carregar um arquivo]**

Este módulo de ação cria ou carrega um arquivo para [!DNL Slack]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canais]</td> 
   <td> <p>Para cada canal para o qual você deseja carregar o arquivo, clique em <b>[!UICONTROL Adicionar item]</b> e selecione o tipo de canal e o canal.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Título]</td> 
   <td>Insira um título para o arquivo que você deseja fazer upload</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Thread (carimbo de data/hora)]</td> 
   <td> <p>Se você estiver fazendo upload do arquivo como uma resposta, digite ou mapeie o carimbo de data e hora da mensagem à qual deseja responder.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comentário Inicial]</td> 
   <td> <p>Insira ou mapeie o texto da mensagem que introduz o arquivo.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Observar arquivos]**

Este módulo de acionamento inicia um cenário quando um novo arquivo é adicionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td>Selecione o tipo de arquivo que o módulo deverá observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td> <p>Selecione o tipo de canal que deseja observar por arquivos e selecione o canal.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criado por]</td> 
   <td> <p>Selecione um usuário para retornar somente os arquivos criados pelo usuário especificado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira ou mapeie o número máximo de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Canais

+++ **[!UICONTROL Arquivar um Canal]**

Este módulo de ação arquiva um canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira ou mapeie a ID do canal que deseja arquivar.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar um canal]**

Este módulo de ação cria um novo canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nome]</p> </td> 
   <td> <p>Insira ou mapeie um nome para o novo canal.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL É particular]</td> 
   <td>Habilite esta opção para definir o novo canal como privado.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obter um Canal]**

Este módulo de ação retorna informações sobre um canal do espaço de trabalho.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira ou mapeie a ID do canal sobre o qual deseja recuperar informações.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ingressar em um Canal]**

Este módulo de ação une o usuário a um canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira ou mapeie a ID do canal no qual você deseja ingressar.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Sair de um canal]**

Este módulo de ação remove o usuário de um canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira ou mapeie a ID do canal que você deseja deixar.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar Canais]**

Este módulo de pesquisa retorna uma lista de todos os canais em um espaço de trabalho.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Excluir arquivado]</p> </td> 
   <td> <p>Selecione [!UICONTROL Yes] para excluir canais arquivados nos resultados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo] </td> 
   <td> <p>Selecione os tipos de canais que deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Defina o número máximo de canais que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar membros no canal]**

Este módulo de pesquisa retorna uma lista de usuários no canal selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal que contém os membros que você deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Canal Privado]</td> 
   <td>Selecione o canal do qual deseja listar membros.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Defina o número máximo de membros que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Definir a Finalidade de um Canal]**

Este módulo de ação altera a finalidade de um canal

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal para o qual você deseja alterar a finalidade.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Privado] / Usuário / [!UICONTROL Vários Canais de IM]</td> 
   <td>Selecione o canal ou usuário para o qual deseja alterar a finalidade.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Finalidade]</td> 
   <td>Insira ou mapeie a nova finalidade do canal. Este campo não oferece suporte a formatação ou links.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Definir o Tópico de um Canal]**

Este módulo de ação altera o tópico de um canal

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal para o qual deseja alterar o tópico.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Privado] / [!UICONTROL Usuário] / [!UICONTROL Vários Canais de IM]</td> 
   <td>Selecione o canal ou usuário para o qual deseja alterar o tópico.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tópico]</td> 
   <td>Insira ou mapeie o novo tópico do canal. Este campo não oferece suporte a formatação ou links.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Desarquivar um Canal]**

Este módulo de ação desarquiva um canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira ou mapeie a ID do canal que você deseja desarquivar.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Reações

+++ **[!UICONTROL Adicionar uma reação]**

Este módulo de ação adiciona uma reação a um item.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal ao qual deseja adicionar uma reação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Privado] / [!UICONTROL Usuário] / [!UICONTROL Vários canais de IM]</td> 
   <td>Selecione o canal ou usuário ao qual deseja adicionar uma reação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Mensagem (carimbo de data/hora)]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem à qual deseja adicionar uma reação.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reação (emoji) name]</td> 
   <td>Insira ou mapeie o nome do emoji que deseja usar para uma reação. Exemplo: <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar reações]**

Esse módulo de ação retorna as reações que um usuário fez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Usuário]</p> </td> 
   <td> <p>Selecione o usuário que fez as reações que deseja listar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de reações que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Remover uma reação]**

Este módulo de ação remove uma reação de um item.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal do qual deseja remover uma reação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Privado] / [!UICONTROL Usuário] / [!UICONTROL Vários canais de IM]</td> 
   <td>Selecione o canal ou usuário do qual deseja remover uma reação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem da qual deseja remover uma reação.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reação (emoji) name]</td> 
   <td>Insira ou mapeie o nome do emoji que deseja remover da mensagem. Exemplo: <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

### Estrelas

+++ **[!UICONTROL Adicionar uma estrela]**

Este módulo de ação faz de um canal um canal estrelado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal ao qual deseja adicionar uma estrela.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Privado] / [!UICONTROL Usuário] / [!UICONTROL Vários canais de IM]</td> 
   <td>Selecione o canal ou usuário ao qual deseja adicionar uma estrela.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Remover uma estrela]**

Este módulo de ação remove a estrela de um canal com estrelas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal ao qual deseja adicionar uma estrela.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Privado] / [!UICONTROL Usuário] / [!UICONTROL Vários canais de IM]</td> 
   <td>Selecione o canal ou usuário ao qual deseja adicionar uma estrela.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Itens salvos

+++ **[!UICONTROL Remover Item Salvo]**

Este módulo de ação remove um item dos itens salvos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem (Carimbo de data/hora)]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem que deseja remover dos itens salvos.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td> <p>Insira ou mapeie o arquivo que deseja remover dos itens salvos.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Salvar um item]**

Este módulo de ação adiciona um item aos itens salvos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem (Carimbo de data/hora)]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem que deseja salvar.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td> <p>Insira ou mapeie o arquivo que deseja salvar.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Pins

+++ **[!UICONTROL Fixar um Item]**

Este módulo de ação fixa um item em um canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal no qual você deseja fixar um item.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Privado] / [!UICONTROL Vários canais de IM] / [!UICONTROL Usuário]</td> 
   <td>Selecione o canal ou usuário ao qual deseja fixar um item.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem que deseja fixar.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Desafixar um Item]**

Este módulo de ação desafixa um item de um canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal do qual você deseja desafixar um item.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Privado] / [!UICONTROL Vários canais de IM] / [!UICONTROL Usuário]</td> 
   <td>Selecione o canal ou usuário do qual deseja desafixar um item.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem que deseja desafixar.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Usuários

+++ **[!UICONTROL Obter um Usuário]**

Este módulo de ação recupera detalhes sobre um membro de um espaço de trabalho.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Usuário]</p> </td> 
   <td> <p>Insira ou mapeie a ID do usuário para o qual deseja recuperar detalhes.</p> <p>Observação: a ID de Usuário pode ser recuperada usando outro módulo, como o módulo [!DNL List Users].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Convidar usuários]**

Este módulo de ação convida de 1 a 30 usuários para um canal público ou privado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal para o qual deseja convidar usuários.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Canal privado]</td> 
   <td>Selecione o canal para o qual deseja convidar usuários.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Usuários]</td> 
   <td> <p>Selecione os usuários que deseja adicionar ao canal.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Expulsar um usuário]**

Este módulo de ação remove um usuário de um canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de canal]</td> 
   <td>Selecione o tipo de canal do qual deseja remover um usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Canal privado]</td> 
   <td>Selecione o canal do qual deseja remover um usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Usuários]</td> 
   <td> <p>Selecione o usuário que deseja remover do canal.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar Usuários]**

Este módulo de ação retorna uma lista de todos os usuários em um espaço de trabalho.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limite]</p> </td> 
   <td> <p>Insira ou mapeie o número máximo de usuários que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Procurar Usuário]**

Este módulo de ação recupera detalhes sobre um único usuário, usando seu endereço de email.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email] </p> </td> 
   <td> <p>Insira ou mapeie o endereço de email do usuário sobre o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assistir Usuários]**

Este módulo de acionador inicia o cenário quando um novo usuário é adicionado ao espaço de trabalho [!DNL Slack].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Defina o número máximo de usuários que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Lembretes

<!--

+++ **[!UICONTROL List Reminders]**

This action module returns a list of all reminders created by or given to the currently authenticated user.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Enter or map the maximum number of reminders you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Reminder]**

This action module retrieves details about a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to retrieve details for.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL Criar um lembrete]**

Este módulo de ação cria um lembrete.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Texto]</td> 
   <td>Inserir ou mapear o conteúdo do lembrete</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hora]</td> 
   <td> <p>Insira ou mapeie a data e a hora em que este lembrete deve ocorrer. Insira uma das seguintes opções: </p> 
    <ul> 
     <li> <p>O carimbo de data e hora Unix (daqui a cinco anos)</p> </li> 
     <li> <p>O número de segundos até o lembrete (se em 24 horas) </p> </li> 
     <li> <p>Uma descrição em linguagem natural (Exemplos: "em 15 minutos" ou "todas as quintas-feiras")</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Usuário] </p> </td> 
   <td> <p>Selecione o usuário que recebe o lembrete.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Complete a Reminder]**

This action module completes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to complete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Reminder]**

This action module deletes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to delete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

### Eventos

+++ **[!UICONTROL Novo Evento]**

Esse acionador instantâneo inicia um cenário quando uma nova mensagem ou outro evento é criado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Selecione o webhook que deseja usar.</p> <p>Ou</p> <p>Crie um novo webhook.</p> 
    <ol> 
     <li value="1"> <p>Clique em <b>[!UICONTROL Adicionar]</b>.</p> </li> 
     <li value="2"> <p>Selecione o tipo de evento.</p> </li> 
     <li value="3"> <p>Selecione ou adicione uma conexão. Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!UICONTROL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas</a></p> </li> 
     <li value="4"> <p>Se solicitado, selecione o canal que deseja assistir.</p> </li> 
     <li value="5"> <p>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Perfil

+++ **[!UICONTROL Definir um status]**

Este módulo de ação atualiza o status atual de um usuário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Texto de status]</p> </td> 
   <td> <p>Insira ou mapeie o texto de status. Considere o seguinte:</p> 
    <ul> 
     <li> <p>É possível inserir até 100 caracteres.</p> </li> 
     <li> <p>Você pode usar marcação ou outra formatação, como menções de usuário.</p> </li> 
     <li> <p>Você pode incluir emojis no texto de status usando o formato <code>:emojiname:</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status emoji]</td> 
   <td> <p>Insira ou mapeie o emoji que deseja usar para representar seu status. Use o formato <code>:emojiname:</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expiração de status]</td> 
   <td>Insira ou mapeie a data e a hora em que deseja que o status expire. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coerção de tipo</a>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Outras

+++ **[!UICONTROL Fazer uma chamada de API]**

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Slack]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Slack].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://slack.com/api/</code>. Exemplo: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O [!UICONTROL Workfront Fusion] adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL Base]</td> 
   <td>Selecione o URL base que deseja usar para a chamada de API.</td> 
  </tr> 
 </tbody> 
</table>

+++

## Terminologia

A terminologia a seguir pode ser útil ao configurar módulos [!DNL Slack]:

* **DM**: [!UICONTROL Mensagem direta]
* **IM**: [!UICONTROL Mensagem Instantânea]
* **Canal Privado**: anteriormente [!UICONTROL Grupo]
* **Mensagem direta**: anteriormente [!UICONTROL IM]
* **Canal**: [!UICONTROL Conversa] na documentação da API, [!UICONTROL canal] no aplicativo [!DNL Slack].

