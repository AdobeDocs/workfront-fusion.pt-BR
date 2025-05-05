---
title: Módulos do Adobe Photoshop
description: Com os módulos do Adobe Photoshop, você pode iniciar um cenário do Adobe Workfront Fusion com base em eventos em sua conta do Adobe Photoshop, criar, ler ou atualizar contratos e outros registros, pesquisar registros usando critérios definidos e fazer upload de documentos.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
source-git-commit: db1d6f5bf29063b069681395c6ff6d3554c67dc3
workflow-type: tm+mt
source-wordcount: '4359'
ht-degree: 0%

---

# [!DNL Adobe Photoshop] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Adobe Photoshop], bem como conectá-los a vários aplicativos e serviços de terceiros.


Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++**Expanda para exibir os requisitos de acesso para a funcionalidade deste artigo.**

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
      <td>
        <p>[!UICONTROL Pro] ou superior</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
      <td>
        <p>[!UICONTROL Plano], [!UICONTROL Trabalho]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td>
      <td >
        <p>[!UICONTROL Workfront Fusion para Automação e Integração do Trabalho]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produto</td>
      <td>Sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</td>
    </tr>
    </tr>
  </tbody>
</table>


&#42;Para saber qual plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

&#42;&#42;Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL [Adobe Workfront Fusion] licenses]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Antes de usar o conector [!DNL Adobe Photoshop], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!DNL Adobe Photoshop] ativa.
* Você deve ter uma licença dos Serviços da Firefly.
* Você deve ter uma ID de cliente e um Segredo do cliente. Você pode adquiri-los na Adobe Developer Console.

## Informações da API do Adobe Photoshop

O conector do Adobe Photoshop usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com [!DNL Adobe Photoshop]

Para criar uma conexão para seus módulos do [!DNL Adobe Photoshop]:

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
        <td role="rowheader">[!UICONTROL ID do Cliente]</td>
        <td>Insira sua [!UICONTROL Adobe] [!UICONTROL ID do cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira seu [!DNL Adobe] [!UICONTROL Segredo do Cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID da conta técnica]</td>
        <td>Insira sua [!DNL Adobe] [!UICONTROL ID da conta técnica]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID da Organização]</td>
        <td>Insira sua [!DNL Adobe] [!UICONTROL ID da Organização]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Chave privada]</td>
        <td>
          <p>Insira a chave privada gerada quando suas credenciais foram criadas no [!DNL Adobe Developer Console]. </p>
          <p>Para extrair sua chave privada ou certificado:</p>
          <ol>
            <li value="1">
              <p>Clique em <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selecione o tipo de arquivo que você está extraindo.</p>
            </li>
            <li value="3">
              <p>Selecione o arquivo que contém a chave privada ou o certificado.</p>
            </li>
            <li value="4">
              <p>Digite a senha do arquivo.</p>
            </li>
            <li value="5">
              <p>Clique em <b>Salvar</b> para extrair o arquivo e retornar à configuração de conexão.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## [!DNL Adobe Photoshop] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Photoshop], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Photoshop] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aplicar edições no PSD](#apply-psd-edits)
