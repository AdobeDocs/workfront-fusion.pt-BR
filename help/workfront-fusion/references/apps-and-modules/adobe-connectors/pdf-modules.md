---
title: Serviços da Adobe PDF
description: Serviços da Adobe PDF
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: 757580687ff5d1617f83432952d9870bd697925e
workflow-type: tm+mt
source-wordcount: '3623'
ht-degree: 0%

---

# [!DNL Adobe PDF Services]

Com o [!DNL Adobe Workfront Fusion] [!DNL Adobe PDF Services], você pode extrair dados de um arquivo de PDF ou gerar um novo arquivo de PDF dos dados fornecidos. Além disso, você pode converter uma variedade de tipos de arquivos em PDF ou PDF em outros tipos de arquivos. Os Serviços de PDF também permitem combinar, compactar ou ler metadados para um arquivo PDF, bem como controlar a proteção por senha no arquivo.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

Para obter informações sobre a API usada para Serviços PDF, consulte [API de Geração de Documentos Adobe](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html).

## Considerações de segurança ao usar [!DNL Adobe PDF Services]

O [!DNL Adobe PDF Services] pode ler, converter ou modificar seus arquivos, mas nem o [!DNL Adobe] nem o [!DNL Workfront Fusion] armazenam seus arquivos ou dados. Isso significa que:

* Você tem controle sobre seus arquivos, incluindo a segurança deles
* Você não precisa ter uma conta de armazenamento [!UICONTROL Adobe] ou de armazenamento na nuvem para usar os Serviços PDF.

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Herdados: Automação e integração do Workfront Fusion for Work </p>
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

## Pré-requisitos

Para criar uma conexão servidor a servidor OAuth, você deve adicionar a API de serviços da Adobe PDF no Console de desenvolvedores do Adobe. Ao adicionar a API, selecione a opção Servidor para servidor do OAuth.

Para obter instruções, consulte [Adicionar API ao projeto usando OAuth](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/) na documentação do desenvolvedor de Adobe.

## Informações da API de serviços da Adobe PDF

O Adobe PDF Services Connector usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://pdf-services-stage.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com [!DNL Adobe PDF Services]

Para criar uma conexão para seus módulos do [!DNL Adobe PDF Services]:

1. Em qualquer módulo [!DNL Adobe PDF Services], clique em **[!UICONTROL Add]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Selecione se deseja criar uma conexão servidor a servidor ou uma conexão JWT.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Insira um nome para esta conexão.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Client ID]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] de [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor do Adobe.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Client Secret]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] de [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor do Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Technical account ID] (somente JWT)</td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Technical account ID]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] de [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor do Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Organization ID] (somente JWT)</td>
          <td>Insira seu [!DNL Adobe] [!UICONTROL Organization ID]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] de [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor do Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Meta scopes] (somente JWT)</td>
          <td>
            Insira todos os metaescopos necessários para a conexão.
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Se você selecionou uma conexão JWT, insira a chave privada que foi gerada quando suas credenciais foram criadas no [!DNL Adobe Developer Console]. </p>
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
              <p>Clique em <b>[!UICONTROL Save]</b> para extrair o arquivo e retornar à configuração de conexão.</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. Clique em **[!UICONTROL Continue]** para salvar a conexão e retornar ao módulo.


## [!DNL Adobe PDF Services] módulos e seus campos

