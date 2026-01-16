---
title: Módulos do Adobe Workfront
description: Você pode usar o conector do Adobe Workfront do Fusion para automatizar seus processos no Workfront. Se você tiver uma licença do Workfront Fusion for Work Automation and Integration, também poderá usá-la para se conectar a aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: ab12dbf0dbad25a8300eb1201fa3e0fde9148acc
workflow-type: tm+mt
source-wordcount: '7366'
ht-degree: 99%

---

# Módulos do Adobe Workfront

>[!IMPORTANT]
>
>Este artigo contém instruções para a nova versão do conector Workfront, lançada em 22 de outubro de 2025. Esse novo conector reflete as alterações feitas na API do Workfront.
>
>O novo conector é rotulado como “Workfront” e o conector disponível anteriormente é rotulado como “Workfront (legado)”.
>
>Recomendamos:
>
>* Usar o novo conector ao criar ou atualizar um cenário.
>* Atualizar os módulos existentes para o novo conector.
>
>O conector Workfront legado usa a API do Workfront versão 20, que está programada para ser descontinuada na versão 28.4 (abril de 2028). Os módulos no conector legado continuarão funcionando até essa data.
>
>Para obter instruções sobre como atualizar os módulos, consulte [Atualizar um módulo do Workfront para uma nova versão](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md) no artigo Atualizar um módulo para uma nova versão.
>
>Para obter informações sobre por que às vezes é necessário um novo conector, consulte [Visão geral de APIs no Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md).

Você pode usar o conector do Adobe Workfront do Fusion para automatizar seus processos no Workfront. Você também pode conectar o Workfront a outros aplicativos e serviços.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Conectar o Workfront ao Workfront Fusion

O conector Workfront usa o OAuth 2.0 para se conectar ao Workfront.

Você pode criar uma conexão com sua conta do Workfront diretamente de dentro de um módulo do Workfront Fusion.

* [Conectar-se ao Workfront usando a ID do cliente e o segredo do cliente](#connect-to-workfront-using-client-id-and-client-secret)
* [Conectar-se ao Workfront usando uma conexão de servidor para servidor](#connect-to-workfront-using-a-server-to-server-connection)

### Conectar-se ao Workfront usando a ID do cliente e o segredo do cliente

1. Em qualquer módulo do Adobe Workfront, clique em **Adicionar** ao lado do campo Conexão.
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
          <p>Selecione <b>Conexão de autenticação do Adobe Workfront</b>.</p>
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

   Se você não estiver conectado ao Workfront, será direcionado para uma tela de logon. Depois de fazer logon, é possível permitir a conexão.

>[!NOTE]
>
>* As conexões do OAuth 2.0 com a API do Workfront não dependem mais das chaves de API.
>* Para criar uma conexão com um ambiente de Sandbox do Workfront, crie um aplicativo OAuth2 nesse ambiente e use a ID do cliente e o segredo do cliente gerados por esse aplicativo em sua conexão.

### Conectar-se ao Workfront usando uma conexão de servidor para servidor

1. Em qualquer módulo do Adobe Workfront, clique em **Adicionar** ao lado do campo Conexão.
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

   Se você não estiver conectado ao Workfront, será direcionado para uma tela de logon. Depois de fazer logon, é possível permitir a conexão.

>[!NOTE]
>
>* As conexões do OAuth 2.0 com a API do Workfront não dependem mais das chaves de API.
>* Para criar uma conexão com um ambiente de Sandbox do Workfront, crie um aplicativo OAuth2 nesse ambiente e use a ID do cliente e o segredo do cliente gerados por esse aplicativo em sua conexão.

## Módulos do Workfront e seus campos

Ao configurar módulos do Workfront, o Workfront Fusion exibe os campos listados abaixo. Junto com esses campos, podem ser exibidos campos adicionais do Workfront, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Se você não vir os campos mais atualizados em um módulo do Workfront, isso pode ser devido a problemas de cache. Aguarde uma hora e tente novamente.
>* Os códigos de status HTTP 429 do Adobe Workfront não devem causar desativações, mas acionar uma pausa de execução curta no cenário.

* [Triggers](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Monitorar eventos]**

Esse módulo de acionador executa um cenário em tempo real quando objetos de um tipo específico são adicionados, atualizados ou excluídos no Workfront.

O módulo exibe todas as assinaturas de evento relacionadas ao webhook. Isso inclui assinaturas de evento criadas por meio do Fusion, bem como assinaturas de evento criadas diretamente pela API. Esta visualização de assinatura de evento não está disponível na versão herdada do módulo Eventos de observação.

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

1. Clique em **[!UICONTROL Adicionar]** à direita da caixa **Webhook**.

1. Configure o webhook na caixa **[!UICONTROL Adicionar um gancho]** que é exibida.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook name]</td> 
      <td>Insira um nome para o webhook</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connection]</td> 
      <td> <p>Para obter instruções sobre como conectar seu aplicativo do Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Type]</td> 
      <td>Selecione o tipo de registro do Workfront que o módulo deve monitorar.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL State]</td> 
      <td>Selecione se deseja monitorar o estado antigo ou novo.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Acione um cenário quando o registro é alterado <b>para</b> um valor específico.</p><p>Por exemplo, se o estado estiver definido como [!UICONTROL New State] e o filtro como [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress], o webhook acionará um cenário quando [!UICONTROL Status] for alterado para [!UICONTROL In Progress], independentemente do status anterior. </p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Acione um cenário quando o registro é alterado <b>de</b> um valor específico.</p><p>Por exemplo, se o estado estiver definido como [!UICONTROL Old State] e o filtro como [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress], o webhook acionará um cenário quando [!UICONTROL Status], atualmente definido como [!UICONTROL In Progress], for alterado para outro status. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>É possível definir filtros para monitorar apenas os registros que atendem aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que você deseja que o filtro avalie, bem como o operador e o valor que deseja que o filtro permita. Você pode usar mais de um filtro adicionando regras AND.</p> <p><b>OBSERVAÇÃO</b>: não é possível editar filtros em webhooks do Workfront. Para configurar filtros diferentes para assinaturas de eventos do Workfront, remova o webhook atual e crie um novo.</p> <p>Para obter mais informações sobre filtros de evento, consulte <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtros de assinatura de evento nos módulos do Workfront &gt; [!UICONTROL Watch Events]</a> neste artigo.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Excluir eventos criados por esta conexão</td> 
      <td>Habilite essa opção para excluir eventos criados ou atualizados usando o mesmo conector que esse módulo de acionador usa. Isso pode evitar situações em que um cenário pode acionar a si mesmo, fazendo com que ele se repita em um loop infinito.<p><b>OBSERVAÇÃO</b>: o tipo de registro Atribuição não inclui essa opção.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Origin]</td> 
      <td>
       <p>Escolha se deseja que o cenário monitore [!UICONTROL New Records Only], [!UICONTROL Updated Records Only], [!UICONTROL New and Updated Records] ou [!DNL Deleted Records Only].</p>
       <p><b>OBSERVAÇÃO</b>: se você escolher [!UICONTROL New and Updated Records], a criação do webhook criará duas assinaturas de evento (para o mesmo endereço do webhook).</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Depois que o webhook for criado, você poderá exibir o endereço do ponto de acesso para o qual os eventos são enviados.

