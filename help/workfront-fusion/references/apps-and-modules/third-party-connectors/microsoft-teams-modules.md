---
title: Módulos do Microsoft Teams
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o Teams, bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
source-git-commit: f5b49cca308fad01167aed27e4716a3d630cb026
workflow-type: tm+mt
source-wordcount: '3642'
ht-degree: 2%

---

# Módulos do Microsoft Teams

<!-- ADD REDIRECTS -->

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Microsoft Teams, bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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
   <p>Novo:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
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

Para usar os módulos do Microsoft Teams, você deve ter uma conta do Microsoft Teams capaz de executar a ação no módulo.

## Conectar o serviço Microsoft Teams ao Workfront Fusion

Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte [Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alguns aplicativos do Microsoft usam a mesma conexão, que está vinculada a permissões de usuário individuais. Portanto, ao criar uma conexão, a tela de consentimento de permissões exibe todas as permissões que foram concedidas anteriormente à conexão deste usuário, além de todas as novas permissões necessárias para o aplicativo atual.
>
>Por exemplo, se um usuário tiver permissões de &quot;Tabela de leitura&quot; concedidas por meio do conector do Excel e criar uma conexão no conector do Outlook para ler emails, a tela de consentimento de permissões mostrará a permissão &quot;Tabela de leitura&quot; já concedida e a permissão &quot;Gravar email&quot; recém-necessária.

## Módulos do Microsoft Teams e seus campos

Ao configurar módulos do Microsoft Teams, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Microsoft Teams podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Equipe](#team)
* [Canal](#channel)
* [Mensagem](#message)
* [Membro](#member)
* [Reunião online](#online-meeting)
* [Outro](#other)

### Equipe

* [Criar uma equipe de um grupo](#create-a-team-from-a-group)
* [Criar um grupo do Office 365](#create-an-office-365-group)
* [Excluir uma equipe ou grupo](#delete-a-team-or-group)
* [Obter uma equipe](#get-a-team)
* [Listar todas as equipes e grupos](#list-all-teams-and-groups)
* [Listar equipes participantes](#list-joined-teams)
* [Atualizar uma equipe](#update-a-team)
* [Assista às equipes](#watch-teams)

#### Criar uma equipe de um grupo

Este módulo de ação cria uma equipe de um grupo existente do Microsoft Office 365 e define as configurações da nova equipe.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de Grupo</td> 
   <td> <p>Selecione o grupo do qual deseja criar uma equipe.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Permitir que membros criem e atualizem canais</td> 
   <td>Selecione se deseja permitir que os membros criem e atualizem canais.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que membros excluam canais</td> 
   <td>Selecione se você deseja permitir que membros excluam canais.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que membros adicionem e removam aplicativos</td> 
   <td>Selecione se você deseja permitir que membros adicionem e removam aplicativos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que membros criem, atualizem e removam guias</td> 
   <td>Selecione se deseja permitir que os membros criem, atualizem e removam guias.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que membros criem e removam conectores</td> 
   <td>Selecione se você deseja permitir que membros criem e removam conectores.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que os usuários editem suas mensagens</td> 
   <td>Selecione se você deseja permitir que os usuários editem suas mensagens.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que usuários excluam suas mensagens</td> 
   <td>Selecione se você deseja permitir que os usuários excluam suas mensagens.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que proprietários excluam mensagens</td> 
   <td>Selecione se você deseja permitir que os proprietários excluam qualquer mensagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir menções @team</td> 
   <td>Selecione se deseja permitir menções @team.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir menções @channel</td> 
   <td>Selecione se deseja permitir menções @channel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir Giphy</td> 
   <td>Selecione se deseja permitir o uso de Giphy para esta Equipe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir adesivos e memes</td> 
   <td>Selecione se você deseja permitir que os usuários incluam adesivos e memes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir memes personalizados</td> 
   <td>Selecione se você deseja permitir que os usuários incluam memes personalizados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que os convidados criem e atualizem canais</td> 
   <td>Selecione se deseja permitir que os convidados criem e atualizem canais.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permitir que os convidados excluam canais</td> 
   <td>Selecione se deseja permitir que os convidados excluam canais.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar um grupo do Office 365

Este módulo de ação cria um grupo no Microsoft Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome de exibição</td> 
   <td> <p>Insira ou mapeie o nome que este grupo exibe em seu catálogo de endereços.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias do grupo</td> 
   <td>Insira ou mapeie o alias de email deste grupo. Você pode incluir letras minúsculas, números e sublinhados. Para o tipo de grupo do Office 365, esse será o alias do email do grupo ([Alias]@[Seu Domínio].onmicrosoft.com). Para o tipo Grupo de segurança, o alias funciona como um apelido.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de grupo</td> 
   <td>Selecione se você está criando um grupo do Office 365 ou um grupo de Segurança.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Descrição</td> 
   <td>Insira ou mapeie uma descrição para este grupo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Segurança ativada</td> 
   <td>Ative esta opção se quiser que o grupo seja ativado por segurança.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietários</td> 
   <td>Selecione os proprietários para este grupo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Membros</td> 
   <td>Selecione os membros deste grupo.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir uma Equipe ou Grupo

Este módulo de ação exclui o grupo ou grupo especificado.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de Grupo</td> 
   <td> <p>Insira ou mapeie a ID do grupo que deseja excluir.</p> 
   </tr> 
 </tbody> 
</table>

#### Obter uma equipe

Este módulo recupera propriedades e relações da equipe do Microsoft ou grupo do Office 365 especificado.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de Grupo</td> 
   <td> <p>Insira ou mapeie a ID do grupo para o qual deseja recuperar detalhes.</p> 
   </tr> 
 </tbody> 
</table>

#### Listar todas as equipes e grupos

Este módulo lista todas as equipes nos grupos do Microsoft Teams e do Office 365 associados à organização. Você pode filtrar para retornar somente resultados que atendam aos critérios especificados.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtro</td> 
   <td> <p>É possível definir um filtro para retornar somente equipes e grupos que atendam aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que deseja que o filtro avalie, o operador e o valor que deseja que o filtro permita. É possível usar mais de um filtro adicionando regras AND ou OR.</p> </td> 
   </tr> 
  <tr> 
   <td>Número máximo de resultados retornados</td> 
   <td>Defina o número máximo de equipes ou grupos que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>


#### Listar equipes unidas

Este módulo de ação lista as equipes às quais o usuário associado à conexão usada neste módulo ingressou.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>Número máximo de resultados retornados</td> 
   <td>Defina o número máximo de equipes ou grupos que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar uma equipe

Este módulo de ação atualiza as propriedades das equipes especificadas no Microsoft Teams ou no grupo do Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome de exibição</td> 
   <td> <p>Insira ou mapeie o nome que este grupo exibe em seu catálogo de endereços.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias do grupo</td> 
   <td>Insira ou mapeie o alias de email deste grupo. Você pode incluir letras minúsculas, números e sublinhados. Para o tipo de grupo do Office 365, esse será o alias do email do grupo ([Alias]@[Seu Domínio].onmicrosoft.com). Para o tipo de grupo Segurança, o alias funciona como um apelido.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Descrição</td> 
   <td>Insira ou mapeie uma descrição para este grupo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Segurança ativada</td> 
   <td>Ative esta opção se quiser que o grupo seja ativado por segurança.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Visibilidade</td> 
   <td>Especifique a visibilidade do grupo do Office 365.</td> 
  </tr> 
 </tbody> 
</table>

#### Assista às equipes

Este módulo de acionamento inicia um cenário quando um grupo é criado.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtro</td> 
   <td> <p>É possível definir um filtro para observar apenas as equipes e grupos que atendem aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que deseja que o filtro avalie, o operador e o valor que deseja que o filtro permita. É possível usar mais de um filtro adicionando regras AND ou OR.</p> </td> 
   </tr> 
  <tr> 
   <td>Número máximo de resultados retornados</td> 
   <td>Defina o número máximo de equipes ou grupos que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

### Canal

* [Criar um canal](#create-a-channel)
* [Excluir um canal](#delete-a-channel)
* [Obter um canal](#get-a-channel)
* [Listar canais](#list-channels)
* [Atualizar um canal](#update-a-channel)

#### Criar um canal

Este módulo de ação cria um novo canal para o grupo especificado.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Selecione a equipe no Microsoft Teams para a qual você deseja criar um canal.</p> </td> 
   </tr> 
  <tr> 
   <td>Nome do canal</td> 
   <td>Insira ou mapeie um nome para o novo canal.</td> 
  </tr> 
  <tr> 
   <td>Descrição</td> 
   <td>Insira ou mapeie uma descrição para o novo canal.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um canal

Este módulo de ação exclui o canal especificado de uma Equipe da Microsoft.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Insira ou mapeie a ID da equipe no Microsoft Teams da qual você deseja excluir um canal.</p> </td> 
   </tr> 
  <tr> 
   <td>ID do canal</td> 
   <td>Insira ou mapeie a ID do canal que deseja excluir.</td> 
  </tr> 
  </tbody> 
</table>

#### Obter um canal

Este módulo recupera as propriedades e os relacionamentos de um canal.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Insira ou mapeie a ID da equipe no Microsoft Teams que é proprietária do canal para o qual você deseja recuperar detalhes.</p> </td> 
   </tr> 
  <tr> 
   <td>ID do canal</td> 
   <td>Insira ou mapeie a ID do canal para o qual deseja recuperar detalhes.</td> 
  </tr> 
  </tbody> 
</table>

#### Listar canais

Estes módulos listam os canais que pertencem à equipe especificada no Microsoft Teams.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Selecione a equipe no Microsoft Teams para a qual você deseja listar canais.</p> </td> 
   </tr> 
  <tr> 
   <td>Número máximo de resultados retornados</td> 
   <td>Defina o número máximo de canais que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
  </tbody> 
</table>

#### Atualizar um canal

Este módulo de ação atualiza a descrição do canal especificado.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Selecione a equipe no Microsoft Teams que é proprietária do canal que você deseja atualizar.</p> </td> 
   </tr> 
  <tr> 
   <td>Nome do canal</td> 
   <td>Insira ou mapeie o nome do canal que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td>Descrição</td> 
   <td>Insira ou mapeie a nova descrição do canal.</td> 
  </tr> 
 </tbody> 
</table>

### Mensagem

* [Responder a uma mensagem de canal](#reply-to-a-channel-message)
* [Enviar uma mensagem](#send-a-message)
* [Assistir mensagens](#watch-messages)
* [Assista a novas respostas](#watch-new-replies)

#### Responder a uma mensagem de canal

Este módulo de ação cria uma resposta a uma mensagem no canal especificado.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Selecione a equipe no Microsoft Teams que é proprietária do canal que contém a mensagem que você deseja responder.</p> </td> 
   </tr> 
  <tr> 
   <td>ID do canal</td> 
   <td>Selecione o canal que contém a mensagem que você deseja responder.</td> 
  </tr> 
  <tr> 
   <td>ID da mensagem</td> 
   <td>Insira ou mapeie a ID da mensagem à qual deseja responder.</td> 
  </tr> 
  <tr> 
   <td>Tipo de conteúdo</td> 
   <td>Selecione se deseja enviar a mensagem em texto sem formatação ou no formato HTML.</td> 
  </tr> 
  <tr> 
   <td>Mensagem de resposta</td> 
   <td>Insira ou mapeie o corpo da mensagem de resposta que deseja enviar.</td> 
  </tr> 
 </tbody> 
</table>

#### Enviar uma mensagem

Este módulo de ação envia uma mensagem para o canal de uma equipe ou para um chat.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de mensagem/td&gt; 
   <td> <p>Selecione se você está enviando uma mensagem de canal ou de chat.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Se estiver enviando uma mensagem para um canal, digite ou mapeie a ID da equipe no Microsoft Teams que é proprietária do canal para o qual deseja enviar uma mensagem.</p> </td> 
   </tr> 
  <tr> 
   <td>ID do canal</td> 
   <td>Se estiver enviando uma mensagem para um canal, digite ou mapeie a ID do canal para o qual deseja enviar uma mensagem.</td> 
  </tr> 
  <tr> 
   <td>Criar um novo chat</td> 
   <td>Se estiver enviando uma mensagem de chat, selecione se deseja criar um novo chat.
   <ul><li><b>Sim</b><p>Selecione se deseja um chat individual ou um chat em grupo e selecione o membro que deseja incluir no chat. Você deve selecionar o usuário associado à conexão que este módulo usa, e um chat individual deve conter somente esse usuário e um outro usuário.</p><p>Se você estiver criando um chat em grupo, poderá definir um tópico no campo Tópico.</p>
   <li><b>Não</b><p>Insira ou mapeie a ID da equipe proprietária do canal para o qual deseja enviar uma mensagem e, em seguida, insira ou mapeie a ID do canal.</td> 
  </tr> 
  <tr> 
   <td>Mensagem</td> 
   <td>Insira ou mapeie o corpo da mensagem que deseja enviar.</td> 
  </tr> 
  <tr> 
   <td>Tipo de conteúdo</td> 
   <td>Selecione se deseja enviar a mensagem em texto sem formatação ou no formato HTML.</td> 
  </tr> 
 </tbody> 
</table>

#### Assistir mensagens

Este módulo de acionamento inicia um cenário quando uma mensagem é enviada para o canal de uma equipe ou para um chat.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de mensagens a serem observadas</td> 
   <td> <p>Selecione se você deseja assistir às mensagens do canal ou de bate-papo.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Se você estiver assistindo a mensagens do canal, selecione a equipe no Microsoft Teams que é proprietária do canal que você assiste a mensagens.</p> </td> 
   </tr> 
  <tr> 
   <td>ID do canal</td> 
   <td>Se você estiver assistindo a mensagens do canal, selecione o canal que deseja assistir a mensagens.</td> 
  </tr> 
  <tr> 
   <td>ID do chat</td> 
   <td>Se você estiver assistindo a mensagens de bate-papo, selecione o bate-papo que deseja assistir a mensagens.</td> 
  </tr> 
  <tr> 
   <td>Número máximo de mensagens retornadas</td> 
   <td>Defina o número máximo de mensagens que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

#### Assista a novas respostas

Esse módulo de acionamento inicia um cenário quando uma nova resposta é recebida pela mensagem especificada.

Este módulo não está disponível para contas pessoais.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> <p>Selecione a equipe no Microsoft Teams que é proprietária do canal que você assiste para respostas.</p> </td> 
   </tr> 
  <tr> 
   <td>ID do canal</td> 
   <td>Selecione o canal que deseja observar para respostas.</td> 
  </tr> 
  <tr> 
   <td>ID da mensagem</td> 
   <td>Selecione o bate-papo que deseja assistir para respostas.</td> 
  </tr> 
  <tr> 
   <td>Número máximo de respostas retornadas</td> 
   <td>Defina o número máximo de respostas que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

### Membro

* [Adicionar um membro](#add-a-member)
* [Adicionar um membro a um grupo](#add-a-member-to-a-group)

#### Adicionar um membro

Este módulo de ação adiciona um membro ao Microsoft Teams.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome do membro</td> 
   <td> <p>Insira ou mapeie o nome do membro que você deseja adicionar ao Microsoft Teams.</p> </td> 
   </tr> 
  <tr> 
   <td>Senha</td> 
   <td>Insira ou mapeie a senha do membro.</td> 
  </tr> 
 </tbody> 
</table>

#### Adicionar um membro a um grupo

Este módulo de ação adiciona um membro a um Grupo do Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de Grupo</td> 
   <td> <p>Selecione o grupo ao qual deseja adicionar um membro.</p> </td> 
   </tr> 
  <tr> 
   <td>ID de membro</td> 
   <td>Selecione o membro que deseja adicionar ao grupo.</td> 
  </tr> 
 </tbody> 
</table>

### Reunião online

* [Criar uma reunião online](#create-an-online-meeting)
* [Excluir uma reunião online](#delete-an-online-meeting)
* [Obter uma reunião online](#get-an-online-meeting)
* [Atualizar uma reunião online](#update-an-online-meeting)

#### Criar uma reunião online

Este módulo de ação cria uma reunião independente que não está associada a um evento no calendário do usuário. Esta reunião não aparecerá no calendário do usuário.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Assunto</td> 
   <td>Insira ou mapeie um assunto para esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Data e hora de início</td> 
   <td>Insira ou mapeie a data e a hora em que deseja que a reunião comece. Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Data e hora final</td> 
   <td>Insira ou mapeie a data e a hora em que deseja que a reunião termine. Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Apresentadores permitidos</td> 
   <td>Selecione o grupo que tem permissão para apresentar nesta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Participantes</td> 
   <td>Para cada participante que você deseja adicionar à reunião, clique em <b>Adicionar item</b> e selecione o nome e a função do participante.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir que os participantes habilitem suas câmeras</td> 
   <td>Selecione se deseja permitir que os participantes habilitem suas próprias câmeras.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir que os participantes habilitem seus microfones</td> 
   <td>Selecione se deseja permitir que os participantes habilitem seus próprios microfones.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir bate-papo de reunião</td> 
   <td>Selecione se deseja que o chat da reunião seja habilitado, desabilitado ou limitado à duração da chamada da reunião</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir reações das equipes</td> 
   <td>Selecione se deseja ativar as reações das equipes para esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID da Thread</td> 
   <td>Insira ou mapeie a ID de um thread associado a esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID da mensagem</td> 
   <td>Insira ou mapeie a ID de uma mensagem associada a esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID da mensagem da cadeia de resposta</td> 
   <td>Insira ou mapeie a ID da cadeia de resposta associada a esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Anunciar entrada e saída</td> 
   <td>Selecione se deseja que a reunião anuncie quando os participantes entrarem ou saírem.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Escopo</td> 
   <td>Selecione o grupo de participantes que pode ignorar a espera no lobby. Esses participantes ingressarão na reunião diretamente.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir que usuários de discagem ignorem a sala de espera</td> 
   <td>Selecione se os usuários de discagem devem ser habilitados a ignorar o lobby.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Gravar automaticamente</td> 
   <td>Selecione se deseja gravar a reunião automaticamente.</td> 
   </tr> 
   </tbody> 
</table>

#### Excluir uma reunião online

Este módulo de ação exclui a reunião online com a ID especificada.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID da reunião</td> 
   <td> <p>Informe ou mapeie a ID da reunião que deseja deletar.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Obter uma reunião online

Este módulo de ação recupera detalhes da reunião online com a ID especificada.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID da reunião</td> 
   <td> <p>Insira ou mapeie a ID da reunião da qual deseja recuperar os detalhes.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Atualizar uma reunião online

Este módulo de ação atualiza a reunião online com a ID especificada.



<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID da reunião</td> 
   <td>Informe ou mapeie a ID da reunião que deseja atualizar.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Assunto</td> 
   <td>Insira ou mapeie um assunto para esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Data e hora de início</td> 
   <td>Insira ou mapeie a data e a hora em que deseja que a reunião comece. Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Data e hora final</td> 
   <td>Insira ou mapeie a data e a hora em que deseja que a reunião termine. Para obter uma lista de formatos de data com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Apresentadores permitidos</td> 
   <td>Selecione o grupo que tem permissão para apresentar nesta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Participantes</td> 
   <td>Para cada participante que você deseja adicionar à reunião, clique em <b>Adicionar item</b> e selecione o nome e a função do participante.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir que os participantes habilitem suas câmeras</td> 
   <td>Selecione se deseja permitir que os participantes habilitem suas próprias câmeras.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir que os participantes habilitem seus microfones</td> 
   <td>Selecione se deseja permitir que os participantes habilitem seus próprios microfones.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir bate-papo de reunião</td> 
   <td>Selecione se deseja que o chat da reunião seja habilitado, desabilitado ou limitado à duração da chamada da reunião</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir reações das equipes</td> 
   <td>Selecione se deseja ativar as reações das equipes para esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID da Thread</td> 
   <td>Insira ou mapeie a ID de um thread associado a esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID da mensagem</td> 
   <td>Insira ou mapeie a ID de uma mensagem associada a esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID da mensagem da cadeia de resposta</td> 
   <td>Insira ou mapeie a ID da cadeia de resposta associada a esta reunião.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Anunciar entrada e saída</td> 
   <td>Selecione se deseja que a reunião anuncie quando os participantes entrarem ou saírem.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Escopo</td> 
   <td>Selecione o grupo de participantes que pode ignorar a espera no lobby. Esses participantes ingressarão na reunião diretamente.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permitir que usuários de discagem ignorem a sala de espera</td> 
   <td>Selecione se os usuários de discagem devem ser habilitados a ignorar o lobby.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Gravar automaticamente</td> 
   <td>Selecione se deseja gravar a reunião automaticamente.</td> 
   </tr> 
   </tbody> 
</table>

### Outro

* [Verificar a presença de usuários](#check-presence-of-users)
* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Procurar usuários](#search-users)

#### Verificar a presença de usuários

Esses módulos de ação verificam se os usuários selecionados estão presentes no Microsoft Teams.

Este módulo não é compatível com contas pessoais.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">IDs de usuário</td> 
   <td> <p>Selecione os usuários para os quais deseja verificar a presença.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma solicitação personalizada para a API do Microsoft Teams.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://graph.microsoft.com</code>. Exemplo:<code> /v1.0/groups</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Procurar usuários

Este módulo procura usuários usando os critérios que você especificar.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Microsoft Teams ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtro</td> 
   <td> <p>É possível definir um filtro para retornar somente os usuários que atendem aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que deseja que o filtro avalie, o operador e o valor que deseja que o filtro permita. É possível usar mais de um filtro adicionando regras AND ou OR.</p> </td> 
   </tr> 
  <tr> 
   <td>Número máximo de resultados retornados</td> 
   <td>Defina o número máximo de equipes ou grupos que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>



