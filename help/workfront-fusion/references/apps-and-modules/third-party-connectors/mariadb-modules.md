---
title: Módulos do MariaDB
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o  [!DNL MariaDB], bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL MariaDB] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL MariaDB], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote de Automação e Integração do Adobe Workfront</p><p>Workfront Ultimate</p><p>Workfront Prime e pacotes Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Standard</p><p>Trabalhar ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (herdado): automação e integração do Workfront Fusion for Work </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos [!DNL MariaDB], você deve ter uma conta [!DNL MariaDB].

## Conectar o [!DNL MariaDB] ao Workfront Fusion

Você pode criar uma conexão com sua conta do [!DNL MariaDB] diretamente de dentro de um módulo do [!DNL MariaDB].

1. Em qualquer módulo [!DNL MariaDB], clique em **[!UICONTROL Adicionar]** ao lado do campo [!UICONTROL Conexão].
1. Configure os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Nome da Conexão]</p> </td> 
      <td> <p>Insira um nome para a nova conexão.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Selecione se essa conexão é para um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Host]</td> 
      <td> <p>Informe o endereço IP ou o nome do host da instância do banco de dados. Esse host deve ser acessível de fora da rede.</p> <p>Exemplo: <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Porta]</td> 
      <td>A porta padrão é 3306. Se você estiver usando uma porta não padrão, defina esse número para sua porta. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Banco de Dados ]</td> 
      <td>Insira o nome do banco de dados com o qual você deseja interagir.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Usuário]</td> 
      <td>Insira seu nome de usuário.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Senha]</td> 
      <td>Digite sua senha.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

## [!DNL MariaDB] Módulos e seus campos

Ao configurar módulos do [!DNL MariaDB], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL MariaDB] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Executar uma consulta (avançado)

Este módulo de ação recupera informações do banco de dados, com base em uma consulta fornecida por você.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL MariaDB] ao Workfront Fusion, consulte <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Conectar [!DNL MariaDB] ao Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Consulta]</td> 
   <td> <p>Insira a consulta SQL que você deseja que o módulo use para recuperar dados.</p> <p>Importante: as variáveis usadas na consulta não são limpas. Certifique-se de limpar as variáveis corretamente para impedir a injeção de SQL.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Selecionar linhas de uma tabela (avançado)]

Esse módulo lê registros do banco de dados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL MariaDB] ao Workfront Fusion, consulte <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Conectar [!DNL MariaDB] ao Workfront Fusion</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tabela]</td> 
   <td> <p>Selecione a tabela que contém os registros que você deseja ler.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Configure o filtro pelo qual deseja selecionar linhas</p> 
    <ul> 
     <li> <p>Selecione o campo pelo qual deseja pesquisar</p> </li> 
     <li> <p>Selecione o operador que deseja usar na pesquisa</p> </li> 
     <li> <p>Insira ou mapeie o valor que você deseja pesquisar.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classificar] </td> 
   <td> <p>Para cada nível pelo qual você deseja classificar os resultados, clique em <strong>[!UICONTROL Adicionar item]</strong> e selecione o campo pelo qual deseja classificar os resultados e se deseja classificar em ordem crescente ou decrescente</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>