Para obter mais informações, consulte a seção [Exemplos de conteúdo de evento](https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) no artigo “API de assinatura de evento” na documentação do Workfront.

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Campo de monitoramento]**

Esse módulo de acionador executa um cenário quando um campo especificado é atualizado. O módulo retorna o valor antigo e o novo do campo especificado. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo do Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro do Workfront que o módulo deve monitorar.</p> <p>Por exemplo, selecione [!UICONTROL Task] para começar a executar o cenário sempre que um campo de registro for atualizado em uma tarefa.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td>Selecione o campo que você deseja que o módulo monitore as atualizações. Esses campos refletem os campos que o administrador do Workfront configurou para rastreamento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td>Selecione os campos de objeto que você deseja incluir no pacote de saída deste módulo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Monitorar registros]**

Esse módulo de acionador executa um cenário quando objetos de um tipo específico são adicionados, atualizados ou ambos. O módulo retorna todos os campos padrão associados a um ou mais registros, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Na saída, o módulo indica se cada registro é novo ou atualizado.

Os registros que foram adicionados e atualizados desde a última vez que o cenário foi executado são retornados como novos registros.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Escolha se deseja que o cenário monitore [!UICONTROL New Records Only], [!UICONTROL Updated Records Only] ou [!UICONTROL New and Updated Records].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro do Workfront que o módulo deve monitorar.</p> <p>Por exemplo, se desejar iniciar o cenário sempre que um novo projeto for criado, selecione [!UICONTROL Project]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecione os campos que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reference]</td> 
   <td> <p>Selecione os campos de referência que você deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecione os campos de coleção que você deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optional Filter]</td> 
   <td> <p>(Avançado) Digite uma string de código da API para definir parâmetros ou códigos adicionais que refinarão os critérios. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++


### Ações

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL Converter objeto]**

Esse módulo de ação faz uma das seguintes conversões:

* Converter problema em projeto
* Converter problema em tarefa
* Converter tarefa em projeto

