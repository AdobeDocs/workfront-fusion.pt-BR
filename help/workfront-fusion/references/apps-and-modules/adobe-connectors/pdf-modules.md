---
title: Adobe PDF Services
description: Adobe PDF Services
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '4151'
ht-degree: 100%

---

# [!DNL Adobe PDF Services]

Com o Adobe Workfront Fusion [!DNL Adobe PDF Services], você pode extrair dados de um arquivo PDF ou gerar um novo arquivo PDF a partir dos dados fornecidos. Além disso, é possível converter diversos tipos de arquivo em PDFs ou PDFs em outros tipos de arquivo. Os PDF Services também permitem combinar, compactar ou ler metadados de um arquivo PDF, bem como controlar a proteção por senha no arquivo.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

Para obter informações sobre a API usada para os PDF Services, consulte [API de geração de documentos da Adobe](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html).

## Considerações de segurança ao usar [!DNL Adobe PDF Services]

Os [!DNL Adobe PDF Services] podem ler, converter ou modificar os arquivos, mas nem o [!DNL Adobe] nem o Workfront Fusion armazenam arquivos ou dados. Isso significa que:

* Você mantém controle sobre seus arquivos, incluindo a segurança deles
* Você não precisa ter uma conta de armazenamento ou de armazenamento na nuvem da [!UICONTROL Adobe] para usar os PDF Services.

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

Para criar uma conexão de servidor para servidor do OAuth, você deve adicionar a API dos Adobe PDF Services no Adobe Developers Console. Ao adicionar a API, selecione a opção Servidor para servidor do OAuth.

Para obter instruções, consulte [Adicionar API ao projeto usando credenciais de autenticação de usuário do OAuth](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication) na documentação do desenvolvedor da Adobe.

## Informações da API dos Adobe PDF Services

O conector Adobe PDF Services usa:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td>https://pdf-services-stage.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com [!DNL Adobe PDF Services]

Para criar uma conexão para os módulos do [!DNL Adobe PDF Services]:

1. Em qualquer módulo do [!DNL Adobe PDF Services], clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

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
            <p>Selecione se deseja criar uma conexão de servidor para servidor ou uma conexão JWT.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Insira um nome para essa conexão.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Insira sua [!UICONTROL Client ID] do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar as credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor da Adobe.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Insira seu [!UICONTROL Client Secret] do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar as credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor da Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Technical account ID] (somente JWT)</td>
          <td>Insira sua [!UICONTROL Technical account ID] do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar as credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor da Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Organization ID] (somente JWT)</td>
          <td>Insira sua [!UICONTROL Organization ID] do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].<p>Para obter instruções sobre como localizar as credenciais, consulte <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenciais</a> na documentação do desenvolvedor da Adobe.</p>
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
          <p>Para extrair a chave privada ou o certificado:</p>
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
              <p>Insira a senha do arquivo.</p>
            </li>
            <li value="5">
              <p>Clique em <b>[!UICONTROL Save]</b> para extrair o arquivo e retornar à configuração de conexão.</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.


## Módulos e campos do [!DNL Adobe PDF Services]

