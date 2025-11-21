---
title: Módulos do Adobe Target
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam  [!DNL Adobe Target], as well as connect it to multiple third-party applications and services. [!DNL Adobe Target] módulos que permitem criar, ler, atualizar ou excluir registros, listar todos os registros de um determinado tipo, pesquisar registros com base em critérios especificados ou executar uma chamada de API personalizada para a API [!DNL Adobe Target] .
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
source-git-commit: f23a089565c2cfb7d2d1321a7bf67ae14e336af3
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 1%

---

# [!DNL Adobe Target] Módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Adobe Target], bem como conectá-lo a vários aplicativos e serviços de terceiros. Os módulos do [!DNL Adobe Target] permitem criar, ler, atualizar ou excluir registros, listar todos os registros de um determinado tipo, pesquisar registros com base nos critérios especificados ou executar uma chamada de API personalizada para a API do [!DNL Adobe Target].


Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote de Automação e Integração do Adobe Workfront</p><p>Workfront Ultimate</p><p>Workfront Prime e pacotes Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Standard</p><p>Trabalhar ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (herdado): automação e integração do Workfront Fusion for Work </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Antes de usar o conector [!DNL Adobe Target], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!DNL Adobe Target] ativa.

## Informações da API do Adobe Target

O conector do Adobe Target usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.7.33</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com [!DNL Adobe Target]

>[!IMPORTANT]
>
>As conexões criadas após 3 de junho de 2024 exigem uma conexão de servidor para servidor do Adobe Target.
>
>* As conexões da Conta de serviço existentes continuarão funcionando até janeiro de 2025. Você deve substituir suas conexões de Conta de serviço pelas conexões servidor a servidor do Adobe Target até janeiro de 2024.
>* Você deve ser um desenvolvedor para que sua organização crie uma conexão de servidor para servidor do Adobe Target. A função de desenvolvedor é definida na Adobe Admin Console.

Para criar uma conexão para seus módulos do [!DNL Adobe Target]:

1. Em qualquer módulo, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

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
          <p>Insira um nome para esta conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo de conexão]</td>
        <td>Selecione se você está criando uma conexão de Conta de Serviço ou uma conexão de Servidor para Servidor do Adobe Target.<p><b>IMPORTANTE</b>: as conexões criadas após 3 de junho de 2024 exigem uma conexão de servidor para servidor do Adobe Target. As conexões da Conta de serviço existentes continuarão funcionando até janeiro de 2025. Você deve substituir suas conexões de Conta de serviço pelas conexões servidor a servidor do Adobe Target até janeiro de 2024.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID do Cliente]</td>
        <td>Insira sua ID de cliente do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira seu Segredo do Cliente do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID da conta técnica]</td>
        <td>Insira sua ID de conta técnica do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID da Organização]</td>
        <td>Insira sua ID da organização [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Locatário]</td>
        <td>
          <p> Para localizar seu Locatário, faça logon no [!DNL Adobe Experience Cloud], abra o [!DNL Target] e clique no cartão [!DNL Target]. Use o valor da ID do locatário conforme observado no subdomínio do URL.</p>
          <p>Por exemplo, se a URL ao fazer logon no [!DNL Adobe Target] for <code>&lt;https://mycompany.experiencecloud.adobe.com/...></code>, sua ID de Locatário será "mycompany".</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Escopos do Meta]</td>
        <td>Inserir <code>ent_marketing_sdk</code>       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Chave privada]</td>
        <td>
          <p>Insira a chave privada gerada quando suas credenciais foram criadas no [!DNL Adobe Developer Console]. </p>
          <p>Para extrair sua chave privada ou certificado:</p>
          <ol>
            <li value="1">
              <p>Clique em <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selecione o tipo de arquivo que você está extraindo.</p>
            </li>
            <li value="3">
              <p>Selecione o arquivo que contém a chave privada ou o certificado.</p>
            </li>
            <li value="4">
              <p>Digite a senha do arquivo.</p>
            </li>
            <li value="5">
              <p>Clique em <b>[!UICONTROL Salvar]</b> para extrair o arquivo e retornar à configuração de conexão.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## [!DNL Adobe Target] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Target], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Target] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ações](#actions)