Quando você configura o [!DNL PDF Services], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Combine PDF files]](#combine-pdf-files)
* [[!UICONTROL Compress PDF files]](#compress-pdf-files)
* [[!UICONTROL Convert document to PDF file]](#convert-document-to-pdf-file)
* [[!UICONTROL Convert HTML to PDF file]](#convert-html-to-pdf-file)
* [[!UICONTROL Convert image to PDF file]](#convert-image-to-pdf-file)
* [[!UICONTROL Convert PDF to document]](#convert-pdf-to-document)
* [[!UICONTROL Convert PDF to image]](#convert-pdf-to-image)
* [[!UICONTROL Extract Text / Table]](#extract-text--table)
* [[!UICONTROL Generate document]](#generate-document)
* [[!UICONTROL Linearize a PDF file]](#linearize-a-pdf-file)
* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [[!UICONTROL OCR for PDF file]](#ocr-for-pdf-file)
* [[!UICONTROL Page manipulation]](#page-manipulation)
* [[!UICONTROL PDF accessibility auto-tag]](#pdf-accessibility-auto-tag)
* [[!UICONTROL PDF file properties]](#pdf-file-properties)
* [[!UICONTROL Protect PDF file]](#protect-pdf-file)
* [[!UICONTROL Remove protection of a PDF file]](#remove-protection-of-a-pdf-file)
* [Dividir um arquivo PDF](#split-a-pdf-file)

### [!UICONTROL Combine PDF files]

Esse módulo de ação pega vários arquivos de PDF e os combina em um único arquivo de PDF. Por exemplo, este módulo poderia combinar todos os documentos em um projeto [!UICONTROL Workfront] em um único PDF após a conclusão do projeto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents]</td> 
   <td> <p>Você pode usar um módulo agregador para coletar documentos para combiná-los em um PDF, ou pode adicionar os documentos manualmente. </p> <p>Recomendamos usar um módulo [!UICONTROL Array Aggregator] para agregar a saída de um módulo anterior. Ao usar um agregador, você não precisa saber os nomes, locais ou números de arquivos a serem combinados. Portanto, usar um agregador é muito mais flexível e escalável do que inserir manualmente os documentos a serem combinados.</p> <p>Para usar o módulo de arquivos [!UICONTROL Combine PDF] com um agregador, você deve habilitar o mapeamento no campo [!UICONTROL Documents]. </p> <p>Neste exemplo, o módulo [!UICONTROL Read Related Records] identifica documentos associados a um projeto, e o módulo [!UICONTROL Download Documents] baixa cada um. Todos os PDF são agregados em uma matriz, que é passada para o módulo de arquivos [!UICONTROL Combine PDF].</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>Também é possível inserir documentos manualmente.</p> <p>Para cada documento a ser incluído no PDF combinado:</p> 
    <ol> 
     <li value="1"> <p>Clique em [!UICONTROL Add a Document]</p> </li> 
     <li value="2"> <p>No campo [!UICONTROL Source file], selecione o módulo que gera o documento que você deseja incluir ou mapeie o nome e os dados do arquivo de origem. </p> </li> 
     <li value="3"> <p>(Opcional) Se quiser incluir apenas determinadas páginas do arquivo de origem, para cada intervalo de páginas que deseja adicionar, clique em <strong>[!UICONTROL Add item]</strong> no campo [!UICONTROL Pages], em seguida, insira a primeira e a última página do intervalo de páginas a ser incluído e clique em <strong>[!UICONTROL Add]</strong>. É possível incluir mais de um intervalo de páginas de um único documento.</p> </li> 
     <li value="4"> <p>Clique em <strong>[!UICONTROL Add]</strong>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Compress PDF files]

Esse módulo de ação pega um arquivo PDF e o compacta. Isso pode ser útil para conservar largura de banda ou memória.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compression level]</td> 
   <td>Selecione o nível de compactação que deseja usar.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert document to PDF file]

Esta ferramenta converte um documento em um arquivo PDF. O arquivo de origem deve ter um dos seguintes formatos de documento:

* DOC
* XLS
* PPT
* TXT
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar em um dos seguintes formatos:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>Selecione o idioma padrão para o documento de origem. Isso permite que o módulo selecione uma fonte apropriada, se a fonte não estiver incluída no arquivo de origem.</p> <p>Selecione um dos seguintes idiomas:</p> 
    <ul> 
     <li> <p>en-US (Padrão): inglês (Estados Unidos da América)</p> </li> 
     <li> <p>ca-ES: Catalão (Espanha)</p> </li> 
     <li> <p>cs-CZ: Tcheco (República Tcheca)</p> </li> 
     <li> <p>da-DK: Dinamarquês (Dinamarca)</p> </li> 
     <li> <p>de-DE: Alemão (Alemanha)</p> </li> 
     <li> <p>en-AE: inglês (Emirados Árabes Unidos)</p> </li> 
     <li> <p>en-GB: inglês (Reino Unido)</p> </li> 
     <li> <p>en-IL: Inglês (Israel)</p> </li> 
     <li> <p>en-US: inglês (Estados Unidos da América)</p> </li> 
     <li> <p>es-ES: Espanhol (Espanha)</p> </li> 
     <li> <p>es-MX: espanhol (México)</p> </li> 
     <li> <p>eu-ES: Basco (Espanha)</p> </li> 
     <li> <p>fi-FI: Finlandês (Finlândia)</p> </li> 
     <li> <p>fr-CA: francês (Canadá)</p> </li> 
     <li> <p>fr-FR: Francês (França)</p> </li> 
     <li> <p>fr-MA: francês (Marrocos)</p> </li> 
     <li> <p>hr-HR: Croata (Croácia)</p> </li> 
     <li> <p>hu-HU: Húngaro (Hungria)</p> </li> 
     <li> <p>it-IT: Italiano (Itália)</p> </li> 
     <li> <p>ja-JP: Japonês (Japão)</p> </li> 
     <li> <p>kr-KR: Coreano (Coreia do Sul)</p> </li> 
     <li> <p>nb-NO: Norueguês Bokmål (Noruega)</p> </li> 
     <li> <p>nl-NL: Holandês (Holanda)</p> </li> 
     <li> <p>pl-PL: Polonês (Polônia)</p> </li> 
     <li> <p>pt-BR: Português (Brasil)</p> </li> 
     <li> <p>pt-PT: Português (Portugal)</p> </li> 
     <li> <p>ro-RO: Romeno (Romênia)</p> </li> 
     <li> <p>ru-RU: Russo (Rússia)</p> </li> 
     <li> <p>sk-SK: Eslovaco (Eslováquia)</p> </li> 
     <li> <p>sl-SI: Esloveno (Eslovênia)</p> </li> 
     <li> <p>sv-SE: Sueco (Suécia)</p> </li> 
     <li> <p>tr-TR: Turco (Turquia)</p> </li> 
     <li> <p>uk-UA: ucraniano (Ucrânia)</p> </li> 
     <li> <p>zh-CN: Chinês (China continental)</p> </li> 
     <li> <p>zh-TW: chinês (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert HTML to PDF file]

Esta ferramenta converte um arquivo HTML em um arquivo PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>Importante: o arquivo do Source deve estar no formato HTML ou ZIP. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>Se o HTML fizer referência às variáveis do JavaScript, você poderá incluir essas variáveis aqui. </p> <p>Para cada variável, clique em <strong>[!UICONTROL Add item]</strong> e inclua a chave e o valor da variável.</p> <p>Nota:   
     <ul> 
      <li> <p>Ao criar um PDF de um arquivo ZIP, o material de apoio de origem deve incluir um elemento de script como: <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code> </p> </li> 
      <li> <p>Ao criar um PDF a partir de um URL, o conteúdo desse objeto JSON é inserido na VM do navegador antes que a página seja renderizada. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include header and footer]</td> 
   <td> <p>Habilite esta opção para criar cabeçalhos e rodapés para o documento PDF.</p> 
    <ul> 
     <li> <p>O cabeçalho inclui uma data e o título do documento.</p> </li> 
     <li> <p>O rodapé inclui o nome do arquivo e um número de página.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page width]</td> 
   <td>Insira a largura do papel, em polegadas. O módulo usa essas informações para formatar as páginas no arquivo PDF criado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page height]</td> 
   <td>Insira a altura do papel, em polegadas. O módulo usa essas informações para formatar as páginas no arquivo PDF criado.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert image to PDF file]

Esta ferramenta converte uma imagem em um arquivo PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de origem e o arquivo de imagem.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert PDF to document]

Esta ferramenta converte um arquivo PDF em um documento. Você pode selecionar um dos formatos a seguir para o arquivo de saída.

* DOC
* DOCX
* PPTX
* XLSX
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Files Format]</td> 
   <td> <p>Selecione o formato como o qual você deseja que os arquivos sejam gerados:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>Selecione o idioma padrão para o documento de origem. Isso permite que o módulo selecione uma fonte apropriada, se a fonte não estiver incluída no arquivo de origem.</p> <p>Selecione um dos seguintes idiomas:</p> 
    <ul> 
     <li> <p>en-US (Padrão): inglês (Estados Unidos da América)</p> </li> 
     <li> <p>ca-ES: Catalão (Espanha)</p> </li> 
     <li> <p>cs-CZ: Tcheco (República Tcheca)</p> </li> 
     <li> <p>da-DK: Dinamarquês (Dinamarca)</p> </li> 
     <li> <p>de-DE: Alemão (Alemanha)</p> </li> 
     <li> <p>en-AE: inglês (Emirados Árabes Unidos)</p> </li> 
     <li> <p>en-GB: inglês (Reino Unido)</p> </li> 
     <li> <p>en-IL: Inglês (Israel)</p> </li> 
     <li> <p>en-US: inglês (Estados Unidos da América)</p> </li> 
     <li> <p>es-ES: Espanhol (Espanha)</p> </li> 
     <li> <p>es-MX: espanhol (México)</p> </li> 
     <li> <p>eu-ES: Basco (Espanha)</p> </li> 
     <li> <p>fi-FI: Finlandês (Finlândia)</p> </li> 
     <li> <p>fr-CA: francês (Canadá)</p> </li> 
     <li> <p>fr-FR: Francês (França)</p> </li> 
     <li> <p>fr-MA: francês (Marrocos)</p> </li> 
     <li> <p>hr-HR: Croata (Croácia)</p> </li> 
     <li> <p>hu-HU: Húngaro (Hungria)</p> </li> 
     <li> <p>it-IT: Italiano (Itália)</p> </li> 
     <li> <p>ja-JP: Japonês (Japão)</p> </li> 
     <li> <p>kr-KR: Coreano (Coreia do Sul)</p> </li> 
     <li> <p>nb-NO: Norueguês Bokmål (Noruega)</p> </li> 
     <li> <p>nl-NL: Holandês (Holanda)</p> </li> 
     <li> <p>pl-PL: Polonês (Polônia)</p> </li> 
     <li> <p>pt-BR: Português (Brasil)</p> </li> 
     <li> <p>pt-PT: Português (Portugal)</p> </li> 
     <li> <p>ro-RO: Romeno (Romênia)</p> </li> 
     <li> <p>ru-RU: Russo (Rússia)</p> </li> 
     <li> <p>sk-SK: Eslovaco (Eslováquia)</p> </li> 
     <li> <p>sl-SI: Esloveno (Eslovênia)</p> </li> 
     <li> <p>sv-SE: Sueco (Suécia)</p> </li> 
     <li> <p>tr-TR: Turco (Turquia)</p> </li> 
     <li> <p>uk-UA: ucraniano (Ucrânia)</p> </li> 
     <li> <p>zh-CN: Chinês (China continental)</p> </li> 
     <li> <p>zh-TW: chinês (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert PDF to image]

Esta ferramenta converte um PDF para uma imagem no formato PNG ou JPEG., que é então emitido como uma lista ou combinado em um ZIP.

Se a saída for um ZIP, o PDF será convertido em uma imagem por página e cada imagem terminará com o número da página. Os arquivos de imagem são então combinados em um arquivo ZIP.

Por exemplo, um arquivo chamado &quot;TestFile&quot; com 8 páginas produziria 8 imagens, chamadas de &quot;TestFile_1&quot; a &quot;TestFile_8&quot;. A saída do módulo é um arquivo ZIP contendo as 8 imagens.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Files Format]</td> 
   <td> <p>Selecione o formato como o qual você deseja que os arquivos sejam gerados:</p> 
    <ul> 
     <li>Imagem PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output type]</td> 
   <td> <p>Selecione se deseja que os arquivos sejam gerados como uma lista de arquivos ou como um arquivo ZIP.</td> 
  </tr> 
  <tr> 
 </tbody> 
</table>

### [!UICONTROL Extract Text / Table]

Esse módulo de ação permite extrair dados de um arquivo PDF. O módulo gera elementos de texto individuais, como um parágrafo ou o texto em uma única célula de uma tabela.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elements that should be extracted as JSON]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Text]</p> </li> 
     <li> <p>[!UICONTROL Tables]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Extract Bounding boxes?]</td> 
   <td>Habilite esta opção para extrair dados sobre a caixa delimitadora do texto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include styling information for output?]</td> 
   <td>Ative essa opção para adicionar informações de estilo ao JSON de saída.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Generate document]

