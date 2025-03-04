---
title: Módulos do Adobe Journey Optimizer
description: Em um cenário  [!DNL Adobe Workfront Fusion] , é possível automatizar fluxos de trabalho que usam  [!DNL Adobe Journey Optimizer], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 1d0ccf4d-9f06-4210-86ec-7da7970f6a47
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '3704'
ht-degree: 0%

---

# [!DNL Adobe Journey Optimizer] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Adobe Journey Optimizer], bem como conectá-los a vários aplicativos e serviços de terceiros. Os módulos do [!DNL Adobe Journey Optimizer] permitem criar, ler, atualizar ou excluir registros, ou executar uma chamada de API personalizada para a API [!DNL Adobe Journey Optimizer].


Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
      <td>
        <p>[!UICONTROL Pro] ou superior</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
      <td>
        <p>[!UICONTROL Plano], [!UICONTROL Trabalho]</p>
      </td>
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
   <p>Requisito atual do produto: se você tiver o Plano [!DNL Adobe Workfront] da [!UICONTROL Select] ou da [!UICONTROL Prime], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!DNL Workfront] da [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td>
    </tr>
  </tbody>
</table>


Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Antes de usar o conector [!DNL Adobe Journey Optimizer], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!DNL Adobe Journey Optimizer] ativa.

## Informações da API do Adobe Journey Optimizer

O conector do Adobe Journey Optimizer usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>{{connection.url}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.7.11</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com o Adobe Journey Optimizer

Você pode criar uma conexão em qualquer módulo do Adobe Journey Optimizer.

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
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID do Cliente]</td>
        <td>Insira sua [!UICONTROL Adobe] [!UICONTROL ID do cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
        <td>Insira seu [!DNL Adobe] [!UICONTROL Segredo do Cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID da Organização]</td>
        <td>Insira sua [!DNL Adobe] [!UICONTROL ID da Organização]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Nome da Sandbox]</td>
        <td>Insira o nome da sandbox que essa conexão usará.</td>
        </tr>
      </tbody>
    </table>



   <!--Markdown 0032 placeholder-->


## [!DNL Adobe Journey Optimizer] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Journey Optimizer], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Journey Optimizer] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Gerenciamento de configuração](#configuration-management)
* [Gerenciamento de pacotes](#package-management)
* [Gerenciamento de registros](#record-management)
* [Gerenciamento de mensagens](#message-management)
* [Verificações de status](#status-checks)
* [Pesquisas](#searches)
* [Outro](#other)




### Gerenciamento de configuração

* [Criar uma configuração](#create-a-configuration)
* [Implantar uma configuração](#deploy-a-configuration)
* [Atualizar uma configuração](#update-a-configuration)
* [Cancelar implantação de uma configuração](#undeploy-a-configuration)
* [Verificar se a configuração pode ser implantada](#check-if-configuration-can-be-deployed)
* [Excluir uma configuração](#delete-a-configuration)
* [Obter uma configuração](#get-a-configuration)

#### Criar uma configuração

Este módulo de ação cria uma configuração de limitação ou endpoint de limitação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de configuração]</td> 
   <td>Selecione se você está criando uma configuração de limitação ou uma configuração de limitação.<ul><li><p><b>Limite</b></p>Continue com <a href="#capping-fields" class="MCXref xref" >Campos de limite</a>.</li><li><p><b>Limitação</b></p>Continue para <a href="#throttling-fields" class="MCXref xref" >Campos de limitação</a>.</li></ul></td> 
  </tr> 
   </tbody> 
</table>

##### Campos de limite

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira ou mapeie o URL do endpoint que você deseja configurar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Organização IMS]</td> 
   <td>Insira ou mapeie a ID do Adobe IMS da organização.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Métodos]</td> 
   <td>Selecione os métodos a serem usados nessa configuração.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Serviço]</td> 
   <td>Selecione se você está usando uma ação ou uma fonte de dados para essa configuração.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Máximo de conexões HTTP]</td> 
   <td>Insira ou mapeie o número máximo de conexões simultâneas para este ponto de extremidade.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Máximo de chamadas]</td> 
   <td>Insira ou mapeie o número máximo de chamadas a serem executadas no período especificado no campo Time period.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Período (milissegundos)]</td> 
   <td>Insira ou mapeie o número de milissegundos relacionado ao campo Maximum calls.</td> 
  </tr> 
 </tbody> 
</table>

##### Campos de limitação

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td>Insira ou mapeie um nome para esta configuração.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td>Insira ou mapeie uma descrição para esta configuração.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Padrão de URL]</td> 
   <td>Insira ou mapeie o URL do ponto de extremidade que deseja limitar.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Métodos]</td> 
   <td>Selecione os métodos a serem usados nessa configuração.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Taxa de transferência máxima]</td> 
   <td>Selecione se você está usando uma ação ou uma fonte de dados para essa configuração.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Máximo de conexões HTTP]</td> 
   <td>Insira ou mapeie o número máximo de conexões simultâneas para este ponto de extremidade.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Máximo de chamadas]</td> 
   <td>Insira ou mapeie a taxa de transferência máxima desejada para esse endpoint. Esse valor deve estar entre 200 e 5000.</td> 
  </tr> 
 </tbody> 
</table>

#### Implantar uma configuração

Este módulo de ação implanta a configuração de limitação ou limitação especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de configuração]</td> 
   <td>Selecione se você está implantando uma configuração de limitação ou uma configuração de limitação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Configuração]</td> 
   <td>Insira ou mapeie a ID da configuração que deseja implantar.</td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar uma configuração

