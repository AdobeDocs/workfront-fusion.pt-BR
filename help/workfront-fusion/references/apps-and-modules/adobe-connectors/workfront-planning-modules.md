---
title: Módulos do Adobe Workfront Planning
description: Com os  [!DNL Adobe Workfront Planning] módulos, você pode iniciar um cenário do Adobe Workfront Fusion com base em eventos na sua  [!DNL Adobe] conta do Workfront Planning, criar, ler ou atualizar contratos e outros registros, pesquisar registros usando critérios definidos por você e carregar documentos.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
TQID: https://experienceleague.adobe.com/QHOFWDOT-18-c0b3wLXsRV5cjGVxlcyLhvZdkev3GFg
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: f0e185778e01b71a91837531a082e88485e97ca2
workflow-type: tm+mt
source-wordcount: 6075
ht-degree: 35%

---


# Módulos do Adobe Workfront Planning

Com os módulos [!DNL Adobe Workfront Planning], é possível acionar um cenário quando os eventos ocorrem no Workfront Planning. Você também pode criar, ler, atualizar e excluir registros ou executar uma chamada de API personalizada para sua conta do [!DNL Adobe Workfront Planning].

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
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Pré-requisitos

Para acessar o Workfront Planning, é necessário ter o seguinte:

* Um novo pacote e licença do Workfront. O Workfront Planning não está disponível para pacotes ou licenças herdadas do Workfront.
* Um pacote do Workfront Planning.
* A instância da Workfront de sua organização deve ser integrada à Adobe Unified Experience.

## Informações da API do Adobe Workfront Planning

O conector do Adobe Workfront Planning usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td><pre><code>https://&#123;&#123;connection.host&#125;&#125;/maestro/api/&#123;&#123;common.maestroApiVersion&#125;&#125;/</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o Workfront Planning ao Workfront Fusion

O conector do Workfront Planning usa o OAuth 2.0 para se conectar ao Workfront Planning.

Você pode criar uma conexão com sua conta do Workfront Planning diretamente de um módulo do Workfront Planning Fusion.