O módulo [!UICONTROL Generate document] é uma maneira poderosa de criar um PDF que contém os dados selecionados. Você pode formatá-lo usando um modelo [!DNL Microsoft Word] ou fornecendo dados no formato JSON.

Para obter mais informações sobre a funcionalidade [!UICONTROL [!DNL Adobe PDF Services] Generate document], consulte a [Visão Geral da Geração de Documento](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html) na documentação [!DNL Adobe Document Services].

* [Usar o módulo [!UICONTROL Generate document] com um  [!DNL Microsoft Word] modelo](#use-the-generate-document-module-with-a-microsoft-word-template)
* [Usar o módulo [!UICONTROL Generate document] com JSON](#use-the-generate-document-module-with-json)

#### Usar o módulo [!UICONTROL Generate document] com um modelo [!DNL Microsoft Word]


>[!NOTE]
>
>Para ver uma discussão sobre modelos do Microsoft Word, consulte [módulos de Modelo do Microsoft Word](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md).
>
>Não é necessário usar os módulos de modelo do Microsoft Word para usar um modelo do Microsoft Word com o módulo Gerar documento do PDF Services.


Para usar o módulo [!UICONTROL Generate document] com um modelo [!UICONTROL Microsoft Word], você deve primeiro criar o modelo. Para obter instruções, procure por &quot;Criar um modelo&quot; na documentação do [!DNL Microsoft Office].

Preencha os campos do módulo [!UICONTROL Generate document] da seguinte maneira:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>Esse arquivo de origem é o modelo [!DNL Microsoft Word] que o módulo usa para gerar o novo PDF.</p> <p>Recomendamos criar um projeto no [!DNL Workfront] para os modelos [!DNL Microsoft Word] que você usa no [!DNL Workfront Fusion]. Você pode usar o módulo [!DNL Workfront] &gt; [!UICONTROL Download document] para inserir o modelo apropriado em seu cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p>Selecione o formato do documento gerado.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data for merge]</td> 
   <td> <p>Para cada tag de valor no modelo que você deseja substituir por texto, preencha o seguinte:</p> 
    <ul> 
     <li> <p>[!UICONTROL Key]</p> <p>Insira uma chave. No modelo, a chave é o texto mostrado na tag de valor. Por exemplo, se você deseja colocar texto na marca de valor <code>&#123;&#123;name&#125;&#125;</code>, digite <code>name </code> no campo de chave.</p> </li> 
     <li> <p>Tipo de valor</p> <p>Selecione se os dados no campo de valor são um valor, um objeto ou uma matriz de objetos.</p> </li> 
     <li> <p>[!UICONTROL Value]</p> <p>Insira ou mapeie o texto que você deseja que apareça no documento gerado no lugar da marca de valor.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Usar o módulo [!UICONTROL Generate document] com JSON

Para usar o módulo [!UICONTROL Generate document] com JSON, preencha os campos da seguinte maneira:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p>Selecione o formato do documento gerado.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data for merge]</td> 
   <td> <p>Para usar o JSON neste módulo, você deve habilitar o mapeamento neste campo.</p> <p>Insira ou mapeie o JSON a partir do qual o documento será gerado. </p> <p>Você pode digitar o JSON diretamente neste campo ou mapear a saída JSON de um módulo JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Linearize a PDF file]

