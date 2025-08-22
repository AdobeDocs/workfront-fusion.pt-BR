---
title: Exibir a execução de um cenário específico
description: Você pode exibir detalhes da execução de um cenário específico, incluindo filtragem e pesquisa de eventos de cenário.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 1%

---

# Exibir a execução de um cenário específico

Você pode exibir detalhes da execução de um cenário específico, incluindo filtragem e pesquisa de eventos de cenário.

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
   <p>Nenhum requisito de licença do Workfront Fusion</p>
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

## Exibir uma execução específica

Você pode exibir uma execução no histórico de cenários do cenário.


1. Clique na guia **[!UICONTROL Cenário]** no painel esquerdo e clique no cenário.

   Ou

   Se você estiver trabalhando no cenário no Editor de cenários, clique na seta para a esquerda ![Sair da seta de edição](assets/exit-editing-arrow.png) próximo ao canto superior esquerdo da janela.

1. Clique em **Histórico** próximo ao nome do cenário.
   ![guia Histórico](assets/history-tab.png)


1. Localize a execução que deseja exibir e clique em **Detalhes** na extremidade direita da linha dessa execução. O link [!UICONTROL details] estará visível somente se a execução tiver detalhes disponíveis.

   O diagrama de cenário é aberto, com o painel de detalhes de execução aberto à direita.

   Os módulos que produziram saída para essa execução são marcados com títulos verdes.

   Os módulos que não foram executados estão esmaecidos.

1. Para visualizar a saída de um módulo, clique na bolha de detalhes da saída próximo ao módulo. O número na bolha representa o número de pacotes gerados pelo módulo.

   ![Bolha de saída próxima a um módulo](assets/output-bubble.png)

1. Para exibir os pacotes que passaram por um filtro, clique no filtro. O número próximo ao filtro representa o número de pacotes que passaram pelo filtro.
1. Para procurar um módulo ou evento específico no painel de execução, insira o termo de pesquisa na caixa **Pesquisar eventos de execução**. Os resultados são exibidos conforme você digita.
1. Para limitar os resultados da pesquisa do painel de execução por status, como Sucesso ou Aviso, clique na lista suspensa **Filtro de Status** e selecione o status.




>[!NOTE]
>
>Para criar um link para um módulo específico, adicione `?moduleId=<module-id>` à URL ao visualizar as seguintes páginas:
>
>* Página de edição do cenário (URL termina em `/edit`)
>* Uma execução de cenário específica (a URL termina em `/logs/<log-id>`)
>
>`<module-id>` refere-se ao número ao lado do rótulo do módulo ao visualizar o cenário.
>
>Isso pode ser útil ao depurar cenários ou copiar a configuração do módulo.
