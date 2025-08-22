---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: Gerenciar conexões
description: Para a maioria dos aplicativos, é necessário criar uma conexão, por meio da qual o Adobe Workfront Fusion pode se comunicar com o serviço de terceiros fornecido, de acordo com as configurações do cenário específico.
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 2%

---

# Gerenciar conexões

Uma conexão representa a autorização e as permissões que o Fusion usa para acessar o aplicativo. É possível criar uma ou mais conexões para cada aplicativo e usar a mesma conexão em vários módulos ou cenários.

Você pode gerenciar essas conexões na área Conexões.

Para obter mais informações sobre conexões, consulte [Visão geral da conexão](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

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
   <td> <p>Novo: Padrão</p><p>Ou</p><p>Atual: [!UICONTROL Trabalho] ou superior</p> </td> 
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
   <p>Novo menu:</p> <ul><li>Plano do Workfront para [!UICONTROL Select] ou [!UICONTROL Prime]: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Workfront do [!UICONTROL Ultimate]: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Exibir e gerenciar conexões

Você pode gerenciar todas as conexões na área Conexões.

>[!NOTE]
>
>As conexões são de propriedade de equipes. Se não conseguir encontrar a conexão que você está procurando, verifique se você está vendo o grupo correto.
>
>Para selecionar um novo grupo, clique no nome do grupo no menu de navegação esquerdo e selecione um novo grupo.

1. Para abrir a área Conexões, clique no ícone **Conexões** ![Conexões](assets/connections-icon.png) no painel de navegação esquerdo.
1. Localize a conexão que você deseja gerenciar e execute uma ou mais das etapas a seguir na linha dessa conexão.
1. (Opcional) Atribua um ambiente e um tipo de conexão clicando nos menus suspensos **Ambiente** e **Tipo** e selecionando uma opção.
1. (Opcional) Para exibir quais permissões foram fornecidas ao Workfront Fusion para a conexão, clique no ícone Exibir ![Exibir permissões de conexão](assets/view-connection-permissions.png) para essa conexão.
1. (Opcional) Para renomear uma conexão, realce o nome da conexão e digite o novo nome.
1. (Opcional) Para reautorizar uma conexão, clique em **Reautorizar**.
1. (Opcional) Para excluir uma conexão, clique em **Excluir** e em **Realmente?**.
1. (Opcional) Para verificar se a conexão com o serviço foi estabelecida com êxito, clique em **Verificar**.

## Renovar uma conexão

O Workfront Fusion geralmente obtém direitos de acesso a um determinado serviço por um período ilimitado. Alguns aplicativos exigem que a permissão de acesso seja renovada após um determinado período. Nesses casos, o Workfront Fusion notifica você por email pouco antes da expiração dos direitos de acesso.

Para renovar uma conexão:

1. Para abrir a área Conexões, clique no ícone **Conexões** ![Conexões](assets/connections-icon.png) no painel de navegação esquerdo.
1. Localize a conexão que deseja renovar.
1. Na linha dessa conexão, clique no botão **[!UICONTROL Reautorizar]** na área **[!UICONTROL Conexões]**.

## Recursos

* Para obter mais informações sobre metadados de conexão, como ambiente e tipo, consulte [Metadados de conexão](/help/workfront-fusion/references/connections/connection-metadata.md).
