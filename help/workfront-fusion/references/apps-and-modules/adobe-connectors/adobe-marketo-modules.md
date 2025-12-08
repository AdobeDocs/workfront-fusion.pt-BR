---
title: Módulos do Marketo
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam  [!DNL Marketo], bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '2237'
ht-degree: 100%

---

# Módulos do [!DNL Marketo]

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam [!DNL Marketo], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter um vídeo de introdução ao conector do Marketo, consulte:

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

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

## Pré-requisitos

Para usar módulos [!DNL Marketo], você deve ter uma conta do [!DNL Marketo].

## Informações da API do Marketo

O conector do Marketo usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL Marketo] ao Workfront Fusion {#connect-marketo-to-workfront-fusion}

Você pode criar uma conexão com sua conta do [!DNL Marketo] diretamente de dentro de qualquer módulo do [!DNL Marketo].

1. Em qualquer módulo do Marketo, clique em **Adicionar** ao lado do campo Conexão.
1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Insira um nome para a nova conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Selecione se estão se conectando a um ambiente de produção ou não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Account / Munchkin ID]</td>
        <td>
          <p>Insira sua conta do [!DNL Marketo] ou a ID do [!UICONTROL Munchkin] do [!DNL Marketo]. Esta é a parte exclusiva do URL de base ou do ponto de acesso atribuído à sua conta, que você usa para acessar o [!DNL Marketo] por meio da API [!UICONTROL REST] correspondente. Para obter instruções sobre como localizar isso, consulte [Base URL](https://developers.marketo.com/rest-api/base-url/) na documentação do [!DNL Marketo].</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira sua ID de cliente do Marketo. Para obter instruções sobre como localizar isso, consulte [Authentication](https://developers.marketo.com/rest-api/authentication/) na documentação do [!DNL Marketo].</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira o Segredo do cliente do Marketo. Para obter instruções sobre como localizar esses itens, consulte [Authentication](https://developers.marketo.com/rest-api/authentication/) na documentação do [!DNL Marketo].</td>
      </tr>
     </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## Módulos do [!DNL Marketo] e seus campos

Ao configurar os módulos do [!DNL Marketo], o Workfront Fusion exibe os campos listados a seguir. Junto com eles, outros campos do [!DNL Marketo] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Acionadores

* [[!UICONTROL Monitorar eventos (instantâneos)]](#watch-events-instant)
* [[!UICONTROL Monitorar registros]](#watch-records)

#### [!UICONTROL Monitorar eventos (instantâneos)]

Este módulo de acionador inicia um cenário quando um registro é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Insira o webhook que você deseja que o módulo use.</p> <p>Para obter mais informações sobre webhooks, consulte <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Monitorar registros]

Este módulo de acionador inicia um cenário quando um registro é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Activity]</strong> </p> <p>Selecione o tipo de atividade que você deseja monitorar. </p> <p>O módulo monitora somente novas atividades.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>No campo <b>Tipo de evento</b>, selecione se deseja monitorar novos registros, registros atualizados, ambos ou atualizações em campos específicos. Se você optar por monitorar atualizações em campos específicos, selecione o campo que deseja que o módulo monitore.</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p>No campo <b>Tipo de evento</b>, selecione se deseja monitorar novos registros, registros atualizados ou ambos.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecione os campos que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Adicionar leads a uma lista]](#add-leads-to-a-list)
* [[!UICONTROL Clonar um programa]](#clone-a-program)
* [[!UICONTROL Criar um registro]](#create-a-record)
* [[!UICONTROL Chamada de API personalizada]](#custom-api-call)
* [[!UICONTROL Baixar um arquivo]](#download-a-file)
* [[!UICONTROL Ler um registro]](#read-a-record)
* [[!UICONTROL Remover leads de uma lista]](#remove-leads-from-a-list)
* [[!UICONTROL Agendar uma campanha]](#schedule-a-campaign)
* [[!UICONTROL Atualizar um registro]](#update-a-record)
* [[!UICONTROL Fazer upload de um arquivo]](#upload-a-file)

#### [!UICONTROL Adicionar leads a uma lista]

Este módulo de ação adiciona um ou mais leads a uma lista usando a ID do lead. Você pode adicionar até 300 leads por vez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Insira ou mapeie a ID da lista em que você deseja adicionar leads.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Para cada lead que você deseja adicionar à lista, clique em <b>[!UICONTROL Add]</b> e, em seguida, insira ou mapeie a ID do lead que deseja adicionar. Você pode adicionar até 300 leads para o módulo que deseja adicionar à lista.</p> <p>Clique no botão de alternância Mapear para mapear uma coleção existente de leads que deseja adicionar à lista.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clonar um programa]

Este módulo de ação faz uma cópia de um programa usando a ID do programa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Existing Program ID]</td> 
   <td>Insira ou mapeie a ID do programa que você deseja copiar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Program Name]</p> </td> 
   <td> <p>Insira ou mapeie um nome para o novo programa</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Insira ou mapeie a ID da pasta em que deseja que o novo programa esteja localizado.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar um registro]

Este módulo de ação cria um novo registro no [!DNL Marketo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Folder]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Se você estiver criando uma Empresa ou um Lead, selecione os campos para os quais deseja definir valores quando o novo registro for criado e, em seguida, insira valores para esses campos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Type]</td> 
   <td>Se você estiver criando um Programa, selecione o tipo de programa que deseja criar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Channel] </td> 
   <td>Se estiver criando um Programa, selecione o canal no qual deseja criá-lo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]/[!UICONTROL Program Name]</td> 
   <td>Se você estiver criando uma Pasta ou um Programa, insira ou mapeie um nome para o novo registro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Se você estiver criando uma Pasta ou um Programa, insira ou mapeie uma descrição para o novo registro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID]</td> 
   <td>Se você estiver criando uma pasta ou um programa, insira ou mapeie a ID da pasta pai na qual deseja criar o novo registro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Se você estiver criando um programa, adicione os custos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Se estiver criando um Programa, adicione tags</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Este módulo de ação permite fazer uma chamada autenticada personalizada para a API do [!DNL Marketo]. Dessa forma, você pode criar uma automação de fluxo de dados que não pode ser realizada pelos outros módulos do [!DNL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo a <code>https://{your-base-url}.mktorest.com/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O [!UICONTROL Workfront Fusion] adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta para a chamada de API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Para cada campo que você deseja adicionar à chamada de API, clique em <b>Adicionar item</b> e insira a chave e o valor do campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Baixar um arquivo]

Este módulo de ação baixa um arquivo usando sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Insira ou mapeie a ID do arquivo que deseja baixar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler um registro]

Este módulo de ação lê as informações sobre um registro usando sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaign]</p> </li> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL List]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione as informações que deseja incluir no pacote de saída deste módulo. Os campos estão disponíveis com base no [!UICONTROL Record Type] selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;Object&gt; ID]</td> 
   <td>Insira ou mapeie a ID do objeto sobre o qual deseja recuperar informações.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remover leads de uma lista]

