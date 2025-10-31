---
title: Armazenamentos de dados no Adobe Workfront Fusion
description: Um armazenamento de dados, semelhante a um banco de dados ou a uma tabela simples, pode armazenar dados de cenários, possibilitando a transferência de dados entre cenários individuais ou execuções de cenário. Você pode usar um armazenamento de dados para armazenar novos dados de vários sistemas durante a sincronização.
author: Becky
feature: Workfront Fusion
exl-id: 8bfa3201-45db-49d7-985d-9c324acd56b6
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '1321'
ht-degree: 1%

---

# Criar e gerenciar armazenamentos de dados

Um armazenamento de dados, semelhante a um banco de dados ou a uma tabela simples, pode armazenar dados de cenários, possibilitando a transferência de dados entre cenários individuais ou execuções de cenário. Você pode usar um armazenamento de dados para armazenar novos dados de vários sistemas durante a sincronização.

Os módulos de armazenamento de dados permitem que você execute as seguintes ações nos registros do seu armazenamento de dados do Adobe Workfront Fusion:

* Add
* Substituir
* Atualização
* Recuperar
* Excluir
* Pesquisar
* Contagem

Para obter informações sobre como usar os módulos de repositório de dados, consulte [[!UICONTROL Repositório de dados] módulos](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md).

Para obter uma introdução em vídeo aos armazenamentos de dados no Workfront Fusion, consulte:

* [Repositórios de Dados](https://video.tv.adobe.com/v/3427029/){target=_blank}

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
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Espaço de dados disponível

Se sua organização estiver no novo modelo de plano do Workfront (pacotes Select, Prime e Ultimate), o plano de sua organização afetará o tamanho e o número de armazenamentos de dados disponíveis na instância do Fusion.

### plano do Ultimate

As instâncias do Fusion no pacote do Ultimate recebem:

* 100 MB de espaço
* 50 armazenamentos de dados

### Planos Select e Prime

As instâncias do Fusion nos pacotes Select ou Prime recebem:-->

* 100 MB para as primeiras operações de 500K.

* 10 MB para cada operação adicional de 100K.

  Por exemplo, uma organização com operações de 600 K recebe 110 MB.

Sua organização pode ter até 50 armazenamentos de dados. O tamanho combinado desses armazenamentos de dados não pode exceder o tamanho total do armazenamento de dados de sua organização.

## Criar um armazenamento de dados no Workfront Fusion

* [Configurar o armazenamento de dados](#set-up-the-data-store)
* [Configurar a estrutura de dados](#set-up-the-data-structure)

### Configurar o armazenamento de dados

Antes de usar um armazenamento de dados em um módulo, você deve criar o armazenamento de dados no Workfront Fusion.

>[!NOTE]
>
>Sua organização tem um número limitado de armazenamentos de dados disponíveis. Se você tentar criar mais armazenamentos de dados do que o número disponível, o Workfront retornará um erro [!UICONTROL Máximo de armazenamentos atingido].
>
>Para obter mais informações, consulte [O máximo de armazenamentos atingiu o erro](#maximum-stores-reached-error) neste artigo.

1. Faça logon na sua conta do Workfront Fusion.
1. Clique em **[!UICONTROL Repositórios de dados]** no painel de navegação esquerdo.
1. Clique em **[!UICONTROL Adicionar armazenamento de dados]** no canto superior direito da tela.
1. Insira as configurações para o novo armazenamento de dados.

   Um título em negrito em um campo em um módulo do Workfront Fusion indica uma configuração necessária.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Nome do armazenamento de dados] </td> 
      <td> <p>Insira um nome para o armazenamento de dados. </p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Estrutura de Dados]</p> </td> 
      <td> <p>Uma estrutura de dados é uma lista das colunas de uma tabela. Essa lista indica o nome da coluna e o tipo de dados.</p> <p>Siga um destes procedimentos:</p> 
       <ul> 
        <li><b>Selecionar uma estrutura de dados que já foi criada</b></li> 
        <li><b>Adicionar uma nova estrutura de dados</b> <p>Clique em <strong>[!UICONTROL Adicionar]</strong> para criar uma nova estrutura de dados.</p> <p>Para obter mais informações, consulte a seção <a href="#set-up-the-data-structure" class="MCXref xref">Configurar a estrutura de dados</a> neste artigo.</p> </li> 
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

1. Ao criar ou editar um armazenamento de dados, clique em **[!UICONTROL Adicionar]**.
1. Na caixa **[!UICONTROL Adicionar estrutura de dados]** que é exibida, configure os seguintes campos:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Nome da estrutura de dados]</td> 
      <td> <p> Insira um nome para a nova estrutura de dados.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Especificação]</p> </td> 
      <td> <p>Siga um destes procedimentos para configurar as colunas do armazenamento de dados.</p> 
       <ul> 
        <li> <p>Clique em <strong>[!UICONTROL Adicionar item]</strong> para especificar as propriedades de uma coluna manualmente.</p> <p>Insira o <strong>[!UICONTROL Name]</strong> e <strong>[!UICONTROL Type]</strong> para a coluna de repositório de dados e defina as propriedades correspondentes.</p> </li> 
        <li> <p>Clique em <strong>[!UICONTROL Generator]</strong> para determinar as colunas a partir dos dados de exemplo fornecidos.</p> 
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
          <p>Você pode adicionar valores ao armazenamento de dados manualmente ou usando os módulos de armazenamento de dados do Workfront Fusion.</p> 
         </div> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Estrito] </td> 
      <td> <p>Habilite essa opção para garantir que a carga corresponda às estruturas de dados. Cargas que contêm itens extras não especificados na estrutura de dados são rejeitadas.</p> </td> 
     </tr> 
    </tbody> 
   </table>

