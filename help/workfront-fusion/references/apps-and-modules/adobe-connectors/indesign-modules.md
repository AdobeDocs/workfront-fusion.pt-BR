---
filename: adobe-indesign-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Módulos do Adobe InDesign
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Adobe InDesign, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
exl-id: 8164487a-d114-4e31-9d1c-8404fc89a04b
TQID: https://experienceleague.adobe.com/D2JdaOqvTA5SUsKm9U8Sjss6dJFMZv2Uo5RGk25QphQ
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 18401e01219383f86e1553e16b21057497d24cc0
workflow-type: tm+mt
source-wordcount: 2240
ht-degree: 17%

---

# Módulos do Adobe InDesign

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Adobe InDesign, bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Antes de usar o conector do Adobe InDesign, é necessário ter uma conta ativa do Adobe InDesign.

## Criar uma conexão com o Adobe InDesign

Para criar uma conexão para os módulos do Adobe InDesign:

1. Em qualquer módulo do Adobe InDesign, clique em **Adicionar** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col>
      </col>
      <col>
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
        <td>
          <p>Selecione se estão se conectando a um ambiente de produção ou não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Tipo</td>
        <td>
          <p>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
        <tr>
          <td role="rowheader">ID do cliente</td>
          <td>Insira a ID do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Segredo do cliente</td>
          <td>Insira o segredo do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">ID da organização IMS</td>
          <td>Insira sua ID da organização da Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console</td>
        </tr>
      </tbody>
    </table>
1. Clique em **Continuar** para salvar a conexão e retornar ao módulo.

## Módulos do InDesign e seus campos

Ao configurar módulos do Adobe InDesign, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Adobe InDesign podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Ações

