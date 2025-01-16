---
title: Módulos do Adobe Lightroom
description: Com os módulos do Adobe Lightroom, é possível iniciar um cenário do Adobe Workfront Fusion com base em eventos em sua conta do Adobe Lightroom.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2025'
ht-degree: 0%

---

# [!DNL Adobe Lightroom] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Adobe Lightroom], bem como conectá-los a vários aplicativos e serviços de terceiros.

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

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
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td>
      <td >
        <p>[!UICONTROL Workfront Fusion for Work Automation and Integration]</p>
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

&#42;&#42;Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [!DNL [Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Pré-requisitos

Antes de usar o conector [!DNL Adobe Lightroom], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!DNL Adobe Lightroom] ativa.

## Informações da API do Adobe Lightroom

O conector do Adobe Lightroom usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://lr.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.17.128</td> 
  </tr>
 </tbody> 
 </table>



## Criar uma conexão com o Adobe Lightroom

Para criar uma conexão para seus módulos do [!DNL Adobe Lightroom]:

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
        <td>Insira seu [!UICONTROL Adobe] [!UICONTROL Client ID]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira seu [!DNL Adobe] [!UICONTROL Client Secret]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continue]** para salvar a conexão e retornar ao módulo.




## Módulos do Adobe Lightroom e seus campos

