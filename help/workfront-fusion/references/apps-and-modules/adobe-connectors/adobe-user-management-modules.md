---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Módulos de gerenciamento de usuários do Adobe
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que gerenciam usuários em sua conta do Adobe.
author: Becky
feature: Workfront Fusion
exl-id: e8fe8ec4-4b00-4c9a-81a5-acb2039b153b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2417'
ht-degree: 2%

---

# Módulos de gerenciamento de usuários do Adobe

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que gerenciam usuários em sua conta do Adobe.

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
   <td role="rowheader">plano do Adobe Workfront*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença da Adobe Workfront*</td>
   <td> <p>[!UICONTROL Plano], [!UICONTROL Trabalho]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Requisito de licença herdado: [!UICONTROL Workfront Fusion para Automação e Integração do Trabalho], [!UICONTROL Workfront Fusion para Automação do Trabalho]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o plano do [!UICONTROL Select] ou do [!UICONTROL Prime] para Adobe Workfront, sua organização deve comprar o Adobe Workfront Fusion e o Adobe Workfront para usar a funcionalidade descrita neste artigo. O Workfront Fusion está incluído no plano do Workfront da [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o Adobe Workfront Fusion e o Adobe Workfront para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para descobrir seu plano, tipo de licença ou acesso, entre em contato com o administrador do Workfront.

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Criar uma conexão com o Gerenciamento de usuários do Adobe

Para criar uma conexão para seus módulos do [!DNL Adobe User Management]:

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
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organization ID]</td>
        <td>Insira suas credenciais do IMS do [!DNL Adobe]. O identificador exclusivo de uma organização. Esta é uma cadeia de caracteres no formato A495E53@AdobeOrg em que o prefixo antes de @ é um número hexadecimal. Você pode encontrar esse valor como parte do caminho de URL da organização na Admin Console ou no console adobe.io para a sua integração com o Gerenciamento de usuários.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Escopos adicionais]</td>
        <td>Para cada escopo adicional que você deseja adicionar, clique em <b>Adicionar item</b> e insira o escopo.</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.



## Módulos de gerenciamento de usuários do Adobe e seus campos

