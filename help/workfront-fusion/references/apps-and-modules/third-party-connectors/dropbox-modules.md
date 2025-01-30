---
title: módulos Dropbox
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Dropbox, bem como conectá-lo a vários aplicativos e serviços de terceiros. Isso permite automatizar atividades como monitoramento, pesquisa, recuperação, listagem, criação e edição de arquivos e pastas no Dropbox.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 29ce5940-4d71-4719-ab5e-f03c44b28c8c
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '2876'
ht-degree: 0%

---

# [!DNL Dropbox] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!UICONTROL Dropbox] ou [!DNL Dropbox Business], bem como conectá-los a vários aplicativos e serviços de terceiros. Isso permite automatizar atividades como monitoramento, pesquisa, recuperação, listagem, criação e edição de arquivos e pastas no [!UICONTROL Dropbox].

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano [!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Adobe Workfront], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Pré-requisitos

* Para usar módulos [!DNL Dropbox], você deve ter uma conta [!DNL Dropbox].

>[!IMPORTANT]
>
>O Dropbox deve aprovar aplicativos com mais de 50 usuários.
>
>Para obter mais informações, pesquise por &quot;Aprovação de produção&quot; no guia do desenvolvedor de Dropbox.

## Informações da API do Dropbox

O conector Dropbox usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.dropboxapi.com/2    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> 2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td><ul><li><p>Dropbox</p><p>v5.3.9</p></li><li><p>Dropbox Business</p><p>v1.0.12</p></li></ul></td> 
  </tr>
 </tbody> 
 </table>


## Criar uma conexão com [!DNL Dropbox]

Para criar uma conexão para seus módulos do [!DNL Dropbox]:

1. Clique em **[!UICONTROL Add]** ao lado da caixa Conexão.

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
          <p>Insira um nome para esta conexão.</p>
        </td>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Selecione se essa conexão é para um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira seu [!UICONTROL Dropbox] [!UICONTROL Client ID]. </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira seu [!DNL Dropbox] [!UICONTROL Client Secret]. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Account Type]</td>
        <td>Selecione se você está se conectando a uma conta Dropbox pessoal ou conta comercial (Dropbox Business).</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continue]** para salvar a conexão e retornar ao módulo.## [!DNL Dropbox] módulos e seus campos

## [!DNL Dropbox] módulos e seus campos

