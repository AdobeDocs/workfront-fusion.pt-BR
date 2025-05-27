---
title: Módulos do Adobe Workfront
description: Você pode usar o conector do Adobe Workfront Fusion Adobe Workfront para automatizar seus processos no Workfront. Se você tiver uma licença do Workfront Fusion for Work Automation and Integration, também poderá usá-la para se conectar a aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: 9dfab6838057a5852a2725dbfd398144ea2097dd
workflow-type: tm+mt
source-wordcount: '8061'
ht-degree: 2%

---

# Módulos do Adobe Workfront

Você pode usar o conector do Adobe Workfront Fusion Adobe Workfront para automatizar seus processos no Workfront. Você também pode conectar o Workfront a outros aplicativos e serviços.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Herdados: Qualquer um </p>
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


>[!NOTE]
>
>* Se sua organização usar o pacote de licenciamento herdado (com base em conectores), ela deverá ter uma licença do Workfront Fusion for Work Automation and Integration para se conectar a aplicativos e serviços de terceiros. O conector do Workfront não é contabilizado em relação ao número de aplicativos ativos disponíveis para sua organização. Todos os cenários, mesmo que usem apenas o aplicativo Workfront, contam com a contagem total de cenários de sua organização.

+++

## Conectar o Workfront ao Workfront Fusion

O conector do Workfront usa o OAuth 2.0 para se conectar ao Workfront.

Você pode criar uma conexão com sua conta do Workfront diretamente de dentro de um módulo do Workfront Fusion.

1. Em qualquer módulo do Adobe Workfront, clique em **Adicionar** ao lado do campo Conexão.
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
          <p>Insira um nome para a nova conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>
          <p>Selecione se estão se conectando a um ambiente de produção ou não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo de conexão]</td>
        <td>
          <p>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID do Cliente]</td>
        <td>Insira a ID do cliente do Workfront. Isso pode ser encontrado na área Aplicativos OAuth2 da área Configuração no Workfront. Abra o aplicativo específico ao qual você está se conectando para ver a ID do cliente.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira o segredo do cliente do Workfront. Isso pode ser encontrado na área Aplicativos OAuth2 da área Configuração no Workfront. Se você não tiver um Segredo do cliente para o aplicativo OAuth2 no Workfront, poderá gerar outro. Para obter instruções, consulte a documentação do Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL URL de Autenticação]</td>
        <td>Isso pode permanecer como o valor padrão, ou você pode inserir a URL da sua instância do Workfront, seguida por <code>/integrations/oauth2</code>. <p>Exemplo: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Prefixo de host]</td>
        <td>Na maioria dos casos, esse valor deve ser <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

   Se você não estiver conectado ao Workfront, será direcionado para uma tela de logon. Depois de fazer logon, é possível permitir a conexão.

>[!NOTE]
>
>* As conexões do OAuth 2.0 com a API do Workfront não dependem mais das chaves de API.
>* Para criar uma conexão com um ambiente de sandbox da Workfront, você deve criar um aplicativo OAuth2 nesse ambiente e usar a ID do cliente e o Segredo do cliente gerados por esse aplicativo em sua conexão.

## Módulos do Workfront e seus campos

Ao configurar módulos do Workfront, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Workfront podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Se você não vir os campos mais atualizados em um módulo do Workfront, isso pode ser devido a problemas de cache. Aguarde uma hora e tente novamente.
>* Os códigos de status HTTP 429 do Adobe Workfront não devem causar desativações, mas acionar uma pausa de execução curta no cenário.

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Assistir a Eventos]**

Esse módulo de acionador executa um cenário em tempo real quando objetos de um tipo específico são adicionados, atualizados ou excluídos no Workfront

O módulo retorna quaisquer campos padrão associados ao registro, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

1. Clique em **[!UICONTROL Adicionar]** à direita da caixa **Webhook**.

