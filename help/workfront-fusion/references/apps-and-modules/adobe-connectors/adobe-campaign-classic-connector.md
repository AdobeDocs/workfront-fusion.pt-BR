---
title: Módulos do Adobe Campaign v7/v8
description: Com os  [!DNL Adobe Campaign] módulos, você pode iniciar um cenário do Adobe Workfront Fusion com base em eventos na sua conta [!DNL Adobe Campaign] criar, ler ou atualizar contratos e outros registros, pesquisar registros usando os critérios definidos e carregar documentos.
author: Becky
feature: Workfront Fusion
exl-id: 9fdff26c-c7c0-4eb8-a36f-4aeaf432b333
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 1%

---

# [!DNL Adobe Campaign] módulos

Com os módulos do [!DNL Adobe Campaign], você pode iniciar um cenário do Adobe Workfront Fusion com base em eventos na sua conta do [!DNL Adobe Campaign v7/v8], criar, ler ou atualizar registros, pesquisar registros usando os critérios definidos e executar chamadas de API personalizadas.

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
   <p>Novo menu:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
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

Você deve adicionar os endereços IP do Fusion a [!DNL Adobe Campaign].

* Para obter instruções sobre como adicionar endereços IP ao arquivo de incluir na lista de permissões inclui na lista de permissões do Campaign, consulte [Adicionar endereços IP ao arquivo](https://experienceleague.adobe.com/pt-br/docs/control-panel/using/sftp-management/ip-range-allow-listing#adding-ip-addresses-allow-list) na documentação do Adobe Campaign.
* Incluir na lista de permissões incluir na lista de permissões Para obter uma lista de endereços IP a serem adicionados ao arquivo, consulte [Configurar Endereços IP para Fusion no arquivo da sua organização](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md).

## Informações da API do Adobe Campaign

O conector do Adobe Campaign usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.7.22</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL Adobe Campaign] ao Adobe Workfront Fusion

>[!IMPORTANT]
>
>É altamente recomendável criar uma conexão de servidor para servidor. A Adobe Campaign atualizou a API para aceitar somente conexões servidor para servidor. Se você estiver se conectando ao Campaign versão 8 ou superior, **deverá** criar uma conexão servidor a servidor.
>
>Para obter mais informações sobre os novos requisitos de conexão do Campaign, consulte [Migração de operadores técnicos do Campaign para o Adobe Developer Console](https://experienceleague.adobe.com/docs/campaign/technotes-ac/tn-new/ims-migration.html?lang=pt-BR) na documentação do Campaign.

1. Em qualquer módulo [!DNL Adobe Campaign], clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. Preencha os seguintes campos:
   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Tipo de conexão]</td>
          <td>
            <p>Selecione se você está criando uma conexão básica ou uma conexão de servidor para servidor.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Nome da Conexão]</td>
          <td>
            <p>Insira um nome para esta conexão.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL URL Base]</td>
          <td>Insira a URL de base que você usa para se conectar à sua instância do [!DNL Adobe Campaign].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Nome de Usuário]</td>
          <td>Se você estiver criando uma conexão básica, digite seu nome de usuário do Adobe Campaign.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Senha]</td>
          <td>Se você estiver criando uma conexão básica, digite sua senha do Adobe Campaign.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID do Cliente]</td>
          <td>Se você estiver criando uma conexão servidor a servidor, digite sua [!DNL Adobe] [!UICONTROL ID do Cliente]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
          <td>Se você estiver criando uma conexão servidor a servidor, digite o [!DNL Adobe] [!UICONTROL Client Secret]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
        </tr>
     </tbody>
    </table>
