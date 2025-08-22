---
title: Módulos do Adobe Lightroom
description: Com os módulos do Adobe Lightroom, é possível iniciar um cenário do Adobe Workfront Fusion com base em eventos em sua conta do Adobe Lightroom.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '3200'
ht-degree: 0%

---

# [!DNL Adobe Lightroom] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Adobe Lightroom], bem como conectá-lo a vários aplicativos e serviços de terceiros.

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion</p>
   <p>Ou</p>
   <p>Herdados: Automação e integração do Workfront Fusion for Work </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo menu:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Antes de usar o conector [!DNL Adobe Lightroom], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!DNL Adobe Lightroom] ativa.
* Você deve ter um aplicativo web OAuth configurado no Adobe Admin Console. Para obter detalhes, consulte [Configurar um aplicativo OAuth na Adobe Admin Console](#configure-an-oauth-application-in-the-adobe-admin-console) neste artigo.

## Informações da API do Adobe Lightroom

O conector do Adobe Lightroom usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td>https://lr.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.17.128</td> 
  </tr>
 </tbody> 
 </table>



## Criar uma conexão com o Adobe Lightroom

Para se conectar ao Adobe Lightroom, primeiro você deve configurar um aplicativo OAuth no Adobe Admin Console. Depois que esse aplicativo é configurado, você pode criar conexões do Workfront Fusion.

### Configurar um aplicativo OAuth no Adobe Admin Console

1. Comece a configurar um aplicativo web OAuth no Adobe Admin Console.

   Para obter instruções, consulte o [Guia de implementação de autenticação de usuário](https://developer.adobe.com/developer-console/docs/guides/authentication/UserAuthentication/implementation) na documentação do desenvolvedor do Adobe.
1. Ao configurar o OAuth Web App, insira os seguintes valores:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Escopos]</td>
        <td>
          <ul>
            <li>AdobeID</li>
            <li>lr_partner_rendition_apis</li>
            <li>openid</li>
            <li>offline_access</li>
            <li>lr_partner_apis</li>
          </ul>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Redirecionar URI]</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Padrão de URI de redirecionamento]</td>
        <td><code>https://app\.workfrontfusion\.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
      </tbody>
    </table>

### Criar uma conexão com o Adobe Lightroom a partir do Workfront Fusion

Para criar uma conexão para seus módulos do [!DNL Adobe Lightroom]:

1. Em qualquer módulo do Adobe Lightroom, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

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
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID do Cliente]</td>
        <td>Insira sua [!UICONTROL Adobe] [!UICONTROL ID do cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira seu [!DNL Adobe] [!UICONTROL Segredo do Cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.


## Módulos do Adobe Lightroom e seus campos

Ao configurar módulos do [!DNL Adobe Lightroom], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Lightroom] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Outras](#other)
* [Ativos](#assets)
* [Álbuns](#albums)

### Outras

* [Verificação de integridade](#health-check)
* [Recuperar metadados de catálogo do usuário](#retrieve-user-catalog-metadata)

#### Verificação de integridade

Este módulo de ação recupera uma ID de versão do servidor do Lightroom, provando se o serviço do Lightroom está em execução no momento.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credenciais]</td>
      <td>
        <p>Se você deseja fornecer credenciais específicas para garantir que um servidor específico esteja em execução, clique em <b>Adicionar item</b> e insira as credenciais.</p><p>Os cabeçalhos de autorização são adicionados automaticamente.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Recuperar metadados de catálogo do usuário

Este módulo de ação recupera metadados de um catálogo no Adobe Lightroom. Um catálogo contém ativos, álbuns ou outros recursos.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credenciais]</td>
      <td>
        <p>Se quiser fornecer credenciais específicas para garantir que você possa acessar a conta de usuário correta, clique em Adicionar item e insira as credenciais.</p><p>Os cabeçalhos de autorização são adicionados automaticamente.</p>
      </td>
    </tr>
  </tbody>
</table>

### Ativos

* [Criar um arquivo original de ativo](#create-an-asset-original-file)
* [Criar um ativo](#create-an-asset)
* [Criar um arquivo de configuração de desenvolvimento externo do XMP de ativos](#create-an-asset-external-xmp-develop-setting-file)
* [Gerar representações para um arquivo original](#generate-renditions-for-an-original-file)
* [Obter um ativo de catálogo](#get-a-catalog-asset)
* [Obter a configuração mais recente de desenvolvimento de ativos XMP externos](#get-the-latest-asset-external-xmp-develop-setting-file)
* [Obter a representação de ativo mais recente](#get-the-latest-asset-rendition)
* [Recuperar ativos](#retrieve-assets)

#### Criar um arquivo original de ativo

Esse módulo de ação cria e faz upload de um arquivo original para um ativo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Ativo]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo para o qual você deseja criar e fazer upload de um arquivo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comprimento do conteúdo em bytes]</td>
      <td>
        <p>Insira ou mapeie o comprimento do conteúdo em bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Intervalo de bytes]</td>
      <td>
        <p>Insira ou mapeie o intervalo de bytes da solicitação, incluindo o primeiro e o último bytes e o comprimento da entidade conforme definido no RFC 2616. Essas informações devem ser incluídas somente quando os dados forem muito grandes para serem carregados em uma única chamada.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de conteúdo]</td>
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
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo onde o ativo será criado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Ativo]</td>
      <td>
        <p>Insira ou mapeie a ID do novo ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de ativo]</td>
      <td>
        <p>Selecione se o ativo é uma imagem ou um vídeo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime criado pelo usuário]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data e hora atualizado pelo usuário]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data capturada]</td>
      <td>
        <p>Insira ou mapeie a data de captura do ativo com o formato <code>YYYY-MM-DDT00:00:00-00:00</code>. Ele será definido pelo servidor se a Data capturada estiver definida como <code>0000-00-00T00:00:00</code>. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome do arquivo]</td>
      <td>
        <p>Insira ou mapeie o nome do arquivo do ativo que você está importando para o Lightroom.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome do Dispositivo Importado em]</td>
      <td>
        <p>Insira ou mapeie o nome do dispositivo que importa o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID da Conta do Usuário que Importou]</td>
      <td>
        <p>Insira ou mapeie a ID do usuário que importa o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Importar Carimbo de Data/Hora]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Criar um arquivo de configuração de desenvolvimento externo do XMP de ativos