Ao configurar módulos do [!DNL Dropbox], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Dropbox] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Módulos acionadores](#trigger-modules)
* [Módulos para obter  [!DNL Dropbox]  arquivos e pastas](#modules-for-getting-dropbox-files-and-folders)
* [Módulos para criação e edição [!DNL Dropbox] de arquivos e pastas](#modules-for-creating-and-editing-dropbox-files-and-folders)
* [Outros módulos](#other-modules)

### Módulos acionadores

#### [!UICONTROL Watch Files]

Este módulo de tipo de Acionador retorna detalhes do arquivo quando ele é modificado em uma pasta especificada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta que deseja observar alterações.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch also subfolders]</td> 
   <td> <p> Habilite esta opção para também monitorar subpastas na pasta selecionada para arquivos modificados.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit] </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Módulos para obter [!DNL Dropbox] arquivos e pastas

* [[!UICONTROL Search Files/Folders]](#search-filesfolders)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Get a Folder Metadata]](#get-a-folder-metadata)
* [[!UICONTROL List All Files/Subfolders in a Folder]](#list-all-filessubfolders-in-a-folder)
* [[!UICONTROL List File Revisions]](#list-file-revisions)

#### [!UICONTROL Search Files/Folders]

Este módulo de pesquisa procura registros em um objeto em [!DNL Dropbox] que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Insira o termo de pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione a pasta que deseja pesquisar. Este módulo pesquisa a [!DNL Dropbox] inteira se você não selecionar uma pasta.</p> </td> 
  </tr> 
  <tr> 
   <td>Status do arquivo</td> 
   <td> <p> Selecione o status do arquivo para restringir a pesquisa ao status do arquivo selecionado.</p> </td> 
  </tr> 
  <tr> 
   <td>Categorias de arquivo</td> 
   <td> <p> Selecione as categorias de arquivo para restringir a pesquisa às categorias selecionadas.</p> </td> 
  </tr> 
  <tr> 
   <td>Extensões de arquivo</td> 
   <td> <p> Escolha as extensões de arquivo que deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Este módulo de ação baixa um arquivo de uma pasta.

Especifique o arquivo e seu local.

O módulo retorna a ID do arquivo e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

>[!NOTE]
>
>Esse módulo é útil para fornecer arquivos aos módulos subsequentes.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Forma de selecionar arquivos</td> 
   <td> <p> Selecione se deseja mapear o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Caminho do arquivo / Arquivo</p> </td> 
   <td> <p style="font-weight: bold;">Caminho do arquivo</p> <p>Insira ou mapeie o caminho de destino para o arquivo.</p> <p style="font-weight: bold;">Arquivo</p> <p>Selecione o arquivo no menu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Folder Metadata]

Este módulo de ação recupera os detalhes da pasta compartilhada.

Especifique a ID da pasta.

O módulo retorna a ID da pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>ID da Pasta Compartilhada</td> 
   <td> <p> Insira ou mapeie a ID da pasta da qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List All Files/Subfolders in a Folder]

Este módulo de ação lista arquivos ou pastas em uma pasta específica.

Especifique a ID da pasta.

O módulo retorna as IDs dos arquivos ou pastas e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Lista </td> 
   <td> <p>Selecione se deseja recuperar arquivos ou pastas.</p> </td> 
  </tr> 
  <tr> 
   <td>Mostrar apenas arquivos baixáveis</td> 
   <td> <p> Habilite esta opção para retornar somente os arquivos baixáveis. Alguns tipos de arquivos, como o Google Docs, não podem ser baixados.</p> </td> 
  </tr> 
  <tr> 
   <td>Pasta </td> 
   <td> <p>Insira ou mapeie a pasta da qual deseja recuperar arquivos ou pastas.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo liste durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List File Revisions]

Este módulo de ação recupera todas as revisões de arquivo (um histórico de versões) de um arquivo específico.\
Especifique a ID do arquivo.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Forma de selecionar arquivos</td> 
   <td> <p> Selecione se deseja mapear o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Caminho do arquivo / Arquivo</p> </td> 
   <td> <p style="font-weight: bold;">Caminho do arquivo</p> <p>Insira ou mapeie o caminho de destino para o arquivo.</p> <p style="font-weight: bold;">Arquivo</p> <p>Selecione o arquivo no menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Limite</p> </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo liste durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Módulos para criação e edição de [!DNL Dropbox] arquivos e pastas

* [[!UICONTROL Upload] um arquivo](#upload-a-file)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Create/Overwrite a Text File]](#createoverwrite-a-text-file)
* [[!UICONTROL Create/Update a Share Link]](#createupdate-a-share-link)
* [[!UICONTROL Restore a File]](#restore-a-file)
* [[!UICONTROL Move a File/Folder]](#move-a-filefolder)
* [[!UICONTROL Rename a File/Folder]](#rename-a-filefolder)
* [[!UICONTROL Delete a File/Folder]](#delete-a-filefolder)

#### [!UICONTROL Upload a File]

Este módulo de ação faz upload de um arquivo para uma pasta.

Especifique informações como o local do arquivo, o arquivo que deseja fazer upload e um novo nome opcional para o arquivo.

O módulo retorna a ID do arquivo e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td> <p> Selecione a pasta do [!DNL Dropbox] para a qual você deseja carregar o arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Insira ou mapeie o arquivo que deseja adicionar à pasta [!DNL Dropbox] selecionada acima.</p> <p style="font-weight: bold;">[!UICONTROL File name]</p> <p>Insira ou mapeie o nome do arquivo, incluindo a extensão.</p> <p style="font-weight: bold;">[!UICONTROL File data]</p> <p>Insira ou mapeie os dados do arquivo (do módulo anterior, como [!UICONTROL Google Drive] &gt;[!UICONTROL Get a File)].</p> <p>Observação: o tamanho máximo do arquivo carregado é de 150 MB.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Overwrite an existing file]</td> 
   <td> <p> Habilite esta opção para substituir o arquivo existente pelo novo arquivo. Se essa opção for deixada desativada, o arquivo carregado será renomeado.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

Este módulo de ação cria uma nova pasta.

Especifique o caminho e um nome para a pasta.

O módulo retorna a ID da pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name] </td> 
   <td> <p>Insira o nome da nova pasta.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Insira ou mapeie o caminho onde deseja criar uma nova pasta.</p> <p>Nota:   <p>Se estiver usando uma conta do [!DNL Dropbox Business] (com espaços de equipe), você deve remover a barra <code>/</code>, ou não clique em <strong>[!UICONTROL Click here] para escolher a pasta </strong> para criar uma pasta de equipe na raiz.</p> <p>Se a barra não for removida, um erro <code>[409] path/malformed_path/..</code> será retornado.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Auto rename]</td> 
   <td> <p> Ative esta opção para renomear a nova pasta, se uma pasta com o mesmo nome já existir no local de destino.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Overwrite a Text File]

Esse módulo de ação cria um arquivo DOC ou substitui o conteúdo de um existente.

Especifique o arquivo de origem e a pasta.

O módulo retorna a ID da pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select to]</td> 
   <td> <p> Selecione se deseja criar ou substituir um arquivo DOC.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecione o local de destino em que deseja criar um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Insira ou mapeie o arquivo que deseja adicionar à pasta [!DNL Dropbox].</p> <p style="font-weight: bold;">Nome do arquivo</p> <p>Insira o nome do novo arquivo DOC (sem uma extensão).</p> <p style="font-weight: bold;">Conteúdo do arquivo</p> <p>Insira o conteúdo de texto do arquivo DOC.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Share Link]

Este módulo de ação cria um link público para um arquivo.

Especifique o arquivo e as informações sobre o link.

O módulo retorna a ID do link e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path / File]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File Path]</p> <p>Insira ou mapeie o caminho de destino para o arquivo.</p> <p style="font-weight: bold;">[!UICONTROL File]</p> <p>Selecione o arquivo no menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Requested Visibility]</p> </td> 
   <td> <p>Selecione se o link é público, para equipe ou com senha restrita.</p> <p>Observação: as opções [!UICONTROL Team only] e [!UICONTROL Access with password] estão disponíveis somente para usuários com [!DNL Dropbox Pro] ou versão superior.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Link's Expiration Date]</td> 
   <td> <p> Insira a data e a hora em que o link expirará e não estará mais acessível. Se esse campo ficar vazio, o link não expirará. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> <p>Observação: as opções [!UICONTROL Team only] e [!UICONTROL Access with password] estão disponíveis somente para usuários com [!UICONTROL Dropbox Pro] ou versões superiores.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Link's Access Level]</p> </td> 
   <td> <p>Defina a permissão para o recipient do link.</p> <p><strong>[!UICONTROL Viewer]</strong> Os usuários que usam o link podem exibir e comentar no conteúdo.</p> <p><strong>[!UICONTROL Editor]</strong> Os usuários que usam o link podem editar, exibir e comentar no conteúdo.</p> <p><strong>[!UICONTROL Max]</strong> Os usuários que usam o link recebem o nível de acesso máximo para o qual você pode definir o link.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Restore a File]

