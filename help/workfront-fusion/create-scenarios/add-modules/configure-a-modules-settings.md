---
title: Configurar um módulo
description: Você deve definir as configurações para cada módulo criado.
author: Becky
feature: Workfront Fusion
exl-id: ae82d1fe-31e1-424a-9c1a-42dc1a20b749
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 32%

---

# Configurar um módulo

Você deve definir as configurações para cada módulo criado.

Por exemplo, o módulo Workfront > Carregar documento exige que você especifique o registro no qual deseja carregar um documento.

>[!NOTE]
>
>Além das configurações do módulo, você também pode ajustar as configurações de um cenário. É possível renomear o cenário, alterar seu agendamento e especificar configurações adicionais, entre outras ações.

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
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Definir as configurações de um módulo

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário ao qual deseja adicionar um filtro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Adicione um novo módulo a um cenário.

   Ou

   Clique no módulo que deseja configurar.

1. Se necessário para o módulo, crie uma **[!UICONTROL Conexão]** para sua conta de usuário registrada para esse serviço específico, conforme descrito na [Visão geral das conexões](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).
1. Em cada campo, digite o texto apropriado.

   Ou

   Mapeie a saída de um módulo anterior para o campo.

   Para obter informações sobre mapeamento, consulte [Visão geral do mapeamento](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

   Para obter informações sobre os diferentes tipos de dados de item que o Workfront Fusion pode reconhecer (como data, número e texto), consulte [Tipos de dados de item](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

   >[!NOTE]
   >
   >Parâmetros em negrito são necessários.

1. (Condicional) Se o módulo tiver opções avançadas que você deseja exibir e usar, selecione **[!UICONTROL Mostrar configurações avançadas]**.
