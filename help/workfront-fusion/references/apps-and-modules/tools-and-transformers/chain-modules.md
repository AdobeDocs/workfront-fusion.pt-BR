---
title: Módulos de Cadeia
description: Com esses módulos, é possível encadear cenários, fazendo com que um chame outro.
author: Becky
feature: Workfront Fusion
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
TQID: https://experienceleague.adobe.com/AlHUrliXikCc3OVHiBTjLNQFndCf5qLzOLuBvnDTUfA
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 81d1dfcdb5c15f6a93e2793f9a0e41821b65c7e3
workflow-type: tm+mt
source-wordcount: 883
ht-degree: 10%

---

# Módulos de cadeia

>[!IMPORTANT]
>
>Esse recurso está no Beta e não é recomendado para fluxos de trabalho de produção de missão crítica. Como um recurso do Beta, o comportamento pode mudar e os casos de borda podem não ser totalmente tratados.
>
>Para integrações estáveis, considere acionar um segundo cenário por meio de um webhook usando um módulo de Solicitação HTTP — esse padrão usa primitivos totalmente compatíveis e fornece a cada cenário um controle de execução independente.
>
>Se você optar por usar cenários encadeados, revise [Vários cenários encadeados](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md) para obter orientação sobre design.

Usando os módulos de Cadeia, você pode conectar um cenário a outro.

<!--This article will be about the specific module configuration-->

Para obter instruções sobre como planejar cenários encadeados, consulte [Cadear vários cenários juntos](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


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

>[!IMPORTANT]
>
> Revise o seguinte antes de configurar esse módulo em um cenário de produção:
>
> * **Não habilitar o CTL (Gatilho de Confirmação Último)** neste cenário quando a opção Acionar e Ignorar estiver desabilitada. A lista de certificados confiáveis repetirá o cenário quando suspender a espera por uma resposta secundária, criando um loop de repetição não vinculado.
> * **Tenha cuidado ao colocar este módulo dentro de um iterador.** O envio de um cenário filho para cada item em um iterador grande cria uma carga de plataforma significativa. Considere embutir a lógica do cenário filho ou realizar pesquisas compartilhadas de pré-computação fora do iterador.
> * **Disparar e Esquecer** significa que o pai não tem visibilidade sobre se o filho foi executado ou bem-sucedido. Use somente quando as falhas secundárias forem monitoradas independentemente.
>
> Para obter orientações completas sobre design, consulte [Cadear vários cenários](https://experienceleague.adobe.com/pt-br/docs/workfront-fusion/using/create-scenarios/plan-a-scenario/chain-scenarios).

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

>[!IMPORTANT]
>
> Se o cenário filho tiver várias rotas, você **deve** garantir que a resposta de Retorno para o módulo pai possa ser acessada de cada caminho de execução. Se o módulo Retornar resposta estiver em uma rota que é ignorada ou não executada, o cenário pai aguardará indefinidamente por uma resposta que nunca chega.
>
> Adicione a resposta Return ao módulo pai depois do roteador, em uma rota que sempre é executada independentemente do resultado do roteador, ou adicione o tratamento de erros para garantir que uma resposta seja sempre retornada mesmo quando ocorrer um erro.

Para configurar o módulo Adicionar respondente:

1. Para usar uma estrutura de dados existente, no campo Estrutura de dados, selecione a estrutura de dados que será usada para os dados que o cenário filho retorna ao cenário pai.

   Ou

   Para criar uma nova estrutura de dados para os dados, clique em **Adicionar** ao lado do campo Estrutura de dados e crie a estrutura de dados.

   Para obter instruções sobre como criar uma estrutura de dados, consulte [Estruturas de dados](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Clique em **OK** para salvar o módulo.
