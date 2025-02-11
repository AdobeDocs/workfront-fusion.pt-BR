---
title: Módulos de armazenamento de dados
description: Um armazenamento de dados  [!DNL Adobe Workfront Fusion] , semelhante a um banco de dados ou uma tabela simples, pode armazenar dados de cenários, possibilitando a transferência de dados entre cenários individuais ou execuções de cenário. Você pode usar um armazenamento de dados para armazenar novos dados de vários sistemas durante a sincronização.
author: Becky
feature: Workfront Fusion
exl-id: 0338b822-b345-429e-850d-3978b692231d
source-git-commit: 7404dafc0b368a8f1785be7b6a65fe45c0f12172
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# [!UICONTROL Data store] módulos

Um armazenamento de dados [!DNL Adobe Workfront Fusion], semelhante a um banco de dados ou uma tabela simples, pode armazenar dados de cenários, possibilitando a transferência de dados entre cenários individuais ou execuções de cenário. Você pode usar um armazenamento de dados para armazenar novos dados de vários sistemas durante a sincronização.

Os módulos de armazenamento de dados permitem que você adicione, substitua, atualize, recupere, exclua, pesquise ou conte registros em seu armazenamento de dados do [!DNL Adobe Workfront Fusion].

<!--For information on creating, editing, and troubleshooting data stores, see [Data Stores in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/mapping-panel/data-types/)-->

Para obter uma introdução em vídeo aos armazenamentos de dados no Workfront Fusion, consulte:

* [Repositórios de Dados](https://video.tv.adobe.com/v/3427029/){target=_blank}

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
   <p>Nenhum requisito de licença do Workfront Fusion.</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Para usar módulos do [!UICONTROL Data Store], primeiro você deve criar um armazenamento de dados.

Para obter informações sobre como criar armazenamentos de dados, consulte [Criar e gerenciar armazenamentos de dados](/help/workfront-fusion/create-scenarios/map-data/data-stores.md).

## [!UICONTROL Data store] módulos e seus campos

Ao configurar módulos de Armazenamento de Dados, o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos adicionais do Data Store podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Não é necessário criar uma conexão para usar armazenamentos de dados.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Adicionar/Substituir um Registro](#addreplace-a-record)
* [Verificar a existência de um registro](#check-the-existence-of-a-record)
* [Contar Registros](#count-records)
* [Excluir um Registro](#delete-a-record)
* [Excluir todos os registros](#delete-all-records)
* [Obter um Registro](#get-a-record)
* [Pesquisar Registros](#search-records)
* [Atualizar um Registro](#update-a-record)

### [!UICONTROL Add/Replace a Record]

Este módulo de ação adiciona ou substitui um registro.

Especifique o armazenamento de dados e a chave do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

>[!NOTE]
>
>O módulo emite um erro quando você tenta adicionar um registro que já está no armazenamento de dados com o mesmo nome e a opção [!UICONTROL Overwrite an existing record] está desabilitada.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store]</td> 
   <td> <p> Selecione ou adicione o armazenamento de dados em que deseja criar um registro. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Insira a chave exclusiva do registro que você deseja que o módulo adicione ou substitua. A chave pode ser usada posteriormente para recuperar o registro. Se você deixar esse campo em branco, uma chave será gerada automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Overwrite an existing record] </td> 
   <td> <p>Habilite esta opção para substituir o registro. O registro que você deseja substituir deve ser especificado no campo Chave acima.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record] </td> 
   <td> <p>Insira os valores desejados nos campos do registro.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Check the Existence of a Record]

Este módulo de ação especifica se um determinado registro existe.

Especifique o armazenamento de dados e a chave do registro.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store] </td> 
   <td> <p>Selecione o armazenamento de dados que deseja verificar a existência do registro.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Insira a chave exclusiva do registro que você deseja que o módulo verifique quanto à existência.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Count Records]

Esse módulo de ação numera os registros em um armazenamento de dados.

Você especifica o armazenamento de dados.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store] </td> 
   <td> <p>Selecione o armazenamento de dados que contém os registros que você deseja contar.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a Record]

Este módulo de ação exclui um registro.

Especifique o armazenamento de dados e a chave do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store] </td> 
   <td> <p>Selecione o armazenamento de dados que deseja verificar a existência do registro.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Insira a chave exclusiva do registro que você deseja que o módulo exclua.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete All Records]

Esse módulo de ação exclui todos os registros de um determinado armazenamento de dados.

Você especifica o armazenamento de dados.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store] </td> 
   <td> <p>Selecione o armazenamento de dados do qual deseja excluir todos os registros.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a Record]

Este módulo de ação recupera um registro.

Especifique o armazenamento de dados e a chave do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store]</td> 
   <td> <p> Selecione o armazenamento de dados do qual deseja recuperar um registro</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Insira a chave exclusiva do registro que você deseja que o módulo recupere.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search Records]

Esse módulo de pesquisa procura registros em um objeto no Armazenamento de dados que correspondam à consulta de pesquisa especificada.

Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store]</td> 
   <td> <p> Selecione o armazenamento de dados que deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>Defina o filtro da pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Sort]</p> </td> 
   <td> <p style="font-weight: normal;">Para cada campo pelo qual você deseja classificar, preencha os seguintes campos:</p> <p style="font-weight: bold;">[!UICONTROL Key]</p> <p>Selecione o nome da coluna pela qual deseja classificar os resultados.</p> <p style="font-weight: bold;">[!UICONTROL Order]</p> <p>Selecione se deseja classificar os resultados na ordem crescente ou decrescente.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p> Defina o número máximo de resultados de pesquisa [!DNL Workfront Fusion] retornos durante um ciclo de execução.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> Se ativado, a rota da qual este módulo faz parte continua sendo processada mesmo que este módulo não retorne resultados.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a Record]

Este módulo de ação atualiza um registro.

Especifique o armazenamento de dados e a chave do registro.

O módulo retorna a ID do registro e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store]</td> 
   <td> <p> Selecione ou adicione o armazenamento de dados em que deseja criar um registro. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Insira a chave exclusiva do registro que você deseja que o módulo atualize.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Insert missing record] </td> 
   <td> <p>Ative esta opção para criar um novo registro se o registro com a chave especificada ainda não existir.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record]</td> 
   <td> <p> Informe os valores desejados nos campos do registro que deseja atualizar.</p> </td> 
  </tr> 
 </tbody> 
</table>
