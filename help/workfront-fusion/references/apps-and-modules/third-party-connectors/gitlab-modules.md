---
title: Módulos do GitLab
description: O Adobe Workfront Fusion exige uma licença do Adobe Workfront Fusion, além de uma licença do Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: 6aad13e81c083754d7aad53dec103715bd6b8807
workflow-type: tm+mt
source-wordcount: '4099'
ht-degree: 10%

---

# [!UICONTROL GitLab] módulos

O Adobe Workfront Fusion exige uma licença do Adobe Workfront Fusion, além de uma licença do Adobe Workfront.

Em um cenário do Adobe Workfront Fusion, você pode automatizar fluxos de trabalho que usam o [!UICONTROL GitLab], bem como conectá-lo a vários aplicativos e serviços de terceiros.

>[!NOTE]
>
>Este artigo espera alguma familiaridade com a documentação da API e com a funcionalidade do [!DNL GitLab] em geral.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

## Conectar o [!DNL GitLab] ao Workfront Fusion {#connect-gitlab-to-workfront-fusion}

1. Em qualquer módulo do Workfront Fusion [!DNL Gitlab], clique em **[!UICONTROL Adicionar]** ao lado do campo de conexão.
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
      <td role="rowheader">[!UICONTROL Token de Acesso]</td> 
      <td><p>Digite o [!UICONTROL Token privado] ou o [!UICONTROL Token de acesso pessoal].</p><p>Para obter informações sobre como localizar ou criar um token de acesso pessoal no [!DNL GitLab], consulte "Criar um token de acesso pessoal" em <a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">Tokens de acesso pessoal</a> na documentação do [!DNL GitLab].</p></td> 
     </tr> 
    </tbody> 
   </table>


1. Clique em **[!UICONTROL Continuar]**.
1. Clique em **[!UICONTROL Autorizar]** para criar a conexão e retornar ao módulo.

## Módulos do [!DNL GitLab] e seus campos

Ao configurar módulos do [!DNL GitLab], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos do [!DNL GitLab] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Acionadores

+++**[!UICONTROL Observar status da compilação]**

Esse módulo de acionador instantâneo inicia um cenário quando o status de uma criação é alterado.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook observe para alterações de status da compilação</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Observar comentários de confirmação/MR/problema/trecho]**

Esse módulo de acionador instantâneo inicia um cenário quando um comentário é feito em uma confirmação, solicitação de mesclagem, problema ou trecho de código.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para comentários</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Observar confirmações (envios)]**

Esse módulo de acionador instantâneo inicia um cenário quando uma confirmação é enviada para um repositório. Esse módulo não inicia um cenário quando uma tag é enviada.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para confirmações</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Assista ao comentário sobre o problema]**

Este módulo de acionamento instantâneo inicia um cenário quando um comentário é feito sobre um problema.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para comentários do problema</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Assistir problemas]**

Este módulo do [!UICONTROL acionador instantâneo] inicia um cenário quando um problema é criado ou quando um problema existente é atualizado, fechado ou reaberto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook observe para problemas</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Assistir solicitações de mesclagem]**

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
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para solicitações de mesclagem</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Observar comentários da solicitação de mesclagem]**

Este módulo de acionamento instantâneo inicia um cenário quando um comentário é feito em uma solicitação de mesclagem.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para comentários de solicitação de mesclagem</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Observar status do pipeline]**

Esse módulo de acionador instantâneo inicia um cenário quando o status de um pipeline é alterado.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook observe para alterações de status do pipeline</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Assistir a projetos]**

Esse módulo de acionamento agendado inicia um cenário quando um novo projeto é adicionado, do qual o usuário autenticado é membro.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL GitLab] ao Workfront Fusion, consulte <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Conectar [!DNL GitLab] ao Workfront Fusion</a> neste artigo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Máximo de Resultados</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que você deseja que o módulo assista durante cada ciclo de execução de cenário.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Observar ramificações do repositório]**

Esse módulo de acionador agendado inicia um cenário quando uma nova ramificação é adicionada a um repositório.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL GitLab] ao Workfront Fusion, consulte <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Conectar [!DNL GitLab] ao Workfront Fusion</a> neste artigo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Máximo de Resultados</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que você deseja que o módulo assista durante cada ciclo de execução de cenário.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Observar marcas de repositório]**

Esse módulo de acionador instantâneo inicia um cenário quando uma tag é criada ou excluída em um repositório.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para tags</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Observar comentários de trecho]**

Este módulo de acionamento instantâneo inicia um cenário quando um novo comentário é feito em um trecho.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para comentários</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Assistir todos]**

