---
title: Módulos do Trello
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Trello, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '4256'
ht-degree: 0%

---

# [!UICONTROL Trello] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!UICONTROL Trello], bem como conectá-los a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano [!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Adobe Workfront], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Pré-requisitos

Para usar módulos [!DNL Trello], você deve ter uma conta [!UICONTROL Trello].

## Informações da API do Trello

O conector Trello usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!UICONTROL Trello] a [!DNL Workfront Fusion]

Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte [Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!UICONTROL Trello] módulos e seus campos

Ao configurar módulos do [!UICONTROL Trello], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!UICONTROL Trello] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Quadros](#boards)
* [Listas](#lists)
* [Cartões](#cards)
* [Membros](#members)
* [Listas de verificação](#checklists)
* [Rótulos](#labels)
* [Comentários](#comments)

### Quadros

+++ **[!UICONTROL Watch Boards]**

Este módulo de acionamento inicia um cenário quando uma nova placa é adicionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>O número máximo de quadros [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Board]**

Este módulo de ação cria um novo quadro com as configurações selecionadas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Informe ou mapeie um nome para o novo quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Informe ou mapeie a descrição do quadro, se necessário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Insira ou mapeie a ID da organização. A ID da organização pode ser recuperada usando outro módulo, como o módulo Atividades de observação.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/id-of-org.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>Os painéis têm regras de votação e comentário diferentes para cada nível de permissão. Por exemplo: se o seu painel for [!UICONTROL Private] e você definir as regras de votação e comentários como [!UICONTROL All], você receberá um erro. </p> <p>A votação e os comentários são limitados aos seguintes grupos para cada nível de permissão:</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      —&gt;Membros, Membros e Observadores</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      —&gt;Membros, Membros e Observadores, Membros da Organização</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      —&gt;Membros, Membros e Observadores, Membros da Organização, Todos</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Selecione uma opção para especificar quem pode votar neste painel. Consulte o campo [!UICONTROL Permission level] para obter limitações de votação em níveis de permissão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Selecione uma opção para especificar quem pode comentar em cartões para este quadro. Consulte o campo [!UICONTROL Permission level] para comentar limitações em níveis de permissão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Invitations]</p> </td> 
   <td> <p>Selecione quem pode convidar outras pessoas para este painel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Self-join]</p> </td> 
   <td> <p>Selecione se os membros da equipe podem ingressar no painel ou se precisam ser convidados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default labels]</p> </td> 
   <td> <p>Selecione se deseja usar o conjunto padrão de rótulos para o novo quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default lists]</p> </td> 
   <td> <p>Selecione se o conjunto padrão de listas deve ser adicionado ao quadro ([!UICONTROL To Do], [!UICONTROL Doing], [!UICONTROL Done]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board source ID]</p> </td> 
   <td> <p>Selecione ou mapeie a ID do quadro que você deseja copiar para o novo quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card Covers]</p> </td> 
   <td> <p>Selecione <strong>[!UICONTROL Yes]</strong> se quiser habilitar capas de cartão para o quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Background]</p> </td> 
   <td> <p>Selecione a cor do plano de fundo ou do plano de fundo personalizado.</p> <p>Observação: planos de fundo personalizados estão disponíveis somente para assinantes [!UICONTROL Trello Gold and Business Class].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Selecione entre dois modos de amadurecimento de cartão. </p> 
    <ul> 
     <li><strong>[!UICONTROL Regular]</strong>: os cartões tornam-se progressivamente mais transparentes à medida que envelhecem. </li> 
     <li><strong>[!UICONTROL Pirate]</strong>: As cartas vão rasgar, amarelar e quebrar como um velho mapa de piratas à medida que envelhecem.</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Board]**

