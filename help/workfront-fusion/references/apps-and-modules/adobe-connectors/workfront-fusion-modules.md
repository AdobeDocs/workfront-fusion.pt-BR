---
title: Módulos do Workfront Fusion
description: Com o conector do Workfront Fusion, é possível gerenciar sua própria organização do Fusion em um cenário, incluindo registros, ganchos, cenários e conexões.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 557ec6de4ccf0753005fed3e4772d2eb9317537d
workflow-type: tm+mt
source-wordcount: 1374
ht-degree: 21%

---

# Módulos do Workfront Fusion

Com o conector do Workfront Fusion, é possível gerenciar sua própria organização do Fusion em um cenário. Ao contrário de outros conectores, que conectam o Fusion a um aplicativo ou serviço de terceiros, esse conector permite que um cenário chame a própria API do Fusion, de modo semelhante ao de como o conector do Adobe Workfront permite que um cenário gerencie o Workfront.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Conectar o Workfront Fusion ao Workfront Fusion

1. Em qualquer módulo do Workfront Fusion, clique em **[!UICONTROL Adicionar]** ao lado do campo Conexão.
1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection type]</td> 
      <td>Selecione o tipo de conexão que deseja criar.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td>Insira um nome para a conexão.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID]</td> 
      <td>Insira sua [!UICONTROL Client ID] do [!DNL Adobe]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td>Insira o [!UICONTROL Client Secret] do [!DNL Adobe]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL ID da Organização]</td> 
      <td>Insira sua [!DNL Adobe] IMS Organization ID.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Região]</td> 
      <td>Selecione a região do Fusion para essa conexão.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## Módulos do Workfront Fusion e seus campos

Ao configurar módulos do Workfront Fusion, o Workfront Fusion exibe os campos listados abaixo. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ações](#actions)
* [Exportar](#export)
* [Diversos](#misc)

### Ações

* [Clonar um registro](#clone-a-record)
* [Criar um registro](#create-a-record)
* [Excluir um registro](#delete-a-record)
* [Listar registros](#list-records)
* [Ler um registro](#read-a-record)
* [Atualizar um registro](#update-a-record)

#### Clonar um registro

Esse módulo faz uma cópia do registro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> Selecione o tipo de registro que deseja clonar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do cenário</td> 
   <td> Insira ou mapeie a ID do cenário que deseja clonar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td> Insira ou mapeie um nome para o novo cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar um registro

Este módulo cria um registro com os dados especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> Selecione o tipo de registro que deseja criar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da equipe</td> 
   <td> Insira ou mapeie a ID da equipe que será proprietária deste registro. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td> Insira ou mapeie um nome para o novo registro.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um registro

Este módulo exclui um registro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> Selecione o tipo de registro que deseja excluir. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Outros campos</td> 
   <td>Insira valores para quaisquer outros campos. Os campos disponíveis dependem do tipo de registro selecionado. </td> 
  </tr> 
 </tbody> 
</table>

#### Listar registros

Este módulo retorna uma lista paginada de registros usando paginação baseada em cursor e filtros de propriedade.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td>Selecione o tipo de registro do qual você deseja retornar uma lista.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Propriedade</td> 
   <td>Para cada filtro de propriedade para o qual deseja retornar resultados, clique em <b>Adicionar item</b> e insira o campo, o operador e o valor que deseja filtrar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Start</td> 
   <td>Insira o local onde deseja iniciar os resultados retornados. Isso é usado para paginação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que você deseja que o módulo retorne para cada ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordenar por</td> 
   <td>Selecione o campo pelo qual deseja ordenar os resultados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direção</td> 
   <td>Selecione se deseja ordenar os resultados em ordem crescente ou decrescente.</td> 
  </tr> 
 </tbody> 
</table>

#### Ler um registro

Este módulo recupera o registro especificado

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> Selecione o tipo de registro que deseja excluir. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Outros campos</td> 
   <td>Insira valores para quaisquer outros campos. Os campos disponíveis dependem do tipo de registro selecionado. </td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um registro

Atualiza um registro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> Selecione o tipo de registro que deseja atualizar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td> Insira ou mapeie um novo nome para o registro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td> Insira ou mapeie a ID do registro que você deseja atualizar. </td> 
  </tr> 
 </tbody> 
</table>

### Exportar

#### Exportar logs de atividades

Esse módulo exporta logs de atividades.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo do arquivo</td> 
   <td>Selecione o formato de arquivo para o qual deseja exportar logs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Propriedade</td> 
   <td>Para cada filtro de propriedade para o qual deseja retornar resultados, clique em <b>Adicionar item</b> e insira o campo, o operador e o valor que deseja filtrar. Também é possível filtrar se o campo existe ou não.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Start</td> 
   <td>Insira o local onde deseja iniciar os resultados retornados. Isso é usado para paginação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que você deseja que o módulo retorne para cada ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordenar por</td> 
   <td>Selecione o campo pelo qual deseja ordenar os resultados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direção</td> 
   <td>Selecione se deseja ordenar os resultados em ordem crescente ou decrescente.</td> 
  </tr> 
 </tbody> 
</table>

### Diversos

* [Obter estatísticas de fila para um gancho](#get-queue-statistics-for-a-hook)
* [Obter dependências de registro](#get-record-dependencies)
* [Listar cenários para uma conexão](#list-scenarios-for-a-connection)
* [Listar as regiões e organizações de Fusão](#list-the-fusion-regions-and-organizations)

#### Obter estatísticas de fila para um gancho

Este módulo retorna as estatísticas de fila para o gancho especificado: o número de eventos atualmente na fila, o limite de fila e se o gancho está ativado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  <tr> 
   <td role="rowheader">ID do gancho</td> 
   <td> Insira ou mapeie a ID do gancho para o qual você deseja retornar detalhes.</td> 
  </tr> 
 </tbody> 
</table>

#### Obter dependências de registro

Esse módulo obtém as dependências do registro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> Selecione o tipo de registro para o qual deseja recuperar dependências. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do cenário</td> 
   <td> Insira ou mapeie a ID do registro para o qual deseja recuperar dependências. </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### Listar cenários para uma conexão

Este módulo retorna uma lista paginada de cenários que fazem referência à conexão fornecida.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da conexão</td> 
   <td>Insira ou mapeie a ID da conexão para a qual deseja retornar cenários.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Propriedade</td> 
   <td>Para cada filtro de propriedade para o qual deseja retornar resultados, clique em <b>Adicionar item</b> e insira o campo, o operador e o valor que deseja filtrar. Também é possível filtrar se o campo existe ou não.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Start</td> 
   <td>Insira o local onde deseja iniciar os resultados retornados. Isso é usado para paginação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que você deseja que o módulo retorne para cada ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordenar por</td> 
   <td>Selecione o campo pelo qual deseja ordenar os resultados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direção</td> 
   <td>Selecione se deseja ordenar os resultados em ordem crescente ou decrescente.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar as regiões e organizações de Fusão

Esse módulo retorna a ID de região e organização para cada organização do Fusion que a conexão pode acessar, com base nas credenciais e no acesso no perfil de usuário IMS das credenciais usadas na conexão.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Workfront Fusion ao Workfront Fusion, consulte <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Conectar o Workfront Fusion ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
 </tbody> 
</table>