1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## [!DNL Adobe Campaign] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Campaign], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Campaign] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<!--* [Triggers](#triggers)-->
* [Ações](#actions)
* [Pesquisas](#searches)

<!--### Triggers

#### [!UICONTROL Watch records]

This scheduled trigger module starts a scenario when a record changes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Create a connection to [!DNL Adobe Campaign]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Select whether you want to watch for new records, updated records, or both.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Select the resource that you want to watch for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output]</td> 
   <td>Select the fields that you want to include in the module's output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>For each custom field that you want to include in output, click <b>[!UICONTROL Add]</b> and enter the name of the custom field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>-->


### Ações

* [[!UICONTROL Criar um registro]](#create-a-record)
* [[!UICONTROL Excluir um registro]](#delete-record)
* [[!UICONTROL Fazer uma chamada de API personalizada]](#make-a-custom-api-call)
* [[!UICONTROL Executar uma ação]](#perform-an-action)
* [[!UICONTROL Ler um registro]](#read-a-record)
* [[!UICONTROL Assinar ou cancelar assinatura]](#subscribe-or-unsubscribe)
* [[!UICONTROL Atualizar um registro]](#update-record)

#### [!UICONTROL Criar um registro]

Este módulo de ação cria um novo registro em [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recurso]</td> 
   <td>Selecione o tipo de registro [!DNL Adobe Campaign] que deseja criar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos] </td> 
   <td>Selecione os campos para os quais deseja definir valores quando o registro for criado e preencha os valores desses campos. Os campos variam de acordo com o tipo de registro selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos personalizados]</td> 
   <td> Para cada campo personalizado que você deseja adicionar ao novo registro, clique em <b>[!UICONTROL Adicionar item]</b> e insira ou mapeie o nome e o valor do campo. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir Registro]

Este módulo de ação exclui um único registro de [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recurso]</td> 
   <td>Selecione o tipo de recurso que deseja excluir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID do recurso que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fazer uma chamada de API personalizada]

Este módulo faz uma chamada de API personalizada para a API [!DNL Adobe Campaign]

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ação]</td>
      <td><p>Selecione a ação que você deseja que a chamada de API execute.</p>
      <p>[!UICONTROL Executar consulta]</p>
      <p>[!UICONTROL Gravar]</p>
      <p>[!UICONTROL Obter entidade se mais recente]</p>
      <p>[!UICONTROL Selecionar tudo]</p>
      <p>[!UICONTROL Evento Push]</p>
    </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cabeçalhos]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona automaticamente o cabeçalho do token [!UICONTROL x-security].</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo XML]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada da API em XML, sem o elemento de sessão. </td>     </tr>
  </tbody>
</table>


#### [!UICONTROL Executar uma ação]

Este módulo de ação executa uma ação selecionada em um objeto na API [!DNL Adobe Campaign].

Para obter informações sobre ações e campos específicos, consulte [[!DNL Adobe Campaign] - Documentação da API](https://experienceleague.adobe.com/developer/campaign-api/api/p-14.html?lang=pt-BR).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ação]</td> 
   <td><p>Selecione a ação a ser executada no objeto.</p>
   <ul>
   <li><p><b>[!DNL List]</b></p><p> Para obter os campos disponíveis, consulte <a href="#search" class="MCXref xref" >[!UICONTROL Pesquisa]</a> neste artigo. </p></li>
     <li><p><b>[!UICONTROL Obter]</b></p><p> Para obter os campos disponíveis, consulte <a href="#search" class="MCXref xref" >[!UICONTROL Pesquisa]</a> neste artigo. </p></li> 
   <li><p><b>[!UICONTROL Criar]</b></p><p> Para campos disponíveis, consulte <a href="#create-a-record" class="MCXref xref" >[!UICONTROL Criar um registro]</a> neste artigo. </p></li>
   <li><p><b>[!UICONTROL Atualizar]</b></p><p> Para campos disponíveis, consulte <a href="#update-record" class="MCXref xref" >[!UICONTROL Atualizar um registro]</a> neste artigo. </p></li>
   <li><p><b>[!UICONTROL Excluir]</b></p><p> Para campos disponíveis, consulte <a href="#delete-record" class="MCXref xref" >[!UICONTROL Excluir um registro]</a> neste artigo. </p></li>
   </ul>
   </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler um registro]

Este módulo de ação lê um registro de [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recurso]</td> 
   <td>Selecione o tipo de registro [!DNL Adobe Campaign] que deseja ler.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Insira do mapa a ID do registro que você deseja ler.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Campos a serem incluídos na saída] </td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos personalizados a serem incluídos na saída]</td> 
   <td>Para cada campo personalizado que você deseja incluir na saída, clique em <b>[!UICONTROL Adicionar]</b> e insira o nome do campo personalizado.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Assinar ou cancelar assinatura]

Este módulo de ação assina um usuário ou cancela a assinatura de um usuário em um serviço de informação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assinar ou cancelar assinatura]</td> 
   <td>Selecione se deseja assinar ou cancelar a assinatura do serviço de informações.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do serviço]</td> 
   <td>Selecione o serviço que deseja assinar ou do qual deseja cancelar a assinatura.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Endereço de email do destinatário] </td> 
   <td>Insira ou mapeie o endereço de email do usuário que deseja assinar ou cancelar a assinatura do serviço de informações.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar registro]

Este módulo de ação atualiza um único registro em [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recurso]</td> 
   <td>Selecione o tipo de registro [!DNL Adobe Campaign] que deseja criar.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Insira do mapa a ID do registro que você deseja atualizar.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Campos] </td> 
   <td>Selecione os campos para os quais deseja atualizar valores e preencha os valores desses campos. Os campos variam de acordo com o tipo de registro selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campos personalizados]</td> 
   <td> Para cada campo personalizado que você deseja atualizar, clique em <b>[!UICONTROL Adicionar item]</b> e insira ou mapeie o nome e o valor do campo. </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

#### [!UICONTROL Pesquisa]

Este módulo de pesquisa retorna registros com base nos critérios especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recurso]</td> 
   <td>Selecione o tipo de registro [!DNL Adobe Campaign] que deseja criar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pesquisar critérios]</td> 
   <td>Informe os campos e valores que deseja que a pesquisa use. Os campos dependem do recurso selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>