>[!NOTE]
>
>Desde julho de 2024, é possível incluir formulários personalizados ao converter um objeto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Object type]</td> 
   <td> <p>Selecione o tipo de objeto que deseja converter. Esse é o tipo que o objeto tem antes da conversão.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Convert to]</td> 
   <td>Selecione o objeto para o qual você deseja convertê-lo. Esse é o tipo que o objeto tem após a conversão.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;Object&gt; ID]</td> 
   <td> <p>Insira a ID do objeto. </p> <p>Observação: ao informar a ID de um objeto, é possível começar digitando o nome do objeto e, em seguida, selecioná-lo na lista. Em seguida, o módulo insere a ID adequada no campo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Template ID]</td> 
   <td> <p>Se você estiver convertendo em um projeto, selecione a ID do modelo que deseja usar para o projeto.</p> <p>Observação: ao informar a ID de um objeto, é possível começar digitando o nome do objeto e, em seguida, selecioná-lo na lista. Em seguida, o módulo insere a ID adequada no campo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Custom forms]</td> 
   <td>Selecione os formulários personalizados que deseja adicionar ao objeto recém-convertido e insira valores para os campos do formulário personalizado.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Options]</td> 
   <td> <p>Habilite as opções desejadas ao converter o objeto. As opções estão disponíveis dependendo do objeto do qual ou no qual você está fazendo a conversão.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copy native fields]</td> 
   <td> <p>Habilite esta opção para copiar quaisquer campos nativos do objeto original para o novo objeto.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copy custom forms]</td> 
   <td> <p>Habilite esta opção para copiar quaisquer campos nativos do objeto original para o novo objeto.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar um registro]** 

Este módulo de ação cria um objeto, como um projeto, uma tarefa ou um problema no Workfront, e permite adicionar um formulário personalizado ao novo objeto. O módulo permite selecionar quais dos campos do objeto estão disponíveis no módulo.

Especifique a ID do registro.

O módulo retorna a ID do registro e todos os campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Não se esqueça de fornecer o número mínimo de campos de entrada. Por exemplo, se você deseja criar um problema, é necessário fornecer uma ID de projeto principal válida no campo ID do projeto para indicar onde o problema deve residir no Workfront. Você pode usar o painel de mapeamento para mapear essas informações de outro módulo em seu cenário ou pode inseri-las manualmente digitando o nome e selecionando-o na lista.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo do Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro do Workfront que deseja que o módulo crie.</p> <p>Por exemplo, se você deseja criar um projeto, selecione [!UICONTROL Project] na lista suspensa.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Selecione os campos que deseja disponibilizar para entrada de dados. Dessa forma, você pode usar esses campos sem precisar percorrer os que não são necessários. Em seguida, você pode inserir ou mapear dados nesses campos.</p> <p>Para campos em formulários personalizados, use o campo <b>[!UICONTROL Attach Custom Form]</b>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Attach Custom Form]</td> 
   <td>Selecione quaisquer formulários personalizados que deseja adicionar ao novo objeto, selecione os campos para os quais deseja inserir valores e, em seguida, insira ou mapeie valores para esses campos.</td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Ao inserir a ID de um objeto, você pode começar a digitar o nome do objeto e, em seguida, selecioná-lo na lista. Em seguida, o módulo insere a ID adequada no campo.
>* Ao inserir o texto para um campo personalizado ou um objeto [!UICONTROL Nota] (Comentário ou resposta), você pode usar as tags HTML no campo [!UICONTROL Texto da nota] para criar rich text, como texto em negrito ou itálico.
>



>[!NOTE]
>
>Os usuários são criados nos status Desativado e Aprovação pendente. Se sua organização tiver migrado para o Adobe Admin Console e o selo Aprovação pendente não for removido em alguns minutos, você poderá aprovar o usuário.
>
>* **Resolver usuários individuais**
>
>      É possível resolver usuários individuais na lista Usuários.
>
>      1. Selecione um ou mais usuários na lista Usuários.
>      1. Clique no menu de três pontos no cabeçalho da lista.
>      1. Selecione **Aprovar**.
>      1. Após alguns minutos, atualize a página.
>
>* **Resolver usuários adicionados em um lote grande**
>
>   Para resolver os usuários que foram adicionados em um lote grande, é possível adicionar o lote de usuários diretamente ao Adobe Admin Console.
>
>   Para obter instruções, consulte [Gerenciar vários usuários | Upload em massa de CSV](https://helpx.adobe.com/br/enterprise/using/bulk-upload-users.html) na documentação da Adobe.

+++

<!--

+++ **[!UICONTROL Create Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Create a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module creates an object, such as a project, task, or issue in Workfront. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

Make sure you provide the minimum number of input fields. For example, if you want to create an issue, you need to provide a valid parent project ID in the Project ID field to indicate where the issue should live in Workfront. You can use the mapping panel to map this information from another module in your scenario, or you can enter it manually by typing in the name and then selecting it from the list.

This module does not attach custom forms when creating the object. To attach custom forms while creating an object, use the [!UICONTROL Create a record (attaching custom forms)] module.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to create.</p> <p>For example, if you want to create a Project, select [!UICONTROL Project] from the dropdown list.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL Chamada de API personalizada]**

Esse módulo de ação permite fazer uma chamada autenticada personalizada para a API do Workfront. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do Workfront.

O módulo retorna as seguintes informações:

* **[!UICONTROL Código do status]** (número): indica o sucesso ou a falha da sua solicitação HTTP. Esses são códigos padrão que você pode pesquisar na Internet.
* **[!UICONTROL Cabeçalhos]** (objeto): um contexto mais detalhado para o código de resposta/status que não está relacionado ao corpo da saída. Nem todos os cabeçalhos que aparecem em um cabeçalho de resposta são cabeçalhos de resposta, portanto, alguns podem não ser úteis para você.

  Os cabeçalhos de resposta dependem da solicitação HTTP escolhida ao configurar o módulo.

* **[!UICONTROL Corpo]** (objeto): dependendo da solicitação HTTP escolhida ao configurar o módulo, é possível receber alguns dados de volta. Esses dados, como os dados de uma solicitação GET, estão contidos neste objeto.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

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
   <td> <p>Insira um caminho relativo a <code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>.</p> </td> 
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
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Isso determina o tipo de conteúdo da solicitação.</p> <p>Por exemplo,<code> {"Content-type":"application/json"}</code></p> <p>Nota: se você estiver recebendo erros e for difícil determinar a origem deles, considere modificar os cabeçalhos com base na documentação do Workfront. Se sua chamada de API personalizada retornar um erro de solicitação HTTP 422, tente usar um cabeçalho <code>"Content-Type":"text/plain"</code>.</p> </td> 
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

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Excluir registro]**

