---
title: Visão geral do mapeamento
description: Mapeamento é o processo de atribuir as saídas de um módulo, estruturadas em itens, aos campos de entrada de outro módulo.
author: Becky
feature: Workfront Fusion
exl-id: 9208ce20-0757-427a-9669-ce4274d05522
source-git-commit: 88147d0305595e1d0d388f510ed43fc5beaa4b64
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 96%

---

# Visão geral do mapeamento

Mapeamento é o processo de atribuir as saídas de um módulo aos campos de entrada de outro módulo.

A operação de um módulo gera zero, um ou mais pacotes como sua saída. Um pacote consiste em um ou mais itens.

Você pode mapear esses itens para campos em módulos posteriores.

Ao clicar em um campo no qual você pode inserir um valor obtido de um módulo anterior em um cenário, o painel de mapeamento é exibido. Aqui, você pode selecionar o item que deseja mapear. Um mapeamento pode incluir:

* Um único item
* Vários itens
* Texto estático
* Funções

>[!BEGINSHADEBOX]

**Exemplos**:

Item único

![Mapear item único](assets/map-single.png)

Vários itens com texto

![Mapear vários itens](assets/map-multiple-with-text.png)

Função com vários itens e texto

![Mapear fórmula com texto](assets/map-formula-with-text.png)


>[!ENDSHADEBOX]


Para obter instruções sobre mapeamento, consulte os artigos em [Mapear dados: índice do artigo](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

>[!NOTE]
>
>As saídas dos módulos envolvidos entre um [!UICONTROL Iterador] e um [!UICONTROL Agregador] não estão acessíveis além do módulo [!UICONTROL Agregador].

## O painel de mapeamento

Ao clicar em um campo no qual você pode mapear dados, o painel de mapeamento é aberto.

A primeira guia ![Mapear de outros módulos](assets/toolbar-icon-functions-you-map-from-other-modules.png) exibe os itens que você pode mapear de outros módulos.

As outras guias incluem funções, operadores e palavras-chave que podem ser usadas para criar fórmulas. Elas são classificadas em guias diferentes, com base no tipo de dados que manipulam.

![Painel de mapeamento](assets/mapping-panel-blank.png)


Para obter mais informações sobre guias de função, consulte [Visão geral da função](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

Para obter mais informações sobre como mapear itens usando funções, consulte [Mapear itens usando funções integradas](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

## Coleções

Os itens podem conter vários valores de vários tipos. São itens do tipo coleção.

Os pacotes do tipo coleção exibem `(Collection)` ao lado do rótulo do pacote na saída do módulo.

![Coleção](assets/collection.png)

Na maioria dos casos, você mapeia os elementos da coleção, em vez de mapear o item que representa a coleção inteira.

Para localizar o elemento de uma coleção no painel de mapeamento, clique na seta ao lado da coleção.

![Lista suspensa Coleção](assets/collection-dropdown.png)

Para obter mais informações sobre coleções, consulte [Tipos de dados de item](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

Para obter instruções sobre como mapear coleções, consulte [Mapear um item](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md#map-an-item) no artigo Mapear informações de um módulo para outro.

## Matrizes

Os itens podem conter vários valores do mesmo tipo. Esses itens são do tipo matriz.

Pacotes do tipo matriz exibem `(Array)` ao lado do rótulo do pacote na saída do módulo.

No painel de mapeamento, as matrizes são exibidas com colchetes. Você pode identificar um item do tipo matriz pelos colchetes no final do rótulo do item. Para localizar um elemento de matriz específico no painel de mapeamento, clique na seta ao lado da matriz.

![Matriz](assets/array.png)

Para obter informações e instruções sobre como mapear matrizes e elementos de matriz, consulte [Mapear matrizes e elementos de matriz](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