Este módulo de ação edita as configurações de um quadro existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Insira ou mapeie o identificador [!UICONTROL Trello] exclusivo do quadro que você deseja que o módulo crie. Você pode recuperar a ID da placa usando outro módulo, como o módulo Watch Boards</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p> Informe ou mapeie um novo nome para o quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New description]</td> 
   <td> <p> Informe ou mapeie uma nova descrição do painel de discussão, se necessário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Insira ou mapeie o identificador [!UICONTROL Trello] exclusivo do quadro que você deseja que o módulo edite. Você pode recuperar a ID da placa usando outro módulo, como o módulo [!DNL Watch Activities].</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/org-id.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Selecione uma opção para especificar se o usuário em exercício está inscrito no quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>Os painéis têm regras de votação e comentário diferentes para cada nível de permissão. Por exemplo: se o seu painel for [!UICONTROL Private] e você definir as regras de votação e comentários como [!UICONTROL All], você receberá um erro. </p> <p>A votação e os comentários são limitados aos seguintes grupos para cada nível de permissão:</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      —&gt;Membros, Membros e Observadores</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      —&gt;Membros, Membros e Observadores, Membros da Organização</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      —&gt;Membros, Membros e Observadores, Membros da Organização, Todos</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Selecione uma opção para especificar quem pode votar neste painel. Consulte o campo [!UICONTROL Permission level] para obter limitações de votação em níveis de permissão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Selecione uma opção para especificar quem pode comentar em cartões para este quadro. Consulte o campo [!UICONTROL Permission level] para comentar limitações em níveis de permissão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Invitations] </td> 
   <td> <p>Selecione quem pode convidar pessoas para este painel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-join]</td> 
   <td> <p> Selecione se os membros da equipe podem ingressar no painel ou se precisam ser convidados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card covers]</td> 
   <td> <p> Selecione se as capas de cartão devem ser exibidas neste quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background] </td> 
   <td> <p>Selecione a cor do plano de fundo ou do plano de fundo personalizado.</p> <p>Observação: planos de fundo personalizados estão disponíveis somente para assinantes [!UICONTROL Trello Gold and Business Class].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> Se você optou por usar um plano de fundo personalizado no campo [!UICONTROL Background], insira ou mapeie a ID do plano de fundo que deseja usar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Selecione entre dois modos de amadurecimento de cartão. </p> 
    <ul> 
     <li><strong>[!UICONTROL Regular]</strong>: os cartões tornam-se progressivamente mais transparentes à medida que envelhecem. </li> 
     <li><strong>[!UICONTROL Pirate]</strong>: As cartas vão rasgar, amarelar e quebrar como um velho mapa de piratas à medida que envelhecem.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar feed enabled]</td> 
   <td> <p> Selecione se o feed de calendário está habilitado ou não.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL <Color> label name]</td> 
   <td> <p> Atribua um nome ao rótulo de cor desejado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Selecione uma opção para indicar se deseja arquivar (fechar) o quadro. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Board]**

Este módulo de ação recupera os detalhes de um quadro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Informe ou mapeie o ID do quadro sobre o qual deseja recuperar informações.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

Este módulo de pesquisa recupera informações sobre um quadro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Informe ou mapeie o nome (ou parte do nome) do quadro sobre o qual deseja obter informações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned boards]</td> 
   <td> <p> Insira o número máximo de painéis que [!DNL Workfront Fusion] retornará durante um ciclo de execução. Este valor deve ser menor ou igual a 1000.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partial] </p> </td> 
   <td> <p>Por padrão, esse módulo pesquisa o conteúdo do membro para correspondências exatas de cada palavra na sua consulta. Quando [!UICONTROL Partial] está habilitado, o módulo procura conteúdo que inicie com qualquer palavra em sua consulta.</p> <p> Por exemplo, se você estiver usando a palavra "desenvolvimento" para procurar um quadro chamado "Meu relatório de status de desenvolvimento", por padrão, seria necessário pesquisar a palavra inteira. Se você tiver o [!UICONTROL Partial] habilitado, poderá pesquisar por "dev", mas não por "desenvolvimento".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Boards] </td> 
   <td> <p>Insira "meu" ou mapeie uma lista separada por vírgulas de IDs de cartão.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archive or Unarchive a Board]**

