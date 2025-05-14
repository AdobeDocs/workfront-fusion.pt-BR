---
title: Módulos DevOps do Azure
description: Em um cenário  [!DNL Adobe Workfront Fusion] , é possível automatizar fluxos de trabalho que usam  [!DNL Azure DevOps], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
source-git-commit: 58bda8289db60ce915613337880297e5c8ec7097
workflow-type: tm+mt
source-wordcount: '1821'
ht-degree: 0%

---

# [!DNL Azure DevOps] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Azure DevOps], bem como conectá-los a vários aplicativos e serviços de terceiros.

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

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos do [!DNL Azure DevOps], você deve ter uma conta DevOps do [!DNL Azure].

## Informações da API [!DNL Azure DevOps]

O conector DevOps do Azure usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## Conectar [!DNL Azure DevOps] a [!DNL Workfront Fusion] {#connect-azure-devops-to-workfront-fusion}

1. Adicione um módulo [!DNL Azure DevOps] ao seu cenário.
1. Clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. No campo [!UICONTROL Tipo de Conexão], selecione o tipo de conexão que deseja usar.

   >[!NOTE]
   >
   >O [!UICONTROL [!DNL Azure DevOps] (EntraApp)] permite solicitar todos os escopos para a conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL Nome da Conexão]</td>
            <td>Insira um nome para a conexão que você está criando.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Organização]</td>
            <td>Digite o nome da organização sob a qual você criou o aplicativo [!DNL Azure DevOps].</td>
      </tr>
      <tr>
            <td>[!UICONTROL ID do Aplicativo]</td>
            <td>Insira a ID do aplicativo DevOps ao qual você está se conectando.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Segredo do Cliente]</td>
            <td>Insira o segredo do cliente para os aplicativos DevOps aos quais você está se conectando.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Solicitar Todos os Escopos]</td>
            <td>Se você estiver usando o tipo de conexão [!DNL Azure DevOps] (EntraApp), habilite essa opção para solicitar todos os escopos para a conexão.</td>
      </tr>
   </table>

1. Para inserir uma ID de Aplicativo DevOps do Azure ou um Segredo do Cliente, clique em <b>Mostrar configurações avançadas</b> e insira-as nos campos abertos.
1. Clique em **[!UICONTROL Continuar]** para concluir a configuração da conexão e continuar criando seu cenário.

## [!UICONTROL DevOps do Azure] módulos e seus campos

Ao configurar módulos do [!DNL Azure DevOps], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Azure DevOps] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

#### [!UICONTROL Fique atento aos itens de trabalho]

Este módulo de disparador instantâneo executa um cenário quando um registro é adicionado, atualizado ou excluído no [!UICONTROL DevOps do Azure].

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecione ou adicione um webhook para o módulo.</p> <p>Para obter mais informações sobre webhooks em módulos de acionador, consulte <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Acionadores instantâneos (webhooks)</a>.</p> <p>Para obter informações sobre como criar um webhook, consulte <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [Criar um registro](#create-a-record)
* [Chamada de API personalizada](#custom-api-call)
* [Baixar um anexo](#download-an-attachment)
* [Vincular itens de trabalho](#link-work-items)
* [Ler registro](#read-record)
* [Atualizar um item de trabalho](#update-a-work-item)
* [[!UICONTROL Carregar um anexo]](#upload-an-attachment)

#### [!UICONTROL Criar um registro]

Este módulo de ação cria um novo projeto ou item de trabalho.

O módulo gera a ID do objeto para o item de trabalho recém-criado ou o URL e o código de status de um projeto recém-criado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de registro]</td> 
   <td> <p>Selecione se deseja criar um item de trabalho ou um projeto.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Projeto]</strong> </p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong>: Insira ou mapeie um nome para o novo projeto.</p> </li> 
       <li> <p><strong>[!UICONTROL Descrição]</strong>: Insira ou mapeie uma descrição para o novo projeto. </p> </li> 
       <li> <p><strong>[!UICONTROL Visibility]</strong>: Selecione se você deseja que seu projeto seja público ou privado. Os usuários devem estar conectados à sua organização e ter acesso ao projeto para interagir com um projeto privado. Os projetos públicos estão visíveis para usuários que não estão conectados à sua organização.</p> </li> 
       <li> <p><strong>[!UICONTROL Controle de Versão]</strong>: Selecione se você deseja que o projeto use [!DNL Git] ou [!UICONTROL Controle de Versão do Team Foundation (TFCV)] para controle de versão.</p> </li> 
       <li> <p><strong>[!UICONTROL Processo de item de trabalho]</strong>: selecione o processo de trabalho que deseja usar para o projeto. As opções são [!UICONTROL Básico], [!UICONTROL Scrum], [!UICONTROL Integração de Modelo de Maturidade de Recursos (CMMI)] e [!UICONTROL Agile].</p> <p>Para obter mais informações sobre [!DNL Azure DevOps] processos, consulte <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&amp;tabs=basic-process">Processos e modelos de processo padrão</a> na Documentação [!DNL Azure DevOps].</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Item de trabalho]</strong> </p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Projeto]</strong>: Selecione o projeto no qual deseja criar o item de trabalho.</p> </li> 
       <li> <p><strong>[!UICONTROL Tipo de item de trabalho]</strong>: selecione o tipo de item de trabalho que deseja criar.</p> </li> 
       <li> <p><strong>[!UICONTROL Outros campos]</strong>: nesses campos, insira o valor que você deseja que o item de trabalho tenha para uma determinada propriedade. Os campos disponíveis dependem do tipo de item de trabalho.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Azure DevOps]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Azure DevOps].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL Base]</td> 
   <td> <p>Selecione ou mapeie a URL base que você usa para se conectar à sua conta [!DNL Azure DevOps]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL relativa]</td> 
   <td> <p>Insira o URL relativo ao qual você deseja se conectar para esta chamada de API.</p> <p><b>Exemplo: </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Versão da API]</td> 
   <td>Selecione ou mapeie a versão da API [!DNL Azure DevOps] à qual você deseja se conectar para esta chamada de API. Se nenhuma versão for selecionada, o [!DNL Workfront Fusion] se conectará ao [!DNL Azure DevOps] API versão 5.1.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> </td> 
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

