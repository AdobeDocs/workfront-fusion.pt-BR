---
title: Adicione um módulo de Roteador e configure rotas
description: O módulo de Roteador permite ramificar seu fluxo em várias rotas e processar os dados em cada rota de forma diferente. Depois que um módulo de roteador recebe um pacote, ele o encaminha para cada rota conectada na ordem em que as rotas foram anexadas ao módulo de roteador.
author: Becky
feature: Workfront Fusion
exl-id: 8344cde4-df3e-4b72-9d10-46ff4b186400
source-git-commit: 839f6edf93df8a935b2c5d0a520bdc125fe60288
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Adicione um módulo de Roteador e configure rotas

O módulo de Roteador permite ramificar seu cenário em várias rotas e processar os dados em cada rota de forma diferente. Quando um módulo de roteador recebe um pacote, ele o encaminha para cada rota conectada na ordem em que as rotas foram anexadas ao módulo de roteador.

As rotas são processadas sequencialmente, não em paralelo. Um pacote não é enviado para a próxima rota até que tenha sido completamente processado pela rota anterior.


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
   <td> <p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
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

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Adicionar um módulo de Roteador a um cenário

Você deve adicionar um módulo de roteador antes de configurar rotas.

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário em que deseja adicionar um roteador.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. No editor de cenários, clique na alça direita do módulo após o qual deseja adicionar o roteador.
1. Selecione **[!UICONTROL Flow Control]** > **Roteador** na lista de módulos a serem exibidos.

   ![](assets/connect-the-router-350x108.png)

   Ou

   Para inserir o módulo Roteador entre dois módulos, clique no ícone de chave inglesa abaixo da rota que conecta os dois módulos e selecione **[!UICONTROL Add a router]** no menu.

   ![](assets/insert-router-350x191.png)
1. Adicione a primeira rota ao roteador clicando na alça direita do roteador e adicionando um módulo, semelhante à adição de qualquer módulo.
1. Para adicionar outra rota, clique no módulo do roteador. Uma rota é exibida. Adicione módulos a essa rota conforme desejado.

   Você pode adicionar quantas rotas desejar.

1. Para verificar a ordem das rotas, clique no ícone Alinhamento automático ![ícone de Alinhamento automático](assets/auto-align.png).

   As rotas são organizadas na ordem em que são executadas. A rota superior é executada primeiro.

1. (Opcional) Para alterar a ordem da rota, desvincule as rotas clicando com o botão direito do mouse no caminho do roteador e selecionando Desvincular, em seguida, arrastando-as para o módulo do roteador na ordem desejada. A primeira rota anexada será a primeira rota a ser executada (a rota superior).

1. Continue em [Adicionar um filtro a uma rota](#add-a-filter-to-a-route).

## Adicionar um filtro a uma rota

Você pode colocar um filtro em uma rota após o módulo de roteador para filtrar pacotes. Somente os pacotes que passarem pelo filtro serão manipulados pelos módulos na rota.

Se os dados passarem pelo filtro de mais de uma rota, os dados serão tratados por ambas as rotas. A rota superior manipula os dados primeiro.

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário ao qual deseja adicionar um filtro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique na chave inglesa ![Wrench](assets/wrench-icon.png) no caminho em que deseja definir um filtro. Esse é o caminho entre o módulo do roteador e o primeiro módulo da rota.
1. Selecione **Configurar um filtro.**
1. No campo de rótulo do painel que é exibido, adicione um rótulo. Esse rótulo é exibido no cenário.
1. Configurar condições de filtro.

   Para obter mais informações, consulte [Adicionar um filtro a um cenário](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).

1. Clique em **[!UICONTROL OK]** para salvar a configuração do filtro.

1. Continue em [Configurar uma rota de fallback](#configure-a-fallback-route).

## Configurar uma rota de fallback

A rota de fallback é a rota que é executada em qualquer conjunto que não passa nenhum filtro para outra rota.

Você pode ativar uma rota de fallback no painel de filtro.

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário em que deseja adicionar uma rota de fallback.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique na chave inglesa ![Wrench](assets/wrench-icon.png) no caminho em que deseja definir um filtro. Esse é o caminho entre o módulo do roteador e o primeiro módulo da rota.
1. Selecione **Configurar um filtro.**
1. No campo de rótulo do painel que é exibido, adicione um rótulo. Esse rótulo é exibido no cenário.
1. Ative a caixa de seleção de rota de fallback.

   ![](assets/fallback-route-350x260.png)

1. Clique em **[!UICONTROL OK]** para salvar a configuração do filtro.

A rota de Fallback está marcada com uma seta diferente no módulo do Roteador:

![](assets/arrow-sign-in-router-module-350x361.png)

## Exemplo: caso de uso `if/else`

>[!BEGINSHADEBOX]

Um caso de uso típico da rota de fallback é continuar o fluxo com uma rota se a condição for atendida e com outra rota se não for. como nas seguintes etapas:

Neste exemplo, a primeira rota é configurada com um filtro. Isso representa o componente `if`.

![](assets/set-up-a-filter-2-350x242.png)

A segunda rota é configurada como uma rota de fallback. Isso representa o componente `else`.

![](assets/enable-fallback-route-option-350x238.png)

>[!ENDSHADEBOX]