* [Criar representação](#create-rendition)
* [Excluir um script personalizado](#delete-a-custom-script)
* [Mesclar dados](#merge-data)
* [Remapear links](#remap-links)
* [Enviar uma solicitação de execução de script personalizado](#submit-a-custom-script-execution-request)

#### Criar representação

Este módulo de ação cria e retorna uma representação JPEG, PNG ou PDF de um documento InDesign específico. Para a estrutura de `StatusCompletedRespons/output/data` consulte `RenditionOutputData`. Também para obter a lista de possíveis códigos de erro em `FailedEvent` consulte `RenditionFailedData`.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Tipo</p>
      </td>
      <td>Selecione o tipo de arquivo da representação que deseja criar. 
      <ul><li>JPEG</li><li>Imagem PNG</li><li>PDF</li></ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ativos</p>
      </td>
      <td>Para cada ativo que deseja adicionar à representação:<ol><li>Clique em <b>Adicionar item</b>.</li><li>Selecione ou mapeie a origem do ativo.</li><li>Insira um destino. O destino é um caminho relativo a um diretório base temporário (diretório de trabalho) onde o recurso é baixado. Isso identifica os ativos dentro dos parâmetros. Ele não pode ser ativado usando '..' ou '/'. Deve haver um nome de arquivo válido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento de destino</td>
      <td>Insira ou mapeie o documento que será processado e renderizado. Atualmente, somente um documento por vez é suportado.</td>
    </tr>
    <tr>
      <td role="rowheader">Outros campos</td>
   <td>Para outros campos, consulte as informações incluídas no módulo.</td>     </tr>
  </tbody>
</table>

#### Excluir um script personalizado

Esse módulo de ação exclui um único script personalizado registrado. Todas as versões do script serão removidas permanentemente.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Nome do script</p>
      </td>
      <td>Insira ou mapeie o nome do script que deseja excluir.</td>
    </tr>
  </tbody>
</table>

#### Mesclar dados

Esse módulo cria documentos ou PDFs do InDesign ao mesclar dados CSV com modelos do InDesign. Os formatos de saída incluem documentos JPEG, PNG, PDF e InDesign.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ativos</p>
      </td>
      <td>Para cada ativo que você deseja adicionar à mesclagem de dados:<ol><li>Clique em <b>Adicionar item</b>.</li><li>Selecione ou mapeie a origem do ativo.</li><li>Insira um destino. O destino é um caminho relativo a um diretório base temporário (diretório de trabalho) onde o recurso é baixado. Isso identifica os ativos dentro dos parâmetros. Ele não pode ser ativado usando '..' ou '/'. Deve haver um nome de arquivo válido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento de destino</td>
      <td>Insira ou mapeie o documento que será usado como modelo para mesclagem.</td>
    </tr>
    <tr>
      <td role="rowheader">Fonte de dados</td>
      <td>Insira ou mapeie os arquivos de origem a serem usados.</td>
    </tr>
    <tr>
      <td role="rowheader">Outros campos</td>
   <td>Para outros campos, consulte as informações incluídas no módulo.</td>     </tr>
  </tbody>
</table>

#### Remapear links

Esse módulo substitui links baseados em arquivos em documentos do InDesign por URLs do Adobe Experience Manager (AEM). Isso pode ser útil para trabalhar com o Adobe Experience Manager usando o Adobe Asset Link.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
      </tr>
    <tr>
      <td role="rowheader">Token do AEM</td>
      <td>Insira ou mapeie o token do portador gerado para a conta técnica do AEM, sem a palavra-chave do portador.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ativos</p>
      </td>
      <td>Para cada ativo que você deseja adicionar ao módulo:<ol><li>Clique em <b>Adicionar item</b>.</li><li>Selecione ou mapeie a origem do ativo.</li><li>Insira um destino. O destino é um caminho relativo a um diretório base temporário (diretório de trabalho) onde o recurso é baixado. Isso identifica os ativos dentro dos parâmetros. Ele não pode ser ativado usando '..' ou '/'. Deve haver um nome de arquivo válido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento de destino</td>
      <td>Insira ou mapeie o documento no qual deseja remapear os links.</td>
    </tr>
    <tr>
      <td role="rowheader">Fonte de dados</td>
      <td>Insira ou mapeie os arquivos de origem a serem usados para extrair e corresponder tags.</td>
    </tr>
    <tr>
      <td role="rowheader">Outros campos</td>
   <td>Para outros campos, consulte as informações incluídas no módulo.</td>     </tr>
  </tbody>
</table>

#### Enviar uma solicitação de execução de script personalizado

Este módulo de ação envia uma solicitação de execução para um script personalizado. Você define os ativos e parâmetros de entrada que o script personalizado usará durante a execução.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>ID do script</p>
      </td>
      <td>Insira ou mapeie a ID do script personalizado.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ativos</p>
      </td>
      <td>Para cada ativo para o qual você deseja submeter uma solicitação de execução, <ol><li>Clique em <b>Adicionar item</b>.</li><li>Selecione ou mapeie a origem do ativo.</li><li>Insira um destino. O destino é um caminho relativo a um diretório base temporário (diretório de trabalho) onde o recurso é baixado. Isso identifica os ativos dentro dos parâmetros. Ele não pode ser ativado usando '..' ou '/'. Deve haver um nome de arquivo válido.</td>
    </tr>
    <tr>
      <td role="rowheader">Outros campos</td>
   <td>Para outros campos, consulte as informações incluídas no módulo.</td>     </tr>
  </tbody>
</table>

### Pesquisas

* [Obter detalhes do script personalizado](#get-custom-script-details)
* [Obter tags de mesclagem de dados](#get-data-merge-tags)
* [Obter informações de documentos](#get-document-information)
* [Listar scripts personalizados](#list-custom-scripts)

#### Obter detalhes do script personalizado

Este módulo de pesquisa recupera detalhes de um único script personalizado registrado, incluindo versão, link de download, data de registro e nome do script.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Nome do script</p>
      </td>
      <td>Insira ou mapeie o nome do script para o qual deseja recuperar detalhes.</td>
    </tr>
  </tbody>
</table>

#### Obter tags de mesclagem de dados

Esse módulo recupera as tags de mesclagem de dados de um documento.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Ativos</p>
      </td>
      <td>Para cada ativo que você deseja adicionar ao módulo:<ol><li>Clique em <b>Adicionar item</b>.</li><li>Selecione ou mapeie a origem do ativo.</li><li>Insira um destino. O destino é um caminho relativo a um diretório base temporário (diretório de trabalho) onde o recurso é baixado. Isso identifica os ativos dentro dos parâmetros. Ele não pode ser ativado usando '..' ou '/'. Deve haver um nome de arquivo válido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento de destino</td>
      <td>Insira ou mapeie o documento do qual deseja recuperar as tags.</td>
    </tr>
    <tr>
      <td role="rowheader">Fonte de dados</td>
      <td>Insira ou mapeie os arquivos de origem a serem usados para extrair e corresponder tags.</td>
    </tr>
    <tr>
      <td role="rowheader">Outros campos</td>
   <td>Para outros campos, consulte as informações incluídas no módulo.</td>     </tr>
  </tbody>
</table>

#### Obter informações de documentos

Este módulo recupera informações abrangentes sobre documentos INDD/IDML e retorna dados com base nos tipos de informações ativadas especificados na solicitação.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Ativos</p>
      </td>
      <td>Para cada ativo que você deseja adicionar ao módulo:<ol><li>Clique em <b>Adicionar item</b>.</li><li>Selecione ou mapeie a origem do ativo.</li><li>Insira um destino. O destino é um caminho relativo a um diretório base temporário (diretório de trabalho) onde o recurso é baixado. Isso identifica os ativos dentro dos parâmetros. Ele não pode ser ativado usando '..' ou '/'. Deve haver um nome de arquivo válido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento de destino</td>
      <td>Insira ou mapeie o documento do qual deseja recuperar as informações.</td>
    </tr>
     <tr>
      <td role="rowheader">Outros campos</td>
   <td>Para outros campos, consulte as informações incluídas no módulo.</td>     </tr>
  </tbody>
</table>

#### Listar scripts personalizados

Este módulo recupera detalhes da versão mais recente de todos os scripts personalizados registrados, incluindo versão, link de download, data de registro e nome do script. Os resultados são paginados com base no comprimento da lista.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
      </tr>
    <tr>
      <td role="rowheader">Número de páginas</td>
      <td>Insira ou mapeie o número da página da qual deseja começar.</td>
    </tr>
  <tr> 
   <td>Número máximo de resultados retornados</td> 
   <td>Defina o número máximo de equipes ou grupos que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
  </tbody>
</table>


### Outros

#### Fazer uma chamada de API personalizada

Este módulo faz uma chamada de API personalizada para a API do Adobe InDesign

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Caminho</p>
      </td>
      <td>
        <p>Insira um caminho relativo a <code>https://indesign.adobe.io/v3</code>.</p><p> Exemplo: <code>/create-rendition</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Método</p>
      </td>
      <td>
        <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte [métodos de solicitação HTTP](/help/workfront-fusion/references/modules/http-request-methods.md).</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Cabeçalhos</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">String de consulta  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  </tbody>
</table>

### Sem categoria

#### Converter PDF para InDesign

Este módulo converte o documento do PDF para o formato editável InDesign (INDD ou IDML). A saída é um arquivo ZIP (nome padrão &quot;output.zip&quot;) contendo subpastas nomeadas após cada PDF de entrada, com o documento convertido e os ativos associados. Se a opção Incorporar links for falsa, os ativos serão fornecidos em uma pasta separada no ZIP. Se for verdadeiro, todos os links serão incorporados ao arquivo InDesign.



<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
      </tr>
    <tr>
      <td role="rowheader">Ativos de entrada</td>
      <td>Para cada ativo que você deseja converter, clique em <b>Adicionar item</b>, insira a URL do ativo e atribua um nome de arquivo local. O nome do arquivo será referenciado posteriormente no módulo.</td>
    </tr>
  <tr> 
   <td>Documentos de destino</td> 
   <td>Para cada documento que você deseja converter, clique em <b>Adicionar item</b> e insira o nome de arquivo atribuído no campo Ativos de entrada.</td> 
  </tr> 
  <tr> 
   <td>Formato de saída</td> 
   <td>Selecione se deseja converter os arquivos em arquivos INDD ou IDML.</td> 
  </tr> 
  <tr> 
   <td>Links incorporados</td> 
   <td>Selecione Sim se quiser que todos os links de imagem e ativo sejam incorporados diretamente no arquivo INDD ou IDML. Selecione Não para colocar esses ativos em uma pasta separada no arquivo ZIP.</td> 
  </tr> 
  <tr> 
   <td>Nome de arquivo ZIP de saída</td> 
   <td>Insira ou nomeie um nome para o arquivo ZIP de saída.</td> 
  </tr> 
  <tr> 
   <td>Saídas</td> 
   <td>Para cada arquivo que deseja gerar saída, selecione o tipo de armazenamento e insira os detalhes de armazenamento.</td> 
  </tr> 
  <tr> 
   <td>Número máximo de resultados retornados</td> 
   <td>Insira o número máximo de resultados que você deseja que o módulo retorne para cada ciclo de execução.</td> 
  </tr> 
  </tbody>
</table>

#### Enviar um script personalizado

Este módulo envia pacotes de script personalizados para registro e retorna um URL para publicar solicitações de execução para o script registrado.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
      </tr>
    <tr>
      <td role="rowheader">Conjunto de scripts</td>
      <td>Mapeie o arquivo de origem de um módulo anterior, como um módulo Baixar um documento. Deve ser um arquivo ZIP.</td>
    </tr>
  <tr> 
   <td>Nome do arquivo</td> 
   <td>Insira ou mapeie o nome do arquivo carregado que contém o pacote de scripts.</td> 
  </tr> 
  </tbody>
</table>

#### Atualizar versão do aplicativo de script personalizado

Esse módulo atualiza a configuração da versão do aplicativo InDesign de um script personalizado registrado. Isso permite especificar estratégias de versão, incluindo o uso da versão mais recente, a correção de uma versão principal ou a correção de uma versão principal e secundária específica.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
      </tr>
    <tr>
      <td role="rowheader">Nome do script</td>
      <td>Insira ou mapeie o nome do script personalizado a ser atualizado. Este é o valor <code>capability</code> retornado quando o script foi registrado.</td>
    </tr>
  <tr> 
   <td>Estratégia de versão do aplicativo</td> 
   <td>Selecione a estratégia de versão do aplicativo que deseja usar.
   <ul>
   <li><b>Sempre usar a versão mais recente</b></li>
   <li><b>Fixar em uma versão principal</b><p>Insira ou mapeie o número da versão principal à qual você deseja aplicar isso.</p></li>
   <li><b>Fixar em uma versão principal e secundária</b><p>Insira as versões principal e secundária às quais deseja aplicar isso.</p></li>
   </ul></td> 
  </tr> 
  </tbody>
</table>

#### Obter versões atuais do aplicativo

Este módulo recupera informações sobre todas as versões do aplicativo InDesign disponíveis, incluindo a versão principal, a versão secundária e o status de cada versão do aplicativo registrada.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Adobe InDesign, consulte <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Criar uma conexão com o Adobe InDesign</a> neste artigo.</td>
      </tr>
  <tr> 
   <td>Número máximo de resultados retornados</td> 
   <td>Insira o número máximo de resultados que você deseja que o módulo retorne para cada ciclo de execução.</td> 
  </tr> 
  </tbody>
</table>

