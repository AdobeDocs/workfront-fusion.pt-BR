---
title: Usar Pacotes de Função Personalizados
description: Ao mapear itens, você pode usar funções para criar fórmulas simples ou complexas.
author: Becky
feature: Workfront Fusion
source-git-commit: 4ec81401b5a76edd620b9779414ee578966b4315
workflow-type: tm+mt
source-wordcount: '2042'
ht-degree: 5%

---


# Usar pacotes de função personalizados

Os pacotes permitem criar e executar sua própria lógica personalizada no Adobe Workfront Fusion, sem sair da interface do Fusion. Quando os módulos padrão não fazem exatamente o que é necessário, você pode usar uma função para transformar dados, fazer um cálculo, chamar um serviço externo ou empacotar uma rotina que deseja reutilizar. Você pode testá-lo, ativá-lo e usá-lo a partir de seus cenários.

Funções complexas podem exigir recursos como variáveis e dependências como bibliotecas. Para essas funções, você pode criar um pacote que inclua a função e seus recursos.

Um pacote pode incluir:

* **Funções**: a lógica que é executada durante a execução de um cenário.
* **Variáveis**: valores reutilizáveis, como uma URL base ou uma chave de API, que a função no pacote usa.
* **Dependências**: as bibliotecas externas nas quais suas funções podem confiar.
* **Histórico**: versões anteriores de cada função, salvas automaticamente, às quais você pode fazer referência.


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
   <p><ul><li>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li><li>Você deve ter uma licença do Adobe App Builder para usar funções personalizadas.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Configurar a conexão do ambiente de tempo de execução

>[!NOTE]
>
>Esta é uma configuração única.

Na primeira vez que sua equipe usar esse recurso, você deve configurar o ambiente que executa as funções. Você só faz isso uma vez por equipe.

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.

   Se o ambiente não foi configurado, a tela **Ambiente de Tempo de Execução Não Configurado** é exibida.

1. Clique em **Inicializar tempo de execução**.

1. Para inserir um nome diferente do padrão, digite o nome no campo **Nome da conexão**.

1. Selecione o projeto do Adobe App Builder ao qual esse pacote pertencerá:

   * Para selecionar um projeto existente, comece digitando o nome do projeto e, em seguida, selecione-o quando ele for exibido.
   * Para criar um novo projeto, insira um nome que ainda não existe e clique em **Criar novo**.
   * Se você deixar isso vazio, o Fusion usará um projeto padrão.

1. Selecione **Continuar**.

   O Fusion conclui a configuração e você está pronto para criar pacotes.

   Seu ambiente aparece como uma guia de conexão na parte superior da página.

   ![Ambiente como guia de conexão](assets/package-environment-as-connection.png)

1. (Condicional) Para adicionar outro ambiente, clique no ícone de adição e siga as instruções desta seção.

1. (Condicional) Para remover um ambiente existente, passe o mouse sobre a guia de conexão de ambiente e clique em **X** quando ele aparecer.

   >[!WARNING]
   >
   >A remoção de uma conexão desconecta o Fusion desse ambiente. Os pacotes nele contidos não estão mais disponíveis no Fusion por meio dessa conexão.

## Criar e abrir um pacote

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.

1. Selecione a guia da conexão na qual deseja trabalhar.

1. Clique em **Criar pacote**.

1. Insira um nome e selecione **Criar**.

   O pacote é aberto automaticamente.

1. Para reabrir um pacote mais tarde, selecione-o na lista Pacotes e selecione **Exibir**.
1. Para excluir um pacote, selecione-o na lista Pacotes e escolha **Excluir**.

   >[!WARNING]
   >
   >A exclusão de um pacote o remove permanentemente e tudo o que está dentro dele.

## Gerenciar um pacote

Um pacote aberto é organizado em quatro áreas:

* **Funções**: criar, testar e publicar a função.
* **Variáveis**: configure variáveis para a função.
* **Dependências**: instale dependências, como bibliotecas externas, para esta função.
* **Histórico**: exibir versões anteriores de cada função.

Além dessas quatro áreas, um medidor de armazenamento na parte superior mostra quanto do seu espaço é usado. Cada pacote tem um limite de tamanho total de **21 MB**. Isso inclui funções, variáveis e dependências, incluindo versões salvas.

Se não houver espaço, recomendamos remover dependências, variáveis ou versões mais antigas não usadas para liberar espaço.

Para voltar para a lista de pacotes, selecione a seta para trás ao lado do nome do pacote.