Este módulo de ação atualiza a configuração de limitação ou limitação especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de configuração]</td> 
   <td>Selecione se você está atualizando uma configuração de limitação ou uma configuração de limitação.<ul><li><p><b>Limite</b></p>Para campos, consulte <a href="#capping-fields" class="MCXref xref" >Limite de campos</a> na seção Criar uma configuração deste artigo.</li><li><p><b>Limitação</b></p>Para campos, consulte <a href="#throttling-fields" class="MCXref xref" >Limitação de campos</a> na seção Criar uma configuração deste artigo.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

#### Cancelar implantação de uma configuração

Este módulo de ação desimplanta uma configuração de limitação. O estado de configuração é alterado de volta para o estado anterior à implantação (`created` ou `updated`).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de configuração]</td> 
   <td>Selecione se você está desimplantando uma configuração de limitação ou uma configuração de limitação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Configuração]</td> 
   <td>Insira ou mapeie a ID da configuração que deseja desimplantar.</td> 
  </tr> 
 </tbody> 
</table>

#### Verificar se a configuração pode ser implantada

Este módulo de ação verifica se uma configuração de limitação ou limitação pode ser implantada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de configuração]</td> 
   <td>Selecione se você está verificando uma configuração de limitação ou uma configuração de limitação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Configuração]</td> 
   <td>Insira ou mapeie a ID da configuração que você deseja verificar.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir uma configuração

Este módulo de ação exclui uma configuração de limitação ou endpoint de limitação.

Se a configuração tiver sido implantada, ela deverá ser desimplantada antes de ser excluída.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de configuração]</td> 
   <td>Selecione se você está excluindo uma configuração de limitação ou uma configuração de limitação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Configuração]</td> 
   <td>Insira ou mapeie a ID da configuração que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Obter uma configuração

Este módulo de ação retorna a configuração de limitação identificada pela ID especificada. A definição mais recente é retornada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de configuração]</td> 
   <td>Selecione se você está recuperando uma configuração de limitação ou uma configuração de limitação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Configuração]</td> 
   <td>Insira ou mapeie a ID da configuração que deseja recuperar.</td> 
  </tr> 
 </tbody> 
</table>