1. Configure o webhook na caixa **[!UICONTROL Adicionar um gancho]** que é exibida.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Nome do Webhook]</td> 
      <td>Insira um nome para o webhook</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Conexão]</td> 
      <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Tipo de Registro]</td> 
      <td>Selecione o tipo de registro Workfront que você deseja que o módulo assista.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Estado]</td> 
      <td>Selecione se deseja observar o estado antigo ou o novo estado.<ul><li><p><b>[!UICONTROL Novo estado]</b></p><p>Acione um cenário quando o registro alterar <b>para</b> um determinado valor.</p><p>Por exemplo, se o estado estiver definido como [!UICONTROL Novo Estado] e o filtro estiver definido como [!UICONTROL Status] [!UICONTROL Igual a] [!UICONTROL Em Andamento], o webhook acionará um cenário quando o [!UICONTROL Status] for alterado para [!UICONTROL Em Andamento], independentemente do status anterior. </p></li><li><p><b>[!UICONTROL Estado antigo]</b></p><p>Acione um cenário quando o registro alterar <b>de</b> um determinado valor.</p><p>Por exemplo, se o estado estiver definido como [!UICONTROL Estado Antigo] e o filtro estiver definido como [!UICONTROL Status] [!UICONTROL Igual a] [!UICONTROL Em Andamento], o webhook acionará um cenário quando um [!UICONTROL Status] atual [!UICONTROL Em Andamento] for alterado para outro status. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Eventos filtros]</p> </td> 
      <td> <p>É possível definir filtros para observar apenas os registros que atendem aos critérios selecionados.</p> <p>Para cada filtro, insira o campo que deseja que o filtro avalie, o operador e o valor que deseja que o filtro permita. Você pode usar mais de um filtro adicionando regras AND.</p> <p><b>OBSERVAÇÃO</b>: não é possível editar filtros em webhooks existentes do Workfront. Para configurar diferentes filtros para assinaturas de eventos do Workfront, remova o webhook atual e crie um novo.</p> <p>Para obter mais informações sobre filtros de evento, consulte <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtros de assinatura de evento nos módulos do Workfront &gt; [!UICONTROL Watch Events]</a> neste artigo.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Excluir eventos feitos por esta conexão</td> 
      <td>Habilite essa opção para excluir eventos criados ou atualizados usando o mesmo conector que esse módulo de acionador usa. Isso pode evitar situações em que um cenário pode ser acionado, fazendo com que ele se repita em um loop infinito.<p><b>OBSERVAÇÃO</b>: o tipo de registro Assignment não inclui essa opção.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Origem do Registro]</td> 
      <td>
       <p>Escolha se deseja que o cenário observe [!UICONTROL Somente Novos Registros], [!UICONTROL Somente Registros Atualizados], [!UICONTROL Registros Novos e Atualizados] ou [!DNL Deleted Records Only].</p>
       <p><b>OBSERVAÇÃO</b>: se você escolher [!UICONTROL Registros novos e atualizados], a criação do webhook criará duas assinaturas de evento (para o mesmo endereço do webhook).</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Depois que o webhook for criado, você poderá exibir o endereço do endpoint para o qual os eventos são enviados.

Para obter mais informações, consulte a seção [Exemplos de cargas de evento](https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) no artigo API de assinatura de evento na documentação do Workfront.

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Campo de observação]**

Esse módulo de acionamento executa um cenário quando um campo especificado é atualizado. O módulo retorna o valor antigo e o novo do campo especificado. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro Workfront que você deseja que o módulo assista.</p> <p>Por exemplo, selecione [!UICONTROL Tarefa] se desejar começar a executar o cenário sempre que um campo de registro for atualizado em uma tarefa.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campo]</td> 
   <td>Selecione o campo que você deseja que o módulo veja por atualizações. Esses campos refletem os campos que o administrador do Workfront configurou para rastreamento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Saídas]</td> 
   <td>Selecione os campos de objeto que você deseja incluir no pacote de saída deste módulo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Assistir ao Registro]**

Esse módulo de acionamento executa um cenário quando objetos de um tipo específico são adicionados, atualizados ou ambos. O módulo retorna todos os campos padrão associados ao registro ou aos registros, juntamente com quaisquer campos e valores personalizados que a conexão acesse. Você pode mapear essas informações em módulos subsequentes no cenário.

Na saída, o módulo indica se cada registro é novo ou atualizado.

Os registros que foram adicionados e atualizados desde a última vez que o cenário foi executado são retornados como novos registros.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Escolha se deseja que o cenário observe [!UICONTROL Somente Novos Registros], [!UICONTROL Somente Registros Atualizados] ou [!UICONTROL Registros Novos e Atualizados].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro Workfront que você deseja que o módulo assista.</p> <p>Por exemplo, se você deseja iniciar o cenário sempre que um novo projeto for criado, selecione [!UICONTROL Projeto]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td> <p>Selecione os campos que você deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Referência]</td> 
   <td> <p>Selecione os campos de referência que você deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td> <p>Selecione os campos de coleção que você deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro Opcional]</td> 
   <td> <p>(Avançado) Digite uma string de código da API para definir parâmetros ou códigos adicionais que refinarão seus critérios. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

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

* Converter Problema em Projeto
* Converter problema em tarefa
* Converter Tarefa em Projeto

>[!NOTE]
>
>A partir de julho de 2024, formulários personalizados poderão ser incluídos ao converter um objeto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo de objeto]</td> 
   <td> <p>Selecione o tipo de objeto que deseja converter. Esse é o tipo que o objeto tem antes da conversão.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Converter em]</td> 
   <td>Selecione o objeto para o qual você deseja convertê-lo. Esse é o tipo que o objeto tem após a conversão.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;Objeto&gt; ID]</td> 
   <td> <p>Insira a ID do objeto. </p> <p>Observação: Ao informar o ID de um objeto, você pode começar a digitar o nome do objeto e, em seguida, selecioná-lo na lista. O módulo insere a ID apropriada no campo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID de Modelo]</td> 
   <td> <p>Se estiver convertendo em um projeto, selecione a ID do modelo que deseja usar para o projeto.</p> <p>Observação: Ao informar o ID de um objeto, você pode começar a digitar o nome do objeto e, em seguida, selecioná-lo na lista. O módulo insere a ID apropriada no campo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Formulários personalizados]</td> 
   <td>Selecione os formulários personalizados que deseja adicionar ao objeto recém-convertido e insira valores para os campos do formulário personalizado.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Opções]</td> 
   <td> <p>Ative as opções desejadas ao converter o objeto. As opções estão disponíveis dependendo do objeto para o qual você está convertendo ou a partir do.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copiar campos nativos]</td> 
   <td> <p>Ative esta opção para copiar quaisquer campos nativos do objeto original para o novo objeto.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copiar formulários personalizados]</td> 
   <td> <p>Ative esta opção para copiar quaisquer campos nativos do objeto original para o novo objeto.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar um registro]**