Esta ferramenta lineariza um documento de PDF para criar um documento de PDF otimizado para a Web. Um documento PDF linearizado pode ser exibido página por página sem a necessidade de baixar o documento inteiro.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Fazer uma chamada de API personalizada

Esse módulo de ação cria uma solicitação HTTP personalizada para a API de serviços do PDF.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> Insira um caminho relativo ou um URL. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Para cada campo que você deseja adicionar à chamada de API, clique em <b>Adicionar item</b> e insira a chave do campo e o valor opcional.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL OCR for PDF file]

Essa ferramenta executa o OCR (Optical Character Recognition, reconhecimento óptico de caracteres) em um arquivo e produz um PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Selecione o idioma deste documento.<p>Para opções de idioma, consulte <a href="#convert-document-to-pdf-file" class="MCXref xref" >Converter documento em arquivo de PDF</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR type]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Modified original image] O texto garante que seja possível pesquisá-lo e selecioná-lo, mas modifica a imagem original durante o processo de limpeza (por exemplo, o distorce) antes de colocar uma camada de texto invisível sobre ele. Esse tipo remove artefatos indesejados e pode resultar em um documento mais legível em alguns cenários. </p> </li> 
     <li> <p>[!UICONTROL Unchanged original image] o texto também sobrepõe uma camada de texto pesquisável sobre a imagem original, mas, nesse caso, a imagem original não é alterada. Esse tipo produz fidelidade máxima à imagem original.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Page manipulation]