Este módulo de ação restaura uma versão anterior de um arquivo.

Especifique o arquivo e o número da revisão desejada.

O módulo retorna a ID da versão e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path] / [!UICONTROL File]</p> </td> 
   <td> <p><strong>[!UICONTROL File Path]</strong> </p> <p>Insira ou mapeie o caminho de destino para o arquivo.</p> <p><strong>[!UICONTROL File]</strong> </p> <p>Selecione o arquivo no menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Revision]</p> </td> 
   <td> <p>Informe ou mapeie o número da revisão que deseja restaurar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder]

Este módulo de ação move um arquivo ou pasta para um local diferente.

Especifique o arquivo ou pasta e como e onde deseja movê-lo.

O módulo retorna a ID do arquivo ou pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files] </td> 
   <td> <p>Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File/Folder Path] / [!UICONTROL File/Folder]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File/Folder Path]</p> <p>Insira ou mapeie o caminho de destino para o arquivo ou pasta.</p> <p style="font-weight: bold;">[!UICONTROL File/Folder]</p> <p>Selecione o arquivo ou pasta no menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL To Folder]</p> </td> 
   <td> <p>Insira ou mapeie o local de destino do arquivo ou pasta.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL New Name]</p> </td> 
   <td> <p>Digite o novo nome do arquivo ou pasta no novo local.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Auto Rename]</p> </td> 
   <td> <p>Habilite esta opção para garantir que, se existir um arquivo ou pasta com o mesmo nome, o módulo renomeie o novo arquivo ou pasta adicionando ([!UICONTROL NUMBER]) após o nome do arquivo ou pasta. Caso contrário, o arquivo ou pasta no local de destino será substituído.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Allow ownership transfer]</p> </td> 
   <td> <p>Ative essa opção para permitir movimentações por proprietário, mesmo que resulte em uma transferência de propriedade para o conteúdo que está sendo movido.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rename a File/Folder]

Esse módulo de ação renomeia um arquivo ou pasta.

Especifique o arquivo ou pasta e o novo nome.

