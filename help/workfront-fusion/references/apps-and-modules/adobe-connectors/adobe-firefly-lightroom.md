---
title: Módulos do Adobe Firefly
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Adobe Firefly Lightroom, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 965cb643039be36eb3608cd801439a6a055974e4
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 16%

---

# Módulos do Adobe Firefly Lightroom

<!--add to tocs-->

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Adobe Firefly Lightroom, bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Antes de usar o conector do Adobe Firefly Lightroom, você deve garantir que os seguintes pré-requisitos sejam atendidos:

* Você deve ter uma conta ativa do Adobe Firefly Lightroom.

## Criar uma conexão com o Adobe Firefly Lightroom

Para criar uma conexão para os módulos do Adobe Firefly Lightroom:

1. Em qualquer módulo, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Nome da conexão</td>
        <td>
          <p>Insira um nome para essa conexão.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Ambiente</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">Tipo</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
        <td role="rowheader">ID do cliente</td>
        <td>Insira a ID do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Segredo do cliente</td>
        <td>Insira o segredo do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.


## Módulos do Adobe Firefly Lightroom e seus campos

Ao configurar módulos do Adobe Firefly Lightroom, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Adobe Firefly Lightroom podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Adicionar XMP à imagem](#add-xmp-to-image)
* [Aplicar edições no Lightroom](#apply-lightroom-edits)
* [Aplicar predefinições do Lightroom](#apply-lightroom-presets)
* [Endireitar automaticamente](#auto-straighten)
* [Tom automático](#auto-tone)


### Adicionar XMP à imagem

Esse módulo aplica uma predefinição do Lightroom com base em XMP a uma imagem.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly Lightroom, consulte <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Criar uma conexão com o Adobe Firefly Lightroom</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL da imagem</td> 
   <td>Insira ou mapeie um URL pré-assinado que represente a imagem à qual você deseja aplicar o XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de armazenamento</td> 
   <td>Selecione o tipo de armazenamento em que a imagem é armazenada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Conteúdo do XMP</td> 
   <td>Insira ou mapeie o texto do conteúdo do XMP que deseja adicionar à imagem. Deve ser uma sequência de caracteres XML.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Orientação</td> 
    <td>Insira ou mapeie a orientação EXIF a ser aplicada à imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Armazenamento de saída</td> 
    <td>Selecione onde deseja que o arquivo de saída seja armazenado. <p>O armazenamento interno do Fusion não armazena a imagem fora do cenário, mas permite que outros módulos no cenário acessem a imagem.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de saída</td> 
   <td>Selecione o tipo de arquivo para o arquivo de saída.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Substituir</td> 
   <td>Selecione sim se quiser permitir que o módulo substitua a saída se ela já existir. Isso se aplica somente ao armazenamento em nuvem do Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualidade</td> 
   <td>Insira ou mapeie a qualidade da imagem de saída. 1 é a qualidade mais baixa e 12 é a mais alta. Isso se aplica somente a arquivos JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Aplicar edições no Lightroom

Este módulo aplica uma ou mais edições do Lightroom a uma imagem. As edições incluem exposição, contraste, nitidez e saturação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly Lightroom, consulte <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Criar uma conexão com o Adobe Firefly Lightroom</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL da imagem</td> 
   <td>Insira ou mapeie um URL pré-assinado que represente a imagem à qual você deseja aplicar o XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de armazenamento</td> 
   <td>Selecione o tipo de armazenamento em que a imagem é armazenada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Editar opções</td> 
   <td>Defina quaisquer opções de edição que deseja aplicar à imagem.<p>Para obter detalhes sobre opções, consulte <a href="https://developer.adobe.com/firefly-services/docs/lightroom/api/#operation/applyEdits">Aplicar edições do Lightroom</a> na documentação da API do Adobe Firefly Lightroom.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Armazenamento de saída</td> 
    <td>Selecione onde deseja que o arquivo de saída seja armazenado. <p>O armazenamento interno do Fusion não armazena a imagem fora do cenário, mas permite que outros módulos no cenário acessem a imagem.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de saída</td> 
   <td>Selecione o tipo de arquivo para o arquivo de saída.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Substituir</td> 
   <td>Selecione sim se quiser permitir que o módulo substitua a saída se ela já existir. Isso se aplica somente ao armazenamento em nuvem do Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualidade</td> 
   <td>Insira ou mapeie a qualidade da imagem de saída. 1 é a qualidade mais baixa e 12 é a mais alta. Isso se aplica somente a arquivos JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Aplicar predefinições do Lightroom

Este módulo aplica uma ou mais predefinições do XMP Lightroom à imagem fornecida, usando os arquivos XMP de predefinição fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly Lightroom, consulte <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Criar uma conexão com o Adobe Firefly Lightroom</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL da imagem</td> 
   <td>Insira ou mapeie um URL pré-assinado que represente a imagem à qual você deseja aplicar o XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de armazenamento</td> 
   <td>Selecione o tipo de armazenamento em que a imagem é armazenada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Predefinições</td> 
   <td>Para cada predefinição que deseja aplicar, clique em <b>Adicionar item</b>, insira a URL pré-assinada da predefinição e selecione seu tipo de armazenamento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Armazenamento de saída</td> 
    <td>Selecione onde deseja que o arquivo de saída seja armazenado. <p>O armazenamento interno do Fusion não armazena a imagem fora do cenário, mas permite que outros módulos no cenário acessem a imagem.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de saída</td> 
   <td>Selecione o tipo de arquivo para o arquivo de saída.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Substituir</td> 
   <td>Selecione sim se quiser permitir que o módulo substitua a saída se ela já existir. Isso se aplica somente ao armazenamento em nuvem do Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualidade</td> 
   <td>Insira ou mapeie a qualidade da imagem de saída. 1 é a qualidade mais baixa e 12 é a mais alta. Isso se aplica somente a arquivos JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Endireitar automaticamente

Esse módulo endireita automaticamente uma imagem aplicando a transformação Auto Upright.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly Lightroom, consulte <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Criar uma conexão com o Adobe Firefly Lightroom</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL da imagem</td> 
   <td>Insira ou mapeie um URL pré-assinado que represente a imagem à qual você deseja aplicar o XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de armazenamento</td> 
   <td>Selecione o tipo de armazenamento em que a imagem é armazenada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Modo ereto</td> 
   <td>Selecione o tipo de modo Vertical que deseja usar. Se você não definir um valor, um modo apropriado será fornecido automaticamente.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Restringir corte</td> 
   <td>Selecione se a imagem endireitada deve ser cortada para remover todas as bordas em branco.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">Armazenamento de saída</td> 
    <td>Selecione onde deseja que o arquivo de saída seja armazenado. <p>O armazenamento interno do Fusion não armazena a imagem fora do cenário, mas permite que outros módulos no cenário acessem a imagem.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de saída</td> 
   <td>Selecione o tipo de arquivo para o arquivo de saída.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Substituir</td> 
   <td>Selecione sim se quiser permitir que o módulo substitua a saída se ela já existir. Isso se aplica somente ao armazenamento em nuvem do Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualidade</td> 
   <td>Insira ou mapeie a qualidade da imagem de saída. 1 é a qualidade mais baixa e 12 é a mais alta. Isso se aplica somente a arquivos JPEG.</td> 
  </tr> 
 </tbody> 
</table>


### Tom automático

Esse módulo corrige automaticamente a exposição, o contraste, a nitidez e a saturação em uma imagem.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly Lightroom, consulte <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Criar uma conexão com o Adobe Firefly Lightroom</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL da imagem</td> 
   <td>Insira ou mapeie um URL pré-assinado que represente a imagem à qual você deseja aplicar o XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de armazenamento</td> 
   <td>Selecione o tipo de armazenamento em que a imagem é armazenada.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Armazenamento de saída</td> 
    <td>Selecione onde deseja que o arquivo de saída seja armazenado. <p>O armazenamento interno do Fusion não armazena a imagem fora do cenário, mas permite que outros módulos no cenário acessem a imagem.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de saída</td> 
   <td>Selecione o tipo de arquivo para o arquivo de saída.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Substituir</td> 
   <td>Selecione sim se quiser permitir que o módulo substitua a saída se ela já existir. Isso se aplica somente ao armazenamento em nuvem do Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualidade</td> 
   <td>Insira ou mapeie a qualidade da imagem de saída. 1 é a qualidade mais baixa e 12 é a mais alta. Isso se aplica somente a arquivos JPEG.</td> 
  </tr> 
 </tbody> 
</table>


