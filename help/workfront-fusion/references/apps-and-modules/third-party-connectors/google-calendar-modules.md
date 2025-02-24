---
title: Módulos do Google Calendar
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Calendário da Google, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 160e503adeca5404e18fd0cba9f475fee8510a48
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# [!DNL Google Calendar] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!UICONTROL Google Calendar], bem como conectá-los a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!DNL Google Calendar], você deve ter uma conta [!DNL Google].

## Informações da API do calendário do Google

O conector do Calendário do Google usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://www.googleapis.com/calendar/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v5.4.5</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Calendar] módulos e seus campos

Ao configurar módulos do [!DNL Google Calendar], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Google Calendar] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Acionadores](#triggers)
* [Ações](#actions)
* [Iteradores](#iterators)

### Acionadores

* [Assistir a eventos](#watch-events)
* [Assistir a eventos (instantâneo)](#watch-events-instant)

#### Assistir a eventos

Esse módulo de acionamento executa um cenário quando um novo evento é adicionado, atualizado, excluído, iniciado ou encerrado no calendário especificado. O módulo retorna todos os campos padrão associados ao registro ou aos registros, juntamente com quaisquer campos e valores personalizados que a conexão acesse. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Calendar] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Selecione o calendário com o qual deseja que o módulo funcione.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Escolha se deseja assistir somente a novos eventos ou a novos eventos e todas as alterações.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>Habilite esta opção para incluir eventos que foram excluídos.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Insira o texto para o qual deseja retornar os resultados.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Defina o número máximo de eventos com os quais [!DNL Workfront Fusion] trabalha durante um ciclo (o número de repetições por execução de cenário). Se o valor for definido como muito alto, a conexão pode ser interrompida no lado do serviço de terceiros especificado (tempo limite). [!DNL Workfront Fusion] não tem nenhuma influência sobre isso. Recomendamos que você defina um valor mais baixo e defina um valor mais alto para o número máximo de ciclos ou execute o cenário com mais frequência.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Assistir a eventos (instantâneo)

Este módulo de acionamento usa um gancho de e-mail para criar um endereço de e-mail que você pode usar como convidado para eventos. O módulo inicia um cenário com base nos eventos para os quais o endereço de email é convidado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Mailhook] </td> 
   <td> <p>Selecione o mailhook que deseja usar para este módulo. Para criar um novo mailhook, clique em <b>Adicionar</b> e insira a conexão que deseja usar para o mailhook.</p><p>Para obter instruções sobre como conectar sua conta do [!DNL Google Calendar] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Defina o número máximo de eventos com os quais [!DNL Workfront Fusion] trabalha durante um ciclo (o número de repetições por execução de cenário). Se o valor for definido como muito alto, a conexão pode ser interrompida no lado do serviço de terceiros especificado (tempo limite). [!DNL Workfront Fusion] não tem nenhuma influência sobre isso. Recomendamos que você defina um valor mais baixo e defina um valor mais alto para o número máximo de ciclos ou execute o cenário com mais frequência.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [Criar um calendário](#create-a-calendar)
* [Criar um evento](#create-an-event)
* [Excluir um evento](#delete-an-event)
* [Obter eventos](#get-events)
* [Atualizar um evento](#update-an-event)

#### Criar um calendário

Este módulo de ação cria um calendário associado à conta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Calendar] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>Selecione a cor a ser associada ao calendário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>Insira ou mapeie um nome para o novo calendário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event]

Esse módulo de ação cria um evento.

Você especifica o calendário e os parâmetros do evento.

O módulo retorna a ID do evento e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL Google Calendar] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selecione o calendário no qual deseja que o evento apareça.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>Selecione a cor que o evento mostra no calendário.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Insira ou mapeie um nome para o evento. </p> <p>Observação: se você selecionou [!UICONTROL Quick add] no campo [!UICONTROL Create an event], é possível incluir a data e a hora do evento, e [!DNL Workfront Fusion] cria o evento para essa data e hora. Exemplo: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Se você selecionou [!UICONTROL Quick add], mas não incluiu uma data e hora no nome do evento, o evento será criado a partir da hora atual e terá duração de uma hora.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Ative essa opção se o evento for um evento de dia inteiro (não requer horas de início e término).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Insira ou mapeie a data e a hora de início do evento. </p> <p>Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Insira ou mapeie a data e a hora de término do evento. </p> <p>Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Insira ou mapeie uma descrição para o evento. Este campo é compatível com o HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Insira um local para o evento em formato de texto.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Habilite esta opção para usar as configurações padrão de lembrete. Se você definir um lembrete personalizado no campo [!UICONTROL Reminder], esse valor será definido como Não.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Adicionar lembrete para o evento. Para cada lembrete que você deseja adicionar, clique em <b>Adicionar item</b>, selecione o método com o qual deseja ser lembrado e defina por quanto tempo (em minutos) antes do evento que você deseja ser lembrado.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Adicionar os participantes ao evento. Para cada participante, clique em <b>Adicionar um participante</b> e, em seguida, insira ou mapeie seu nome e endereço de email.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Selecione se você deseja que as pessoas que exibem seu calendário o vejam como Ocupado ou Disponível durante este evento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Selecione a visibilidade deste evento. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>O evento tem a visibilidade definida nas configurações do calendário.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Qualquer pessoa com quem o calendário é compartilhado pode ver este evento.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Somente os participantes podem ver este evento.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Selecione se deseja enviar notificações sobre a criação de um novo evento para todos os convidados, para convidados que não sejam [!DNL Google Calendar] ou para ninguém.</p> <p>Dica: recomendamos usar a opção [!UICONTROL None] somente para casos de uso de migração.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Ative esta opção se quiser que os convidados modifiquem este evento.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Adicione todas as regras de recorrência que deseja aplicar a este evento. Cada regra requer uma lista de [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] e [!UICONTROL EXDATE] linhas para um evento recorrente. Observe que [!UICONTROL DTSTART] e [!UICONTROL DTEND] linhas não são permitidas neste campo; as horas de início e término do evento são especificadas nos campos de início e término. Esse campo é omitido para eventos únicos ou instâncias de eventos recorrentes. Para obter mais informações, consulte <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an event]

Este módulo de ação exclui um evento.

Você especifica o calendário e a ID do evento.

O módulo retorna a ID do evento e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Calendar] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selecione o calendário que contém o evento que você deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> Insira a ID de evento de um evento [!DNL Google Calendar] criado anteriormente que você deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get events]

Este módulo recupera informações sobre eventos no calendário selecionado com base nos critérios que você especificar.

Você especifica o calendário e os parâmetros da pesquisa.

O módulo retorna a ID dos eventos e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL Google Calendar] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selecione o calendário para o qual deseja recuperar eventos.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> Insira ou mapeie a data de início do evento. Esse módulo também recupera eventos iniciados antes dessa data, que ainda estão ocorrendo na data inicial inserida. </p> <p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Insira ou mapeie a data de término do evento. </p> <p> Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Single events]</td> 
   <td> <p> Habilite esta opção para tratar eventos recorrentes como instâncias únicas. Por exemplo, se você tiver uma reunião semanal e essa opção estiver habilitada, o módulo retornará a reunião de cada semana como um evento separado.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Informe ou mapeie o termo de pesquisa pelo qual deseja pesquisar. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td> <p>Selecione a ordem dos eventos retornados no resultado.</p> 
    <ul> 
     <li><strong>[!UICONTROL Start Time]</strong>: ordene pela data e hora de início (em ordem crescente). Isso só está disponível ao consultar eventos únicos.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>: ordene por hora da última modificação (crescente).</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mazimum number of returned events]</td> 
   <td> <p>Defina o número máximo de eventos que [!DNL Workfront Fusion] retorna durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an event]