Ao configurar o [!DNL PDF Services], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Combinar arquivos PDF]](#combine-pdf-files)
* [[!UICONTROL Compactar arquivos PDF]](#compress-pdf-files)
* [[!UICONTROL Converter documento em arquivo PDF]](#convert-document-to-pdf-file)
* [[!UICONTROL Converter HTML em arquivo PDF]](#convert-html-to-pdf-file)
* [[!UICONTROL Converter imagem em arquivo PDF]](#convert-image-to-pdf-file)
* [[!UICONTROL Converter PDF em documento]](#convert-pdf-to-document)
* [[!UICONTROL Converter PDF em imagem]](#convert-pdf-to-image)
* [[!UICONTROL Extrair texto/tabela]](#extract-text--table)
* [[!UICONTROL Gerar documento]](#generate-document)
* [[!UICONTROL Linearizar um arquivo PDF]](#linearize-a-pdf-file)
* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [[!UICONTROL OCR para arquivo PDF]](#ocr-for-pdf-file)
* [[!UICONTROL Manipulação de página]](#page-manipulation)
* [[!UICONTROL Tag automática de acessibilidade de PDF]](#pdf-accessibility-auto-tag)
* [[!UICONTROL Propriedades do arquivo PDF]](#pdf-file-properties)
* [[!UICONTROL Proteger arquivo PDF]](#protect-pdf-file)
* [[!UICONTROL Remover proteção de um arquivo PDF]](#remove-protection-of-a-pdf-file)
* [Dividir um arquivo PDF](#split-a-pdf-file)

### [!UICONTROL Combinar arquivos PDF]

Este módulo de ação obtém vários arquivos PDF e os combina em um só. Por exemplo, este módulo pode combinar todos os documentos de um projeto do [!UICONTROL Workfront] em um único PDF após a conclusão do projeto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents]</td> 
   <td> <p>Você pode usar um módulo agregador para coletar documentos a serem combinados em um PDF ou pode adicionar os documentos manualmente. </p> <p>Recomendamos usar um módulo [!UICONTROL Array Aggregator] para agregar resultados de um módulo anterior. Ao usar um agregador, você não precisa saber os nomes, os locais ou os números de arquivos a serem combinados. Portanto, o uso de um agregador é muito mais flexível e escalonável do que inserir manualmente os documentos a serem combinados.</p> <p>Para usar o módulo de arquivos [!UICONTROL Combine PDF] com um agregador, é necessário habilitar o mapeamento no campo [!UICONTROL Documents]. </p> <p>Neste exemplo, o módulo [!UICONTROL Read Related Records] identifica os documentos associados a um projeto, e o módulo [!UICONTROL Download Documents] baixa cada um. Todos os PDFs são agregados em uma matriz, que é passada para o módulo de arquivos [!UICONTROL Combine PDF].</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>Também é possível inserir documentos manualmente.</p> <p>Para cada documento a ser incluído no PDF combinado:</p> 
    <ol> 
     <li value="1"> <p>Clique em [!UICONTROL Add a Document]</p> </li> 
     <li value="2"> <p>No campo [!UICONTROL Source file], selecione o módulo que gera o documento que você deseja incluir ou mapeie o nome e os dados do arquivo de origem. </p> </li> 
     <li value="3"> <p>(Opcional) Se desejar incluir apenas determinadas páginas do arquivo de origem, para cada intervalo de páginas que deseja adicionar, clique em <strong>[!UICONTROL Add item]</strong> no campo [!UICONTROL Pages]. Em seguida, insira a primeira e a última página do intervalo de páginas a ser incluído e clique em <strong>[!UICONTROL Add]</strong>. É possível incluir mais de um intervalo de páginas de um único documento.</p> </li> 
     <li value="4"> <p>Clique em <strong>[!UICONTROL Add]</strong>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Compactar arquivos PDF]

Este módulo de ação obtém um arquivo PDF e o compacta. Isso pode ser útil para preservar a largura de banda ou a memória.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
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

### [!UICONTROL Converter documento em arquivo PDF]

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
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
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
     <li> <p>ca-ES: catalão (Espanha)</p> </li> 
     <li> <p>cs-CZ: tcheco (República Tcheca)</p> </li> 
     <li> <p>da-DK: dinamarquês (Dinamarca)</p> </li> 
     <li> <p>de-DE: alemão (Alemanha)</p> </li> 
     <li> <p>en-AE: inglês (Emirados Árabes Unidos)</p> </li> 
     <li> <p>en-GB: inglês (Reino Unido)</p> </li> 
     <li> <p>en-IL: inglês (Israel)</p> </li> 
     <li> <p>en-US: inglês (Estados Unidos da América)</p> </li> 
     <li> <p>es-ES: espanhol (Espanha)</p> </li> 
     <li> <p>es-MX: espanhol (México)</p> </li> 
     <li> <p>eu-ES: basco (Espanha)</p> </li> 
     <li> <p>fi-FI: finlandês (Finlândia)</p> </li> 
     <li> <p>fr-CA: francês (Canadá)</p> </li> 
     <li> <p>fr-FR: francês (França)</p> </li> 
     <li> <p>fr-MA: francês (Marrocos)</p> </li> 
     <li> <p>hr-HR: croata (Croácia)</p> </li> 
     <li> <p>hu-HU: húngaro (Hungria)</p> </li> 
     <li> <p>it-IT: italiano (Itália)</p> </li> 
     <li> <p>ja-JP: japonês (Japão)</p> </li> 
     <li> <p>kr-KR: coreano (Coreia do Sul)</p> </li> 
     <li> <p>nb-NO: norueguês bokmål (Noruega)</p> </li> 
     <li> <p>nl-NL: holandês (Holanda)</p> </li> 
     <li> <p>pl-PL: polonês (Polônia)</p> </li> 
     <li> <p>pt-BR: português (Brasil)</p> </li> 
     <li> <p>pt-PT: português (Portugal)</p> </li> 
     <li> <p>ro-RO: romeno (Romênia)</p> </li> 
     <li> <p>ru-RU: russo (Rússia)</p> </li> 
     <li> <p>sk-SK: eslovaco (Eslováquia)</p> </li> 
     <li> <p>sl-SI: esloveno (Eslovênia)</p> </li> 
     <li> <p>sv-SE: sueco (Suécia)</p> </li> 
     <li> <p>tr-TR: turco (Turquia)</p> </li> 
     <li> <p>uk-UA: ucraniano (Ucrânia)</p> </li> 
     <li> <p>zh-CN: chinês (China continental)</p> </li> 
     <li> <p>zh-TW: chinês (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converter HTML em arquivo PDF]

Esta ferramenta converte um arquivo HTML em PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>Importante: o arquivo de origem deve estar no formato HTML ou ZIP. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>Se o HTML fizer referência a variáveis do JavaScript, você poderá incluí-las aqui. </p> <p>Para cada variável, clique em <strong>[!UICONTROL Add item]</strong> e inclua a chave e o valor da variável.</p> <p>Observação:   
     <ul> 
      <li> <p>Ao criar um PDF a partir de um arquivo ZIP, o material de apoio de origem deve incluir um elemento de script, como: <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code> </p> </li> 
      <li> <p>Ao criar um PDF a partir de um URL, o conteúdo do objeto JSON é inserido na VM do navegador antes da página ser renderizada. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include header and footer]</td> 
   <td> <p>Habilite essa opção para criar cabeçalhos e rodapés para o documento PDF.</p> 
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

### [!UICONTROL Converter imagem em arquivo PDF]

Esta ferramenta converte uma imagem em um arquivo PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome do arquivo de origem e o arquivo de imagem.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converter PDF em documento]

Esta ferramenta converte um arquivo PDF em documento. Você pode selecionar um dos formatos a seguir para o arquivo de saída.

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
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Files Format]</td> 
   <td> <p>Selecione o formato no qual deseja que os arquivos sejam gerados:</p> 
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
     <li> <p>ca-ES: catalão (Espanha)</p> </li> 
     <li> <p>cs-CZ: tcheco (República Tcheca)</p> </li> 
     <li> <p>da-DK: dinamarquês (Dinamarca)</p> </li> 
     <li> <p>de-DE: alemão (Alemanha)</p> </li> 
     <li> <p>en-AE: inglês (Emirados Árabes Unidos)</p> </li> 
     <li> <p>en-GB: inglês (Reino Unido)</p> </li> 
     <li> <p>en-IL: inglês (Israel)</p> </li> 
     <li> <p>en-US: inglês (Estados Unidos da América)</p> </li> 
     <li> <p>es-ES: espanhol (Espanha)</p> </li> 
     <li> <p>es-MX: espanhol (México)</p> </li> 
     <li> <p>eu-ES: basco (Espanha)</p> </li> 
     <li> <p>fi-FI: finlandês (Finlândia)</p> </li> 
     <li> <p>fr-CA: francês (Canadá)</p> </li> 
     <li> <p>fr-FR: francês (França)</p> </li> 
     <li> <p>fr-MA: francês (Marrocos)</p> </li> 
     <li> <p>hr-HR: croata (Croácia)</p> </li> 
     <li> <p>hu-HU: húngaro (Hungria)</p> </li> 
     <li> <p>it-IT: italiano (Itália)</p> </li> 
     <li> <p>ja-JP: japonês (Japão)</p> </li> 
     <li> <p>kr-KR: coreano (Coreia do Sul)</p> </li> 
     <li> <p>nb-NO: norueguês bokmål (Noruega)</p> </li> 
     <li> <p>nl-NL: holandês (Holanda)</p> </li> 
     <li> <p>pl-PL: polonês (Polônia)</p> </li> 
     <li> <p>pt-BR: português (Brasil)</p> </li> 
     <li> <p>pt-PT: português (Portugal)</p> </li> 
     <li> <p>ro-RO: romeno (Romênia)</p> </li> 
     <li> <p>ru-RU: russo (Rússia)</p> </li> 
     <li> <p>sk-SK: eslovaco (Eslováquia)</p> </li> 
     <li> <p>sl-SI: esloveno (Eslovênia)</p> </li> 
     <li> <p>sv-SE: sueco (Suécia)</p> </li> 
     <li> <p>tr-TR: turco (Turquia)</p> </li> 
     <li> <p>uk-UA: ucraniano (Ucrânia)</p> </li> 
     <li> <p>zh-CN: chinês (China continental)</p> </li> 
     <li> <p>zh-TW: chinês (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converter PDF em imagem]

Esta ferramenta converte um PDF em imagem no formato PNG ou JPEG, que é então gerada como uma lista ou combinada em um ZIP.

Se for gerado como um ZIP, o PDF será convertido em uma imagem por página e cada imagem terminará com o número da página. Os arquivos de imagem são combinados em um arquivo ZIP.

Por exemplo, um arquivo chamado &quot;TestFile&quot; com 8 páginas gerará 8 imagens, denominadas de &quot;TestFile_1&quot; a &quot;TestFile_8&quot;. A saída do módulo é um arquivo ZIP que contém as 8 imagens.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Files Format]</td> 
   <td> <p>Selecione o formato no qual deseja que os arquivos sejam gerados:</p> 
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

### [!UICONTROL Extrair texto/tabela]

Este módulo de ação permite extrair dados de um arquivo PDF. O módulo gera elementos de texto individuais, como um parágrafo, ou o texto em uma única célula de uma tabela.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elementos a serem extraídos como JSON]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Text]</p> </li> 
     <li> <p>[!UICONTROL Tables]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Extract Bounding boxes?]</td> 
   <td>Habilite essa opção para extrair dados sobre a caixa delimitadora do texto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Incluir informação de estilo na saída?]</td> 
   <td>Habilite essa opção para adicionar informações de estilo ao JSON de saída.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Gerar documento]

O módulo [!UICONTROL Gerar documento] é uma maneira poderosa de criar um PDF que contenha os dados selecionados. Você pode formatá-lo usando um modelo do [!DNL Microsoft Word] ou fornecendo dados no formato JSON.

Para obter mais informações sobre a funcionalidade Gerar documento do [!UICONTROL [!DNL Adobe PDF Services]], consulte a seção [Visão geral da geração de documento](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html) na documentação do [!DNL Adobe Document Services].

* [Usar o módulo [!UICONTROL Gerar documento] com um modelo do  [!DNL Microsoft Word] ](#use-the-generate-document-module-with-a-microsoft-word-template)
* [Usar o módulo [!UICONTROL Gerar documento] com JSON](#use-the-generate-document-module-with-json)

#### Usar o módulo [!UICONTROL Gerar documento] com um modelo do [!DNL Microsoft Word]


>[!NOTE]
>
>Para ver uma discussão sobre modelos do Microsoft Word, consulte [Módulos de modelos do Microsoft Word](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md).
>
>Não é necessário usar os módulos de modelo do Microsoft Word para usar um modelo do Microsoft Word com o módulo Gerar documento dos PDF Services.


Para usar o módulo [!UICONTROL Gerar documento] com um modelo do [!UICONTROL Microsoft Word], você deve primeiro criar o modelo. Para obter instruções, procure &quot;Criar um modelo&quot; na documentação do [!DNL Microsoft Office].

Preencha os campos do módulo [!UICONTROL Gerar documento] da seguinte maneira:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>Esse arquivo de origem é o modelo do [!DNL Microsoft Word] que o módulo usa para gerar o novo PDF.</p> <p>Recomendamos criar um projeto no Workfront para os modelos do [!DNL Microsoft Word] que você usa no Workfront Fusion. Em seguida, você pode usar o Workfront &gt; módulo [!UICONTROL Download document] para inserir o modelo apropriado em seu cenário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p>Selecione o formato para o documento gerado.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data for merge]</td> 
   <td> <p>Para cada tag de valor no modelo que você deseja substituir por texto, preencha o seguinte:</p> 
    <ul> 
     <li> <p>[!UICONTROL Key]</p> <p>Insira uma chave. No modelo, a chave é o texto mostrado na tag de valor. Por exemplo, se você deseja inserir texto na tag de valor <code>&#123;&#123;name&#125;&#125;</code>, insira <code>name </code>no campo de chave.</p> </li> 
     <li> <p>Tipo de valor</p> <p>Selecione se os dados no campo de valor são um valor, um objeto ou uma matriz de objetos.</p> </li> 
     <li> <p>[!UICONTROL Value]</p> <p>Insira ou mapeie o texto que você deseja que apareça no documento gerado no lugar da tag de valor.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Usar o módulo [!UICONTROL Gerar documento] com JSON

Para usar o módulo [!UICONTROL Gerar documento] com JSON, preencha os campos da seguinte maneira:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p>Selecione o formato para o documento gerado.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data for merge]</td> 
   <td> <p>Para usar JSON neste módulo, habilite o mapeamento neste campo.</p> <p>Insira ou mapeie o JSON a partir do qual o documento será gerado. </p> <p>Você pode digitar JSON diretamente nesse campo ou mapear a saída de JSON de um módulo JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Linearizar um arquivo PDF]

Esta ferramenta lineariza um documento PDF para criar um documento PDF otimizado para a Web. Um documento PDF linearizado pode ser exibido página por página sem que seja necessário baixar o documento inteiro.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Fazer uma chamada de API personalizada

Este módulo de ação cria uma solicitação HTTP personalizada para a API dos PDF Services.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
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
   <td> <p>Adicione a consulta para a chamada de API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Para cada campo que você deseja adicionar à chamada de API, clique em <b>Adicionar item</b> e insira a chave do campo e o valor opcional.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code>, no JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL OCR para arquivo PDF]

Esta ferramenta executa o reconhecimento de caracteres ópticos (OCR) em um arquivo e gera um PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Selecione o idioma deste documento.<p>Para opções de idioma, consulte <a href="#convert-document-to-pdf-file" class="MCXref xref" >Converter documento em arquivo PDF</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR type]</td> 
   <td> 
    <ul> 
     <li> <p>O tipo [!UICONTROL Modified original image] garante que o texto seja pesquisável e selecionável, mas modifica a imagem original durante o processo de limpeza (por exemplo, desentorta a imagem) antes de colocar uma camada de texto invisível sobre ela. Esse tipo remove artefatos indesejados e pode resultar em um documento mais legível em alguns cenários. </p> </li> 
     <li> <p>O tipo [!UICONTROL Unchanged original image] também sobrepõe uma camada de texto pesquisável sobre a imagem original, mas nesse caso, a imagem original não é alterada. Esse tipo produz fidelidade máxima à imagem original.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Manipulação de página]

Este módulo permite girar ou excluir seletivamente as páginas em um documento PDF. Por exemplo, você pode alterar o modo de exibição de retrato para paisagem ou remover determinadas páginas do documento PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> <p>Selecione a ação que deseja executar no arquivo.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Delete]</b> </p> <p>Selecione essa opção para excluir páginas do documento.</p><p>Para cada intervalo de páginas a ser excluído, clique em <strong>[!UICONTROL Add]</strong> e insira a primeira e a última página do intervalo. </p> <p>Observação:   
     <ul> 
      <li> <p>Você pode usar números negativos para contar de trás para frente a partir do final do documento. A última página de um documento é -1, penúltima é -2, e assim por diante.</p> </li> 
      <li> <p>Para excluir uma página única, defina o mesmo número de página como o de início e o de fim do intervalo.</p></ul> </li> 
     <li> <p><b>[!UICONTROL Rotate]</b> </p> <p>Selecione essa opção para girar as páginas e, em seguida, insira o ângulo, em graus no sentido horário, que você deseja girar as páginas do documento em relação à sua orientação inicial.</p> <p>Para girar de retrato para paisagem ou vice-versa, gire a página 90 ou 270 graus.</p> <p>Se uma página estiver de cabeça para baixo, gire-a 180 graus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pages]</td> 
   <td> <p>Para cada intervalo de páginas a ser excluído, clique em <strong>[!UICONTROL Add]</strong> e insira a primeira e a última página do intervalo. </p> <p>Observação:   
     <ul> 
      <li> <p>Você pode usar números negativos para contar de trás para frente a partir do final do documento. A última página de um documento é -1, penúltima é -2, e assim por diante.</p> </li> 
      <li> <p>Para excluir uma página única, defina o mesmo número de página como o de início e o de fim do intervalo.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros com os quais você deseja que o módulo trabalhe durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Tag automática de acessibilidade de PDF]

