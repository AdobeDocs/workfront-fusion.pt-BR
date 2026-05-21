---
title: Módulos do Adobe Firefly
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam  [!DNL Adobe Firefly], bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
TQID: https://experienceleague.adobe.com/1hI4NuUl2eEAgWyXRKLHQ3-6MM9-2tFyujGbRfHSBmU
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 3886
ht-degree: 15%

---

# Módulos do [!DNL Adobe Firefly]

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam [!DNL Adobe Firefly], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

Para criar uma conexão para os módulos do [!DNL Adobe Firefly]:

1. Em qualquer módulo, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Insira um nome para essa conexão.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira sua [!UICONTROL Adobe] [!UICONTROL ID do cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira o [!UICONTROL Client Secret] do [!DNL Adobe]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## Módulos do [!DNL Adobe Firefly] e seus campos

Ao configurar módulos do [!DNL Adobe Firefly], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos do [!DNL Adobe Firefly] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Expandir uma imagem

Esse módulo de ação expande uma imagem, opcionalmente com conteúdo de um prompt fornecido.

Esse módulo funciona com a API do Firefly V3 Async. A versão anterior deste módulo foi descontinuada e será removida em breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
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

### Gerar composto adaptável

Este módulo de ação compõe uma imagem do assunto de maneira uniforme em uma imagem de fundo em um local mascarado. É possível controlar a intensidade de aplicação das sombras, a forma como a iluminação e a cor do objeto são harmonizadas com o plano de fundo e se os detalhes do plano de fundo original são preservados na área mascarada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Plano de fundo &gt; Imagem &gt; Source]</td> 
   <td>Selecione como você está fornecendo a imagem de fundo. A imagem de plano de fundo é a cena de destino na qual o objeto será composto.<ul><li><p><b>Fazer upload de imagem</b></p><p>Faça upload da imagem de fundo ou mapeie o arquivo de imagem de um módulo anterior.</p></li><li><p><b>URL da imagem</b></p><p>Insira ou mapeie o URL da imagem de fundo.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Plano de Fundo &gt; Máscara de Área de Preenchimento &gt; Source]</td> 
   <td>Selecione como você está fornecendo a máscara da área de preenchimento. A máscara da área de preenchimento indica a área do plano de fundo onde o objeto será colocado.<ul><li><p><b>Fazer upload de imagem</b></p><p>Faça upload da imagem da máscara de área de preenchimento ou mapeie o arquivo de imagem de um módulo anterior.</p></li><li><p><b>URL da imagem</b></p><p>Insira ou mapeie o URL da imagem da máscara da área de preenchimento.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objeto &gt; Imagem &gt; Source]</td> 
   <td>Selecione como você está fornecendo a imagem do objeto. A imagem de objeto é a imagem de origem do objeto a ser composto no plano de fundo.<ul><li><p><b>Fazer upload de imagem</b></p><p>Faça upload da imagem do objeto ou mapeie o arquivo de imagem de um módulo anterior.</p></li><li><p><b>URL da imagem</b></p><p>Insira ou mapeie o URL da imagem do objeto.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objeto &gt; Máscara &gt; Source]</td> 
   <td>Selecione como você está fornecendo a máscara de objeto. A máscara de objeto é a máscara de segmentação do objeto.<ul><li><p><b>Fazer upload de imagem</b></p><p>Faça upload da imagem da máscara de objeto ou mapeie o arquivo de imagem de um módulo anterior.</p></li><li><p><b>URL da imagem</b></p><p>Insira ou mapeie o URL da imagem da máscara de objeto.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de Variações]</td> 
   <td>Insira um número entre 1 e 3. O módulo gera esse número de variações compostas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]*</td> 
   <td>Clique em <b>Adicionar item</b> para adicionar um valor de propagação e, em seguida, insira ou mapeie um inteiro. Use uma seed por variação. A contagem de valores de propagação deve corresponder ao valor de [!UICONTROL Number of Variations] se ambos forem fornecidos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Harmonização]*</td> 
   <td>Insira um número entre 0 e 1 para controlar o quanto as cores e a iluminação do objeto são ajustadas para corresponder ao plano de fundo. <code>0.0</code> aplica harmonização mínima e <code>1.0</code> aplica harmonização máxima.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intensidade da Sombra]*</td> 
   <td>Insira um número entre 0 e 1 para controlar a intensidade da sombra no resultado composto. Valores mais baixos reduzem a sombra.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preservar Tela de Fundo]*</td> 
   <td>Selecione se deseja preservar os detalhes do plano de fundo original na área mascarada durante a composição. <ul><li><b>Sim</b><p>Os detalhes de fundo originais dentro da área mascarada são preservados durante a composição.</p></li><li><b>Não</b><p>Os detalhes de fundo originais dentro da área mascarada não são preservados durante a composição.</p></li><li><b>Não definido</b><p>Use o comportamento padrão para essa opção.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saída &gt; Tipo de mídia]*</td> 
   <td>Selecione o formato de arquivo em que o composto gerado será salvo.</td> 
  </tr> 
 </tbody> 
