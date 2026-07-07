---
title: Mapear dados usando funções personalizadas
description: Ao mapear itens, você pode usar funções para criar fórmulas simples ou complexas.
author: Becky
feature: Workfront Fusion
exl-id: dc4e697a-a65c-48bc-99de-8e26fbeb7ba7
source-git-commit: 314c4535a5ef14794458f40002a53ee529c1a4b6
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 15%

---

# Mapear dados usando funções personalizadas

É possível criar funções personalizadas na área Funções do Fusion. Em seguida, adicione essas funções aos seus cenários na forma de um módulo do Adobe App Builder.

Como as funções personalizadas funcionam por meio do Adobe App Builder, sua organização deve ter uma licença do Adobe App Builder para usá-las.

As funções personalizadas, como a maioria dos elementos de cenário, são de propriedade de equipes.

As funções são funções simples do JavaScript. Para incluir variáveis ou dependências na lógica da função, use pacotes.

Para obter informações sobre pacotes, consulte [Usar pacotes de função personalizada](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

O Workfront Fusion também inclui funções integradas que permitem criar fórmulas simples ou complexas. Essas funções cobrem uma grande variedade de casos de uso, incluindo funções para matrizes, sequências, números e dados de módulos anteriores.

Para obter informações e instruções sobre funções internas, consulte [Mapear um item usando funções internas](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

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

## Configurar uma função personalizada

Você pode criar uma função personalizada na área Funções que pode ser usada em vários cenários ou pode configurar funções personalizadas em cenários individuais.

* [Criar uma função personalizada para usar em vários cenários](#create-a-custom-function-to-use-in-multiple-scenarios)
* [Criar uma função personalizada em um cenário](#create-a-custom-function-within-a-scenario)

### Criar uma função personalizada para usar em vários cenários

As funções personalizadas que podem ser usadas em vários cenários são configuradas na área Funções do Workfront Fusion. Depois que uma função é configurada, é possível adicioná-la a um cenário usando o conector do Adobe App Builder.

* [Inicializar o ambiente de tempo de execução](#initialize-your-runtime-environment)
* [Crie uma função personalizada na área Funções](#create-a-custom-function-in-the-functions-area)

#### Inicializar o ambiente de tempo de execução

Antes de criar funções personalizadas, você deve inicializar seu ambiente de tempo de execução. Isso só precisa ser feito se a sua equipe não tiver funções personalizadas.

>[!IMPORTANT]
>
>A inicialização só pode ser executada por um usuário com acesso ao Adobe App Builder, um desenvolvedor ou um administrador do sistema na organização IMS.
>
>Após a conclusão da inicialização, todos os usuários da equipe onde ela foi executada podem criar e utilizar funções.

1. Clique na guia **Funções** ![Ícone Funções](assets/functions-icon.png) no painel esquerdo.

   Se ainda não tiver configurado o tempo de execução, você verá a mensagem &quot;Ambiente de tempo de execução não configurado&quot;.
1. Clique em **Inicializar tempo de execução**.

   Após algum tempo, uma lista de Funções é exibida, com duas funções de exemplo.

#### Crie uma função personalizada na área Funções

Depois que o ambiente de tempo de execução for configurado, você poderá começar a criar funções personalizadas.

>[!IMPORTANT]
>
>* Sua função personalizada **deve** ser uma função JavaScript.
>* Sua função personalizada **deve** retornar um objeto.
>* Depois de criar uma função personalizada, você não pode:
>
>   * Alterar seu nome
>   * Exibir os valores de parâmetro padrão

1. Clique na guia **Funções** ![Ícone Funções](assets/functions-icon.png) no painel esquerdo.
1. Clique em **Adicionar função**.
1. Insira um nome para a função personalizada.

   Você não poderá alterar este nome posteriormente.
1. Insira o código da função.
1. Para cada valor de parâmetro padrão que você deseja adicionar, clique em **Adicionar Parâmetro** e insira o nome do parâmetro e o valor padrão.

   Você pode substituir parâmetros padrão ao adicionar a função a um cenário.
1. Clique em **Salvar**

### Criar uma função personalizada em um cenário

Para criar uma função personalizada em um cenário, use o módulo **Executar um bloco de código personalizado** no conector do Adobe App Builder.

Para obter instruções, consulte [módulo Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

## Adicionar uma função personalizada a um cenário

Para adicionar uma função personalizada a um cenário, use o conector do Adobe App Builder.

Para obter instruções, consulte [módulo Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