* [Conectar-se ao Workfront Planning usando a ID do cliente e o segredo do cliente](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [Conectar-se ao Workfront Planning usando uma conexão Servidor a Servidor](#connect-to-workfront--planning-using-a-server-to-server-connection)

### Conectar-se ao Workfront Planning usando a ID do cliente e o segredo do cliente

1. Em qualquer módulo do Adobe Workfront Planning, clique em **Adicionar** ao lado do campo Conexão.
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
          <p>Selecione a conexão <b>autenticação do Adobe Workfront</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Insira um nome para a nova conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira sua ID de cliente do Workfront. Isso pode ser encontrado na área Aplicativos OAuth2 da área Configuração no Workfront. Abra o aplicativo específico ao qual você está se conectando para ver a ID de cliente.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira o segredo do cliente do Workfront. Isso pode ser encontrado na área Aplicativos OAuth2 da área Configuração no Workfront. Se não tiver um segredo do cliente para o aplicativo OAuth2 no Workfront, você poderá gerar outro. Para obter instruções, consulte a documentação do Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>Isso pode permanecer como o valor padrão, ou você pode inserir o URL da sua instância do Workfront, seguido por <code>/integrations/oauth2</code>. <p>Exemplo: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>Na maioria dos casos, esse valor deve ser <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

   Se você não estiver conectado ao Workfront Planning, será direcionado para uma tela de logon. Depois de fazer logon, é possível permitir a conexão.

>[!NOTE]
>
>* As conexões do OAuth 2.0 com a API do Workfront não dependem mais das chaves de API.
>* Para criar uma conexão com um ambiente de Sandbox do Workfront, crie um aplicativo OAuth2 nesse ambiente e use a ID do cliente e o segredo do cliente gerados por esse aplicativo em sua conexão.

### Conectar-se ao Workfront Planning usando uma conexão Servidor a Servidor

1. Em qualquer módulo do Adobe Workfront Planning, clique em **Adicionar** ao lado do campo Conexão.
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
          <p>Selecione <b>Conexão de servidor para servidor do Adobe Workfront</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Insira um nome para a nova conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance name]</td>
        <td>
          <p>Insira o nome da instância, também conhecido como domínio.</p><p>Exemplo: se a URL for <code>https://example.my.workfront.com</code>, insira <code>example</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance lane]</td>
        <td>
          <p>Insira o tipo de ambiente ao qual esta conexão será feita.</p><p>Exemplo: se a URL for <code>https://example.my.workfront.com</code>, insira <code>my</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira sua ID de cliente do Workfront. Isso pode ser encontrado na área Aplicativos OAuth2 da área Configuração no Workfront. Abra o aplicativo específico ao qual você está se conectando para ver a ID de cliente.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira o segredo do cliente do Workfront. Isso pode ser encontrado na área Aplicativos OAuth2 da área Configuração no Workfront. Se não tiver um segredo do cliente para o aplicativo OAuth2 no Workfront, você poderá gerar outro. Para obter instruções, consulte a documentação do Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Insira todos os escopos aplicáveis para esta conexão.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>Na maioria dos casos, esse valor deve ser <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

   Se você não estiver conectado ao Workfront Planning, será direcionado para uma tela de logon. Depois de fazer logon, é possível permitir a conexão.

>[!NOTE]
>
>* As conexões do OAuth 2.0 com a API do Workfront não dependem mais das chaves de API.
>* Para criar uma conexão com um ambiente de Sandbox do Workfront, crie um aplicativo OAuth2 nesse ambiente e use a ID do cliente e o segredo do cliente gerados por esse aplicativo em sua conexão.

## [!DNL Adobe Workfront Planning] módulos da versão 2 e seus campos

>[!IMPORTANT]
>
>Os módulos desta seção pertencem ao conector do Workfront Planning V2.Para módulos no conector do Workfront Planning V1, consulte [[!DNL Adobe Workfront Planning] Módulos da Versão 1 e seus campos](#adobe-workfront-planning-version-1-modules-and-their-fields).

Ao configurar módulos do Workfront Planning, o Workfront Fusion exibe os campos listados abaixo. Junto com esses campos, podem ser exibidos campos adicionais do Workfront, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

* [Espaços de trabalho](#workspaces-v2)
* [Tipos de registro](#record-types-v2)
* [Registros](#records-v2)
* [Campos](#fields-v2)
* [Exibições](#views-v2)
* [Permissões](#permissions-v2)
* [Outras](#other-v2)

### Espaços De Trabalho (V2)

* [Criar um espaço de trabalho](#create-a-workspace-v2)
* [Excluir um espaço de trabalho](#delete-a-workspace-v2)
* [Obter todos os espaços de trabalho](#get-all-workspaces-v2)
* [Obter um espaço de trabalho](#get-a-workspace-v2)
* [Atualizar um espaço de trabalho](#update-a-workspace-v2)

#### Criar um espaço de trabalho (V2)

Este módulo de ação cria um novo espaço de trabalho no Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace name]</p>
      </td>
      <td>Insira ou mapeie um nome para o novo espaço de trabalho.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrição</p>
      </td>
      <td>Insira ou mapeie uma descrição para o novo espaço de trabalho/td&gt; 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Cor</p>
      </td>
      <td>Selecione a cor que deseja usar para representar o novo tipo de registro</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ícone</p>
      </td>
      <td>Mapeie o ícone que você deseja usar para este tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Proprietário</p>
      </td>
      <td>Insira ou mapeie a ID de usuário do Adobe IMS do usuário que você deseja que seja o proprietário do espaço de trabalho.</td> 
    </tr>
  </tbody>
</table>

#### Excluir um espaço de trabalho (V2)

Este módulo de ação exclui um único espaço de trabalho, especificado pela ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace ID]</p>
      </td>
      <td>Insira ou mapeie a ID do espaço de trabalho que deseja excluir.</td> 
    </tr>
  </tbody>
</table>

#### Obter todos os espaços de trabalho (V2)

Este módulo recupera uma lista de todos os espaços de trabalho.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de workspaces retornados]</p>
      </td>
      <td>Insira ou mapeie o número máximo de espaços de trabalho que o módulo retornará durante um ciclo de execução.</td> 
    </tr>
  </tbody>
</table>

#### Obter um espaço de trabalho (V2)

Este módulo recupera um espaço de trabalho pela respectiva ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace ID]</p>
      </td>
      <td>Insira ou mapeie a ID do espaço de trabalho que você deseja recuperar.</td> 
    </tr>
  </tbody>
</table>

#### Atualizar um espaço de trabalho (V2)

Este módulo de ação atualiza um novo espaço de trabalho no Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que deseja atualizar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace name]</p>
      </td>
      <td>Insira ou mapeie um nome para o novo espaço de trabalho.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrição</p>
      </td>
      <td>Insira ou mapeie uma descrição para o novo espaço de trabalho/td&gt; 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Cor</p>
      </td>
      <td>Selecione a cor que deseja usar para representar o novo tipo de registro</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ícone</p>
      </td>
      <td>Mapeie o ícone que você deseja usar para este tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Proprietário</p>
      </td>
      <td>Insira ou mapeie a ID de usuário do Adobe IMS do usuário que você deseja que seja o proprietário do espaço de trabalho.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Seções de tipo de registro</p>
      </td>
      <td>Para cada seção de tipo de registro que você deseja adicionar a este espaço de trabalho, clique em <b>Adicionar item</b> e insira o nome da seção, as IDs de tipo de registro e se deseja substituir as IDs de tipo de registro existentes.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Seções do tipo de registro &gt; Substituir</p>
      </td>
      <td>Selecione se as seções existentes devem ser substituídas pelas do módulo. Se não, as seções do módulo serão adicionadas à lista de seções existente.</td> 
    </tr>
  </tbody>
</table>


### Tipos de registro (V2)

* [Criar um tipo de registro](#create-a-record-type-v2)
* [Excluir um tipo de registro](#delete-a-record-type-v2)
* [Obter tipos de registro global](#get-global-record-types-v2)
* [Obter um tipo de registro](#get-a-record-type-v2)
* [Obter tipos de registro](#get-record-types-v2)
* [Atualizar um tipo de registro](#update-a-record-type-v2)

#### Criar um tipo de registro (V2)

Este módulo de ação cria um novo tipo de registro no espaço de trabalho selecionado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho onde deseja criar um tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nome de exibição</p>
      </td>
      <td>Insira ou mapeie um nome para o novo tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrição</p>
      </td>
      <td>Insira ou mapeie uma descrição para o novo tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ícone</p>
      </td>
      <td>Mapeie o ícone que você deseja usar para este tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Cor</p>
      </td>
      <td>Selecione a cor que deseja usar para representar o novo tipo de registro</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Tipo de registro do Source</p>
      </td>
      <td>Se você estiver usando outro tipo de registro para copiar como ponto de partida, selecione esse tipo de registro.</td> 
    </tr>
  </tbody>
</table>

#### Excluir um tipo de registro (V2)

Esse módulo de ação exclui um único tipo de registro, especificado pela ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de tipo de registro]</p>
      </td>
      <td>Informe ou mapeie a ID do tipo de registro que deseja deletar.</td> 
    </tr>
  </tbody>
</table>

#### Obter tipos de registro global (V2)

Este módulo recupera uma lista de tipos de registros em uma conta do Adobe Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione um espaço de trabalho. O módulo retornará os tipos de registro global que estão disponíveis para adicionar a este espaço de trabalho.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de tipos de registros retornados]</p>
      </td>
      <td>Insira ou mapeie o número máximo de tipos de registros que o módulo retornará durante um ciclo de execução.</td> 
    </tr>
  </tbody>
</table>

#### Obter um tipo de registro (V2)

Este módulo recupera um tipo de registro por sua ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de tipo de registro]</p>
      </td>
      <td>Insira ou mapeie a ID do tipo de registro que você deseja recuperar.</td> 
    </tr>
  </tbody>
</table>

#### Obter tipos de registro (V2)

Este módulo recupera uma lista de tipos de registros disponíveis em um determinado espaço de trabalho.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho para o qual deseja recuperar tipos de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de tipos de registros retornados]</p>
      </td>
      <td>Insira ou mapeie o número máximo de tipos de registros que o módulo retornará durante um ciclo de execução.</td> 
    </tr>
  </tbody>
</table>

#### Atualizar um tipo de registro (V2)

Este módulo atualiza um tipo de registro.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho no qual deseja atualizar um tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o espaço de trabalho no qual deseja atualizar um tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nome de exibição</p>
      </td>
      <td>Insira ou mapeie um nome para o tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrição</p>
      </td>
      <td>Insira ou mapeie uma descrição para o tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>ID do campo primário</p>
      </td>
      <td>Insira ou mapeie a ID do campo usado como o título do tipo de registro.</td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>Ícone</p>
      </td>
      <td>Mapeie o ícone que você deseja usar para este tipo de registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Cor</p>
      </td>
      <td>Selecione a cor que deseja usar para representar o novo tipo de registro</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Vinculável a Workspace IDs</p>
      </td>
      <td>Para cada espaço de trabalho ao qual você deseja que esse tipo de registro possa se vincular, clique em <b>Adicionar item</b> e insira a ID do espaço de trabalho.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Vinculável a Workspace IDs &gt; Substituir</p>
      </td>
      <td>Selecione se os espaços de trabalho existentes devem ser substituídos pelos do módulo. Se não, os espaços de trabalho do módulo serão adicionados à lista existente de espaços de trabalho.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autorizado a criar tipo de registro dinâmico</p>
      </td>
      <td>Para cada assunto autorizado a criar tipos de registro dinâmicos com base neste tipo de registro, clique em <b>Adicionar item</b> e insira o tipo e a ID do assunto.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autorizado a criar tipo de registro dinâmico &gt; Substituir</p>
      </td>
      <td>Selecione se os assuntos existentes devem ser substituídos pelos assuntos do módulo. Se não, os assuntos do módulo serão adicionados à lista de assuntos existente.</td> 
    </tr>
  </tbody>
</table>



### Registros (V2)

* [Criar um registro](#create-a-record-v2)
* [Excluir um registro](#delete-a-record-v2)
* [Obter um registro](#get-a-record-v2)
* [Obter registros por tipo de registro](#get-records-by-record-type-v2)
* [Mover registros](#move-records-v2)
* [Pesquisar registros](#search-records-v2)
* [Atualizar um registro](#update-a-record-v2)

#### Criar um registro (V2)

Essa ação cria um único registro no Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho no qual deseja criar um registro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro que deseja criar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Outros campos</p>
      </td>
      <td>Insira os valores que você deseja que o novo registro tenha. Esses campos são baseados no tipo de registro selecionado e são exclusivos de sua organização do Workfront Planning.</td> 
    </tr>
  </tbody>
</table>

#### Excluir um registro (V2)

Esse módulo de ação exclui um único registro, especificado pela ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Registro]</p>
      </td>
      <td>Insira ou mapeie a ID do registro que deseja excluir.</td> 
    </tr>
  </tbody>
</table>

#### Obter um registro (V2)

Este módulo de ação recupera um registro, especificado por sua ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace ID]</p>
      </td>
      <td>Insira ou mapeie a ID do registro que você deseja recuperar.</td> 
    </tr>
  </tbody>
</table>

#### Obter registros por tipo de registro (V2)

Este módulo recupera uma lista de todos os registros do tipo de registro fornecido.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que contém os registros que você deseja recuperar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro que deseja retornar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de registros retornados]</p>
      </td>
      <td>Insira ou mapeie o número máximo de registros que o módulo retornará durante um ciclo de execução.</td> 
    </tr>
  </tbody>
</table>

#### Mover registros (V2)

Este módulo reorganiza um ou mais registros em um tipo de registro especificando onde colocá-los.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que contém os registros que você deseja mover.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro que deseja mover.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que contém os registros que você deseja mover.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que contém os registros que você deseja mover.</td> 
    </tr>
  </tbody>
</table>

#### Pesquisar registros (V2)

Retornar registros com base nos critérios especificados

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que contém os registros que você deseja recuperar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro que contém os registros que você deseja recuperar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Outros campos]</p>
      </td>
      <td>Para cada campo que deseja filtrar, insira o operador e o valor desse campo. Esses campos são baseados no tipo de registro selecionado e são exclusivos de sua organização do Workfront Planning.</td> 
    </tr>
  </tbody>
</table>

#### Atualizar um registro (V2)

Este módulo atualiza o registro especificado.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que contém o registro que você deseja atualizar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de tipo de registro]</p>
      </td>
      <td>Selecione o tipo de registro que deseja atualizar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Registro]</p>
      </td>
      <td>Insira ou mapeie a ID do registro que você deseja atualizar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Outros campos]</p>
      </td>
      <td>Insira valores para outros campos. Os campos disponíveis dependem do registro selecionado.</td> 
    </tr>
  </tbody>
</table>


### Campos (V2)

* [Criar um campo](#create-a-field-v2)
* [Excluir um campo](#delete-a-field-v2)
* [Obter um campo](#get-a-field-v2)
* [Obter campos por tipo de registro](#get-fields-by-record-type-v2)
* [Atualizar um campo](#update-a-field-v2)

#### Criar um campo (V2)

Esse módulo de ação cria um novo campo no tipo de registro especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho onde deseja criar um campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro para o qual deseja criar um campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nome de exibição</p>
      </td>
      <td>Insira ou mapeie um nome para o novo campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrição</p>
      </td>
      <td>Insira ou mapeie uma descrição para o novo campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Tipo de campo</p>
      </td>
      <td>Selecione o tipo de dados do campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Outros campos</p>
      </td>
      <td>Outros campos específicos para o tipo de campo selecionado podem estar disponíveis. Preencha os valores para esses campos.</td> 
    </tr>
  </tbody>
</table>

#### Excluir um campo (V2)

Esse módulo de ação exclui um único campo, especificado pela ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Campo]</p>
      </td>
      <td>Insira ou mapeie o ID do campo que você deseja excluir.</td> 
    </tr>
  </tbody>
</table>

#### Obter um campo (V2)

Este módulo recupera um campo por sua ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Campo]</p>
      </td>
      <td>Insira ou mapeie a ID do campo que você deseja recuperar.</td> 
    </tr>
  </tbody>
</table>

#### Obter campos por tipo de registro (V2)

Este módulo recupera uma lista de campos para um tipo de registro específico.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que contém os campos que deseja retornar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro para o qual você deseja retornar campos.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de campos retornados]</p>
      </td>
      <td>Insira ou mapeie o número máximo de campos que o módulo retornará durante um ciclo de execução.</td> 
    </tr>
  </tbody>
</table>

#### Atualizar um campo (V2)

Este módulo atualiza parcialmente um campo por sua ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de recurso]</p>
      </td>
      <td>Selecione o tipo de recurso que contém o campo que você deseja atualizar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Campo]</p>
      </td>
      <td>Selecione o campo que deseja atualizar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nome para exibição]</p>
      </td>
      <td>Insira ou mapeie um nome para o campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Description]</p>
      </td>
      <td>Insira ou mapeie uma descrição para o campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Outros parâmetros]</p>
      </td>
      <td>Insira valores para outros parâmetros de campo. Os parâmetros disponíveis dependem do campo selecionado.</td> 
    </tr>
  </tbody>
</table>


### Visualizações (V2)

* [Criar um modo de exibição](#create-a-view-v2)
* [Excluir um modo de exibição](#delete-a-view-v2)
* [Obter uma visualização](#get-a-view-v2)
* [Obter visualizações por tipo de registro](#get-views-by-record-type-v2)
* [Atualizar uma exibição](#update-a-view-v2)

#### Criar uma visualização (V2)

Esse módulo de ação cria uma nova exibição para o tipo de registro selecionado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho no qual deseja criar uma view.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro para o qual deseja criar uma exibição.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Exibir nome</p>
      </td>
      <td>Insira ou mapeie um nome para a nova exibição.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Tipo de visualização</p>
      </td>
      <td>Selecione se a nova exibição é uma exibição de tabela, linha do tempo ou calendário.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Campo de data inicial</p>
      </td>
      <td>Se a exibição for uma exibição de linha do tempo ou calendário, selecione o campo que a exibição usará para colocar o registro na linha do tempo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Campo de data final.</p>
      </td>
      <td>Se a exibição for uma exibição de linha do tempo ou calendário, selecione o campo que a exibição usará para determinar a data final na linha do tempo.</td> 
    </tr>
  </tbody>
</table>

#### Excluir um modo de exibição (V2)

Esse módulo de ação exclui uma única visualização, especificada pela ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Exibir ID]</p>
      </td>
      <td>Informe ou mapeie a ID da view que deseja deletar.</td> 
    </tr>
  </tbody>
</table>

#### Obter uma visualização (V2)

Este módulo recupera uma visualização por sua ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Exibir ID]</p>
      </td>
      <td>Informe ou mapeie a ID da view que deseja recuperar.</td> 
    </tr>
  </tbody>
</table>

#### Obter visualizações por tipo de registro (V2)

Esse módulo recupera uma lista de exibições para o tipo de registro específico.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho que contém as views que você deseja recuperar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro que contém as exibições que você deseja recuperar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Número máximo de exibições retornadas]</p>
      </td>
      <td>Insira ou mapeie o número máximo de exibições que o módulo retornará durante um ciclo de execução.</td> 
    </tr>
  </tbody>
</table>

#### Atualizar uma visualização (V2)

Este módulo de ação atualiza a exibição especificada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Selecione o espaço de trabalho no qual deseja atualizar uma view.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro para o qual você deseja atualizar uma exibição.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>ID da Visualização</p>
      </td>
      <td>Selecione a view que deseja atualizar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Exibir nome</p>
      </td>
      <td>Insira ou mapeie um nome para a nova exibição.</td> 
    </tr>
  </tbody>
</table>

### Permissões (V2)

* [Ignorar solicitações de acesso](#dismiss-access-requests-v2)
* [Obter todos os membros e suas funções para um recurso](#get-all-members-and-their-roles-for-a-resource-v2)
* [Obter as permissões efetivas do usuário atual em um recurso](#get-the-current-users-effective-permissions-on-a-resource-v2)
* [Listar solicitações de acesso pendentes de um recurso](#list-pending-access-requests-for-a-resource-v2)
* [Solicitar acesso a um recurso](#request-access-to-a-resource-v2)

#### Ignorar solicitações de acesso (V2)

Este módulo de ação ignora uma ou mais solicitações de acesso, especificadas pela ID.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de recurso]</p>
      </td>
      <td>Insira ou mapeie a ID da Workspace que deseja excluir.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Recurso]</p>
      </td>
      <td>Insira ou mapeie a ID do recurso para o qual você deseja descartar solicitações de acesso.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL IDs de Solicitação]</p>
      </td>
      <td>Para cada solicitação de acesso que você deseja ignorar, clique em <b>Adicionar item</b> e insira a ID da solicitação.</td> 
    </tr>
  </tbody>
</table>

#### Obter todos os membros e suas funções para um recurso (V2)

Este módulo lista todos os usuários, grupos e equipes que têm uma relação de compartilhamento explícita no recurso. As credenciais usadas na conexão para este módulo devem ter a permissão Gerenciar no recurso.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de recurso]</p>
      </td>
      <td>Selecione o tipo de recurso para o qual deseja recuperar informações.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Recurso]</p>
      </td>
      <td>Insira ou mapeie a ID do recurso para o qual deseja recuperar informações.</td> 
    </tr>
  </tbody>
</table>

#### Obter as permissões efetivas do usuário atual em um recurso (V2)

Este módulo retorna a visualização, edição, exclusão e adição de permissões do usuário atual para um determinado recurso.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de recurso]</p>
      </td>
      <td>Selecione o tipo de recurso para o qual deseja recuperar permissões.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Recurso]</p>
      </td>
      <td>Insira ou mapeie a ID do recurso para o qual deseja recuperar permissões.</td> 
    </tr>
  </tbody>
</table>

#### Listar solicitações de acesso pendentes para um recurso (V2)

Este módulo retorna todas as solicitações de acesso pendentes para o recurso fornecido.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de recurso]</p>
      </td>
      <td>Selecione o tipo de recurso para o qual deseja recuperar informações.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Recurso]</p>
      </td>
      <td>Insira ou mapeie a ID do recurso para o qual deseja recuperar informações.</td> 
    </tr>
  </tbody>
</table>

#### Solicitar acesso a um recurso (V2)

Este módulo cria ou atualiza uma solicitação de acesso para o usuário atual no recurso fornecido.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo de recurso]</p>
      </td>
      <td>Selecione o tipo de recurso para o qual deseja criar ou atualizar uma solicitação de acesso.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Recurso]</p>
      </td>
      <td>Insira ou mapeie a ID do recurso para o qual você deseja criar ou atualizar uma solicitação de acesso.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mensagem]</p>
      </td>
      <td>Insira ou mapeie o texto de uma mensagem que você deseja incluir na solicitação de acesso.</td> 
    </tr>
  </tbody>
</table>



### Outro (V2)

* [Obter ID de autenticação da Workfront ID](#get-auth-id-from-workfront-id-v2)
* [Fazer uma chamada de API personalizada](#make-a-custom-api-call-v2)
* [Monitorar eventos](#watch-events-v2)

#### Obter ID de autenticação da Workfront ID (V2)

Esse módulo pega uma ID de usuário do Workfront e retorna a ID de autorização correspondente que o Planning usa.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Usuário do Workfront]</p>
      </td>
      <td>Insira ou mapeie a Workfront ID do usuário para o qual você deseja recuperar uma ID de autorização.</td> 
    </tr>
  </tbody>
</table>

#### Fazer uma chamada de API personalizada (V2)&lt;table

Este módulo faz uma chamada personalizada para a API do Workfront Planning.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Insira um caminho relativo a <code> https://&lt;WORKFRONT_DOMAIN>/maestro/api/.</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Selecione a versão da API do Workfront que você deseja que o módulo use.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP no Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Isso determina o tipo de conteúdo da solicitação.</p> <p>Por exemplo,<code> {"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta para a chamada de API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> <p>Dica: é recomendável enviar informações por meio do corpo do JSON, em vez de como parâmetros de consulta.</p> </td> 
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

#### Eventos De Observação (V2)

Este módulo de acionamento inicia um cenário quando um registro, tipo de registro ou espaço de trabalho é criado, atualizado ou excluído no Workfront Planning.

>[!IMPORTANT]
>
>Você pode editar esse módulo posteriormente, o que editará o webhook.
>
>Considere o seguinte ao atualizar um webhook:
>
>* O webhook editado é tratado pelas assinaturas de evento do Workfront como uma nova assinatura. O histórico de assinaturas do evento não é preservado para a configuração de webhook anterior, pois essa é considerada uma assinatura de evento separada.
>* A alternância da assinatura de evento antiga para a nova pode não estar perfeitamente sincronizada. Portanto, é possível receber um evento duas vezes (se a nova assinatura começar a ser executada antes da antiga) ou perder um evento (se a assinatura antiga for interrompida antes da nova começar a ser executada).
>
>Para obter mais informações sobre edição de webhooks, consulte [Editar webhooks](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Selecione o webhook que deseja usar ou clique em Adicionar para criar um novo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>Selecione se deseja observar registros, tipos de registro ou espaços de trabalho.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objetos a serem observados]</td>
      <td>Selecione se deseja observar novos registros, registros atualizados, registros novos e atualizados ou registros excluídos.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de configuração]</td>
      <td>Selecione se deseja configuração simples ou avançada. <p>Para obter mais informações sobre configuração avançada, consulte <a href="#example-of-advanced-logic-in-the-watch-events-module" class="MCXref xref" >Exemplo de lógica avançada no módulo Eventos observados</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Selecione se deseja monitorar o estado antigo ou novo.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Acione um cenário quando o registro é alterado <b>para</b> um valor específico.</p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Acione um cenário quando o registro é alterado <b>de</b> um valor específico.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Espaço de trabalho]</td>
      <td>Se estiver observando registros, selecione o Workspace que deseja observar para os registros.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Se estiver observando registros, selecione o tipo de registro que deseja observar.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>É possível definir filtros para monitorar apenas os registros que atendem aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que você deseja que o filtro avalie, bem como o operador e o valor que deseja que o filtro permita. Você pode usar mais de um filtro adicionando regras AND.</p> <p>Observação: não é possível editar filtros em webhooks existentes do Workfront. Para configurar filtros diferentes para assinaturas de eventos do Workfront, remova o webhook atual e crie um novo.</p> <p>Para obter mais informações sobre filtros de evento, consulte <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtros de assinatura de evento no Workfront &gt; [!UICONTROL Watch Events] módulos</a> no artigo sobre módulos do Workfront.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objetos a serem observados]</td>
      <td>Selecione se você deseja observar novos. registros atualizados, novos e atualizados ou excluídos.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Excluir atualizações feitas por esta conexão]</p>
      </td>
      <td>Habilite esta opção para impedir que o cenário seja acionado quando uma alteração for feita pela conexão usada por este módulo. Isso impede que outra instância do cenário seja acionada se esse cenário executar uma ação de acionamento.</td> 
    </tr>
  </tbody>
</table>

Para obter um exemplo de uso da lógica avançada neste módulo, consulte [Exemplo de lógica avançada no módulo Eventos observados](#example-of-advanced-logic-in-the-watch-events-module).






## Módulos da versão 1 do [!DNL Adobe Workfront Planning] e seus campos

>[!IMPORTANT]
>
>Os módulos desta seção pertencem ao conector do Workfront Planning V1.Para módulos no conector do Workfront Planning V2, consulte [[!DNL Adobe Workfront Planning] Módulos da versão 2 e seus campos](#adobe-workfront-planning-version-2-modules-and-their-fields).

Ao configurar módulos do Workfront Planning, o Workfront Fusion exibe os campos listados abaixo. Junto com esses campos, podem ser exibidos campos adicionais do Workfront, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)
* [Sem categoria](#uncategorized)

### Acionadores

#### Monitorar eventos

Este módulo de acionamento inicia um cenário quando um registro, tipo de registro ou espaço de trabalho é criado, atualizado ou excluído no Workfront Planning.

>[!IMPORTANT]
>
>Você pode editar esse módulo posteriormente, o que editará o webhook.
>
>Considere o seguinte ao atualizar um webhook:
>
>* O webhook editado é tratado pelas assinaturas de evento do Workfront como uma nova assinatura. O histórico de assinaturas do evento não é preservado para a configuração de webhook anterior, pois essa é considerada uma assinatura de evento separada.
>* A alternância da assinatura de evento antiga para a nova pode não estar perfeitamente sincronizada. Portanto, é possível receber um evento duas vezes (se a nova assinatura começar a ser executada antes da antiga) ou perder um evento (se a assinatura antiga for interrompida antes da nova começar a ser executada).
>
>Para obter mais informações sobre edição de webhooks, consulte [Editar webhooks](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Selecione o webhook que deseja usar ou clique em Adicionar para criar um novo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>Selecione se deseja observar registros, tipos de registro ou espaços de trabalho.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Selecione se deseja monitorar o estado antigo ou novo.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Acione um cenário quando o registro é alterado <b>para</b> um valor específico.</p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Acione um cenário quando o registro é alterado <b>de</b> um valor específico.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Espaço de trabalho]</td>
      <td>Se estiver observando registros, selecione o Workspace que deseja observar para os registros.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Se estiver observando registros, selecione o tipo de registro que deseja observar.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>É possível definir filtros para monitorar apenas os registros que atendem aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que você deseja que o filtro avalie, bem como o operador e o valor que deseja que o filtro permita. Você pode usar mais de um filtro adicionando regras AND.</p> <p>Observação: não é possível editar filtros em webhooks existentes do Workfront. Para configurar filtros diferentes para assinaturas de eventos do Workfront, remova o webhook atual e crie um novo.</p> <p>Para obter mais informações sobre filtros de evento, consulte <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtros de assinatura de evento no Workfront &gt; [!UICONTROL Watch Events] módulos</a> no artigo sobre módulos do Workfront.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objetos a serem observados]</td>
      <td>Selecione se você deseja observar novos. registros atualizados, novos e atualizados ou excluídos.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Excluir atualizações feitas por esta conexão]</p>
      </td>
      <td>Habilite esta opção para impedir que o cenário seja acionado quando uma alteração for feita pela conexão usada por este módulo. Isso impede que outra instância do cenário seja acionada se esse cenário executar uma ação de acionamento.</td> 
    </tr>
  </tbody>
</table>

Para obter um exemplo de uso da lógica avançada neste módulo, consulte [Exemplo de lógica avançada no módulo Eventos observados](#example-of-advanced-logic-in-the-watch-events-module).

### Ações

* [Excluir um tipo de registro](#delete-a-record-type)
* [Fazer uma chamada de IA personalizada](#make-a-custom-api-call)

#### Excluir um tipo de registro

Este módulo de ação exclui um único tipo de registro no Workfront Planning por sua ID.

>[!WARNING]
>
>A exclusão de um tipo de registro no Workfront Planning também exclui todos os registros na tabela de tipo de registro.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de tipo de registro]</p>
      </td>
      <td>Informe ou mapeie a ID do tipo de registro que deseja deletar.</td> 
    </tr>
  </tbody>
</table>

#### Fazer uma chamada de API personalizada

Este módulo faz uma chamada de API personalizada para a API [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Insira um caminho relativo a <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Para cada par de chave/valor que você deseja adicionar à sequência de consulta, clique em <b>Adicionar item</b> e insira a chave e o valor.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>


### Pesquisas

#### Pesquisar registros

Este módulo de ação recupera uma lista de registros com base nos critérios que você especificar.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de trabalho]</p>
      </td>
      <td>Insira ou mapeie a Workspace que contém os registros que você deseja pesquisar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecione o tipo de registro que deseja pesquisar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Campos de Registro]</p>
      </td>
      <td>Para cada campo que deseja usar na pesquisa, localize esse campo, selecione o operador e insira ou mapeie o valor que deseja pesquisar. Os campos estão disponíveis com base no tipo de registro selecionado.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Condição para filtros]</p>
      </td>
      <td>Selecione a condição para seus filtros:<ul><li><b>E</b><p>O módulo retorna registros que correspondem a <b>todos</b> dos valores de campo selecionados.</p></li><li><b>OR</b><p>O módulo retorna registros que correspondem a <b>qualquer</b> dos valores de campo selecionados.</p></li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Limit]</p>
      </td>
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
    </tr>
  </tbody>
