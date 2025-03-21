---
title: Módulos do Slack
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Slack, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: e52af924094722b0d212098ae2af5eded12a5309
workflow-type: tm+mt
source-wordcount: '1864'
ht-degree: 0%

---

# [!DNL Slack] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Slack], bem como conectá-los a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
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
   <p>Herdados: Automação e integração do Workfront Fusion for Work </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
   <td role="rowheader">URL base</td> 
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
* [Conversas](#channels)
* [Outro](#other)

### Mensagens

* [Criar uma mensagem](#create-a-message)
* [Excluir uma mensagem](#delete-a-message)
* [Obter uma mensagem de canal privado](#get-a-private-channel-message)
* [Obter uma mensagem de canal público](#get-a-public-channel-message)
* [Atualizar uma mensagem](#update-a-message)
* [Assistir Mensagens Do Canal Privado](#watch-private-channel-messages)
* [Assistir Mensagens Do Canal Público](#watch-public-channel-messages)

### [!UICONTROL Criar uma Mensagem]

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
   <td role="rowheader">[!UICONTROL Como usuário]</td> 
   <td>Ative essa opção para publicar a mensagem como o usuário proprietário das credenciais usadas pela conexão para esse módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de mensagem de thread (carimbo de data/hora)]</td> 
   <td>Se a nova mensagem for uma resposta, digite o carimbo de data e hora da mensagem à qual deseja responder. Não insira o carimbo de data e hora de uma mensagem que já é uma resposta.</td> 
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
   <td role="rowheader">[!UICONTROL Anexos]</td> 
   <td>Para cada item que você deseja anexar à mensagem, clique em <b>Adicionar item</b> e preencha os detalhes do item.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ícone emoji]</td> 
   <td>Insira ou mapeie o emoji a ser usado como ícone para esta mensagem, no formato <code>:icon-name:</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ícone URL]</td> 
   <td>Insira ou mapeie o URL da imagem a ser usada como o ícone desta mensagem. </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Nome de Usuário]</td> 
   <td>Especifique o nome de usuário usado para publicar a mensagem. Se nenhum nome de usuário for especificado, o nome "Bot" será usado.</td> 
  </tr> 
 </tbody> 
</table>

<!--Becky start here-->


#### [!UICONTROL Excluir uma Mensagem]

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
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem que deseja excluir.</p> <p>Observação: o carimbo de data e hora pode ser recuperado usando outro módulo, como o Módulo Watch Private Channel.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma Mensagem de Canal Privado]

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
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira (mapeie) a ID do canal.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID da Mensagem (Carimbo de data/hora)]</p> </td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem sobre a qual deseja recuperar informações.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma Mensagem de Canal Público]**

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
   <td> <p>Insira ou mapeie a ID do canal.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem (Carimbo de data/hora)]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem sobre a qual deseja recuperar informações.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar uma Mensagem]

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

### [!UICONTROL Assistir Mensagens de Canal Privado]

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
   <td> <p>Defina o número máximo de mensagens que [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assistir a Mensagens de Canal Público]

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
   <td> <p>Defina o número máximo de mensagens que [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Conversas

* [Obter um canal](#get-a-channel)
* [Listar canais](#list-channels)
* [Membros da lista no canal](#list-members-in-channel)

#### [!UICONTROL Obter um Canal]

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

#### [!UICONTROL Listar Canais]

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
   <td> <p>Defina o número máximo de canais que [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Listar membros no canal]

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
   <td>Selecione o tipo de canal que contém a lista de membros que você deseja listar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Público] / [!UICONTROL Canal Privado]</td> 
   <td>Selecione o canal do qual deseja listar membros.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Defina o número máximo de membros que [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Outro

#### [!UICONTROL Fazer uma chamada de API]

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
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
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

## Terminologia

A terminologia a seguir pode ser útil ao configurar módulos [!DNL Slack]:

* **DM**: [!UICONTROL Mensagem direta]
* **IM**: [!UICONTROL Mensagem Instantânea]
* **Canal Privado**: anteriormente [!UICONTROL Grupo]
* **Mensagem direta**: anteriormente [!UICONTROL IM]
* **Canal**: [!UICONTROL Conversa] na documentação da API, [!UICONTROL canal] no aplicativo [!DNL Slack].