* [Pesquisas](#searches)


### Ações

* [[!UICONTROL Criar um registro]](#create-a-record)

* [[!UICONTROL Fazer uma chamada de API personalizada]](#make-a-custom-api-call)

* [[!UICONTROL Excluir um registro]](#delete-a-record)

* [[!UICONTROL Ler um registro]](#read-a-record)

* [[!UICONTROL Atualizar um registro]](#update-a-record)


#### [!UICONTROL Criar um registro]

Esse módulo de ação cria uma atividade AB ou XT, uma oferta ou um público-alvo.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Conexão]</td>
    <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Target], consulte <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Target]</a> neste artigo.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Tipo de registro]</td>
    <td>
      <p>Selecione o tipo de registro que deseja criar.</p>
      <ul>
        <li>
        <b>Propriedade</b><p>Para obter detalhes sobre campos, consulte <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Properties/operation/createProperty">Criar uma propriedade</a> na documentação da API do Adobe Target.</p>
        </li>
        <li>
        <b>Recomendação da oferta</b><p>Para obter detalhes sobre campos, consulte <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Offers/operation/createOffer">Criar uma nova oferta recs</a> na documentação da API do Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Oferta JSON]</b>
          <p>Continue para <a href="#offer-fields" class="MCXref xref" >Campos de oferta</a>.</p>
        </li>
        <li>
          <b>[!UICONTROL Conteúdo da Oferta]</b>
          <p>Continue para <a href="#offer-fields" class="MCXref xref" >Campos de oferta</a>.</p>
        </li>
        <li>
        <b>Ambiente</b><p>Para obter detalhes sobre campos, consulte <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Environments/operation/createEnvironment">Criar ambiente</a> na documentação da API do Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Público-alvo]</b>
          <p>Para obter detalhes sobre campos, consulte <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Audiences/operation/createAudience_1_1">Criar público-alvo</a> na documentação da API do Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Atividade AB]</b>
          <p>Para obter detalhes sobre campos, consulte <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Criar atividade AB</a> na documentação da API do Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Atividade XT]</b>
          <p>Prossiga para <a href="#xt-activity-fields" class="MCXref xref" >Campos de atividade XT</a>.</p>
        </li>
        <li>
          <b>[!UICONTROL Atividade AP]</b>
          <p>Para obter detalhes sobre campos, consulte <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_2">Criar atividade AP</a> na documentação da API do Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Token de Resposta]</b>
          <p>Para obter detalhes sobre campos, consulte <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Response-tokens/operation/createResponseToken">Criar token de resposta</a> na documentação da API do Adobe Target.</p>
        </li>
      </ul>
    </td>
  </tr>
</tbody>
</table>

<!--

##### AB Activity fields

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this activity. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>For each option that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the option across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the option. The name must be no more than 250 characters.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Select or map the Offer associated with the option.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Mboxes]</td>
      <td>
        <p>For each Mbox that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selectors]</td>
      <td>
        <p>For each selector that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Selector]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>A list of locations on the page where the content offer is served. A location contains the following:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Enter or map the ID of the experience</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map the name of the experience
</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>For each audience that you want to see the experience, click <b>[!UICONTROL Add item]</b> and enter the Audience ID.
</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Enter or map the percentage of visitors that is allocated to the experience</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td><p>For details on metrics, see <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Create AB activity</a> in the Adobe Target API documentation.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Enter or map an ID to identify this activity. You can choose this ID. This ID must not be the same as another activity, and can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Enter or map the date and time to start the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Enter or map the date and time to end the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Enter or map the state of the activity.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Enter a number that defines the priority of the activity. Higher numbers have higher priority. This value must be between 0 and 999. The default value is 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Enable this option to auto-allocate traffic. Auto-allocating sends more traffic to the more successful experience.</p>
        <p>Select or map the evaluation criteria by which to judge which experience is more successful.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Enter or map the workspace that the activity is associated with</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>For each property that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and select or map the property's ID.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>For each reporting audience that you want to add to the activity, click [!UICONTROL Add item] and enter the following information:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the Reporting Audience across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Enter or map the Segment to be used in reporting</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the metric across API requests.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