</table>

* Esses campos são avançados e não são exibidos a menos que você selecione **[!UICONTROL Mostrar configurações avançadas]**.

### Gerar uma imagem

Esse módulo de ação gera uma imagem e com base em um prompt fornecido. Você também pode fornecer uma imagem de referência opcional, e a imagem gerada corresponderá ao estilo da imagem de referência.

Esse módulo funciona com a API do Firefly V3 Async. A versão anterior deste módulo foi descontinuada e será removida em breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
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

### Gerar imagens com Imagem5

Este módulo de ação gera uma imagem usando o modelo Image5 [!DNL Adobe Firefly]. Você fornece um prompt de texto e, opcionalmente, uma imagem de referência para orientar a geração.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Insira ou mapeie uma descrição da imagem que você deseja gerar. O prompt deve ter entre 1 e 1500 caracteres. Mais detalhes no prompt permitem mais controle sobre o que aparece na imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Proporção]</td> 
   <td>Selecione a forma da imagem gerada. Se uma imagem de referência for fornecida, selecione <b>Automático</b>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resolução]</td> 
   <td>Selecione a resolução da imagem gerada. Resoluções mais altas demoram mais para serem geradas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Imagem de Referência]</td> 
   <td>Opcionalmente, forneça uma imagem de referência para orientar a geração. Clique em <b>Adicionar item</b> e forneça a imagem. Ao usar uma imagem de referência, defina [!UICONTROL Aspect Ratio] como <b>Auto</b>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]*</td> 
   <td>Clique em <b>Adicionar item</b> e insira ou mapeie um número inteiro para reproduzir um resultado de geração específico. Deixe vazio para gerar um resultado aleatório.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Raciocínio de Prompt]*</td> 
   <td>Selecione a estratégia de raciocínio rápido usada durante a geração.<ul><li><p><b>Qualidade - Gera a descrição da imagem</b></p><p>Gera uma descrição da imagem na saída do módulo.</p></li><li><p><b>Velocidade - Geração mais rápida, sem descrição</b></p><p>Gera a imagem mais rapidamente, mas deixa a descrição da imagem vazia.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Localidade]*</td> 
   <td>Insira ou mapeie um idioma e código de região para adaptar o conteúdo gerado a um país e idioma específicos. <p>A localidade deve ser fornecida no código de idioma ISO 639-1 e na região ISO 3166-1.</p><p>Exemplo: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de Variações]*</td> 
   <td>Insira o número de imagens para gerar por solicitação. No momento, somente 1 é compatível. Para gerar várias imagens, envie solicitações separadas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modelo]*</td> 
   <td>Selecione o modelo [!DNL Firefly] que deseja usar para gerar a imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

*Estes campos são avançados e não são exibidos a menos que você selecione **[!UICONTROL Mostrar configurações avançadas]**.

### Gerar compostos precisos