Esse módulo de ação cria um objeto, como um projeto, tarefa ou problema no Workfront, e permite adicionar um formulário personalizado ao novo objeto. O módulo permite selecionar quais dos campos do objeto estão disponíveis no módulo.

Especifique a ID do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Forneça o número mínimo de campos de entrada. Por exemplo, se você deseja criar um problema, é necessário fornecer uma ID de projeto principal válida no campo ID do projeto para indicar onde o problema deve residir na Workfront. Você pode usar o painel de mapeamento para mapear essas informações de outro módulo em seu cenário ou pode inseri-las manualmente digitando o nome e selecionando-o na lista.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro Workfront que deseja que o módulo crie.</p> <p>Por exemplo, se você deseja criar um projeto, selecione [!UICONTROL Project] na lista suspensa.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Selecionar campos a serem mapeados]</td> 
   <td> <p>Selecione os campos que deseja disponibilizar para entrada de dados. Isso permite usar esses campos sem precisar percorrer os que não são necessários. Em seguida, você pode inserir ou mapear dados nesses campos.</p> <p>Para campos em formulários personalizados, use o campo <b>[!UICONTROL Anexar Formulário Personalizado]</b>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Anexar Formulário Personalizado]</td> 
   <td>Selecione quaisquer formulários personalizados que deseja adicionar ao novo objeto e, em seguida, insira ou mapeie valores para esses campos.</td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Ao inserir a ID de um objeto, você pode começar a digitar o nome do objeto e, em seguida, selecioná-lo na lista. O módulo insere a ID apropriada no campo.
>* Ao inserir o texto para um campo personalizado ou um objeto [!UICONTROL Nota] (Comentário ou resposta), você pode usar as marcas HTML no campo [!UICONTROL Texto da Nota] para criar rich text, como negrito ou itálico.
>



>[!NOTE]
>
>Os usuários são criados com os status Desativado e Aprovação pendente. Se sua organização tiver migrado para a Adobe Admin Console e o selo Aprovação pendente não for removido em alguns minutos, você poderá aprovar o usuário.
>
>* **Resolver usuários individuais**
>
>      Você pode resolver usuários individuais na lista Usuários.
>
>      1. Selecione o usuário ou usuários na lista Usuários.
>      1. Clique no menu de três pontos no cabeçalho da lista.
>      1. Selecione **Aprovar**.
>      1. Após alguns minutos, atualize a página.
>
>* **Resolver usuários adicionados em um lote grande**
>
>   Para resolver usuários que foram adicionados em um lote grande, é possível adicionar o lote de usuários diretamente ao Adobe Admin Console.
>
>   Para obter instruções, consulte [Gerenciar vários usuários | Upload em massa de CSV](https://helpx.adobe.com/br/enterprise/using/bulk-upload-users.html) na documentação do Adobe.

+++

+++ **[!UICONTROL Criar Registro (Herdado)]**

>[!IMPORTANT]
>
>Esse módulo foi substituído pelo módulo Criar um registro. Recomendamos o uso desse módulo em novos cenários.
>Os cenários existentes que usam esse módulo continuarão a funcionar conforme esperado. Este módulo será removido do seletor de módulos em maio de 2025.

Esse módulo de ação cria um objeto, como um projeto, tarefa ou problema no Workfront. O módulo permite selecionar quais dos campos do objeto estão disponíveis no módulo.

Especifique a ID do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Forneça o número mínimo de campos de entrada. Por exemplo, se você deseja criar um problema, é necessário fornecer uma ID de projeto principal válida no campo ID do projeto para indicar onde o problema deve residir na Workfront. Você pode usar o painel de mapeamento para mapear essas informações de outro módulo em seu cenário ou pode inseri-las manualmente digitando o nome e selecionando-o na lista.

Esse módulo não anexa formulários personalizados ao criar o objeto. Para anexar formulários personalizados ao criar um objeto, use o módulo [!UICONTROL Criar um registro (anexando formulários personalizados)].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro Workfront que deseja que o módulo crie.</p> <p>Por exemplo, se você deseja criar um projeto, selecione [!UICONTROL Project] na lista suspensa.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Selecionar campos a serem mapeados]</td> 
   <td>Selecione os campos que deseja disponibilizar para entrada de dados. Isso permite usar esses campos sem precisar percorrer os que não são necessários.</td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Ao inserir a ID de um objeto, você pode começar a digitar o nome do objeto e, em seguida, selecioná-lo na lista. O módulo insere a ID apropriada no campo.
>* Ao inserir o texto para um campo personalizado ou um objeto [!UICONTROL Nota] (Comentário ou resposta), você pode usar as marcas HTML no campo [!UICONTROL Texto da Nota] para criar rich text, como negrito ou itálico.

+++

+++ **[!UICONTROL Chamada de API personalizada]**

Esse módulo de ação permite fazer uma chamada autenticada personalizada para a API do Workfront. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do Workfront.

O módulo retorna as seguintes informações:

