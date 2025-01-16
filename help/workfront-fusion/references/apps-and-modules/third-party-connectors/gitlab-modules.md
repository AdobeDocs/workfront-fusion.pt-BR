---
title: Módulos do GitLab
description: O Adobe Workfront Fusion exige uma licença do Adobe Workfront Fusion, além de uma licença do Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3554'
ht-degree: 0%

---

# [!UICONTROL GitLab] módulos

O Adobe Workfront Fusion exige uma licença do Adobe Workfront Fusion, além de uma licença do Adobe Workfront.

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!UICONTROL GitLab], bem como conectá-los a vários aplicativos e serviços de terceiros.

>[!NOTE]
>
>Este artigo espera alguma familiaridade com a documentação da API e com a funcionalidade do [!DNL GitLab] em geral.

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

## Conectar [!DNL GitLab] a [!DNL Workfront Fusion] {#connect-gitlab-to-workfront-fusion}

1. Em qualquer módulo [!DNL Workfront Fusion] [!DNL Gitlab], clique em **[!UICONTROL Add]** ao lado do campo de conexão.
1. Configure os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td> <p>Insira um nome para a conexão.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL [!DNL GitLab] URL]</td> 
      <td>Insira a URL da instância [!DNL GitLab].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Access Token]</td> 
      <td><p>Insira seu [!UICONTROL Private Token] ou [!UICONTROL Personal Access Token].</p><p>Para obter informações sobre como localizar ou criar um token de acesso pessoal no [!DNL GitLab], consulte "Criar um token de acesso pessoal" em <a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">Tokens de acesso pessoal</a> na documentação do [!DNL GitLab].</p></td> 
     </tr> 
    </tbody> 
   </table>


1. Clique em **[!UICONTROL Continue]**.
1. Clique em **[!UICONTROL Authorize]** para criar a conexão e retornar ao módulo.

## [!DNL GitLab] módulos e seus campos

Ao configurar módulos do [!DNL GitLab], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL GitLab] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Triggers

+++**[!UICONTROL Watch build status]**

Esse módulo de acionador instantâneo inicia um cenário quando o status de uma criação é alterado.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook observe para alterações de status da compilação</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commit/MR/issue/snippet comments]**

Esse módulo de acionador instantâneo inicia um cenário quando um comentário é feito em uma confirmação, solicitação de mesclagem, problema ou trecho de código.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para comentários</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commits (pushes)]**

Esse módulo de acionador instantâneo inicia um cenário quando uma confirmação é enviada para um repositório. Esse módulo não inicia um cenário quando uma tag é enviada.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para confirmações</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issue comment]**

Este módulo de acionamento instantâneo inicia um cenário quando um comentário é feito sobre um problema.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para comentários do problema</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issues]**

Este módulo [!UICONTROL instant trigger] inicia um cenário quando um problema é criado ou quando um problema existente é atualizado, fechado ou reaberto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook observe para problemas</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge requests]**

Esse módulo de acionador instantâneo inicia um cenário quando uma das situações a seguir ocorre:

* Uma nova solicitação de mesclagem é criada
* Uma solicitação de mesclagem existente foi atualizada, mesclada ou fechada
* Uma confirmação é adicionada na ramificação de origem


<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para solicitações de mesclagem</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge request comments]**

Este módulo de acionamento instantâneo inicia um cenário quando um comentário é feito em uma solicitação de mesclagem.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para comentários de solicitação de mesclagem</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch pipeline status]**

Esse módulo de acionador instantâneo inicia um cenário quando o status de um pipeline é alterado.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook observe para alterações de status do pipeline</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch projects]**

Esse módulo de acionamento agendado inicia um cenário quando um novo projeto é adicionado, do qual o usuário autenticado é membro.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL GitLab] ao [!DNL Workfront] Fusion, consulte <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Conectar [!DNL GitLab] ao [!DNL Workfront] Fusion</a> neste artigo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Máximo de Resultados</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que você deseja que o módulo assista durante cada ciclo de execução de cenário.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository branches]**

Esse módulo de acionador agendado inicia um cenário quando uma nova ramificação é adicionada a um repositório.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL GitLab] ao [!DNL Workfront] Fusion, consulte <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Conectar [!DNL GitLab] ao [!DNL Workfront] Fusion</a> neste artigo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Máximo de Resultados</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que você deseja que o módulo assista durante cada ciclo de execução de cenário.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository tags]**