Ao configurar módulos do [!DNL Adobe Lightroom], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Lightroom] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Outro](#other)
* [Ativos](#assets)
* [Álbuns](#albums)

### Outro

* [Verificação de integridade](#health-check)
* [Recuperar metadados de catálogo do usuário](#retrieve-user-catalog-metadata)

#### Verificação de integridade

Este módulo de ação recupera uma ID de versão do servidor do Lightroom, provando se o serviço do Lightroom está em execução no momento.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Se quiser fornecer credenciais específicas para garantir que um servidor específico esteja em execução, clique em Adicionar item e insira as credenciais.</p><p>Os cabeçalhos de autorização são adicionados automaticamente.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Recuperar metadados de catálogo do usuário

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Se quiser fornecer credenciais específicas para garantir que você possa acessar a conta de usuário correta, clique em Adicionar item e insira as credenciais.</p><p>Os cabeçalhos de autorização são adicionados automaticamente.</p>
      </td>
    </tr>
  </tbody>
</table>

### Ativos

* [Criar um arquivo original de ativo](#create-an-asset-external-xmp-develop-setting-file)
* [Criar um ativo](#create-an-asset)
* [Criar um arquivo externo de configuração de desenvolvimento de XMP do ativo](#create-an-asset-external-xmp-develop-setting-file)
* [Gerar representações para um arquivo original](#generate-renditions-for-an-original-file)
* [Obter um ativo de catálogo](#get-a-catalog-asset)
* [Obter a configuração mais recente de desenvolvimento de XMP externo de ativos](#get-the-latest-asset-external-xmp-develop-setting-file)
* [Obter a representação de ativo mais recente](#get-the-latest-asset-rendition)
* [Recuperar ativos](#retrieve-assets)

#### Criar um arquivo original de ativo

Esse módulo de ação cria e faz upload de um arquivo original para um ativo.


<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo para o qual você deseja criar e fazer upload de um arquivo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Insira ou mapeie o comprimento do conteúdo em bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Byte range]</td>
      <td>
        <p>Insira ou mapeie o intervalo de bytes da solicitação, incluindo o primeiro e o último bytes e o comprimento da entidade conforme definido no RFC 2616. Deve ser incluído somente quando os dados são muito grandes para serem carregados em uma única chamada.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content type]</td>
      <td>
        <p>Selecione o tipo de conteúdo para o novo arquivo.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Criar um ativo

Esse módulo de ação cria um novo ativo com metadados iniciais e informações de importação.


<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo onde o ativo será criado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Insira ou mapeie a ID do novo ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset type]</td>
      <td>
        <p>Selecione se o ativo é uma imagem ou um vídeo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user created]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user updated]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Date captured]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Criar um arquivo externo de configuração de desenvolvimento de XMP do ativo

Esse módulo de ação suporta dois workflows. O primeiro fluxo de trabalho é carregar o arquivo externo de configurações de desenvolvimento de XMP para o ativo. O segundo fluxo de trabalho é criar um arquivo externo de configurações de desenvolvimento de XMP copiando do arquivo externo de configuração de desenvolvimento xmp de outro ativo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Insira ou mapeie o comprimento do conteúdo em bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Upload new or copy XMP/develop file]</td>
      <td>
        <p>Selecione se você está fazendo upload de um novo arquivo ou copiando um arquivo de um ativo existente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo para o qual você deseja fazer upload ou copiar um arquivo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Link to XMP/develop file]</td>
      <td>
        <p>Insira ou mapeie um link para o arquivo que deseja fazer upload ou copiar.</p><p>Esse arquivo deve ser JSON ao copiar um arquivo ou XML ao fazer upload de um arquivo.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Gerar representações para um arquivo original

Esse módulo de ação gera representações de forma assíncrona para um arquivo original.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rendition Type(s) (semi-colon separated)]</td>
      <td>
        <p>Insira o tipo de representação da representação que deseja criar. Se inserir mais de um tipo, separe-os com um ponto e vírgula (;). <p>Tipos possíveis:</p><ul><li><code>fullsize</code></li><li><code>2560</code></li></ul></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Insira ou mapeie o comprimento do conteúdo em bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo para o qual você deseja criar uma representação de um arquivo.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Obter um ativo de catálogo

Este módulo de ação recupera informações sobre um único ativo em um catálogo. O catálogo deve ser de propriedade do usuário cujas credenciais estão representadas na conexão usada neste módulo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo para o qual deseja recuperar as informações.</p>
      </td>
    </tr>
  </tbody>
</table>


#### Obter o arquivo de configuração de desenvolvimento de XMP externo de ativo mais recente

Esse módulo de ação recupera o arquivo de configuração XMP externo do ativo mais recente.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo associado ao arquivo de configuração de desenvolvimento do XMP.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Obter a representação de ativo mais recente

Este módulo de ação recupera a representação de ativo mais recente do tipo especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo associado ao arquivo de configuração de desenvolvimento do XMP.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rendition type]</td>
      <td>
        <p>Selecione o tipo de representação que deseja recuperar.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Recuperar ativos

Este módulo de ação recupera ativos de propriedade do usuário cujas credenciais estão representadas na conexão usada neste módulo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starting timestamp]</td>
      <td>
        <p>Insira ou mapeie um carimbo de data e hora. O módulo retorna registros que foram atualizados após esse carimbo de data e hora.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Return assets captured before]</td>
      <td>
        <p>Insira uma data com o formato <code>YYYY-MM-DDT00:00:00</code>. O módulo retorna resultados capturados antes dessa data.</p><p> Este campo não pode ser usado com o campo <code>Return assets captured after</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned assets]</td>
      <td>
        <p>Defina o número máximo de ativos que [!DNL Workfront Fusion] retornará durante um ciclo de execução. Este número deve ser menor ou igual a 100.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SHA256 Hash value of original file]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Hide assets that are inside stacks?"]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset subtype values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset IDs]</td>
      <td>
        <p>Insira ou mapeie até 100 IDs de ativos, separadas por vírgulas.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Types of assets to exclude]</td>
      <td>
        <p>Selecione se deseja excluir ativos completos ou incompletos. Para incluir todos os ativos, deixe este campo em branco.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Group values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Favorite status]</td>
      <td>
        <p></p>
      </td>
    </tr>
    </tr>
  </tbody>
</table>

### Álbuns

