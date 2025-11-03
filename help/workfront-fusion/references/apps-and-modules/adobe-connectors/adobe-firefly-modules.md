---
title: Módulos do Adobe Firefly
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o  [!DNL Adobe Firefly], bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '2488'
ht-degree: 0%

---

# [!DNL Adobe Firefly] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Adobe Firefly], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote de Automação e Integração do Adobe Workfront</p><p>Workfront Ultimate</p><p>Workfront Prime e pacotes Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Standard</p><p>Trabalhar ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (herdado): automação e integração do Workfront Fusion for Work </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Antes de usar o conector [!DNL Adobe Firefly], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!DNL Adobe Firefly] ativa.

## Informações da API do Adobe Firefly

O conector do Adobe Firefly usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com [!DNL Adobe Firefly]

Para criar uma conexão para seus módulos do [!DNL Adobe Firefly]:

1. Em qualquer módulo, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Nome da Conexão]</td>
        <td>
          <p>Insira um nome para esta conexão.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID do Cliente]</td>
        <td>Insira sua [!UICONTROL Adobe] [!UICONTROL ID do cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira seu [!DNL Adobe] [!UICONTROL Segredo do Cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## [!DNL Adobe Firefly] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Firefly], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Firefly] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Expandir uma imagem

Esse módulo de ação expande uma imagem, opcionalmente com conteúdo de um prompt fornecido.

Esse módulo funciona com a API do Firefly V3 Async. A versão anterior deste módulo foi descontinuada e será removida em breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Insira ou mapeie um prompt para o conteúdo com o qual deseja expandir a imagem. Se nenhum prompt for fornecido, a imagem será expandida com o conteúdo correspondente à imagem original.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de variações]</td> 
   <td>Insira um número entre 1-4. O módulo gerará esse número de variações de imagem expandidas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source]</td> 
   <td>Selecione como você está fornecendo o arquivo de origem:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de imagem expandido]</td> 
   <td>Selecione o formato de arquivo com o qual a imagem expandida será salva.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expandir por]</td> 
   <td>  <p>Selecione se deseja expandir a imagem usando a inserção de imagem ou uma máscara.</p> 
   <ul>
   <li><b>Posicionamento</b><p>Insira o alinhamento horizontal e vertical e a margem interna da imagem inserida a partir das arestas.</p></li>
   <li><b>Máscara</b><p>Selecione o arquivo de origem da máscara e se a máscara deve ser invertida.</p></li>
   </ul>
</td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tamanho]</td> 
   <td>Selecione a altura e a largura desejadas para a imagem expandida.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Para cada imagem gerada pelo módulo, clique em <b>Adicionar item</b> e insira ou mapeie um inteiro. Você pode usar essa mesma semente em outro módulo Expandir uma imagem para gerar uma imagem semelhante com estilos diferentes. O número de seeds que você adicionar deve ser igual ao campo Number of variation.</td> 
  </tr> 
 </tbody> 
</table>

### Expandir uma imagem (desaprovado)

Este módulo foi descontinuado e será removido em breve. Em vez disso, use o módulo Expandir uma imagem.

### Preencher uma imagem

Esse módulo de ação preenche a área mascarada de uma imagem, opcionalmente com o conteúdo de um prompt fornecido.

Esse módulo funciona com a API do Firefly V3 Async. A versão anterior deste módulo foi descontinuada e será removida em breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Imagem &gt; Source]</td> 
   <td>Selecione como você está fornecendo o arquivo de origem da imagem:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask &gt; Source]</td> 
   <td>Selecione como você está fornecendo o arquivo de origem da máscara:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Insira ou mapeie um prompt para o conteúdo com o qual deseja preencher a imagem. Se nenhum prompt for fornecido, a imagem será preenchida com o conteúdo correspondente à imagem original.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de variações]</td> 
   <td>Insira um número entre 1-4. O módulo gerará esse número de variações de imagem preenchidas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de imagem preenchido]</td> 
   <td>Selecione o formato de arquivo com o qual a imagem preenchida será salva.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Para cada imagem gerada pelo módulo, clique em <b>Adicionar item</b> e insira ou mapeie um inteiro. Você pode usar essa mesma semente em outro módulo Expandir uma imagem para gerar uma imagem semelhante com estilos diferentes. O número de seeds que você adicionar deve ser igual ao campo Number of variation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tamanho]</td> 
   <td>Selecione o tamanho desejado para a imagem preenchida.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Localidade]</td> 
   <td>Se um local for fornecido, o módulo gerará conteúdo mais relevante para o local especificado. <p>A localidade deve ser fornecida no código de idioma ISO 639-1 e na região ISO 3166-1.</p><p> Exemplo: <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>