-->

##### Campos de atividade de XT

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Nome]</td>
      <td>Insira ou mapeie um nome para esta atividade. O nome não pode ter mais de 250 caracteres.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Opções]</td>
      <td>
        <p>Para cada opção que você deseja adicionar à atividade, clique em <b>[!UICONTROL Adicionar item]</b> e preencha os seguintes campos:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL ID de Opção local]</b>
            </p>
            <p>Insira ou mapeie uma string a ser usada para rastrear a opção nas solicitações da API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Nome]</b>
            </p>
            <p>Insira ou mapeie um nome para a opção. O nome não deve ter mais de 250 caracteres.</p>
          </li>
          <li>
            <p><b>[!UICONTROL ID da oferta]</b>
            </p>
          </li>
          <li>
            <p>Selecione ou mapeie a Oferta associada à opção.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Locais]</td>
      <td>
        <p>Para cada Mbox que você deseja adicionar à atividade, clique em <b>[!UICONTROL Adicionar item]</b> e preencha os seguintes campos:</p>
        <ul>
          <li>
            <p>[!UICONTROL IDs de público-alvo]</p>
            <p>Para cada público-alvo que você deseja adicionar à Mbox, clique em <b>[!UICONTROL Adicionar item]</b> e selecione a ID de público-alvo.</p>
          </li>
          <li>
            <p><b>[!UICONTROL ID Local do Local]</b>
            </p>
            <p>Insira ou mapeie uma string a ser usada para rastrear o local nas solicitações da API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Nome]</b>
            </p>
            <p>Insira ou mapeie um nome para o Local. O nome não deve ter mais de 250 caracteres.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiências]</td>
      <td>
        <p>Uma lista de locais na página onde a oferta de conteúdo é apresentada. Um local contém o seguinte:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL ID de Experiência local]</b>
            </p>
            <p>Insira ou mapeie a ID da experiência</p>
          </li>
          <li>
            <p><b>[!UICONTROL Nome]</b>
            </p>
            <p>Insira ou mapeie o nome da experiência

</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>Para cada público-alvo que você deseja ver a experiência, clique em <b>[!UICONTROL Adicionar item]</b> e insira a ID de público-alvo.

