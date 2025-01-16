---
title: Módulos DevOps do Azure
description: Em um cenário  [!DNL Adobe Workfront Fusion] , é possível automatizar fluxos de trabalho que usam  [!DNL Azure DevOps], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1564'
ht-degree: 0%

---

# [!DNL Azure DevOps] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Azure DevOps], bem como conectá-los a vários aplicativos e serviços de terceiros.

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
1. Clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. No campo [!UICONTROL Connection Type], selecione **[!DNL Azure DevOps]**.

   >[!IMPORTANT]
   >
   >O tipo de conexão [!UICONTROL [!DNL Azure DevOps] (Request All Scopes)] será descontinuada em breve. Portanto, não recomendamos usá-lo.

1. Preencha os seguintes campos:

   <table style="table-layout:auto">
        <tr>
            <td>[!UICONTROL Connection name]</td>
            <td>Insira um nome para a conexão que você está criando.</td>
        </tr>
      <tr>
            <td>[!UICONTROL Organization]</td>
            <td>Digite o nome da organização sob a qual você criou o aplicativo [!DNL Azure DevOps].</td>
        </tr>
    </table>

1. Clique em **[!UICONTROL Continue]** para concluir a configuração da conexão e continuar criando seu cenário.

## [!UICONTROL Azure DevOps] módulos e seus campos

Ao configurar módulos do [!DNL Azure DevOps], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Azure DevOps] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Triggers

#### [!UICONTROL Watch for work items]

Este módulo de disparador instantâneo executa um cenário quando um registro é adicionado, atualizado ou excluído em [!UICONTROL Azure DevOps].

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecione ou adicione um webhook para o módulo.</p> <p>Para obter mais informações sobre webhooks em módulos de acionadores, consulte <!--<a href="For instructions, see [Instant triggers (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->" class="MCXref xref"&gt;Acionadores instantâneos (webhooks) em [!DNL Adobe Workfront Fusion]</a>.</p> <p>Para obter informações sobre como criar um webhook, consulte <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
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
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)

#### [!UICONTROL Custom API Call]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API [!DNL Azure DevOps]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Azure DevOps].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Base URL]</td> 
   <td> <p>Selecione ou mapeie a URL base que você usa para se conectar à sua conta [!DNL Azure DevOps]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> <p>Insira o URL relativo ao qual você deseja se conectar para esta chamada de API.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Selecione ou mapeie a versão da API [!DNL Azure DevOps] à qual você deseja se conectar para esta chamada de API. Se nenhuma versão for selecionada, o [!DNL Workfront Fusion] se conectará ao [!DNL Azure DevOps] API versão 5.1.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a record]

Este módulo de ação cria um novo projeto ou item de trabalho.

O módulo gera a ID do objeto para o item de trabalho recém-criado ou o URL e o código de status de um projeto recém-criado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecione se deseja criar um item de trabalho ou um projeto.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong> </p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong>:Insira ou mapeie um nome para o novo projeto.</p> </li> 
       <li> <p><strong>[!UICONTROL Description]</strong>:Insira ou mapeie uma descrição para o novo projeto. </p> </li> 
       <li> <p><strong>[!UICONTROL Visibility]</strong>: selecione se deseja que o projeto seja público ou privado. Os usuários devem estar conectados à sua organização e ter acesso ao projeto para interagir com um projeto privado. Os projetos públicos estão visíveis para usuários que não estão conectados à sua organização.</p> </li> 
       <li> <p><strong>[!UICONTROL Version control]</strong>: selecione se deseja que o projeto use [!DNL Git] ou [!UICONTROL Team Foundation Version Control (TFCV)] para controle de versão.</p> </li> 
       <li> <p><strong>[!UICONTROL Work item process]</strong>: selecione o processo de trabalho que deseja usar para o projeto. As opções são [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration (CMMI)] e [!UICONTROL Agile].</p> <p>Para obter mais informações sobre [!DNL Azure DevOps] processos, consulte <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&amp;tabs=basic-process">Escolher um Processo</a> na Documentação [!DNL Azure DevOps].</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Work item]</strong> </p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Project]</strong>: selecione o projeto no qual deseja criar o item de trabalho.</p> </li> 
       <li> <p><strong>[!UICONTROL Work item type]</strong>: selecione o tipo de item de trabalho que deseja criar.</p> </li> 
       <li> <p><strong>[!UICONTROL Other fields]</strong>: nesses campos, insira o valor que você deseja que o item de trabalho tenha para uma determinada propriedade. Os campos disponíveis dependem do tipo de item de trabalho.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

