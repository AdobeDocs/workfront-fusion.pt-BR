---
title: Módulos do Slack
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Slack, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: eb0518ba0d1a0c758cb547e362c722f4be3674c7
workflow-type: tm+mt
source-wordcount: '1954'
ht-degree: 0%

---

# [!DNL Slack] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Slack], bem como conectá-los a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice](/help/workfront-fusion/references/modules/modules-toc.md) do artigo.

## Requisitos de acesso

+++ Expanda para visualização requisitos de acesso do funcionalidade neste artigo.

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
   <p>Novo:</p> <ul><li>Selecione ou pacote Prime Workfront: sua organização deve comprar Adobe Systems Workfront Fusion.</li><li>Pacote Ultimate Workfront: Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar Adobe Systems Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Os requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter mais informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] as licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
   <td role="rowheader">tag da API</td> 
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack] módulos e seus campos

Ao configurar [!DNL Slack] módulos, [!DNL Workfront Fusion] exibe os campos listados abaixo. Além desses, campos adicionais [!DNL Slack] podem ser exibidos, dependendo de fatores como o nível de acesso no aplicativo ou no serviço. Um título em negrito em uma módulo indica um campo obrigatório.

Se você vir o mapa botão acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [informações de mapa de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternar mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Mensagens](#messages)
* [Conversas](#channels)
* [Outro](#other)

### Mensagens

* [Criar um Enviar mensagem](#create-a-message)
* [Excluir uma mensagem](#delete-a-message)
* [Obter um canal privado Enviar mensagem](#get-a-private-channel-message)
* [Obtenha um Enviar mensagem de Canal Público](#get-a-public-channel-message)
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
   <td> <p>Insira o conteúdo do texto da mensagem que deseja criar.</p> <p>Observação: para obter informações detalhadas sobre formatação de texto, consulte <a href="https://api.slack.com/reference/surfaces/formatting">Formatação de texto para visualização</a> do aplicativo na [!DNL Slack] documentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL Como usuário]</td> 
   <td>Ative essa opção para postagem a mensagem como a usuário de propriedade das credenciais usadas pela conexão para esse módulo.</td> 
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
   <td> <p>Habilite esta opção para permitir que nomes e canais usem o formato <code>@username</code> ou <code>#channel</code>. </p> <p>Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies</a> do aplicativo na [!DNL Slack] documentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[! Texto da mensagem de análise UICONTROL]</p> </td> 
   <td> <p>Ative essa opção para permitir a análise automática. </p> <p>Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies do aplicativo</a> na documentação de [!DNL Slack].</p> <p>Observação: se você usou as opções [!UICONTROL Link names] ou [!UICONTROL Parse message text] na mensagem original, deverá especificá-las ao executar o módulo [!UICONTROL Update a Message] também.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Usar markdown]</p> </td> 
   <td> <p>Habilite esta opção para permitir que [!DNL Slack] use a marcação no texto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Desfazer conteúdo baseado principalmente em texto]</p> </td> 
   <td> <p>Ative essa opção para permitir o cancelamento de conteúdo baseados em texto principalmente. </p> <p>Para obter mais informações sobre a desenrolação [!DNL Slack], consulte <a href="https://api.slack.com/reference/messaging/link-unfurling">Cancelar links em mensagens</a> na [!DNL Slack] documentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[! Desfazer a mídia conteúdo UICONTROL]</p> </td> 
   <td> <p>Ative essa opção para permitir o cancelamento de conteúdo de mídia. </p> <p>Para obter mais informações sobre a desenrolação [!DNL Slack], consulte <a href="https://api.slack.com/reference/messaging/link-unfurling">Cancelar links em mensagens</a> na [!DNL Slack] documentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Nome de usuário UICONTROL]</td> 
   <td>Especifique o usuário nome usado para postagem a mensagem. Se não usuário nome for especificado, o nome "Bot" será usado.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Excluir uma Enviar mensagem]

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
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem que deseja excluir.</p> <p>Observação: O carimbo de data e hora pode ser recuperado usando outro módulo, como o Módulo Watch Private Channel Messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Como usuário]</td> 
   <td> <p> Habilite esta opção para excluir a mensagem como o usuário com as credenciais usadas na conexão.</p> </td> 
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
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem sobre a qual deseja recuperar informações.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Observar Mensagens de Canal Privado].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma Mensagem de Canal Público]**