* [Adicionar ativos a um álbum](#add-assets-to-an-album)
* [Criar um álbum](#create-an-album)
* [Excluir um álbum](#delete-an-album)
* [Obter um álbum](#get-an-album)
* [Listar os ativos de um álbum](#list-assets-of-an-album)
* [Recuperar álbuns](#retrieve-albums)
* [Atualizar um álbum](#update-album)

#### Adicionar ativos a um álbum

Este módulo de ação adiciona um ou mais ativos ao álbum especificado. Você pode adicionar até 50 ativos em um ciclo de execução.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum ao qual você deseja adicionar ativos.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Insira ou mapeie a ID do álbum ao qual você deseja adicionar ativos.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Assets]</td>
      <td>
        <p>Para cada ativo que você deseja adicionar ao álbum, clique em <b>Adicionar item</b> e insira os seguintes campos.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo que você deseja adicionar ao álbum</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Is this asset an album cover?]</td>
      <td>
        <p>Selecione se deseja que esse ativo seja exibido como a imagem que representa o álbum.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Order]</td>
      <td>
        <p></p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Metadata]</td>
      <td>
        <p>Insira ou mapeie quaisquer metadados que deseja incluir com o ativo. Deve ser uma única cadeia de texto com um comprimento máximo de 1 a 24 caracteres.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Remote ID]</td>
      <td>
        <p>Insira um identificador para o ativo.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Criar um álbum

Este módulo de ação cria um novo álbum no Lightroom.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo em que deseja criar um álbum.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Insira ou mapeie uma ID para o novo álbum.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype]</td>
      <td>
        <p>Selecione o subtipo do álbum.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL API key]</td>
      <td>
        <p>Insira a chave da API do serviço que está criando o álbum.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user created]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user updated]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album name]</td>
      <td>
        <p>Insira ou mapeie um nome para o novo álbum.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Cover ID]</td>
      <td>
        <p>Insira ou mapeie a ID de um ativo para usar como capa deste álbum.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Remote ID]</td>
      <td>
        <p>Insira um identificador para o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Created date]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Updated date]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Is the album deleted?]</td>
      <td>
        <p>Ative essa opção se o conteúdo externo afiliado tiver sido excluído.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to edit affiliated content]</td>
      <td>
        <p>Se houver um URL no qual os usuários possam editar o conteúdo desse álbum, insira o URL aqui.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to view affiliated content]</td>
      <td>
        <p>Se houver um URL no qual os usuários possam visualizar o conteúdo desse álbum, insira o URL aqui.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Excluir um álbum

Este módulo de ação exclui um álbum.

O álbum excluído deve ter sido criado pelo mesmo aplicativo cliente que o está excluindo agora e deve ser do subtipo `project` ou `project_set`.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum que você deseja excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Insira ou mapeie a ID do álbum que você deseja excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Delete child albums?]</td>
      <td>
        <p>Selecione se deseja excluir os álbuns filhos do álbum excluído.</p>
      </td>
    </tr>
  </tbody>
</table>

### Obter um álbum

Este módulo de ação recupera o álbum especificado

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum que você deseja recuperar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Insira ou mapeie a ID do álbum que você deseja recuperar.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Listar os ativos de um álbum

Este módulo de ação recupera uma lista de ativos no álbum especificado.



#### Recuperar álbuns

Este módulo de ação recupera uma lista de álbuns no catálogo especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém os álbuns que você deseja recuperar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtypes]</td>
      <td>
        <p>Insira ou mapeie a ID do álbum que você deseja recuperar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name of album to precede current results]</td>
      <td>
        <p>Se estiver paginando os resultados, digite ou mapeie o nome do último álbum na página anterior.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned albums]</td>
      <td>
        <p>Defina o número máximo de ativos que [!DNL Workfront Fusion] retornará durante um ciclo de execução. O valor padrão deste campo é 100.Este módulo pode retornar mais álbuns do que este limite se vários álbuns no limite tiverem o mesmo valor <code>name_after</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Atualizar álbum

Este módulo de ação atualiza o álbum especificado.

O álbum atualizado deve ter sido criado pelo mesmo aplicativo cliente que o está atualizando, e deve ser do subtipo `project` ou `project_set`.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum que você deseja atualizar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Insira ou mapeie a ID do álbum que você deseja atualizar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Outros campos</td>
      <td>
      <td>Para obter descrições de outros campos neste módulo, consulte <a href="#create-an-album" class="MCXref xref" >Criar um álbum</a> neste artigo.</td>
      </td>
    </tr>
  </tbody>
</table>