### Gerenciamento de pacotes

* [Criar um pacote](#create-a-package)
* [Atualizar um pacote](#update-a-package)
* [Excluir um pacote](#delete-a-package)
* [Pesquisar um pacote](#look-up-a-package)
* [Importar um pacote](#import-a-package)
* [Publicar um pacote](#publish-a-package)
* [Enviar uma importação](#submit-an-import)



#### Criar um pacote

Esse módulo de ação cria um pacote de vários artefatos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td>Insira ou mapeie um nome para o pacote.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td>Insira ou mapeie uma descrição do pacote.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data de expiração]</td> 
   <td>Insira ou mapeie o carimbo de data e hora que define a data de expiração do pacote. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Pacote]</td> 
   <td>Selecione o tipo de pacote que deseja criar.<ul><li><p><b>Completo</b></p>O pacote incluirá todos os artefatos</p></li><li><p><b>Parcial</b></p><p>O pacote incluirá somente artefatos adicionados. </p></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artefatos]</td> 
   <td>Se você estiver criando um pacote parcial, para cada artefato que deseja adicionar, clique em <b>Adicionar artefato</b> e especifique a ID, o tipo e o título do artefato. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Sandbox]</td> 
   <td>Insira ou mapeie o Nome e a ID da Organização IMS da sandbox que contém os itens que você deseja que o pacote contenha.</td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um pacote

Esse módulo de ação adiciona ou exclui artefatos de um pacote ou atualiza metadados do pacote.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar ação]</td> 
   <td>Selecione a ação que deseja realizar.<ul><li><p><b>Adicionar artefato</b></p><p>Para cada artefato que você deseja adicionar, clique em <b>Adicionar artefato</b>, especifique a ID, o tipo e o título do artefato e insira ou mapeie a data de expiração do pacote. </p></li><li><p><b>Excluir artefato</b></p><p>Para cada artefato que você deseja excluir, clique em <b>Adicionar artefato</b> e especifique a ID, o tipo e o título do artefato. </p></li><li><p><b>Atualizar metadados</b></p><p>Insira novos valores para o nome, a descrição, o nome da sandbox de origem ou a ID da organização IMS.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um pacote

Esse módulo de ação exclui um pacote de vários artefatos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Pacote]</td> 
   <td>Insira ou mapeie a ID do pacote que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Pesquisar um pacote

Este módulo de ação recupera detalhes do pacote especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Pacote]</td> 
   <td>Insira ou mapeie a ID do pacote do qual deseja retornar detalhes.</td> 
  </tr> 
 </tbody> 
</table>

#### Importar um pacote

Este módulo de ação busca os objetos conflitantes na sandbox de destino especificada. Objetos conflitantes representam objetos semelhantes que já estão presentes na sandbox de destino.

Você deve publicar um pacote antes de importá-lo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Pacote]</td> 
   <td>Insira ou mapeie a ID do pacote que você deseja importar.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Sandbox de destino]</td> 
   <td>Insira ou mapeie o nome da sandbox onde deseja importar o pacote.</td> 
  </tr> 
 </tbody> 
</table>

#### Publicar um pacote

Você deve publicar um pacote antes de importá-lo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Pacote]</td> 
   <td>Insira ou mapeie a ID do pacote que deseja publicar.</td> 
  </tr> 
 </tbody> 
</table>

#### Enviar uma importação

