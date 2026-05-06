---
title: Funções de data e hora
description: As seguintes funções de data e hora estão disponíveis no painel de mapeamento do Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 92813dac-4bf0-4681-9b71-7bd2e92a89a4
source-git-commit: fc7f98c128f73a60d75750c6bd57ec8ddc31954c
workflow-type: tm+mt
source-wordcount: '2375'
ht-degree: 3%

---

# Funções de data e hora

## Variáveis

### now

Obtém a hora atual no formato AAAA-MM-DD-hh:mm:ss.

### carimbo de data e hora

Obtém a hora atual como um carimbo de data/hora Unix.

## Funções

### [!UICONTROL addSeconds (data; número)]

Retorna uma nova data como resultado da adição de um determinado número de segundos a uma data. Para subtrair segundos, informe um número negativo.

>[!BEGINSHADEBOX]

**Exemplos:**

* `addSeconds(2016-12-08T15:55:57.536Z;2)`

  Retorna 2016-12-08T15:55:59.536Z

* `addSeconds(2016-12-08T15:55:57.536Z;-2)`

  Retorna 2016-12-08T15:55:55.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addMinutes (data; número)] {#addminutes-date-number}

Retorna uma nova data como resultado da adição de um determinado número de minutos a uma data. Para subtrair minutos, informe um número negativo.

>[!BEGINSHADEBOX]

**Exemplos:**

* `addMinutes(2016-12-08T15:55:57.536Z;2)`

  Retorna 2016-12-08T15:57:57.536Z

* `addMinutes(2016-12-08T15:55:57.536Z;-2)`

  Retorna 2016-12-08T15:53:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addHours (data; número)] {#addhours-date-number}

Retorna uma nova data como resultado da adição de um determinado número de horas a uma data. Para subtrair horas, informe um número negativo.

>[!BEGINSHADEBOX]

**Exemplos:**

* `addHours(2016-12-08T15:55:57.536Z; 2)`

  Retorna 2016-12-08T17:55:57.536Z

* `addHours(2016-12-08T15:55:57.536Z;-2)`

  Retorna 2016-12-08T13:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addDays (data; número)] {#adddays-date-number}

Retorna uma nova data como resultado da adição de um determinado número de dias a uma data. Para subtrair dias, informe um número negativo.

>[!BEGINSHADEBOX]

**Exemplos:**

* `addDays(2016-12-08T15:55:57.536Z;2)`

  Retorna 2016-12-10T15:55:57.536Z

* `addDays(2016-12-08T15:55:57.536Z;-2)`

  Retorna 2016-12-6T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addWeekDays(data; número)]

[!BADGE Novo!]{type=Informative}

Adiciona o número de dias úteis à data. Somente valores inteiros são adicionados (valores fracionais são arredondados para baixo).

>[!BEGINSHADEBOX]

**Exemplos:**

`addWeekDays("2016-12-08T15:55:57.536Z"; 2)`

Retorna 2016-12-12T15:55:57.536Z
`addWeekDays("2016-12-08T15:55:57.536Z"; -2)`
Retorna 2016-12-06T15:55:57.536Z

>[!ENDSHADEBOX]


### [!UICONTROL addMonths (data; número)]

Retorna uma nova data como resultado da adição de um determinado número de meses a uma data. Para subtrair meses, informe um número negativo.

>[!BEGINSHADEBOX]

**Exemplos:**

* `addMonths(2016-08-08T15:55:57.536Z;2)`

  Retorna 2016-10-08T15:55:57.536Z

* `addMonths(2016-08-08T15:55:57.536Z;-2)`

  Retorna 2016-06-08T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addYears (data; número)]

Retorna uma nova data como resultado da adição de um determinado número de anos a uma data. Para subtrair anos, informe um número negativo.

>[!BEGINSHADEBOX]

**Exemplos:**

* `addYears(2016-08-08T15:55:57.536Z;2)`

  Retorna 2018-08-08T15:55:57.536Z

* `addYears(2016-12-08T15:55:57.536Z; -2)`

  Retorna 2014-08-08T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL dayOfMonth(data)]

[!BADGE Novo!]{type=Informative}