### Preencher uma imagem (desaprovado)

Este módulo foi descontinuado e será removido em breve. Em vez disso, use o módulo Fill an image.

### Gerar uma imagem

Esse módulo de ação gera uma imagem e com base em um prompt fornecido. Você também pode fornecer uma imagem de referência opcional, e a imagem gerada corresponderá ao estilo da imagem de referência.

Esse módulo funciona com a API do Firefly V3 Async. A versão anterior deste módulo foi descontinuada e será removida em breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Insira ou mapeie um prompt para a imagem que deseja gerar. Mais detalhes no prompt permitirão que você tenha mais controle sobre o que aparece na imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Versão do modelo]</td> 
   <td>Selecione a versão do modelo do Firefly que deseja usar para gerar a imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de variações]</td> 
   <td>Insira um número entre 1-4. O módulo gerará esse número de variações de imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de imagem gerado]</td> 
   <td>Selecione o formato de arquivo com o qual a imagem expandida será salva. Se você selecionar padrão, o formato de arquivo será JPEG se nenhuma imagem de referência for fornecida. Se uma imagem de referência for fornecida, o formato de arquivo da imagem gerada será igual ao da imagem de referência.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estrutura &gt; Referência de imagem]</td> 
    <td>Selecione como você está fornecendo o arquivo de origem para a estrutura da nova imagem:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estrutura &gt; Força]</td> 
    <td>Insira um número entre 0 e 100 para controlar a restrição com que o Firefly segue a estrutura da imagem de origem. Números mais altos significam que o Firefly segue a imagem com mais rigor.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estilo &gt; Referência da imagem]</td> 
    <td>Selecione como você está fornecendo o arquivo de origem para o estilo da nova imagem:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estrutura &gt; Força]</td> 
    <td>Insira um número entre 0 e 100 para controlar a restrição com que o Firefly segue o estilo da imagem de origem. Números mais altos significam que o Firefly segue a imagem com mais rigor.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estilo &gt; Predefinições]</td> 
   <td>Se quiser usar um estilo predefinido, clique em Adicionar item e insira ou mapeie o estilo que deseja usar.<p>Para obter uma lista de estilos predefinidos, consulte <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Estilos de modelo de imagem</a> na documentação do desenvolvedor do Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt negativo]</td> 
   <td>Insira ou mapeie as palavras que deseja evitar no conteúdo gerado. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classe de conteúdo]</td> 
   <td>Selecione se você deseja que a imagem gerada seja mais como uma foto ou mais como uma arte criada. <ul><li><b>Foto</b><p>Insira valores para a abertura, velocidade do obturador (em segundos) e campo de visão (em milímetros).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]</td> 
   <td>Para cada imagem gerada pelo módulo, clique em <b>Adicionar item</b> e insira ou mapeie um inteiro. Você pode usar essa mesma semente em outro módulo Expandir uma imagem para gerar uma imagem semelhante com estilos diferentes. O número de seeds que você adicionar deve ser igual ao campo Number of variation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tamanho]</td> 
   <td>Selecione o tamanho que você deseja que a imagem gerada tenha.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Intensidade visual]</td> 
   <td>Insira ou mapeie um número inteiro que represente a intensidade geral das características visuais existentes da foto. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Localidade]</td> 
   <td>Se um local for fornecido, o módulo gerará conteúdo mais relevante para o local especificado. <p>A localidade deve ser fornecida no código de idioma ISO 639-1 e na região ISO 3166-1.</p><p> Exemplo: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inclinável]</td> 
   <td>Habilite esta opção para gerar uma imagem que pode ser repetida infinitamente em todas as direções.</td> 
  </tr> 
 </tbody> 
