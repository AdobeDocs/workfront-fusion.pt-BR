---
title: Módulos de Cadeia
description: Com esses módulos, é possível encadear cenários, fazendo com que um chame outro.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---

# Módulos de corrente

Usando os módulos de Cadeia, você pode conectar um cenário a outro.

<!--This article will be about the specific module configuration-->

Para obter instruções sobre como planejar cenários encadeados, consulte [Cadear vários cenários juntos](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


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

## Módulos de cadeia e seus campos

### Acionadores

#### Receber dados do responsável

Esse módulo é o módulo de acionamento no cenário filho e é acionado pelo módulo Chamar um cenário filho no cenário pai. Ele recebe dados do cenário pai, que podem ser processados no cenário filho.

Para configurar os dados de Recebimento do módulo pai:

1. Para usar uma estrutura de dados existente, no campo Estrutura de dados, selecione a estrutura de dados que será usada para os dados de entrada do cenário.

   Ou

   Para criar uma nova estrutura de dados para usar como os dados de entrada do cenário, clique em **Adicionar** ao lado do campo Estrutura de dados e crie a estrutura de dados.

   Para obter instruções sobre como criar uma estrutura de dados, consulte [Estruturas de dados](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Clique em **OK** para salvar o módulo.

### Ações

#### Chamar um cenário filho

Esse módulo está localizado no cenário principal. Os campos refletem a estrutura de dados definida em Receber dados do módulo pai no cenário filho.

>[!NOTE]
>
>* Você pode selecionar um cenário filho existente ou criar um novo por meio desse módulo.
>* Você pode criar a estrutura de dados ao criar um cenário filho.

Para configurar o módulo Chamar um cenário filho

1. Adicione o módulo Call a child scenario ao seu cenário.
1. Para usar um cenário filho existente, no campo Cadeia, selecione o cenário filho que deseja chamar.

   Ou

   Para criar um novo cenário filho, clique em Adicionar ao lado do campo Cadeia. O cenário filho aparece em uma janela separada, com a resposta Receber dados do pai e Retornar dos módulos pai no lugar.

   Os campos configurados no módulo de acionador do cenário filho aparecem no módulo Chamar um cenário filho.

1. Insira ou mapeie as informações a serem passadas para o cenário filho no módulo Chamar um cenário filho.
1. (Condicional) Se desejar que o cenário pai continue sua execução sem esperar uma resposta do cenário filho, habilite a opção **Acionar e Ignorar**.
1. Clique em **OK** para salvar o módulo.

>[!NOTE]
>
>Se você criar um novo cenário filho para esse módulo, o cenário filho será aberto em uma janela do navegador separada, permitindo que você veja e configure os cenários pai e filho ao mesmo tempo.

#### Retornar resposta ao pai

Isso está no cenário filho e envia dados na estrutura selecionada para o cenário pai. Você pode mapear esses dados em módulos posteriores no cenário principal.

Se o cenário filho tiver várias rotas, recomendamos adicionar esse módulo a uma rota que sempre é executada e executada após qualquer outra rota.

Para configurar o módulo Adicionar respondente:

1. Para usar uma estrutura de dados existente, no campo Estrutura de dados, selecione a estrutura de dados que será usada para os dados que o cenário filho retorna ao cenário pai.

   Ou

   Para criar uma nova estrutura de dados para os dados, clique em **Adicionar** ao lado do campo Estrutura de dados e crie a estrutura de dados.

   Para obter instruções sobre como criar uma estrutura de dados, consulte [Estruturas de dados](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Clique em **OK** para salvar o módulo.
