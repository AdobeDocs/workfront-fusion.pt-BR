---
title: Controle de fluxo
description: Ao criar ou editar um cenário, você pode definir configurações para controlar como os dados fluem por ele.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: ce2f13866fef97b5687991dfcf5d9579a5e539e4
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Controle de fluxo

Ao criar ou editar um cenário, você pode definir configurações para controlar como os dados fluem por ele.

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
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho, [!UICONTROL [!DNL Workfront Fusion] para Automação do Trabalho</p>
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

## Repetidor

Você pode usar um módulo [!UICONTROL Repeater] para repetir uma tarefa um determinado número de vezes. Um módulo [!UICONTROL Repeater] gera pacotes, um após o outro.

Por exemplo, você pode usar um módulo [!UICONTROL Repeater] para enviar cinco emails com os assuntos &quot;Olá 1&quot;, &quot;Olá 2&quot; e assim por diante, conectando o módulo **[!UICONTROL Email]>[!UICONTROL Send me an email]** ao módulo [!UICONTROL Repeater].

Para usar um módulo [!UICONTROL Repeater]:

1. Clique no ícone [!UICONTROL Flow Control] ![](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif), na parte inferior da tela, e clique em **[!UICONTROL Repeater]**, no menu exibido.
1. Clique no pacote [!UICONTROL Repeater] e, em seguida, clique em **[!UICONTROL Connect automatically]** na caixa que é exibida.
1. Na caixa [!UICONTROL Flow Control] exibida, digite o número de repetições (pacotes de saída) desejadas na caixa **[!UICONTROL Repeats]**.

   Em nosso exemplo de email, você digitaria 5.

   ![](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   O valor do item aumenta em cada repetição por este valor especificado no campo **[!UICONTROL Step]**, que pode ser visualizado ao selecionar **[!UICONTROL Show advanced settings]**. Esse número é 1 por padrão.

1. Clique em **[!UICONTROL OK]** para fechar a caixa **[!UICONTROL Flow Control]**.

1. Clique no módulo de aplicativo ou serviço conectado ao módulo [!UICONTROL Repeater].
1. Na caixa exibida, digite as informações que deseja repetir.

   No nosso exemplo de email, você digitaria Olá na caixa [!UICONTROL Subject] e mapearia `i` do módulo do repetidor.

   ![](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)

| Item | Descrição |
|---|---|
| [!UICONTROL Initial value] | Insira ou mapeie o número que você deseja que o módulo defina como `i` na primeira iteração. O valor padrão é 1. |
| [!UICONTROL Repeats] | Insira ou mapeie o número de vezes que você deseja que o módulo se repita. Esse número deve ser maior ou igual a 0 e menor ou igual a 10.000. |
| [!UICONTROL Step] | Este é o número pelo qual o módulo aumenta o valor de `i`. O valor padrão é 1. |

{style="table-layout:auto"}

>[!NOTE]
>
>O número de repetições não é determinado pelo valor de `i`, pois estaria em um loop na programação. O módulo repetirá o número de vezes indicado no campo [!UICONTROL Repeats]. O valor `i` é alterado com cada iteração do módulo [!DNL repeater] e pode ser mapeado para módulos posteriores. O exemplo acima mapeia o valor de `i` na mensagem Hello, resultando em mensagens que leem &quot;Hello 1,&quot; Hello 2 e assim por diante.

## [!UICONTROL Iterator]

Um [!UICONTROL Iterator] é um tipo especial de módulo que converte uma matriz em uma série de pacotes. Cada item de matriz será um conjunto separado na saída do módulo [!UICONTROL Iterator]. Para obter mais informações, consulte [Módulo Iterador](/help/workfront-fusion/references/modules/iterator-module.md).

## Agregador de matrizes

Um agregador de matriz é um tipo especial de módulo que permite mesclar vários pacotes em um único pacote. Para obter mais informações, consulte [Módulo agregador](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

O módulo [!UICONTROL Router] permite ramificar seu fluxo em várias rotas e processar os dados em cada rota de forma diferente. Depois que um módulo [!UICONTROL Router] recebe um pacote, ele o encaminha para cada rota conectada na ordem em que as rotas foram anexadas ao módulo [!UICONTROL Router]. Para obter mais informações, consulte [Módulo de roteador em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

<!--
<div>
<h2>Directives</h2>
<p>The error handling directives allow you to control how your scenario reacts to errors. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md" class="MCXref xref">Advanced error handling in Adobe Workfront Fusion</a> and <a href="/help/workfront-fusion/references/errors/directives-for-error-handling.md" class="MCXref xref">Directives for error handling in Adobe Workfront Fusion</a>.</p>
</div>
-->