Esse módulo de ação é compatível com dois fluxos de trabalho: fazer upload do arquivo externo de configurações de desenvolvimento do XMP para o ativo ou criar um arquivo externo de configurações de desenvolvimento do XMP copiando do arquivo externo de configuração de desenvolvimento xmp de outro ativo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tamanho do Conteúdo em Bytes]</td>
      <td>
        <p>Insira ou mapeie o comprimento do conteúdo em bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Carregar arquivo XMP/develop novo ou copiado]</td>
      <td>
        <p>Selecione se você está fazendo upload de um novo arquivo ou copiando um arquivo de um ativo existente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo em que deseja criar o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Ativo]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo para o qual você deseja fazer upload ou copiar um arquivo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Vincular ao XMP/desenvolver arquivo]</td>
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
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo(s) de representação (separados por ponto-e-vírgula)]</td>
      <td>
        <p>Insira o tipo de representação da representação que deseja criar. Se inserir mais de um tipo, separe-os com um ponto e vírgula (;). <p>Tipos possíveis:</p><ul><li><code>fullsize</code></li><li><code>2560</code></li></ul></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comprimento do conteúdo em bytes]</td>
      <td>
        <p>Insira ou mapeie o comprimento do conteúdo em bytes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo em que deseja gerar as representações.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Ativo]</td>
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
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Ativo]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo para o qual deseja recuperar as informações.</p>
      </td>
    </tr>
  </tbody>
</table>


#### Obter o arquivo de configuração de desenvolvimento de XMP externo de ativos mais recente

Este módulo de ação recupera o arquivo de configuração XMP externo de ativo mais recente.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo associado ao arquivo de configuração de desenvolvimento do XMP.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Ativo]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo associado ao arquivo de configuração de desenvolvimento do XMP.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Obter a última representação de ativos

