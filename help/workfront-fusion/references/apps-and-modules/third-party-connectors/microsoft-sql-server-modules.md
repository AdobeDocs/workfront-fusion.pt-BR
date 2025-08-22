---
title: Módulos do Microsoft SQL Server
description: Você pode usar o Adobe Workfront Fusion para se conectar ao Microsoft SQL Server.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server] módulos

Você pode usar o Adobe Workfront Fusion para se conectar ao [!UICONTROL Microsoft SQL Server].

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

## Conectando o serviço [!DNL Microsoft SQL Server] ao Workfront Fusion

Para obter instruções sobre como conectar sua conta do [!DNL Microsoft SQL Server] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alguns aplicativos do Microsoft usam a mesma conexão, que está vinculada a permissões de usuário individuais. Portanto, ao criar uma conexão, a tela de consentimento de permissões exibe todas as permissões que foram concedidas anteriormente à conexão deste usuário, além de todas as novas permissões necessárias para o aplicativo atual.
>
>Por exemplo, se um usuário tiver permissões de &quot;Tabela de leitura&quot; concedidas por meio do conector do Excel e criar uma conexão no conector do Outlook para ler emails, a tela de consentimento de permissões mostrará a permissão &quot;Tabela de leitura&quot; já concedida e a permissão &quot;Gravar email&quot; recém-necessária.

## Usando módulos [!DNL Microsoft SQL Server]

Você pode executar a lógica personalizada diretamente no servidor de banco de dados por meio de procedimentos armazenados. O Adobe Workfront Fusion carrega a interface de parâmetros de entrada/saída e o conjunto de registros dinamicamente para que cada parâmetro ou valor possa ser mapeado individualmente. Antes de começar a configurar seu cenário, verifique se a conta que você está usando para se conectar ao banco de dados tem acesso de leitura às visualizações `INFORMATION_SCHEMA.ROUTINES` e `INFORMATION_SCHEMA.PARAMETERS`.

Quando [!DNL Fusion] estabelece a conexão com o destino [!DNL SQL server], o usuário [!DNL Fusion] identifica o Host (o nome de domínio ou endereço IP onde o servidor está hospedado) e a porta. O [!DNL Fusion] pode se conectar a qualquer host e porta disponíveis.

Para obter informações sobre endereços IP específicos usados pelo Workfront Fusion, consulte [Endereços IP para acessar o Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Para saber mais sobre como criar um procedimento armazenado, consulte a documentação do [!DNL Microsoft SQL Server].

>[!NOTE]
>
>O Workfront Fusion não é compatível com vários conjuntos de registros. Somente o primeiro é processado.

## Solução de problemas de erro [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Tempo limite de espera de bloqueio excedido; tente reiniciar a transação]

Esse erro ocorre quando você modifica os mesmos dados usando vários módulos. É causado por transações SQL.

Quando qualquer módulo SQL é executado, ele inicia uma transação. A transação é concluída após a execução completa do cenário.

Se outro módulo tentar acessar os mesmos dados, ele precisará aguardar até que a transação anterior seja concluída. Como a primeira transação será concluída após a conclusão do cenário, a segunda transação nunca poderá começar.

### Solução:

Ative a Confirmação automática. A confirmação automática conclui (confirma) cada transação imediatamente após a execução do módulo ser concluída.

1. Clique no ícone [!UICONTROL Configurações de cenário] ![Ícone de configurações de cenário](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png)na parte inferior da tela.
1. Clique na caixa de seleção **[!UICONTROL Confirmação automática]**.
1. Clique em **[!UICONTROL OK]** para salvar as configurações do cenário.