Esse módulo de ação fecha ou reabre um quadro especificado por você.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Informe ou mapeie a ID do quadro que você deseja fechar ou reabrir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Selecione se deseja fechar (arquivar) ou reabrir (desarquivar) o quadro.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

Esse módulo de ação atribui um membro a um quadro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Selecione o painel em que deseja adicionar um membro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email address]</td> 
   <td> <p> Insira ou mapeie o endereço de email do membro que deseja adicionar ao quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Member type]</p> </td> 
   <td> <p>Selecione o tipo de membro que deseja adicionar ao quadro.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: Um administrador de placa pode executar qualquer ação na placa.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: um membro normal é simplesmente um membro do painel.</li> 
     <li><strong>[!UICONTROL Observer]</strong>: um observador é um membro com acesso somente leitura ao painel. <br>Os observadores só estão disponíveis para equipes com [!UICONTROL Trello Business Class].</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Full name]</td> 
   <td> <p> Insira o nome completo do usuário que deseja adicionar ao quadro.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

Este módulo de ação remove um membro de um quadro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Insira (mapeie ou selecione) a ID do quadro do qual deseja remover o usuário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Member] </td> 
   <td> <p>Selecione o membro que deseja remover do painel.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Listas

+++ **[!UICONTROL Watch cards moved to a list]**

Esse módulo acionador é ativado quando um cartão é movido para uma lista específica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board]</td> 
   <td>Selecione o quadro que contém a lista que você deseja observar para os cartões.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List]</td> 
   <td>Selecione a lista que deseja observar com relação aos cartões.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>O número máximo de cartões [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p>  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a List]**

Esse módulo de ação cria uma lista em um quadro que você especifica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Insira ou mapeie a ID do quadro em que deseja criar uma lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Insira ou mapeie um nome para a nova lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecione se deseja adicionar a lista à parte superior ou anexá-la à parte inferior do cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy list]</td> 
   <td> <p> Selecione como você deseja inserir a ID da lista a ser copiada.</p> 
    <ul> 
     <li> <p><strong>Inserir manualmente</strong> </p> <p>No campo <strong>[!UICONTROL List ID]</strong>, insira ou mapeie a ID da lista que deseja copiar.<br></p> </li> 
     <li> <p><strong>Selecionar</strong> </p> <p>Selecione o quadro que contém a lista que você deseja copiar e selecione a lista.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a List]**

Este módulo de ação edita uma lista existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td> <p> Insira ou mapeie a ID da lista que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Insira ou mapeie um novo nome para a lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Mapeie ou selecione o quadro para onde deseja mover a lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecione se deseja adicionar a lista à parte superior ou anexá-la à parte inferior do cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribed]</td> 
   <td> <p>Ative esta opção se quiser inscrever o membro ativo na lista.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a List]**

Este módulo de ação recupera detalhes sobre uma lista específica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL List ID]</p> </td> 
   <td> <p>Insira ou mapeie a ID da lista da qual deseja recuperar informações.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Cartões

+++ **[!UICONTROL Watch cards]**

Esse módulo acionador é ativado quando um novo cartão é adicionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Selecione o local que deseja observar para os cartões.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards]</strong> </li> 
     <li> <p><strong>Cartões no painel específico</strong> </p> <p>Selecione o painel que deseja observar para os cartões</p> </li> 
     <li> <p><strong>[!UICONTROL Cards on specific list]</strong> </p> <p>Selecione o quadro que contém a lista que você deseja observar para os cartões e selecione a lista.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>O número máximo de cartões [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a card]**

