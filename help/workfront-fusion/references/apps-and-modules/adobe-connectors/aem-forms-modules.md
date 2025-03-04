---
title: Módulos do Adobe Experience Manager Forms
description: Com o conector  [!DNL Adobe Experience Manager Forms] para [!DNL Adobe Workfront Fusion], you can start a scenario based on events in your [!DNL Adobe Experience Manager Forms] conta, crie, carregue e atualize ativos e copie ou mova pastas e ativos.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 1%

---

# [!DNL Adobe Experience Manager Forms] módulos

Com o conector [!DNL Adobe Experience Manager Forms] para [!DNL Adobe Workfront Fusion], você pode iniciar um cenário com base em eventos na sua conta [!DNL Adobe Experience Manager Forms] criando um webhook.

Você pode configurar um formulário no [!DNL Adobe Experience Manager Forms] para enviar envios de formulários para este webhook.

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
   <td> <p>[!UICONTROL Plano], [!UICONTROL Trabalho]</p> </td> 
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

## Pré-requisitos

* Você deve ter uma conta [!DNL Adobe Experience Manager Forms] para usar este módulo.

## Informações da API do Adobe Experience Manager Assets

O conector do Adobe Experience Manager Assets usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.2.27</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com o Adobe Experience Manager Forms

Para criar uma conexão para seus módulos do [!DNL Adobe Experience Manager Forms]:

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
        <td>
          <p>Selecione se essa conexão se conecta a um ambiente de Produção ou Não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>
          <p>Selecione se esta é uma conta de serviço ou uma conta pessoal.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL URL da instância sem barra à direita]</td>
        <td>
          <p>Insira o URL que você usa para acessar a conta, sem a barra final.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ponto de extremidade IMS]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
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
        <td role="rowheader">[!UICONTROL ID da Organização]</td>
        <td>Insira sua ID da organização [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID da conta técnica]</td>
        <td>Insira sua ID de conta técnica do [!DNL Adobe]. Isso pode ser encontrado na seção [!UICONTROL Credentials details] do [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Metaescopos]</td>
        <td>Insira qualquer metaescopo apropriado       </td>
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

## Módulo Adobe Experience Manager Forms e seus campos

Atualmente, há apenas um módulo no conector do Adobe Experience Manager Forms.

### Aguardar eventos de formulário

Esse acionador instantâneo (webhook) permite iniciar um cenário quando uma ação Enviar ocorre em um Formulário do Adobe Experience Manager.

>[!IMPORTANT]
>
>Esse módulo também requer configuração no Adobe Experience Manager. Após configurar este webhook, você deve abrir o Adobe Experience Manager e configurar seu formulário para enviar envios para o webhook.
>
><!--For instructions on the required form configuration, see insert url here-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Webhook]</td> 
   <td> <p>Insira um nome para o webhook</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">Criar uma conexão com o [!DNL Adobe Experience Manager Forms]</a></p> </td> 
  </tr>

O módulo cria um webhook e fornece o endereço do webhook, que você pode inserir na caixa de diálogo de envio do formulário em [!DNL Adobe Experience Manager Forms].