Retorna o dia do mês da data como um número entre 1 e 31.

>[!BEGINSHADEBOX]

**Exemplos:**

* `dayOfMonth("2016-12-28T16:03:06.372Z")`

  Retorna 28
* `dayOfMonth("2015-01-05T11:36:39.138Z")`

  Devoluções 5

>[!ENDSHADEBOX]


### [!UICONTROL dayOfWeek(data)]

[!BADGE Novo!]{type=Informative}

Retorna o dia da semana da data como um número entre 1 (domingo) e 7 (sábado).

>[!BEGINSHADEBOX]

**Exemplos:**

* `dayOfWeek("2016-12-28T16:03:06.372Z")`

  Devoluções 4
* `dayOfWeek("2016-12-25T16:03:06.372Z")`

  Devoluções 1

>[!ENDSHADEBOX]


### [!UICONTROL daysInMonth(data)]

[!BADGE Novo!]{type=Informative}

Retorna o número total de dias no mês de uma data informada.

>[!BEGINSHADEBOX]

**Exemplos:**

* `daysInMonth("2016-01-01T00:00:00.000Z")`

  Retorna 31
* `daysInMonth("2016-02-01T00:00:00.000Z")`

  Retorna 29

>[!ENDSHADEBOX]


### [!UICONTROL daysInSplitWeek(date)]

[!BADGE Novo!]{type=Informative}

Retorna o número total de dias da semana entre a data informada e o fim da semana, ou o fim do mês, o qual vier primeiro.

>[!BEGINSHADEBOX]

**Exemplos:**

* `daysInSplitWeek("2016-12-28T16:03:06.372Z")`

  Devoluções 3
* `daysInSplitWeek("2016-01-25T16:03:06.372Z")`

  Devoluções 5

>[!ENDSHADEBOX]


### [!UICONTROL daysInYear(data)]

[!BADGE Novo!]{type=Informative}

Retorna o número total de dias no ano de uma data informada (365 para um ano regular, 366 para um ano bissexto).

>[!BEGINSHADEBOX]

**Exemplos:**

* `daysInYear("2016-06-01T00:00:00.000Z")`

  Retorna 366
* `daysInYear("2015-06-01T00:00:00.000Z")`

  Retorna 365

>[!ENDSHADEBOX]


### [!UICONTROL dateMax(date1; date2; ...)]

[!BADGE Novo!]{type=Informative}

Retorna a data mais recente (mais recente) da lista.

>[!BEGINSHADEBOX]

**Exemplos:**

* `dateMax("2016-06-01T00:00:00.000Z"; "2016-12-01T00:00:00.000Z") `

  Retorna 2016-12-01T00:00:00.000Z

* `dateMax("2015-01-01T00:00:00.000Z"; "2016-06-15T00:00:00.000Z"; "2014-03-20T00:00:00.000Z")`

  Retorna 2016-06-15T00:00:00.000Z

>[!ENDSHADEBOX]


### [!UICONTROL dateMin(data1; data2; ...)]

[!BADGE Novo!]{type=Informative}

Retorna a data mais antiga da lista.

>[!BEGINSHADEBOX]

**Exemplos:**

* `dateMin("2016-06-01T00:00:00.000Z"; "2016-12-01T00:00:00.000Z")`

  Retorna 2016-06-01T00:00:00.000Z

* `dateMin("2015-01-01T00:00:00.000Z"; "2016-06-15T00:00:00.000Z"; "2014-03-20T00:00:00.000Z") `

  Retorna 2014-03-20T00:00:00.000Z

>[!ENDSHADEBOX]


### [!UICONTROL endOfMonth(data)]

[!BADGE Novo!]{type=Informative}

Retorna o último momento do mês de uma data informada — o milissegundo final do último dia (23:59:59.999). Contabiliza automaticamente o número de dias do mês, incluindo anos bissextos.

>[!BEGINSHADEBOX]

**Exemplos:**

* `endOfMonth("2016-06-15T12:30:00.000Z")`

  Retorna 30T23:59:59.999Z/2016

* `endOfMonth("2016-01-01T00:00:00.000Z")`

  Retorna 31T23:59:59.999Z de 2016