Esse módulo de ação cria um cartão em uma lista selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a list ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID da lista à qual deseja adicionar um cartão.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL List ID]</strong>, insira ou mapeie a ID da lista à qual deseja adicionar um cartão.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém a lista que você deseja copiar e selecione a lista.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>Para cada rótulo que você deseja adicionar ao cartão, insira a ID do rótulo. A ID pode ser recuperada, por exemplo, usando o módulo [!UICONTROL Retrieve Labels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members]</td> 
   <td>Para cada membro que deseja adicionar ao cartão, insira a ID do membro. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Insira um nome para o novo cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Description]</p> </td> 
   <td> <p>Insira a descrição do cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecione se deseja adicionar o cartão à parte superior ou [!UICONTROL append] o cartão à parte inferior da lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Insira uma data de vencimento para o cartão. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Habilite esta opção para marcar o cartão como concluído na data de vencimento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td> <p>Insira ou mapeie o URL de um arquivo que você deseja adicionar como anexo ao cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Source file]</p> </td> 
   <td> <p>Insira ou mapeie informações para um arquivo que deseja adicionar como anexo ao cartão.</p> 
    <ul> 
     <li>[!UICONTROL File name]: Insira ou mapeie o nome do arquivo, incluindo a extensão.</li> 
     <li> 
     <p>Selecione um arquivo de um módulo anterior ou mapeie o nome e os dados do arquivo</p> 
     <p>Observação: há um limite de upload de arquivo de 10 MB por anexo. No entanto, os membros [!UICONTROL Business Class] e [!UICONTROL Trello Gold] têm um limite de carregamento de arquivo de 250 MB por anexo.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy card]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão que deseja copiar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Card ID]</strong>, insira ou mapeie a ID do cartão que deseja copiar.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão que deseja copiar, selecione a lista que contém o cartão e selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Card]**

Esse módulo de ação edita um cartão existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Card ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão que deseja editar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Card ID]</strong>, insira ou mapeie a ID do cartão que deseja editar.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão que deseja editar, selecione a lista que contém o cartão e selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p>Insira ou mapeie um novo nome para o cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New description]</p> </td> 
   <td> <p>Insira ou mapeie uma nova descrição para o cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Move a card]</p> </td> 
   <td> <p>Selecione o quadro ou o quadro e a lista para onde deseja mover o cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>Adicione as IDs de todos os rótulos que deseja adicionar ao cartão. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecione se deseja adicionar o cartão à parte superior ou [!UICONTROL append] o cartão à parte inferior da lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Insira uma data de vencimento para o cartão. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Se essa opção estiver ativada, o cartão será marcado como concluído na data de vencimento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members] </td> 
   <td> <p>Adicione ou mapeie a ID de membros que deseja adicionar ao cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment cover ID]</p> </td> 
   <td> <p>Insira ou mapeie a ID do anexo de imagem que você deseja que o cartão use como capa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Selecione se o membro deve assinar o cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Selecione uma opção para indicar se deseja arquivar (fechar) o cartão. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Card]**

Esse módulo de ação recupera os detalhes de um cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p>Insira a ID do quadro que contém o cartão sobre o qual deseja recuperar detalhes. Isso permite que você veja os nomes dos campos personalizados do quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão sobre o qual deseja recuperar detalhes.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Card ID]</strong>, insira ou mapeie a ID do cartão sobre o qual deseja recuperar detalhes.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão do qual deseja recuperar detalhes e selecione a lista que contém o cartão e, em seguida, selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Cards]**