Este módulo de ação envia uma importação para um pacote após você ter revisado conflitos e fornecido substituições. O resultado é fornecido como uma carga, o que inicia o trabalho de importação para a sandbox de destino, conforme especificado na carga.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Pacote]</td> 
   <td>Insira ou mapeie a ID do pacote que deseja publicar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td>Insira ou mapeie um nome para o trabalho de importação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td>Insira ou mapeie uma descrição do trabalho de importação</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Nome da sandbox de destino)]</td> 
   <td>Insira ou mapeie o nome da sandbox para a qual você está enviando a importação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (sandbox de destino) IMS Org ID]</td> 
   <td>Insira ou mapeie a ID organizacional do Adobe IMS para a sandbox para a qual você está enviando a importação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (sandbox Source) ID]</td> 
   <td>Insira ou mapeie a ID da sandbox que contém o pacote que você deseja publicar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (sandbox Source) Type]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (sandbox Source) Link]</td> 
   <td>Insira ou mapeie o link para o pacote que deseja publicar.</td> 
  </tr> 
 </tbody> 
</table>


<!--

### Artifact management

* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)

#### Copy artifacts synchronously

This action module copies artifacts from a source sandbox into a destination sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination sandbox]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to copy, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

#### Export Artifacts asynchronously

This action module exports artifacts from the specified sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to export, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



#### Import Artifacts asynchronously

This action module imports a snapshot containing artifacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Snapshot ID]</td> 
   <td>Enter or map the ID of the snapshot you want to import.</td> 
  </tr> 
 </tbody> 
</table>

-->

### Gerenciamento de registros

* [Criar um registro](#create-a-record)
* [Atualizar um registro](#update-a-record)
* [Excluir um registro](#delete-a-record)
* [Corrigir um registro](#patch-a-record)
* [Obter um registro](#get-a-record)

#### Criar um registro

Esse módulo de ação cria um novo modelo de conteúdo ou fragmento de conteúdo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de conteúdo]</td> 
   <td>Selecione se você está criando um modelo de conteúdo ou um fragmento de conteúdo.<ul><li><p><b>Modelo de conteúdo</b></p>Continue para <a href="#template-fields" class="MCXref xref" >Campos de modelo</a>.</li><li><p><b>Fragmento do conteúdo</b></p>Continue em <a href="#fragment-fields" class="MCXref xref" >Campos de fragmento</a>.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

##### Campos de modelo

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td>Insira ou mapeie um nome para este modelo de conteúdo.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td>Insira ou mapeie uma descrição para este modelo de conteúdo.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td>Selecione o tipo de modelo que deseja criar.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canais]</td> 
   <td>Selecione os canais incluídos neste modelo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Origem do modelo de conteúdo]</td> 
   <td>Selecione a origem deste modelo.</td>  
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadados]</td> 
   <td>Para incluir propriedades personalizadas no novo modelo, selecione "Adicionar metadados" e insira ou mapeie a chave e o valor dos metadados. Repita o procedimento para cada campo personalizado que deseja incluir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL HTML de email]</td> 
   <td>Insira ou mapeie a HTML do email incluído neste modelo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contexto do Editor]</td> 
   <td>Para incluir propriedades personalizadas no email, selecione "Adicionar contexto do editor" e insira ou mapeie a chave e o valor do contexto. Repita o procedimento para cada campo personalizado que deseja incluir.</td> 
  </tr> 
 </tbody> 
</table>

##### Campos de fragmento

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Nome]</td> 
   <td>Insira ou mapeie um nome para este fragmento de conteúdo.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td>Insira ou mapeie uma descrição para este fragmento de conteúdo.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td>Selecione o tipo de modelo que deseja criar.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canais]</td> 
   <td>Selecione os canais incluídos neste modelo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Origem do fragmento de conteúdo]</td> 
   <td>Selecione a origem desse fragmento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadados]</td> 
   <td>Para incluir propriedades personalizadas no novo modelo, selecione "Adicionar metadados" e insira ou mapeie a chave e o valor dos metadados. Repita o procedimento para cada campo personalizado que deseja incluir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conteúdo]</td> 
   <td>Insira ou mapeie o conteúdo do fragmento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contexto do Editor]</td> 
   <td>Para incluir propriedades personalizadas no email, selecione "Adicionar contexto do editor" e insira ou mapeie a chave e o valor do contexto. Repita o procedimento para cada campo personalizado que deseja incluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um registro