## Editar um armazenamento de dados existente

É possível editar as propriedades e o conteúdo de um armazenamento de dados existente na área [!UICONTROL Repositórios de dados] do Workfront Fusion.

* [Editar as propriedades de um armazenamento de dados](#edit-the-properties-of-a-data-store)
* [Editar o conteúdo de um armazenamento de dados](#edit-the-contents-of-a-data-store)

### Editar as propriedades de um armazenamento de dados

As propriedades de um armazenamento de dados incluem a estrutura de dados que o armazenamento de dados usa, bem como o tamanho do armazenamento de dados.

1. Clique em **[!UICONTROL Repositórios de dados]** ![Ícone de repositório de dados](assets/data-store-icon.png) no painel de navegação esquerdo para abrir a área [!UICONTROL Repositórios de dados].
1. Clique em **[!UICONTROL Editar]** ![Editar armazenamento de dados](assets/data-store-edit.png) ao lado do armazenamento de dados que você deseja editar.
1. (Opcional) Se desejar alterar a estrutura de dados usada por esse armazenamento de dados para outra estrutura de dados existente, selecione-a no menu suspenso **[!UICONTROL Estrutura de dados]**.

   Ou

   (Opcional) Se você quiser alterar a estrutura de dados usada por esse armazenamento de dados para uma estrutura de dados totalmente nova, consulte [Configurar a estrutura de dados](#set-up-the-data-structure) neste artigo.

1. (Opcional) Altere o tamanho do armazenamento de dados inserindo o novo tamanho no campo **[!UICONTROL Tamanho do armazenamento de dados em MB]**.
1. Clique em **[!UICONTROL Salvar]**.

### Editar o conteúdo de um armazenamento de dados

1. Clique no ícone do **[!UICONTROL Repositório de Dados]** ![Ícone do repositório de dados](assets/data-store-icon.png) no painel de navegação esquerdo para abrir a área do [!UICONTROL Repositório de Dados].
1. Clique em **[!UICONTROL Procurar]** ao lado do armazenamento de dados que você deseja editar.
1. (Opcional) Reordene as colunas arrastando-as para o local desejado.
1. (Opcional) [!UICONTROL Edite] uma única célula clicando no ícone **[!UICONTROL Editar]** nessa célula e inserindo o valor desejado.
1. (Opcional) Adicione um novo item ao armazenamento de dados clicando em **[!UICONTROL Adicionar]** e inserindo as informações do novo item.
1. Clique em **[!UICONTROL Salvar]**.

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

### Erro [!UICONTROL Sem espaço]

Erro [!UICONTROL Sem Espaço] porque o armazenamento de dados alocado já foi atribuído a seus armazenamentos de dados criados anteriormente.

#### Solução alternativa

1. Edite qualquer um dos armazenamentos de dados existentes para usar menos espaço. Isso libera espaço para o novo armazenamento de dados.

   Para obter mais informações, consulte [Editar as propriedades de um armazenamento de dados](#edit-the-properties-of-a-data-store) neste artigo.

>[!NOTE]
>
>Recomendamos que você não atribua todo o seu espaço a um único armazenamento de dados, a menos que tenha certeza de que não exigirá mais armazenamentos de dados.

### Erro [!UICONTROL Máximo de armazenamentos atingido]

Um erro de [!UICONTROL Máximo de armazenamentos atingido] ocorre porque sua organização usou todos os seus armazenamentos de dados disponíveis.

#### Solução alternativa

Para reduzir o número de armazenamentos de dados existentes, considere seguir um destes procedimentos:

* Combinar armazenamentos de dados existentes
* Excluir armazenamentos de dados não utilizados