Este módulo de ação retorna cartões que correspondem à consulta de pesquisa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board] </td> 
   <td> <p>Selecione os painéis de discussão que deseja pesquisar. Se nenhum painel for selecionado, todos os painéis serão pesquisados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Query]</p> </td> 
   <td> <p>Insira a consulta de pesquisa. Você pode refinar sua pesquisa usando os seguintes operadores de pesquisa:</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>Você pode adicionar "-" a qualquer operador para fazer uma pesquisa negativa, como <code>[!UICONTROL -has:members]</code> para procurar cartões sem nenhum membro atribuído.</p> </li> 
     <li><code><strong>@name</strong></code> <p>Retorna cartões atribuídos a um membro. Você também pode usar <code>member:</code>. Use o <code>@me</code> para incluir apenas seus cartões.</p> </li> 
     <li><code><strong>#label</strong></code> <p>Retorna cartões rotulados. Você também pode usar <code>label:</code>. Por exemplo, <code>label:"FIX IT"</code> retornará cartões com o rótulo chamado "CORRIGIR".</p> </li> 
     <li><code><strong>board:id</strong></code> <p>Retorna cartões em um quadro específico. Por exemplo, <code>board:Trello</code> retornará cartões em quadros com [!UICONTROL Trello] no nome do quadro.</p> </li> 
     <li><code><strong>list:name</strong></code> <p>Retorna cartões dentro da lista chamada "nome".</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>Retorna cartões com anexos. O operador <code>has</code>: também pode ser usado com outros atributos, como <code>has:description</code>, <code>has:cover</code>, <code>has:members</code> ou <code>has:stickers</code>.</p> </li> 
     <li><code><strong>due:day</strong></code> <p>Retorna cartões com vencimento em 24 horas. O operador <code>due:</code> também pode ser usado com outros períodos, como <code>due:week</code>, <code>due:month</code> ou <code>due:overdue</code>. Você também pode procurar um intervalo de dias específico. Por exemplo, adicionar <code>due:14</code> à pesquisa inclui cartões com vencimento nos próximos 14 dias.</p> </li> 
     <li><code><strong>created:day</strong></code> <p>Retorna cartões criados nas últimas 24 horas. O operador <code> created:</code> também pode ser usado com outros cronogramas, como <code>created:week</code> ou <code>created:month</code>. Você também pode procurar um intervalo de dias específico. Por exemplo, adicionar <code>created:14</code> à pesquisa inclui cartões criados nos últimos 14 dias.</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>Retorna cartões editados nas últimas 24 horas. O operador <code>edited:</code> também pode ser usado com outros intervalos de tempo, como <code>edited:week</code> ou <code>edited:month</code>. Você também pode procurar um intervalo de dias específico. Por exemplo, adicionar <code>edited:21</code> à pesquisa inclui cartões editados nos últimos 21 dias.</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>Retorna cartões que correspondem ao texto de descrições, listas de verificação, comentários ou nomes de cartões. Por exemplo, comentário: "CORRIGIR TI" retornará cartões com "CORRIGIR TI" em um comentário.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>Retorna cartões abertos ou arquivados. Se nenhum for especificado, [!UICONTROL Trello] retornará os dois tipos.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>Inclui apenas cartões em quadros estrelados.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned cards]</td> 
   <td> <p> O número máximo de cartões [!DNL Workfront Fusion] retornará durante um ciclo de execução. Este valor deve ser menor ou igual a 1000.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Por padrão, esse módulo pesquisa o conteúdo do membro para correspondências exatas de cada palavra na sua consulta. Quando [!UICONTROL Partial] está habilitado, o módulo procura conteúdo que inicie com qualquer palavra em sua consulta.</p> <p> Por exemplo, se você estiver usando a palavra "desenvolvimento" para procurar um quadro chamado "Meu relatório de status de desenvolvimento", por padrão, seria necessário pesquisar a palavra inteira. Se você tiver o [!UICONTROL Partial] habilitado, poderá pesquisar por "dev", mas não por "desenvolvimento".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cards] </td> 
   <td> <p>Adicione todos os cartões que você deseja procurar especificamente.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archive or Unarchive a Card]**

Esse módulo de ação arquiva ou envia um cartão de volta para a placa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card ID]</td> 
   <td> <p> Insira ou mapeie a ID do cartão que deseja arquivar ou enviar de volta para o quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Selecione se deseja fechar o cartão (arquivar) ou enviá-lo de volta para o quadro (desarquivar).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Add an Attachment]**