* **[!UICONTROL Código de Status]** (número): indica o sucesso ou a falha da sua solicitação HTTP. Esses são códigos padrão que você pode pesquisar na Internet.
* **[!UICONTROL Cabeçalhos]** (objeto): um contexto mais detalhado para o código de resposta/status que não está relacionado ao corpo de saída. Nem todos os cabeçalhos que aparecem em um cabeçalho de resposta são cabeçalhos de resposta, portanto, alguns podem não ser úteis para você.

  Os cabeçalhos de resposta dependem da solicitação HTTP escolhida ao configurar o módulo.

* **[!UICONTROL Corpo]** (objeto): dependendo da solicitação HTTP escolhida ao configurar o módulo, você poderá receber alguns dados de volta. Esses dados, como os dados de uma solicitação GET, estão contidos neste objeto.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Insira um caminho relativo a <code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Versão da API]</td> 
   <td>Selecione a versão da API do Workfront que você deseja que o módulo use.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP no Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Isso determina o tipo de conteúdo da solicitação.</p> <p>Por exemplo,<code> {"Content-type":"application/json"}</code></p> <p>Observação: se você estiver recebendo erros e for difícil determinar sua origem, considere modificar cabeçalhos com base na documentação do Workfront. Se sua Chamada de API personalizada retornar um Erro de solicitação HTTP 422, tente usar um cabeçalho <code>"Content-Type":"text/plain"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> <p>Dica: recomendamos que você envie informações por meio do corpo JSON, em vez de como parâmetros de consulta.</p> </td> 
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

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Excluir Registro]**

Esse módulo de ação exclui um objeto, como um projeto, tarefa ou problema no Workfront.

Especifique a ID do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Forçar exclusão]</td> 
   <td>Ative essa opção para garantir que o registro seja excluído, mesmo que a interface do usuário do Workfront solicite a confirmação da exclusão.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Exclusão assíncrona]</td> 
   <td>Ative essa opção para permitir que o módulo seja excluído de forma assíncrona.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>Insira o identificador exclusivo do Workfront do registro que você deseja que o módulo exclua.</p> <p>Para obter a ID, abra o objeto do Workfront em seu navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro]</td> 
   <td>Selecione o tipo de registro Workfront que você deseja que o módulo exclua.</td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>Recomendamos a configuração do cenário a seguir para evitar a possibilidade de registros não serem excluídos devido a operações assíncronas.
>
>1. Excluir o registro de forma síncrona.
>1. Adicione a manipulação de erros ao módulo Delete Record para Ignorar o erro causado pelo tempo limite de 40 segundos.


+++

+++ **[!UICONTROL Baixar Documento]**

Este módulo de ação baixa um documento do Workfront.

Especifique a ID do registro.

O módulo retorna o conteúdo do documento, o nome do arquivo, a extensão do arquivo e o tamanho do arquivo. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Documento]</td> 
   <td> <p>Mapeie ou insira manualmente a ID exclusiva do Workfront do documento do qual você deseja que o módulo seja baixado.</p> <p>Para obter a ID, abra o objeto do Workfront em seu navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Ações diversas]**

Esse módulo de ação permite executar ações na API.

>[!NOTE]
>
>A partir de julho de 2024, a ação `convertToProject` inclui o campo `copyCategories`. Quando definido como `TRUE`, todos os formulários personalizados serão incluídos no projeto para o qual o problema é convertido.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro do Workfront com o qual você deseja que o módulo interaja.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Ação]</td> 
   <td> <p>Selecione a ação que deseja que o módulo execute.</p> <p>Talvez seja necessário preencher campos adicionais, dependendo do [!UICONTROL Record Type] e da [!UICONTROL Action] escolhidos. Algumas combinações dessas duas configurações podem exigir apenas uma ID de registro, enquanto outras (como Projeto para o <strong>[!UICONTROL Tipo de Registro]</strong> e [!UICONTROL Anexar Modelo] para a <strong>[!UICONTROL Ação]</strong>) exigem informações adicionais (como uma ID de Objeto e uma ID de Modelo).</p><p>Para opções disponíveis para algumas ações, consulte <a href="#misc-action-options" class="MCXref xref">Opções de ações diversas</a> neste artigo.</p> <p>Para obter detalhes sobre campos individuais, consulte a <a href="http://developer.workfront.com/">documentação para desenvolvedor do Workfront</a>. <p><strong>Observação</strong>: o site de documentação do desenvolvedor inclui informações somente da API versão 14, mas ainda contém informações valiosas para chamadas de API. </p> 
    <ol> 
     <li value="1"> <p>Selecione o tipo de registro na navegação à esquerda na página da documentação do desenvolvedor do Workfront. Os seguintes tipos têm suas próprias páginas:</p> 
      <ul> 
       <li> <p>[!UICONTROL Projetos]</p> </li> 
       <li> <p>[!UICONTROL Tarefas]</p> </li> 
       <li> <p>[!UICONTROL Problemas]</p> </li> 
       <li> <p>[!UICONTROL Usuários]</p> </li> 
       <li> <p>[!UICONTROL Documentos]</p> </li> 
      </ul> <p>Para todos os outros tipos de registro, selecione <b>[!UICONTROL Outros objetos e pontos de extremidade]</b> e localize o tipo de registro nas páginas classificadas alfabeticamente.</p> </li> 
     <li value="2"> <p>Na página do tipo de registro apropriado, pesquise (Ctrl-F ou Cmd-F) a ação.</p> </li> 
     <li value="3"> <p>Exibir descrições para campos disponíveis sob a ação selecionada.</p> </li> 
    </ol> <p>Nota:  <p>Ao criar uma prova por meio do módulo [!UICONTROL Misc Action] da Workfront, a prática recomendada é criar uma prova sem nenhuma opção avançada e, em seguida, atualizar a prova usando a API do SOAP [!DNL Workfront Proof].</p><p>Para obter mais informações sobre como criar uma prova com a API Workfront (que este módulo usa), consulte <a href="https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Adicionar opções de prova avançada ao criar uma prova por meio da API Adobe Workfront</a></p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a Workfront ID exclusiva do registro com o qual você deseja que o módulo interaja.<p>Para obter a ID, abra o objeto do Workfront em seu navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