</table>

### Gerar uma imagem (desaprovado)

Este módulo foi descontinuado e será removido em breve. Em vez disso, use o módulo Generate an image.

### Gerar uma composição de objeto

Este módulo de ação combina imagens geradas pelo Firefly para criar uma composição de imagem.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Insira ou mapeie um prompt para a imagem que deseja gerar. Mais detalhes no prompt permitirão que você tenha mais controle sobre o que aparece na imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de variações]</td> 
   <td>Insira um número entre 1-4. O módulo gerará esse número de variações de imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classe de conteúdo]</td> 
   <td>Selecione se você deseja que a imagem gerada seja mais como uma foto ou como uma arte.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Imagem &gt; Source]</td> 
    <td>Selecione como você está fornecendo o arquivo de origem para a estrutura da nova imagem:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de imagem gerado]</td> 
   <td>Selecione o formato de arquivo com o qual a imagem expandida será salva. Se você selecionar padrão, o formato de arquivo será JPEG se nenhuma imagem de referência for fornecida. Se uma imagem de referência for fornecida, o formato de arquivo da imagem gerada será igual ao da imagem de referência.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estilo &gt; Referência da imagem]</td> 
    <td>Selecione como você está fornecendo o arquivo de origem para o estilo da nova imagem:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estrutura &gt; Força]</td> 
    <td>Insira um número entre 0 e 100 para controlar a restrição com que o Firefly segue o estilo da imagem de origem. Números mais altos significam que o Firefly segue a imagem com mais rigor.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estilo &gt; Predefinições]</td> 
   <td>Se quiser usar um estilo predefinido, clique em Adicionar item e insira ou mapeie o estilo que deseja usar.<p>Para obter uma lista de estilos predefinidos, consulte <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Estilos de modelo de imagem</a> na documentação do desenvolvedor do Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tamanho]</td> 
   <td>Selecione o tamanho em que deseja que o composto gerado seja. </td> 
  </tr> 
 </tbody> 
</table>

### Gerar imagens semelhantes

Esse módulo de ação gera imagens semelhantes à imagem de origem especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de variações]</td> 
   <td>Insira um número entre 1-4. O módulo gerará esse número de variações de imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Versão do modelo]</td> 
   <td>Selecione a versão do modelo do Firefly que deseja usar para gerar as imagens.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de imagem gerado]</td> 
   <td>Selecione o formato de arquivo com o qual a imagem expandida será salva. Se você selecionar padrão, o formato de arquivo será JPEG se nenhuma imagem de referência for fornecida. Se uma imagem de referência for fornecida, o formato de arquivo da imagem gerada será igual ao da imagem de referência.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Imagem &gt; Source]</td> 
    <td>Selecione como você está fornecendo o arquivo de origem para a estrutura da nova imagem:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estilo &gt; Referência da imagem]</td> 
    <td>Selecione como você está fornecendo o arquivo de origem para o estilo da nova imagem:<ul><li><p><b>Arquivo</b></p><p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de imagem de referência do arquivo de origem e o arquivo de imagem de referência.</p></li><li><p><b>URL pré-assinado</b></p><p>Insira ou mapeie o URL da imagem de origem.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tamanho]</td> 
   <td>Selecione o tamanho em que deseja que o composto gerado seja. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Para cada imagem gerada pelo módulo, clique em <b>Adicionar item</b> e insira ou mapeie um inteiro. Você pode usar essa mesma semente em outro módulo Expandir uma imagem para gerar uma imagem semelhante com estilos diferentes. O número de seeds que você adicionar deve ser igual ao campo Number of variation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inclinável]</td> 
   <td>Habilite esta opção para gerar uma imagem que pode ser repetida infinitamente em todas as direções.</td> 
  </tr> 
 </tbody> 
</table>


### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada personalizada para a API do Firefly.

Para obter as APIs específicas disponíveis, consulte [API do Adobe Firefly](https://developer.adobe.com/firefly-services/docs/firefly-api/) na documentação do Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Firefly]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Insira um caminho relativo para <code>https://firefly-api.adobe.io/</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Método]</p>
      </td>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cabeçalhos]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