</table>


### Sem categoria


#### Criar um registro

Essa ação cria um único registro no Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de tipo de registro]</p>
      </td>
      <td>Insira ou mapeie o tipo de registro que deseja criar. Os tipos de registro disponíveis baseiam-se na sua conta do Workfront Planning.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Outros campos</p>
      </td>
      <td>Insira os valores que você deseja que o novo registro tenha. Esses campos se baseiam no tipo de registro selecionado.</td> 
    </tr>
    <tr>
  </tbody>
</table>

### Excluir um registro

Este módulo de ação exclui o registro especificado no Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Registro]</p>
      </td>
      <td>Informe ou mapeie a ID do registro que deseja deletar.</td> 
    </tr>
  </tbody>
</table>

### Obter um registro

Este módulo de ação recupera um único registro de [!DNL Adobe Workfront Planning], especificado por sua ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Registro]</td>
      <td>Insira ou mapeie a ID do registro que deseja recuperar.</td>
    </tr>
  </tbody>
</table>

### Obter registros por tipo de registro

Este módulo de ação recupera todos os registros do tipo especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Espaço de trabalho]</td>
      <td>Selecione ou mapeie o espaço de trabalho que contém os registros que deseja recuperar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Selecione o tipo de registro que deseja recuperar.</td>
    </tr>
    <!--
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
    -->
  </tbody>