Esse módulo permite que você gire ou exclua seletivamente as páginas de um documento PDF. Por exemplo, você pode alterar a visualização de retrato para paisagem ou remover determinadas páginas do documento PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> <p>Selecione a ação que deseja executar no arquivo.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Delete]</b> </p> <p>Selecione esta opção para excluir páginas do documento.</p><p>Para cada intervalo de páginas a ser excluído, clique em <strong>[!UICONTROL Add]</strong> e insira a primeira e a última página do intervalo de páginas. </p> <p>Nota:   
     <ul> 
      <li> <p>Você pode usar números negativos para contar do final do documento. A última página de um documento é -1, a segunda página à última é -2 e assim por diante.</p> </li> 
      <li> <p>Para excluir uma única página, defina o mesmo número de página que o início e o fim do intervalo.</p></ul> </li> 
     <li> <p><b>[!UICONTROL Rotate]</b> </p> <p>Selecione esta opção para girar as páginas e, em seguida, insira o ângulo, em graus no sentido horário, que você deseja girar as páginas do documento em relação à sua orientação inicial.</p> <p>Para girar de retrato para paisagem ou vice-versa, gire a página 90 ou 270 graus.</p> <p>Se uma página estiver de cabeça para baixo, gire-a 180 graus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pages]</td> 
   <td> <p>Para cada intervalo de páginas a ser excluído, clique em <strong>[!UICONTROL Add]</strong> e insira a primeira e a última página do intervalo de páginas. </p> <p>Nota:   
     <ul> 
      <li> <p>Você pode usar números negativos para contar do final do documento. A última página de um documento é -1, a segunda página à última é -2 e assim por diante.</p> </li> 
      <li> <p>Para excluir uma única página, defina o mesmo número de página que o início e o fim do intervalo.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF accessibility auto-tag]