* `endOfMonth("2016-02-01T00:00:00.000Z")`

  Retorna 29/02/2016:59:59.999Z

>[!ENDSHADEBOX]


### [!UICONTROL hora(data)]

[!BADGE Novo!]{type=Informative}

Retorna a hora da data como um número entre 0 e 23.

>[!BEGINSHADEBOX]

**Exemplos:**

* `hour("2016-12-08T15:55:57.536Z")`

  Retorna 15
* `hour("2016-12-08T00:00:00.000Z")`

  Retorna 0

>[!ENDSHADEBOX]


### [!UICONTROL isWeekend(data)]

[!BADGE Novo!]{type=Informative}

Retorna `true` se a data cair em um sábado ou domingo, e `false` para qualquer outro dia. O resultado é determinado no fuso horário configurado do cenário.

>[!BEGINSHADEBOX]

**Exemplos:**

* `isWeekend("2016-12-10T00:00:00.000Z")`

  Retorna verdadeiro (sábado)

* `isWeekend("2016-12-11T00:00:00.000Z")`

  Retorna verdadeiro (domingo)

* `isWeekend("2016-12-12T00:00:00.000Z")`

  Retorna falso (segunda-feira)

* `isWeekend("2016-12-09T00:00:00.000Z")`

  Retorna falso (sexta-feira)

>[!ENDSHADEBOX]


### [!UICONTROL minuto(data)]

[!BADGE Novo!]{type=Informative}

Retorna os minutos da data como um número entre 0 e 59.

>[!BEGINSHADEBOX]

**Exemplos:**

* `minute("2016-12-08T15:55:57.536Z")`

  Retorna 55
* `minute("2016-12-08T15:00:00.000Z")`

  Retorna 0

>[!ENDSHADEBOX]


### [!UICONTROL mês(data)]

[!BADGE Novo!]{type=Informative}

Retorna o mês da data como um número entre 1 e 12.

>[!BEGINSHADEBOX]

**Exemplos:**

* `month("2016-12-08T15:55:57.536Z")`

  Retorna 12
* `month("2016-01-08T15:55:57.536Z")`

  Devoluções 1

>[!ENDSHADEBOX]


### [!UICONTROL segundo(data)]

[!BADGE Novo!]{type=Informative}

Retorna o segundo da data como um número entre 0 e 59.

>[!BEGINSHADEBOX]

**Exemplos:**

* `second("2016-12-08T15:55:57.536Z")`

  Retorna 57
* `second("2016-12-08T15:55:00.000Z")`

  Retorna 0

>[!ENDSHADEBOX]


### [!UICONTROL startOfMonth(data)]

[!BADGE Novo!]{type=Informative}

Retorna o primeiro momento do mês de uma data informada — meia-noite no primeiro dia (00:00:00.000). O resultado reconhece fusos horários.

>[!BEGINSHADEBOX]

**Exemplos:**

* `startOfMonth("2016-06-15T12:30:00.000Z")`

  Retorna 2016-06-01T00:00:00.000Z

* `startOfMonth("2024-02-14T08:00:00.000Z")`

  Retorna 2024-02-01T00:00:00.000Z

>[!ENDSHADEBOX]


### [!UICONTROL weekDayDiff(date2; date1)]

[!BADGE Novo!]{type=Informative}

Retorna o número de dias da semana entre duas datas, contabilizando os carimbos de data e hora nesses dias. Por exemplo, se a hora de início for 15h, o dia de início não será contado como um dia inteiro.

>[!BEGINSHADEBOX]

**Exemplos:**

* `weekDayDiff("2016-12-07T12:00:00.000Z"; "2016-12-05T00:00:00.000Z")`

  Retorna 2,5
* `weekDayDiff("2016-12-09T15:00:00.000Z"; "2016-12-05T15:00:00.000Z")`

  Devoluções 4

>[!ENDSHADEBOX]


### [!UICONTROL workMinutesDiff(date1; date2)]

[!BADGE Novo!]{type=Informative}

Retorna o número de minutos de trabalho agendados entre duas datas, com base em um agendamento padrão de segunda a sexta-feira, das 9h às 17h.