Esse módulo de ação adiciona um anexo ao cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão sobre o qual deseja recuperar detalhes.</p> 
    <ul> 
     <li> <p><strong>Inserir manualmente</strong> </p> <p>No campo <strong>[!UICONTROL Card ID]</strong>, insira ou mapeie a ID do cartão sobre o qual deseja recuperar detalhes.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão do qual deseja recuperar detalhes e selecione a lista que contém o cartão e, em seguida, selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment type]</p> </td> 
   <td> <p>Selecione se deseja fazer upload do arquivo diretamente ou fornecer um URL para o arquivo.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </li> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Insira a URL do arquivo e forneça um nome para o anexo.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Membros

+++ **[!UICONTROL Assign a Member to a Board]**

Consulte &quot;[!UICONTROL Assign a Member to a Board]&quot; em [Quadros](#boards).

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

Consulte &quot;[!UICONTROL Unassign a Member from a Board]&quot; em [Quadros](#boards).

+++

+++ **[!UICONTROL Add a Member to a Card]**

Esse módulo de ação adiciona o membro especificado ao cartão especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter card ID and member ID]</p> </td> 
   <td> <p>Escolha como você deseja inserir a ID do cartão e a ID do membro.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Insira ou mapeie o <strong>[!UICONTROL Card ID]</strong> e o <strong>[!UICONTROL Member ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o painel que contém o cartão ao qual deseja adicionar um membro e selecione a lista que contém o cartão, o próprio cartão e o membro que deseja adicionar ao cartão.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Members]**

Este módulo de ação recupera informações sobre [!UICONTROL Trello] membros.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Insira o nome completo ou o nome de usuário do usuário que deseja localizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Por padrão, esse módulo pesquisa o conteúdo do membro para correspondências exatas de cada palavra na sua consulta. Quando [!UICONTROL Partial] está habilitado, o módulo procura conteúdo que inicie com qualquer palavra em sua consulta.</p> <p> Por exemplo, se você estiver usando a palavra "desenvolvimento" para procurar um quadro chamado "Meu relatório de status de desenvolvimento", por padrão, seria necessário pesquisar a palavra inteira. Se você tiver o [!UICONTROL Partial] habilitado, poderá pesquisar por "dev", mas não por "desenvolvimento".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned members]</td> 
   <td> <p> O número máximo de membros [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Listas de verificação

+++ **[!UICONTROL Create a Checklist]**

Esse módulo de ação cria uma lista de verificação no cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão no qual deseja adicionar uma lista de verificação.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Card ID]</strong>, insira ou mapeie a ID do cartão ao qual deseja adicionar uma lista de verificação.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar uma lista de verificação, selecione a lista que contém o cartão e selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Insira ou mapeie um nome para a lista de verificação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecione se deseja adicionar a lista de verificação à parte superior ou a lista de verificação [!UICONTROL append the] à parte inferior do cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter checklist ID]</p> </td> 
   <td> <p>Insira ou mapeie a ID de uma lista de verificação de origem que você deseja copiar para a nova.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Checklist Item]**

Este módulo de ação adiciona um item a uma lista de verificação específica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter checklist ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID da lista de verificação à qual deseja adicionar um item.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Checklist ID]</strong>, insira ou mapeie a ID do cartão ao qual deseja adicionar uma lista de verificação.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar uma lista de verificação e selecione a lista que contém o cartão, em seguida, selecione o cartão e selecione a lista de verificação.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Insira ou mapeie um nome para o novo item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Selecione se deseja adicionar o item à parte superior ou [!UICONTROL append] à parte inferior da lista de verificação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Checked]</p> </td> 
   <td> <p>Habilite esta opção se você deseja adicionar o item como já selecionado.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Checklist Item]**

