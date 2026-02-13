---
title: Módulo agregador
description: Um módulo agregador é um tipo de módulo projetado para unir vários pacotes de dados em um único pacote.
author: Becky
feature: Workfront Fusion
exl-id: 93cde0d0-4013-463a-b19c-d58180632739
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 11%

---

# Módulo [!UICONTROL Agregador]

Um módulo agregador é um módulo que mescla vários pacotes de dados em um único pacote.

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

## Visão geral do módulo [!UICONTROL Agregador]

Quando um módulo [!UICONTROL Aggregator] é executado, ele faz o seguinte:

* Acumula todos os pacotes da operação de um único módulo de origem.
* Gera um único pacote com uma matriz contendo um item por pacote acumulado. O conteúdo dos itens da matriz depende do módulo [!UICONTROL Aggregator] específico e de sua configuração.

A imagem a seguir mostra uma configuração típica do módulo [!UICONTROL Agregador]:

![Agregador de matriz](assets/array-aggregator.png)

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Módulo Source]</p> </td> 
   <td> <p>O módulo onde a agregação do pacote começa. O módulo de origem geralmente é um iterador ou um módulo de pesquisa que gera uma série de pacotes.</p><p>Quando você configura o módulo de origem do agregador (e fecha a configuração do agregador), a rota entre o módulo de origem e o módulo do agregador é colocada em uma área cinza, para que você possa ver claramente o início e o fim da agregação. 
   </p> <p>Para obter mais informações sobre iteradores, consulte módulo <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL Iterator]</a>.</p> 
   <p>Para obter mais informações sobre módulos de pesquisa, consulte <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#search-modules" class="MCXref xref">Módulos de pesquisa</a> na visão geral do Módulo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo de estrutura de destino]</p><p>(Aplicável somente ao módulo [!UICONTROL Array aggregator].)</p> </td> 
   <td> <p> A estrutura de público-alvo onde os dados são agregados. A opção padrão, [!UICONTROL Personalizado], permite que você escolha itens que devem ser agregados no <code>Array </code>item do pacote de saída do [!UICONTROL Array aggregator]:</p> <p> <img src="assets/output-bundle-array-item.png"> </p> <p>Depois de conectar mais módulos após o módulo [!UICONTROL Array aggregator] e retornar à configuração do módulo agregador, o menu suspenso do tipo de estrutura [!UICONTROL Target] conterá todos os módulos a seguir e seus campos que são do tipo "Matriz de Coleções". <p>Neste exemplo, o campo [!UICONTROL Attachments] do módulo [!DNL Slack] &gt;[!UICONTROL Create a Message] aparece no campo de tipo Array aggregator &gt; Target structure. </p> <p> <img src="assets/array-aggregator-slack.png"> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campos Agregados]</td> 
   <td>Os campos que você deseja incluir na saída do módulo agregador.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Agrupar por]</p> </td> 
   <td> <p>Usando o campo Agrupar por, você pode definir uma expressão contendo um ou mais itens mapeados. Os dados agregados serão separados em Grupos pelo valor da expressão. Cada Grupo gera um pacote separado, contendo uma Chave e uma matriz de dados. Ao agrupar os resultados, é possível usar a tecla como um filtro nos módulos subsequentes.</p>
   <p>Cada pacote contém dois itens:</p> 
    <ul> 
     <li><code>Key</code>: o valor pelo qual você está agrupando.</li> 
     <li><code>Array</code>: os dados agregados dos pacotes para os quais a fórmula avaliou para o valor <code>Key</code>.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>Parar o processamento após uma agregação vazia</p> </td> 
   <td> <p>Por padrão, o módulo [!UICONTROL Aggregator] gera o resultado da agregação mesmo quando nenhum pacote atinge o módulo [!UICONTROL Aggregator] (por exemplo, porque todos foram filtrados para fora do caminho que inclui o agregador). Se a opção [!UICONTROL Parar processamento após uma agregação vazia] estiver habilitada, o módulo [!UICONTROL Aggregator] não produzirá nenhum conjunto de saída quando não houver conjuntos de entrada. Em vez disso, o fluxo pára.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Os pacotes gerados pelos módulos entre o módulo de origem e o módulo [!UICONTROL Agregador] não são gerados pelo módulo [!UICONTROL Agregador]. Esses pacotes não são acessíveis pelos módulos no fluxo após o [!UICONTROL Agregador]. Se você precisar de dados de um pacote emitido por um módulo entre o módulo de origem e o módulo [!UICONTROL Agregador], inclua o item fornecido na configuração do módulo [!UICONTROL Agregador] (como no campo [!UICONTROL Campos agregados] da configuração do módulo [!UICONTROL Agregador de matrizes]).


## Exemplo de cenário de como os agregadores funcionam

Este exemplo de cenário mostra como compactar todos os anexos de email e fazer upload do ZIP para [!DNL Dropbox].

![exemplo de arquivamento do Dropbox](assets/dropbox-archive.png)

O cenário abaixo mostra como:

* O primeiro módulo observa uma caixa de entrada para emails recebidos. O disparador do [!UICONTROL Email] >[!UICONTROL Assistir emails] gera um pacote com o item `Attachments[]`, que é uma matriz que contém todos os anexos de email.

* O segundo modelo repete os anexos do email: [!UICONTROL Email] >[!UICONTROL Iterar anexos] O iterador pega os itens da matriz `Attachments[]` um por um e os envia como pacotes separados.

* O terceiro módulo é o agregador. Ele agrega os pacotes gerados pelo módulo [!UICONTROL Email] >[!UICONTROL Iterar anexos]. [!UICONTROL Arquivar] >[!UICONTROL Criar um agregador de arquivamento] acumula todos os pacotes que recebe e gera um único pacote contendo o arquivo ZIP.

* O último módulo carrega o arquivo ZIP resultante para [!DNL Dropbox].  [!DNL Dropbox] > [!UICONTROL Carregar um arquivo] obtém o arquivo ZIP do [!UICONTROL Arquivo morto] > [!UICONTROL Criar um arquivo morto] e o carrega no [!DNL Dropbox].



Abaixo está uma configuração de exemplo do agregador [!UICONTROL Arquivo] > [!UICONTROL Criar um arquivo]:

![Criar um arquivo morto](assets/archive-create-an-archive.png)