>[!BEGINSHADEBOX]

**Exemplos:**

* `workMinutesDiff("2016-12-05T09:00:00.000Z"; "2016-12-05T17:00:00.000Z")`

  Retorna 480
* `workMinutesDiff("2016-12-05T09:00:00.000Z"; "2016-12-06T17:00:00.000Z")`

  Retorna 960

>[!ENDSHADEBOX]


### [!UICONTROL ano(data)]

[!BADGE Novo!]{type=Informative}

Retorna o ano da data como um número de 4 dígitos.

>[!BEGINSHADEBOX]

**Exemplos:**

* `year("2016-12-08T15:55:57.536Z")`

  Devoluções em 2016
* `year("2000-01-01T00:00:00.000Z")`

  Retorna 2000

>[!ENDSHADEBOX]

### [!UICONTROL setSecond (data; número)]

Esta função retorna uma nova data com os segundos especificados em parâmetros.

Especifique um número de 0 a 59. Se o número estiver fora desse intervalo, a função retornará um segundo do minuto anterior (para um número negativo) ou do minuto subsequente (para um número positivo).

Se você precisar especificar um número fora do intervalo, recomendamos usar [!UICONTROL  addSeconds], conforme descrito acima na seção [addSeconds (date; number)](#addseconds-date-number).

>[!BEGINSHADEBOX]

**Exemplos:**

* `setSecond(2015-10-07T11:36:39.138Z;10)`

  Retorna 2015-10-07T11:36:10.138Z

* `setSecond(2015-10-07T11:36:39.138Z; 61)`

  Retorna 2015-10-07T11:37:01.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setMinute (data; número)]

Esta função retorna uma nova data com os minutos especificados em parâmetros.

Especifique um número de 0 a 59. Se o número estiver fora desse intervalo, a função retornará um minuto da hora anterior (para um número negativo) ou da hora subsequente (para um número positivo).

Se você precisar especificar um número fora do intervalo, recomendamos usar addMinutes, conforme descrito acima em [addMinutes (date; number)](#addminutes-date-number).

>[!BEGINSHADEBOX]

**Exemplos:**

* `setMinute(2015-10-07T11:36:39.138Z;10)`

  Retorna 2015-10-07T11:10:39.138Z

* `setMinute(2015-10-07T11:36:39.138Z;61)`

  Retorna 2015-10-07T12:01:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setHour (data; número)]

Esta função retorna uma nova data com a hora especificada nos parâmetros.

Especifique um número de 0 a 23. Se o número estiver fora desse intervalo, a função retornará uma hora do dia anterior (para um número negativo) ou do dia subsequente (para um número positivo).

Se você precisar especificar um número fora do intervalo, recomendamos usar addHours, conforme descrito acima em [addHours (date; number)](#addhours-date-number).

>[!BEGINSHADEBOX]

**Exemplos:**

* `setHour(2015-08-07T11:36:39.138Z;6)`

  Retorna 2015-08-07T06:36:39.138Z

* `setHour(2015-08-07T11:36:39.138;-6)`

  Retorna 2015-08-06T18:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setDay (data; número/nome do dia em inglês)]

Esta função retorna uma nova data com o dia especificado nos parâmetros.

Você pode usar essa função para definir o dia da semana, com Domingo como 1 e Sábado como 7. Se você especificar um número de 1 a 7, a data resultante estará na semana atual (de domingo a sábado). Se o número estiver fora desse intervalo, a função retornará um dia da semana anterior (para um número negativo) ou da semana subsequente (para um número positivo).