Esse módulo de ação altera um evento existente.

Você especifica o calendário e a ID do evento.

O módulo retorna a ID do evento e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Calendar] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe [!DNL Workfront Fusion] - Instruções básicas</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Selecione o calendário com o qual deseja trabalhar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Insira a ID do evento [!DNL Google Calendar] criado anteriormente que você deseja atualizar.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Insira ou mapeie um nome para o evento. </p> <p>Observação: se você selecionou [!UICONTROL Quick add] no campo [!UICONTROL Create an event], é possível incluir a data e a hora do evento, e [!DNL Workfront Fusion] cria o evento para essa data e hora. Exemplo: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Se você selecionou [!UICONTROL Quick add], mas não incluiu uma data e hora no nome do evento, o evento será criado a partir da hora atual e terá duração de uma hora.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Ative essa opção se o evento for um evento de dia inteiro (não requer horas de início e término).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Insira ou mapeie a data e a hora de início do evento. </p> <p>Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Insira ou mapeie a data e a hora de término do evento. </p> <p>Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Insira ou mapeie uma descrição para o evento. Este campo é compatível com o HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Insira um local para o evento em formato de texto.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Habilite esta opção para usar as configurações padrão de lembrete. Se você definir um lembrete personalizado no campo [!UICONTROL Reminder], esse valor será definido como Não.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Adicionar lembrete para o evento. Para cada lembrete que você deseja adicionar, clique em <b>Adicionar item</b>, selecione o método com o qual deseja ser lembrado e defina por quanto tempo (em minutos) antes do evento que você deseja ser lembrado.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Adicionar os participantes ao evento. Para cada participante, clique em <b>Adicionar um participante</b> e, em seguida, insira ou mapeie seu nome e endereço de email.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Selecione se você deseja que as pessoas que exibem seu calendário o vejam como Ocupado ou Disponível durante este evento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Selecione a visibilidade deste evento. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>O evento tem a visibilidade definida nas configurações do calendário.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Qualquer pessoa com quem o calendário é compartilhado pode ver este evento.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Somente os participantes podem ver este evento.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Selecione se deseja enviar notificações sobre a criação de um novo evento para todos os convidados, para convidados que não sejam [!DNL Google Calendar] ou para ninguém.</p> <p>Dica: recomendamos usar a opção [!UICONTROL None] somente para casos de uso de migração.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Ative esta opção se quiser que os convidados modifiquem este evento.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Adicione todas as regras de recorrência que deseja aplicar a este evento. Cada regra requer uma lista de [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] e [!UICONTROL EXDATE] linhas para um evento recorrente. Observe que [!UICONTROL DTSTART] e [!UICONTROL DTEND] linhas não são permitidas neste campo; as horas de início e término do evento são especificadas nos campos de início e término. Esse campo é omitido para eventos únicos ou instâncias de eventos recorrentes. Para obter mais informações, consulte <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr>