Esse módulo de ação atualiza um modelo ou fragmento de conteúdo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de conteúdo]</td> 
   <td>Selecione se você está atualizando uma configuração de limitação ou uma configuração de limitação.<ul><li><p><b>Modelo</b></p>Para campos, consulte <a href="#template-fields" class="MCXref xref" >Campos de modelo</a> na seção Criar um registro deste artigo.</li><li><p><b>Fragmento</b></p>Para campos, consulte <a href="#fragment-fields" class="MCXref xref" >Campos de fragmento</a> na seção Criar um registro deste artigo.</li></ul></td> 
  </tr> 
  </tbody> 
  </table>

#### Excluir um registro

Esse módulo de ação exclui um modelo de conteúdo ou fragmento de conteúdo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de conteúdo]</td> 
   <td>Selecione se você está excluindo um modelo de conteúdo ou fragmento de conteúdo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Modelo/Fragmento]</td> 
   <td>Insira ou mapeie a ID do modelo ou fragmento que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Corrigir um registro

Este módulo de ação atualiza um registro usando PATCH com formato de ponteiro JSON

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de conteúdo]</td> 
   <td>Selecione se você está corrigindo um modelo de conteúdo ou fragmento de conteúdo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Modelo/Fragmento]</td> 
   <td>Insira ou mapeie a ID do modelo ou fragmento que deseja corrigir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dados de carga]</td> 
   <td>Para adicionar um registro à carga deste patch: <ol><li>Clique em <b>Adicionar um registro</b>.</li><li>Selecione a operação: Adicionar, Remover ou Substituir.</li><li>No campo Caminho, selecione se deseja corrigir o nome ou a descrição.</li><li> No campo De, insira ou mapeie uma string que contenha um valor de ponteiro JSON.</li><li>No campo Valor, informe o valor a ser usado na operação.</li></ol></td> 
  </tr> 
 </tbody> 
</table>

#### Obter um registro

Esse módulo de ação retorna o modelo de conteúdo ou o fragmento de conteúdo identificado pela ID especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de conteúdo]</td> 
   <td>Selecione se você está recuperando um modelo de conteúdo ou fragmento de conteúdo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Modelo/Fragmento]</td> 
   <td>Insira ou mapeie a ID do modelo ou fragmento que deseja recuperar.</td> 
  </tr> 
 </tbody> 
</table>


### Gerenciamento de mensagens

* [Acionar uma execução de mensagem unitária](#trigger-a-unitary-message-execution)
* [Acionar uma mensagem baseada em público](#trigger-an-audience-based-message)
* [Verificar o status de uma mensagem baseada em público-alvo](#check-the-status-for-audience-based-message)



#### Acionar uma execução de mensagem unitária

Esse módulo de ação aciona uma mensagem unitária para os recipients especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Solicitação]</td> 
   <td>Insira ou mapeie a ID da solicitação associada a esta mensagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da campanha]</td> 
   <td>Insira ou mapeie a ID da campanha associada a esta mensagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destinatários]</td> 
   <td>Para cada destinatário que você deseja receber esta mensagem, clique em <b>Adicionar destinatário</b> e insira o seguinte:
   <ul>
   <li><p><b>Tipo</b></p>Selecione <code>aep</code>.</li>
   <li><p><b>ID de usuário</b></p>Insira ou mapeie o identificador de perfil do Adobe Experience Platform do recipient.</li>
   <li><p><b>Namespace</b></p>Insira ou mapeie o namespace do perfil do Adobe Experience Platform do recipient.</li>
   <li><p><b>Endereço de email</b></p></li>
   <li><p><b>Número de celular</b></p></li>
   <li><p><b>Nome</b></p></li>
   <li><p><b>Sobrenome</b></p></li>
   <li><p><b>Produto</b></p>Insira ou mapeie o produto associado a esta mensagem. Isso é usado para substituição de variável dinâmica no conteúdo da mensagem.</li>
   </ul></td> 
  </tr> 
 </tbody> 
