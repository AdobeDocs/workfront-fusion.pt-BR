---
title: Módulos do Figma
description: Com os  [!DNL Adobe Workfront Fusion] módulos Figma, você pode recuperar listas de comentários, arquivos, versões de arquivos ou projetos. Você também pode postar um comentário ou fazer uma chamada para a API do Figma.
author: Becky
feature: Workfront Fusion
exl-id: 1220460b-1957-4dfc-b7c1-4c97b36ea061
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '2246'
ht-degree: 0%

---

# [!DNL Figma] Módulos

Com os módulos [!DNL Adobe Workfront Fusion] [!DNL Figma], você pode recuperar listas de comentários, arquivos, versões de arquivos ou projetos. Você também pode postar um comentário ou chamar a API [!DNL Figma].

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Para usar módulos [!DNL Figma], você deve ter uma conta [!DNL Figma].

## Informações da API do Figma

O conector Figma usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.figma.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.8.25</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com Figma

Para criar uma conexão para os módulos do Figma:

1. Em qualquer módulo Figma, clique em **[!UICONTROL Add]** ao lado da caixa Conexão.

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
          <p> Para novas conexões, selecione <code>Figma</code> sem a marca Herdada. </p><p>O Figma alterou seus requisitos de autenticação em janeiro de 2025. O tipo de conexão <code>Figma</code> atende aos novos requisitos. O tipo de conexão <code>Figma (Legacy)</code> será removido no futuro.</p>
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
        <td>Insira seu [!UICONTROL Figme] [!UICONTROL Client ID].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Digite seu Figma [!UICONTROL Client Secret].</td>
        </tr>
        <tr>
        <td role="rowheader">Escopos personalizados</td>
        <td>Insira os escopos personalizados necessários para esta conexão.</td>
        </tr>
        <tr>
        <td role="rowheader">URL de Verificação de Conexão Personalizada</td>
        <td>O ponto de extremidade padrão para verificar se a conexão foi criada com êxito é: <code>https://api.figma.com/v1/me</code> Se esta URL não tiver suporte para o Escopo Personalizado, forneça uma URL de Verificação personalizada.</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continue]** para salvar a conexão e retornar ao módulo.



## [!DNL Figma] módulos e seus campos