Este módulo de ação remove um ou mais leads de uma lista usando a ID do lead. Você pode restaurar até 300 leads por vez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Insira ou mapeie a ID da lista em que deseja remover leads.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Para cada lead que você deseja remover da lista, clique em <b>[!UICONTROL Add item]</b> e, em seguida, insira ou mapeie a ID do lead que deseja remover. Você pode adicionar até 300 leads do módulo para remover da lista. </p> <p>Clique no botão Mapear para mapear uma coleção de leads que deseja remover da lista.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Agendar uma campanha]

Este módulo de ação agenda uma campanha para uma determinada data.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Insira ou mapeie a ID da campanha que você deseja agendar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Schedule for Date]</p> </td> 
   <td>Selecione a data em que deseja que a campanha seja executada. Se esse campo ficar em branco, a campanha será executada cinco minutos após o início do cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um registro]

Este módulo de ação atualiza um registro usando sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja criar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Company]/[!UICONTROL Lead]/[!UICONTROL Program ID]</td> 
   <td>Insira ou mapeie a ID do registro que deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Se você estiver atualizando uma empresa ou um lead, selecione os campos que deseja atualizar e insira os valores.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Name]</td> 
   <td>Se você estiver atualizando um programa, insira ou mapeie um novo nome para o programa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Se você estiver atualizando um programa, insira ou mapeie uma nova descrição para o programa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Se você estiver atualizando um programa, insira ou mapeie uma nova data inicial para o programa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Se você estiver atualizando um programa, insira ou mapeie uma nova data final para ele.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Se você estiver atualizando um programa, adicione os custos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Se você estiver atualizando um programa, adicione tags</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fazer upload de um arquivo]

Este módulo de ação faz upload de um novo arquivo para o [!UICONTROL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Insira ou mapeie a ID da pasta na qual deseja que o novo arquivo esteja localizado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Insira uma descrição para o arquivo enviado.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [[!UICONTROL Listar registros]](#list-records)
* [[!UICONTROL Pesquisar registros]](#update-a-record)

#### [!UICONTROL Listar registros]

Este módulo de ação recupera todos os registros de um tipo específico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecione o tipo de registro que deseja listar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Read all campaigns]</p> </li> 
     <li> <p>[!UICONTROL Read all programs]</p> </li> 
     <li> <p>[!UICONTROL Read all leads] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field]</td> 
   <td>Se você selecionou para recuperar leads, selecione se deseja recuperá-los de uma lista ou de um programa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecione as informações que deseja incluir no pacote de saída deste módulo. Os campos estão disponíveis com base no [!UICONTROL Record Type] selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar registros]

Este módulo de pesquisa recupera uma lista de registros que correspondem a critérios de pesquisa específicos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Marketo] ao Workfront Fusion, consulte <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Marketo] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecione o tipo de ambiente que deseja pesquisar.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaigns]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programs]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Field]</p> </td> 
   <td> <p>Selecione o campo pelo qual deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value / values]</td> 
   <td>Insira o valor do campo que você deseja pesquisar. Se o campo permitir a pesquisa de vários valores, para cada valor que você deseja pesquisar, clique em <b>[!UICONTROL Add item]</b> e insira o valor.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Selecione as informações que deseja incluir no pacote de saída deste módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>
