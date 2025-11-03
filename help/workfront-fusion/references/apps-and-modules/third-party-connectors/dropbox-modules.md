---
title: Módulos do Dropbox
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Dropbox, bem como conectá-lo a vários aplicativos e serviços de terceiros. Isso permite automatizar atividades como monitoramento, pesquisa, recuperação, listagem, criação e edição de arquivos e pastas no Dropbox.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 29ce5940-4d71-4719-ab5e-f03c44b28c8c
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '3292'
ht-degree: 0%

---

# [!DNL Dropbox] módulos

Em um cenário do Adobe Workfront Fusion, você pode automatizar fluxos de trabalho que usam o [!UICONTROL Dropbox] ou o [!DNL Dropbox Business], bem como conectá-lo a vários aplicativos e serviços de terceiros. Isso permite automatizar atividades como monitoramento, pesquisa, recuperação, listagem, criação e edição de arquivos e pastas no [!UICONTROL Dropbox].

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

* Para usar módulos [!DNL Dropbox], você deve ter uma conta [!DNL Dropbox].

>[!IMPORTANT]
>
>* Para usar o conector do Dropbox, primeiro crie um aplicativo no Dropbox.
>  >   Para obter mais informações, pesquise por &quot;Criar um aplicativo&quot; no guia do desenvolvedor do Dropbox.
>* Ao criar o aplicativo, use o seguinte URI de redirecionamento: `https://app.workfrontfusion.com/oauth/cb/dropbox`
>* A Dropbox deve aprovar aplicativos com mais de 50 usuários.
>  >   Para obter mais informações, pesquise por &quot;Aprovação de produção&quot; no guia do desenvolvedor do Dropbox.

## Informações da API do Dropbox

O conector do Dropbox usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
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
        <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Selecione se essa conexão é para um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID do Cliente]</td>
        <td>Insira sua [!UICONTROL Dropbox] [!UICONTROL ID do cliente]. </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira seu [!DNL Dropbox] [!UICONTROL Segredo do Cliente]. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo de Conta]</td>
        <td>Selecione se você está se conectando a uma conta pessoal da Dropbox ou a uma conta comercial (Dropbox Business).</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Excluir cabeçalho dropbox-api-path-root]</td>
        <td>Habilite essa opção para excluir o cabeçalho dropbox-api-path-root para aplicativos Dropbox com acesso à pasta de aplicativos</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.## [!DNL Dropbox] módulos e seus campos

## [!DNL Dropbox] módulos e seus campos