Este módulo de ação recupera a representação de ativo mais recente do tipo especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo para o qual você deseja recuperar uma representação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Ativo]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo para o qual você deseja recuperar uma representação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de representação]</td>
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
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Iniciando carimbo de data/hora]</td>
      <td>
        <p>Insira ou mapeie um carimbo de data e hora. O módulo retorna registros que foram atualizados após esse carimbo de data e hora.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Retornar ativos capturados antes do tempo especificado]</td>
      <td>
        <p>Insira uma data com o formato <code>YYYY-MM-DDT00:00:00</code>. O módulo retorna resultados capturados antes dessa data.</p><p> Este campo não pode ser usado com o campo <code>Return assets captured after given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Retornar ativos capturados após determinado tempo]</td>
      <td>
        <p>Insira uma data com o formato <code>YYYY-MM-DDT00:00:00</code>. O módulo retorna resultados capturados antes dessa data.</p><p> Este campo não pode ser usado com o campo <code>Return assets captured before given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Número máximo de ativos retornados]</td>
      <td>
        <p>Insira o número máximo de registros que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL valor de hash SHA256 do arquivo original]</td>
      <td>
        <p>Insira ou mapeie o valor de hash do arquivo original. O Assets com um hash correspondente é retornado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ocultar ativos que estão dentro de pilhas?"]</td>
      <td>
        <p>Selecione Sim para ocultar ativos dentro de pilhas (os ativos dentro de pilhas não são retornados). Selecione Não para incluir ativos em pilhas nos resultados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Valores de subtipo de ativo]</td>
      <td>
        <p>Insira ou mapeie uma lista separada por ponto e vírgula de valores de subtipo a serem retornados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL IDs de Ativo]</td>
      <td>
        <p>Insira ou mapeie até 100 IDs de ativos, separadas por vírgulas.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipos de ativos a serem excluídos]</td>
      <td>
        <p>Selecione se deseja excluir ativos completos ou incompletos. Para incluir todos os ativos, deixe este campo em branco.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Agrupar valores]</td>
      <td>
        <p>Insira ou mapeie uma lista de valores de grupo separados por ponto-e-vírgula.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nomear valores]</td>
      <td>
        <p>Insira ou mapeie uma lista de valores de nome separados por ponto-e-vírgula.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Status Favorito]</td>
      <td>
        <p>Insira ou mapeie o status favorito para o qual deseja retornar resultados.</p>
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
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum ao qual você deseja adicionar ativos.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Álbum]</td>
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
      <td role="rowheader">[!UICONTROL ID de Ativo]</td>
      <td>
        <p>Insira ou mapeie a ID do ativo que você deseja adicionar ao álbum</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Este ativo é uma capa de álbum?]</td>
      <td>
        <p>Selecione se deseja que esse ativo seja exibido como a imagem que representa o álbum.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Ordem]</td>
      <td>
        <p>Especifique a ordem do ativo.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Carga do Serviço]</td>
      <td>
        <p>Insira ou mapeie quaisquer metadados que deseja incluir com o ativo. Deve ser uma única cadeia de texto com um comprimento máximo de 1 a 24 caracteres.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL ID Remota]</td>
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
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo em que deseja criar um álbum.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Álbum]</td>
      <td>
        <p>Insira ou mapeie uma ID para o novo álbum.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtipo]</td>
      <td>
        <p>Selecione o subtipo do álbum.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Serviço]</td>
      <td>
        <p>Insira a chave da API do serviço que está criando o álbum.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Data de Criação pelo Usuário]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Atualização de Usuário de Data]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome do Álbum]</td>
      <td>
        <p>Insira ou mapeie um nome para o novo álbum.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Capa]</td>
      <td>
        <p>Insira ou mapeie a ID de um ativo para usar como capa deste álbum.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID Pai]</td>
      <td>
        <p>Insira ou mapeie a ID do responsável deste álbum.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Carga do Serviço]</td>
      <td>
        <p>Insira ou mapeie os metadados do álbum como uma sequência de caracteres.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID Remota]</td>
      <td>
        <p>Insira um identificador para o ativo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data de criação]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Data de atualização]</td>
      <td>
        <p>Insira ou mapeie uma data com o formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL O álbum foi excluído?]</td>
      <td>
        <p>Ative essa opção se o conteúdo externo afiliado tiver sido excluído.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL do local para editar conteúdo afiliado]</td>
      <td>
        <p>Se houver um URL no qual os usuários possam editar o conteúdo desse álbum, insira o URL aqui.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL do local para exibir conteúdo afiliado]</td>
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
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum que você deseja excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Álbum]</td>
      <td>
        <p>Insira ou mapeie a ID do álbum que você deseja excluir.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Excluir álbuns filhos?]</td>
      <td>
        <p>Selecione se deseja excluir os álbuns filhos do álbum excluído.</p>
      </td>
    </tr>
  </tbody>
</table>

### Obter um álbum