#### [!UICONTROL Baixar um anexo]

Este módulo de ação baixa um anexo.

O módulo retorna o conteúdo do arquivo do anexo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL do Anexo]</td> 
   <td> <p>Insira ou mapeie o URL do anexo que você deseja baixar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Vincular itens de trabalho]

Esse módulo de ação vincula dois itens de trabalho e define a relação entre eles.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de item de trabalho]</td> 
   <td>Insira ou mapeie a ID do item de trabalho principal ao qual você deseja vincular outro item de trabalho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de item de trabalho vinculado]</td> 
   <td>Insira ou mapeie a ID do item de trabalho que você deseja vincular ao item de trabalho principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Link]</td> 
   <td> <p>Defina a relação entre os itens de trabalho que deseja vincular.</p> <p>Para obter mais informações, consulte o <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">Guia de referência para tipos de link</a> na Documentação do [!UICONTROL Azure DevOps].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comentário]</td> 
   <td>Insira ou mapeie o texto de um comentário. Isso é útil para explicar o raciocínio ou a intenção do link.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler registro]

Este módulo de ação lê dados de um único registro em [!DNL Azure DevOps].

Especifique a ID do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de registro]</td> 
   <td> <p>Selecione se você deseja ler um projeto ou um item de trabalho</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Projeto]</strong>: Selecione o projeto que você deseja ler.</p> </li> 
     <li> <p><strong>[!UICONTROL Item de trabalho]</strong>: selecione o projeto que contém o item de trabalho que você deseja ler e selecione o tipo de item de trabalho.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td>Selecione as informações que deseja incluir no pacote de saída deste módulo. Os campos disponíveis dependem do tipo de item de trabalho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID do registro que deseja ler.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um item de trabalho]

Este módulo de ação atualiza um item de trabalho existente usando sua ID.

O módulo retorna a ID do item de trabalho atualizado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projeto]</td> 
   <td>Selecione o projeto que contém o item de trabalho que você deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Item de Trabalho]</td> 
   <td> <p>Selecione o tipo de item de trabalho que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outros Campos]</td> 
   <td>Em cada um desses campos, insira o valor que você deseja que o item de trabalho tenha para uma determinada propriedade. Os campos disponíveis dependem do tipo de item de trabalho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de item de trabalho]</td> 
   <td>Informe ou mapeie a ID do item de trabalho que você deseja atualizar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um anexo]

Este módulo de ação carrega um arquivo e o anexa a um item de trabalho.

O módulo retorna a ID do anexo e um URL de download para o anexo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projeto] </td> 
   <td> <p>Selecione o projeto no qual deseja fazer upload de um anexo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de item de trabalho]</td> 
   <td> <p>Insira ou mapeie a ID do item de trabalho para o qual você deseja fazer upload de um anexo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comentário]</td> 
   <td>Insira o texto de um comentário que deseja adicionar ao anexo carregado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source] </td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou insira ou mapeie o nome e o conteúdo do arquivo de origem.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

#### [!UICONTROL Listar itens de trabalho]

Este módulo de ação recupera todos os itens de trabalho de um tipo específico em um projeto [!DNL Azure DevOps].

O módulo retorna a ID do item de trabalho principal e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projeto]</td> 
   <td>Selecione o projeto do qual deseja recuperar itens de trabalho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de item de trabalho]</td> 
   <td> <p>Selecione o tipo de item de trabalho que deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. Os campos disponíveis dependem do tipo de item de trabalho que você deseja recuperar. Você deve selecionar pelo menos uma propriedade.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de itens de trabalho que [!DNL Workfront Fusion] retorna durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>
