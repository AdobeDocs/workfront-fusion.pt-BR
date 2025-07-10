---
title: Exibir e resolver execuções incompletas
description: A pasta [!UICONTROL Execuções incompletas] armazena execuções de cenário que não foram finalizadas com êxito devido a um erro. Cada execução incompleta armazenada pode ser resolvida manual ou automaticamente.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: f2ddf62d660c4709f1e7e59c4302cde5b062725f
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 5%

---

# Exibir e resolver execuções incompletas

A pasta [!UICONTROL Execuções incompletas] armazena execuções de cenário que não foram finalizadas com êxito devido a um erro. Cada execução incompleta armazenada pode ser resolvida manual ou automaticamente.

>[!NOTE]
>
>Por padrão, o armazenamento de execuções incompletas é desativado. Para habilitá-lo, habilite a opção [!UICONTROL Permitir o armazenamento de execuções incompletas] nas configurações avançadas de cenário.
>
>Para obter mais informações sobre configurações de cenário, consulte [Definir configurações de cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacote</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença</td> 
   <td> <p>Novo: [!UICONTROL Padrão]</p><p>Ou</p><p>Atual: [!UICONTROL Trabalho] ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Plano [!DNL Workfront] da [!UICONTROL Select] ou da [!UICONTROL Prime]: sua organização deve comprar [!DNL Adobe Workfront Fusion].</li><li>Plano [!DNL Workfront] da [!UICONTROL Ultimate] [!DNL Workfront Fusion] incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso*</td> 
   <td> 
     <p>Você deve ser um administrador do [!DNL Workfront Fusion] para sua organização.</p>
     <p>Você deve ser um administrador [!DNL Workfront Fusion] para sua equipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Exibir execuções incompletas

Se um módulo encontrar um erro durante sua operação, uma nova execução incompleta será adicionada à pasta Incomplete executions. Cada execução incompleta contém o blueprint do cenário e todos os pacotes que podem ser mapeados no módulo com falha. É possível abrir a lista de execuções incompletas clicando na guia [!UICONTROL Execuções Incompletas] na página de detalhes do cenário.

<!--

![Incomplete executions tab](assets/incomplete-executions-tab-350x102.png)

-->

Para obter mais informações, consulte [Erros que resultam em execuções incompletas](#errors-resulting-into-incomplete-executions) neste artigo.

>[!NOTE]
>
>O limite de tamanho atual da pasta de execuções incompletas não resolvidas por cenário é de 10 MB. Se o cenário exceder esse limite, você poderá ver o seguinte erro:
>
>`DLQ limit per scenario has been exceeded`
>
>As equipes são limitadas a um total de 500 MB para todas as execuções incompletas não resolvidas.
>
>Para obter mais informações, consulte [Habilitar perda de dados](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) no artigo Definir configurações de cenário.


## Resolver execuções incompletas na guia Execuções incompletas

Quando uma nova execução incompleta é armazenada, você pode resolvê-la da seguinte maneira:

1. Abra o cenário afetado.
1. Clique na guia **[!UICONTROL Execuções incompletas]**.
1. Localize a execução incompleta que você deseja resolver e clique em **[!UICONTROL Detalhes]**.
1. Abra o registro do módulo em que todas as operações do módulo são exibidas.
1. Localize a operação com falha e clique em **[!UICONTROL Resolver]**:

   ![Botão Resolver](assets/resolve-btn-350x188.png)



## Resolver execuções incompletas na guia Histórico

Se quiser ver o log de todas as operações do módulo antes de tentar resolver a execução incompleta, você poderá resolver a execução incompleta na pasta [!UICONTROL Histórico]:

1. Abra o cenário afetado.
1. Clique na guia **[!UICONTROL Histórico]**.
1. Localize a execução com falha do cenário e clique em **[!UICONTROL Detalhes]**.
1. Abra o registro do módulo em que todas as operações do módulo são exibidas.
1. Localize a operação com falha e clique em **[!UICONTROL Resolver]**:

   ![Botão Resolver](assets/resolve-btn-350x188.png)

## Opções relacionadas a execuções incompletas

As seguintes opções no painel [!UICONTROL Configurações de cenário] determinam se e como as execuções incompletas são armazenadas:

* Permitir o armazenamento de execuções incompletas
* Processamento sequencial
* Ativar perda de dados

Para obter mais informações sobre essas opções, consulte [Definir configurações de cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Erros que resultam em execuções incompletas

Há várias categorias de erros que resultam no armazenamento de execuções incompletas. Estas podem incluir:

* Erros de validação decorrentes de dados incompletos ou errôneos, principalmente por causa de um item ausente esperado para processar com êxito todos os dados que passam por um módulo.
* Erros que ocorrem devido à indisponibilidade do destino final devido a uma falha temporária ou de longa duração na conexão (por exemplo, durante a conexão com o servidor de email ou FTP remoto).

Se ocorrer um erro no primeiro módulo do cenário, a execução será interrompida imediatamente e nenhuma execução incompleta será armazenada.

Se ocorrer um erro em qualquer outro módulo e não houver nenhuma rota de manipulador de erros anexada, uma das seguintes situações ocorrerá:

* Um registro de execução incompleto com repetição automática é armazenado para os seguintes tipos de erro:

   * `ConnectionError`
   * `RateLimitError`
   * `OutOfSpaceError`
   * `ModuleTimeoutError`

* Um registro de execução incompleto sem repetição automática é armazenado para os seguintes tipos de erro:

   * `DataError`
   * `InvalidConfigurationError`
   * `InvalidAccessTokenError`
   * `UnexpectedError`
   * `MaxFileSizeExceededError`
   * `MaxResultsExceededError`

* Se o tipo de erro for diferente dos mencionados acima, a execução falhará.