#### Opções de ação diversas

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
   <li>clearTimedNotifications<p>Limpa as notificações de lembrete</p></li>
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
   <li>clearTimedNotifications<p>Limpa as notificações de lembrete</p></li>
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
   <li>preserveIssue<p>Conservar o problema original e vincular a sua resolução a esta tarefa</p></li>
   <li>preservePrimaryContact<p>Permitir que o contato primário do problema acesse esta tarefa</p></li>
   <li>preserveCompletionDate<p>Manter a data de conclusão planejada do problema</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Converter em projeto</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Conservar o problema original e vincular a sua resolução a esta tarefa</p></li>
   <li>preservePrimaryContact<p>Permitir que o contato primário do problema acesse esta tarefa</p></li>
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
   <li>clearTimedNotifications<p>Limpa as notificações de lembrete</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Anexar modelo / Salvar como modelo</td> 
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
   <li>clearIssueSetup<p>Limpa as propriedades da fila e a configuração de problemas</p></li>
   <li>clearPredecessors</li>
   <li>clearRisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>Limpa as notificações de lembrete</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Ler um Registro]**

Este módulo de ação recupera dados de um único registro.

Especifique a ID do registro. Você também pode especificar quais registros relacionados deseja que o módulo leia.

Por exemplo, se o registro que o módulo está lendo for um projeto, você pode especificar que deseja ler as tarefas do projeto.

O módulo retorna uma matriz de dados dos campos de saída especificados.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Conexão]</td>
    <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Tipo de Registro]</td>

<td>Escolha o tipo de objeto do Workfront que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Saídas]</td>

<td> <p>Selecione as informações que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Formulário Personalizado de Saída]</td>
     <td> <p>Selecione os formulários personalizados que deseja incluir no pacote de saída para este módulo e selecione os campos específicos desses formulários personalizados que deseja incluir na saída.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Referências]</td>
   <td>Selecione os campos de referência que deseja incluir na saída.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Coleções]</td>
   <td>Selecione os campos de referência que deseja incluir na saída.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Insira o identificador exclusivo do Workfront do registro que você deseja que o módulo leia.</p> <p>Para obter a ID, abra o objeto do Workfront em seu navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Ler um Registro (Herdado)]**

>[!IMPORTANT]
>
>Esse módulo foi substituído pelo módulo Ler um registro. Recomendamos o uso desse módulo em novos cenários.
>Os cenários existentes que usam esse módulo continuarão a funcionar conforme esperado. Este módulo será removido do seletor de módulos em maio de 2025.

Este módulo de ação recupera dados de um único registro.

Especifique a ID do registro. Você também pode especificar quais registros relacionados deseja que o módulo leia.

Por exemplo, se o registro que o módulo está lendo for um projeto, você pode especificar que deseja ler as tarefas do projeto.

O módulo retorna uma matriz de dados dos campos de saída especificados.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Conexão]</td>
    <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Tipo de Registro]</td>

<td>Escolha o tipo de objeto do Workfront que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Saídas]</td>

<td> <p>Selecione as informações que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Referências]</td>
   <td>Selecione os campos de referência que deseja incluir na saída.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Coleções]</td>
   <td>Selecione os campos de referência que deseja incluir na saída.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Insira o identificador exclusivo do Workfront do registro que você deseja que o módulo leia.</p> <p>Para obter a ID, abra o objeto do Workfront em seu navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **Atualizar Versão da Carga dos Eventos**

A Workfront lançou recentemente uma nova versão de seu serviço de assinatura de eventos. A nova versão não é uma alteração na API do Workfront, mas uma alteração na funcionalidade de assinatura do evento. Este módulo de ação atualiza a versão de carga útil do evento usada para este cenário.

Para obter mais informações sobre a nova versão de assinatura de eventos, consulte [Versão de assinatura de eventos](https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) na documentação da Workfront

Para obter recursos sobre como preservar seus cenários do Workfront Fusion durante a atualização da assinatura do evento, incluindo uma gravação de webinário, consulte [Preservando seus cenários do Fusion Durante a Atualização da V2 de Assinaturas do Evento](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=pt).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Versão]</td> 
   <td> Selecione a versão da assinatura de evento que deseja usar para essa carga. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **Atualizar um registro**


Esse módulo de ação atualiza um objeto, como um projeto, tarefa ou problema. O módulo permite selecionar quais dos campos do objeto estão disponíveis no módulo.

