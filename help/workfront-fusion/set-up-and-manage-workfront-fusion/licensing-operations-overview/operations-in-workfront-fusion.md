---
title: Operações
description: Uma operação no Adobe Workfront Fusion é uma tarefa executada por um módulo. Para fins de rastreamento, qualquer ação bem-sucedida executada por um módulo é uma operação.
author: Becky
feature: Workfront Fusion
exl-id: c14e2bb2-1cce-48ff-8bea-acc9829d3cf2
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---

# Operações

Uma operação no Adobe Workfront Fusion é uma tarefa executada por um módulo. Para fins de rastreamento, qualquer ação bem-sucedida executada por um módulo é uma operação.

## Considerações ao contar o número de operações

* Em geral, qualquer execução bem-sucedida da etapa de ação é considerada uma operação.
* O primeiro módulo em um cenário é executado apenas uma vez e é sempre contado como uma operação, mesmo que não retorne um pacote.
* O número de vezes que o restante dos módulos é executado depende do número de pacotes que eles devem processar.  Uma execução de um módulo para um pacote é uma operação. Uma exceção é o módulo agregador, que é contado como uma operação por conjunto de pacotes sendo processados.
* As operações são contadas no estágio [!UICONTROL Finalization] de execução de um cenário.
* Os itens a seguir são **não** contados como operações:
   * Quaisquer etapas de filtro.
   * Qualquer ação que cause erros ou seja interrompida.
   * Qualquer rota que não seja executada porque as regras da rota não foram atendidas, como rotas de fallback ou desabilitadas.
   * Qualquer ação que não seja executada porque um filtro não permitiu a passagem de dados ou porque o cenário foi interrompido devido a um erro.

## Limites de operação

Sua organização pode ter um limite mensal de operações. Isso se baseia no plano Workfront adquirido pela sua organização. O plano do Workfront [!UICONTROL Ultimate] oferece operações ilimitadas.

Se sua organização tiver um limite mensal, você será notificado quando ela estiver perto do limite. Se sua organização ultrapassar o limite, a Workfront entrará em contato com sua organização para garantir que seu plano atenda às suas necessidades.

O Workfront Fusion envia uma notificação quando sua organização atinge as seguintes porcentagens do limite mensal da organização:

* 50%
* 75%
* 90%
* 100%

## Exibir o número de operações executadas nos últimos 30 dias

Você pode ver um gráfico que mostra o número de operações realizadas. Esses gráficos estão disponíveis nos seguintes locais:

* **Painel da organização**: operações usadas por toda a organização
* **Painel da equipe**: operações usadas pelos cenários pertencentes a esta equipe
* **Página de detalhes do cenário**: Operações usadas por este cenário
