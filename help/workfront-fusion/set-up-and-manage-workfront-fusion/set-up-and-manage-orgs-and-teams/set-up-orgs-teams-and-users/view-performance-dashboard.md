---
title: Exibir o painel de desempenho de uma organização
description: Os administradores do Fusion podem visualizar um painel que mostra as métricas de execução de uma organização.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
source-git-commit: 1d8504b10d9ca74a5df5532232cda235c67b0185
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 7%

---

# Exibir o painel de desempenho de uma organização

O Painel de Desempenho do Fusion permite que você veja rapidamente quais cenários estão sendo mais executados, onde os atrasos estão ocorrendo e com que eficiência seus pools de trabalhadores estão operando. Isso proporciona visibilidade em tempo real dos volumes de execução, profundidade da fila, utilização do pool e desempenho em nível de cenário.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Adobe Workfront Workflow Ultimate e Adobe Workfront Automation and Integration Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso</td> 
   <td> 
     <p>Você deve ser um administrador do Workfront Fusion para sua organização.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações desta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Componentes do painel de desempenho

>[!NOTE]
>
>As métricas são mostradas pelo pool de trabalhadores. Para exibir um pool de trabalhadores diferente, clique no campo Pool próximo ao canto superior esquerdo do painel e selecione o pool para o qual deseja exibir métricas.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

No painel de desempenho do Fusion, é possível ver as seguintes métricas.

* **Execuções aguardando para serem processadas**
Este gráfico mostra o número de execuções aguardando para serem processadas (também conhecido como backlog de execução) em um determinado momento.

  Um alto número de execuções aguardando para serem processadas pode afetar o desempenho em sua instância do Fusion. Você receberá uma notificação se o backlog de execução atingir 5000 execuções. Recomendamos identificar cenários responsáveis e modificá-los ou desativá-los. Se o backlog de alta execução persistir, a equipe do Fusion protegerá o desempenho da instância do Fusion desativando os cenários responsáveis.
* **Utilização do Pool**
Este gráfico mostra a utilização do pool de trabalhadores ao longo do tempo. Se este gráfico mostrar rotineiramente a utilização do pool de trabalhadores, talvez você queira atribuir alguns cenários a outro pool.

  Se um pool estiver perto de 100% de utilização, outros recursos que usam o mesmo pool poderão ser atrasados ou interrompidos. Se isso ocorrer, é recomendável reatribuir um cenário de alto uso a outro pool de trabalhadores ou modificar cenários existentes para que consumam menos recursos.
* **Execuções por cenário**
Este gráfico exibe execuções por cenário. Cores diferentes representam cenários diferentes. Quando você passa o mouse sobre o gráfico, é exibida uma janela mostrando qual cor é qual cenário.

  Você pode usar este gráfico para identificar quais cenários podem estar causando um backlog de execução ou alta utilização do pool de trabalhadores.
* **Duração das execuções**
Este gráfico exibe execuções por cenário. Cores diferentes representam cenários diferentes. Quando você passa o mouse sobre o gráfico, é exibida uma janela mostrando qual cor é qual cenário.

  Você pode usar este gráfico para identificar cenários que estão demorando mais do que o normal, incluindo aqueles afetados por problemas com um aplicativo ou serviço conectado.

## Exibir o Painel de Desempenho do Fusion

1. No Fusion, clique em Desempenho no painel de navegação esquerdo.

   O Painel é aberto.

1. Para visualizar dados de um momento específico, passe o mouse sobre um painel e ajuste o cursor para estar sobre o momento que deseja visualizar.

   Uma linha aparece sobre esse ponto no tempo em todos os gráficos, e uma janela mostrando dados para esse tempo aparece em cada gráfico.
1. Para exibir dados de um cenário específico no gráfico Execuções por cenário ou no gráfico Duração de execuções, clique em uma barra da cor do cenário para o qual deseja exibir dados. Para retornar à visualização que mostra todos os cenários, clique no gráfico novamente.
1. Para ir para um cenário específico mostrado no gráfico Execuções por cenário ou no gráfico Duração de execuções, clique com o botão direito do mouse em uma barra da cor do cenário e selecione **Abrir cenário em nova guia**.
1. Para expandir um gráfico, clique no ícone **Expandir** ![Ícone Expandir](assets/expand-icon.png) no canto superior direito desse gráfico.
1. Para alterar o intervalo de tempo do painel, abra o campo Intervalo de tempo no canto superior direito do painel e selecione um novo intervalo de tempo. O período mais longo disponível é de 24 horas e o mais curto é de 15 minutos.
1. Para atualizar os gráficos, clique no ícone Atualizar próximo ao canto superior direito do painel.
1. Para exibir um pool de trabalhadores diferente, clique no campo Pool próximo ao canto superior esquerdo do painel e selecione o pool que deseja exibir.
