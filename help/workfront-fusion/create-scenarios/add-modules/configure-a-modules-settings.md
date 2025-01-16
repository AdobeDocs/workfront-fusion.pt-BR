---
title: Configurar um módulo
description: Você deve definir as configurações para cada módulo criado.
author: Becky
feature: Workfront Fusion
exl-id: ae82d1fe-31e1-424a-9c1a-42dc1a20b749
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 2%

---

# Configurar um módulo

Você deve definir as configurações para cada módulo criado.

Por exemplo, o módulo Workfront > Carregar documento exige que você especifique o registro no qual deseja carregar um documento.

>[!NOTE]
>
>Além das configurações do módulo, você também pode ajustar as configurações de um cenário. É possível renomear o cenário, alterar seu agendamento e especificar configurações adicionais, entre outras ações.

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
   <td> <p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p> </td> 
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
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou plano do [!UICONTROL Prime] [!DNL Workfront]: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plano: [!DNL Workfront Fusion] está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Definir as configurações de um módulo

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário ao qual deseja adicionar um filtro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Adicione um novo módulo a um cenário.

   Ou

   Clique no módulo que deseja configurar.

1. Se necessário para o módulo, crie um **[!UICONTROL Connection]** para sua conta de usuário registrada para esse serviço específico, conforme descrito na [Visão geral das conexões](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).
1. Em cada campo, digite o texto apropriado.

   Ou

   Mapeie a saída de um módulo anterior para o campo.

   Para obter informações sobre mapeamento, consulte [Visão geral do mapeamento](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

   Para obter informações sobre os diferentes tipos de dados de item que [!DNL Workfront Fusion] pode reconhecer (como data, número e texto), consulte [Tipos de dados de item](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

   >[!NOTE]
   >
   >Parâmetros em negrito são necessários.

1. (Condicional) Se o módulo tiver opções avançadas que você deseja exibir e usar, selecione **[!UICONTROL Show advanced settings]**.