Ao configurar módulos do [!DNL Figma], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Figma] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Comentários](#comments)

* [Projetos e arquivos](#projects-and-files)

* [Componentes e estilos](#components-and-styles)

* [Outro](#other)


### Comentários

* [Excluir um comentário](#delete-a-comment)

* [Listar comentários](#list-comments)

* [Postar um comentário](#post-a-comment)


#### [!UICONTROL Delete a comment]

Este módulo de ação exclui um único comentário de um arquivo.

<table style="table-layout:auto"> 
  <col/>
  <col />
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>Insira ou mapeie a ID do arquivo do qual você deseja adicionar um comentário para exclusão. </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comment ID]</td>
      <td>Insira o texto do comentário que deseja excluir.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List comments]

Este módulo de pesquisa lista todos os comentários anexados a um único arquivo no [!DNL Figma].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>Insira ou mapeie a ID do arquivo para o qual deseja recuperar comentários. </p>
        <ul>
          <li>
            <p>Caso não saiba a ID, clique em <b>[!UICONTROL Find Files]</b>, insira ou mapeie a ID do projeto ao qual o arquivo está associado e selecione o arquivo.</p>
          </li>
          <li>
            <p>Se você não souber a ID do projeto, clique em <b>[!UICONTROL Find Projects]</b>, insira ou mapeie a ID da equipe que possui o projeto ao qual o arquivo está associado, selecione o projeto e selecione o arquivo.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td>
      <td>Insira ou mapeie o número máximo de comentários que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Post a comment]

Este módulo de ação publica um comentário em um arquivo Figma.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
    </tr>
    <tr>
      <td  role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>Insira ou mapeie a ID do arquivo no qual você deseja postar um comentário. </p>
        <ul>
          <li>
            <p>Se você não souber a ID do arquivo, clique em <b>[!UICONTROL Find Files]</b>, insira ou mapeie a ID do projeto ao qual o arquivo está associado e selecione o arquivo.</p>
          </li>
          <li>
            <p>Se você estiver tentando encontrar a ID do arquivo e não souber a ID do projeto, clique em <b>[!UICONTROL Find Projects]</b> e insira ou mapeie a ID da equipe que possui o projeto ao qual o arquivo está associado. Selecione o projeto e, em seguida, o arquivo.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comment]</td>
      <td>Insira o texto do comentário.</td>
    </tr>
  </tbody>
</table>


### Projetos e arquivos

* [Obter um arquivo ou uma imagem](#get-a-file-or-image)

* [Listar histórico de versão do arquivo](#list-file-version-history)

* [Listar arquivos de projeto](#list-project-files)

* [Listar projetos](#list-projects)


#### [!UICONTROL Get a file or image]

Este módulo de ação recupera um único arquivo ou imagem de uma biblioteca Figma

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>
        <p>Selecione o tipo de objeto que deseja recuperar.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL File]</b>
            </p>
            <p>O módulo retorna o documento referenciado por [!UICONTROL Key] como um objeto JSON. A chave do arquivo pode ser analisada de qualquer URL do arquivo Figma.</p>
            <p>Para campos, consulte <a href="#get-a-file-or-image-file" class="MCXref xref" >[!UICONTROL Get a file or image: File]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL File nodes]</b>
            </p>
            <p>Retorna os nós aos quais as IDs fazem referência como um objeto JSON. Os nós são recuperados do arquivo [!DNL Figma] referenciado por [!UICONTROL Key].</p>
            <p>Para campos, consulte <a href="#get-a-file-or-image-file-nodes" class="MCXref xref" >[!UICONTROL Get a file or image: File nodes]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Image]</b>
            </p>
            <p>O módulo renderiza imagens de um arquivo.</p>
            <p>Para campos, consulte <a href="#get-a-file-or-image-image" class="MCXref xref" >[!UICONTROL Get a file or image: Image]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Image fills]</b>
            </p>
            <p>O módulo retorna links de download para todas as imagens presentes em preenchimentos de imagem em um documento. Os preenchimentos de imagem são como [!DNL Figma] representa quaisquer imagens fornecidas pelo usuário. Quando você arrasta uma imagem para [!DNL Figma], [!DNL Figma] cria um retângulo com um único preenchimento que representa a imagem, e o usuário pode transformar o retângulo (e as propriedades no preenchimento).</p>
            <p>Para campos, consulte <a href="#get-a-file-or-image-image-fills" class="MCXref xref" >[!UICONTROL Get a file or image: Image fills]</a>.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>


##### Obter um arquivo ou imagem: Arquivo

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>Selecione o arquivo do qual deseja retornar JSON.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version ID]</td>
      <td>Insira ou mapeie a versão do arquivo que o módulo deve retornar. Para o módulo atual, deixe este campo em branco.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>Para retornar apenas um subconjunto do documento, insira os nós que você deseja que o módulo retorne. O módulo retorna os nós listados, seus filhos e qualquer item entre o nó raiz e os nós listados.</p>
        <p>Para cada nó que você deseja retornar, clique em <b>[!UICONTROL Add]</b> e insira o texto do nó.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Depth]</td>
      <td>
        <p>Insira ou mapeie um número inteiro que represente a profundidade máxima na árvore de documentos para a qual você deseja retornar resultados. </p>
        <div class="example"><span class="autonumber"><span><b>Exemplo: </b></span></span>
          <ul>
            <li>
              <p>Para retornar somente páginas, digite <code>1</code>.</p>
            </li>
            <li>
              <p>Para retornar páginas e objetos de nível superior, digite <code>2</code>.</p>
            </li>
          </ul>
        </div>
        <p>Para retornar todos os nós, deixe este campo em branco.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Geometry]</td>
      <td>Para retornar dados vetoriais, digite <code>paths</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plugin data]</td>
      <td>Uma lista separada por vírgulas de IDs de plug-in e/ou a sequência de caracteres "[!UICONTROL shared]". Quaisquer dados presentes no documento escrito por esses plug-ins serão incluídos no resultado nas propriedades <code>pluginData</code> e <code>sharedPluginData</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Branch data]</td>
      <td>Habilite esta opção para retornar os metadados da ramificação para o arquivo solicitado. Se o arquivo for uma ramificação, a chave do arquivo principal será incluída na resposta retornada. Se o arquivo tiver ramificações, os metadados serão incluídos na resposta retornada. Padrão: <code>false</code>.</td>
    </tr>
  </tbody>
</table>

