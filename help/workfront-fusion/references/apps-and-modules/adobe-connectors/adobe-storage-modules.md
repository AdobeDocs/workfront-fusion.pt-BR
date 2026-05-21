---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Módulos do Adobe Storage
description: Em um cenário do Adobe Workfront Fusion, é necessário criar e gerenciar projetos no Adobe Admin Console.
author: Becky
feature: Workfront Fusion
exl-id: 78ee905f-4713-44a4-bffb-c64cdb3665c2
TQID: https://experienceleague.adobe.com/sp6gMeEhVxN0QjviLXm9GnI7NSLEp93PnSQkH45zHXI
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1413
ht-degree: 28%

---

# Módulos do Adobe Storage

Em um cenário do Adobe Workfront Fusion, é possível criar e gerenciar projetos no Adobe Admin Console.

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Criar uma conexão com o Adobe Storage

A criação de uma conexão com o Adobe Storage requer alguma configuração no Adobe Developer Console, bem como no Fusion.

### Configurar o projeto no Adobe Developer Console

Você deve adicionar a API ao seu projeto na Adobe Developer Console.

1. Abra o projeto na Adobe Developer Console.
1. Clique em **Adicionar ao projeto** e selecione **API**.
1. Na lista de APIs disponíveis, selecione **Adobe Cloud Platform e Collaboration API**.
1. Na tela Selecionar tipo de autenticação, selecione **Servidor a Servidor OAuth** e clique em **Avançar**.
1. Adicione um nome para a credencial.
1. Clique em **Avançar** e em **Salvar API configurada**.
1. Anote as credenciais fornecidas, que você usará ao configurar a conexão no Workfront Fusion.
1. Prossiga para [Torne sua conta técnica um administrador na Adobe Admin Console](#make-your-technical-account-an-admin-in-the-adobe-admin-console).

### Torne sua conta técnica um administrador no Adobe Admin Console

Na página do Adobe Admin Console, selecione a guia Produtos na barra de navegação superior e, em seguida, selecione Workfront Fusion

1. Localize e copie o endereço de email do usuário da conta técnica em sua organização.
1. Se uma lista for exibida, selecione o link na parte superior.
1. Esta é a sua instância de produção, onde seus usuários trabalham.
1. Na lista exibida, com a guia Perfis de produto selecionada, clique no nome do link Perfil de produto do Workfront.

   Esta lista inclui todos os usuários que já estão atribuídos à sua instância de produção do Workfront.

1. Selecione a aba **Administradores** acima da lista de usuários.
1. Selecione **Adicionar administrador**.
1. Na caixa Adicionar administradores de perfil de produto, digite os endereços de email da conta técnica e selecione **Salvar**.

   A conta técnica passa a ser de administrador.

1. Continue em [Criar a conexão no Workfront Fusion](#create-the-connection-in-workfront-fusion).

### Criar a conexão no Workfront Fusion

Para criar uma conexão para os módulos do [!DNL Adobe Storage]:

1. Em qualquer módulo, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>Selecione <code>Server to server</code>.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Insira um nome para essa conexão.</p>
        </td>
        </tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira sua [!UICONTROL Adobe] [!UICONTROL ID do cliente]. Isso pode ser encontrado na seção [!UICONTROL Credential details] do projeto no [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira o [!UICONTROL Client Secret] do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credential details] do projeto no [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organization ID]</td>
        <td>Insira ou mapeie sua ID da organização do Adobe IMS. Esta é uma cadeia de caracteres com o formato <code> 123abc@AdobeOrg</code>, em que a seção antes de @ é um número hexadecimal. Você pode encontrar esse valor como parte do caminho de URL da sua organização no Adobe Admin Console ou no console Adobe.IO da sua integração de gerenciamento de usuários.</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## Módulos de armazenamento da Adobe e seus campos

Ao configurar os módulos de Gerenciamento de Usuários do Adobe, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Gerenciamento de usuários da Adobe podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Lojas ESM](#esm-stores)
* [Convites](#invitations)
* [Outras](#other)

### Lojas ESM

* [Criar um armazenamento ESM](#create-an-esm-store)
* [Excluir um armazenamento ESM](#delete-an-esm-store)
* [Descartar um armazenamento ESM](#discard-an-esm-store)
* [Restaurar um armazenamento ESM](#restore-an-esm-store)

#### Criar um armazenamento ESM

Esse módulo de ação configura um novo armazenamento ESM (Enterprise Storage Management, gerenciamento de armazenamento corporativo) para organizar e gerenciar ativos essenciais aos negócios.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Storage, consulte <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Criar uma conexão com o Adobe Storage</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do projeto</td> 
   <td>Insira ou mapeie um nome para o novo projeto.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um armazenamento ESM

Esse módulo de ação remove permanentemente um armazenamento ESM existente e todos os seus dados associados. Esta ação não pode ser desfeita.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Storage, consulte <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Criar uma conexão com o Adobe Storage</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da loja</td> 
   <td>Insira ou mapeie a ID do armazenamento que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Descartar um armazenamento ESM

Esse módulo de ação marca um armazenamento EMS para exclusão, permitindo um período de carência antes da remoção permanente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Storage, consulte <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Criar uma conexão com o Adobe Storage</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da loja</td> 
   <td>Insira ou mapeie a ID do armazenamento que deseja descartar.</td> 
  </tr> 
 </tbody> 
</table>

#### Restaurar um armazenamento ESM

Esse módulo de ação recupera um armazenamento ESM excluído anteriormente e restaura o acesso a seus dados e configurações.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Storage, consulte <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Criar uma conexão com o Adobe Storage</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da loja</td> 
   <td>Insira ou mapeie a ID do armazenamento que você deseja restaurar.</td> 
  </tr> 
 </tbody> 
</table>

### Convites

#### Convidar usuário

Esse módulo de ação envia um convite para conceder a um novo usuário acesso a um armazenamento ESM específico, permitindo a colaboração e o gerenciamento de arquivos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Storage, consulte <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Criar uma conexão com o Adobe Storage</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Endereço de email</td> 
   <td>Insira ou mapeie o endereço de email do usuário que você deseja convidar para a loja.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do ativo</td> 
   <td>Insira ou mapeie a ID do ativo para o qual você deseja convidar o usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Função</td> 
   <td>Selecione a função que você deseja que o usuário recém-convidado tenha para o ativo.<ul><li>Proprietário</li><li>Editor</li><li>Visualizador</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">É possível comentar</td> 
   <td>Ative essa opção para permitir que o usuário comente no ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pode compartilhar</td> 
   <td>Habilite essa opção para permitir que o usuário compartilhe o ativo com outro usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aceitação necessária</td> 
   <td>Habilite essa opção para garantir que o usuário aceite o convite antes de colaborar no ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usar montagens</td> 
   <td>Habilite esta opção se for necessário criar um ponto de montagem para o convite. A opção Acceptance required deve estar ativada para ativar essa opção.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de notificação</td> 
   <td>Insira ou mapeie o tipo de notificação do Adobe que deseja usar para notificar o usuário sobre o convite. Se isso for deixado em branco, o tipo de notificação será baseado no tipo MIME do ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do modelo</td> 
   <td>Insira ou mapeie a ID de correio da Adobe do modelo que você deseja usar para o email de convite.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Localidade</td> 
   <td>Insira o local do usuário na forma de um código de idioma e código de país. <p>Exemplo: <code>en-us</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Externo</td> 
   <td>Defina essa opção como true se desejar enviar notificações usando um sistema externo ao Serviço de Convites da Adobe. A notificação externa é suportada somente quando a aceitação não é necessária.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de ativo</td> 
   <td>Insira ou mapeie o tipo de ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mensagem</td> 
   <td>Insira ou mapeie uma mensagem para incluir no email de convite.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL de direcionamento</td> 
   <td>Insira ou mapeie o URL que o convidado pode usar para exibir o ativo.</td> 
  </tr> 
 </tbody> 
</table>

### Outras

#### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma solicitação HTTP personalizada para a API de armazenamento do Adobe.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Storage, consulte <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Criar uma conexão com o Adobe Storage</a> neste artigo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Insira um caminho relativo a <code>https://ccprojects.adobe.io/api/v3/.</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Método</p>
      </td>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Cabeçalhos</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização e cabeçalhos x-api-key automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">String de consulta  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Corpo</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