Este módulo de ação exclui um objeto, por exemplo, projeto, tarefa ou problema no Workfront.

Especifique a ID do registro.

O módulo retorna a ID do registro e todos os campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Force delete]</td> 
   <td>Habilite essa opção para garantir que o registro seja excluído, mesmo que a interface do usuário do Workfront solicite a confirmação da exclusão.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Async delete]</td> 
   <td>Habilite essa opção para permitir que o módulo seja excluído de forma assíncrona.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>Insira a ID exclusiva do Workfront do registro que você deseja que o módulo exclua.</p> <p>Para obter a ID, abra o objeto do Workfront no navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>Selecione o tipo de registro do Workfront que você deseja que o módulo exclua.</td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>Recomendamos a configuração do cenário a seguir para evitar a possibilidade de registros não serem excluídos devido a operações assíncronas.
>
>1. Exclua o registro de forma síncrona.
>1. Adicione a manipulação de erros ao módulo Excluir registro para ignorar o erro causado pelo tempo-limite de 40 segundos.


+++

+++ **[!UICONTROL Baixar documento]**

Este módulo de ação baixa um documento do Workfront.

Especifique a ID do registro.

O módulo retorna o conteúdo do documento, o nome do arquivo, a extensão do arquivo e o tamanho do arquivo. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Document ID]</td> 
   <td> <p>Mapeie ou insira manualmente a ID exclusiva do Workfront do documento do qual você deseja que o módulo seja baixado.</p> <p>Para obter a ID, abra o objeto do Workfront no navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

### **Obter um URL de arquivo pré-assinado**

Esse módulo de ação obtém URLs de arquivos pré-assinados que podem ser usados posteriormente por outras APIs.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Document ID]</td> 
   <td> <p>Mapeie ou insira manualmente a ID exclusiva do Workfront do documento para o qual você deseja obter um URL pré-assinado.</p> <p>Para obter a ID, abra o objeto do Workfront no navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Time to URL expiration]</td> 
   <td> <p>Insira ou mapeie o número de minutos que esse URL existirá antes de expirar. O valor padrão é 1 minuto.</p><p>Para alterar esse valor, é necessário que esse parâmetro seja habilitado pela equipe do Workfront Fusion. Se não estiver habilitado, o valor permanecerá 1 minuto independentemente do número inserido.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++ **[!UICONTROL Ações diversas]**

Esse módulo de ação permite executar ações na API.

