---
title: Criar uma conexão - Instruções básicas
description: Muitos  [!DNL Adobe Workfront Fusion]  conectores não exigem configuração personalizada ao criar uma conexão. Este artigo descreve o processo de criação de conexão padrão.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: ef1a96d9ef4c2c82eaf376c84188e3ed6ea7b2cf
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Criar uma conexão - Instruções básicas

Muitos conectores do [!DNL Adobe Workfront Fusion] não exigem configuração personalizada ao criar uma conexão. Este artigo descreve o processo de criação de conexão padrão.

>[!NOTE]
>
>
>Se o Adobe Workfront Fusion não oferecer um aplicativo para o serviço Web que você deseja usar no cenário, é possível conectar-se ao serviço Web usando os módulos HTTP e Webhooks do [!DNL Workfront Fusion], conforme explicado nos seguintes artigos:
>
>* [Conecte o Adobe Workfront Fusion a um serviço Web que usa a autorização do token de API](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [Configurar um webhook para um serviço Web sem um conector](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licença do Adobe Workfront</td> 
   <td> <p>Novo: Padrão</p><p>Ou</p><p>Atual: trabalho ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion**</td> 
   <td>
   <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecione ou Prime Workfront Plan: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Criar uma conexão

Para criar uma conexão dentro de um módulo [!DNL Workfront Fusion]:

1. Clique em **[!UICONTROL Add]** ao lado da caixa [!UICONTROL Connection] para abrir o painel **[!UICONTROL Create a connection]**.
1. (Opcional) Altere o padrão **[!UICONTROL Connection name]**.
1. No campo Ambiente, selecione se é um ambiente de produção ou não produção. Essas informações aparecem na área Conexões do Fusion.
1. No campo Tipo, selecione se é uma conta de serviço ou pessoal. Essas informações aparecem na área Conexões do Fusion.
1. (Condicional) Se o aplicativo exigir configurações de conexão avançadas, como ID, chave ou [!UICONTROL secret], insira essas informações.

   Talvez seja necessário clicar em **[!UICONTROL Show advanced settings]** para exibir os campos nos quais você pode inserir esse tipo de informação.

1. Clique em **[!UICONTROL Continue]**.
1. Na janela de logon que é exibida, digite suas credenciais para fazer logon no aplicativo, se ainda não tiver feito.
1. (Condicional) Se um botão **[!UICONTROL Allow]** for exibido, examine as ações que o conector poderá realizar e clique no botão para conectar o aplicativo ao [!DNL Workfront Fusion].

   >[!NOTE]
   >
   >Alguns aplicativos do Microsoft usam a mesma conexão, que está vinculada a permissões de usuário individuais. Portanto, ao criar uma conexão, a tela de consentimento de permissões exibe todas as permissões que foram concedidas anteriormente à conexão deste usuário, além de todas as novas permissões necessárias para o aplicativo atual.
   >
   >Por exemplo, se um usuário tiver permissões de &quot;Tabela de leitura&quot; concedidas por meio do conector do Excel e criar uma conexão no conector do Outlook para ler emails, a tela de consentimento de permissões mostrará a permissão &quot;Tabela de leitura&quot; já concedida e a permissão &quot;Gravar email&quot; recém-necessária.