Esse módulo de ação cria um PDF que é marcado para casos de uso de acessibilidade. Ele também cria um relatório opcional do Microsoft Excel que lista problemas e sugere correções.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shift Headings]</td> 
   <td> <p>Habilite esta opção para deslocar cabeçalhos no documento.</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generate Report]</td> 
   <td> <p>Habilite esta opção para gerar um relatório que liste os problemas de acessibilidade no PDF junto com seus locais, e dê sugestões sobre como corrigir esses problemas.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF file properties]

Esta ferramenta extrai informações básicas sobre o documento, como:

* Contagem de páginas
* versão do PDF
* Se o arquivo está criptografado
* Se o arquivo está linerizado
* Se o arquivo contém arquivos incorporados

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Protect a PDF file]

Esta ferramenta protege um documento PDF com uma senha de usuário ou proprietário. Também define restrições em determinados recursos, como impressão, edição e cópia no documento PDF. Você seleciona o tipo de conteúdo a ser criptografado e o algoritmo de criptografia.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password Protection Type]</td> 
   <td> <p>Habilite esta opção para usar senhas para criptografar o documento do PDF de entrada. Se você habilitar essa opção, deverá especificar e inserir um valor para um ou para ambos os itens a seguir: </p> 
    <ul> 
     <li> <p>[!UICONTROL User Password]</p> </li> 
     <li> <p>[!UICONTROL Owner Password] </p> </li> 
    </ul> <p>Cada senha pode ter até 128 caracteres.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encryption Algorithm]</td> 
   <td> <p>Selecione o algoritmo de criptografia. </p> 
    <ul> 
     <li> <p>[!UICONTROL AES-128 encryption]</p> <p>A senha aceita somente caracteres LATINO-I. </p> </li> 
     <li> <p>[!UICONTROL AES-256 encryption]</p> <p>A senha suporta o conjunto de caracteres Unicode</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content to Encrypt]</td> 
   <td> <p>Selecione o tipo de conteúdo a ser criptografado.</p> 
    <ul> 
     <li> <p>[!UICONTROL All content]</p> </li> 
     <li> <p>[!UICONTROL All content except metadata]</p> </li> 
     <li> <p>[!UICONTROL Only embedded data] </p> </li> 
    </ul> <p>Selecionar "[!UICONTROL Only embedded data]" renderiza qualquer permissão de acesso fornecida como ineficaz.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permissions]</td> 
   <td> <p>Selecione as permissões que deseja incluir para permitir impressão, edição ou cópia de conteúdo.</p> <p>As configurações de permissões só serão usadas se [!UICONTROL Owner Password] estiver definido no campo [!UICONTROL Password Protection Type].</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Remove protection of a PDF file]

Esta ferramenta remove a segurança (proteção por senha) de um documento PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password]</td> 
   <td>Digite a senha que protege o arquivo atualmente.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Split a PDF file]

Esse módulo de ação divide um documento PDF em vários documentos menores. Especifique se deseja dividi-la pelo número de arquivos, páginas por arquivo ou intervalos de páginas.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split option]</td> 
   <td>Selecione como deseja dividir o arquivo. 
   <ul>
   <li><p><b>Intervalos de páginas</b></p><p>Para cada intervalo de páginas que você deseja dividir em um documento separado, clique em <b>Adicionar</b> e insira a página inicial e a página final.</p></li>
   <li><p><b>Contagem de páginas</b></p><p>Insira o número de páginas que deseja incluir nos novos documentos.</p></li>
   <li><p><b>Conta do arquivo</b></p><p>Insira o número de arquivos de tamanho igual para os quais você deseja dividir o documento.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

