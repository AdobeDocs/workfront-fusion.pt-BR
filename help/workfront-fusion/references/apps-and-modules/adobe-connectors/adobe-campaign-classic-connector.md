---
title: Módulos do Adobe Campaign v7/v8
description: Com os  [!DNL Adobe Campaign] módulos, você pode iniciar um [!DNL Adobe Workfront Fusion] cenário com base nos eventos da sua [!DNL Adobe Campaign] conta, criar, ler ou atualizar contratos e outros registros, pesquisar registros usando os critérios que você definiu e carregar documentos.
author: Becky
feature: Workfront Fusion
exl-id: 9fdff26c-c7c0-4eb8-a36f-4aeaf432b333
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!DNL Adobe Campaign] módulos

Com os módulos do [!DNL Adobe Campaign], você pode iniciar um cenário do [!DNL Adobe Workfront Fusion] com base em eventos na sua conta do [!DNL Adobe Campaign v7/v8], criar, ler ou atualizar registros, pesquisar registros usando critérios que você definiu e executar chamadas de API personalizadas.

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

Você deve adicionar os endereços IP do Fusion a [!DNL Adobe Campaign].

* Para obter instruções sobre como adicionar endereços IP ao arquivo de incluir na lista de permissões inclui na lista de permissões do Campaign, consulte [Adicionar endereços IP ao arquivo](https://experienceleague.adobe.com/en/docs/control-panel/using/sftp-management/ip-range-allow-listing#adding-ip-addresses-allow-list) na documentação do Adobe Campaign.
* Incluir na lista de permissões Para obter uma lista de endereços IP a serem adicionados ao arquivo, consulte [Endereços IP para acessar o Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md).

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

## Conectar [!DNL Adobe Campaign] a [!DNL Adobe Workfront Fusion]

>[!IMPORTANT]
>
>É altamente recomendável criar uma conexão de servidor para servidor. A Adobe Campaign atualizou a API para aceitar somente conexões servidor para servidor. Se você estiver se conectando ao Campaign versão 8 ou superior, **deverá** criar uma conexão servidor a servidor.
>
>Para obter mais informações sobre os novos requisitos de conexão do Campaign, consulte [Migração de operadores técnicos do Campaign para o Adobe Developer Console](https://experienceleague.adobe.com/docs/campaign/technotes-ac/tn-new/ims-migration.html) na documentação do Campaign.

1. Em qualquer módulo [!DNL Adobe Campaign], clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
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
            <p>Selecione se você está criando uma conexão básica ou uma conexão de servidor para servidor.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Insira um nome para esta conexão.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Base URL]</td>
          <td>Insira a URL de base que você usa para se conectar à sua instância do [!DNL Adobe Campaign].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Username]</td>
          <td>Se você estiver criando uma conexão básica, digite seu nome de usuário do Adobe Campaign.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Password]</td>
          <td>Se você estiver criando uma conexão básica, digite sua senha do Adobe Campaign.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Se você estiver criando uma conexão servidor a servidor, digite o [!DNL Adobe] [!UICONTROL Client ID]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] de [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Se você estiver criando uma conexão servidor a servidor, digite o [!DNL Adobe] [!UICONTROL Client Secret]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] de [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Environment]</td>
          <td>Selecione se você está conectado a um ambiente de Produção ou Não produção.
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Type]</td>
          <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.
        </tr>
   </tbody>
    </table>
1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.

## [!DNL Adobe Campaign] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Campaign], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Campaign] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Triggers

#### [!UICONTROL Watch records]

Esse módulo de acionador agendado inicia um cenário quando um registro é alterado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Selecione se deseja observar novos registros, registros atualizados ou ambos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecione o recurso que deseja observar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output]</td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>Para cada campo personalizado que você deseja incluir na saída, clique em <b>[!UICONTROL Add]</b> e insira o nome do campo personalizado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>


### Ações

* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)
* [[!UICONTROL Delete a record]](#delete-record)
* [[!UICONTROL Perform an action]](#perform-an-action)
* [[!UICONTROL Read a record]](#-read-a-record)
* [[!UICONTROL Subscribe or unsubscribe]](#subscribe-or-unsubscribe)
* [[!UICONTROL Update a record]](#update-record)

#### [!UICONTROL Create a record]

Este módulo de ação cria um novo registro em [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecione o tipo de registro [!DNL Adobe Campaign] que deseja criar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>Selecione os campos para os quais deseja definir valores quando o registro for criado e preencha os valores desses campos. Os campos variam de acordo com o tipo de registro selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> Para cada campo personalizado que você deseja adicionar ao novo registro, clique em <b>[!UICONTROL Add item]</b> e insira ou mapeie o nome e o valor do campo. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make a custom API call]

Este módulo faz uma chamada de API personalizada para a API [!DNL Adobe Campaign]

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Action]</td>
      <td><p>Selecione a ação que você deseja que a chamada de API execute.</p>
      <p>[!UICONTROL Execute query]</p>
      <p>[!UICONTROL Write]</p>
      <p>[!UICONTROL Get entity if more recent]</p>
      <p>[!UICONTROL Select all]</p>
      <p>[!UICONTROL Push event]</p>
    </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] adiciona o cabeçalho de token [!UICONTROL x-security] automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL XML Body]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada da API em XML, sem o elemento de sessão. </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL Delete Record]

Este módulo de ação exclui um único registro de [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecione o tipo de recurso que deseja excluir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Insira ou mapeie a ID do recurso que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Perform an action]

Este módulo de ação executa uma ação selecionada em um objeto na API [!DNL Adobe Campaign].

Para obter informações sobre ações e campos específicos, consulte [[!DNL Adobe Campaign] - Documentação da API](https://experienceleague.adobe.com/developer/campaign-api/api/p-14.html).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td><p>Selecione a ação a ser executada no objeto.</p>
   <ul>
   <li><p><b>[!DNL List]</b></p><p> Para obter os campos disponíveis, consulte <a href="#search" class="MCXref xref" >[!UICONTROL Search]</a> neste artigo. </p></li>
     <li><p><b>[!UICONTROL Get]</b></p><p> Para obter os campos disponíveis, consulte <a href="#search" class="MCXref xref" >[!UICONTROL Search]</a> neste artigo. </p></li> 
   <li><p><b>[!UICONTROL Create]</b></p><p> Para obter os campos disponíveis, consulte <a href="#create-a-record" class="MCXref xref" >[!UICONTROL Create a record]</a> neste artigo. </p></li>
   <li><p><b>[!UICONTROL Update]</b></p><p> Para obter os campos disponíveis, consulte <a href="#update-record" class="MCXref xref" >[!UICONTROL Update a record]</a> neste artigo. </p></li>
   <li><p><b>[!UICONTROL Delete]</b></p><p> Para obter os campos disponíveis, consulte <a href="#delete-record" class="MCXref xref" >[!UICONTROL Delete a record]</a> neste artigo. </p></li>
   </ul>
   </td>
</tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Este módulo de ação lê um registro de [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecione o tipo de registro [!DNL Adobe Campaign] que deseja ler.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Insira do mapa a ID do registro que você deseja ler.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output] </td> 
   <td>Selecione os campos que deseja incluir na saída do módulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>Para cada campo personalizado que você deseja incluir na saída, clique em <b>[!UICONTROL Add]</b> e insira o nome do campo personalizado.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Subscribe or unsubscribe]

Este módulo de ação assina um usuário ou cancela a assinatura de um usuário em um serviço de informação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe or unsubscribe]</td> 
   <td>Selecione se deseja assinar ou cancelar a assinatura do serviço de informações.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service name]</td> 
   <td>Selecione o serviço que deseja assinar ou do qual deseja cancelar a assinatura.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipient email address] </td> 
   <td>Insira ou mapeie o endereço de email do usuário que deseja assinar ou cancelar a assinatura do serviço de informações.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update record]

Este módulo de ação atualiza um único registro em [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecione o tipo de registro [!DNL Adobe Campaign] que deseja criar.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Insira do mapa a ID do registro que você deseja atualizar.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>Selecione os campos para os quais deseja atualizar valores e preencha os valores desses campos. Os campos variam de acordo com o tipo de registro selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> Para cada campo personalizado que você deseja atualizar, clique em <b>[!UICONTROL Add item]</b> e insira ou mapeie o nome e o valor do campo. </td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

#### [!UICONTROL Search]

Este módulo de pesquisa retorna registros com base nos critérios especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Campaign], consulte <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Campaign]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecione o tipo de registro [!DNL Adobe Campaign] que deseja criar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>