</table>

#### Acionar uma mensagem baseada em público

Esse módulo de ação aciona a execução de uma mensagem baseada no público-alvo, com base na solicitação e na campanha especificadas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Solicitação]</td> 
   <td>Insira ou mapeie a ID da solicitação associada a esta mensagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da campanha]</td> 
   <td>Insira ou mapeie a ID da campanha associada a esta mensagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Produto]</td> 
   <td>Insira ou mapeie o produto associado a esta mensagem. Isso é usado para substituição de variável dinâmica no conteúdo da mensagem.</td> 
  </tr> 
 </tbody> 
</table>

#### Verificar o status de mensagem baseada em público-alvo

Este módulo de ação verifica o status de uma mensagem em lote com base no público-alvo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de execução de mensagem]</td> 
   <td>Insira ou mapeie a ID da execução da mensagem que deseja verificar.</td> 
  </tr> 
 </tbody> 
</table>

### Verificações de status

<!--* [Check service health](#check-service-health)-->
* [Verifique as dependências de importação](#check-the-import-dependencies)
* [Verificar o status de um trabalho de importação](#check-the-status-of-an-import-job)

<!--

#### Check service health

This action module checks that the service represented by the connection is running.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
 </tbody> 
</table>

-->

#### Verifique as dependências de importação

Esse módulo de ação verifica as dependências para artefatos do pacote. Isso permite verificar se você tem permissões para importar artefatos de pacote.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Pacote]</td> 
   <td>Insira ou mapeie a ID do pacote para o qual deseja verificar permissões.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sandbox de destino]</td> 
   <td>Insira ou mapeie o nome da sandbox para a qual deseja importar o pacote.</td> 
  </tr> 
 </tbody> 
</table>

#### Verificar o status de um trabalho de importação

Esse módulo de ação verifica se um trabalho de importação foi bem-sucedido ou falhou.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Trabalho]</td> 
   <td>Insira ou mapeie a ID do trabalho para o qual deseja recuperar dados.</td> 
  </tr> 
 </tbody> 
</table>

### Pesquisas

* [Listar todos os objetos dependentes](#list-all-dependent-objects)
* [Configurações de lista](#list-configurations)
* [Listar trabalhos de exportação e importação](#list-export-and-import-jobs)
* [Listar pacotes](#list-packages)
* [Listar registros](#list-records)

#### Listar todos os objetos dependentes

Este módulo de pesquisa lista todos os objetos dependentes para objetos no pacote especificado

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objetos de Pacote]</td> 
   <td>Para cada objeto do pacote para o qual você deseja retornar um objeto dependente, clique em <b>Adicionar objeto</b> e insira o nome e o tipo do objeto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Pacote]</td> 
   <td>Informe ou mapeie o ID do pacote para o qual você deseja listar objetos dependentes.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Sandbox de destino]</td> 
   <td>Insira ou mapeie o nome da sandbox que contém o pacote para o qual você deseja listar objetos dependentes.</td> 
  </tr> 
 </tbody> 
</table>

#### Configurações de lista

Este módulo de ação lista todas as configurações de limitação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de configuração]</td> 
   <td>Selecione se deseja listar configurações de limite ou configurações de limitação.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar trabalhos de exportação e importação

Este módulo de pesquisa lista a tarefa de exportação e importação atual. Você pode usar parâmetros de consulta para filtrar a lista.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Iniciar]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de resultados retornados]</td> 
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordenar por]</td> 
      <td>Selecione se os resultados devem ser ordenados por data de criação ou data de modificação.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Parâmetro de consulta]</td> 
   <td>Para cada parâmetro de consulta pelo qual você deseja filtrar, clique em <b>Adicionar parâmetro de consulta</b>, selecione o campo e o operador e insira o valor do campo para o filtro.</td> 
  </tr> 
 </tbody> 