Especifique a ID do registro.

O módulo retorna a ID do objeto e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Insira o identificador exclusivo do Workfront do registro que você deseja que o módulo atualize.</p> <p>Para obter a ID, abra o objeto do Workfront em seu navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Selecione o tipo de registro Workfront que você deseja que o módulo atualize.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Selecione os campos que deseja disponibilizar para entrada de dados. Isso permite usar esses campos sem precisar percorrer os que não são necessários. Em seguida, você pode inserir ou mapear dados nesses campos.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>Selecione os formulários personalizados que deseja fornecer valores de campo para o novo registro. Após selecionar o formulário, insira os dados dos campos nele contidos.<p> Para fornecer valores de campo para um formulário que você está anexando neste módulo, inclua a ID de formulário personalizada na seção campos a mapear.</td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
> Ao inserir o texto para um campo personalizado ou um objeto [!UICONTROL Nota] (Comentário ou resposta), você pode usar as marcas HTML no campo [!UICONTROL Texto da Nota] para criar rich text, como negrito ou itálico.


+++

+++ **[!UICONTROL Atualizar Registro (Herdado)]**

>[!IMPORTANT]
>
>Este módulo foi substituído pelo módulo Atualizar um registro. Recomendamos o uso desse módulo em novos cenários.
>Os cenários existentes que usam esse módulo continuarão a funcionar conforme esperado. Este módulo será removido do seletor de módulos em maio de 2025.

Esse módulo de ação atualiza um objeto, como um projeto, tarefa ou problema. O módulo permite selecionar quais dos campos do objeto estão disponíveis no módulo.

Especifique a ID do registro.

O módulo retorna a ID do objeto e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Insira o identificador exclusivo do Workfront do registro que você deseja que o módulo atualize.</p> <p>Para obter a ID, abra o objeto do Workfront em seu navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Selecione o tipo de registro Workfront que você deseja que o módulo atualize.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Selecione os campos que deseja disponibilizar para entrada de dados. Isso permite usar esses campos sem precisar percorrer os que não são necessários. Em seguida, você pode inserir ou mapear dados nesses campos.</td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Ao inserir a ID de um objeto, você pode começar a digitar o nome do objeto e, em seguida, selecioná-lo na lista. O módulo insere a ID apropriada no campo.
>* Ao inserir o texto para um campo personalizado ou um objeto [!UICONTROL Nota] (Comentário ou resposta), você pode usar as marcas HTML no campo [!UICONTROL Texto da Nota] para criar rich text, como negrito ou itálico.

+++

+++ **[!UICONTROL Carregar documento]**

Esse módulo de ação faz upload de um documento para um objeto do Workfront, como um projeto, tarefa ou problema. Esse módulo carrega o documento em partes, o que torna o processo de upload mais suave para o Workfront.

Esse módulo pode lidar com arquivos maiores do que o módulo herdado e faz parte de uma implantação em fases para organizações com um pacote Ultimate Workfront.

Especifique o local do documento, o arquivo que deseja fazer upload e um novo nome opcional para o arquivo.

O módulo retorna a ID do documento e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID de Registro Relacionado]</td> 
   <td>Informe o Workfront ID exclusivo do registro para o qual você deseja fazer upload do documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro Relacionado]</td> 
   <td>Selecione o tipo de registro Workfront no qual você deseja que o módulo faça upload do documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID da Pasta]</td> 
   <td>Dependendo do tipo de registro relacionado, talvez seja necessário inserir ou mapear uma ID de pasta.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Carregar Documento (Herdado)]**

Esse módulo de ação faz upload de um documento para um objeto do Workfront, como um projeto, tarefa ou problema. Ele carrega o documento inteiro de uma só vez.

Especifique o local do documento, o arquivo que deseja fazer upload e um novo nome opcional para o arquivo.

O módulo retorna a ID do documento e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID de Registro Relacionado]</td> 
   <td>Informe o Workfront ID exclusivo do registro para o qual você deseja fazer upload do documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro Relacionado]</td> 
   <td>Selecione o tipo de registro Workfront no qual você deseja que o módulo faça upload do documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID da Pasta]</td> 
   <td>Dependendo do tipo de registro relacionado, talvez seja necessário inserir ou mapear uma ID de pasta.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

Veja uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em [tipos de objetos do Workfront disponíveis para cada módulo do Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

### Pesquisas

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Ler Registros Relacionados]**

Esse módulo de pesquisa lê registros que correspondem à consulta de pesquisa especificada em um determinado objeto pai.