Este módulo de acionamento agendado inicia um cenário quando uma nova tarefa é adicionada. Quando nenhum filtro é aplicado, o acionador é executado quando uma nova tarefa pendente é adicionada.

Para obter informações sobre campos, consulte [Obter uma lista de tarefas](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Assistir à página wiki]**

Este módulo de acionamento instantâneo inicia um cenário quando uma página wiki é criada ou editada.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Selecione o webhook que deseja usar para este acionador ou adicione um novo webhook. </p><p>Para adicionar um novo webhook, <ol><li>Clique em <b>[!UICONTROL Adicionar]</b> ao lado do campo [!UICONTROL webhook].</li><li>Insira o seguinte: <ul><li>Um nome para o webhook</li><li>A conexão que você deseja usar com este webhook</li><li>O projeto que você deseja que o webhook assista para páginas wiki</li></ul></li><li>Clique em <b>[!UICONTROL Salvar]</b> para salvar o webhook e retornar ao módulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

### Ações

+++**[!UICONTROL Aceitar solicitação de mesclagem]**

Este módulo de ação mescla as alterações enviadas com a solicitação de mesclagem fornecida.

Para obter informações sobre campos, consulte [Aceitar solicitação de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Cancelar uma compilação]**

Este módulo de ação cancela uma única build de um projeto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL GitLab] ao Workfront Fusion, consulte <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Conectar [!DNL GitLab] ao Workfront Fusion</a> neste artigo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Selecione ou mapeie o projeto que contém a build que você deseja cancelar.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL ID de Compilação]</td> 
   <td>Selecione ou mapeie a build que deseja cancelar.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL mesclar mensagem de confirmação]</td> 
   <td> Insira ou mapeie uma mensagem de confirmação para a mesclagem.
    </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Deve remover ramificação de origem]</td> 
   <td>Selecione se deseja remover a ramificação de origem quando a mesclagem for concluída.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Mesclar quando a compilação for bem-sucedida]</td> 
   <td>Selecione se deseja mesclar a solicitação de mesclagem assim que a compilação for concluída.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL SHA]</td> 
   <td>Se presente, esse SHA deve corresponder ao HEAD da ramificação de origem. Se não corresponder, a mesclagem falhará.</td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Cancelar as compilações de um pipeline]**

Esse módulo de ação cancela as builds de um único pipeline.

Para obter informações sobre campos, consulte [Cancelar trabalhos de um pipeline](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Cancelar mesclagem quando o pipeline tiver êxito]**

Se uma solicitação de mesclagem for definida para mesclar quando um pipeline for bem-sucedido, esse módulo de ação cancelará essa ação.

