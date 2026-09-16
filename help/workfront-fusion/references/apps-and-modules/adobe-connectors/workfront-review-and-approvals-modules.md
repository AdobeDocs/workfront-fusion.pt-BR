---
title: Módulos de conteúdo e aprovação do Adobe Workfront
description: Com os módulos de Conteúdo e Aprovações do Adobe Workfront, você pode obter detalhes de aprovação, tomar uma decisão sobre um ativo, adicionar ou excluir participantes de aprovação, adicionar ou atualizar estágios de aprovação, bloquear ou desbloquear estágios e fazer chamadas de API personalizadas.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4f637dcb9d7865f73b41faa5b0acf397944bb559
workflow-type: tm+mt
source-wordcount: '5202'
ht-degree: 11%
---
# Módulos de revisão e aprovação unificados do Adobe Workfront

Com os módulos Unified Review and Approvals da Adobe Workfront, você pode obter detalhes de aprovação, tomar uma decisão sobre um ativo, adicionar ou excluir participantes de aprovação, adicionar ou atualizar estágios de aprovação, bloquear ou desbloquear estágios e fazer chamadas de API personalizadas.

Para obter informações sobre a revisão e as aprovações unificadas da Workfront, consulte [Visão geral da revisão e aprovação unificadas](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/document-approvals-overview) na documentação da Workfront.

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
* [Criar aprovação agrupada](#create-grouped-approval)
* [Criar estágios](#create-stages)
* [Bloquear um estágio](#lock-a-stage)
* [Tomar uma decisão](#make-a-decision)
* [Tomar uma decisão em um estágio](#make-a-decision-on-a-stage)
* [Gerenciar ativos em uma aprovação agrupada](#manage-assets-on-a-grouped-approval)
* [Gerenciar participantes do estágio](#manage-stage-participants)
* [Gerenciar estágios em uma aprovação agrupada](#manage-stages-on-a-grouped-approval)
* [Lembrar um participante de um estágio](#remind-a-participant-on-a-stage)
* [Lembrar participante](#remind-participant)
* [Lembrar participantes indecisos](#remind-undecided-participants)
* [Lembrar participantes indecisos em um estágio](#remind-undecided-participants-on-a-stage)
* [Desbloquear um estágio](#unlock-a-stage)
* [Atualizar um estágio](#update-a-stage)
* [Atualizar um modelo](#update-a-template)
* [Atualizar todos os estágios](#update-all-stages)
* [Atualizar aprovação agrupada (estado completo)](#update-grouped-approval-full-state)


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

#### Criar aprovação agrupada

Esse módulo de ação cria uma aprovação agrupada: um conjunto de versões de documento que se movem juntas por um ou mais caminhos de aprovação, cada um com uma sequência ordenada de estágios com seus próprios participantes.

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
      <td>Insira ou mapeie um nome de exibição para a aprovação agrupada. O nome deve ter entre 1 e 255 caracteres.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Ativos</p></td>
      <td>Para cada versão de documento que você deseja incluir no grupo, clique em <b>Adicionar item</b> e insira a ID da versão do documento (DOCV).</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Caminhos</p></td>
      <td>Para cada caminho de aprovação que você deseja adicionar, clique em <b>Adicionar item</b> e insira a ID do caminho, o nome e os estágios. Cada caminho contém uma sequência ordenada de estágios. Para cada estágio, no campo Estágios, clique em <b>Adicionar item</b> e insira os seguintes dados:
      <ul>
      <li><b>ID do estágio</b><p>Insira um identificador atribuído pelo cliente para o estágio, exclusivo em todos os caminhos. Deve ser alfanumérico, com sublinhados ou hifens permitidos e até 64 caracteres.</p></li>
      <li><b>Nome do estágio</b><p>Insira ou mapeie um nome para o estágio.</p></li>
      <li><b>IDs dos estágios principais</b><p>Para cada estágio pai que você deseja adicionar ao estágio, clique em <b>Adicionar item</b> e insira a ID Pai.</p></li>
      <li><b>Participantes</b><p>Para cada participante que você deseja adicionar ao estágio, clique em <b>Adicionar item</b> e insira os detalhes do participante.
      <ul>
      <li><b>ID do participante</b><p>Insira ou mapeie o ID do participante.</p></li>
      <li><b>Tipo de participante</b><p>Selecione se o participante é um usuário ou uma equipe.</p></li>
      <li><b>Função do participante</b><p>Selecione se o participante é um aprovador ou um revisor.</p></li>
      </ul>
      </p></li>
      <li><b>Data do prazo</b><p>Se o prazo final for uma data específica, insira ou mapeie a data.</p></li>
      <li><b>Dias úteis até o prazo</b><p>Se o prazo final for após um número específico de dias úteis, informe ou mapeie o número de dias.</p></li>
      <li><b>Hora do prazo: Horas</b><p>Insira ou mapeie a hora do dia para o prazo final (0-23). Emparelhar com prazo final: minutos.</p></li>
      <li><b>Hora do Prazo: Minutos</b><p>Insira ou mapeie o minuto da hora para o prazo final (0-59). Emparelhar com tempo limite: horas.</p></li>
      <li><b>Mensagem personalizada</b><p>Insira ou mapeie uma mensagem personalizada para o estágio.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do Objeto Pai</p></td>
      <td>Insira ou mapeie a ID do objeto pai do Workfront (por exemplo, um projeto ou uma tarefa) que você deseja associar à aprovação agrupada. Se você usar esse campo, também deverá inserir o Código do objeto.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Código do objeto</p></td>
      <td>Insira ou mapeie o código do tipo de objeto Workfront para o objeto pai (por exemplo, <code>PROJ</code> ou <code>TASK</code>). Obrigatório se você informar uma ID de Objeto Pai.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do modelo</p></td>
      <td>(Opcional) Insira ou mapeie uma ID de modelo para registrar na aprovação agrupada para rastreabilidade.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
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
      <td role="rowheader"><p>ID do modelo</p></td>
      <td>Insira ou mapeie a ID do ativo para o qual deseja criar estágios.</td> 
      </tr>
  </tbody>
</table>

<!--
BECKY CHECK ME: The following block of Delete-prefixed Actions modules (Delete a decision on a stage, Delete a stage, Delete a template, Delete an approval, Delete decisions, Delete grouped approval, Delete participants) is not confirmed to be current in the live connector as of this update - status uncertain. Commented out for now; restore (and remove this comment) once confirmed, or delete for good if confirmed removed.

#### Delete a decision on a stage

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
   </tbody>
</table>


#### Delete a stage

This action module deletes the specified stage from the approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a stage from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete a template

This module deletes the specified approval template.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Template ID</p></td>
      <td>Enter or map the ID of the template that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete an approval

This action module deletes the approval for the given document.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete an approval from.</td> 
      </tr>
  </tbody>
</table>

#### Delete decisions

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
  </tbody>
</table>

#### Delete grouped approval

This action module deletes a grouped approval, cascading to its child asset approvals and paths.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Group GUID</p></td>
      <td>Enter or map the GUID of the grouped approval that you want to delete.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limit</p></td>
      <td>Enter or map the maximum number of results you want the module to work with during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

#### Delete participants

This action module deletes participants from an approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to delete participants from.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant type</p>
      </td>
      <td>Select whether the participants is a user or a team.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant ID</p>
      </td>
      <td>Enter or map the ID of the participant.</td> 
      </tr>
  </tbody>
</table>
-->

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

#### Gerenciar ativos em uma aprovação agrupada

Este módulo de ação adiciona e/ou remove versões de documentos em uma aprovação agrupada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID da Aprovação Agrupada</p></td>
      <td>Insira ou mapeie o GUID da aprovação agrupada na qual você deseja gerenciar ativos.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Adicionar o Assets</p></td>
      <td>Para cada versão de documento que você deseja adicionar ao grupo, clique em <b>Adicionar item</b> e insira a ID da versão do documento (DOCV).</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Remover Assets</p></td>
      <td>Para cada versão de documento que você deseja remover do grupo, clique em <b>Adicionar item</b> e insira a ID da versão do documento (DOCV).</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
      </tr>
  </tbody>
</table>

#### Gerenciar participantes do estágio

Este módulo de ação adiciona, atualiza e/ou remove participantes de um estágio específico de uma aprovação agrupada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID da Aprovação Agrupada</p></td>
      <td>Insira ou mapeie o GUID da aprovação agrupada.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID do estágio</p></td>
      <td>Insira ou mapeie a ID do estágio no qual você deseja gerenciar os participantes.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Adicionar participantes</p></td>
      <td>Para cada participante que você deseja adicionar ao estágio, clique em <b>Adicionar item</b> e insira os seguintes detalhes:
      <ul>
      <li><b>Tipo de participante</b><p>Selecione se o participante é um usuário ou uma equipe.</p></li>
      <li><b>Participante</b><p>Insira ou mapeie o ID do participante.</p></li>
      <li><b>Função</b><p>Selecione se o participante é um aprovador ou um revisor.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Atualizar participantes</p></td>
      <td>Para cada participante que você deseja atualizar no estágio, clique em <b>Adicionar item</b> e insira os seguintes detalhes:
      <ul>
      <li><b>Tipo de participante</b><p>Selecione se o participante é um usuário ou uma equipe.</p></li>
      <li><b>Participante</b><p>Insira ou mapeie o ID do participante.</p></li>
      <li><b>Função</b><p>Selecione se o participante é um aprovador ou um revisor.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Remover Participantes</p></td>
      <td>Para cada participante que você deseja remover do estágio, clique em <b>Adicionar item</b> e insira os seguintes detalhes:
      <ul>
      <li><b>Tipo de participante</b><p>Selecione se o participante é um usuário ou uma equipe.</p></li>
      <li><b>Participante</b><p>Insira ou mapeie o ID do participante.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
      </tr>
  </tbody>
</table>

#### Gerenciar estágios em uma aprovação agrupada

Este módulo de ação adiciona, atualiza e/ou remove estágios em uma aprovação agrupada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID da Aprovação Agrupada</p></td>
      <td>Insira ou mapeie o GUID da aprovação agrupada.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Adicionar estágios</p></td>
      <td>Para cada estágio que você deseja adicionar, clique em <b>Adicionar item</b> e insira os seguintes detalhes:
      <ul>
      <li><b>ID do estágio</b><p>Insira ou mapeie um identificador para o estágio.</p></li>
      <li><b>Nome do estágio</b><p>Insira ou mapeie um nome para o estágio.</p></li>
      <li><b>Data do prazo</b><p>Se o prazo final for uma data específica, insira ou mapeie a data.</p></li>
      <li><b>Dias úteis até o prazo</b><p>Se o prazo final for após um número específico de dias úteis, informe ou mapeie o número de dias.</p></li>
      <li><b>Mensagem personalizada</b><p>Insira ou mapeie uma mensagem personalizada para o estágio.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Estágios de Atualização</p></td>
      <td>Para cada estágio que você deseja atualizar, clique em <b>Adicionar item</b> e insira os seguintes detalhes:
      <ul>
      <li><b>ID do estágio</b><p>Insira ou mapeie a ID do estágio que você deseja atualizar.</p></li>
      <li><b>Nome do estágio</b><p>Insira ou mapeie um nome para o estágio.</p></li>
      <li><b>Data do prazo</b><p>Se o prazo final for uma data específica, insira ou mapeie a data.</p></li>
      <li><b>Dias úteis até o prazo</b><p>Se o prazo final for após um número específico de dias úteis, informe ou mapeie o número de dias.</p></li>
      <li><b>Mensagem personalizada</b><p>Insira ou mapeie uma mensagem personalizada para o estágio.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Remover estágios</p></td>
      <td>Para cada estágio que você deseja remover, clique em <b>Adicionar item</b> e insira a ID do estágio.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
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
      <td role="rowheader"><p>ID do modelo</p></td>
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

#### Atualizar aprovação agrupada (estado completo)

Este módulo de ação aplica uma atualização de estado completo a uma aprovação agrupada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID da Aprovação Agrupada</p></td>
      <td>Insira ou mapeie o GUID da aprovação agrupada que você deseja atualizar. Por exemplo, <code>9f8b60820000462ecf66c409d1248fa9</code>.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Caminhos</p></td>
      <td>Para cada caminho de aprovação que você deseja que a aprovação agrupada tenha, clique em <b>Adicionar item</b> e insira a ID do caminho, o nome e os estágios. O Fusion reconcilia isso com o estado atual, adicionando, atualizando e removendo caminhos para corresponder ao que você envia. Cada caminho contém uma sequência ordenada de estágios. Para cada estágio, no campo Estágios, clique em <b>Adicionar item</b> e insira os seguintes dados:
      <ul>
      <li><b>ID do estágio</b><p>Insira um identificador atribuído pelo cliente para o estágio, exclusivo em todos os caminhos. Deve ser alfanumérico, com sublinhados ou hifens permitidos e até 64 caracteres.</p></li>
      <li><b>Nome do estágio</b><p>Insira ou mapeie um nome para o estágio.</p></li>
      <li><b>IDs dos estágios principais</b><p>Para cada estágio pai que você deseja adicionar ao estágio, clique em <b>Adicionar item</b> e insira a ID Pai.</p></li>
      <li><b>Participantes</b><p>Para cada participante que você deseja adicionar ao estágio, clique em <b>Adicionar item</b> e insira os detalhes do participante.
      <ul>
      <li><b>ID do participante</b><p>Insira ou mapeie o ID do participante.</p></li>
      <li><b>Tipo de participante</b><p>Selecione se o participante é um usuário ou uma equipe.</p></li>
      <li><b>Função do participante</b><p>Selecione se o participante é um aprovador ou um revisor.</p></li>
      </ul>
      </p></li>
      <li><b>Data do prazo</b><p>Se o prazo final for uma data específica, insira ou mapeie a data.</p></li>
      <li><b>Dias úteis até o prazo</b><p>Se o prazo final for após um número específico de dias úteis, informe ou mapeie o número de dias.</p></li>
      <li><b>Hora do prazo: Horas</b><p>Insira ou mapeie a hora do dia para o prazo final (0-23). Emparelhar com prazo final: minutos.</p></li>
      <li><b>Hora do Prazo: Minutos</b><p>Insira ou mapeie o minuto da hora para o prazo final (0-59). Emparelhar com tempo limite: horas.</p></li>
      <li><b>Mensagem personalizada</b><p>Insira ou mapeie uma mensagem personalizada para o estágio.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Ativos</p></td>
      <td>(Opcional) Para cada versão de documento que você deseja que o grupo contenha, clique em <b>Adicionar item</b> e insira a ID da versão do documento (DOCV). Se você omitir esse campo, os ativos atuais serão deixados inalterados.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Chave de Idempotência</p></td>
      <td>(Opcional) Insira ou mapeie uma chave fornecida pelo cliente (máximo de 128 caracteres) que torne segura uma solicitação repetida. Se você enviar a mesma chave novamente, o módulo não aplicará a atualização uma segunda vez.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
      </tr>
  </tbody>
</table>

### Pesquisas

* [Obter um modelo](#get-a-template)
* [Obter detalhes da aprovação](#get-approval-details)
* [Obter aprovações em uma aprovação agrupada](#get-approvals-in-a-grouped-approval)
* [Obter detalhes de aprovação agrupados](#get-grouped-approval-details)
* [Obter várias aprovações](#get-multiple-approvals)
* [Obter aprovações sugeridas](#get-suggested-approvals)
* [Obter participantes sugeridos](#get-suggested-participants)
* [Listar bots](#list-bots)
* [Listar aprovações agrupadas por responsável](#list-grouped-approvals-by-parent)
* [Modelos de lista](#list-templates)
* [Pesquisar análises de marca de IA](#search-ai-brand-reviews)
* [Pesquisar aprovações agrupadas](#search-grouped-approvals)


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
      <td role="rowheader"><p>ID do modelo</p></td>
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

#### Obter aprovações em uma aprovação agrupada

Este módulo de pesquisa retorna as aprovações de ativos individuais que compõem uma aprovação agrupada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Grupo GUID</p></td>
      <td>Insira ou mapeie o GUID da aprovação agrupada para a qual você deseja obter aprovações.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Dados da versão do documento</p></td>
      <td>Selecione se o registro Redrock documentVersion deve ser anexado a cada aprovação de versão de documento (DOCV). </td>
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
      </tr>
  </tbody>
</table>

#### Obter detalhes de aprovação agrupados

Este módulo de pesquisa retorna uma aprovação agrupada por seu GUID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Grupo GUID</p></td>
      <td>Insira ou mapeie o GUID da aprovação agrupada para a qual você deseja obter detalhes.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
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

#### Listar bots

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

#### Listar aprovações agrupadas por responsável

Este módulo de pesquisa retorna as aprovações agrupadas associadas a um objeto principal do Workfront.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID do Pai</p></td>
      <td>Insira ou mapeie a ID do objeto principal do Workfront (por exemplo, um projeto ou uma tarefa) para o qual você deseja obter aprovações agrupadas.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Código do objeto</p></td>
      <td>(Opcional) Insira ou mapeie o código do tipo de objeto Workfront para o objeto pai (por exemplo, <code>PROJ</code> ou <code>TASK</code>).</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
      </tr>
  </tbody>
</table>

#### Modelos de lista

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

#### Pesquisar aprovações agrupadas

Este módulo de pesquisa pesquisa pesquisa aprovações agrupadas usando uma visualização nomeada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Conexão</td>
      <td>Para obter instruções sobre como criar uma conexão com a Revisão e Aprovações Unificadas do Adobe Workfront, consulte <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Conectar-se à Revisão e Aprovações Unificadas do Adobe Workfront</a> neste artigo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Exibir</p></td>
      <td>(Opcional) Selecione ou mapeie a exibição nomeada que determina a forma da resposta. No momento, somente Aguardando aprovações é suportado.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>(Opcional) Insira ou mapeie o tamanho da página para a primeira página de resultados. O máximo é 100 e o padrão é 20.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Cursor</p></td>
      <td>(Opcional) Insira ou mapeie o cursor opaco de uma resposta anterior para buscar a próxima página de resultados. Se você fornecer um cursor, o módulo ignorará o campo Limite.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>IDs das Equipes</p></td>
      <td>(Opcional) Para cada equipe pela qual você também deseja corresponder aprovações agrupadas (em que a equipe é um participante), clique em <b>Adicionar item</b> e insira a ID da equipe.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
      </tr>
  </tbody>
</table>

<!-- BECKY CHECK ME: the screenshot shows two separate fields both labeled "Limit" - an optional pagination page-size field (max 100, default 20, ignored if Cursor is set) and a required general execution-cycle limit, matching the Limit field used in every other module in this article. Confirm this isn't a UI labeling issue before publishing, and that both rows are needed/correctly distinguished. -->

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