Você especifica quais campos deseja incluir na saída. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo do registro pai (objeto Workfront) cujos registros associados você deseja ler.</p> <p>Consulte uma lista dos tipos de objetos do Workfront para os quais você pode usar este módulo em <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">Tipos de objetos do Workfront disponíveis para cada módulo do Workfront</a> neste artigo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID de Registro Pai]</td> 
   <td> <p>Informe ou mapeie o ID do registro-pai cujos registros associados você deseja ler.</p> <p>Para obter a ID, abra o objeto do Workfront em seu navegador e copie o texto no final do URL após "ID=". Por exemplo: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Coleções]</td> 
   <td>Selecione ou mapeie o tipo de registro filho que você deseja que o módulo leia.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Saídas]</td> 
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
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro Workfront que você deseja que o módulo procure.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Lista de formulários personalizados]</td> 
   <td> <p>Selecione pelo menos um formulário personalizado. Os campos desses formulários personalizados estarão disponíveis para a consulta de pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conjunto de Resultados]</td> 
   <td>Selecione uma opção para especificar se você deseja que o módulo obtenha o primeiro resultado que corresponda aos seus critérios de pesquisa ou todos os resultados que correspondam a ele.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Máximo]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar campos de critérios]</td> 
   <td> <p>Selecione os campos que deseja usar com os critérios de pesquisa. Esses campos estarão disponíveis na lista suspensa Search criteria.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar critérios]</td> 
   <td> <p>Digite o campo pelo qual deseja pesquisar, o operador que deseja usar na consulta e o valor que está procurando no campo.</p> <p>Observação: não use <code>username </code> nos seus critérios de pesquisa. A inclusão de <code>username </code> em uma consulta de API para o Workfront registra o usuário no Workfront e a pesquisa não será bem-sucedida.</p> <p>Observação: <code>In</code> e <code>NotIn</code>funcionam com matrizes. As entradas devem estar em formato de matriz.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Saídas]</td> 
   <td> <p>Selecione os campos que deseja incluir na saída deste módulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Referências]</td> 
   <td>Selecione os campos de referência que deseja incluir na pesquisa.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Coleções]</td> 
   <td>Selecione todas as coleções que deseja adicionar à pesquisa.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Pesquisar (Herdado)]**

>[!IMPORTANT]
>
>Esse módulo foi substituído pelo módulo Search records. Recomendamos o uso desse módulo em novos cenários.
>Os cenários existentes que usam esse módulo continuarão a funcionar conforme esperado. Este módulo será removido do seletor de módulos em maio de 2025.

Esse módulo de pesquisa procura registros em um objeto no Workfront que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar seu aplicativo Workfront ao Workfront Fusion, consulte <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Conectar o Workfront ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de Registro]</td> 
   <td> <p>Selecione o tipo de registro Workfront que você deseja que o módulo procure.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conjunto de Resultados]</td> 
   <td>Selecione uma opção para especificar se você deseja que o módulo obtenha o primeiro resultado que corresponda aos seus critérios de pesquisa ou todos os resultados que correspondam a ele.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Máximo]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar campos de critérios]</td> 
   <td> <p>Selecione os campos que deseja usar com os critérios de pesquisa. Esses campos estarão disponíveis na lista suspensa Search criteria.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar critérios]</td> 
   <td> <p>Digite o campo pelo qual deseja pesquisar, o operador que deseja usar na consulta e o valor que está procurando no campo.</p> <p>Observação: não use <code>username </code> nos seus critérios de pesquisa. A inclusão de <code>username </code> em uma consulta de API para o Workfront registra o usuário no Workfront e a pesquisa não será bem-sucedida.</p> <p>Observação: <code>In</code> e <code>NotIn</code>funcionam com matrizes. As entradas devem estar em formato de matriz.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Saídas]</td> 
   <td> <p>Selecione os campos que deseja incluir na saída deste módulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Referências]</td> 
   <td>Selecione os campos de referência que deseja incluir na pesquisa.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Coleções]</td> 
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

## Tipos de objetos do Workfront disponíveis para cada módulo do Workfront

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**Tipos de objeto disponíveis para cada módulo de gatilho Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Observar Registro]</th> 
   <th>[!UICONTROL Campo de Observação]</th> 
   <th>[!UICONTROL Observar Eventos]</th> 
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
   <td> Registro de Cobrança </td> 
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
   <td>Versão do Documento</td> 
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
   <td>Tipo de Despesa</td> 
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
   <td>Entrada no Relatório</td> 
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
   <td>Caminho de Etapas</td> 
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
   <td>Etiqueta de nota</td> 
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
   <td>Usuário de Projeto</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aprovação da revisão</td> 
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
   <td>Tipo de Risco</td> 
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
   <td>Modelo de Tarefa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Planilha de horas</td> 
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
   <td>Atualizar</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tipos de objetos disponíveis para cada módulo de ação do Workfront**

>[!NOTE]
>
>O módulo [!UICONTROL Baixar Documento] não está incluído nesta tabela porque os tipos de objeto do Workfront não fazem parte de sua configuração.

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
   <th>[!UICONTROL Criar um registro]</th> 
   <th>[!UICONTROL Atualizar um registro]</th> 
   <th>[!UICONTROL Excluir um registro]</th> 
   <th>[!UICONTROL Carregar Documento]</th> 
   <th>[!UICONTROL Ler um registro]</th> 
   <th>[!UICONTROL Chamada de API Personalizada]</th> 
   <th>[!UICONTROL Ação Diversa]</th> 
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
   <td>Registro de Cobrança</td> 
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
   <td>Versão do Documento</td> 
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
   <td>Tipo de Despesa</td> 
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
   <td>Entrada no Relatório</td> 
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
   <td>Caminho de Etapas</td> 
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
   <td>Etiqueta de nota</td> 
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
   <td>Usuário de Projeto</td> 
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
   <td>Tipo de Risco</td> 
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
   <td>Modelo de Tarefa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Planilha de horas</td> 
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
   <td>Atualizar</td> 
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
   <th>[!UICONTROL Pesquisar]</th> 
   <th>[!UICONTROL Ler registros relacionados]</th> 
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
   <td>Registro de Cobrança</td> 
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
   <td>Versão do Documento</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Despesa</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo de Despesa</td> 
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
   <td>Entrada no Relatório</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Marco</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Caminho de Etapas</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Nota</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Etiqueta de nota</td> 
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
   <td>Usuário de Projeto</td> 
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
   <td>Tipo de Risco</td> 
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
   <td>Modelo de Tarefa</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Planilha de horas</td> 
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

