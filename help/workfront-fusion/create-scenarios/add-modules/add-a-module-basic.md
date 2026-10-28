---
title: Adicionar módulo a um cenário
description: Este artigo descreve o processo básico de adicionar um módulo a um cenário.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
TQID: 'https://experienceleague.adobe.com/R2JCX7aaYzmYHgiLqj1WDlVFHI-s-qanltoOrycQ5JU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 8%
---
# Adicionar módulo a um cenário

Um cenário é composto de uma série de módulos que indicam como os dados devem ser transformados em um aplicativo ou transferidos entre aplicativos e serviços da Web. Você constrói um módulo adicionando e configurando módulos.

Este artigo descreve o processo básico de adicionar um módulo a um cenário. Para obter instruções mais específicas sobre como adicionar um cenário, consulte os outros artigos em [Adicionar módulos: índice do artigo](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

>[!NOTE]
>
>O Workfront Fusion está fazendo a transição do editor de cenários para uma nova experiência. Durante essa transição, as experiências clássicas e novas estão disponíveis e você pode alternar entre elas a qualquer momento. Recomendamos usar a nova experiência. Para obter mais informações, consulte [Experiências novas e clássicas](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) no artigo Editor de cenários.

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

## Adicionar o primeiro módulo a um cenário

O primeiro módulo de um cenário geralmente é um módulo acionador.

Para obter mais informações sobre módulos de acionador, consulte [Módulos de acionador](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) no artigo Visão geral do módulo.

* [Adicionar o primeiro módulo na nova experiência do (recomendado)](#add-the-first-module-in-the-new-experience-recommended)
* [Adicionar o primeiro módulo na experiência clássica](#add-the-first-module-in-the-classic-experience)

### Adicionar o primeiro módulo na nova experiência do (recomendado)

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Comece a criar um cenário clicando em **Criar um novo cenário** no canto superior direito da tela.

   O editor de cenários é aberto, com um módulo de espaço reservado e a lista de conectores disponíveis.

   ![Módulo de espaço reservado](/help/workfront-fusion/build-practice-scenarios/assets/new-placeholder-module.png)

   ![Seletor de aplicativos e serviços](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Selecione o conector ou webhook que iniciará este cenário:

   * Navegue por categoria usando o painel à esquerda ([!UICONTROL Favoritos], [!UICONTROL Todos os aplicativos], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative e Conteúdo], [!UICONTROL Adobe Cloud Services], [!UICONTROL IA Gerativa] ou [!UICONTROL Interno]) ou
   * Digite um termo na caixa de pesquisa. Os resultados são atualizados à medida que você digita e as correspondências do conector são listadas antes que o nome do módulo e a descrição correspondam.

1. Clique no módulo que deseja adicionar ao cenário.

1. Configure o módulo.

   As configurações do módulo são abertas no painel no lado direito da tela de desenho.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>* Na lista de conectores, os selos identificam aplicativos privados, premium e beta.
>* Os módulos para aplicativos grandes são organizados em grupos.
>* Quando você adiciona um manipulador de erros, as diretivas são listadas primeiro.
>* Se um conector tiver mais de uma versão, você poderá selecionar a versão depois de selecionar o conector.

>[!NOTE]
>
>Se você removeu o primeiro módulo de um cenário e deseja substituí-lo, clique no módulo de espaço reservado para abrir a lista de conectores.

### Adicionar o primeiro módulo na experiência clássica

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Comece a criar um cenário clicando em **Criar um novo cenário** no canto superior direito da tela.

   O editor de cenários é aberto, com um módulo de espaço reservado (ponto de interrogação) e a lista de conectores disponíveis.

   ![Módulo de espaço reservado](assets/placeholder-module.png)

1. Selecione o conector ou webhook que iniciará esse cenário. Você pode digitar o nome do conector na barra de pesquisa da lista para filtrar a lista.
1. Configure o módulo.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Se você removeu o primeiro módulo de um cenário e deseja substituí-lo, clique no módulo de espaço reservado (ponto de interrogação) para abrir a lista de conectores.

## Adicionar outro módulo a um cenário

* [Adicionar outro módulo na nova experiência do (recomendado)](#add-another-module-in-the-new-experience-recommended)
* [Adicionar outro módulo na experiência clássica](#add-another-module-in-the-classic-experience)

### Adicionar outro módulo na nova experiência do (recomendado)

1. Se você não estiver no editor de cenários do cenário ao qual deseja adicionar um módulo, clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Para adicionar um módulo após outro módulo, passe o mouse sobre a borda direita do módulo após a qual deseja adicionar um módulo, em seguida, clique em **Adicionar outro módulo** quando ele aparecer.

   A lista de conectores é aberta, mostrando todos os conectores já usados no cenário.

1. (Opcional) Para selecionar outro conector, clique em **Adicionar outro módulo** na lista e selecione o conector:

   * Navegue por categoria usando o painel à esquerda ([!UICONTROL Favoritos], [!UICONTROL Todos os aplicativos], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative e Conteúdo], [!UICONTROL Adobe Cloud Services], [!UICONTROL IA Gerativa] ou [!UICONTROL Interno]) ou
   * Digite um termo na caixa de pesquisa. Os resultados são atualizados à medida que você digita e as correspondências do conector são listadas antes que o nome do módulo e a descrição correspondam.

1. Clique no módulo que deseja adicionar ao cenário.

1. Configure o módulo.

   As configurações do módulo são abertas no painel no lado direito da tela de desenho.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

### Adicionar outro módulo na experiência clássica

1. Se você não estiver no editor de cenários do cenário ao qual deseja adicionar um módulo, clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Para adicionar um módulo a outro módulo, passe o mouse sobre a alça direita do módulo após a qual deseja adicionar um módulo, em seguida, clique em **Adicionar outro módulo** quando ele aparecer.

   A lista de conectores é aberta, mostrando todos os conectores já usados no cenário.

1. (Opcional) Para selecionar outro conector, clique em **Adicionar outro módulo** na lista e selecione o conector. Você pode digitar o nome do conector na barra de pesquisa da lista para filtrar a lista.
1. Configure o módulo.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Inserir um módulo entre módulos existentes em um cenário

* [Inserir um módulo na nova experiência do (recomendado)](#insert-a-module-in-the-new-experience-recommended)
* [Inserir um módulo na experiência clássica](#insert-a-module-in-the-classic-experience)

### Inserir um módulo na nova experiência do (recomendado)

1. Se você não estiver no editor de cenários do cenário ao qual deseja adicionar um módulo, clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique com o botão direito do mouse no caminho entre os módulos em que deseja inserir um módulo e selecione **Adicionar um módulo**.

   ![Adicionar um módulo entre módulos existentes](assets/add-a-module-between-modules.png)

   A lista de conectores é aberta, mostrando todos os conectores já usados no cenário.

1. (Opcional) Para selecionar outro conector, clique em **Adicionar outro módulo** na lista e selecione o conector:

   * Navegue por categoria usando o painel à esquerda ([!UICONTROL Favoritos], [!UICONTROL Todos os aplicativos], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative e Conteúdo], [!UICONTROL Adobe Cloud Services], [!UICONTROL IA Gerativa] ou [!UICONTROL Interno]) ou
   * Digite um termo na caixa de pesquisa. Os resultados são atualizados à medida que você digita e as correspondências do conector são listadas antes que o nome do módulo e a descrição correspondam.

1. Clique no módulo que deseja adicionar ao cenário.

1. Configure o módulo.

   As configurações do módulo são abertas no painel no lado direito da tela de desenho.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Para criar um link para um módulo específico, adicione `?moduleId=<module-id>` à URL ao visualizar as seguintes páginas:
>
>* Página de edição do cenário (URL termina em `/edit`)
>* Uma execução de cenário específica (URL termina em `/logs/<log-id>`)
>
>`<module-id>` refere-se ao número ao lado do rótulo do módulo ao visualizar o cenário.
>
>Isso pode ser útil ao depurar cenários ou copiar a configuração do módulo.

### Inserir um módulo na experiência clássica

1. Se você não estiver no editor de cenários do cenário ao qual deseja adicionar um módulo, clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no caminho pontilhado entre os módulos em que deseja inserir um módulo.
1. No menu exibido, selecione **Adicionar um módulo**.

A lista de conectores é aberta, mostrando todos os conectores já usados no cenário.

1. (Opcional) Para selecionar outro conector, clique em **Adicionar outro módulo** na lista e selecione o conector. Você pode digitar o nome do conector na barra de pesquisa da lista para filtrar a lista.
1. Configure o módulo.

   Para obter instruções sobre como configurar módulos específicos, consulte o artigo para os aplicativos escolhidos, listados em [Aplicativos Fusion e suas referências de módulos: índice do artigo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Para criar um link para um módulo específico, adicione `?moduleId=<module-id>` à URL ao visualizar as seguintes páginas:
>
>* Página de edição do cenário (URL termina em `/edit`)
>* Uma execução de cenário específica (a URL termina em `/logs/<log-id>`)
>
>`<module-id>` refere-se ao número ao lado do rótulo do módulo ao visualizar o cenário.
>
>Isso pode ser útil ao depurar cenários ou copiar a configuração do módulo.