Este módulo de ação edita uma lista de verificação existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Card ID and Checklist Item ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão e a lista de verificação onde deseja editar um item.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Checklist ID]</strong>, insira ou mapeie a ID do cartão ao qual deseja adicionar uma lista de verificação.</p> <p>No campo <strong>[!UICONTROL Checklist Item ID]</strong>, insira ou mapeie a ID da lista de verificação.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar uma lista de verificação e selecione a lista que contém o cartão, em seguida, selecione o cartão e selecione a lista de verificação.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Checklist ID]</td> 
   <td>Selecione ou mapeie a lista de verificação para a qual você deseja mover o item da lista.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Insira ou mapeie um nome para o novo item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Selecione se deseja adicionar o item à parte superior ou anexar à parte inferior da lista de verificação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL State]</p> </td> 
   <td> <p>Selecione se o item da lista de verificação está completo ou incompleto.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Rótulos

+++ **[!UICONTROL Add a Label to a Card]**

Esse módulo de ação adiciona um rótulo a um cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão no qual deseja adicionar uma lista de verificação.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Card ID]</strong>, insira ou mapeie a ID do cartão ao qual deseja adicionar uma lista de verificação. No campo <strong>[!UICONTROL Label ID]</strong>, insira ou mapeie a ID do rótulo que deseja adicionar.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar uma lista de verificação, selecione a lista que contém o cartão e selecione o cartão. </p> <p>Selecione o rótulo que deseja adicionar ao cartão.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Comentários

+++ **[!UICONTROL Watch Comments]**

Recupera detalhes do comentário quando há um novo comentário em um local especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Selecione o local que deseja observar para comentários.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards] em todos os lugares</strong> </li> 
     <li> <p><strong>[!UICONTROL Board]</strong> </p> <p>Selecione o painel que deseja observar para comentários</p> </li> 
     <li> <p><strong>[!UICONTROL List]</strong> </p> <p>Selecione o painel que contém a lista que você deseja observar para comentários e, em seguida, selecione a lista.</p> </li> 
     <li><strong>[!UICONTROL Card]</strong> </li> 
     <li>Selecione o quadro que contém o cartão que você deseja observar para comentários, selecione a lista que contém o cartão e selecione o cartão.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>O número máximo de comentários [!DNL Workfront Fusion] retornados durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Comment in a Card]**

Esse módulo de ação adiciona um comentário a um cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão ao qual deseja adicionar um comentário.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Card ID]</strong>, insira ou mapeie a ID do cartão ao qual deseja adicionar um comentário.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar um comentário e selecione a lista que contém o cartão e, em seguida, selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment] </td> 
   <td> <p>Insira o comentário que deseja adicionar ao cartão selecionado.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Comments in a Card]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão ao qual deseja adicionar um comentário.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>No campo <strong>[!UICONTROL Card ID]</strong>, insira ou mapeie a ID do cartão ao qual deseja adicionar um comentário.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar um comentário e selecione a lista que contém o cartão e, em seguida, selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td> <p> Insira o número máximo de comentários que [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since] </td> 
   <td> <p>Defina a data de início do período em que o comentário foi criado. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before] </td> 
   <td> <p>Defina a data final do período em que o comentário foi criado. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL Trello] IDs de objeto

* [Como localizar a ID ou o link curto de um cartão no  [!DNL Trello]](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [Como localizar IDs de outros objetos no  [!DNL Trello]](#how-to-find-ids-of-other-objects-in-trello)

### Como encontrar a ID ou o link curto de um cartão no [!DNL Trello]

Se quiser editar um cartão ou criar um novo comentário, é necessário saber a ID do cartão ou seu link curto. Essas informações podem ser obtidas na saída do gatilho [!UICONTROL New Card]. O link curto para um cartão também pode ser obtido abrindo o cartão e clicando no botão [!UICONTROL Share]. O link curto pode ser encontrado na caixa [!UICONTROL Link to this card], no final da URL após `https://trello.com/c/`.

![](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### Como encontrar IDs de outros objetos em [!DNL Trello]

As IDs de quadro, lista e comentário só podem ser obtidas usando acionadores. O site do [!DNL trello.com] não mostra essas IDs.