>[!NOTE]
>
>Desde julho de 2024, a ação `convertToProject` inclui o campo `copyCategories`. Quando definido como `TRUE`, todos os formulários personalizados serão incluídos no projeto no qual o problema é convertido.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo do Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro do Workfront com o qual você deseja que o módulo interaja.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Action]</td> 
   <td> <p>Selecione a ação que deseja que o módulo execute.</p> <p>Talvez seja necessário preencher campos adicionais, dependendo do [!UICONTROL Record Type] e da [!UICONTROL Action] escolhidos. Algumas combinações dessas duas configurações podem exigir apenas uma ID de registro, enquanto outras (como Projeto para o <strong>[!UICONTROL Record Type]</strong> e [!UICONTROL Attach Template] para <strong>[!UICONTROL Action]</strong>) requerem informações adicionais (como uma ID de objeto e uma ID de modelo).</p><p>Para opções disponíveis para algumas ações, consulte <a href="#misc-action-options" class="MCXref xref">Opções de ações diversas</a> neste artigo.</p> <p>Para obter detalhes sobre campos individuais, consulte a <a href="http://developer.workfront.com/">documentação para desenvolvedor do Workfront</a>. <p><strong>Observação</strong>: o site de documentação para desenvolvedor inclui informações somente até a API versão 14, mas ainda contém informações valiosas para chamadas de API. </p> 
    <ol> 
     <li value="1"> <p>Selecione o tipo de registro no painel de navegação esquerdo na página da documentação do desenvolvedor do Workfront. Os seguintes tipos têm suas próprias páginas:</p> 
      <ul> 
       <li> <p>[!UICONTROL Projects]</p> </li> 
       <li> <p>[!UICONTROL Tasks]</p> </li> 
       <li> <p>[!UICONTROL Issues]</p> </li> 
       <li> <p>[!UICONTROL Users]</p> </li> 
       <li> <p>[!UICONTROL Documents]</p> </li> 
      </ul> <p>Para todos os outros tipos de registro, selecione <b>[!UICONTROL Other objects and endpoints]</b> e localize o tipo de registro nas páginas classificadas alfabeticamente.</p> </li> 
     <li value="2"> <p>Na página do tipo de registro apropriado, pesquise a ação, usando Ctrl+F ou Cmd+F.</p> </li> 
     <li value="3"> <p>Exibir descrições para campos disponíveis sob a ação selecionada.</p> </li> 
    </ol> <p>Observação:  <p>Ao criar uma prova por meio do módulo [!UICONTROL Misc Action] do Workfront, a prática recomendada é criar uma prova sem nenhuma opção avançada e, em seguida, atualizar a prova usando a API SOAP [!DNL Workfront Proof].</p><p>Para obter mais informações sobre como criar uma prova com a API do Workfront (que este módulo usa), consulte <a href="https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Adicionar opções de prova avançadas ao criar uma prova por meio da API do Adobe Workfront</a></p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID exclusiva do Workfront do registro com o qual você deseja que o módulo interaja.<p>Para obter a ID, abra o objeto do Workfront no navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais é possível usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

#### Opções de ações diversas

##### Tarefa

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Ação</th> 
   <th>Opções</th> 
  </tr> 
  <tr> 
   <td>Copiar</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Limpa dados financeiros</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Limpa notificações de lembrete</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Mover</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Limpa dados financeiros</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Limpa notificações de lembrete</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### Problema

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Ação</th> 
   <th>Opções</th> 
  </tr> 
  <tr> 
   <td>Copiar</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearPermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Converter em tarefa</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Conservar o problema original e vincular sua resolução a essa tarefa</p></li>
   <li>preservePrimaryContact<p>Permitir o acesso do contato primário do problema a esta tarefa</p></li>
   <li>preserveCompletionDate<p>Manter a data de conclusão planejada do problema</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Converter em projeto</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Conservar o problema original e vincular sua resolução a essa tarefa</p></li>
   <li>preservePrimaryContact<p>Permitir o acesso do contato primário do problema a esta tarefa</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### Projeto

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Ação</th> 
   <th>Opções</th> 
  </tr> 
  <tr> 
   <td>Copiar</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Limpa dados financeiros</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Limpa notificações de lembrete</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Anexar modelo/Salvar como modelo</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverables<p>Limpa metas</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Limpa dados financeiros</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>Limpa propriedades da fila e configuração de problemas</p></li>
   <li>clearPredecessors</li>
   <li>clearRisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>Limpa notificações de lembrete</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Ler um registro]**

Esse módulo de ação recupera dados de um único registro.

Especifique a ID do registro. Você também pode especificar quais registros relacionados deseja que o módulo leia.

Por exemplo, se o registro que o módulo está lendo for um projeto, você pode especificar que deseja ler as tarefas do projeto.

O módulo retorna uma matriz de dados dos campos de saída especificados.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Para obter instruções sobre como conectar seu aplicativo do Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>

<td>Escolha o tipo de objeto do Workfront que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>

<td> <p>Selecione as informações que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Output Custom Form]</td>
     <td> <p>Selecione os formulários personalizados que deseja incluir no pacote de saída deste módulo e selecione os campos específicos desses formulários personalizados que deseja incluir na saída.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Selecione os campos de referência que deseja incluir na saída.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Selecione os campos de referência que deseja incluir na saída.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Insira a ID exclusiva do Workfront do registro que você deseja que o módulo leia.</p> <p>Para obter a ID, abra o objeto do Workfront no navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

<!--

