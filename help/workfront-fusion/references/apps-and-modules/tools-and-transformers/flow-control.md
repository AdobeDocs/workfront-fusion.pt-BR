---
title: Controle de fluxo
description: Ao criar ou editar um cenário, você pode definir configurações para controlar como os dados fluem por ele.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 5a95b2c191d4e6d8750dc57a47923f416612b4a9
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Controle de fluxo

Ao criar ou editar um cenário, você pode definir configurações para controlar como os dados fluem por ele.

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
   <p>Nenhum requisito de licença do Workfront Fusion.</p>
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

## Repetidor

Você pode usar um módulo [!UICONTROL Repeater] para repetir uma tarefa um determinado número de vezes. Um módulo [!UICONTROL Repeater] gera pacotes, um após o outro.


<table>
    <tr>
        <td>[!UICONTROL Initial value]</td>
        <td>Insira ou mapeie o valor que você deseja que o módulo tenha na primeira iteração. O valor padrão é 1.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Repeats]</td>
        <td>Insira ou mapeie o número de vezes que você deseja que o módulo se repita. Esse número deve ser maior ou igual a 0 e menor ou igual a 10.000.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Step]</td>
        <td>Este é o número pelo qual o módulo aumenta o valor. O valor padrão é 1.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

Por exemplo, você pode usar um módulo [!UICONTROL Repeater] para enviar cinco emails com os assuntos &quot;Olá 1&quot;, &quot;Olá 2&quot; e assim por diante, conectando o módulo **[!UICONTROL Email]>[!UICONTROL Send me an email]** ao módulo [!UICONTROL Repeater].

1. Clique no ícone [!UICONTROL Flow Control] ![Ícone de Controle de fluxo](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif), na parte inferior da tela, e clique em **[!UICONTROL Repeater]**, no menu exibido.
1. Clique no módulo [!UICONTROL Repeater] e, em seguida, clique em **[!UICONTROL Connect automatically]** na caixa que é exibida.

   O módulo Repetidor se abre.

1. No campo **[!UICONTROL Repeats]**, insira o número de repetições (pacotes de saída) que o módulo deverá produzir.

   Neste exemplo, você digitaria 5.

   ![Repetidor](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   O valor do item aumenta em cada repetição por este valor especificado no campo **[!UICONTROL Step]**, que pode ser visualizado ao selecionar **[!UICONTROL Show advanced settings]**. Esse número é 1 por padrão.

1. Clique em **[!UICONTROL OK]** para fechar a caixa **[!UICONTROL Flow Control]**.

1. Clique no módulo de aplicativo ou serviço conectado ao módulo [!UICONTROL Repeater].
1. Na caixa exibida, digite as informações que deseja repetir.

   No nosso exemplo de email, você digitaria Olá na caixa [!UICONTROL Subject] e mapearia `i` do módulo do repetidor.

   ![Repetidor](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>O número de repetições não é determinado pelo valor de `i`, pois estaria em um loop na programação. O módulo repetirá o número de vezes indicado no campo [!UICONTROL Repeats]. O valor `i` é alterado com cada iteração do módulo [!DNL repeater] e pode ser mapeado para módulos posteriores. O exemplo acima mapeia o valor de `i` na mensagem Hello, resultando em mensagens que leem &quot;Hello 1,&quot; Hello 2 e assim por diante.

>[!ENDSHADEBOX]

## [!UICONTROL Iterator]

Um [!UICONTROL Iterator] é um tipo especial de módulo que converte uma matriz em uma série de pacotes. Cada item de matriz será um conjunto separado na saída do módulo [!UICONTROL Iterator]. Para obter mais informações, consulte [Módulo Iterador](/help/workfront-fusion/references/modules/iterator-module.md).

## Agregador de matrizes

Um agregador de matriz é um tipo especial de módulo que permite mesclar vários pacotes em um único pacote. Para obter mais informações, consulte [Módulo agregador](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

O módulo [!UICONTROL Router] permite ramificar seu fluxo em várias rotas e processar os dados em cada rota de forma diferente. Depois que um módulo [!UICONTROL Router] recebe um pacote, ele o encaminha para cada rota conectada na ordem em que as rotas foram anexadas ao módulo [!UICONTROL Router]. Para obter mais informações, consulte [Módulo de roteador em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Diretivas

As diretivas de manipulação de erros permitem controlar como seu cenário reage a erros.

Para obter informações sobre diretivas de tratamento de erros, consulte [Diretivas de tratamento de erros](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