Esse módulo de acionador instantâneo inicia um cenário quando uma tag é criada ou excluída em um repositório.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para tags</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch snippet comments]**

Este módulo de acionamento instantâneo inicia um cenário quando um novo comentário é feito em um trecho.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para comentários</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch todos]**

Este módulo de acionamento agendado inicia um cenário quando uma nova tarefa é adicionada. Quando nenhum filtro é aplicado, o acionador é executado quando uma nova tarefa pendente é adicionada.

Para obter informações sobre campos, consulte [Obter uma lista de tarefas](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Watch wiki page]**

Este módulo de acionamento instantâneo inicia um cenário quando uma página wiki é criada ou editada.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Add]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para páginas wiki</li></ul></li><li>Clique em <b>[!UICONTROL Save]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

### Ações

+++**[!UICONTROL Accept merge request]**

Este módulo de ação mescla as alterações enviadas com a solicitação de mesclagem fornecida.

Para obter informações sobre campos, consulte [Aceitar solicitação de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Cancel a build]**

Este módulo de ação cancela uma única build de um projeto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL GitLab] ao [!DNL Workfront] Fusion, consulte <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Conectar [!DNL GitLab] ao [!DNL Workfront] Fusion</a> neste artigo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Selecione ou mapeie o projeto que contém a build que você deseja cancelar.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td>Selecione ou mapeie a build que deseja cancelar.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge commit message]</td> 
   <td> Insira ou mapeie uma mensagem de confirmação para a mesclagem.
    </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Should remove source branch]</td> 
   <td>Selecione se deseja remover a ramificação de origem quando a mesclagem for concluída.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge when build succeeds]</td> 
   <td>Selecione se deseja mesclar a solicitação de mesclagem assim que a compilação for concluída.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL SHA]</td> 
   <td>Se presente, esse SHA deve corresponder ao HEAD da ramificação de origem. Se não corresponder, a mesclagem falhará.</td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Cancel a pipeline's builds]**

Esse módulo de ação cancela as builds de um único pipeline.

Para obter informações sobre campos, consulte [Cancelar trabalhos de um pipeline](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Cancel merge when pipeline succeeds]**

Se uma solicitação de mesclagem for definida para mesclar quando um pipeline for bem-sucedido, esse módulo de ação cancelará essa ação.

