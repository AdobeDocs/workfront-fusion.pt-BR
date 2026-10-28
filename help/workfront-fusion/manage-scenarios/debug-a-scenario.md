---
title: Depurar um cenário
description: O Adobe Workfront Fusion Devtool permite compreender e solucionar problemas de cenários. O Devtool adiciona um painel extra às Ferramentas do desenvolvedor do Chrome. Usando esse painel do depurador, você pode verificar todas as execuções manuais do cenário, revisar todas as operações executadas e ver os detalhes de cada chamada de API realizada. Você pode ver qual módulo, operação ou única resposta causou o erro e usar esse conhecimento para refinar seu cenário.
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
TQID: 'https://experienceleague.adobe.com/7NXYVXxbQvgKnqvRUNV-ySBApe9kl-Kn57sSKCh4NLE'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '1962'
ht-degree: 5%
---
# Depurar um cenário

O Adobe Workfront Fusion Devtool ajuda você a entender e solucionar problemas de cenários. Usando o Devtool, você pode verificar todas as execuções manuais do cenário, revisar todas as operações executadas e ver os detalhes de cada chamada de API executada. Você pode ver qual módulo, operação ou única resposta causou o erro e usar esse conhecimento para refinar seu cenário.

>[!NOTE]
>
>Fazer logon no painel do depurador será limitado ou não estará disponível para cenários confidenciais, execuções automáticas e operações bem-sucedidas.

>[!NOTE]
>
>Na nova experiência do, várias ferramentas DevTool são criadas no editor de cenários, de modo que você pode usá-las sem abrir a DevTool:
>
>| Ferramenta | Onde encontrá-lo na nova experiência do |
>| ---------- | ---------- |
>| Obter metadados do aplicativo | Clique com o botão direito em um módulo e selecione **Metadados do aplicativo**. |
>| Copiar mapeamento | Clique com o botão direito do mouse no módulo de origem, selecione **Copiar mapeamento** e cole-o em um módulo compatível. |
>| Copiar filtro | Clique com o botão direito do mouse no link filtrado, selecione **Copiar filtro** e cole-o em outro link. |
>| Copiar nome do módulo | Clique com o botão direito em um módulo e selecione **Copiar nome do módulo** ou **Colar nome do módulo**. |
>| Trocar conexão | Abra Localizar e substituir, em seguida, use a guia **Conexão**. |
>| Trocar variável | Abra Localizar e substituir, em seguida, use a guia **Variável**. |
>| Remapear origem | Abra Localizar e substituir e, em seguida, use a guia **Source**. |
>
>Essas ferramentas também estão disponíveis na guia **Ferramentas** da DevTool, juntamente com Focalizar um módulo, Localizar módulos por mapeamento e Base 64. Você também pode usar as funções `base64()` e conversão binária em mapeamentos.
>
>Você também pode exibir os detalhes da solicitação e da resposta diretamente do [Live Trail](/help/workfront-fusion/manage-scenarios/live-trail.md) e do histórico de execução no editor de cenários. Para obter mais informações sobre Localizar e substituir, consulte [Localizar e substituir variáveis, fontes e conexões em um cenário](/help/workfront-fusion/manage-scenarios/find-and-replace.md).
<!-- BECKY CHECK ME: DevTool screenshots (10/27/26) show all ten tools still on the Tools tab, so this note now says the seven built-in tools are available in both places. The release notes implied only Focus a module, Find modules by mapping, and Base 64 would remain. Confirm after release whether the other seven are removed from the DevTool, and update this note and the Tools section if so.  -->
<!-- BECKY CHECK ME: note added from the 10/23/26 release notes; the DevTool is NOT being removed. This article still needs a fuller restructure (new/classic split for the seven tools, Live Trail section or separate article). Confirm the menu labels. -->

Para obter uma introdução em vídeo e uma apresentação do Fusion Devtool, consulte