Para obter informações sobre campos, consulte [Cancelar mesclagem quando o pipeline tiver êxito](https://docs.gitlab.com/ee/api/merge_requests.html) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Escolha uma confirmação]**

Essa cereja do módulo de ação escolhe uma confirmação em uma determinada ramificação.

Para obter informações sobre campos, consulte [Escolha uma confirmação](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar um novo rótulo]**

Esse módulo de ação cria um novo rótulo para o repositório especificado.

Para obter informações sobre campos, consulte [Criar um novo rótulo](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar um novo pipeline]**

Este módulo de ação cria um novo pipeline para o projeto fornecido.

Para obter informações sobre campos, consulte [Criar um novo pipeline](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar uma nova versão]**

Este módulo de ação adiciona notas de versão à tag do Git existente.

Para obter informações sobre campos, consulte [Criar uma versão](https://docs.gitlab.com/ee/api/releases/#create-a-release) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar uma nova tag]**

Esse módulo de ação cria uma nova tag no repositório que aponta para a referência fornecida.

Para obter informações sobre campos, consulte [Criar uma nova marca](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar uma tarefa]**

Este módulo de ação cria uma tarefa para o usuário atual sobre o problema selecionado. O usuário atual é o usuário identificado pelas credenciais na conexão usada para este módulo.

Para obter informações sobre campos, consulte [Criar uma tarefa pendente](https://docs.gitlab.com/ee/api/issues.html#create-a-todo) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar uma tarefa em uma solicitação de mesclagem]**

Este módulo de ação cria uma tarefa para o usuário atual na solicitação de mesclagem selecionada. O usuário atual é o usuário identificado pelas credenciais na conexão usada para este módulo.

Para obter informações sobre campos, consulte [Criar uma tarefa](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar solicitação de mesclagem]**

Este módulo de ação cria uma nova solicitação de mesclagem em um projeto.

Para obter informações sobre campos, consulte [Criar solicitação de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar novo arquivo no repositório]**

Este módulo de ação cria um novo arquivo no repositório selecionado.

Para obter informações sobre campos, consulte [Criar novo arquivo no repositório](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Criar nova nota de problema]**

Este módulo de ação cria uma nota de problema para um único problema do projeto.

Para obter informações sobre campos, consulte [Criar nova nota de problema](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Criar nova nota de solicitação de mesclagem]**

Este módulo de ação cria uma observação para uma única solicitação de mesclagem.

Para obter informações sobre campos, consulte [Criar nova nota de solicitação de mesclagem](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar um novo marco]**

Este módulo de ação cria uma nova etapa para um projeto.

Para obter informações sobre campos, consulte [Criar novo marco](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar nova nota de trecho]**

Este módulo de ação cria uma nova nota para um único trecho. As notas de trecho são comentários que os usuários podem publicar em um trecho.

Para obter informações sobre campos, consulte [Criar nova nota de trecho](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar ramificação do repositório]**

Esse módulo de ação cria uma única ramificação de repositório.

Para obter informações sobre campos, consulte [Criar ramificação do repositório](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Criar variável de compilação]**

Este módulo de ação cria uma nova variável de build.

Para obter informações sobre campos, consulte [Criar variável](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Excluir uma solicitação de mesclagem]**

Este módulo de ação é somente para administradores e proprietários de projetos. Ele exclui a solicitação de mesclagem em questão

Para obter informações sobre campos, consulte [Excluir uma solicitação de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Excluir arquivo existente no repositório]**

Este módulo de ação exclui um arquivo existente do repositório.

Para obter informações sobre campos, consulte [Excluir arquivo existente no repositório](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Excluir ramificação do repositório]**

Este módulo de ação exclui uma ramificação do repositório.

Para obter informações sobre campos, consulte [Excluir ramificação do repositório](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Editar problema]**

Este módulo de ação atualiza um problema existente do projeto. Esta chamada também é usada para marcar um problema como encerrado.

Para obter informações sobre campos, consulte [Editar problema](https://docs.gitlab.com/ee/api/issues.html#edit-issue) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Editar Etapa]**
Este módulo de ação atualiza um marco de projeto existente.

Para obter informações sobre campos, consulte [Editar marco](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Apagar uma compilação]**

Esse módulo de ação apaga uma criação de um projeto (remove artefatos e o log de trabalhos).

Para obter informações sobre campos, consulte [Apagar um trabalho](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter uma lista de tarefas]**

Este módulo de pesquisa recupera uma lista de itens por- fazer.

Para obter informações sobre campos, consulte [Obter uma lista de tarefas](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter uma única compilação]**

Este módulo de ação recupera um único trabalho de um projeto.

Para obter informações sobre campos, consulte [Obter um único trabalho](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter uma única marca de repositório]**

Esse módulo de ação recupera uma tag de repositório específica determinada pelo nome.

Para obter informações sobre campos, consulte [Obter uma única marca de repositório](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Obter uma implantação específica]**

Este módulo de ação recupera uma implantação específica.

Para obter informações sobre campos, consulte [Obter uma implantação específica](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter todos os problemas atribuídos a um único marco]**

Este módulo de pesquisa recupera todos os problemas atribuídos a uma única etapa do projeto.

Para obter informações sobre campos, consulte [Obter todos os problemas atribuídos a um único marco](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter arquivo do repositório]**

Este módulo de ação recupera informações sobre um arquivo no repositório, como nome, tamanho ou conteúdo.

Para obter informações sobre campos, consulte [Obter arquivo do repositório](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Obter usuários do projeto]**

Este módulo de pesquisa recupera os usuários do projeto.

Para obter informações sobre campos, consulte [Obter usuários do projeto](https://docs.gitlab.com/ee/api/projects.html#get-project-users) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Obter um único problema]**

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
   <td role="rowheader">[!UICONTROL Identificação de Problema]</td> 
   <td> <p>Insira ou mapeie o nome do problema sobre o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Obter observação sobre um único problema]**

Este módulo de ação recupera uma única nota para um problema de projeto específico.

Para obter informações sobre campos, consulte [Obter observação sobre um único problema](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Obter solicitação de mesclagem única]**

Este módulo de ação recupera informações sobre uma única solicitação de mesclagem.

Para obter informações sobre campos, consulte [Obter solicitação de mesclagem única](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter alterações de solicitação de mesclagem única]**

Este módulo de pesquisa recupera informações sobre a solicitação de mesclagem, incluindo seus arquivos e alterações.

Para obter informações sobre campos, consulte [Obter alterações de solicitação de mesclagem única](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter confirmações de solicitação de mesclagem única]**

Este módulo de ação recupera uma lista de confirmações de solicitações de mesclagem.

Para obter informações sobre campos, consulte [Obter confirmações de solicitação de mesclagem única](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter nota de solicitação de mesclagem única]**

Este módulo de ação retorna uma única nota para uma determinada solicitação de mesclagem.

Para obter informações sobre campos, consulte [Obter nota de solicitação de mesclagem única](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter um Marco]**

Este módulo de ação recupera os detalhes das etapas.

Para obter informações sobre campos, consulte [Obter marco único](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter um único projeto]**

Este módulo de ação recupera os detalhes do projeto.

Para obter informações sobre campos, consulte [Obter um único projeto](https://docs.gitlab.com/ee/api/projects.html#get-single-project) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter ramificação única do repositório]**

Este módulo de ação recupera os detalhes da ramificação do repositório.

Para obter informações sobre campos, consulte [Obter ramificação única do repositório](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter nota de trecho]**

Este módulo recupera uma única nota para um determinado trecho.

Para obter informações sobre campos, consulte [Obter uma única nota de trecho](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter os comentários de uma confirmação]**

Este módulo de pesquisa recupera comentários de uma confirmação em um projeto.

Para obter informações sobre campos, consulte [Obter os comentários de uma confirmação](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter a diferença de uma confirmação]**

Este módulo de ação obtém a diferença de uma confirmação em um projeto.

Para obter informações sobre campos, consulte [Obter a diferença de uma confirmação](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Manter artefatos]**

Impede que artefatos sejam excluídos quando a expiração é definida.

Para obter informações sobre campos, consulte [Manter artefatos](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar todas as notas de solicitação de mesclagem]**

Este módulo de pesquisa recupera uma lista de todas as notas para uma única solicitação de mesclagem.

Para obter informações sobre campos, consulte [Listar todas as notas de solicitação de mesclagem](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar todas as anotações de trecho]**

Este módulo obtém uma lista de todas as notas de um único trecho. As notas de trecho são comentários que os usuários podem publicar em um trecho.

Para obter informações sobre campos, consulte [Listar todas as notas de trecho](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar compilações de confirmação]**

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
   <td role="rowheader">[!UICONTROL Escopo]</td> 
   <td> Para limitar a pesquisa a ser criada com um status específico, selecione o status. Deixar esse campo em branco retorna todas as criações da confirmação.  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Listar problemas]**

Este módulo de pesquisa retorna todos os problemas de acordo com as configurações de filtro especificadas.

Para obter informações sobre campos, consulte [Listar problemas](https://docs.gitlab.com/ee/api/issues.html#list-issues) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar Problemas que Serão Encerrados na Mesclagem]**

Este módulo de pesquisa recupera todos os problemas que seriam fechados ao mesclar a solicitação de mesclagem fornecida.

Para obter informações sobre campos, consulte [Listar problemas que serão fechados na mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar rótulos]**

Este módulo de pesquisa recupera todos os rótulos no projeto.

Para obter informações sobre campos, consulte [Listar rótulos](https://docs.gitlab.com/ee/api/labels.html#list-labels) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar solicitações de mesclagem]**

Este módulo de pesquisa recupera todas as solicitações de mesclagem pelas configurações de filtro.

Para obter informações sobre campos, consulte [Listar solicitações de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar Projetos]**

Este módulo de pesquisa recupera projetos em que o usuário autenticado está definido como proprietário.

Para obter informações sobre campos, consulte [Listar projetos de usuário](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar compilações de projeto]**

Este módulo de pesquisa recupera uma lista de builds em um projeto.

Para obter informações sobre campos, consulte [Listar trabalhos do projeto](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar implantações de projeto]**

Este módulo de pesquisa recupera uma lista de implantações em um projeto.

Para obter informações sobre campos, consulte [Listar implantações de projeto](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar notas de problemas do projeto]**

Este módulo de pesquisa recupera uma lista de todas as notas para um único problema.

Para obter informações sobre campos, consulte [Listar notas de problemas do projeto](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Listar problemas do projeto]**

Este módulo de pesquisa retorna todos os problemas em um projeto especificado.

Para obter informações sobre campos, consulte [Listar problemas do projeto](https://docs.gitlab.com/ee/api/issues.html#list-project-issues) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar marcos do projeto]**

Este módulo de pesquisa recupera todos os marcos no projeto.

Para obter informações sobre campos, consulte [Listar marcos do projeto](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar pipelines de projeto]**

Este módulo de pesquisa recupera todos os pipelines do projeto.

Para obter informações sobre campos, consulte [Listar pipelines de projeto](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Listar marcas de repositório de projeto]**

Este módulo de pesquisa recupera uma lista de tags do repositório de um projeto, classificadas por nome em ordem alfabética inversa.

Para obter informações sobre campos, consulte [Listar marcas de repositório de projeto](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar variáveis de projeto]**

Este módulo de pesquisa recupera uma lista de variáveis de um projeto.

Para obter informações sobre campos, consulte [Listar variáveis de projeto](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Listar projetos]**

Este módulo de pesquisa recupera todos os projetos dos quais o usuário autenticado é membro.

Para obter informações sobre campos, consulte [Listar todos os projetos](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar ramificações do repositório]**

Este módulo pesquisa ramificações de repositório pelo termo de pesquisa.

Para obter informações sobre campos, consulte [Listar ramificações do repositório](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Listar confirmações de repositório]**

Este módulo de pesquisa recupera uma lista de confirmações de repositório em um projeto.

Para obter informações sobre campos, consulte [Listar confirmações de repositório](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Listar colaboradores do repositório]**

Este módulo de pesquisa recupera uma lista de colaboradores do repositório.

Para obter informações sobre campos, consulte [Contribuidores](https://docs.gitlab.com/ee/api/repositories.html#contributors) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Listar árvore de repositório]**

Este módulo de pesquisa recupera uma lista de arquivos e diretórios do repositório em um projeto.

Para obter informações sobre campos, consulte [Listar árvore de repositório](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Marcar uma tarefa como concluída]**

Este módulo de ação marca um único item pendente fornecido por sua ID para o usuário atual como concluído.

Para obter informações sobre campos, consulte [Marcar um item de tarefa como concluído](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Modificar observação sobre problema existente]**

Modifica uma nota existente de um problema.

Para obter informações sobre campos, consulte [Modificar observação sobre problemas existentes](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Modificar nota de solicitação de mesclagem existente]**

Modifica a nota existente de uma solicitação de mesclagem.

Para obter informações sobre campos, consulte [Modificar nota de solicitação de mesclagem existente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Modificar nota de trecho existente]**

Este módulo de ação modifica uma nota existente de um trecho.

Para obter informações sobre campos, consulte [Modificar nota de trecho existente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Novo problema]**

Este módulo de ação cria um novo problema de projeto.

Para obter informações sobre campos, consulte [Novo problema](https://www.integromat.com/en/help/app/gitlab) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Executar uma compilação]**

Este módulo de ação dispara uma ação manual para iniciar um trabalho.

Para obter informações sobre campos, consulte [Reproduzir um trabalho](https://docs.gitlab.com/ee/api/jobs.html#play-a-job) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Postar comentário para confirmar]**

Este módulo de ação adiciona um comentário a uma confirmação.

Para obter informações sobre campos, consulte [Postar comentário para confirmar](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Remover variável]**

Este módulo de ação remove a variável de um projeto.

Para obter informações sobre campos, consulte [Remover variável](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Repetir uma compilação]**

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
   <td role="rowheader">[!UICONTROL ID de Compilação]</td> 
   <td> Selecione a build que deseja tentar novamente. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Repetir Trabalhos com Falha em um Pipeline]**

Este módulo de ação tenta novamente builds com falha em um pipeline.

Para obter informações sobre campos, consulte [Repetir trabalhos em um pipeline](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Obter uma Variável]**

Este módulo recupera detalhes da variável específica de um projeto.

Para obter informações sobre campos, consulte [Mostrar detalhes da variável](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Atualizar uma versão]**

Este módulo de ação atualiza uma versão.

Para obter informações sobre campos, consulte [Atualizar uma versão](https://docs.gitlab.com/ee/api/releases/#update-a-release) na documentação de [!DNL GitLab].

+++

+++**[!UICONTROL Atualizar solicitação de mesclagem]**

Este módulo de ação atualiza uma solicitação de mesclagem existente. Você pode alterar a ramificação de destino, o título ou até mesmo fechar a MR.

Para obter informações sobre campos, consulte [Atualizar solicitação de mesclagem](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr) na documentação [!DNL GitLab].

+++

+++**[!UICONTROL Atualizar uma Variável]**

Este módulo de ação atualiza a variável de um projeto.

Para obter informações sobre campos, consulte [Atualizar variável](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable) na documentação [!DNL GitLab].

+++