+++ **[!UICONTROL Read a Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Read a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module retrieves data from a single record.

You specify the ID of the record. You can also specify which related records you want the module to read.

For example, if the record that the module is reading is a project, you can specify that you want the project's tasks read.

The module returns an array of data from the output fields you specified.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
  
   <td>Choose the Workfront object type that you want the module to read.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
  
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Enter the unique Workfront ID of the record that you want the module to read.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++

-->

+++ **Atualizar versão de conteúdo dos eventos**

A Workfront lançou recentemente uma nova versão de seu serviço de assinatura de eventos. A nova versão não é uma alteração na API do Workfront, mas uma alteração na funcionalidade de assinatura do evento. Este módulo de ação atualiza a versão de conteúdo do evento usada para este cenário.

Para obter mais informações sobre a nova versão de assinatura do evento, consulte [Controle de versão de assinatura do evento](https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) na documentação do Workfront

Para obter recursos sobre como preservar os cenários do Workfront Fusion durante a atualização da assinatura do evento, incluindo uma gravação de webinário, consulte [Preservação de seus cenários do Fusion durante a atualização da V2 de assinaturas do evento](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=pt).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Version]</td> 
   <td> Selecione a versão da assinatura do evento que deseja usar para este conteúdo. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **Atualizar um registro**


Esse módulo de ação atualiza um objeto, por exemplo, projeto, tarefa ou problema. O módulo permite selecionar quais dos campos do objeto estão disponíveis no módulo.

Especifique a ID do registro.

O módulo retorna a ID do objeto e todos os campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Insira a ID exclusiva do Workfront do registro que você deseja que o módulo atualize.</p> <p>Para obter a ID, abra o objeto do Workfront no navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Selecione o tipo de registro do Workfront que deseja que o módulo atualize.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Selecione os campos que deseja disponibilizar para entrada de dados. Dessa forma, você pode usar esses campos sem precisar percorrer os que não são necessários. Em seguida, você pode inserir ou mapear dados nesses campos.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>Selecione os formulários personalizados para os quais você deseja fornecer valores de campo no novo registro. Após selecionar o formulário, insira os dados dos campos nesse formulário.<p> Para fornecer valores de campo para um formulário que você está anexando neste módulo, inclua a ID do formulário personalizado na seção dos campos a serem mapeados.</td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
> Ao inserir o texto para um campo personalizado ou um objeto [!UICONTROL Nota] (Comentário ou resposta), você pode usar as tags HTML no campo [!UICONTROL Texto da nota] para criar um rich text, como texto em negrito ou itálico.


+++

<!--

+++ **[!UICONTROL Update Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Update a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module updates an object, such as a project, task, or issue. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  object and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Enter the unique Workfront ID of the record that you want the module to update.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to update.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need. You can then enter or map data into these fields.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL Fazer upload de documento]**

Esse módulo de ação faz o upload de um documento para um objeto do Workfront, por exemplo, projeto, tarefa ou problema. Esse módulo faz o upload do documento em partes, tornando o processo de upload mais suave para o Workfront.

Esse módulo pode lidar com arquivos maiores do que o módulo herdado e faz parte de uma implantação em fases para organizações com um pacote Ultimate Workfront.

Especifique o local do documento, o arquivo que deseja fazer upload e um novo nome opcional para o arquivo.

O módulo retorna a ID do documento e todos os campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o aplicativo Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Insira a ID exclusiva do Workfront do registro para o qual você deseja fazer upload do documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Selecione o tipo de registro do Workfront no qual você deseja que o módulo faça upload do documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Dependendo do tipo de registro relacionado, talvez seja necessário inserir ou mapear uma ID de pasta.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em [Tipos de objeto do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

<!--

+++ **[!UICONTROL Upload Document (Legacy)]**

This action module uploads a document to a Workfront object, such as a project, task, or issue. It uploads the entire document at once. 

You specify the location for the document, the file you want to upload, and an optional new name for the file.

The module returns the ID of the document and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Enter the unique Workfront ID of the record to which you want to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Select the type of Workfront record where you want the module to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Depending on the type of related record, you may need to enter or map a folder ID.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).


+++
-->

### Pesquisas

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Ler registros relacionados]**

Esse módulo de pesquisa lê registros que correspondem à consulta de pesquisa especificada em determinado objeto principal.

Você especifica quais campos deseja incluir na saída. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo do Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo do registro principal (objeto do Workfront) cujos registros associados você deseja ler.</p> <p>Veja uma lista dos tipos de objeto do Workfront para os quais você pode usar este módulo em <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">Tipos de objeto do Workfront disponíveis para cada módulo do Workfront</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Parent Record ID]</td> 
   <td> <p>Insira ou mapeie a ID do registro principal cujos registros associados você deseja ler.</p> <p>Para obter a ID, abra o objeto do Workfront no navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Selecione ou mapeie o tipo de registro filho que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Selecione as informações que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Pesquisa]**