* [Corrigir uma imagem com cor automática](#auto-color-correct-an-image)
* [Converter formato de imagem](#convert-image-format)
* [Criar uma máscara](#create-a-mask)
* [Criar uma nova PSD](#create-a-new-psd)
* [Editar camadas de texto](#edit-text-layers)
* [Executar desfoque de profundidade](#execute-depth-blur)
* [Executar ações do Photoshop](#execute-photoshop-actions)
* [Executar ações do Photoshop (JSON)](#execute-photoshop-actions-json)
* [Executar corte do produto](#execute-product-crop)
* [Obter informações da camada](#get-layer-info)
* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Remover plano de fundo](#remove-background)
* [Substituir um objeto inteligente](#replace-a-smart-object)
* [Redimensionar uma imagem](#resize-an-image)
* [Marca d&#39;água em uma imagem](#watermark-an-image)

### Aplicar edições no PSD

Esse módulo de ação aplica uma variedade de edições de documento e nível de camada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da imagem) Altura]</p>
      </td>
      <td> Insira ou mapeie a altura da imagem em pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da imagem) Largura]</p>
      </td>
      <td> Insira ou mapeie a largura da imagem em pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da tela de desenho) Superior]</p>
      </td>
   <td> Insira ou mapeie, em pixels, a coordenada y do canto superior esquerdo do documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da tela de desenho) Inferior]</p>
      </td>
   <td> Insira ou mapeie, em pixels, a coordenada y do canto inferior direito do documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da tela de desenho) à esquerda]</p>
      </td>
   <td> Insira ou mapeie, em pixels, a coordenada x do canto superior esquerdo do documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da tela de desenho) Direita]</p>
      </td>
   <td> Insira ou mapeie, em pixels, a coordenada x do canto inferior direito do documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento) Cortar]</p>
      </td>
   <td> Selecione Pixels transparentes para basear o corte em pixels transparentes na imagem. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Fonte padrão]</p>
      </td>
   <td> Digite o nome completo do postscript da fonte a ser usada como padrão global para o documento. Essa fonte será usada para qualquer camada de texto que tenha uma fonte ausente e nenhuma outra fonte tenha sido especificamente fornecida para essa camada. Se esta fonte estiver ausente, a opção especificada em Gerenciar fontes ausentes entrará em vigor. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Fontes]</p>
      </td>
   <td> Para cada fonte que o documento precisa, clique em Adicionar item e insira o local de armazenamento e o local do arquivo da fonte. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Gerenciar fontes ausentes]</p>
      </td>
   <td> Selecione a ação a ser tomada se houver uma ou mais fontes ausentes no documento. <ul><li><code>fail</code>: A tarefa não será bem-sucedida e o status será definido como Falha, com os detalhes do erro fornecidos na seção de detalhes no status.</li><li><code>useDefault</code>: a tarefa será bem-sucedida, no entanto, por padrão, todas as fontes ausentes serão substituídas por ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Camadas]</p>
      </td>
   <td> Para cada camada que deseja adicionar, clique em Adicionar item e preencha os detalhes da camada. <p>Para obter detalhes sobre opções de camada, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_applyPsdEdits/">Aplicar edições de PSD</a> na documentação do Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Saídas]</td>
      <td>
        <p>Para cada arquivo convertido que deseja criar, clique em Add item e insira o armazenamento, o local e o tipo, conforme listado nesta tabela.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de resultados retornados]</p>
      </td>
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
    </tr>
    </tbody>
</table>



### Corrigir uma imagem com cor automática

Essa cor automática do módulo de ação corrige a imagem especificada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o arquivo que você deseja corrigir as cores está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo cuja cor você deseja corrigir. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de resultados retornados]</p>
      </td>
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
    </tr>
    </tbody>
</table>


### Converter formato de imagem

Esse módulo de ação converte um arquivo em JPEG, PNG, PSD ou TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo do qual você deseja remover o plano de fundo está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo do qual deseja remover o plano de fundo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Saídas]</td>
      <td>
        <p>Para cada arquivo convertido que deseja criar, clique em Add item e insira o armazenamento, o local e o tipo, conforme listado nesta tabela.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de resultados retornados]</p>
      </td>
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
    </tr>
    </tbody>
</table>



### Criar uma máscara

Este módulo de ação retorna um arquivo PNG com um mastro aplicado ao redor do assunto.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo do qual você deseja criar uma máscara está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo a partir do qual deseja criar uma máscara. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo de máscara seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo de máscara será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de cor]</p>
      </td>
   <td>Selecione se a imagem de saída usa cores RGB ou RGBA. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Formato de máscara]</p>
      </td>
   <td>Selecione se a máscara deve ser suave (difusa) ou binária. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Otimizar]</p>
      </td>
   <td>Selecione Desempenho para otimizar a velocidade ou Lote para permitir o tempo de espera. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Pós-processamento]</p>
      </td>
   <td></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Versão]</p>
      </td>
   <td>O padrão é 4,0</td> 
    </tr> 
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de resultados retornados]</p>
      </td>
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
    </tr>
    </tbody>
</table>

### Criar uma nova PSD

Esse módulo de ação cria uma nova PSD com camadas opcionais e gera representações ou salva como um PSD.

Para campos relacionados a este módulo, consulte [Criar uma nova PSD](https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/documentCreate) na documentação do Adobe Photoshop.

### Editar camadas de texto