Este módulo de ação baixa um anexo.

O módulo retorna o conteúdo do arquivo do anexo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment URL]</td> 
   <td> <p>Insira ou mapeie o URL do anexo que você deseja baixar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Link work items]

Esse módulo de ação vincula dois itens de trabalho e define a relação entre eles.

O módulo retorna a ID do item de trabalho principal e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td>Insira ou mapeie a ID do item de trabalho principal ao qual você deseja vincular outro item de trabalho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Linked work item ID]</td> 
   <td>Insira ou mapeie a ID do item de trabalho que você deseja vincular ao item de trabalho principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Link Type]</td> 
   <td> <p>Defina a relação entre os itens de trabalho que deseja vincular.</p> <p>Para obter mais informações, consulte <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">Referência de tipo de link</a> na Documentação [!UICONTROL Azure DevOps].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Insira ou mapeie o texto de um comentário. Isso é útil para explicar o raciocínio ou a intenção do link.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read record]

Este módulo de ação lê dados de um único registro em [!DNL Azure DevOps].

Especifique a ID do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecione se você deseja ler um projeto ou um item de trabalho</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong>: selecione o projeto que deseja ler.</p> </li> 
     <li> <p><strong>[!UICONTROL Work item]</strong>: selecione o projeto que contém o item de trabalho que você deseja ler e selecione o tipo de item de trabalho.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione as informações que deseja incluir no pacote de saída deste módulo. Os campos disponíveis dependem do tipo de item de trabalho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID do registro que deseja ler.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a work item]

Este módulo de ação atualiza um item de trabalho existente usando sua ID.

O módulo retorna a ID do item de trabalho atualizado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td>Selecione o projeto que contém o item de trabalho que você deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work Item Type]</td> 
   <td> <p>Selecione o tipo de item de trabalho que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other Fields]</td> 
   <td>Em cada um desses campos, insira o valor que você deseja que o item de trabalho tenha para uma determinada propriedade. Os campos disponíveis dependem do tipo de item de trabalho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td>Informe ou mapeie a ID do item de trabalho que você deseja atualizar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an attachment]

Este módulo de ação carrega um arquivo e o anexa a um item de trabalho.

O módulo retorna a ID do anexo e um URL de download para o anexo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project] </td> 
   <td> <p>Selecione o projeto no qual deseja fazer upload de um anexo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td> <p>Insira ou mapeie a ID do item de trabalho para o qual você deseja fazer upload de um anexo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Insira o texto de um comentário que deseja adicionar ao anexo carregado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file] </td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou insira ou mapeie o nome e o conteúdo do arquivo de origem.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

#### [!UICONTROL List work items]

Este módulo de ação recupera todos os itens de trabalho de um tipo específico em um projeto [!DNL Azure DevOps].

O módulo retorna a ID do item de trabalho principal e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Azure DevOps] ao [!DNL Workfront Fusion], consulte <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Azure DevOps] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td>Selecione o projeto do qual deseja recuperar itens de trabalho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item type]</td> 
   <td> <p>Selecione o tipo de item de trabalho que deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. Os campos disponíveis dependem do tipo de item de trabalho que você deseja recuperar. Você deve selecionar pelo menos uma propriedade.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Insira ou mapeie o número máximo de itens de trabalho que [!DNL Workfront Fusion] retorna durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>
