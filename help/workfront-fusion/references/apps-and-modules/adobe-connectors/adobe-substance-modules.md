---
title: Módulos de substâncias do Adobe
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o  [!DNL Adobe Substance], bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
source-git-commit: 2e44c89d487100b3245b40f6927185a0ff12ef2f
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 2%

---

# [!DNL Adobe Substance] Módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Adobe Substance], bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Antes de usar o conector [!DNL Adobe Substance], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!DNL Adobe Substance] ativa.



## [!DNL Adobe Substance] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Substance], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Substance] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um asterisco ao lado do nome do campo em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Compostos](#composites)
* [Cenas](#scenes)
* [Espaços](#spaces)

### Compostos

#### Gerar composto de objeto 3D

Esse módulo de ação gera conteúdo para um composto 3D que inclui o ativo principal selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Substance] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Outros campos</td> 
   <td>Configure outros campos conforme desejado. Para obter detalhes sobre campos, consulte a <a href="https://s3d.adobe.io/docs#/operations/v1/composites/compose">documentação da API de substâncias do Adobe</a>.</td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">Camera name</td> 
   <td>Enter or map the name of an existing camera that has been previously defined in the source 3D file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content class</td> 
   <td>Select whether you want the composite to have the style of art or of a photo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable ground plane</td> 
   <td>Enable this to enable the auto-generated ground plane under the hero asset. This is useful if the 3D scene contains only a hero asset, without additional elements.</td> 
  </tr> -->
 </tbody> 
</table>

### Cenas

* [Converter arquivos 3D](#convert-3d-files)
* [Criar cena 3D](#create-3d-scene)
* [Descrever cena 3D](#describe-3d-scene)
* [Renderizar objeto 3D](#render-3d-object)
* [Renderizar objeto 3D (versão básica)](#render-3d-object-basic-version)

#### Converter arquivos 3D

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Substance] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Formato</td> 
   <td>Selecione o formato para o qual você está convertendo o arquivo.</td> 
  </tr> 
<tr> 
   <td role="rowheader">Ponto de entrada do modelo</td> 
   <td>A conversão geralmente usa o primeiro arquivo considerado um modelo 3D válido. Defina esse ponto de entrada para desfazer a ambiguidade quando houver várias opções.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Origens</td> 
   <td>Para cada arquivo que você deseja converter, clique em <b> Adicionar item</b> e insira as informações do arquivo.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar cena 3D

Esse módulo de ação cria uma cena usando os ativos especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Substance] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Codificação</td> 
   <td>Selecione o tipo de arquivo para a cena.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome de base do arquivo</td> 
   <td>Insira ou mapeie um nome para o arquivo de saída.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Outros campos</td> 
   <td>Configure outros campos conforme desejado. Para obter detalhes sobre campos, consulte a <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/assemble">documentação da API de substâncias do Adobe</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Origens</td> 
   <td>Para cada arquivo que você deseja usar, clique em <b> Adicionar item</b> e insira as informações do arquivo.</td> 
  </tr> 
 </tbody> 
</table>

#### Descrever cena 3D

Este módulo de ação recupera informações sobre o conteúdo da cena 3D.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Substance] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Arquivo de cena</td> 
   <td>Insira ou mapeie o caminho para o arquivo de cena que deseja descrever.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Origens</td> 
   <td>Para cada arquivo que você deseja descrever, clique em <b> Adicionar item</b> e insira as informações do arquivo.</td> 
  </tr> 
 </tbody> 
</table>

#### Renderizar objeto 3D

Este módulo de ação renderiza uma imagem de uma cena.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Substance] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
   <td role="rowheader">Outros campos</td> 
   <td>Configure outros campos conforme desejado. Para obter detalhes sobre campos, consulte a <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render">documentação da API de substâncias do Adobe</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Origens</td> 
   <td>Para cada arquivo que você deseja usar, clique em <b> Adicionar item</b> e insira as informações do arquivo.</td> 
  </tr> 
 </tbody> 
</table>

#### Renderizar objeto 3D (versão básica)

Esse módulo de ação renderiza uma imagem de uma cena, mas tem menos opções do que o módulo de objeto Renderizar 3D.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Substance] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
   <td role="rowheader">Outros campos</td> 
   <td>Configure outros campos conforme desejado. Para obter detalhes sobre campos, consulte a <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render-basic">documentação da API de substâncias do Adobe</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Origens</td> 
   <td>Para cada arquivo que você deseja usar, clique em <b> Adicionar item</b> e insira as informações do arquivo.</td> 
  </tr> 
 </tbody> 
</table>

### Espaços

#### Criar espaço

Esse módulo de ação permite fazer upload e armazenar temporariamente arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Substance] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Nome do arquivo</td> 
   <td>Insira ou mapeie o nome do arquivo que está sendo carregado.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Dados do arquivo</td> 
   <td>Insira ou mapeie os dados binários do arquivo.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome</td> 
   <td>Insira ou mapeie um nome para o valor de formulário multipart.</td> 
  </tr> 
 </tbody> 
</table>