Ao configurar os módulos de Gerenciamento de Usuários do Adobe, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Gerenciamento de usuários da Adobe podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Pesquisas](#searches)
* [Ações do usuário](#user-actions)
* [Ações do grupo de usuários](#user-group-actions)
* [Outras](#other)

### Pesquisas

* [Obter grupos de usuários e perfis de produtos](#get-user-groups-and-product-profiles)
* [Obter informações do usuário](#get-user-information)
* [Colocar usuários em um grupo de usuários ou perfil de produto](#get-users-in-a-user-group-or-product-profile)
* [Obter usuários em uma organização](#get-users-in-an-organization)

#### Obter grupos de usuários e perfis de produtos

Este módulo de pesquisa recupera uma lista de todos os grupos de usuários e perfis de produtos em sua organização, juntamente com detalhes sobre os grupos e perfis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### Obter informações do usuário

Este módulo de pesquisa recupera detalhes de um único usuário na organização, identificado por seu endereço de email.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Endereço de email</td> 
   <td>Insira ou mapeie o endereço de email do usuário para o qual deseja retornar detalhes. Para AdobeID, Enterprise e usuários federados por email, esse deve ser o endereço de email completo, incluindo o domínio. Em todos os casos, o parâmetro não diferencia maiúsculas de minúsculas.</td> 
  </tr> 
 </tbody> 
</table>

#### Colocar usuários em um grupo de usuários ou perfil de produto

Este módulo de pesquisa recupera uma lista de todos os usuários no grupo de usuários ou perfil de produto especificado, juntamente com detalhes sobre os usuários.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do grupo</td> 
   <td>O grupo de usuários, o nome do perfil do produto ou um grupo administrativo. Para um grupo de administradores, o nome pode ser um dos grupos fixos <code>_org_admin</code>, <code>_deployment_admin</code> ou <code>_support_admin</code>; ou um grupo de administradores específico do grupo. Eles são identificados com um prefixo no nome do grupo, como <code>_admin_groupName</code>, <code>_product_admin_productName</code> ou <code>_developer_groupName</code>. Se o grupo existir, mas o grupo de administradores não, uma lista vazia é retornada.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Somente direto</td> 
   <td>Especifique se o campo de grupos na estrutura de usuário retornada contém somente os perfis de produto dos quais esse usuário é membro direto. Se falso, retorna todos os grupos (grupos de usuários, perfis de produtos e grupos de administradores) que contêm o usuário, independentemente de um direito a um perfil de produto específico vir diretamente (por meio da atribuição de usuário) ou indiretamente (por meio de um grupo de usuários que contém o usuário que está sendo atribuído ao perfil do produto). Se verdadeiro, retorna todos os grupos de usuários e grupos de administradores que contêm o usuário, mas somente os perfis de produtos para os quais o usuário recebeu um direito explicitamente. Um usuário pode ser um membro direto e indireto de um perfil de produto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Excluir grupos</td> 
   <td>Especifique se a resposta exclui a matriz de grupos de ser retornada para cada usuário individual.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Status</td> 
   <td>Essa opção se aplica somente aos perfis de produtos. Selecione Ativo para listar os usuários que foram provisionados para o produto e que têm uma licença ativa. Selecione Inativo para listar os usuários que foram adicionados ao perfil do produto, mas não têm uma licença ativa. Se deixado em branco, o módulo retornará todos os usuários membros independentemente de seus status de direito.
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### Obter usuários em uma organização

Este módulo de pesquisa retorna todos os usuários da organização associados à conexão.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

### Ações do usuário

* [Adicionar um usuário como membro de um grupo](#add-a-user-as-a-member-of-a-group)
* [Criar um usuário](#create-a-user)
* [Remover um usuário dos grupos](#remove-a-user-from-groups)
* [Atualizar um usuário](#update-a-user)

#### Adicionar um usuário como membro de um grupo

Este módulo de ação adiciona um usuário como membro do(s) grupo(s) especificado(s). Esse módulo pode adicionar o usuário a até quatro grupos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usuário</td> 
   <td>Insira ou mapeie o usuário que deseja adicionar aos grupos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domínio</td> 
   <td>Para Federated IDs que não são endereços de email, insira o domínio ao qual o usuário pertence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Grupos</td> 
   <td>Para cada grupo ao qual você deseja adicionar o usuário, clique em <b>Adicionar item</b> e insira ou mapeie o grupo. Você pode inserir até quatro grupos e deve inserir pelo menos um.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usar o Adobe ID</td> 
   <td>Selecione verdadeiro para garantir que a ID do usuário seja interpretada como uma referência a uma Adobe ID existente, mesmo se uma Enterprise ou Federated ID existir com o mesmo nome.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar um usuário

Esse módulo de ação cria um novo usuário na organização.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de ID</td> 
   <td>Selecione se deseja criar um usuário com uma Adobe ID, Enterprise ID ou Federated ID. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Logon</td> 
   <td>Se você estiver criando um usuário com uma Federated ID, selecione o tipo de logon.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Email</td> 
   <td>Insira ou mapeie o endereço de email do novo usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domínio</td> 
   <td>Se você estiver criando um usuário com uma Federated ID com um logon baseado em domínio, insira ou mapeie o domínio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usuário</td> 
   <td>Se você estiver criando um usuário com uma Federated ID com um logon baseado em domínio, insira ou mapeie o usuário que este novo usuário representará.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Insira ou mapeie o nome do usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sobrenome</td> 
   <td>Insira ou mapeie o sobrenome do usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">País</td> 
   <td>Insira ou mapeie o código ISO de país com dois caracteres. Isso não pode ser alterado após a criação do usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Opção</td> 
   <td>Selecione a ação a ser tomada se o usuário já existir na organização. Se nenhuma opção estiver selecionada e o usuário já existir, o módulo retornará um erro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usar o Adobe ID</td> 
   <td>Quando verdadeiro, a ID de usuário é interpretada como referindo-se a uma Adobe ID existente, mesmo se uma Enterprise ou Federated ID existir com o mesmo nome.</td> 
  </tr> 
 </tbody> 
</table>

#### Remover um usuário dos grupos

Este módulo de ação remove a associação de um usuário dos grupos especificados. Você pode remover um usuário de até quatro grupos por vez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usuário</td> 
   <td>Insira ou mapeie o usuário que deseja remover dos grupos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domínio</td> 
   <td>Para Federated IDs que não são endereços de email, insira o domínio ao qual o usuário pertence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Grupos</td> 
   <td>Para cada grupo do qual você deseja remover o usuário, clique em <b>Adicionar item</b> e insira ou mapeie o grupo. Você pode inserir até quatro grupos e deve inserir pelo menos um.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usar o Adobe ID</td> 
   <td>Selecione verdadeiro para garantir que a ID do usuário seja interpretada como uma referência a uma Adobe ID existente, mesmo se uma Enterprise ou Federated ID existir com o mesmo nome.</td> 
  </tr> 
 </tbody> 
</table>



#### Atualizar um usuário

Este módulo de ação atualiza um usuário existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usuário</td> 
   <td>Insira ou mapeie a ID do usuário que você deseja atualizar. Esse é o endereço de email do usuário, como <code>user@example.com</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domínio</td> 
   <td>Se estiver atualizando um usuário com uma Federated ID que não seja um endereço de email, insira ou mapeie o domínio ao qual o usuário pertence para identificá-lo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Email</td> 
   <td>Insira ou mapeie o novo endereço de email do usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Insira ou mapeie o nome do usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sobrenome</td> 
   <td>Insira ou mapeie o sobrenome do usuário.</td> 
  </tr> 
 </tbody> 
</table>

### Ações do grupo de usuários

* [Adicionar associações a um grupo de usuários](#add-memberships-for-a-user-group)
* [Criar um grupo de usuários](#create-a-user-group)
* [Excluir um grupo de usuários](#delete-a-user-group)
* [Remover associações de um grupo de usuários](#remove-memberships-for-a-user-group)
* [Atualizar um grupo de usuários](#update-a-user-group)

#### Adicionar associações a um grupo de usuários

Este módulo de ação adiciona usuários e perfis de produto a um grupo de usuários. Os usuários adicionados ao grupo de usuários obtêm direito a todos os perfis de produtos no grupo de usuários. Adicionar um perfil de produto dá direito a esse perfil para usuários no grupo de usuários.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do grupo</td> 
   <td>Insira ou mapeie o nome do grupo do qual deseja remover os usuários ou perfis.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usuários</td> 
   <td>Para cada usuário que você deseja adicionar, clique em <b>Adicionar usuário</b> e insira o endereço de email do usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Perfis</td> 
   <td>Para cada perfil que você deseja adicionar ao grupo, clique em <b>Adicionar usuário</b> e insira o nome do perfil</td> 
  </tr> 
 </tbody> 
</table>

#### Criar um grupo de usuários

Este módulo de ação cria um novo grupo de usuários. Se um grupo já existir com o nome fornecido, o módulo poderá atualizar o grupo existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do grupo</td> 
   <td>Insira ou mapeie um nome para o novo grupo de usuários.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Descrição</td> 
   <td>Insira ou mapeie uma descrição para o novo grupo de usuários.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Opção</td> 
   <td>Selecione a ação a ser tomada se o grupo de usuários já existir na organização. Se nenhuma opção estiver selecionada e o grupo de usuários já existir, o módulo retornará um erro.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um grupo de usuários

Este módulo de ação exclui um grupo de usuários existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do grupo</td> 
   <td>Informe ou mapeie o nome do grupo que deseja deletar.</td> 
  </tr> 
 </tbody> 
</table>

#### Remover associações de um grupo de usuários

Este módulo de ação remove usuários ou perfis de um grupo de usuários.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do grupo</td> 
   <td>Insira ou mapeie o nome do grupo do qual deseja remover os usuários ou perfis.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usuários</td> 
   <td>Para cada usuário que você deseja remover, clique em <b>Adicionar usuário</b> e insira o endereço de email do usuário.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Perfis</td> 
   <td>Para cada perfil que você deseja remover do grupo, clique em <b>Adicionar usuário</b> e digite o nome do perfil</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usar o Adobe ID</td> 
   <td>Quando verdadeiro, a ID de usuário é interpretada como referindo-se a uma Adobe ID existente, mesmo se uma Enterprise ou Federated ID existir com o mesmo nome.</td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um grupo de usuários

Este módulo de ação atualiza um grupo de usuários existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do grupo original</td> 
   <td>Informe ou mapeie o nome atual do grupo que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do novo grupo</td> 
   <td>Insira ou mapeie o novo nome que você deseja que o grupo tenha.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do grupo original</td> 
   <td>Insira ou mapeie a descrição atualizada do grupo.</td> 
  </tr> 
 </tbody> 
 </table>

### Outras


#### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada personalizada para a API de gerenciamento de usuários do Adobe.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com o Gerenciamento de usuários do Adobe, consulte <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Criar uma conexão com o Gerenciamento de usuários do Adobe</a> neste artigo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Insira um caminho relativo a <code>https://usermanagement.adobe.io/v2/usermanagement/</code></p>
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
      <td role="rowheader">Sequência de consulta  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Corpo</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