Para obter informações sobre campos, consulte [Cancelar mesclagem quando o pipeline tiver êxito](https://docs.gitlab.com/ee/api/merge_requests.html) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Cherry pick a commit]**

Essa cereja do módulo de ação escolhe uma confirmação em uma determinada ramificação.

Para obter informações sobre campos, consulte [Escolha uma confirmação](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create a new label]**

Esse módulo de ação cria um novo rótulo para o repositório especificado.

Para obter informações sobre campos, consulte [Criar um novo rótulo](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create a new pipeline]**

Este módulo de ação cria um novo pipeline para o projeto fornecido.

Para obter informações sobre campos, consulte [Criar um novo pipeline](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create a new release]**

Este módulo de ação adiciona notas de versão à tag do Git existente.

Para obter informações sobre campos, consulte [Criar uma versão](https://docs.gitlab.com/ee/api/releases/#create-a-release) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create a new tag]**

Esse módulo de ação cria uma nova tag no repositório que aponta para a referência fornecida.

Para obter informações sobre campos, consulte [Criar uma nova marca](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create a todo]**

Este módulo de ação cria uma tarefa para o usuário atual sobre o problema selecionado. O usuário atual é o usuário identificado pelas credenciais na conexão usada para este módulo.

Para obter informações sobre campos, consulte [Criar uma tarefa pendente](https://docs.gitlab.com/ee/api/issues.html#create-a-todo) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create a todo on a merge request]**

Este módulo de ação cria uma tarefa para o usuário atual na solicitação de mesclagem selecionada. O usuário atual é o usuário identificado pelas credenciais na conexão usada para este módulo.

Para obter informações sobre campos, consulte [Criar uma tarefa](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create merge request]**

Este módulo de ação cria uma nova solicitação de mesclagem em um projeto.

Para obter informações sobre campos, consulte [Criar solicitação de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create new file in repository]**

Este módulo de ação cria um novo arquivo no repositório selecionado.

Para obter informações sobre campos, consulte [Criar novo arquivo no repositório](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Create new issue note]**

Este módulo de ação cria uma nota de problema para um único problema do projeto.

Para obter informações sobre campos, consulte [Criar nova nota de problema](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Create new merge request note]**

Este módulo de ação cria uma observação para uma única solicitação de mesclagem.

Para obter informações sobre campos, consulte [Criar nova nota de solicitação de mesclagem](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create a new milestone]**

Este módulo de ação cria uma nova etapa para um projeto.

Para obter informações sobre campos, consulte [Criar novo marco](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create new snippet note]**

Este módulo de ação cria uma nova nota para um único trecho. As notas de trecho são comentários que os usuários podem publicar em um trecho.

Para obter informações sobre campos, consulte [Criar nova nota de trecho](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create repository branch]**

Esse módulo de ação cria uma única ramificação de repositório.

Para obter informações sobre campos, consulte [Criar ramificação do repositório](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Create build variable]**

Este módulo de ação cria uma nova variável de build.

Para obter informações sobre campos, consulte [Criar variável](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Delete a merge request]**

Este módulo de ação é somente para administradores e proprietários de projetos. Ele exclui a solicitação de mesclagem em questão

Para obter informações sobre campos, consulte [Excluir uma solicitação de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Delete existing file in repository]**

Este módulo de ação exclui um arquivo existente do repositório.

Para obter informações sobre campos, consulte [Excluir arquivo existente no repositório](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Delete repository branch]**

Este módulo de ação exclui uma ramificação do repositório.

Para obter informações sobre campos, consulte [Excluir ramificação do repositório](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Edit issue]**

Este módulo de ação atualiza um problema existente do projeto. Esta chamada também é usada para marcar um problema como encerrado.

Para obter informações sobre campos, consulte [Editar problema](https://docs.gitlab.com/ee/api/issues.html#edit-issue) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Edit Milestone]**
Este módulo de ação atualiza um marco de projeto existente.

Para obter informações sobre campos, consulte [Editar marco](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Erase a build]**

Esse módulo de ação apaga uma criação de um projeto (remove artefatos e o log de trabalhos).

Para obter informações sobre campos, consulte [Apagar um trabalho](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get a list of todos]**

Este módulo de pesquisa recupera uma lista de itens por- fazer.

Para obter informações sobre campos, consulte [Obter uma lista de tarefas](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get a single build]**

Este módulo de ação recupera um único trabalho de um projeto.

Para obter informações sobre campos, consulte [Obter um único trabalho](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get a single repository tag]**

Esse módulo de ação recupera uma tag de repositório específica determinada pelo nome.

Para obter informações sobre campos, consulte [Obter uma única marca de repositório](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Get a specific deployment]**

Este módulo de ação recupera uma implantação específica.

Para obter informações sobre campos, consulte [Obter uma implantação específica](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get all issues assigned to a single milestone]**

Este módulo de pesquisa recupera todos os problemas atribuídos a uma única etapa do projeto.

Para obter informações sobre campos, consulte [Obter todos os problemas atribuídos a um único marco](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get file from repository]**

Este módulo de ação recupera informações sobre um arquivo no repositório, como nome, tamanho ou conteúdo.

Para obter informações sobre campos, consulte [Obter arquivo do repositório](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Get project users]**

Este módulo de pesquisa recupera os usuários do projeto.

Para obter informações sobre campos, consulte [Obter usuários do projeto](https://docs.gitlab.com/ee/api/projects.html#get-project-users) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Get a single issue]**

Este módulo de ação recupera os detalhes do problema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para criar uma nova conexão, consulte <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td> <p>Selecione o projeto que contém o problema sobre o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID]</td> 
   <td> <p>Insira ou mapeie o nome do problema sobre o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Get single issue note]**

Este módulo de ação recupera uma única nota para um problema de projeto específico.

Para obter informações sobre campos, consulte [Obter observação sobre um único problema](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request]**

Este módulo de ação recupera informações sobre uma única solicitação de mesclagem.

Para obter informações sobre campos, consulte [Obter solicitação de mesclagem única](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request changes]**

Este módulo de pesquisa recupera informações sobre a solicitação de mesclagem, incluindo seus arquivos e alterações.

Para obter informações sobre campos, consulte [Obter alterações de solicitação de mesclagem única](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request commits]**

Este módulo de ação recupera uma lista de confirmações de solicitações de mesclagem.

Para obter informações sobre campos, consulte [Obter confirmações de solicitação de mesclagem única](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request note]**

Este módulo de ação retorna uma única nota para uma determinada solicitação de mesclagem.

Para obter informações sobre campos, consulte [Obter nota de solicitação de mesclagem única](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get a Milestone]**

Este módulo de ação recupera os detalhes das etapas.

Para obter informações sobre campos, consulte [Obter marco único](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get single project]**

Este módulo de ação recupera os detalhes do projeto.

Para obter informações sobre campos, consulte [Obter um único projeto](https://docs.gitlab.com/ee/api/projects.html#get-single-project) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get single repository branch]**

Este módulo de ação recupera os detalhes da ramificação do repositório.

Para obter informações sobre campos, consulte [Obter ramificação única do repositório](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get snippet note]**

Este módulo recupera uma única nota para um determinado trecho.

Para obter informações sobre campos, consulte [Obter uma única nota de trecho](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get the comments of a commit]**

Este módulo de pesquisa recupera comentários de uma confirmação em um projeto.

Para obter informações sobre campos, consulte [Obter os comentários de uma confirmação](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get the diff of a commit]**

Este módulo de ação obtém a diferença de uma confirmação em um projeto.

Para obter informações sobre campos, consulte [Obter a diferença de uma confirmação](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Keep artifacts]**

Impede que artefatos sejam excluídos quando a expiração é definida.

Para obter informações sobre campos, consulte [Manter artefatos](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List all merge request notes]**

Este módulo de pesquisa recupera uma lista de todas as notas para uma única solicitação de mesclagem.

Para obter informações sobre campos, consulte [Listar todas as notas de solicitação de mesclagem](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List all snippet notes]**

Este módulo obtém uma lista de todas as notas de um único trecho. As notas de trecho são comentários que os usuários podem publicar em um trecho.

Para obter informações sobre campos, consulte [??](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL List commit builds]**

Este módulo de pesquisa retorna uma lista de builds para uma confirmação específica em um projeto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para criar uma nova conexão, consulte <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Selecione o projeto que contém a confirmação que você deseja listar builds.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> Para limitar a pesquisa a ser criada com um status específico, selecione o status. Deixar esse campo em branco retorna todas as criações da confirmação.  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL List issues]**

Este módulo de pesquisa retorna todos os problemas de acordo com as configurações de filtro especificadas.

Para obter informações sobre campos, consulte [Listar problemas](https://docs.gitlab.com/ee/api/issues.html#list-issues) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List Issues That Close on Merge]**

Este módulo de pesquisa recupera todos os problemas que seriam fechados ao mesclar a solicitação de mesclagem fornecida.

Para obter informações sobre campos, consulte [Listar problemas que serão fechados na mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List Labels]**

Este módulo de pesquisa recupera todos os rótulos no projeto.

Para obter informações sobre campos, consulte [Listar rótulos](https://docs.gitlab.com/ee/api/labels.html#list-labels) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List merge requests]**

Este módulo de pesquisa recupera todas as solicitações de mesclagem pelas configurações de filtro.

Para obter informações sobre campos, consulte [Listar solicitações de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List Owned Projects]**

Este módulo de pesquisa recupera projetos em que o usuário autenticado está definido como proprietário.

Para obter informações sobre campos, consulte [Listar projetos de usuário](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List project builds]**

Este módulo de pesquisa recupera uma lista de builds em um projeto.

Para obter informações sobre campos, consulte [Listar trabalhos do projeto](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List project deployments]**

Este módulo de pesquisa recupera uma lista de implantações em um projeto.

Para obter informações sobre campos, consulte [Listar implantações de projeto](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List project issue notes]**

Este módulo de pesquisa recupera uma lista de todas as notas para um único problema.

Para obter informações sobre campos, consulte [Listar notas de problemas do projeto](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL List project issues]**

Este módulo de pesquisa retorna todos os problemas em um projeto especificado.

Para obter informações sobre campos, consulte [Listar problemas do projeto](https://docs.gitlab.com/ee/api/issues.html#list-project-issues) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List project milestones]**

Este módulo de pesquisa recupera todos os marcos no projeto.

Para obter informações sobre campos, consulte [Listar marcos do projeto](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List project pipelines]**

Este módulo de pesquisa recupera todos os pipelines do projeto.

Para obter informações sobre campos, consulte [Listar pipelines de projeto](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL List project repository tags]**

Este módulo de pesquisa recupera uma lista de tags do repositório de um projeto, classificadas por nome em ordem alfabética inversa.

Para obter informações sobre campos, consulte [Listar marcas de repositório de projeto](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List project variables]**

Este módulo de pesquisa recupera uma lista de variáveis de um projeto.

Para obter informações sobre campos, consulte [Listar variáveis de projeto](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL List projects]**

Este módulo de pesquisa recupera todos os projetos dos quais o usuário autenticado é membro.

Para obter informações sobre campos, consulte [Listar todos os projetos](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List repository branches]**

Este módulo pesquisa ramificações de repositório pelo termo de pesquisa.

Para obter informações sobre campos, consulte [Listar ramificações do repositório](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL List repository commits]**

Este módulo de pesquisa recupera uma lista de confirmações de repositório em um projeto.

Para obter informações sobre campos, consulte [Listar confirmações de repositório](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL List repository contributors]**

Este módulo de pesquisa recupera uma lista de colaboradores do repositório.

Para obter informações sobre campos, consulte [Contribuidores](https://docs.gitlab.com/ee/api/repositories.html#contributors) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL List repository tree]**

Este módulo de pesquisa recupera uma lista de arquivos e diretórios do repositório em um projeto.

Para obter informações sobre campos, consulte [Listar árvore de repositório](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Mark a todo as done]**

Este módulo de ação marca um único item pendente fornecido por sua ID para o usuário atual como concluído.

Para obter informações sobre campos, consulte [Marcar um item de tarefa como concluído](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing issue note]**

Modifica uma nota existente de um problema.

Para obter informações sobre campos, consulte [Modificar observação sobre problemas existentes](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing merge request note]**

Modifica a nota existente de uma solicitação de mesclagem.

Para obter informações sobre campos, consulte [Modificar nota de solicitação de mesclagem existente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing snippet note]**

Este módulo de ação modifica uma nota existente de um trecho.

Para obter informações sobre campos, consulte [Modificar nota de trecho existente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL New issue]**

Este módulo de ação cria um novo problema de projeto.

Para obter informações sobre campos, consulte [Novo problema](https://www.integromat.com/en/help/app/gitlab) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Play a build]**

Este módulo de ação dispara uma ação manual para iniciar um trabalho.

Para obter informações sobre campos, consulte [Reproduzir um trabalho](https://docs.gitlab.com/ee/api/jobs.html#play-a-job) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Post comment to commit]**

Este módulo de ação adiciona um comentário a uma confirmação.

Para obter informações sobre campos, consulte [Postar comentário para confirmar](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Remove variable]**

Este módulo de ação remove a variável de um projeto.

Para obter informações sobre campos, consulte [Remover variável](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Retry a build]**

Este módulo de ação tenta novamente um único build em uma confirmação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para criar uma nova conexão, consulte <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Selecione o projeto que contém a build que você deseja tentar novamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td> Selecione a build que deseja tentar novamente. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Retry Failed Jobs in a Pipeline]**

Este módulo de ação tenta novamente builds com falha em um pipeline.

Para obter informações sobre campos, consulte [Repetir trabalhos em um pipeline](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Get a Variable]**

Este módulo recupera detalhes da variável específica de um projeto.

Para obter informações sobre campos, consulte [Mostrar detalhes da variável](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Update a release]**

Este módulo de ação atualiza uma versão.

Para obter informações sobre campos, consulte [Atualizar uma versão](https://docs.gitlab.com/ee/api/releases/#update-a-release) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Update merge request]**

Este módulo de ação atualiza uma solicitação de mesclagem existente. Você pode alterar a ramificação de destino, o título ou até mesmo fechar a MR.

Para obter informações sobre campos, consulte [Atualizar solicitação de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Update a Variable]**

Este módulo de ação atualiza a variável de um projeto.

Para obter informações sobre campos, consulte [Atualizar variável](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable) na documentação [!DNL GitLab].

+++
