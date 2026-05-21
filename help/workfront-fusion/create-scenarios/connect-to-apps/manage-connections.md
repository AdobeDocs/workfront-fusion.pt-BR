---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: Gerenciar conexões
description: Para a maioria dos aplicativos, é necessário criar uma conexão, por meio da qual o Adobe Workfront Fusion possa se comunicar com o serviço de terceiros fornecido, de acordo com as configurações do cenário específico.
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
TQID: https://experienceleague.adobe.com/P-zEd2tJCk9-uzE1xW6COpTCdFJiIq4NwGRLDdpCSVU
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 586
ht-degree: 28%

---

# Gerenciar conexões

Uma conexão representa a autorização e as permissões que o Fusion usa para acessar o aplicativo. É possível criar uma ou mais conexões para cada aplicativo e usar a mesma conexão em vários módulos ou cenários.

Você pode gerenciar essas conexões na área Conexões.

Para obter mais informações sobre conexões, consulte [Visão geral da conexão](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

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
   <p>Baseado em conector (herdado): para se conectar a aplicativos fora da família de produtos Workfront, é necessário ter a Automação e Integração do Workfront Fusion for Work </p>
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

## Exibir e gerenciar conexões

Você pode gerenciar todas as conexões na área Conexões.

>[!NOTE]
>
>As conexões pertencem às equipes. Se não conseguir encontrar a conexão que você está procurando, verifique se você está vendo o grupo correto.
>
>Para selecionar um novo grupo, clique no nome do grupo no menu de navegação esquerdo e selecione um novo grupo.

1. Para abrir a área Conexões, clique no ícone **Conexões** ![Conexões](assets/connections-icon.png) no painel de navegação esquerdo.
1. Localize a conexão que você deseja gerenciar e execute uma ou mais das etapas a seguir na linha dessa conexão.
1. (Opcional) Atribua um ambiente e um tipo de conexão clicando nos menus suspensos **Ambiente** e **Tipo** e selecionando uma opção.
1. (Opcional) Para exibir quais permissões foram fornecidas ao Workfront Fusion para a conexão, clique no ícone Exibir ![Exibir permissões de conexão](assets/view-connection-permissions.png) para essa conexão.
1. (Opcional) Para renomear uma conexão, realce o nome da conexão e digite o novo nome.
1. (Opcional) Para reautorizar uma conexão, marque a caixa de seleção ao lado da conexão e clique em **Reautorizar** próximo à parte inferior da tela.
1. (Opcional) Para excluir uma conexão, marque a caixa de seleção ao lado da conexão, clique em **Excluir** próximo à parte inferior da tela e clique em **Deseja realmente?**.
1. (Opcional) Para verificar se a conexão com o serviço foi estabelecida com êxito, marque a caixa de seleção ao lado da conexão e clique em **Verificar** próximo à parte inferior da tela.
1. (Opcional) Para exibir cenários ativos que usam essa conexão, marque a caixa de seleção ao lado da conexão e clique em **Buscar cenários ativos**. Você pode clicar em um cenário na lista Cenários ativos para ir para esse cenário.

## Renovar uma conexão

O Workfront Fusion geralmente obtém direitos de acesso a um determinado serviço por um período ilimitado. Alguns aplicativos exigem que a permissão de acesso seja renovada após um determinado período. Nesses casos, o Workfront Fusion notifica você por email pouco antes da expiração dos direitos de acesso.

Para renovar uma conexão:

1. Para abrir a área Conexões, clique no ícone **Conexões** ![Conexões](assets/connections-icon.png) no painel de navegação esquerdo.
1. Localize a conexão que deseja renovar.
1. Na linha dessa conexão, marque a caixa de seleção ao lado da conexão e clique em **Reautorizar** próximo à parte inferior da tela.

## Recursos

* Para obter mais informações sobre metadados de conexão, como ambiente e tipo, consulte [Metadados de conexão](/help/workfront-fusion/references/connections/connection-metadata.md).
