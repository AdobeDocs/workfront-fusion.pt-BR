---
title: Atualizar um módulo para uma nova versão
description: Como os aplicativos aos quais o Workfront Fusion se conecta podem atualizar ou lançar uma nova versão, às vezes é necessário que o Fusion libere módulos atualizados para esses aplicativos.
author: Becky
feature: Workfront Fusion
exl-id: b7f07fa5-9d81-48b3-b0ce-7a18b3b44508
source-git-commit: b30aac8040cc0b6bcad92914b1c0997a8ddebdd5
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 2%

---

# Atualizar um módulo para uma nova versão

Como os aplicativos aos quais o Workfront Fusion se conecta podem atualizar ou lançar novas versões, às vezes é necessário que o Fusion libere módulos atualizados para esses aplicativos.

Se você vir um ícone verde do módulo de Atualização em um módulo em um cenário, o Workfront Fusion lançou uma nova versão desse módulo.

![Ícone Atualizar](assets/update-indicator-workfront.png)

Você pode atualizar o módulo sem criar um novo cenário.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso*</td> 
   <td> 
     <p>Você deve ser um administrador do Workfront Fusion para sua organização.</p>
     <p>Você deve ser um administrador do Workfront Fusion para sua equipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Atualizar um módulo do Workfront para uma nova versão

1. Clique no ícone **Atualizar módulo** ![Atualizar ícone](assets/upgrade-icon.png) no módulo que você deseja atualizar para uma nova versão.
   ![Ícone Atualizar](assets/update-indicator-workfront.png)
1. Escolha uma das seguintes opções:

   * Para selecionar um novo módulo para substituir este módulo (em vez de atualizar o módulo), clique em **Escolher novo** e prossiga conforme descrito em [Atualizar um módulo que não seja da Workfront para uma nova versão](#upgrade-a-non-workfront-module-to-a-new-version).
   * Para atualizar apenas este módulo, preservando a configuração do módulo, clique em **Atualizar**.
   * Para atualizar todos os módulos do Workfront no cenário, clique em **Atualizar tudo**.

1. Salve o cenário.

>[!NOTE]
>
>Se você atualizou módulos do Workfront, recomendamos abri-los e verificar a configuração do módulo.

## Atualizar um módulo que não seja do Workfront para uma nova versão

1. Clique no ícone **Atualizar módulo** ![Atualizar ícone](assets/upgrade-icon.png) no módulo que você deseja atualizar para uma nova versão.
   ![Ícone Atualizar](assets/update-indicator.png)
1. Clique em **Escolher novo**.
1. Selecione o módulo que você deseja substituir o módulo anterior.
1. Configure o módulo com as mesmas configurações do módulo existente.
1. Conecte o novo módulo ao cenário no mesmo lugar que o módulo existente.
1. Exclua o módulo antigo.
1. Salve o cenário.