## Filtros de assinatura de evento na Workfront > [!UICONTROL Assistir Eventos] módulos

>[!NOTE]
>
>* É altamente recomendável usar filtros de assinatura de evento em seus módulos [!UICONTROL Assistir Eventos].
>
>* A Workfront lançou recentemente uma nova versão de seu serviço de assinatura de eventos. A nova versão não é uma alteração na API do Workfront, mas uma alteração na funcionalidade de assinatura do evento. Este módulo de ação atualiza a versão de carga útil do evento usada para este cenário.
>
>   Para obter mais informações sobre a nova versão de assinatura de eventos, consulte [Versão de assinatura de eventos](https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) na documentação da Workfront
>
>   Para obter recursos sobre como preservar seus cenários do Workfront Fusion durante a atualização da assinatura do evento, incluindo uma gravação de webinário, consulte [Preservando seus cenários do Fusion Durante a Atualização de Assinaturas de Eventos V2(https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=pt)].

O módulo [!UICONTROL Assistir Eventos] do Workfront aciona cenários com base em um webhook que cria uma assinatura de evento na API do Workfront. A assinatura do evento é um conjunto de dados que determina quais eventos são enviados para o webhook. Por exemplo, se você configurar um módulo [!UICONTROL Eventos de observação] que esteja observando problemas, a assinatura do evento enviará somente eventos relacionados a problemas.

Ao usar filtros de subscrição de eventos, os usuários do Fusion podem criar subscrições de eventos que são mais adequadas para seus casos de uso. Por exemplo, você pode configurar uma assinatura de evento na API do Workfront para enviar somente problemas que estejam em um projeto específico para o webhook, garantindo que o módulo [!UICONTROL Eventos de observação] acionará apenas problemas nesse projeto. A capacidade de criar acionadores mais estreitos melhora o design do cenário ao reduzir o número de acionadores irrelevantes.

Isso é diferente da configuração de um filtro no cenário do Workfront Fusion. Sem um filtro de inscrição de evento, seu webhook recebe todos os eventos relacionados ao tipo de objeto selecionado. A maioria desses eventos seria irrelevante para o cenário e deve ser filtrada para que o cenário possa continuar.

Os seguintes operadores estão disponíveis no filtro Workfront > Eventos de observação:

* Igual
* Não é igual
* Maior que
* Menor que
* Maior que ou igual a
* Menor que ou igual a
* Contém
* Existe
   * Esse operador não requer um valor e o campo de valor está ausente.
* Não existe
   * Esse operador não requer um valor e o campo de valor está ausente.
* Alterado
   * Esse operador não requer um valor e o campo de valor está ausente.
   * Este operador ignora o campo Estado.
   * Ao usar `Changed`, selecione **Somente Eventos Atualizados** no campo **Origem do Registro**.

>[!IMPORTANT]
>
>Não é possível editar filtros em webhooks existentes do Workfront. Para configurar diferentes filtros para assinaturas de eventos do Workfront, remova o webhook atual e crie um novo.

>[!INFO]
>
>**Exemplo:** Considere um cenário que processa novos problemas atribuídos a um usuário específico, Ana.
>
>### Filtrar eventos usando um filtro de assinatura de evento (recomendado)
>
>Usando o filtro de eventos, você pode configurar o webhook para acionar o cenário quando um problema for atribuído a Ana quando o problema for criado. Ana tem a ID de usuário b378489d8f7cd3cee0539260720a84b7.
>
>![Filtro de eventos](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>Se forem criados 100 problemas em um dia, mas apenas dois deles forem atribuídos a Ana, o cenário seria executado duas vezes.
>
>### Filtrar eventos dentro do cenário (não recomendado)
>
>Para filtrar eventos de modo que somente problemas atribuídos a Ana sejam processados, você pode criar um filtro após o módulo [!UICONTROL Assistir Eventos].
>
>![Sem filtro de evento](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>Se 100 edições forem criadas em um dia, mas apenas duas delas forem atribuídas a Ana, o cenário seria executado 100 vezes. 98 das execuções parariam no filtro, mas o módulo de acionamento ainda está consumindo dados e executando operações em todas as execuções.

Para obter mais informações sobre assinaturas de eventos do Workfront, consulte [Perguntas frequentes - Assinaturas de Eventos](https://experienceleague.adobe.com/pt-br/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq).

Para obter mais informações sobre webhooks, consulte [Acionadores instantâneos (webhooks) no Adobe Workfront Fusion](/help/workfront-fusion/references/modules/webhooks-reference.md)

Para obter mais informações sobre filtros em cenários, consulte [Adicionar um filtro a um cenário](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