Ao configurar módulos do [!DNL Dropbox], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Dropbox] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Módulos acionadores](#trigger-modules)
* [Módulos para obter  [!DNL Dropbox]  arquivos e pastas](#modules-for-getting-dropbox-files-and-folders)
* [Módulos para criação e edição [!DNL Dropbox] de arquivos e pastas](#modules-for-creating-and-editing-dropbox-files-and-folders)
* [Outros módulos](#other-modules)

### Módulos acionadores

#### [!UICONTROL Observar arquivos]

Este módulo de tipo de Acionador retorna detalhes do arquivo quando ele é modificado em uma pasta especificada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta que deseja observar alterações.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Observar também subpastas]</td> 
   <td> <p> Habilite esta opção para também monitorar subpastas na pasta selecionada para arquivos modificados.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limite] </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Módulos para obter [!DNL Dropbox] arquivos e pastas

* [[!UICONTROL Baixar um Arquivo]](#download-a-file)
* [[!UICONTROL Obter Metadados de Pasta]](#get-a-folder-metadata)
* [[!UICONTROL Listar Todos os Arquivos/Subpastas em uma Pasta]](#list-all-filessubfolders-in-a-folder)
* [[!UICONTROL Listar revisões de arquivos]](#list-file-revisions)
* [[!UICONTROL Pesquisar Arquivos/Pastas]](#search-filesfolders)

#### [!UICONTROL Baixar um Arquivo]

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
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
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

#### [!UICONTROL Obter Metadados de Pasta]

Este módulo de ação recupera os detalhes da pasta compartilhada.

Especifique a ID da pasta.

O módulo retorna a ID da pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>ID da Pasta Compartilhada</td> 
   <td> <p> Insira ou mapeie a ID da pasta da qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar Todos os Arquivos/Subpastas em uma Pasta]

Este módulo de ação lista arquivos ou pastas em uma pasta específica.

Especifique a ID da pasta.

O módulo retorna as IDs dos arquivos ou pastas e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
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

#### [!UICONTROL Listar revisões de arquivos]

Este módulo de ação recupera todas as revisões de arquivo (um histórico de versões) de um arquivo específico.\
Especifique a ID do arquivo.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Forma de selecionar arquivos</td> 
   <td> <p> Selecione se deseja mapear o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Caminho do arquivo / Arquivo</p> </td> 
   <td> <p><b>Caminho do arquivo</b></p> <p>Insira ou mapeie o caminho de destino para o arquivo.</p> <p><b>Arquivo</b></p> <p>Selecione o arquivo no menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Limite</p> </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo liste durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar Arquivos/Pastas]

Este módulo de pesquisa procura registros em um objeto em [!DNL Dropbox] que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar] </td> 
   <td> <p>Insira o termo de pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta que deseja pesquisar. Este módulo pesquisa toda a conta [!DNL Dropbox] se você não selecionar uma pasta.</p> </td> 
  </tr> 
  <tr> 
   <td>Status do arquivo</td> 
   <td> <p> Selecione o status do arquivo que deseja incluir na pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td>Categorias de arquivo</td> 
   <td> <p> Selecione as categorias de arquivo que deseja incluir na pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td>Extensões de arquivo</td> 
   <td> <p>Para cada extensão de arquivo que você deseja incluir na pesquisa, clique em <b>Adicionar item</b> e insira ou mapeie a extensão de arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Módulos para criação e edição de [!DNL Dropbox] arquivos e pastas

* [[!UICONTROL Criar uma pasta]](#create-a-folder)
* [[!UICONTROL Criar/Substituir um Arquivo de Texto]](#createoverwrite-a-text-file)
* [[!UICONTROL Criar/atualizar um link de compartilhamento]](#createupdate-a-share-link)
* [[!UICONTROL Excluir um Arquivo/Pasta]](#delete-a-filefolder)
* [[!UICONTROL Mover um Arquivo/Pasta]](#move-a-filefolder)
* [[!UICONTROL Renomear um Arquivo/Pasta]](#rename-a-filefolder)
* [[!UICONTROL Restaurar um Arquivo]](#restore-a-file)
* [[!UICONTROL Carregar] um arquivo](#upload-a-file)

#### [!UICONTROL Criar uma pasta]

Este módulo de ação cria uma nova pasta.

Especifique o caminho e um nome para a pasta.

O módulo retorna a ID da pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nome da Pasta] </td> 
   <td> <p>Insira o nome da nova pasta.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Pasta]</p> </td> 
   <td> <p>Insira ou mapeie o caminho onde deseja criar uma nova pasta.</p> <p>Observação:   <p>Se você estiver usando uma conta do [!DNL Dropbox Business] (com espaços de equipe), remova a barra <code>/</code> ou não clique <strong>Clique aqui para escolher a pasta</strong> para criar uma pasta de equipe na raiz.</p> <p>Se a barra não for removida, um erro <code>[409] path/malformed_path/..</code> será retornado.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Renomear automaticamente]</td> 
   <td> <p> Ative esta opção para renomear a nova pasta, se uma pasta com o mesmo nome já existir no local de destino.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar/Substituir um Arquivo de Texto]

Esse módulo de ação cria um arquivo DOC ou substitui o conteúdo de um existente.

Especifique o arquivo de origem e a pasta.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Selecionar para]</td> 
   <td> <p> Selecione se deseja criar ou substituir um arquivo DOC.</p><ul><li><b>Criar</b></p>Selecione a pasta na qual deseja criar um arquivo.</li><li><b>Substituir</b><p>Selecione como você deseja escolher o arquivo a ser substituído e, em seguida, mapeie o caminho do arquivo ou selecione o arquivo. </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Arquivo Source]</p> </td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o conteúdo do arquivo de origem. </p> <p>Se você estiver criando um arquivo, selecione <b>Vazio</b>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar/atualizar um link de compartilhamento]

Este módulo de ação cria um link público para um arquivo.

Especifique o arquivo e as informações sobre o link.

O módulo retorna a ID do link e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maneira de selecionar arquivos]</td> 
   <td> <p> Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Caminho/Arquivo]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Caminho do Arquivo]</p> <p>Insira ou mapeie o caminho para o arquivo de destino.</p> <p style="font-weight: bold;">[!UICONTROL Arquivo]</p> <p>Selecione o arquivo de destino.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Solicitou Visibilidade]</p> </td> 
   <td> <p>Selecione se o link é público, para equipe ou com senha restrita.</p> <p><b>Observação:</b></p><p> [!UICONTROL Equipe somente] está disponível somente para contas do Dropbox Business. O [!UICONTROL Access com senha] está disponível somente para contas [!DNL Dropbox Pro] ou Dropbox Business.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data de expiração do link]</td> 
   <td> <p> Insira a data e a hora em que o link expirará e não estará mais acessível. Se esse campo ficar vazio, o link não expirará. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coerção de tipo</a>.</p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Nível de Acesso do Link]</p> </td> 
   <td> <p>Defina a permissão para o recipient do link.</p> <ul><li><strong>[!UICONTROL Viewer]</strong> <p>Os usuários que usam o link podem exibir e comentar no conteúdo.</p> </li><li><strong>[!UICONTROL Editor]</strong><p> Os usuários que usam o link podem editar, exibir e comentar no conteúdo. Esse nível de acesso está disponível somente para documentos baseados em nuvem.</p> </li><li><strong>[!UICONTROL Máx.]</strong> <p>Os usuários que usam o link recebem o nível de acesso máximo para o qual você pode definir o link.</p></li><ul> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Excluir um Arquivo/Pasta]