##### Obter um arquivo ou imagem: nós de arquivo

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>Selecione o arquivo do qual deseja retornar JSON.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>Insira os nós que você deseja que o módulo retorne e converta</p>
        <p>Para cada nó que você deseja retornar, clique em <b>[!UICONTROL Add]</b> e insira o texto do nó.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version ID]</td>
      <td>Insira ou mapeie a versão do arquivo que o módulo deve retornar. Para o módulo atual, deixe este campo em branco.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Depth]</td>
      <td>
        <p>Insira ou mapeie um número inteiro que represente a profundidade máxima na árvore de documentos para a qual você deseja retornar resultados. </p>
        <div class="example"><span class="autonumber"><span><b>Exemplo: </b></span></span>
          <ul>
            <li>
              <p>Para retornar somente páginas, digite <code>1</code>.</p>
            </li>
            <li>
              <p>Para retornar páginas e objetos de nível superior, digite <code>2</code>.</p>
            </li>
          </ul>
        </div>
        <p>Para retornar todos os nós, deixe este campo em branco.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Geometry]</td>
      <td>Para retornar dados vetoriais, digite <code>paths</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plugin data]</td>
      <td>Uma lista separada por vírgulas de IDs de plug-in e/ou a sequência "compartilhada". Quaisquer dados presentes no documento escrito por esses plug-ins serão incluídos no resultado nas propriedades pluginData e sharedPluginData.</td>
    </tr>
  </tbody>
</table>


##### Obter um arquivo ou imagem: Imagem

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>Selecione o arquivo do qual deseja retornar JSON.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>Insira os nós que você deseja que o módulo renderize.</p>
        <p>Para cada nó que você deseja renderizar, clique em <b>[!UICONTROL Add]</b> e insira o texto do nó.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Scale]</td>
      <td>Para dimensionar a imagem, insira ou mapeie o fator de dimensionamento. Este número deve estar entre 0,01 e 4.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Format]</td>
      <td>
        <p>Selecione o formato para a saída da imagem.</p>
        <ul>
          <li>
            <p>JPG</p>
          </li>
          <li>
            <p>Imagem PNG</p>
          </li>
          <li>
            <p>SVG</p>
          </li>
          <li>
            <p>PDF</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SVG - Include ID]</td>
      <td>Habilite esta opção para incluir atributos de ID para todos os elementos de SVG. Padrão: [!UICONTROL false].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SVG - Simplify Stroke]</td>
      <td>Ative essa opção para simplificar traçados internos/externos e, se possível, use o atributo de traçado em vez de &lt;mask&gt;. Padrão: [!UICONTROL true].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Use absolute bounds]</td>
      <td>Habilite essa opção para usar as dimensões completas do nó, independentemente de ele estar ou não cortado ou do espaço ao redor estar vazio. Use isso para exportar nós de texto sem cortar. Padrão: [!UICONTROL false].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version]</td>
      <td>Insira ou mapeie a versão do arquivo que o módulo deve retornar. Para o módulo atual, deixe este campo em branco.</td>
    </tr>
  </tbody>
</table>

##### Obter um arquivo ou imagem: preenchimentos de imagem

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>Selecione o arquivo do qual deseja retornar JSON.</td>
    </tr>
  </tbody>
</table>

### [!UICONTROL List file version history]

Este módulo de pesquisa retorna o histórico de versões de um único arquivo em [!UICONTROL Figma].
<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>Insira ou mapeie a ID do arquivo para o qual você deseja recuperar o histórico de versões. </p>
        <ul>
          <li>
            <p>Se você não souber a ID do arquivo, clique em <b>[!UICONTROL Find Files]</b>, insira ou mapeie a ID do projeto ao qual o arquivo está associado e selecione o arquivo.</p>
          </li>
          <li>
            <p>Se você estiver tentando encontrar a ID do arquivo e não souber a ID do projeto, clique em <b>[!UICONTROL Find Projects]</b> e insira ou mapeie a ID da equipe que possui o projeto ao qual o arquivo está associado. Selecione o projeto e, em seguida, o arquivo.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned files]</td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List project files]

Este módulo de pesquisa retorna uma lista de todos os arquivos no projeto especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>Insira ou mapeie a ID do projeto para o qual você deseja recuperar os arquivos. </p>
        <ul>
          <li>
            <p>Se você não souber a ID do projeto, clique em <b>[!UICONTROL Find Projects]</b>, insira ou mapeie a ID da equipe à qual o projeto está associado e selecione o projeto.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned files]</td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List projects]

