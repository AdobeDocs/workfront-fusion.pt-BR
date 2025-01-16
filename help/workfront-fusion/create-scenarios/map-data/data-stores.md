---
title: Repositórios de Dados em [!DNL Adobe Workfront Fusion]
description: Um armazenamento de dados, semelhante a um banco de dados ou a uma tabela simples, pode armazenar dados de cenários, possibilitando a transferência de dados entre cenários individuais ou execuções de cenário. Você pode usar um armazenamento de dados para armazenar novos dados de vários sistemas durante a sincronização.
author: Becky
feature: Workfront Fusion
exl-id: 8bfa3201-45db-49d7-985d-9c324acd56b6
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 1%

---

# Criar e gerenciar armazenamentos de dados

Um armazenamento de dados, semelhante a um banco de dados ou a uma tabela simples, pode armazenar dados de cenários, possibilitando a transferência de dados entre cenários individuais ou execuções de cenário. Você pode usar um armazenamento de dados para armazenar novos dados de vários sistemas durante a sincronização.

Os módulos de armazenamento de dados permitem que você execute as seguintes ações nos registros do seu armazenamento de dados [!DNL Adobe Workfront Fusion]:

* Adicionar
* Substituir
* Atualizar
* Recuperar
* Excluir
* Pesquisar
* Contagem

Para obter informações sobre como usar módulos de armazenamento de dados, consulte [[!UICONTROL Data store] módulos](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md).

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

## Espaço de dados disponível

Se sua organização estiver no novo modelo de plano do Workfront (pacotes Select, Prime e Ultimate), o plano de sua organização afetará o tamanho e o número de armazenamentos de dados disponíveis na instância do Fusion.

### plano do Ultimate

As instâncias do Fusion no pacote do Ultimate recebem:

* 100 MB de espaço
* 50 armazenamentos de dados

### Planos Select e Prime

As instâncias do Fusion nos pacotes Select ou Prime recebem:—>

* 100 MB para as primeiras operações de 500K.

* 10 MB para cada operação adicional de 100K.

  Por exemplo, uma organização com operações de 600 K recebe 110 MB.

Sua organização pode ter até 50 armazenamentos de dados. O tamanho combinado desses armazenamentos de dados não pode exceder o tamanho total do armazenamento de dados de sua organização.

## Criar um armazenamento de dados em [!DNL Workfront Fusion]