* [Ferramenta de Desenvolvimento Fusion](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [Apresentação do Devtool](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough.html?lang=en)

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

## Acesse o Devtool

Se você usar o Fusion no Unified Shell do Adobe ou tiver atualizado para a nova experiência do Fusion, poderá acessar o Devtool no editor de Cenário.

### Acesse o Devtool na nova experiência do

1. Vá para o Editor de cenários do cenário que deseja depurar.

   Para localizar o editor de cenários, consulte [O editor de cenários](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Clique no ícone de três pontos na área Controles e selecione **DevTool**.

Ou:

1. Vá para o Editor de cenários do cenário que deseja depurar.
1. Clique com o botão direito do mouse em uma área vazia da página (não em um módulo ).
1. Selecione **Abrir Devtool**.

A DevTool é aberta em um painel abaixo da tela.

<!-- BECKY CHECK ME: new-experience access steps from your 10/27/26 notes (three-dot menu in Controls, or right-click). Confirm the menu label ('DevTool') and the 'panel below the canvas' description, and add a screenshot. I assumed the Helper tools icon steps below apply to the classic experience only; confirm. -->

### Acesse o Devtool na experiência clássica

1. Clique no ícone **Ferramentas auxiliares** ![Ferramentas auxiliares](assets/debugger-icon.png) próximo à parte inferior da tela.

Ou:

1. Vá para o Editor de cenários do cenário que deseja depurar.

   Para localizar o editor de cenários, consulte [O editor de cenários](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Clique com o botão direito do mouse em uma área vazia da página (não em um módulo ).
1. Selecione **Abrir Devtool**.

## Usar o Workfront Fusion Devtool

O Workfront Fusion Devtool é dividido em três seções principais, além de um link de ajuda. Você pode encontrá-los no painel esquerdo da janela Devtool.

* [Live Stream](#live-stream)
* [Depurador de cenários](#scenario-debugger)
* [Ferramentas](#tools)
* **Ajuda do DevTool**: Clique no ícone de ponto de interrogação para abrir o artigo sobre o DevTool.

<!-- BECKY CHECK ME: the DevTool left panel now has a fourth item, 'DevTool help' (question mark icon), per your 10/27/26 screenshots. Confirm the label, that it opens this article or another one, and whether to apply this to the classic experience too. Retake the left-panel screenshot. -->

### Live Stream

O Live Stream exibe o que está acontecendo em segundo plano quando você clica em Executar uma vez no seu cenário.

<!-- BECKY CHECK ME: HOLD: in the new experience, Live Stream shows a 'no events available' message even while a scenario is running, which may be a bug. No updates have been made to this section. Re-test after release before changing anything here. If it is intended behavior, this section may need to point to Live Trail instead. -->

1. Clique no ícone **[!UICONTROL Live Stream]** ![Ícone Live Stream](assets/live-stream-icon.png) para abrir a seção Live Stream.
1. Siga um destes procedimentos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Ação</th> 
      <th>Instruções</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td role="rowheader">Exibir informações da solicitação</td> 
      <td> <p>Você pode exibir as seguintes informações para cada módulo em seu cenário</p> 
       <ul> 
        <li> <p>Cabeçalhos de solicitação (URL do endpoint da API, método http, hora e data em que a solicitação foi chamada, cabeçalhos de solicitação e sequência de consulta)</p> </li> 
        <li> <p>Corpo da solicitação</p> </li> 
        <li> <p>Cabeçalhos de resposta</p> </li> 
        <li> <p>Corpo da resposta</p> </li> 
       </ul> <p>Para exibir essas informações, clique na guia apropriada no painel direito do Workfront Fusion Devtool.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Pesquisar eventos por conteúdo</p> </td> 
      <td> <p>Insira o termo de pesquisa no campo de pesquisa no painel esquerdo do Workfront Fusion Devtool para exibir somente solicitações que contenham o termo de pesquisa.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Limpar lista de solicitações </p> </td> 
      <td> <p>Clique no ícone de lixeira no canto superior direito do painel esquerdo do Devtool para limpar a lista de solicitações registradas pelo Workfront Fusion Devtool. </p> </td> 
     </tr> 
     <!--
     <tr>
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>
     -->
     <tr> 
      <td role="rowheader"> <p>Recuperar a solicitação no formato JSON bruto ou cURL</p> </td> 
      <td> 
       <ul> 
        <li> <p><strong>JSON bruto</strong> </p> <p>Clique em <strong>[!UICONTROL Copiar RAW]</strong> no canto superior direito do painel direito de Devtool.</p> </li> 
        <li> <p><strong>cURL</strong> </p> <p>Clique em <strong>[!UICONTROL Copiar cURL]</strong> no canto superior direito do painel direito de Devtool.</p> </li> 
       </ul> </td> 
     </tr> 
    </tbody> 
   </table>

### Depurador de cenários

>[!NOTE]
>
>Para acessar rapidamente o depurador a partir de um cenário com erro, você pode clicar em **Obter detalhes** na mensagem de erro na saída do módulo.
>
>![Obter detalhes na saída do módulo](assets/go-to-debugger.png)

O Depurador de cenários é útil para cenários mais complexos. Ele exibe o histórico das execuções de cenário e permite pesquisar módulos pelo nome ou ID.

1. Clique no **[!UICONTROL ícone do Scenario Debugger]** ![ícone do Debugger](assets/scenario-debugger-icon.png) para abrir o Scenario Debugger.

   O Scenario Debugger lista os módulos no seu cenário. Cada módulo mostra seu nome, o aplicativo e a ação, além de um selo numerado com a ID do módulo.

1. (Opcional) Insira o termo de pesquisa (nome ou ID do módulo) no campo **Pesquisar módulos por nome ou ID**.
1. Clique no nome do módulo.

   Os ciclos da execução mais recente do módulo são listados ao lado da lista de módulos. Se o módulo não tiver dados de execução, o Scenario Debugger exibirá **Nenhum resultado encontrado**.

1. Expanda um ciclo e clique em uma operação.

   Cada operação mostra se teve êxito e quanto tempo levou, por exemplo **Operação 1** com duração de 0 ms.

1. Revise os detalhes da solicitação. Use as guias para exibir:

   * **Cabeçalhos de Solicitação**: a URL do ponto de extremidade da API, o método HTTP, quando a solicitação foi chamada, e os cabeçalhos de solicitação.
   * **Solicitar corpo**
   * **Cabeçalhos de resposta**
   * **Corpo da resposta**

1. (Opcional) Para copiar a solicitação, clique em **Copiar RAW** ou **Copiar cURL**.

<!-- BECKY CHECK ME: Scenario Debugger steps expanded from your 10/27/26 new-experience DevTool screenshots. Confirm: (1) the 'Search modules by Name or ID' label; (2) that the module list sub-labels, badge (module ID), cycle/operation layout, and 'No Result found' state are described correctly; (3) the tab names, since Response Body was partly hidden behind the Copy buttons in the screenshot; (4) whether Copy RAW and Copy cURL copy the request only or the request and response; (5) whether the classic experience's Scenario Debugger looks the same, or this needs a new/classic split. The screenshot also shows a collapsed 'Live trail' tab with an event count on the right edge of the editor; see the Live Trail article. Retake the Scenario Debugger screenshots. -->

### Ferramentas

O Workfront Fusion Devtool apresenta ferramentas que facilitam a configuração do seu cenário.

1. Clique no ícone **[!UICONTROL Ferramentas]** ![Ícone Ferramentas do console](assets/console-tools-icon.png) para abrir as Ferramentas.
1. (Opcional) Para localizar uma ferramenta, digite seu nome no campo **Pesquisar ferramenta por nome**.
1. Selecione a ferramenta que deseja usar
1. Configure os campos conforme detalhado abaixo.
1. Clique em **[!UICONTROL Executar]**.

Até selecionar uma ferramenta, o lado direito do painel solicitará que você a selecione. Um link na parte inferior da guia Ferramentas direciona você ao artigo sobre a DevTool.

<!-- BECKY CHECK ME: added from your 10/27/26 screenshots: the 'Search tool by name' field, the select-a-tool prompt, and the link to the DevTool article. Confirm the field label and link destination; retake the Tools screenshot. -->

Ferramentas e seus campos:

* [Focalizar em um módulo](#focus-a-module)
* [Localizar Módulos por Mapeamento](#find-modules-by-mapping)
* [Obter metadados do aplicativo](#get-app-metadata)
* [Copiar mapeamento](#copy-mapping)
* [Copiar Filtro](#copy-filter)
* [Copiar Nome do Módulo](#copy-module-name)
* [Trocar Conexão](#swap-connection)
* [Trocar variável](#swap-variable)
* [Base 64](#base-64)
* [Remapear Source](#remap-source)

#### [!UICONTROL Focalizar em um módulo]

Abre as configurações do módulo especificado por ID.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL ID de Módulo]</td>
        <td>Insira a ID do módulo para abrir suas configurações.</td>
    </tr>
</table>

#### [!UICONTROL Localizar Módulos por Mapeamento]

Permite pesquisar valores de módulos para um termo especificado. A saída contém IDs de módulos que contêm o termo que você pesquisou.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Palavra-chave]</td> 
   <td> <p> Insira o termo que deseja pesquisar. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Usar Somente Valores]</p> </td> 
   <td> <p>Habilite esta opção para pesquisar apenas nos valores dos campos do módulo.</p> <p>Desative essa opção para pesquisar também nos nomes dos campos do módulo.</p> <p>A pesquisa é realizada por meio dos parâmetros name e label.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter metadados do aplicativo]

Recupera metadados do aplicativo pelo nome do módulo ou ID do aplicativo. Isso é útil, por exemplo, quando você precisa saber a versão do aplicativo usada em seu cenário.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Módulo Source]</td>
        <td>Selecione o módulo para o qual deseja recuperar metadados.</td>
    </tr>
</table>

#### [!UICONTROL Copiar mapeamento]

Copia valores do módulo de origem para o módulo de destino.

>[!CAUTION]
>
>Defina os módulos de origem e de destino corretos. Se você selecionar um tipo diferente de módulo, os valores no módulo de destino serão excluídos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Módulo Source]</td> 
   <td> <p> Selecione o módulo ou insira a ID do módulo do qual deseja copiar valores de campo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Módulo de Destino]</p> </td> 
   <td> <p>Selecione o módulo ou insira a ID do módulo no qual deseja inserir os valores do módulo de origem.</p> <p>Importante: os valores no módulo de destino serão substituídos.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copiar Filtro]

Copia as configurações de filtro do módulo de origem para o módulo de destino.

>[!NOTE]
>
>A ação de cópia é executada no filtro colocado no lado esquerdo do módulo selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Módulo Source]</td> 
   <td> <p> Selecione o módulo ou insira a ID do módulo do qual deseja copiar valores de filtro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Módulo de Destino]</p> </td> 
   <td> <p>Selecione o módulo ou insira a ID do módulo no qual deseja inserir os valores de filtro do módulo de origem.</p> <p>Importante: os valores no módulo de destino serão substituídos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Preservar Configuração de Rota de Fallback]</p> </td> 
   <td> <p>O filtro de origem é definido como a rota de fallback. Habilite esta opção para também definir o filtro de destino como a rota de fallback.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Copiar Nome do Módulo]

Copia o nome do módulo selecionado para a área de transferência.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Module] </td> 
   <td> <p>Selecione o módulo do qual deseja copiar o nome.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Trocar Conexão]

Duplica uma conexão do módulo de origem para cada módulo no cenário do mesmo aplicativo.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Módulo Source]</td>
        <td>Selecione o módulo ou insira a ID do módulo do qual deseja duplicar a conexão.</td>
    </tr>
</table>

#### [!UICONTROL Trocar variável]

Pesquisa variáveis especificadas no cenário e as substitui por uma nova variável.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variável a ser Localizada]</td> 
   <td> <p> Localize o preenchimento de variável que deseja substituir no módulo de variável no cenário e copie-o para este campo ([!UICONTROL Variável a Ser Localizada]). No campo, ele é exibido com chaves duplas. Exemplo: <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Substituir Por]</p> </td> 
   <td> <p>Localize o preenchimento de variável que deseja substituir a variável no módulo de variáveis no cenário e copie-o para este campo ([!UICONTROL Variável a Ser Localizada]). No campo, ele é exibido com chaves duplas. Exemplo: <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module]</p> </td> 
   <td> <p>Selecione o módulo de variáveis no qual deseja substituir a variável. Se nenhum módulo for selecionado, a variável será substituída em todo o cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Base 64]

