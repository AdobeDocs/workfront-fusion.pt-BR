---
title: Criar uma conexão - Instruções básicas
description: Muitos conectores do Adobe Workfront Fusion não exigem configuração personalizada ao criar uma conexão. Este artigo descreve o processo de criação de conexão padrão.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Criar uma conexão - Instruções básicas

Muitos conectores do Adobe Workfront Fusion não exigem configuração personalizada ao criar uma conexão. Este artigo descreve o processo de criação de conexão padrão.

>[!NOTE]
>
>
>Se o Adobe Workfront Fusion não oferecer um aplicativo para o serviço Web que você deseja usar em seu cenário, é possível se conectar ao serviço Web usando os módulos HTTP e Webhooks do Workfront Fusion, conforme explicado nos seguintes artigos:
>
>* [Conecte o Adobe Workfront Fusion a um serviço Web que usa a autorização do token de API](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [Configurar um webhook para um serviço Web sem um conector](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

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
   <p>Baseado em conector (herdado): para se conectar a aplicativos fora da família de produtos Workfront, é necessário ter a Automação e Integração do Workfront Fusion for Work </p>
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

## Criar uma conexão

Para criar uma conexão com um determinado aplicativo, você deve estar em um módulo desse aplicativo. Por exemplo, para criar uma conexão com o Workfront, você deve estar em um módulo do Workfront.

Para criar uma conexão dentro de um módulo do Workfront Fusion:

1. Em qualquer módulo do aplicativo fornecido, clique em **[!UICONTROL Adicionar]** ao lado da caixa [!UICONTROL Conexão] para abrir o painel **[!UICONTROL Criar uma conexão]**.
1. (Opcional) Altere o **[!UICONTROL Nome da conexão]** padrão.
1. No campo Ambiente, selecione se é um ambiente de produção ou não produção.
1. No campo Tipo, selecione se é uma conta de serviço ou pessoal.
1. (Condicional) Se o aplicativo exigir configurações de conexão avançadas, como ID, chave ou [!UICONTROL segredo], insira essas informações.

   Talvez seja necessário clicar em **[!UICONTROL Mostrar configurações avançadas]** para exibir os campos nos quais você pode inserir esse tipo de informação.

1. Clique em **[!UICONTROL Continuar]**.
1. Na janela de logon que é exibida, digite suas credenciais para fazer logon no aplicativo, se ainda não tiver feito.
1. (Condicional) Se um botão **[!UICONTROL Permitir]** for exibido, examine as ações que o conector poderá realizar e clique no botão para conectar o aplicativo ao Workfront Fusion.

   >[!NOTE]
   >
   >* Os campos Ambiente e Tipo são somente para fins informativos e não alteram a funcionalidade da conexão. Essas informações são exibidas na área Conexões do Fusion, permitindo determinar qual conexão usar para um determinado caso de uso na organização.
   >* Alguns aplicativos do Microsoft usam a mesma conexão, que está vinculada a permissões de usuário individuais. Portanto, ao criar uma conexão, a tela de consentimento de permissões exibe todas as permissões que foram concedidas anteriormente à conexão deste usuário, além de todas as novas permissões necessárias para o aplicativo atual.
   >
   >   Por exemplo, se um usuário tiver permissões de &quot;Tabela de leitura&quot; concedidas por meio do conector do Excel e criar uma conexão no conector do Outlook para ler emails, a tela de consentimento de permissões mostrará a permissão &quot;Tabela de leitura&quot; já concedida e a permissão &quot;Gravar email&quot; recém-necessária.