Esse módulo de pesquisa procura registros em um objeto no Workfront que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo do Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro do Workfront que o módulo deve procurar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom forms list]</td> 
   <td> <p>Selecione pelo menos um formulário personalizado. Os campos desses formulários personalizados estarão disponíveis para a consulta de pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Selecione uma opção para especificar se você deseja que o módulo obtenha o primeiro resultado que corresponda aos seus critérios de pesquisa ou todos os resultados que correspondam a ele.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria fields]</td> 
   <td> <p>Selecione os campos que deseja usar para os critérios de pesquisa. Esses campos estarão disponíveis na lista suspensa Critérios de pesquisa.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Insira o campo pelo qual deseja pesquisar, o operador que deseja usar na consulta e o valor que está procurando no campo.</p> <p>Observação: não use <code>username </code>em seus critérios de pesquisa. A inclusão de <code>username </code>em uma consulta de API para o Workfront registra o usuário no Workfront e a pesquisa não será bem-sucedida.</p> <p>Observação: <code>In</code> e <code>NotIn</code>trabalham com matrizes. As entradas devem estar em formato de matriz.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Selecione os campos que deseja incluir na saída deste módulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Selecione os campos de referência que deseja incluir na pesquisa.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Selecione todas as coleções que deseja adicionar à pesquisa.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Pesquisa (legado)]**

>[!IMPORTANT]
>
>Esse módulo foi substituído pelo módulo Pesquisar registros. Recomendamos o uso desse módulo em novos cenários.
>Os cenários existentes que usam esse módulo continuarão funcionando conforme esperado. Esse módulo será removido do seletor de módulos em maio de 2025.

Esse módulo de pesquisa procura registros em um objeto no Workfront que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo do Workfront ao Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro do Workfront que o módulo deve procurar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Selecione uma opção para especificar se você deseja que o módulo obtenha o primeiro resultado que corresponda aos seus critérios de pesquisa ou todos os resultados que correspondam a ele.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria fields]</td> 
   <td> <p>Selecione os campos que deseja usar para os critérios de pesquisa. Esses campos estarão disponíveis na lista suspensa Critérios de pesquisa.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Insira o campo pelo qual deseja pesquisar, o operador que deseja usar na consulta e o valor que está procurando no campo.</p> <p>Observação: não use <code>username </code>em seus critérios de pesquisa. A inclusão de <code>username </code>em uma consulta de API para o Workfront registra o usuário no Workfront e a pesquisa não será bem-sucedida.</p> <p>Observação: <code>In</code> e <code>NotIn</code>trabalham com matrizes. As entradas devem estar em formato de matriz.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Selecione os campos que deseja incluir na saída deste módulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Selecione os campos de referência que deseja incluir na pesquisa.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Selecione todas as coleções que deseja adicionar à pesquisa.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## Tipos de objeto do Workfront disponíveis para cada módulo do Workfront

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**Tipos de objeto disponíveis para cada módulo de acionador do Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Watch Record]</th> 
   <th>[!UICONTROL Watch Field]</th> 
   <th>[!UICONTROL Watch Events]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processo de aprovação</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Atribuição</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Linha de base</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Registro de cobrança </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taxa de faturamento</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Empresa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Painel</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Pasta de documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Solicitação de documento</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Versão do documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Despesa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tipo de despesa</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Grupo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Hora</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tipo de hora</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problema</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iteração</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Função no trabalho</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Lançamento documentado</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Marco</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Caminho de marcos</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Nota</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tag de nota</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfólio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projeto</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Usuário de projeto</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aprovação da prova</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tempo reservado* </td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Relatório</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Risco</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo de risco</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aprovador da etapa</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tarefa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Equipe</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modelo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tarefa de modelo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Folha de horas</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Usuário</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Atualização</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tipos de objeto disponíveis para cada módulo de ação do Workfront**

>[!NOTE]
>
>O módulo [!UICONTROL Baixar documento] não está incluído nesta tabela porque os tipos de objeto do Workfront não fazem parte de sua configuração.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Create a record]</th> 
   <th>[!UICONTROL Update a record]</th> 
   <th>[!UICONTROL Delete a record]</th> 
   <th>[!UICONTROL Upload Document]</th> 
   <th>[!UICONTROL Read a record]</th> 
   <th>[!UICONTROL Custom API Call]</th> 
   <th>[!UICONTROL Misc Action]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processo de aprovação</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Atribuição</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Linha de base</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>Registro de cobrança</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taxa de faturamento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Empresa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Pasta de documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Versão do documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Taxa de câmbio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Despesa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tipo de despesa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Documento externo</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Grupo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Hora</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo de hora</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problema</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iteração</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Função no trabalho</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Lançamento documentado</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Marco</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Caminho de marcos</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Nota</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tag de nota</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfólio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projeto</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Usuário de projeto</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tempo reservado* </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risco</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo de risco</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aprovador da etapa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tarefa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Equipe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modelo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tarefa de modelo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Folha de horas</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Usuário</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Atualização</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tipos de objeto disponíveis para cada módulo de pesquisa do Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Search]</th> 
   <th>[!UICONTROL Read Related Records]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processo de aprovação</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Atribuição</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Registro de cobrança</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taxa de faturamento</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Empresa</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documento</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Pasta de documento</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Versão do documento</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Despesa</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo de despesa</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Grupo</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Hora</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo de hora</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problema</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iteração</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Função no trabalho</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Lançamento documentado</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Marco</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Caminho de marcos</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Nota</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tag de nota</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfólio</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programa</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Projeto</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Usuário de projeto</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tempo reservado* </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risco</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo de risco</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aprovador da etapa</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tarefa</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Equipe</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modelo</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tarefa de modelo</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Folha de horas</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Usuário</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Delegação de usuários</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