Este módulo de ação recupera o álbum especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum que você deseja recuperar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Álbum]</td>
      <td>
        <p>Insira ou mapeie a ID do álbum que você deseja recuperar.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Listar os ativos de um álbum

Este módulo de ação recupera uma lista de ativos no álbum especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Álbum]</td>
      <td>
        <p>Insira ou mapeie a ID do álbum para o qual deseja listar ativos.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Capturar Assets Antes do Tempo]</td>
      <td>
        <p>Insira uma data com o formato <code>YYYY-MM-DDT00:00:00</code>. O módulo retorna resultados capturados antes dessa data.</p><p> Este campo não pode ser usado com o campo <code>Return assets captured after given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Capturar Assets Depois do Tempo]</td>
      <td>
        <p>Insira uma data com o formato <code>YYYY-MM-DDT00:00:00</code>. O módulo retorna resultados capturados antes dessa data.</p><p> Este campo não pode ser usado com o campo <code>Return assets captured before given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Valor de Ordem de Ativo Final]</td>
      <td>
        <p>Insira ou mapeie o valor do pedido do ativo final.</p><p> Este campo só pode ser usado com o campo <code>Capture Assets After Time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Iniciando Valor de Ordem de Ativo]</td>
      <td>
        <p>Insira ou mapeie o valor do pedido do ativo inicial.</p><p> Este campo só pode ser usado com o campo <code>Capture Assets BEfore Time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Número de Assets a serem retornados (1-500)]</td>
      <td>
        <p>Insira o número máximo de registros que você deseja que o módulo retorne durante cada ciclo de execução de cenário. Esse número deve estar entre 1-500.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ocultar ativos que estão dentro de pilhas?"]</td>
      <td>
        <p>Selecione Sim para ocultar ativos dentro de pilhas (os ativos dentro de pilhas não são retornados). Selecione Não para incluir ativos em pilhas nos resultados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Valores de Subtipo (separados por ponto e vírgula)]</td>
      <td>
        <p>Insira ou mapeie uma lista separada por ponto e vírgula de valores de subtipo a serem retornados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Sinalizar Valores (separados por ponto-e-vírgula)]</td>
      <td>
        <p>Insira ou mapeie uma lista separada por ponto e vírgula de valores de sinalizador a serem retornados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Campos de Dados Adicionais a Serem Incluídos (separados por ponto e vírgula)]</td>
      <td>
        <p>Se o ativo for incluído, todos os campos serão incluídos, caso contrário, somente a id e o link self href serão retornados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipos de ativos a serem excluídos]</td>
      <td>
        <p>Selecione se deseja excluir ativos completos ou incompletos. Para incluir todos os ativos, deixe este campo em branco.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL IDs de Ativo]</td>
      <td>
        <p>Insira ou mapeie até 100 IDs de ativos, separadas por vírgulas.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Filtrar ativos do álbum com base nos filtros de apresentação]</td>
      <td>
        <p>Quando esse campo é definido como 'true', ele filtra todos os ativos do álbum com base nos filtros de apresentação definidos no álbum. Com esse parâmetro, os ativos rejeitados sempre são filtrados independentemente das configurações nos filtros de apresentação. Os filtros de apresentação não são aplicados quando qualquer valor diferente de 'true' está definido para album_filters. O comportamento padrão é exibir todos os ativos. Este parâmetro não pode ser usado junto com o parâmetro de sinalizador. </p>
      </td>
    </tr>
  </tbody>
</table>

#### Recuperar álbuns

Este módulo de ação recupera uma lista de álbuns no catálogo especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém os álbuns que você deseja recuperar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtipos]</td>
      <td>
        <p>Insira ou mapeie uma lista separada por ponto e vírgula de valores de subtipo a serem retornados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome do álbum para preceder os resultados atuais]</td>
      <td>
        <p>Se estiver paginando os resultados, digite ou mapeie o nome do último álbum na página anterior.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Número de Álbuns a Serem Retornados]</td>
      <td>
        <p>Defina o número máximo de ativos que o Workfront Fusion retornará durante um ciclo de execução. O valor padrão deste campo é 100.Este módulo pode retornar mais álbuns do que este limite se vários álbuns no limite tiverem o mesmo valor <code>name_after</code>.</p>
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
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Lightroom], consulte <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Lightroom]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Catálogo]</td>
      <td>
        <p>Insira ou mapeie a ID do catálogo que contém o álbum que você deseja atualizar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Álbum]</td>
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