Este módulo de ação coloca um assunto na região mascarada de uma imagem de fundo e aplica harmonização generativa para que o assunto se misture naturalmente com o fundo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Plano de fundo &gt; Imagem &gt; Source]</td> 
   <td>Selecione como você está fornecendo a imagem de fundo. A imagem de plano de fundo é a cena de destino na qual o objeto será composto.<ul><li><p><b>Fazer upload de imagem</b></p><p>Faça upload da imagem de fundo ou mapeie o arquivo de imagem de um módulo anterior.</p></li><li><p><b>URL da imagem</b></p><p>Insira ou mapeie o URL da imagem de fundo.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Plano de Fundo &gt; Máscara de Área de Preenchimento &gt; Source]</td> 
   <td>Selecione como você está fornecendo a máscara da área de preenchimento. A máscara da área de preenchimento indica a área do plano de fundo onde o objeto será colocado.<ul><li><p><b>Fazer upload de imagem</b></p><p>Faça upload da imagem da máscara de área de preenchimento ou mapeie o arquivo de imagem de um módulo anterior.</p></li><li><p><b>URL da imagem</b></p><p>Insira ou mapeie o URL da imagem da máscara da área de preenchimento.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objeto &gt; Imagem &gt; Source]</td> 
   <td>Selecione como você está fornecendo a imagem do objeto. A imagem de objeto é a imagem de origem do objeto a ser composto no plano de fundo.<ul><li><p><b>Fazer upload de imagem</b></p><p>Faça upload da imagem do objeto ou mapeie o arquivo de imagem de um módulo anterior.</p></li><li><p><b>URL da imagem</b></p><p>Insira ou mapeie o URL da imagem do objeto.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número de Variações]</td> 
   <td>Insira um número entre 1 e 3. O módulo gera esse número de variações compostas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]*</td> 
   <td>Clique em <b>Adicionar item</b> para adicionar um valor de propagação e, em seguida, insira ou mapeie um inteiro. Use uma seed por variação. A contagem de valores de propagação deve corresponder ao valor de [!UICONTROL Number of Variations] se ambos forem fornecidos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mesclar]*</td> 
   <td>Insira um número entre 0 e 1 para controlar a mesclagem entre a aparência harmonizada e original do objeto. <code>0.0</code> aplica harmonização total e <code>1.0</code> preserva a aparência do objeto original.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saída &gt; Tipo de mídia]*</td> 
   <td>Selecione o formato de arquivo em que o composto gerado será salvo.</td> 
  </tr> 
 </tbody> 
</table>

* Esses campos são avançados e não são exibidos a menos que você selecione **[!UICONTROL Mostrar configurações avançadas]**.

### Gerar imagens semelhantes

Esse módulo de ação gera imagens semelhantes à imagem de origem especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
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


### Gerar vídeo

Esse módulo de ação gera um vídeo de um prompt de texto. Você também pode fornecer uma ou mais imagens de referência para orientar a geração do vídeo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Insira ou mapeie uma descrição do vídeo que você deseja gerar. Mais detalhes no prompt permitem mais controle sobre o que aparece no vídeo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Imagem &gt; Condições]</td> 
   <td>Opcionalmente, forneça uma ou mais imagens de referência para orientar a geração do vídeo. Clique em <b>Adicionar item</b> para cada imagem de referência.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tamanhos]</td> 
   <td>Clique em <b>Adicionar item</b> e insira ou mapeie as dimensões do vídeo gerado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fator de Taxa de Bits]*</td> 
   <td>Digite um número entre 0 e 63 para especificar o fator de taxa de bits do vídeo gerado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configurações de vídeo &gt; Movimento da câmera]*</td> 
   <td>Selecione o movimento da câmera que deseja usar no vídeo gerado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configurações de Vídeo &gt; Estilo de Aviso]*</td> 
   <td>Selecione o estilo de prompt que deseja usar para o vídeo gerado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configurações de vídeo &gt; Ângulo de captura]*</td> 
   <td>Selecione o ângulo de captura que deseja usar no vídeo gerado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configurações de vídeo &gt; Tamanho da captura]*</td> 
   <td>Selecione o tamanho da captura que deseja usar no vídeo gerado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

* Esses campos são avançados e não são exibidos a menos que você selecione **[!UICONTROL Mostrar configurações avançadas]**.

### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada personalizada para a API do Firefly.

Para obter as APIs específicas disponíveis, consulte [API do Adobe Firefly](https://developer.adobe.com/firefly-services/docs/firefly-api/) na documentação do Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Firefly], consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Firefly]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Insira um caminho relativo a <code>https://firefly-api.adobe.io/</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