* [Configurar o armazenamento de dados](#set-up-the-data-store)
* [Configurar a estrutura de dados](#set-up-the-data-structure)

### Configurar o armazenamento de dados

Antes de usar um armazenamento de dados em um módulo, você deve criar o armazenamento de dados em [!DNL Workfront Fusion].

>[!NOTE]
>
>Sua organização tem um número limitado de armazenamentos de dados disponíveis. Se você tentar criar mais armazenamentos de dados do que o número disponível, o [!DNL Workfront] retornará um erro [!UICONTROL Maximum stores reached].
>
>Para obter mais informações, consulte [O máximo de armazenamentos atingiu o erro](#maximum-stores-reached-error) neste artigo.

1. Faça logon em sua conta do [!DNL Workfront Fusion].
1. Clique em **[!UICONTROL Data stores]** no painel de navegação esquerdo.
1. Clique em **[!UICONTROL Add data store]** no canto superior direito da tela.
1. Insira as configurações para o novo armazenamento de dados.

   Um título em negrito em um campo em um módulo [!DNL Workfront Fusion] indica uma configuração necessária.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data store name] </td> 
      <td> <p>Insira um nome para o armazenamento de dados. </p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Data Structure]</p> </td> 
      <td> <p>Uma estrutura de dados é uma lista das colunas de uma tabela. Essa lista indica o nome da coluna e o tipo de dados.</p> <p>Siga um destes procedimentos:</p> 
       <ul> 
        <li><b>Selecionar uma estrutura de dados que já foi criada</b></li> 
        <li><b>Adicionar uma nova estrutura de dados</b> <p>Clique em <strong>[!UICONTROL Add]</strong> para criar uma nova estrutura de dados.</p> <p>Para obter mais informações, consulte a seção <a href="#set-up-the-data-structure" class="MCXref xref">Configurar a estrutura de dados</a> neste artigo.</p> </li> 
        <li style="font-weight: bold;"> <p>Deixe o campo vazio</p> <p style="font-weight: normal;">Se você não selecionar ou adicionar uma estrutura de dados, o banco de dados conterá apenas a chave primária. Esse tipo de banco de dados é útil se você quiser salvar somente as chaves e estiver interessado em saber apenas se uma chave específica existe ou não no banco de dados.</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>Tamanho do armazenamento de dados em MB</td> 
      <td> <p>Aloque o tamanho do armazenamento de dados do armazenamento de dados interno total.</p> <p> O valor padrão é 10 MB. Se você tiver menos de 10 MB de espaço não alocado no Armazenamento de dados da alocação de 95 MB, o tamanho padrão será o volume de armazenamento não alocado.  <p>Nota: A quantia reservada pode ser alterada a qualquer momento.</p>  </td> 
     </tr> 
    </tbody> 
   </table>

### Configurar a estrutura de dados

1. Ao criar ou editar um armazenamento de dados, clique em **[!UICONTROL Add]**.
1. Na caixa **[!UICONTROL Add data structure]** que é exibida, configure os seguintes campos:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data structure name]</td> 
      <td> <p> Insira um nome para a nova estrutura de dados.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Specification]</p> </td> 
      <td> <p>Siga um destes procedimentos para configurar as colunas do armazenamento de dados.</p> 
       <ul> 
        <li> <p>Clique em <strong>[!UICONTROL Add item]</strong> para especificar as propriedades de uma coluna manualmente.</p> <p>Insira o <strong>[!UICONTROL Name]</strong> e o <strong>[!UICONTROL Type]</strong> para a coluna de armazenamento de dados e defina as propriedades correspondentes.</p> </li> 
        <li> <p>Clique em <strong>[!UICONTROL Generator]</strong> para determinar as colunas com base nos dados de exemplo fornecidos.</p> 
         <div class="example" data-mc-autonum="<b>Example: </b>">
          <span class="autonumber"><span><b>Exemplo: </b></span></span> 
          <p>Por exemplo, os seguintes dados de amostra JSON criam três colunas: nome, idade e número de telefone. O número de telefone é uma coleção de números de telefone celular e fixo.</p> 
          <p><code>&lbrace;</code> </p> 
          <p><code>"name":"John",</code> </p> 
          <p><code>"age":30,</code> </p> 
          <p><code>"phone number": &lbrace;</code> </p> 
          <p><code>"mobile":"987654321",</code> </p> 
          <p><code>"landline":"123456789"</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p>As colunas vazias na exibição do armazenamento de dados:</p> 
          <p> <img src="assets/empty-columns-350x132.png" style="width: 350;height: 132;"> </p> 
          <p>Você pode adicionar valores ao armazenamento de dados manualmente ou usando os módulos de armazenamento de dados [!DNL Workfront Fusion].</p> 
         </div> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Strict] </td> 
      <td> <p>Habilite essa opção para garantir que a carga corresponda às estruturas de dados. Cargas que contêm itens extras não especificados na estrutura de dados são rejeitadas.</p> </td> 
     </tr> 
    </tbody> 
   </table>

## Editar um armazenamento de dados existente

Você pode editar as propriedades e o conteúdo de um armazenamento de dados existente na área [!UICONTROL Data stores] de [!DNL Workfront Fusion].