Essa ação módulo retorna uma mensagem com uma determinada ID de uma canal pública especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! Conexão UICONTROL] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Slack] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira ou mapeie a ID do canal.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem (Carimbo de data/hora)]</td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem sobre a qual deseja recuperar informações.</p> <p>Observação: o carimbo de data/hora pode ser recuperado usando outro módulo, como o módulo [!UICONTROL Observar Mensagens de Canal Público].</p> </td> 
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
<!--  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the message you want to .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or of the channel that contains the message, then enter the <strong>[!UICONTROL Time Stamp (Message ID)]</strong> of the message.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel, then select the message.</p> </li> 
    </ul> </td> 
  </tr> -->
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Canal]</p> </td> 
   <td> <p>Insira ou mapeie a ID do canal que contém a mensagem que você deseja atualizar.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID da Mensagem (Carimbo de data/hora)]</p> </td> 
   <td> <p> Insira ou mapeie o carimbo de data e hora da mensagem sobre a qual deseja recuperar informações.</p> <p>Observação: o carimbo de data e hora pode ser recuperado usando outra módulo, como o [! UICONTROL Assista a mensagens de canal público] módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[! Texto UICONTROL]</p> </td> 
   <td> <p>Insira o novo texto conteúdo da mensagem que deseja atualizar.</p> <p>Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies do aplicativo</a> na documentação de [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Como usuário]</td> 
   <td>Ative essa opção para atualizar a mensagem como a usuário de propriedade das credenciais usadas pela conexão para esse módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Anexos UICONTROL]</td> 
   <td>Para cada item que você deseja anexar à mensagem, clique <b>em Adicionar item</b> e preencha os detalhes do item.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[! Nomes de links UICONTROL]</p> </td> 
   <td> <p>Ative essa opção para permitir o uso <code>@username</code> ou <code>#channel</code> o formato de nomes e canais. </p> <p>Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies</a> do aplicativo na [!DNL Slack] documentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[! Texto da mensagem de análise UICONTROL]</p> </td> 
   <td> <p>Ative essa opção para permitir a análise automática. </p> <p> Para obter mais informações, consulte <a href="https://api.slack.com/docs/formatting">Formatação de texto para superfícies</a> do aplicativo na [!DNL Slack] documentação.</p> <p>Observação: se tiver usado [! Nomes de links UICONTROL] ou [! Opções de texto da mensagem de análise UICONTROL na mensagem original, especifique-as ao executar a Enviar mensagem módulo também.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Assista a mensagens de canal privado]

Esse acionador módulo inicia o cenário quando uma nova mensagem é adicionada a uma canal privada (grupo).

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
   <td> <p>Insira ou mapeie a ID do canal com a qual deseja recuperar informações.</p> <p>Observação: a ID de canal pode ser recuperada usando o [! Canais de lista UICONTROL] módulo.</p> </td> 
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

Essa pesquisa módulo retorna uma lista de usuários no canal selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! Conexão UICONTROL] </td> 
   <td> <p>Para obter instruções sobre como conectar suas [!DNL Slack] conta, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] instruções básicas</a>[!DNL Workfront Fusion].</p> </td> 
  </tr> 
<tr> 
   <td role="rowheader"> <p>[! UICONTROL Insira uma ID ou nome de canal]</p> </td> 
   <td> <p>Escolha como deseja selecionar a mensagem desejada.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Canal ou nome]</strong>, insira ou mapeie a ID de Canal ou do canal do qual deseja listar os usuários.</p> <p>Observação: a ID de canal pode ser recuperada usando o módulo [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[! UICONTROL Selecione no lista]</strong> </p> <p>Selecione o tipo de canal e selecione o canal.</p> </li> 
    </ul> </td> 
  </tr>
  <tr> 
   <td role="rowheader">[! Limite UICONTROL] </td> 
   <td> <p>Defina o número máximo de membros [!DNL Workfront Fusion] que retornarão durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Outro

#### [!UICONTROL Fazer uma chamada de API]

Essa ação módulo permite fazer uma chamada autenticada personalizada para a [!DNL Slack] API. Dessa forma, é possível criar uma automação de fluxo de dados que não possa ser realizada pelos outros [!DNL Slack] módulos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! Conexão UICONTROL] </td> 
   <td> <p>Para obter instruções sobre como conectar suas [!DNL Slack] conta, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] instruções básicas</a>[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! URL UICONTROL]</td> 
   <td>Insira um caminho relativo a <code>https://slack.com/api/</code>. Exemplo: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! Método UICONTROL]</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada da API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">solicitação HTTP métodos</a>.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Enviar token de acesso]</td> 
   <td>Selecione se deseja enviar o token de acesso como um cabeçalho ou como um parâmetro de consulta.</td> 
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
