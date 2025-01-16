---
title: Módulo agregador
description: Um módulo agregador é um tipo de módulo projetado para unir vários pacotes de dados em um único pacote.
author: Becky
feature: Workfront Fusion
exl-id: 93cde0d0-4013-463a-b19c-d58180632739
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Módulo [!UICONTROL Aggregator]

Um módulo agregador é um módulo que mescla vários pacotes de dados em um único pacote.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] pacote</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença</td> 
   <td> Novo: Padrão<p>Ou</p><p>Atual: trabalho ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licença</td> 
   <td>
   <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou plano do [!UICONTROL Prime] [!DNL Workfront]: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plano: [!DNL Workfront Fusion] está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>


Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre as licenças do Adobe Workfront Fusion, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Visão geral do módulo [!UICONTROL Aggregator]

Quando um módulo [!UICONTROL Aggregator] é executado, ele faz o seguinte:

* Acumula todos os pacotes da operação de um único módulo de origem.
* Gera um único pacote com uma matriz contendo um item por pacote acumulado. O conteúdo dos itens da matriz depende do módulo [!UICONTROL Aggregator] específico e de sua configuração.

A imagem a seguir mostra uma configuração típica do módulo [!UICONTROL Aggregator]:

![](assets/array-aggregator.png)

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source Module]</p> </td> 
   <td> <p>O módulo onde a agregação do pacote começa. O módulo de origem geralmente é um iterador ou um módulo de pesquisa que gera uma série de pacotes.</p><p>Quando você configura o módulo de origem do agregador (e fecha a configuração do agregador), a rota entre o módulo de origem e o módulo do agregador é colocada em uma área cinza, para que você possa ver claramente o início e o fim da agregação. 
   </p> <p>Para obter mais informações sobre iteradores, consulte <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL Iterator] módulo</a>.</p> 
   <p>Para obter mais informações sobre módulos de pesquisa, consulte <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#search-modules" class="MCXref xref">Módulos de pesquisa</a> na visão geral do Módulo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Target structure type]</p><p>(Aplicável somente para o módulo [!UICONTROL Array aggregator].)</p> </td> 
   <td> <p> A estrutura de público-alvo onde os dados são agregados. A opção padrão, [!UICONTROL Custom], permite que você escolha itens que devem ser agregados no <code>Array </code> item do pacote de saída de [!UICONTROL Array aggregator]:</p> <p> <img src="assets/output-bundle-array-item.png"> </p> <p>Depois de conectar mais módulos após o módulo [!UICONTROL Array aggregator] e retornar à configuração do módulo agregador, o menu suspenso do tipo de estrutura [!UICONTROL Target] contém todos os módulos a seguir e seus campos que são do tipo "Matriz de Coleções". <p>Neste exemplo, o campo [!UICONTROL Attachments] do módulo [!DNL Slack] &gt;[!UICONTROL Create a Message] aparece no campo de tipo de estrutura Array aggregator &gt; Target. </p> <p> <img src="assets/array-aggregator-slack.png"> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aggregated fields]</td> 
   <td>Os campos que você deseja incluir na saída do módulo agregador.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>Usando o campo Agrupar por, você pode definir uma expressão contendo um ou mais itens mapeados. Os dados agregados serão separados em Grupos pelo valor da expressão. Cada Grupo gera um pacote separado, contendo uma Chave e uma matriz de dados. Ao agrupar os resultados, é possível usar a tecla como um filtro nos módulos subsequentes.</p>
   <p>Cada pacote contém dois itens:</p> 
    <ul> 
     <li><code>Key</code>: o valor pelo qual você está agrupando.</li> 
     <li><code>Array</code>: os dados agregados dos pacotes para os quais a fórmula avaliou para o valor <code>Key</code>.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>Parar o processamento após uma agregação vazia</p> </td> 
   <td> <p>Por padrão, o módulo [!UICONTROL Aggregator] gera o resultado da agregação mesmo quando nenhum pacote atinge o módulo [!UICONTROL Aggregator] (por exemplo, porque todos foram filtrados para fora do caminho que inclui o agregador). Se a opção [!UICONTROL Stop processing after an empty aggregation] estiver habilitada, o módulo [!UICONTROL Aggregator] não produzirá nenhum pacote de saída quando não houver nenhum pacote de entrada. Em vez disso, o fluxo pára.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Os pacotes gerados pelos módulos entre o módulo de origem e o módulo [!UICONTROL Aggregator] não são gerados pelo módulo [!UICONTROL Aggregator]. Esses pacotes não são acessíveis pelos módulos no fluxo após o [!UICONTROL Aggregator]. Se você precisar de dados de um pacote emitido por um módulo entre o módulo de origem e o módulo [!UICONTROL Aggregator], certifique-se de incluir o item fornecido na configuração do módulo [!UICONTROL Aggregator] (como no campo [!UICONTROL Aggregated fields] na configuração do módulo [!UICONTROL Array aggregator]).


## Exemplo de cenário de como os agregadores funcionam

Este exemplo de cenário mostra como compactar todos os anexos de email e fazer upload do ZIP para [!DNL Dropbox].

![](assets/dropbox-archive.png)

O cenário abaixo mostra como:

* O primeiro módulo observa uma caixa de entrada para emails recebidos. O gatilho [!UICONTROL Email] >[!UICONTROL Watch emails] gera um conjunto com o item `Attachments[]`, que é uma matriz que contém todos os anexos de email.

* O segundo modelo repete os anexos do email: o iterador [!UICONTROL Email] >[!UICONTROL Iterate attachments] pega os itens da matriz `Attachments[]` um por um e os envia como pacotes separados.

* O terceiro módulo é o agregador. Ele agrega os pacotes gerados pelo módulo [!UICONTROL Email] >[!UICONTROL Iterate attachments]. [!UICONTROL Archive] >[!UICONTROL Create an archive aggregator] acumula todos os pacotes que recebe e gera um único pacote contendo o arquivo ZIP.

* O último módulo carrega o arquivo ZIP resultante para [!DNL Dropbox].  [!DNL Dropbox] > [!UICONTROL Upload a file] obtém o arquivo ZIP do módulo [!UICONTROL Archive] > [!UICONTROL Create an archive] e faz o upload para [!DNL Dropbox].



Abaixo está uma configuração de exemplo do agregador [!UICONTROL Archive] > [!UICONTROL Create an archive]:

![](assets/archive-create-an-archive.png)