O módulo retorna a ID do arquivo ou pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Forma de selecionar arquivos</td> 
   <td> <p> Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Caminho de arquivo/pasta/Arquivo/Pasta</p> </td> 
   <td> <p style="font-weight: bold;">Caminho do arquivo/pasta</p> <p>Insira ou mapeie o caminho de destino para o arquivo ou pasta.</p> <p style="font-weight: bold;">Arquivo/Pasta</p> <p>Selecione o arquivo ou pasta no menu.</p> </td> 
  </tr> 
  <tr> 
   <td>Renomear </td> 
   <td> <p>Insira o [!UICONTROL target name] para o arquivo, incluindo a extensão.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File/Folder]

Este módulo de ação exclui um arquivo ou pasta.

Especifique o arquivo ou pasta.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path] / [!UICONTROL File]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File Path]</p> <p>Insira ou mapeie o caminho de destino para o arquivo.</p> <p style="font-weight: bold;">[!UICONTROL File]</p> <p>Selecione o arquivo no menu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outros módulos

#### [!UICONTROL Make an API Call]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Dropbox]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Dropbox].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Digite um caminho relativo a Digite um caminho relativo a <code>https://api.dropboxapi.com</code>. Por exemplo, <code>/2/files/list_folder</code></p> <p>Observação: para obter a lista de pontos de extremidade disponíveis, consulte a <a href="https://www.dropbox.com/developers/documentation/http/documentation">Documentação da API v2 do Dropbox</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers] </td> 
   <td> <p>Insira os cabeçalhos de solicitação desejados. [!DNL Workfront Fusion] adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p> Insira a string de consulta da solicitação.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body] </td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:   <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemplo:** a chamada de API a seguir retorna os primeiros 10 arquivos da pasta [!DNL /Text files] da sua conta [!DNL Dropbox]:
>
>URL: `/2/files/list_folder`
>
>Corpo:
> 
>`{`
>
>`"path": "/Text files",`
>
>`"limit": 10,`
>
>`"recursive": false,`
>
>`"include_deleted": false`
>
>`}`
>
>Correspondências da pesquisa podem ser encontradas na Saída do módulo em [!UICONTROL Bundle] > [!UICONTROL Body] > entradas.
>
>No nosso exemplo, 10 tíquetes foram retornados:

## Problemas comuns

* [Não é possível carregar ou atualizar um arquivo](#unable-to-upload-or-update-a-file)
* [A imagem referenciada por um link compartilhado não é renderizada](#image-referenced-via-a-shared-link-does-not-render)

### Não é possível carregar ou atualizar um arquivo

Há várias situações em que ocorre uma falha no upload ou na atualização de um arquivo:

* O arquivo carregado é muito grande e excede o tamanho máximo de arquivo permitido para o plano [!DNL Dropbox], ou você usou toda a cota de armazenamento da sua conta [!DNL Dropbox]. Você deve excluir arquivos existentes da sua conta [!DNL Dropbox] ou atualizar seu plano.
* A pasta selecionada anteriormente, para a qual o arquivo está sendo carregado, não existe mais. O cenário é interrompido e você deve selecionar a pasta de destino novamente.

### A imagem referenciada por um link compartilhado não é renderizada

A URL retornada por [!UICONTROL Dropbox] >[!UICONTROL Create a shared link] não está vinculada diretamente a uma imagem, mas a uma página [!DNL Dropbox]. Para forçar o download da imagem, substitua o `?dl=0` à direita por `?dl=1`. Para forçar a imagem a ser renderizada (por exemplo, em um navegador da Web ou no Facebook Messenger), anexe `&raw=1` à URL.

Se você precisar obter o link direto ou bruto da imagem para o seu site ou para outros módulos do [!DNL Workfront Fusion], modifique a URL compartilhada inicial da seguinte maneira:

URL original:

`https://www.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png?dl=0`

1. Substituir `www` por `dl`.
1. Remover `?dl=0`.

URL final:

`https://dl.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png`

Para modificar automaticamente a URL, você pode usar a função `replace()` duas vezes:

* Substituir www por dl

  ![Substituir www por dl](/help/workfront-fusion/references/apps-and-modules/assets/www-to-dl-350x32.png)

* E para remover ?dl=0

  ![Remover DL](/help/workfront-fusion/references/apps-and-modules/assets/remove-dl0-350x33.png)

Para fazer isso em uma etapa, combine estas funções:

![Substituir ambos](/help/workfront-fusion/references/apps-and-modules/assets/replace-both-350x47.png)

Também é possível copiá-la e colá-la no campo. Substituir `1.url` pela URL.

```
{{replace(replace(1.url; "?dl=0"; ""); "www"; "dl")}}
```