Este módulo de ação cria um PDF marcado com tags para casos de uso de acessibilidade. Ele também cria um relatório opcional do Microsoft Excel que lista problemas e sugere correções.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
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
   <td> <p>Habilite esta opção para gerar um relatório que lista os problemas de acessibilidade no PDF, juntamente com a sua localização e dá sugestões sobre como corrigi-los.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Propriedades do arquivo PDF]

Esta ferramenta extrai informações básicas sobre o documento, como:

* Contagem de páginas
* Versão do PDF
* Se o arquivo está criptografado
* Se o arquivo está linearizado
* Se o arquivo contém arquivos incorporados

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Proteger um arquivo PDF]

Esta ferramenta protege um documento PDF com uma senha de usuário ou proprietário. Ela também define restrições em determinados recursos, como impressão, edição e cópia no documento PDF. Você seleciona o tipo de conteúdo a ser criptografado e o algoritmo de criptografia.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password Protection Type]</td> 
   <td> <p>Habilite esta opção para usar senhas para criptografar o documento PDF de entrada. Se você habilitar essa opção, especifique e insira um valor para um ou ambos os campos a seguir: </p> 
    <ul> 
     <li> <p>[!UICONTROL User Password]</p> </li> 
     <li> <p>[!UICONTROL Owner Password] </p> </li> 
    </ul> <p>Cada senha pode ter até 128 caracteres.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encryption Algorithm]</td> 
   <td> <p>Selecione o algoritmo de criptografia. </p> 
    <ul> 
     <li> <p>[!UICONTROL AES-128 encryption]</p> <p>A senha aceita somente caracteres LATIN-I. </p> </li> 
     <li> <p>[!UICONTROL AES-256 encryption]</p> <p>A senha aceita um conjunto de caracteres Unicode</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content to Encrypt]</td> 
   <td> <p>Selecione o tipo de conteúdo a ser criptografado.</p> 
    <ul> 
     <li> <p>[!UICONTROL All content]</p> </li> 
     <li> <p>[!UICONTROL All content except metadata]</p> </li> 
     <li> <p>[!UICONTROL Only embedded data] </p> </li> 
    </ul> <p>Selecionar "[!UICONTROL Only embedded data]" renderiza as permissões de acesso fornecidas como ineficazes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permissions]</td> 
   <td> <p>Selecione as permissões que deseja incluir para permitir impressão, edição ou cópia de conteúdo.</p> <p>As configurações de permissão só serão usadas se a [!UICONTROL Owner Password] estiver definida no campo [!UICONTROL Password Protection Type].</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Remover proteção de um arquivo PDF]

Esta ferramenta remove a segurança (proteção por senha) de um documento PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p>O arquivo de origem deve estar no formato PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password]</td> 
   <td>Insira a senha que protege o arquivo atualmente.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Dividir um arquivo PDF]

Este módulo de ação divide um documento PDF em vários documentos menores. Especifique se deseja dividir o documento por número de arquivos, páginas por arquivo ou intervalos de páginas.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecione a conexão a ser usada para este módulo.</p> Para obter instruções sobre como criar uma conexão com o [!DNL Adobe PDF Services], consulte <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe PDF Services]</a> neste artigo. </td> 
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
   <li><p><b>Contagem de arquivos</b></p><p>Insira o número de arquivos de tamanho igual em que você deseja dividir o documento.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