</tbody> 
</table>

### Iteradores

#### Iterar anexos

Esses módulos de ação repetem por meio de anexos para um evento e geram cada anexo em um conjunto separado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Selecione o módulo neste cenário que gera o evento que contém os anexos que você deseja iterar. </td> 
  </tr> 
 </tbody> 
</table>

#### Iterar participantes

Estes módulos de ação repetem os participantes de um evento e geram cada participante em um conjunto separado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Selecione o módulo neste cenário que gera o evento que contém os participantes que você deseja iterar. </td> 
  </tr> 
 </tbody> 
</table>





## Acionar um cenário antes de um evento

Você pode acionar um cenário em um horário especificado antes de um evento com a ajuda de lembretes de email padrão [!DNL Google Calendar] e do módulo [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook].

1. Use o módulo [!UICONTROL Google Calendar] >[!UICONTROL Update an event] para adicionar um lembrete de email ao seu evento:

   ![Acionar cenário antes do evento](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. Crie um novo cenário começando com o módulo [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook].

   1. Copie o endereço de email do mailhook.
   1. Salve o cenário e execute-o.

1. Em [!DNL Gmail], redirecionar os lembretes de email do [!DNL Google Calendar] para o endereço de email do mailhook:

   1. Abra o **[!UICONTROL [!DNL Gmail] settings]**.
   1. Abra a guia **[!UICONTROL Forwarding and POP/IMAP]**.
   1. Clique em **[!UICONTROL Add a forwarding address].**
   1. Cole o endereço de email dos ganchos de email copiados, clique em&#x200B;**[!UICONTROL Next]**, confirme pressionando **[!UICONTROL Proceed]** na janela pop-up e depois clique em **[!UICONTROL OK]**.

   1. Em [!DNL Workfront Fusion], alterne para o novo cenário que deve concluir sua execução recebendo o email de confirmação.
   1. Clique no balão acima do módulo para inspecionar a saída do módulo.
   1. Expanda o item `Text` e copie o código de Confirmação:

      ![Código de confirmação](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. No Gmail, cole o código de Confirmação na caixa de edição e clique em&#x200B;**[!UICONTROL Verify]**:

      ![Colar código](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Abra a guia **[!UICONTROL Filters and Blocked Addresses]**.
   1. Clique em **[!UICONTROL Create a new filter]**.
   1. Configure um filtro para todos os emails provenientes de `     calendar-notification@google.com` e clique&#x200B;**[!UICONTROL Create a filter]**:
   1. Selecione **[!UICONTROL Forward it to]** e escolha na lista o endereço de email dos ganchos.
   1. Clique em **[!UICONTROL Create filter]** para criar o filtro.

1. (Opcional) Em [!DNL Workfront Fusion], adicione o módulo [!UICONTROL Text parser] > [!UICONTROL Match pattern] após o módulo [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] para analisar o código HTML do email e obter as informações necessárias.

   Por exemplo, você pode configurar o módulo da seguinte maneira para obter a ID do evento:

   *Padrão*: `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Texto*: o item `HTML content` emitido do módulo [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook].