Este módulo de ação exclui um arquivo ou pasta.

Especifique o arquivo ou pasta.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maneira de selecionar arquivos]</td> 
   <td> <p> Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Caminho do Arquivo ou da Pasta] / [!UICONTROL Arquivo ou Pasta]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Caminho de Arquivo/Pasta]</p> <p>Insira ou mapeie o caminho de destino para o arquivo ou pasta.</p> <p style="font-weight: bold;">[!UICONTROL Arquivo/Pasta]</p> <p>Selecione o arquivo ou pasta no menu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mover um Arquivo/Pasta]

Este módulo de ação move um arquivo ou pasta para um local diferente.

Especifique o arquivo ou pasta e como e onde deseja movê-lo.

O módulo retorna a ID do arquivo ou pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maneira de selecionar arquivos/pastas] </td> 
   <td> <p>Selecione se deseja mapear ou inserir o caminho do arquivo ou pasta ou selecione o arquivo ou pasta manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Arquivo / Caminho da Pasta] /</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Caminho de Arquivo/Pasta]</p> <p>Insira ou mapeie o caminho de destino para o arquivo ou pasta.</p> <p style="font-weight: bold;">[!UICONTROL Arquivo/Pasta]</p> <p>Selecione se você está movendo um arquivo ou pasta e, em seguida, o arquivo ou pasta.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Para Pasta]</p> </td> 
   <td> <p>Insira ou mapeie o local de destino do arquivo ou pasta.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Novo Nome]</p> </td> 
   <td> <p>Digite o novo nome do arquivo ou pasta no novo local.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Renomear Automaticamente]</p> </td> 
   <td> <p>Habilite esta opção para garantir que, se existir um arquivo ou pasta com o mesmo nome, o módulo renomeie o novo arquivo ou pasta adicionando ([!UICONTROL NUMBER]) após o nome do arquivo ou pasta. Caso contrário, o arquivo ou pasta no local de destino será substituído.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permitir transferência de propriedade]</p> </td> 
   <td> <p>Ative essa opção para permitir movimentações por proprietário, mesmo que resulte em uma transferência de propriedade para o conteúdo que está sendo movido.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Renomear um Arquivo/Pasta]

Esse módulo de ação renomeia um arquivo ou pasta.

Especifique o arquivo ou pasta e o novo nome.

O módulo retorna a ID do arquivo ou pasta e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Forma de selecionar arquivos</td> 
   <td> <p> Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Caminho de arquivo/pasta/Arquivo/Pasta</p> </td> 
   <td> <p style="font-weight: bold;">Caminho do arquivo/pasta</p> <p>Insira ou mapeie o caminho de destino para o arquivo ou pasta.</p> <p style="font-weight: bold;">Arquivo/Pasta</p> <p>Selecione se você está movendo um arquivo ou pasta e, em seguida, o arquivo ou pasta.</p> </td> 
  </tr> 
  <tr> 
   <td>Renomear </td> 
   <td> <p>Insira o novo nome do arquivo, incluindo a extensão.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Restaurar um Arquivo]