</p>
          </li>
          <li>
            <p><b>[!UICONTROL Porcentagem de Visitantes]</b>
            </p>
            <p>Insira ou mapeie a porcentagem de visitantes alocada para a experiência</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Métricas]</td>
      <td> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID de Terceiros]</td>
      <td>Insira ou mapeie uma ID para identificar esta atividade. Você pode escolher essa ID. Essa ID não deve ser igual a outra atividade e não pode ter mais de 250 caracteres.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inicia às]</td>
      <td>Insira ou mapeie a data e a hora para iniciar a atividade no formato <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Termina em]</td>
      <td>Insira ou mapeie a data e a hora para terminar a atividade no formato <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Estado]</td>
      <td>
        <p>Insira ou mapeie o estado da atividade.</p>
        <ul>
          <li>
            <p>[!UICONTROL Aprovado]</p>
          </li>
          <li>
            <p>[!UICONTROL Desativado]</p>
          </li>
          <li>
            <p>[!UICONTROL Pausado]</p>
          </li>
          <li>
            <p>[!UICONTROL Salvo] </p>
          </li>
          <li>
            <p>[!UICONTROL Excluído]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Prioridade]</td>
      <td>Insira um número que defina a prioridade da atividade. Números mais altos têm prioridade mais alta. Esse valor deve estar entre 0 e 999. O valor padrão é 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Alocar tráfego automaticamente]</td>
      <td>
        <p>Ative essa opção para alocar o tráfego automaticamente. A alocação automática envia mais tráfego para a experiência mais bem-sucedida.</p>
        <p>Selecione ou mapeie os critérios de avaliação pelos quais julgar qual experiência é mais bem-sucedida.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Insira ou mapeie o espaço de trabalho ao qual a atividade está associada</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL IDs de Propriedades] </td>
      <td>Para cada propriedade que você deseja adicionar à atividade, clique em <b>[!UICONTROL Adicionar item]</b> e selecione ou mapeie a ID da propriedade.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Relatórios de públicos-alvo]</td>
      <td>
        <p>Para cada público-alvo de relatório que você deseja adicionar à atividade, clique em [!UICONTROL Adicionar item] e insira as seguintes informações:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL ID de Público-alvo local do Relatório]</b>
            </p>
            <p>Insira ou mapeie uma cadeia de caracteres a ser usada para rastrear o Público-alvo do relatório nas solicitações da API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL ID de Público]</b>
            </p>
            <p>Inserir ou mapear o segmento a ser usado no relatório</p>
          </li>
          <li>
            <p><b>[!UICONTROL ID de Métrica local]</b>
            </p>
            <p>Insira ou mapeie uma string a ser usada para rastrear a métrica nas solicitações da API.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Campos de oferta

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Nome]</td>
      <td>Insira ou mapeie um nome para esta atividade. O nome não pode ter mais de 250 caracteres.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Conteúdo]</td>
      <td>
        <p>Insira ou mapeie o conteúdo da oferta que será exibido para o usuário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Insira ou mapeie a ID do espaço de trabalho associado à oferta. Se deixado em branco, a oferta é associada ao espaço de trabalho padrão da conta. Essa funcionalidade aplica-se somente a contas do [!DNL Target] Premium.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Insira ou mapeie a data e a hora em que esta oferta foi modificada.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--

##### Audience fields

>[!NOTE]
>
>Audiences created through Workfront Fusion can only be edit in Fusion or through the API. They cannot be edited from within Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this audience. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Description]</td>
      <td>
        <p>Enter or map a description of this audience.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Origin]</td>
      <td>
        <p>Select whether this audience's origin is from Target or from the cloud.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Target Rule]</td>
      <td>
        <p>Enable the toggle to make rules AND, that is, all rules must be applied.</p>
        <p>For each rule that you want to apply to the audience, click <b>[!UICONTROL Add item]</b> and enter the JSON of the rule you want to apply. </p>
        <div class="example"><span class="autonumber"><span><b>Example: </b></span></span>
          <p>Example 1:</p>
          <p ><code>&lbrace;</code></p>
                    <p ><code>                "page": "url",</code>
                    </p>
                    <p><code>                "equals":&lbrack;</code>
                    </p>
                    <p ><code>                    "http://www.myhomepage.com/"</code>
                    </p>
                    <p><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;,</code>
                    </p>
                    <p>Example 2</p>
                    <p ><code>            &lbrace;</code>
                    </p>
                    <p><code>                "geo": "region",</code>
                    </p>
                    <p><code>                "matches": &lbrack;</code>
                    </p>
                    <p ><code>                    "california"</code>
                    </p>
                    <p ><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;</code>
                    </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Enter or map the ID of the workspace associated with the audience. If left blank, the offer is associated with the default workspace of the account. This functionality applies only to [!DNL Target Premium] accounts.</p>
      </td>
    </tr>
  </tbody>
</table>

-->

#### [!UICONTROL Fazer uma chamada de API personalizada]

Este módulo faz uma chamada de API personalizada para a API [!DNL Adobe Target].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Target], consulte <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Target]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL [!DNL Target] URL Base]</td>
      <td>Insira ou mapeie sua URL de base [!DNL Target].</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Caminho]</p>
      </td>
      <td>
        <p>Insira um caminho relativo a {baseURL}/</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Método]</p>
      </td>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cabeçalhos]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização e cabeçalhos x-api-key automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cadeia de Consulta]  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL Excluir um registro]