Se você precisar especificar um número fora do intervalo, recomendamos usar addDays, conforme descrito acima em [addDays (date; number)](#adddays-date-number).

>[!BEGINSHADEBOX]

**Exemplos:**

* `setDay(2018-06-27T11:36:39.138Z;Monday)`

  Retorna 25T11:36:39.138Z/2018

* `setDay(2018-06-27T11:36:39.138Z;1)`

  Retorna 24/06/2018:36:39.138Z

* `setDay(2018-06-27T11:36:39.138Z;7)`

  Retorna 30T11:36:39.138Z/2018

>[!ENDSHADEBOX]

### [!UICONTROL setDate (data; número)]

Esta função retorna uma nova data com o dia do mês especificado em parâmetros.

Especifique um número de 1 a 31. Se o número estiver fora desse intervalo, a função retornará um dia do mês anterior (para um número negativo) ou do mês seguinte (para um número positivo).

>[!BEGINSHADEBOX]

**Exemplos:**

* `setDate(2015-08-07T11:36:39.138Z;5)`

  Retorna 2015-08-05T11:36:39.138Z

* `setDate(2015-08-07T11:36:39.138Z;32)`

  Retorna 2015-09-01T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setMonth (data; número/nome do mês em inglês)]

Esta função retorna uma nova data com o mês especificado em parâmetros.

Especifique um número de 1 a 12. Se o número estiver fora desse intervalo, a função retornará o mês do ano anterior (para um número negativo) ou o ano subsequente (para um número positivo).

>[!BEGINSHADEBOX]

**Exemplos:**

* `setMonth(2015-08-07T11:36:39.138Z;5)`

  Retorna 2015-05-07T11:36:39.138Z

* `setMonth(2015-08-07T11:36:39.138Z;17)`

  Retorna 2016-05-07T11:36:39.138Z

* `setMonth(2015-08-07T11:36:39.138Z;january)`

  Retorna 2015-01-07T12:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setYear (data; número)]

Retorna uma nova data com o ano especificado em parâmetros.

>[!BEGINSHADEBOX]

**Exemplo:**

* `setYear(2015-08-07T11:36:39.138Z;2017)`

  Retorna 2017-08-07T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL formatDate (data; formato; [fuso horário])]

Use esta função quando tiver um valor Date, como `12-10-2021 20:30`, que você deseja formatar como um valor Text, como `Dec 10, 2021 8:30 PM`.

Isso é útil, por exemplo, quando é necessário alterar o formato de data de um aplicativo ou serviço da Web para o de um aplicativo ou serviço da Web conectado no mesmo cenário.

Para obter mais informações, consulte Data e Texto no artigo [Tipos de dados do item](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

#### Parâmetros

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Parâmetro</th> 
   <th>Tipo de dados esperado* </th> 
   <th>O que faz</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL data] </td> 
   <td>Data </td> 
   <td> <p>Converte um valor Date em um valor Text. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL formato] </td> 
   <td>Texto </td> 
   <td> <p>Permite especificar um formato usando tokens de formatação de data/hora. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">Tokens para formatação de data e hora</a>.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL fuso horário] </td> 
   <td>Texto </td> 
   <td> <p>(Opcional) Permite especificar o fuso horário usado para a conversão. </p> <p>Para obter a lista de fusos horários reconhecidos, consulte a coluna "TZ database name" na Wikipédia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">List of tz database time zones</a>. Somente os valores listados nesta coluna são reconhecidos pela função como um fuso horário válido. Qualquer outro valor é ignorado e o fuso horário de Cenários especificado em seu Perfil é usado. </p> <p>Se você omitir esse parâmetro, o fuso horário de Cenários especificado nas configurações de Perfil será aplicado. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span><code>Europe/Prague</code>, <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