Este módulo de ação restaura uma versão anterior de um arquivo.

Especifique o arquivo e o número da revisão desejada.

O módulo retorna a ID da versão e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maneira de selecionar arquivos]</td> 
   <td> <p> Selecione se deseja mapear ou inserir o caminho do arquivo ou selecione o arquivo manualmente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Caminho do Arquivo] / [!UICONTROL Arquivo]</p> </td> 
   <td> <p><strong>[!UICONTROL Caminho do Arquivo]</strong> </p> <p>Insira ou mapeie o caminho de destino para o arquivo.</p> <p><strong>[!UICONTROL Arquivo]</strong> </p> <p>Selecione o arquivo no menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Revisão]</p> </td> 
   <td> <p>Informe ou mapeie o número da revisão que deseja restaurar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um arquivo]

Este módulo de ação faz upload de um arquivo para uma pasta.

Especifique informações como o local do arquivo, o arquivo que deseja fazer upload e um novo nome opcional para o arquivo.

O módulo retorna a ID do arquivo e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta]</td> 
   <td> <p> Selecione a pasta do [!DNL Dropbox] para a qual você deseja carregar o arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Arquivo Source]</p> </td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> <p><b>Observação:</b></p><p> O tamanho máximo do arquivo carregado é de 150 MB.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Substituir um arquivo existente]</td> 
   <td> <p> Habilite esta opção para substituir o arquivo existente pelo novo arquivo. Se essa opção for deixada desativada, o arquivo carregado será renomeado.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Outros módulos

#### [!UICONTROL Fazer uma chamada de API]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Dropbox]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Dropbox].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Dropbox] ao Workfront Fusion, consulte <a href="#create-a-connection-to-dropbox" class="MCXref xref">Criar uma conexão com o [!DNL Dropbox]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Digite um caminho relativo a Digite um caminho relativo a <code>https://api.dropboxapi.com</code>. Por exemplo, <code>/2/files/list_folder</code></p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Método]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cabeçalhos] </td> 
   <td> <p>Insira os cabeçalhos de solicitação desejados. O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p> Insira a string de consulta da solicitação.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Corpo] </td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:   <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Exemplo:**

A chamada de API a seguir retorna os primeiros 10 arquivos da pasta [!DNL /Text files] da sua conta [!DNL Dropbox]:

URL: `/2/files/list_folder`

Corpo:

```
{
"path": "/Text files",
"limit": 10,
"recursive": false,
"include_deleted": false
}
```

Correspondências da pesquisa podem ser encontradas na Saída do módulo em [!UICONTROL Pacote] > [!UICONTROL Corpo] > entradas.

No nosso exemplo, 10 tíquetes foram retornados.

>[!ENDSHADEBOX]

## Problemas comuns

* [Não é possível carregar ou atualizar um arquivo](#unable-to-upload-or-update-a-file)
* [A imagem referenciada por um link compartilhado não é renderizada](#image-referenced-via-a-shared-link-does-not-render)

### Não é possível carregar ou atualizar um arquivo

Os motivos a seguir podem ser uma falha no upload ou na atualização de um arquivo:

* O arquivo carregado é muito grande e excede o tamanho máximo de arquivo permitido para o plano [!DNL Dropbox], ou você usou toda a cota de armazenamento da sua conta [!DNL Dropbox]. Você deve excluir arquivos existentes da sua conta [!DNL Dropbox] ou atualizar seu plano.
* A pasta selecionada anteriormente, para a qual o arquivo está sendo carregado, não existe mais. O cenário é interrompido e você deve selecionar a pasta de destino novamente.

### A imagem referenciada por um link compartilhado não é renderizada

A URL retornada pela [!UICONTROL Dropbox] >[!UICONTROL Criar um link compartilhado] não está vinculada diretamente a uma imagem, mas a uma página [!DNL Dropbox]. Para forçar o download da imagem, substitua o `?dl=0` à direita por `?dl=1`. Para forçar a imagem a ser renderizada (por exemplo, em um navegador da Web ou no Facebook Messenger), anexe `&raw=1` à URL.

Se você precisar obter o link direto ou bruto da imagem para o seu site ou para outros módulos do Workfront Fusion, modifique o URL compartilhado inicial da seguinte maneira:

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