* [Editar as propriedades de um armazenamento de dados](#edit-the-properties-of-a-data-store)
* [Editar o conteúdo de um armazenamento de dados](#edit-the-contents-of-a-data-store)

### Editar as propriedades de um armazenamento de dados

As propriedades de um armazenamento de dados incluem a estrutura de dados que o armazenamento de dados usa, bem como o tamanho do armazenamento de dados.

1. Clique em **[!UICONTROL Data stores]** ![](assets/data-store-icon.png) no painel de navegação esquerdo para abrir a área [!UICONTROL Data stores].
1. Clique em **[!UICONTROL Edit]** ![](assets/data-store-edit.png) ao lado do armazenamento de dados que você deseja editar.
1. (Opcional) Se quiser alterar a estrutura de dados usada por esse armazenamento de dados para outra estrutura de dados existente, selecione-a no menu suspenso **[!UICONTROL Data structure]**.

   Ou

   (Opcional) Se você quiser alterar a estrutura de dados usada por esse armazenamento de dados para uma estrutura de dados totalmente nova, consulte [Configurar a estrutura de dados](#set-up-the-data-structure) neste artigo.

1. (Opcional) Altere o tamanho do armazenamento de dados inserindo o novo tamanho no campo **[!UICONTROL Data storage size in MB]**.
1. Clique em **[!UICONTROL Save]**.

### Editar o conteúdo de um armazenamento de dados

1. Clique no ícone **[!UICONTROL Data Store]** ![](assets/data-store-icon.png) no painel de navegação esquerdo para abrir a área [!UICONTROL Data Store].
1. Clique em **[!UICONTROL Browse]** ao lado do armazenamento de dados que você deseja editar.
1. (Opcional) Reordene as colunas arrastando-as para o local desejado.
1. (Opcional) [!UICONTROL Edit] uma única célula, clicando no ícone **[!UICONTROL Edit]** nessa célula e digitando o valor desejado.
1. (Opcional) Adicione um novo item ao armazenamento de dados, clicando em **[!UICONTROL Add]** e inserindo as informações do novo item.
1. Clique em **[!UICONTROL Save]**.

## Solução de problemas

* [Restauração de dados perdidos de um armazenamento de dados](#restoring-lost-data-from-a-data-store)
* [Erro de falta de espaço](#out-of-space-error)
* [Erro de máximo de armazenamentos atingido](#maximum-stores-reached-error)

### Restauração de dados perdidos de um armazenamento de dados

No momento, não há nenhuma ferramenta que possa automatizar a restauração de dados perdidos.

#### Solução alternativa

1. Examine todos os logs de execução de cenários em que os itens foram inseridos no armazenamento de dados.

   Para obter mais informações sobre o exame de logs de execução, consulte [Exibir o histórico de execução de um cenário](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md).

1. Copie os dados.
1. Insira os dados no armazenamento de dados novamente.

   Para obter informações sobre como inserir dados em um armazenamento de dados, consulte [Editar o conteúdo de um armazenamento de dados](#edit-the-contents-of-a-data-store) neste artigo.

### Erro [!UICONTROL Out of space]

Erro [!UICONTROL Out of Space]. Seus armazenamentos de dados criados anteriormente já receberam o armazenamento de armazenamento de dados alocado.

#### Solução alternativa

1. Edite qualquer um dos armazenamentos de dados existentes para usar menos espaço. Isso libera espaço para o novo armazenamento de dados.

   Para obter mais informações, consulte [Editar as propriedades de um armazenamento de dados](#edit-the-properties-of-a-data-store) neste artigo.

>[!NOTE]
>
>Recomendamos que você não atribua todo o seu espaço a um único armazenamento de dados, a menos que tenha certeza de que não exigirá mais armazenamentos de dados.

### Erro [!UICONTROL Maximum stores reached]

Um erro [!UICONTROL Maximum stores reached] ocorre porque sua organização usou todos os seus armazenamentos de dados disponíveis.

#### Solução alternativa

Para reduzir o número de armazenamentos de dados existentes, considere seguir um destes procedimentos:

* Combinar armazenamentos de dados existentes
* Excluir armazenamentos de dados não utilizados