Permite codificar os dados inseridos em Base64 ou decodificar Base64. Algumas solicitações estão codificadas em Base64. Essa ferramenta pode ser útil quando você deseja pesquisar dados específicos na solicitação codificada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operação] </td> 
   <td> <p>Selecione se deseja codificar os dados do campo [!UICONTROL Dados Brutos] em Base64 ou decodificar Base64 em Dados Brutos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Dados Brutos]</p> </td> 
   <td> <p> Insira os dados que deseja codificar em Base64 ou Base64 se quiser decodificar em dados brutos, dependendo da opção selecionada no campo [!UICONTROL Operation] acima.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remapear Source]

Permite alterar a origem do mapeamento de um módulo para outro.

Primeiro, você deve adicionar o módulo que deseja usar como módulo de origem à rota em seu cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Módulo Source] </td> 
   <td> <p> Selecione o módulo que você deseja substituir como a origem de mapeamento para outros módulos em seu cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Módulo de Destino]</p> </td> 
   <td> <p>Selecione o módulo que deseja usar como uma nova origem de mapeamento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Módulo a ser Editado]</p> </td> 
   <td> <p>Selecione o módulo para o qual deseja alterar o mapeamento se não quiser alterar o mapeamento em todo o cenário. </p> </td> 
  </tr> 
 </tbody> 
</table>