</table>

### Obter tipos de registro

Este módulo de ação recupera uma lista de tipos de registros em uma conta [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Espaço de trabalho]</td>
      <td>Selecione ou mapeie o espaço de trabalho que contém os tipos de registro que deseja recuperar.</td>
    </tr>
  </tbody>
</table>

### Atualizar registro

Essa ação atualiza um único registro no Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Workfront Planning], consulte <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Workfront Planning]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de Registro]</p>
      </td>
      <td>Insira ou mapeie o tipo de registro que deseja atualizar. Os tipos de registro disponíveis baseiam-se na sua conta do Workfront Planning.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Outros campos</p>
      </td>
      <td>Informe os novos valores que deseja que o registro tenha. Esses campos se baseiam no tipo de registro selecionado.</td> 
    </tr>
    <tr>
  </tbody>
</table>


## Usar JSONata para o detalhamento `record-types` legível

A expressão JSONata a seguir cria uma saída legível da consulta do Planning que fornece o detalhamento dos tipos de registro. Isso torna o nome do tipo de registro, os nomes dos campos e os nomes das opções de campo (quando aplicável) legíveis por um nome e mantém o restante da estrutura intacta.

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

Para obter informações sobre o uso de módulos JSONata, consulte [módulos JSONata](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md).

## Exemplo de lógica avançada no módulo Eventos observados

Este é um exemplo do formato usado pela lógica avançada ao usar o módulo Workfront Planning > Eventos de observação.

```
[
  {
    "fieldName": "recordTypeId",
    "fieldValue": "Rt68c886502d4b5554ee80896b",
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "planning"
    },
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "active"
    },
    "comparison": "eq",
    "state": "newState"
  }
]
```

Considere o seguinte ao usar a lógica avançada no módulo Evento de observação:

* A primeira entrada `"fieldvalue":` é a ID de Tipo de Registro de Planejamento extraída da URL. Neste exemplo, a ID do Tipo de Registro de Planejamento é `Rt68c886502d4b5554ee80896b`.
* Os dados de planejamento são retornados dentro de uma matriz chamada `data `, que aparece neste exemplo como `"fieldName": "data"`.
* FieldNames do Planning são retornados como IDs que começam com `F`.
* Como este exemplo está avaliando em relação a um conector de filtro `OR`, ele tem duas entradas para o mesmo campo (`F68c886502d4b5554eec808975`).  As duas opções suspensas que o módulo está filtrando são `"planning"` e `"active"`.