Esse módulo de ação exclui uma única atividade AB, atividade XT, Oferta ou Público-alvo.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Conexão]</td>
    <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Target], consulte <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Target]</a> neste artigo.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Tipo de registro]</td>
    <td>Selecione o tipo de registro que deseja excluir.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL ID de Registro]</td>
    <td>Informe ou mapeie a ID do registro que deseja deletar.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Ler um registro]

Este módulo de ação recupera dados para uma única Atividade, Oferta, Público-alvo, Propriedade ou Relatório.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Conexão]</td>
    <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Target], consulte <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Target]</a> neste artigo.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Tipo de registro]</td>
    <td>Selecione o tipo de registro que deseja ler.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL ID de Registro]</td>
    <td>Insira ou mapeie a ID do registro que deseja ler.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Atualizar um registro]

Este módulo de ação atualiza um registro no Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Target], consulte <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Target]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de registro]</td>
      <td>
        <p>Selecione o tipo de registro que deseja atualizar.</p>
       </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nomes de campos]</td>
      <td>Selecione os campos que deseja atualizar. Os campos são exibidos abaixo de.
          <p>Para obter detalhes sobre campos, consulte <a href="https://developer.adobe.com/target/administer/admin-api/">a documentação da API do Adobe Target</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

### Pesquisas

* [[!UICONTROL Obter registros]](#get-records)

* [[!UICONTROL Pesquisa]](#search)


#### [!UICONTROL Obter registros]

Este módulo de pesquisa recupera uma lista de registros do tipo selecionado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
      <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Target], consulte <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Target]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de registro]</td>
      <td>Selecione o tipo de registro que deseja atualizar.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Classificar por]</td>
      <td>Para cada campo pelo qual você deseja classificar, clique em <b>[!UICONTROL Adicionar item]</b> e selecione o campo e se os resultados retornados devem ser crescentes ou decrescentes.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Inicia Em]</td>
      <td>
        <p>Insira a data mais antiga para a qual você deseja recuperar registros. </p>
        <p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Termina Em]</td>
      <td>
        <p>Insira a última data para a qual deseja recuperar registros. </p>
        <p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Pesquisa]

Este módulo de pesquisa pesquisa por Atividades, Ofertas ou Públicos-alvo com base nos critérios especificados.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Conexão]</td>
    <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Target], consulte <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Target]</a> neste artigo.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Tipo de registro]</td>
    <td>Selecione o tipo de registro que deseja atualizar.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Classificar por]</td>
    <td>Para cada campo pelo qual você deseja classificar, clique em <b>[!UICONTROL Adicionar item]</b> e selecione o campo e se os resultados retornados devem ser crescentes ou decrescentes.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Pesquisar critérios]</td>
    <td>Para cada regra que você deseja configurar, selecione o campo, o operador e o valor. Clique em <b>[!UICONTROL Adicionar regra AND]</b> para criar regras adicionais.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Deslocamento]</td>
    <td>
      <p>Insira o número da primeira resposta que você deseja que o módulo retorne. A primeira resposta retornada tem um deslocamento de <code>0</code>. Use este campo em combinação com o campo [!UICONTROL Número máximo de resultados retornados] para paginar as respostas.</p>
      <p>Por exemplo, para ver a terceira página de respostas, quando cada página tiver dez respostas, defina [!UICONTROL Deslocamento] como 20 e [!UICONTROL Número máximo de resultados retornados] como 10.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limite]</td>
    <td>
      <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário. Use este campo em combinação com o campo [!UICONTROL Deslocamento] para paginar as respostas.</p>
      <p>Por exemplo, para ver a terceira página de respostas, quando cada página tiver dez respostas, defina [!UICONTROL Deslocamento] como 20 e [!UICONTROL Número máximo de resultados retornados] como 10.</p>
    </td>
  </tr>
</tbody>
</table>
