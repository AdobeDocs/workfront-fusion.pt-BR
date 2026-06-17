---
title: Módulos de conteúdo e aprovação do Adobe Workfront
description: Com os módulos de Conteúdo e Aprovações do Adobe Workfront, você pode obter detalhes de aprovação, tomar uma decisão sobre um ativo, adicionar ou excluir participantes de aprovação, adicionar ou atualizar estágios de aprovação, bloquear ou desbloquear estágios e fazer chamadas de API personalizadas.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 8b031ed2093d4844f05c52db9fc79ce9e7e4b85c
workflow-type: tm+mt
source-wordcount: 3743
ht-degree: 15%

---

# Módulos de revisão e aprovação unificados do Adobe Workfront

Com os módulos Unified Review and Approvals da Adobe Workfront, você pode obter detalhes de aprovação, tomar uma decisão sobre um ativo, adicionar ou excluir participantes de aprovação, adicionar ou atualizar estágios de aprovação, bloquear ou desbloquear estágios e fazer chamadas de API personalizadas.

Para obter informações sobre a revisão e as aprovações unificadas da Workfront, consulte [Visão geral da revisão e aprovação unificadas](https://experienceleague.adobe.com/pt-br/docs/workfront/using/review-and-approve-work/document-approvals-overview) na documentação da Workfront.

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

Você deve ter o seguinte para acessar o conteúdo e as aprovações do Workfront:

* Você deve ter uma versão do Workfront compatível com o armazenamento em nuvem da Adobe. Se sua organização ainda não tiver uma versão compatível, entre em contato com o representante de conta da Adobe.

## Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront


1. Em qualquer módulo de Revisão e Aprovações Unificadas do Adobe Workfront, clique em **Adicionar** ao lado do campo Conexão.
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

   Se você não estiver conectado ao Workfront Unified Review and Approvals, será direcionado para uma tela de logon. Depois de fazer logon, é possível permitir a conexão.

## Módulos de revisão e aprovação unificados do Adobe Workfront

Ao configurar módulos do Workfront, o Workfront Fusion exibe os campos listados abaixo. Junto com esses campos, podem ser exibidos campos adicionais do Workfront, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ações](#actions)
* [Pesquisas](#searches)
* [Outras](#other)

### Ações

* [Adicionar ou atualizar participantes](#add-or-update-participants)
* [Modelos de exclusão em massa](#bulk-delete-templates)
* [Criar um modelo](#create-a-template)
* [Criar uma aprovação](#create-an-approval)
* [Criar estágios](#create-stages)
* [Excluir uma decisão em um estágio](#delete-a-decision-on-a-stage)
* [Excluir um estágio](#delete-a-stage)
* [Excluir um modelo](#delete-a-template)
* [# Excluir uma aprovação](#delete-an-approval)
* [Excluir decisões](#delete-decisions)
* [Excluir participantes](#delete-participants)
* [Bloquear um estágio](#lock-a-stage)
* [Tomar uma decisão](#make-a-decision)
* [Tomar uma decisão em um estágio](#make-a-decision-on-a-stage)
* [Lembrar um participante de um estágio](#remind-a-participant-on-a-stage)
* [Lembrar participante](#remind-participant)
* [Lembrar participantes indecisos](#remind-undecided-participants)
* [Lembrar participantes indecisos em um estágio](#remind-undecided-participants-on-a-stage)
* [Desbloquear um estágio](#unlock-a-stage)
* [Atualizar um estágio](#update-a-stage)
* [Atualizar um modelo](#update-a-template)
* [Atualizar todos os estágios](#update-all-stages)


#### Adicionar ou atualizar participantes

Este módulo de ação adiciona ou atualiza os participantes no estágio padrão em uma aprovação.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>ID do Documento</p>
      </td>
      <td>Informe ou mapeie o ID do ativo para o qual você deseja adicionar ou atualizar um participante.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Adicionar participantes aos estágios</p>
      </td>
      <td>Para cada estágio ao qual você deseja adicionar participantes, clique em <b>Adicionar item</b> e entre no estágio.<p> Em seguida, para cada participante que deseja adicionar ao estágio, clique em <b>Adicionar item</b> e insira os detalhes do participante.</p>
      <ul>
      <li><b>ID do participante</b><p>Insira ou mapeie o ID do participante.</p></li>
      <li><b>Tipo de participante</b><p>Selecione se o participante é um usuário ou uma equipe.</p></li>
      <li><b>Função do participante</b><p>Selecione se o participante é um aprovador ou um revisor.</p></li>
      </ul> 
      </td> 
      </tr>
  </tbody>
</table>

#### Modelos de exclusão em massa

Este módulo exclui os modelos de aprovação especificados.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>IDs de modelo</p></td>
      <td>Para cada modelo que você deseja excluir, clique em <b>Adicionar item</b> e insira a ID do modelo.</td> 
      </tr>
  </tbody>
</table>

#### Criar um modelo

Este módulo de ação cria um modelo de aprovação

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Nome</p></td>
      <td>Insira ou mapeie um nome para o modelo.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID da Empresa</p></td>
      <td>Se quiser adicionar um escopo de empresa ao modelo, insira ou mapeie a ID da empresa.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Estágios</p>
      </td>
      <td>Para cada estágio que você deseja adicionar, clique em <b>Adicionar item</b> e insira os dados do estágio.<p>Para obter informações específicas, consulte <a href="#stages-fields" class="MCXref xref" >Campos de estágios</a> neste artigo. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Compartilhado com</p></td>
      <td>Para cada usuário com o qual você deseja compartilhar o modelo, clique em <b>Adicionar item</b>, na ID do usuário e no nível de acesso desejado.</td> 
      </tr>
  </tbody>
</table>

#### Criar uma aprovação

Este módulo de ação cria uma aprovação para um documento no armazenamento em nuvem do Adobe, incluindo dados de preparo ou um modelo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual deseja criar uma aprovação.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Estágios</p>
      </td>
      <td>Para cada estágio que você deseja adicionar, clique em <b>Adicionar item</b> e insira os dados do estágio.<p>Para obter informações específicas, consulte <a href="#stages-fields" class="MCXref xref" >Campos de estágios</a> neste artigo. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>ID do Modelo</p></td>
      <td>Insira ou mapeie a ID do modelo que você deseja usar para esta aprovação.</td> 
      </tr>
  </tbody>
</table>

#### Criar estágios

Esse módulo de ação cria uma aprovação com os dados de estágio fornecidos.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual você deseja criar ou atualizar um estágio.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Estágios</p>
      </td>
      <td>Para cada estágio que você deseja adicionar, clique em <b>Adicionar item</b> e insira os dados do estágio.<p>Para obter informações específicas, consulte <a href="#stages-fields" class="MCXref xref" >Campos de estágios</a> neste artigo. </p> </td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Modelo</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual deseja criar estágios.</td> 
      </tr>
  </tbody>
</table>

#### Excluir uma decisão em um estágio

Este módulo remove a decisão do usuário atual do estágio especificado. O usuário atual é o usuário cujas credenciais são usadas na conexão usada neste módulo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do documento do qual você deseja excluir uma decisão.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do estágio</p></td>
      <td>Insira ou mapeie a ID do estágio que deseja excluir.</td> 
      </tr>
   </tbody>
</table>


#### Excluir um estágio

Esse módulo de ação exclui o estágio especificado da aprovação.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do documento do qual você deseja excluir um estágio.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do estágio</p></td>
      <td>Insira ou mapeie a ID do estágio que deseja excluir.</td> 
      </tr>
  </tbody>
</table>

#### Excluir um modelo

Este módulo exclui o modelo de aprovação especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Modelo</p></td>
      <td>Insira ou mapeie a ID do modelo que deseja excluir.</td> 
      </tr>
  </tbody>
</table>

#### Excluir uma aprovação

Este módulo de ação exclui a aprovação para o documento em questão.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Informe ou mapeie a ID do documento do qual deseja excluir uma aprovação.</td> 
      </tr>
  </tbody>
</table>

#### Excluir decisões

Este módulo remove a decisão do usuário atual do estágio especificado. O usuário atual é o usuário cujas credenciais são usadas na conexão usada neste módulo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do documento do qual você deseja excluir uma decisão.</td> 
      </tr>
  </tbody>
</table>

#### Excluir participantes

Este módulo de ação exclui os participantes de uma aprovação.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Informe ou mapeie a ID do ativo do qual deseja deletar participantes.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Tipo de participante</p>
      </td>
      <td>Selecione se os participantes são um usuário ou uma equipe.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID do participante</p>
      </td>
      <td>Insira ou mapeie o ID do participante.</td> 
      </tr>
  </tbody>
</table>

#### Bloquear um estágio

Esses módulos de ação bloqueiam o estágio de aprovação especificado e definem o estágio como inativo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo que deseja bloquear.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID do estágio</p>
      </td>
      <td>Insira ou mapeie a ID do estágio que você deseja bloquear.</td> 
      </tr>
  </tbody>
</table>

#### Tomar uma decisão

Este módulo de ação aplica uma decisão a um estágio de aprovação ou aprovação.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo que deseja bloquear.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Decisão</p></td>
      <td>Selecione a decisão a ser aplicada à aprovação ou ao estágio.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>IDs de estágio</p>
      </td>
      <td>Para cada estágio ao qual você deseja aplicar a decisão, clique em <b>Adicionar item</b> e insira a ID do estágio.</td> 
      </tr>
  </tbody>
</table>

#### Tomar uma decisão em um estágio

Este módulo aplica uma decisão ao estágio especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do documento no qual você deseja tomar uma decisão.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do estágio</p></td>
      <td>Insira ou mapeie a ID do estágio no qual você deseja tomar uma decisão.</td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Decisão</p></td>
      <td>Selecione a decisão que deseja aplicar a esse estágio.</td> 
      </tr>
  </tbody>
</table>

#### Lembrar um participante de um estágio

Este módulo envia um lembrete para um participante específico em um estágio específico.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual você deseja enviar um lembrete.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID do estágio</p>
      </td>
      <td>Insira ou mapeie a ID do estágio para o qual você deseja enviar um lembrete.</td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do participante</p></td>
      <td>Insira ou mapeie a ID do participante para o qual você deseja enviar um lembrete.</td> 
      </tr>
  </tbody>
</table>

#### Lembrar participante

Este módulo envia uma notificação de lembrete para o participante especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual você deseja enviar um lembrete.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID do participante</p>
      </td>
      <td>Insira ou mapeie o ID do participante que você deseja lembrar.</td> 
      </tr>
      <tr>
      <td role="rowheader">
        <p>Tipo de participante</p>
      </td>
      <td>Insira ou mapeie o tipo do participante que você deseja lembrar.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Função do participante</p>
      </td>
      <td>Insira ou mapeie a função do participante que você deseja lembrar.</td> 
      </tr>
  </tbody>
</table>

#### Lembrar participantes indecisos

Este módulo envia notificações de lembrete para todos os participantes indecisos na aprovação especificada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual você deseja enviar um lembrete.</td> 
      </tr>
  </tbody>
</table>

#### Lembrar participantes indecisos em um estágio

Este módulo envia notificações de lembrete para todos os participantes indecisos em um estágio.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual você deseja enviar um lembrete.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID do estágio</p>
      </td>
      <td>Insira ou mapeie a ID do estágio para o qual você deseja enviar um lembrete.</td> 
      </tr>
  </tbody>
</table>

#### Desbloquear um estágio

Esses módulos de ação desbloqueiam o estágio de aprovação especificado e define o estágio como ativo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo que deseja desbloquear.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID do estágio</p>
      </td>
      <td>Insira ou mapeie a ID do estágio que você deseja bloquear.</td> 
      </tr>
  </tbody>
</table>


#### Atualizar um estágio

Esse módulo de ação atualiza campos no estágio especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do documento no qual você deseja tomar uma decisão.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do estágio</p></td>
      <td>Insira ou mapeie a ID do estágio no qual você deseja tomar uma decisão.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Nome do estágio</p></td>
      <td>Insira ou mapeie um nome para o modelo.</td> 
      </tr>
      <td role="rowheader">
        <p>Outros campos</p>
      </td>
      <td>Insira dados nos campos de estágio.<p>Para obter mais informações, consulte <a href="#stages-fields" class="MCXref xref" >Campos de estágios</a> neste artigo. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Compartilhado com</p></td>
      <td>Para cada usuário com o qual você deseja compartilhar o modelo, clique em <b>Adicionar item</b>, na ID do usuário e no nível de acesso desejado.</td> 
      </tr>
  </tbody>
</table>

#### Atualizar um modelo

Este módulo atualiza os campos no modelo de aprovação especificado.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Modelo</p></td>
      <td>Insira ou mapeie um nome para o modelo.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Nome</p></td>
      <td>Insira ou mapeie a ID do modelo que você deseja atualizar.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID da Empresa</p></td>
      <td>Se quiser adicionar um escopo de empresa ao modelo, insira ou mapeie a ID da empresa.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Estágios</p>
      </td>
      <td>Para cada estágio que você deseja adicionar, clique em <b>Adicionar item</b> e insira os dados do estágio.<p>Para obter informações específicas, consulte <a href="#stages-fields" class="MCXref xref" >Campos de estágios</a> neste artigo. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Compartilhado com</p></td>
      <td>Para cada usuário com o qual você deseja compartilhar o modelo, clique em <b>Adicionar item</b>, na ID do usuário e no nível de acesso desejado.</td> 
      </tr>
  </tbody>
</table>

#### Atualizar todos os estágios

Este módulo substitui todos os estágios em uma aprovação existente pelos dados de estágio fornecidos. O documento deve estar em um estado editável.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual deseja atualizar os estágios.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Estágios</p>
      </td>
      <td>Para cada estágio que você deseja atualizar, clique em <b>Adicionar item</b> e insira os dados do estágio.<p>Para obter informações específicas, consulte <a href="#stages-fields" class="MCXref xref" >Campos de estágios</a> neste artigo. </p> </td> 
      </tr>
  </tbody>
</table>

### Pesquisas

* [Obter um modelo](#get-a-template)
* [Obter detalhes da aprovação](#get-approval-details)
* [Obter várias aprovações](#get-multiple-approvals)
* [Obter aprovações sugeridas](#get-suggested-approvals)
* [Obter participantes sugeridos](#get-suggested-participants)
* [Listar bots](#list-bots)
* [Modelos de lista](#list-templates)
* [Pesquisar revisores de marca de IA](#search-ai-brand-reviews)


#### Obter um modelo

Este módulo retorna o modelo de aprovação especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Modelo</p></td>
      <td>Insira ou mapeie a ID do documento para o qual você deseja obter participantes de aprovação sugeridos.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Número máximo de modelos retornados
         </td>
         <td>
              Insira ou mapeie o número máximo de modelos que você deseja que o módulo retorne durante cada ciclo de execução de cenário. 
         </td>
       </tr>
  </tbody>
</table>

#### Obter detalhes da aprovação

Este módulo de pesquisa recupera detalhes de aprovação de um ativo.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Documento</p>
      </td>
      <td>Insira ou mapeie a ID do ativo para o qual deseja recuperar os detalhes de aprovação.</td> 
      </tr>
  </tbody>
</table>

#### Obter várias aprovações

Este módulo recupera detalhes de aprovações para uma lista de documentos de um tipo específico.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>IDs de documento</p></td>
      <td>Para cada documento para o qual deseja recuperar detalhes de aprovação, clique em <b>Adicionar item</b> e insira a ID do documento.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Número máximo de resultados retornados
         </td>
         <td>
              Insira ou mapeie o número máximo de resultados que você deseja que o módulo retorne durante cada ciclo de execução de cenário. 
         </td>
       </tr>
  </tbody>
</table>

#### Obter aprovações sugeridas

Esse módulo retorna cargas de aprovação sugeridas de versões anteriores do documento.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do documento para o qual você deseja obter as aprovações sugeridas.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Número máximo de aprovações retornadas
         </td>
         <td>
              Insira ou mapeie o número máximo de aprovações que você deseja que o módulo retorne durante cada ciclo de execução de cenário. 
         </td>
       </tr>
  </tbody>
</table>

#### Obter participantes sugeridos

Este módulo retorna as sugestões dos participantes da aprovação para a aprovação do documento anterior.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Documento</p></td>
      <td>Insira ou mapeie a ID do documento para o qual você deseja obter participantes de aprovação sugeridos.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Número máximo de participantes retornados
         </td>
         <td>
              Insira ou mapeie o número máximo de participantes que você deseja que o módulo retorne durante cada ciclo de execução do cenário. 
         </td>
       </tr>
  </tbody>
</table>

#### Lista de bots

Este módulo retorna uma lista paginada de contas de bot.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Página</p></td>
      <td>Insira ou mapeie a página de resultados que deseja retornar.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Número máximo de resultados retornados
         </td>
         <td>
              Insira ou mapeie o número máximo de resultados que você deseja que o módulo retorne durante cada ciclo de execução de cenário. 
         </td>
       </tr>
  </tbody>
</table>

#### Listar Modelos

Este módulo retorna uma lista de todos os modelos de aprovação disponíveis para o usuário atual. O usuário atual é o usuário cujas credenciais são usadas na conexão usada neste módulo.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
   </tbody>
</table>

#### Pesquisar análises de marca de IA

Este módulo retorna os resultados da análise de marca de IA produzidos para uma versão do documento como parte de uma aprovação.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de usuário de bot</p></td>
      <td>Insira ou mapeie a ID de usuário do bot pelo qual deseja pesquisar revisões.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do documento principal</p></td>
      <td>Insira ou mapeie a ID do documento pai pelo qual você deseja pesquisar revisões.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID da versão do documento</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual você deseja enviar um lembrete.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do estágio</p></td>
      <td>Insira ou mapeie uma ID de estágio para limitar os resultados a um estágio específico da aprovação.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Página</p></td>
      <td>Insira ou mapeie um número de página para limitar os resultados a essa página.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Número máximo de análises retornadas
         </td>
         <td>
              Insira ou mapeie o número máximo de revisões que você deseja que o módulo retorne durante cada ciclo de execução do cenário. 
         </td>
       </tr>
  </tbody>
</table>

### Outras

* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Campos de estágios](#stages-fields)


#### Fazer uma chamada de API personalizada

Este módulo faz uma chamada de API personalizada para a API de Revisão e Aprovações unificadas do Adobe Workfront.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Caminho relativo</p>
      </td>
      <td>
        <p>Insira um caminho relativo a <code>https://workfront.adobe.io</code>. Por exemplo, <code>/unified-approvals/public/api/v1/approvals/&lt;ASSET_TYPE&gt;/&lt;ASSET_ID&gt;</code></p>
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



#### Campos de estágios

Os seguintes campos estão disponíveis ao configurar estágios. Nem todos os campos podem estar disponíveis para todos os módulos.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Nome do estágio</td>
      <td>Insira ou mapeie um nome para o estágio.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Data do prazo</p></td>
      <td>Se o prazo final for uma data específica, insira ou mapeie a data.</td> 
      </tr>
  </tbody>
     <tr>
      <td role="rowheader"><p>Dias úteis dentro do prazo</p></td>
      <td>Se o prazo final for após um número específico de dias úteis, informe ou mapeie o número de dias.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Hora do prazo final</p></td>
      <td>Se o prazo final for um horário específico, insira ou mapeie o horário.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Participantes</p></td>
      <td>Para cada participante que você deseja adicionar ao estágio, clique em <b>Adicionar item</b> e insira os detalhes do participante.      
      <ul>
      <li><b>ID do participante</b><p>Insira ou mapeie o ID do participante.</p></li>
      <li><b>Tipo de participante</b><p>Selecione se o participante é um usuário ou uma equipe.</p></li>
      <li><b>Função do participante</b><p>Selecione se o participante é um aprovador ou um revisor.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Bloqueio automático habilitado</p></td>
      <td>Especifique se deseja bloquear automaticamente o estágio.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Regras de decisão</p></td>
      <td>Selecione se deseja exigir apenas uma decisão para o estágio.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>IDs Pai/IDs de Estágio Pai</p></td>
      <td>Para cada estágio pai que você deseja adicionar ao estágio, clique em <b>Adicionar item</b> e insira a ID Pai.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Acionadores</p></td>
      <td>Para configurar um acionador para este estágio de aprovação, clique em <b>Adicionar item</b> e insira os detalhes do acionador.      <ul>
      <li><b>Tipo</b><p>Selecionar <b>Ativação</b></p></li>
      <li><b>Quando</b><p>Selecione se deseja acionar o estágio quando a aprovação for criada ou quando outro estágio for concluído.</p></li>
      <li><b>Estágios</b><p>Para cada estágio que você deseja adicionar ao acionador, clique em <b>Adicionar item</b> e insira ou mapeie a ID do estágio.</p></li>
      <li><b>Decisões</b><p>Para cada decisão que você deseja adicionar ao acionador, clique em <b>Adicionar item</b> e insira ou mapeie a decisão.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Mensagem personalizada</p></td>
      <td>Insira ou mapeie uma mensagem personalizada para o estágio.</td> 
      </tr>
</table>