<!--Create toc here-->
* [Funções](#functions)
* [Variáveis](#variables)
* [Dependências](#dependencies)
* [Histórico](#history)

### Funções

A área **Funções** exibe uma lista de funções no pacote, incluindo o nome da função, seu status, seu tamanho e quantas entradas ele espera.

* [Exibir e gerenciar a lista de Funções](#view-and-manage-the-functions-list)
* [Crie ou edite uma função na área Pacotes](#create-or-edit-a-function-in-the-packages-area)
* [Fazer alterações em uma função ativa](#make-changes-to-a-live-function)
* [Excluir uma função](#delete-a-function)

#### Exibir e gerenciar a lista de Funções

Para filtrar a lista Funções:

1. Filtre por status clicando em **Todos**, **Rascunhos** ou **Publicados**.
1. Use a barra de pesquisa para procurar funções específicas.

Uma função pode ter o status de rascunho ou publicada.

* **Rascunho**: as funções no status Rascunho são trabalhos em andamento. É possível editar e testar livremente sem afetar os dados em tempo real.
* **Publicado**: as versões publicadas estão online. Seus cenários executam versões publicadas das funções.

Usar rascunhos permite fazer alterações com segurança. Você pode refinar um rascunho, testá-lo e publicá-lo quando estiver satisfeito.

| Status | O que significa |
|---|---|
| **Publicado** | Existe uma versão disponível. |
| **Rascunho** | A função ainda está em andamento ou uma função ativa tem alterações que você ainda não publicou. |

#### Crie ou edite uma função na área Pacotes

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Na área **Funções**, selecione **Criar função**.

   Ou

   Clique na caixa de seleção ao lado de uma função existente e selecione **Editar** na barra de ações na parte inferior da página.

1. (Condicional) Se você estiver criando uma nova função, no campo **Nova função**, digite um nome para a função.

1. (Opcional e condicional) Para renomear uma função existente, clique no ícone Editar ao lado do nome da função e insira o novo nome.

1. Na guia **Código**, insira a lógica da função.

   Considere o seguinte ao criar sua função:

   * As funções devem ser gravadas no JavaScript.
   * Você pode ler as entradas definidas, reutilizar as variáveis e chamar as outras funções.
   * À medida que você digita, as sugestões são exibidas.

1. Para limpar a formatação da função, clique em **Beliscar**.

1. (Opcional) Na guia **Parâmetros**, defina as entradas que sua função espera.

   Para obter informações sobre entradas, consulte [Definir entradas](#define-inputs) neste artigo.

1. Na guia **Testar**, teste sua função.

   Para obter instruções, consulte [Testar uma função](#test-a-function) neste artigo.

1. Para salvar esta função como rascunho, clique em **Salvar como rascunho**.

   Ou

   Para publicar a função, clique em **Publicar**.

   >[!NOTE]
   >
   >A publicação de uma função limpa seu histórico de versões. A versão publicada se torna o ponto de partida atual e as versões de rascunho anteriores não são mais mantidas.

* [Definir entradas](#define-inputs)
* [Testar uma função](#test-a-function)

##### Definir entradas

Você pode usar a guia **Parâmetros** para descrever as informações de que sua função precisa sempre que for executada.

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Na área **Funções**, selecione **Criar função**.

   Ou

   Clique na caixa de seleção ao lado de uma função existente e selecione **Editar** na barra de ações na parte inferior da página.

1. Clique na guia **Parâmetros**.

1. Para cada parâmetro que você deseja adicionar, clique em **Adicionar Parâmetro** e configure o seguinte:

* **Nome**: o nome da entrada
* **Rótulo**: um nome amigável mostrado quando você testa a função
* **Tipo**: o tipo de dados, como texto, número, verdadeiro/falso ou um objeto estruturado.
* **Obrigatório**: se um valor deve ser fornecido.

Essas entradas se tornam os campos que você preenche ao testar e os valores que o cenário passa ao executar a função.

##### Testar uma função

Recomendamos testar uma função antes de publicá-la.

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Na área **Funções**, selecione **Criar função**.

   Ou

   Clique na caixa de seleção ao lado de uma função existente e selecione **Editar** na barra de ações na parte inferior da página.

1. Clique na guia **Testar**.

1. Insira um valor para cada entrada.

1. Execute a função:

   * Selecione **Testar rascunho** para experimentar sua versão de trabalho em andamento.
   * Selecione **Executar Publicado** para executar a versão ao vivo.

1. Revise o resultado, incluindo se ele foi bem-sucedido, quanto tempo levou e a saída retornada.

>[!NOTE]
>
>**Executar Publicado** está disponível somente após uma função ter sido publicada.

#### Fazer alterações em uma função ativa

Depois que uma função é publicada, o botão **Publicar** se torna um menu:

* **Republicar** — envie suas alterações de rascunho mais recentes para a versão ao vivo.
* **Cancelar publicação** — retire a função do serviço. Seu trabalho é mantido como um rascunho para que você possa voltar a ele.

#### Excluir uma função

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Clique na caixa de seleção ao lado de uma função existente e selecione **Excluir** na barra de ações, na parte inferior da página.

>[!WARNING]
>
>Excluir uma função a remove completamente, juntamente com seu histórico. Qualquer cenário ou função que o use deixará de funcionar.

### Variáveis

As variáveis são valores reutilizáveis que suas funções podem usar, como um URL de base, uma ID de conta ou uma chave de API. Armazená-los como variáveis significa definir um valor uma vez e atualizá-lo em um local, em vez de atualizá-lo em várias funções.

* [Criar ou editar uma variável](#create-or-edit-a-variable)
* [Excluir uma variável](#delete-a-variable)

#### Criar ou editar uma variável

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Na guia **Variáveis**, selecione **Nova variável**.

   Ou


   Clique no ícone **Editar** ao lado da variável que você deseja editar.

1. Preencha os detalhes:

   * **Chave**: insira o nome que suas funções usam para fazer referência ao valor.

   Para renomear essa variável, altere o valor da Chave.
   * **Valor**: insira o valor a ser armazenado.
   * **Tipo**: selecione se o tipo de valor é texto, um número, booleano (true/false) ou um objeto estruturado.
   * **Descrição**: insira uma observação opcional para lembrá-lo de sua finalidade.
   * **Público**: ative esta opção se desejar usar a variável no designer de cenários. Quando desativada, a variável só estará disponível dentro das funções do pacote.
   * **Segredo**: ative esta opção para ocultar valores confidenciais, como chaves. O valor é oculto na lista de variáveis e também é limpo para não ser exposto no designer de cenário. Suas funções ainda recebem o valor real quando são executadas.

1. Selecione **Criar variável** ou **Salvar alterações**.

#### Excluir uma variável

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Na guia **Variáveis**, clique no ícone **Excluir** ao lado da variável que você deseja excluir.

>[!WARNING]
>
>As funções que usam uma variável excluída deixarão de funcionar.

### Dependências

Algumas funções exigem bibliotecas extras para fazer seu trabalho. A guia **Dependências** é onde você adiciona e gerencia essas bibliotecas.

* [Adicionar bibliotecas](#add-libraries)
* [Remover uma biblioteca](#remove-a-library)

#### Adicionar bibliotecas

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Na guia **Dependências**, digite um ou mais nomes de biblioteca, separados por vírgulas. Você pode solicitar uma versão específica adicionando-a depois do nome (por exemplo, `axios, lodash@4.17.21`).

1. Clique em **Instalar**.

#### Remover uma biblioteca

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Na guia **Dependências**, clique no ícone **Excluir** ao lado da biblioteca que você deseja remover.

>[!WARNING]
>
>As funções que dependem de uma biblioteca removida podem parar de funcionar.

### Histórico

Toda vez que você salva um rascunho de uma função, o Fusion mantém uma cópia. A guia **Histórico** permite exibir e restaurar versões anteriores.

1. Clique na guia **Pacotes** ![Pacotes](assets/packages-icon.png) no painel de navegação esquerdo.
1. Na guia **Histórico**, selecione uma função à esquerda para ver suas versões salvas, as mais recentes primeiro.
1. Selecione uma versão para visualizar exatamente o que ela continha naquele momento.
1. Para restaurar uma versão, clique em **Restaurar como rascunho**.

   A versão é restaurada como um novo rascunho, para que você possa revisá-la e testá-la antes de publicar. Sua versão ao vivo permanecerá em vigor até que você publique.
1. Para excluir uma versão, selecione-a, clique em **Excluir versão** e confirme.

>[!NOTE]
>
>* A publicação de uma função limpa seu histórico. O histórico acompanha as alterações feitas enquanto você trabalha em um rascunho, até que você publique.
>* A exclusão de uma versão não pode ser desfeita.



## Usar um pacote em um cenário

A finalidade de criar funções e variáveis é colocá-las para funcionar em seus cenários. Para usar funções e variáveis, use o conector do **Adobe App Builder**.

* **Usar função do pacote**: este módulo executa uma de suas funções como uma etapa em um cenário. Escolha o pacote e a função, preencha as entradas definidas e o resultado da função será transmitido para os módulos a seguir.
* **Usar variável do pacote**: este módulo traz uma das variáveis do pacote para um cenário, de modo que você possa mapear seu valor para outros módulos.

Para obter informações e instruções, consulte [módulos do Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

<!--

To add one:

1. In the scenario designer, add a module and choose the **Adobe App Builder** connector.

1. Select **Use function from package** or **Use variable from package**.

1. Choose the package and the function or variable you want, then map the inputs or value as needed.

>[!NOTE]
>
>Publish a function before using it in a scenario, and turn on **Public** for any variable you want to use there.

-->