Se um tipo diferente for fornecido, a coerção de tipo será aplicada. Para obter mais informações, consulte [Coerção de tipo](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

#### Valor e tipo de retorno

A função `formatDate` retorna uma representação de texto do valor de Data especificado de acordo com o formato e o fuso horário especificados. O tipo de dados é Texto.

>[!BEGINSHADEBOX]

**Exemplos:** O Cenário e o fuso horário da Web foram definidos como `Europe/Prague` nesses exemplos.

![Exemplo de função de data e hora](assets/date-time-functions-examples-350x61.png)

* `formatDate(1. Date created;MM/DD/YYYY)`

  Devoluções em 01/10/2018

* `formatDate(1. Date created; YYYY-MM-DD hh:mm A)`

  Retorna 01/10/2018 9:32 AM

* `formatDate(1. Date created;DD.MM.YYYY HH:mm;UTC)`

  Retorna 01.10.2018 07:32

* `formatDate(now;DD.MM.YYYY HH:mm)`

  Retorna 19.03.2019 15:30

>[!ENDSHADEBOX]

### [!UICONTROL parseDate (texto; formato; [fuso horário])]

Use esta função quando tiver um valor de Texto representando uma data (como `12-10-2019 20:30` ou `Aug 18, 2019 10:00 AM`) e quiser convertê-lo (analisar) em um valor de Data (uma representação binária legível por máquina). Para obter mais informações, consulte Data e Texto no artigo [Tipos de dados do item](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

#### Parâmetros

A segunda coluna indica o tipo esperado. Se um tipo diferente for fornecido, a coerção de tipo será aplicada. Para obter mais informações, consulte [Coerção de tipo](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Parâmetro</th> 
   <th>Tipo de dados esperado* </th> 
   <th>O que faz</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL texto] </td> 
   <td>Texto </td> 
   <td> <p>Converte um valor Date em um valor Text. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL formato] </td> 
   <td>Texto </td> 
   <td> <p>Permite especificar um formato usando tokens de formatação de data/hora. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">Tokens para formatação de data e hora</a>.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL fuso horário] </td> 
   <td>Texto </td> 
   <td> <p>(Opcional) Permite especificar o fuso horário usado para a conversão. </p> <p>Para obter a lista de fusos horários reconhecidos, consulte a coluna "TZ database name" na Wikipédia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">List of tz database time zones</a>. Somente os valores listados nesta coluna são reconhecidos pela função como um fuso horário válido. Qualquer outro valor é ignorado e o fuso horário de Cenários especificado em seu Perfil é usado. </p> <p>Se você omitir esse parâmetro, o fuso horário de Cenários especificado nas configurações de Perfil será aplicado.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span><code>Europe/Prague</code>, <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

Se um tipo diferente for fornecido, a coerção de tipo será aplicada. Para obter mais informações, consulte [Coerção de tipo](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

#### Valor e tipo de retorno

Essa função converte uma sequência de caracteres de texto em uma data, de acordo com o formato e o fuso horário especificados. O tipo de dados do valor é Data.

>[!BEGINSHADEBOX]

**Exemplos:** Nos exemplos a seguir, o valor de Data retornado é expresso de acordo com a ISO 8601, mas o tipo de dados do resultado é Data.

* `parseDate(2016-12-28;YYYY-MM-DD)`

  Retorna 2016-12-28T00:00:00.000Z

* `parseDate(2016-12-28 16:03;YYYY-MM-DD HH:mm)`

  Retorna 2016-12-28T16:03:00.000Z

* `parseDate(2016-12-28 04:03 pm; YYYY-MM-DD hh:mm a)`

  Retorna 2016-12-28T16:03:06.000Z

* `parseDate(1482940986;X)`

  Retorna 2016-12-28T16:03:06.000Z

>[!ENDSHADEBOX]

### [!UICONTROL diferençaData (Data1; Data2; Unidade)]

Retorna um número que representa a diferença nas duas datas, expressas na unidade especificada.

A Data2 é subtraída da Data1.

Use um dos seguintes valores de tempo para o parâmetro `unit`:

* milissegundos
* segundos
* minutos
* horas
* dias
* semanas
* meses

Se nenhuma unidade for especificada, a função retornará a diferença em milissegundos.

>[!BEGINSHADEBOX]

**Exemplos:**

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z)`

  Retorna `600,000`

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;hours)`

  Retorna `4`

* `dateDifference2021-06-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;months)`

  Retorna `1`

>[!ENDSHADEBOX]

### Exemplos adicionais

#### Como calcular o n-ésimo dia da semana no mês

Esta seção é adaptada para o Workfront Fusion a partir da página da Web [!DNL Exceljet], que explica como obter o enésimo dia da semana em um mês.

Se você precisar calcular uma data correspondente ao n-ésimo dia da semana no mês (por exemplo, primeira terça-feira, terceira sexta-feira e assim por diante), poderá usar a seguinte fórmula:

![Calcular dia n](assets/date-time-functions-calc-nth-day-350x31.png)


```
{{addDays(setDate(1.date; 1); 1.n * 7 - formatDate(addDays(setDate(1.date; 1); "-" + 1.dow); "E"))}}
```

A fórmula contém os seguintes itens:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>1.n</code> </td> 
   <td> <p> Dia n:</p> 
    <ul> 
     <li><code>1</code> para 1ª terça-feira</li> 
     <li><code>2</code> para a 2ª terça-feira</li> 
     <li><code>3</code> para a 3ª terça-feira e assim por diante</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>2.dow</code> </td> 
   <td> <p> dia da semana:</p> 
    <ul> 
     <li><code>1</code> para segunda-feira</li> 
     <li><code>2</code> para terça-feira</li> 
     <li><code>3</code> para quarta-feira</li> 
     <li><code>4</code> para quinta-feira</li> 
     <li><code>5</code> para sexta-feira</li> 
     <li><code>6</code> para sábado</li> 
     <li><code>7</code> para domingo</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>1.date</code> </td> 
   <td> <p> A data determina o mês. Para calcular o dia n da semana no mês atual, use a variável <code>now</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

Caso queira calcular apenas um caso específico, por exemplo, a cada segunda quarta-feira, você pode substituir os itens `1.n` e `2.dow` na fórmula por números correspondentes. Para a segunda quarta-feira do mês atual, você usaria os seguintes valores:

* `1.n` = `2`
* `1.dow` = `3`
* `1.date` = `now`

![Valor da variável de dia ](assets/nth-day-variable-value-350x33.png)

#### Explicação:

* `setDate(now;1)` retorna o primeiro dia do mês atual
* `formatDate(....;E)` retorna o dia da semana (1, 2, ... 6)

### Como calcular dias entre datas

Uma possibilidade é empregar a seguinte expressão:

![Calcular dias entre datas](assets/calculate-days-between-dates-350x68.png)


```
{{round((2.value - 1.value) / 1000 / 60 / 60 / 24)}}
```

>[!NOTE]
>
>* Os valores de `D1` e `D2` devem ser valores do tipo Data. Se forem valores do tipo String (por exemplo, 20.10.2018), use a função `parseDate()` para convertê-los em valores do tipo Date.
>
>* A função `round()` é usada para casos em que uma das datas está dentro do período de horário de verão e a outra não. Nesses casos, a diferença em horas é de uma hora a menos ou mais. Você pode dividi-la por 24 para um resultado não inteiro. Você perde uma hora de verão. Arredondar nivela para que você não tenha uma porcentagem

#### Como calcular o último dia/milissegundo do mês

Ao especificar um intervalo de datas, por exemplo, em um módulo de pesquisa, se o intervalo abranger todo o mês anterior como um intervalo fechado (o intervalo que inclui ambos os pontos de limite), será necessário calcular o último dia do mês.

2019-09-01 ≤ D ≤ 2019-09-30

A fórmula abaixo mostra uma maneira de calcular o último dia do mês anterior:

![Último dia do mês anterior](assets/last-day-prev-month.png)


```
{{addDays(setDate(now; 1); -1)}}
```

Em alguns casos, é necessário calcular não apenas o último dia do mês, mas literalmente seu último milissegundo:

2019-09-01T00:00:00.000Z ≤ D ≤ 2019-09-30T23:59:59.999Z

Esta fórmula mostra uma maneira de calcular o último milissegundo do mês anterior:

![Último milissegundo do mês anterior](assets/last-millisecond-prev-month-350x45.png)


```
{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD"; "UTC") - 1; "x")}}
```

Se precisar que o resultado use a configuração de fuso horário, omita o argumento UTC:

![Omitir UTC](assets/omit-utc-argument-350x45.png)

`{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD") - 1; "x")}}`

No entanto, é preferível usar o intervalo de meia abertura (o intervalo que exclui um de seus pontos de limite), especificando o primeiro dia do mês seguinte e substituindo o operador &quot;less or equal than&quot; por &quot;less than&quot;, da seguinte maneira:

`2019-09-01 ≤ D < 2019-10-01`

`2019-09-01T00:00:00.000Z ≤ D < 2019-10-01T00:00:00.000Z`
