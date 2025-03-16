---
title: Controle de fluxo
description: Ao criar ou editar um cenário, você pode definir configurações para controlar como os dados fluem por ele.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '640'
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
   <p>Nenhum requisito de licença do Workfront Fusion</p>
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

Você pode usar um módulo [!UICONTROL Repetidor] para repetir uma tarefa um determinado número de vezes. Um módulo [!UICONTROL Repetidor] gera conjuntos, um após o outro.


<table>
    <tr>
        <td>[!UICONTROL Valor inicial]</td>
        <td>Insira ou mapeie o valor que você deseja que o módulo tenha na primeira iteração. O valor padrão é 1.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Repete]</td>
        <td>Insira ou mapeie o número de vezes que você deseja que o módulo se repita. Esse número deve ser maior ou igual a 0 e menor ou igual a 10.000.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Etapa]</td>
        <td>Este é o número pelo qual o módulo aumenta o valor. O valor padrão é 1.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

Por exemplo, você pode usar um módulo [!UICONTROL Repetidor] para enviar cinco emails com os assuntos &quot;Olá 1&quot;, &quot;Olá 2&quot; e assim por diante, conectando o módulo **[!UICONTROL Email] >[!UICONTROL Enviar um email]** ao módulo [!UICONTROL Repetidor].

1. Clique no ícone [!UICONTROL Controle de Fluxo] ![Ícone de Controle de fluxo](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif), na parte inferior da tela, e clique em **[!UICONTROL Repetidor]**, no menu exibido.
1. Clique no módulo [!UICONTROL Repetidor] e em **[!UICONTROL Conectar-se automaticamente]** na caixa exibida.

   O módulo Repetidor se abre.

1. No campo **[!UICONTROL Repetições]**, digite o número de repetições (pacotes de saída) que o módulo deve produzir.

   Neste exemplo, você digitaria 5.

   ![Repetidor](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   O valor do item aumenta em cada repetição com este valor especificado no campo **[!UICONTROL Etapa]**, que pode ser visualizado ao selecionar **[!UICONTROL Mostrar configurações avançadas]**. Esse número é 1 por padrão.

1. Clique em **[!UICONTROL OK]** para fechar a caixa **[!UICONTROL Controle de Fluxo]**.

1. Clique no módulo de aplicativo ou serviço conectado ao módulo [!UICONTROL Repetidor].
1. Na caixa exibida, digite as informações que deseja repetir.

   No nosso exemplo de email, você digitaria Olá na caixa [!UICONTROL Assunto] e mapearia `i` do módulo do repetidor.

   ![Repetidor](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>O número de repetições não é determinado pelo valor de `i`, pois estaria em um loop na programação. O módulo repetirá o número de vezes indicado no campo [!UICONTROL Repetições]. O valor `i` é alterado com cada iteração do módulo [!DNL repeater] e pode ser mapeado para módulos posteriores. O exemplo acima mapeia o valor de `i` na mensagem Hello, resultando em mensagens que leem &quot;Hello 1,&quot; Hello 2 e assim por diante.

>[!ENDSHADEBOX]

## [!UICONTROL Iterador]

Um [!UICONTROL Iterador] é um tipo especial de módulo que converte uma matriz em uma série de conjuntos. Cada item de matriz será um conjunto separado na saída do módulo [!UICONTROL Iterador]. Para obter mais informações, consulte [Módulo Iterador](/help/workfront-fusion/references/modules/iterator-module.md).

## Agregador de matrizes

Um agregador de matriz é um tipo especial de módulo que permite mesclar vários pacotes em um único pacote. Para obter mais informações, consulte [Módulo agregador](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Roteador]

O módulo [!UICONTROL Roteador] permite ramificar seu fluxo em várias rotas e processar os dados em cada rota de forma diferente. Depois que um módulo [!UICONTROL Roteador] receber um pacote, ele o encaminhará para cada rota conectada na ordem em que as rotas foram anexadas ao módulo [!UICONTROL Roteador]. Para obter mais informações, consulte [Módulo de roteador em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Diretivas

As diretivas de manipulação de erros permitem controlar como seu cenário reage a erros.

Para obter informações sobre diretivas de tratamento de erros, consulte [Diretivas de tratamento de erros](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