Este módulo de pesquisa retorna uma lista de todos os projetos dentro da equipe especificada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Team ID]</td>
      <td>Insira ou mapeie a ID do projeto do qual você deseja recuperar os arquivos. A ID da equipe pode ser encontrada no URL da página da equipe no Figma</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned projects]</td>
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
    </tr>
  </tbody>
</table>


### Componentes e estilos

#### [!UICONTROL Get a style or component]

Este módulo de ação recupera um único estilo ou componente, ou um conjunto de estilos ou componentes.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
    </tr>
    <tr>
      <td role="rowheader">Objeto&gt; tipo</td>
      <td>Selecione o tipo de objeto que deseja recuperar.</td>
    </tr>
    <tr>
      <td role="rowheader">&lt;[!UICONTROL Object> key]</td>
      <td>Informe a chave (identificador exclusivo) do objeto que deseja recuperar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Team ID]</td>
      <td>Se estiver recuperando um componente de equipe ou conjunto de componentes de equipe, digite ou mapeie a ID da equipe à qual o registro ou os registros estão associados.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Page Size]</td>
      <td>Se estiver recuperando um componente de grupo ou conjunto de componentes de grupo, digite ou mapeie o número ou os resultados a serem retornados por página. Padrão: 30.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL After]</td>
      <td>
        <p>Se estiver recuperando um componente de grupo ou conjunto de componentes de grupo, digite ou mapeie o número do resultado após o qual deve começar a recuperar os resultados. Isso pode ser combinado com o campo [!UICONTROL Page Size] para paginar resultados.</p>
        <p>Esse valor não corresponde às IDs de objeto.</p>
        <p>Este campo não pode ser usado em combinação com o campo [!UICONTROL Before].</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Before]</td>
      <td>
        <p>Se estiver recuperando um componente de grupo ou conjunto de componentes de grupo, digite ou mapeie o número do resultado antes de começar a recuperar os resultados. Isso pode ser combinado com o campo [!UICONTROL Page Size] para paginar resultados.</p>
        <p>Esse valor não corresponde às IDs de objeto.</p>
        <p>Este campo não pode ser usado em combinação com o campo [!UICONTROL After].</p>
      </td>
    </tr>
  </tbody>
</table>


### Outro

* [Fazer uma chamada de API](#make-an-api-call)

* [Assistir a eventos](#watch-events)


#### [!UICONTROL Make an API call]

Esse módulo de ação permite fazer uma chamada autenticada personalizada para a API Figma sem precisar pensar na autenticação. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do Figma.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!DNL Workfront Fusion], consulte <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Figma</a> neste artigo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Insira um caminho relativo para <code>https://api.figma.com/v1/</code>.</p>
        <p>Por exemplo: <code>[!DNL files/7179110/comments]</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Method]</td>
      <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] O adiciona os cabeçalhos de autorização para você.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]</td>
      <td>
        <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p>
        <p>Por exemplo: <code>{"name":"something-urgent"}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL Watch events]

Este módulo de acionador inicia um cenário quando um dos seguintes eventos ocorre para uma equipe específica no espaço de equipe do [!DNL Figma]:

* Atualização de arquivo

* Atualização da versão do arquivo

* Arquivo excluir

* Publicação da biblioteca

* Comentário do arquivo

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>
        <p>Selecione o webhook que o módulo observa.</p>
        <p>Para adicionar um novo webhook:</p>
        <ol>
          <li>
            <p>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL Webhook].</p>
          </li>
          <li>
            <p>Insira um nome para o webhook.</p>
          </li>
          <li>
            <p>Selecione a conexão que deseja usar com este webhook. Para obter instruções sobre como conectar sua conta do [!DNL Figma] ao [!UICONTROL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas.</a></p>
          </li>
          <li>
            <p>Selecione o tipo de evento que você deseja que o módulo veja.</p>
          </li>
          <li>
            <p>Digite a ID da equipe cujos eventos você deseja que o webhook assista.</p>
          </li>
          <li>
            <p>Selecione se deseja que o webhook fique ativo ou pausado.</p>
          </li>
          <li>
            <p>Insira uma descrição para o webhook.</p>
          </li>
          <li>
            <p>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo.</p>
          </li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>