Recomendamos que você verifique novamente para garantir que isso funcione da maneira esperada.

+++

## Filtros de assinatura de evento no Workfront > módulos [!UICONTROL Monitorar eventos]

>[!NOTE]
>
>* É altamente recomendável usar filtros de assinatura de evento em seus módulos [!UICONTROL Monitorar eventos].
>
>* A Workfront lançou recentemente uma nova versão de seu serviço de assinatura de eventos. A nova versão não é uma alteração na API do Workfront, mas uma alteração na funcionalidade de assinatura do evento. Este módulo de ação atualiza a versão de conteúdo do evento usada para este cenário.
>
>   Para obter mais informações sobre a nova versão de assinatura do evento, consulte [Controle de versão de assinatura do evento](https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) na documentação do Workfront
>
>   Para obter recursos sobre como preservar os cenários do Workfront Fusion durante a atualização da assinatura do evento, incluindo uma gravação de webinário, consulte [Preservação de seus cenários do Fusion durante a atualização da V2 de assinaturas de evento (https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=pt)].

O módulo [!UICONTROL Monitorar eventos] do Workfront aciona cenários com base em um webhook que cria uma assinatura de evento na API do Workfront. A assinatura do evento é um conjunto de dados que determina quais eventos são enviados para o webhook. Por exemplo, se você configurar um módulo [!UICONTROL Monitorar eventos] que esteja observando problemas, a assinatura do evento enviará somente eventos relacionados a problemas.

Ao usar filtros de subscrição de evento, os usuários do Fusion podem criar assinaturas de evento que sejam mais adequadas para seus casos de uso. Por exemplo, você pode configurar uma assinatura de evento na API do Workfront para enviar somente problemas que estejam em um projeto específico para o webhook, garantindo que o módulo [!UICONTROL Monitorar eventos] acionará apenas problemas nesse projeto. A capacidade de criar acionadores mais restritos melhora o design do cenário ao reduzir o número de acionadores irrelevantes.

Isso é diferente de configurar um filtro no cenário do Workfront Fusion. Sem um filtro de assinatura de evento, o webhook recebe todos os eventos relacionados ao tipo de objeto selecionado. A maioria desses eventos será irrelevante para o cenário e deve ser retirada para que o cenário possa continuar.

Os seguintes operadores estão disponíveis no filtro Workfront > Monitorar eventos:

* Igual a
* Diferente de
* Maior que
* Menor que
* Maior ou igual a
* Menor ou igual a
* Contém
* Existe
   * Esse operador não requer um valor e o campo de valor está ausente.
* Não existe
   * Esse operador não requer um valor e o campo de valor está ausente.
* Alterado
   * Esse operador não requer um valor e o campo de valor está ausente.
   * Esse operador ignora o campo Estado.
   * Ao usar `Changed`, selecione **Somente eventos atualizados** no campo **Origem do registro**.

>[!IMPORTANT]
>
>Não é possível editar filtros em webhooks existentes do Workfront. Para configurar filtros diferentes para assinaturas de eventos do Workfront, remova o webhook atual e crie um novo.

>[!INFO]
>
>**Exemplo:** considere um cenário que processa novos problemas atribuídos a um usuário específico, Ana.
>
>### Filtrar eventos usando um filtro de assinatura de evento (recomendado)
>
>Usando o filtro de eventos, você pode configurar o webhook para acionar o cenário quando um problema é atribuído a Ana, assim que ele é criado. Ana tem a userID b378489d8f7cd3cee0539260720a84b7.
>
>![Filtro de eventos](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>Se forem criados 100 problemas em um dia, mas apenas dois deles forem atribuídos a Ana, o cenário será executado duas vezes.
>
>### Filtrar eventos dentro do cenário (não recomendado)
>
>Para filtrar eventos de modo que somente problemas atribuídos a Ana sejam processados, você pode criar um filtro após o módulo [!UICONTROL Monitorar eventos].
>
>![Sem filtro de evento](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>Se forem criados 100 problemas em um dia, mas apenas dois deles forem atribuídos a Ana, o cenário será executado 100 vezes. 98 das execuções parariam no filtro, mas o módulo de acionador ainda está consumindo dados e executando operações em todas as execuções.

Para obter mais informações sobre assinaturas de eventos do Workfront, consulte [Perguntas frequentes — Assinaturas de eventos](https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq).

Para obter mais informações sobre webhooks, consulte [Acionadores instantâneos (webhooks) no Adobe Workfront Fusion](/help/workfront-fusion/references/modules/webhooks-reference.md)

Para obter mais informações sobre filtros em cenários, consulte [Adicionar um filtro a um cenário](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