</table>



#### Listar pacotes

Este módulo de pesquisa lista todos os pacotes em sua organização. Você pode usar parâmetros de consulta para filtrar a lista.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Iniciar]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de resultados retornados]</td> 
      <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordenar por]</td> 
      <td>Selecione se os resultados devem ser ordenados por data de criação ou data de modificação.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Parâmetro de consulta]</td> 
   <td>Para cada parâmetro de consulta pelo qual você deseja filtrar, clique em <b>Adicionar parâmetro de consulta</b>, selecione o campo e o operador e insira o valor do campo para o filtro.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar registros

Este módulo de pesquisa lista todas as configurações de limitação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar tipo de conteúdo]</td> 
   <td>Selecione se você está recuperando um modelo de conteúdo ou fragmento de conteúdo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordenar por]</td> 
   <td>Informe ou mapeie o nome do parâmetro pelo qual deseja classificar esta lista. Adicione <code>-</code> ou <code>+</code> para classificar em ordem decrescente ou crescente. Se nenhum sinal for especificado, a lista será classificada em ordem decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Iniciar]</td> 
   <td>Esse campo é usado para paginação. Insira ou mapeie os critérios da próxima página com relação à propriedade especificada no campo Ordenar por.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordenar por]</td> 
   <td>Informe ou mapeie o nome do parâmetro pelo qual deseja classificar esta lista. Adicione <code>-</code> ou <code>+</code> para classificar em ordem decrescente ou crescente. Se nenhum sinal for especificado, a lista será classificada em ordem decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtrar por propriedade]</td> 
   <td>Para cada filtro de propriedade que você deseja adicionar, clique em <b>Adicionar item</b> e insira a chave e o valor da propriedade. Os registros que incluem o valor especificado para a propriedade são incluídos na lista.</td> 
  </tr> 
 </tbody> 
</table>


### Outro


#### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada de API personalizada para a API do Adobe Journey Optimizer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Conexão]</td>
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Adobe Journey Optimizer], consulte <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Criar uma conexão com [!DNL Adobe Journey Optimizer]</a> neste artigo.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Insira um caminho relativo ao URL de base.</p>
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
        <p>[!DNL Workfront Fusion] adiciona a autorização, <code>x-api-key</code> e <code>x-gw-ims-org-id</code> cabeçalhos automaticamente.</p>
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
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>







<!--

* [Check if configuration can be deployed](#check-if-configuration-can-be-deployed)
* [Check service health](#check-service-health)
* [Check the import dependencies](#check-the-import-dependencies)
* [Check the status for audience-based message](#status-for-audience-based-message)
* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Create a configuration](#create-a-configuration)
* [Create a package](#create-a-package)
* [Create a record](#create-a-record)
* [Delete a configuration](#delete-a-configuration)
* [Delete a package](#delete-a-package)
* [Delete a record](#delete-a-record)
* [Deploy a configuration](#deploy-a-configuration)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Get a configuration](#get-a-configuration)
* [Get a record](#get-a-record)
* [Import a package](#import-a-package)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)
* [List all dependent objects](#list-all-dependent-objects)
* [List export and import jobs](#list-import-and-export-jobs)
* [Look up a package](#look-up-a-package)
* [Make a custom API call](#make-a-custom-api-call)
* [Patch a record](#patch-a-record)
* [Publish a package](#publish-a-package)
* [Submit an import](#submit-an-import)
* [Trigger a unitary message execution](#trigger-a-unitary-message-execution)
* [Trigger an audience-based message](#trigger-an-audience-based-message)
* [Undeploy a configuration](#undeploy-a-configuration)
* [Update a configuration](#update-a-configuration)
* [Update a package](#update-a-package)
* [Update a record](#update-a-record)
* [List configurations](#list-configurations)
* [List packages](#list-packages)
* [List records](#list-records)

-->