Esse módulo de ação edita camadas de texto em um arquivo do Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gerenciar fontes ausentes]</td>
      <td>
        <p>Selecione a ação a ser tomada se houver uma ou mais fontes ausentes no documento. Se a fonte não for fornecida, o módulo usará a fonte padrão.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fonte padrão]  </td>
      <td>
        <p>Digite o nome completo do postscript da fonte a ser usada como padrão global para o documento. Essa fonte será usada para qualquer camada de texto que tenha uma fonte ausente e nenhuma outra fonte tenha sido especificamente fornecida para essa camada. Se esta fonte estiver ausente, a opção especificada em Gerenciar fontes ausentes entrará em vigor.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Camadas]</td>
   <td> <p>Para obter detalhes sobre opções de camada, consulte <a href="https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/text">Editar camada de texto</a> na documentação do Adobe Photoshop.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de saída]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de saída]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de arquivo de saída]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compactação]</p>
      </td>
   <td> Selecione o nível de compactação para o arquivo de saída. </td> 
    </tr>
  </tbody>
</table>



### Executar ações do Photoshop (JSON)

Esse módulo de ação executa ações do Photoshop usando comandos JSON.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ação JSON]</td>
      <td>
        <p>Insira o comando JSON para a ação que deseja realizar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fontes / Padrões / Pincéis / Imagens adicionais]</td>
      <td>
        <p>Para cada fonte, padrão, pincel ou imagem adicional que você deseja usar nesta ação, clique em Adicionar item e insira o armazenamento e o local do arquivo do item.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Fonte / Padrão / URL do arquivo de Pincel]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja usar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gera armazenamento de arquivos de saída]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de saída]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de arquivo de saída]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compactação]</p>
      </td>
   <td> Selecione o nível de compactação para o arquivo de saída. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Saídas]</td>
      <td>
        <p>Para cada arquivo convertido que deseja criar, clique em Add item e insira o armazenamento, o local e o tipo, conforme listado nesta tabela.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de resultados retornados]</p>
      </td>
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
    </tr>
      </tbody>
</table>

### Executar desfoque de profundidade

Esse módulo de ação executa o Desfoque de Profundidade no arquivo selecionado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de saída]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de saída]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de arquivo de saída]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outros campos]</td>
      <td>
        <p>Para obter detalhes sobre outras opções de Desfoque de Profundidade, consulte <a href="https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/depthBlur">Executar Desfoque de Profundidade </a>na documentação da API do Adobe Photoshop.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compactação]</p>
      </td>
   <td> Selecione o nível de compactação para o arquivo de saída. </td> 
    </tr>
  </tbody>
</table>

### Executar ações do Photoshop

Esse módulo de ação executa uma ação Photoshop na imagem selecionada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ações armazenamento de arquivo]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o arquivo de ações está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de ações]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo de ações. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nome da ação]</p>
      </td>
   <td> Se desejar executar apenas uma ação específica, você pode especificar qual ação executar a partir do ActionSet. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de fonte / padrão / pincel]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que deseja usar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Fonte / Padrão / URL do arquivo de Pincel]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja usar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de saída]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de saída]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de arquivo de saída]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compactação]</p>
      </td>
   <td> Selecione o nível de compactação para o arquivo de saída. </td> 
    </tr>
  </tbody>
</table>

### Executar corte do produto

Esse módulo de ação executa o Recorte de produto na imagem selecionada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o arquivo que você deseja cortar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que você deseja cortar. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Unidade]</p>
      </td>
   <td> Selecione se deseja descrever o ajuste de altura e largura em pixels ou como uma porcentagem. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Largura]</p>
      </td>
   <td> Insira ou mapeie a quantidade de preenchimento de largura que deseja adicionar. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Altura]</p>
      </td>
   <td> Insira ou mapeie a quantidade de preenchimento de altura que deseja adicionar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de saída]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de saída]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de arquivo de saída]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compactação]</p>
      </td>
   <td> Selecione o nível de compactação para o arquivo de saída. </td> 
    </tr>
  </tbody>
</table>

### Obter informações da camada

Esse módulo de ação recupera informações de camada do arquivo PSD especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivo no qual o arquivo do qual você deseja recuperar as informações de camada é armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo do qual deseja recuperar as informações da camada. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Miniaturas]</p>
      </td>
   <td> </td> 
    </tr>
  </tbody>
</table>

### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada personalizada para a API do Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Insira um caminho relativo para <code>https://image.adobe.io/pie/psdService</code>. Exemplo: <code>/photoshopActions</code></p>
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
        <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cadeia de Consulta]  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### Remover plano de fundo

Este módulo de ação identifica o assunto principal da imagem e remove o plano de fundo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo do qual você deseja remover o plano de fundo está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo do qual deseja remover o plano de fundo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de cor]</p>
      </td>
   <td>Selecione se a imagem de saída usa cores RGB ou RGBA. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Formato de máscara]</p>
      </td>
   <td>Selecione se as bordas da imagem devem ser suaves (difusas) ou binárias. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Otimizar]</p>
      </td>
   <td>Selecione Desempenho para otimizar a velocidade ou Lote para permitir o tempo de espera. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Pós-processamento]</p>
      </td>
   <td></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Versão]</p>
      </td>
   <td>O padrão é 4,0</td> 
    </tr> 
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de resultados retornados]</p>
      </td>
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
    </tr>
    </tbody>
</table>



### Substituir um objeto inteligente

Esse módulo de ação substitui um Objeto inteligente em uma camada do PSD e gera novas representações.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o Objeto Inteligente está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do Objeto inteligente. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Camadas]</p>
      </td>
   <td>Para cada camada que você deseja adicionar ao Objeto inteligente, clique em Adicionar item e Insira o nome ou ID do objeto, o serviço de arquivos onde o Objeto inteligente está armazenado e o URL ou caminho da camada.<p>Para obter descrições das configurações dos avanços nesta área, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">Substituir um objeto inteligente</a> na documentação da API do Photoshop </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Saídas]</td>
      <td>
        <p>Para cada nova representação que você deseja que o módulo produza, clique em Adicionar item e preencha os campos a seguir. Você pode ter no máximo 25 arquivos de saída.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Largura de Saída)]</p>
      </td>
   <td> A largura, em pixels, do arquivo de saída. O módulo preservará a proporção original. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de resultados retornados]</p>
      </td>
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
    </tr>
    </tbody>
</table>



### Redimensionar uma imagem

Essa ação redimensiona uma imagem usando a mesma proporção.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivo onde o arquivo que você deseja redimensionar está armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Local do arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que você deseja redimensionar.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Saídas]</td>
      <td>
        <p>Para cada arquivo convertido que você deseja criar, clique em Add item e insira o armazenamento, o local e outras opções conforme listado nesta tabela.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Largura]</p>
      </td>
   <td>Insira um número que represente a largura, em pixels, da imagem redimensionada. A proporção será preservada.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Largura máxima]</p>
      </td>
   <td>Quando a largura for 0, Max com poderá ser fornecido para obter o tamanho. A largura máxima tem precedência sobre uma largura menor que a largura do documento.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Aparar na tela]</p>
      </td>
   <td>Selecione Sim para recortar as representações para o tamanho da Tela de Pintura ou Não para criar o Tamanho da Camada de representações.</td> 
    </tr>
    </tbody>
</table>

### Marca d&#39;água em uma imagem

Esse módulo de ação adiciona uma marca d&#39;água à imagem selecionada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Base / Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo ao qual você deseja adicionar uma marca d'água está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Base / Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo ao qual você deseja adicionar uma marca d'água. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Marca D'Água / Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual a marca d'água que você deseja adicionar está armazenada.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Marca D'Água / Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual a marca d'água que você deseja adicionar está armazenada.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Marca D'Água / Limites) Altura]</p>
      </td>
   <td>Insira ou mapeie a altura desejada da marca d'água em pixels.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Marca D'Água / Limites) Largura]</p>
      </td>
   <td> Insira ou mapeie a largura desejada da marca d'água em pixels. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Marca D'Água / Limites) Esquerda]</p>
      </td>
   <td> Insira ou mapeie a distância em pixels do lado esquerdo da imagem que a marca d'água deve estar.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Marca D'Água / Limites) Superior]</p>
      </td>
   <td> Insira ou mapeie a distância em pixels a partir da parte superior da imagem que a marca d'água deve estar.</td> 
    </tr>  
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo de marca d'água seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo de marca d'água será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Largura de Saída)]</p>
      </td>
   <td> A largura, em pixels, do arquivo de saída. O módulo preservará a proporção original. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de resultados retornados]</p>
      </td>
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
    </tr>
    </tbody>
</table>
