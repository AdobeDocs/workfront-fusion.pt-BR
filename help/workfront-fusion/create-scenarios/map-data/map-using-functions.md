---
title: Mapear itens usando funções
description: Ao mapear itens, você pode usar funções para criar fórmulas simples ou complexas.
author: Becky
feature: Workfront Fusion
exl-id: b9d7643e-febf-42e2-9ddc-8ec8eba98e7a
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Mapear um item usando funções

Ao mapear itens, você pode usar funções para criar fórmulas simples ou complexas. As funções disponíveis são semelhantes às funções no Excel e em algumas linguagens de programação:

* Eles avaliam a lógica geral, matemática, texto, datas e matrizes.
* Elas permitem executar lógica condicional e transformações de valores de item, como converter um texto em maiúsculas, cortar texto, converter uma data em um formato diferente e muito mais.

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

## Inserir funções em campos

Para inserir uma função em um campo:

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja mapear dados.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no campo onde deseja inserir uma função.
1. Selecione a guia no painel de mapeamento que contém a função que você deseja inserir.

   Para obter informações sobre guias do painel de mapeamento, consulte [Visão geral da função](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)
   1. Clique no nome da função.

      Ou

      Arraste a função para o campo.
1. Configure os parâmetros da função.

   Para obter uma explicação dos parâmetros da função, passe o mouse sobre a função no painel de mapeamento.

   Para obter mais informações sobre funções e seus parâmetros, consulte os artigos em [Referências da função: índice do artigo](/help/workfront-fusion/references/mapping-panel/functions/functions-toc.md).

1. Continue a configurar o módulo ou clique em **OK**.

>[!TIP]
>
>Ao criar uma fórmula complexa que deseja reutilizar em outro campo, você pode clicar no campo que contém a combinação, usar Cmd-A ou Ctrl-A para selecioná-lo e, em seguida, copiá-lo e colá-lo no outro campo.


>[!BEGINSHADEBOX]

**Exemplo:** alguns tipos de dados impedem que os usuários insiram mais do que um determinado número de caracteres. Você pode usar a função substring para limitar um valor a um determinado número de caracteres.

Neste exemplo, a função de subsequência de caracteres limita o nome do projeto a 50 caracteres.

![Exemplo de restrição de duração da reunião](assets/example-meet-length-restriction-350x184.png)

>[!ENDSHADEBOX]

## Aninhamento de funções

É possível aninhar funções entre si.

>[!BEGINSHADEBOX]

**Exemplo:**

Neste exemplo, a função substring limita o nome do projeto aparado a 50 caracteres.

![Nome reduzido](assets/trimmed-name-under-50.png)

>[!ENDSHADEBOX]

Para aninhar uma função:

1. Clique no campo onde você está criando uma fórmula.

   Isso abre o painel de mapeamento.

1. Clique na primeira função que deseja adicionar. Esta é a função no exterior. No exemplo a seguir, esta é a função `substring`.
1. Nessa função, clique para onde deseja que a função aninhada vá. Neste exemplo, a função aninhada vai no lugar do primeiro parâmetro.
1. No painel de mapeamento, clique na função aninhada. Neste exemplo, esta é a função `trim`.
1. Continue a configurar a função conforme desejado.
1. Continue a configurar o módulo ou clique em **OK**.

## Usar funções [!DNL Google Sheets]

Se o Workfront Fusion não apresentar uma função que você queira usar, mas que seja apresentada por [!DNL Google Sheets], você poderá usá-la seguindo estas etapas:

1. Em [!DNL Google Sheets], crie uma nova planilha vazia.
1. No Workfront Fusion, abra o cenário.
1. Adicione o módulo **[!DNL Google Sheets]** >**[!UICONTROL Atualizar uma célula]** ao cenário.

1. Configure o módulo:

   1. Escolha a planilha recém-criada no campo **[!UICONTROL Planilha]**.
   1. Insira a fórmula que contém as funções [!DNL Google Sheets] no campo **[!UICONTROL Valor]**.

      Você pode usar a saída dos módulos anteriores como de costume.

      ![Usar funções do Google Sheets](assets/exploit-google-sheet-functions-350x218.png)

1. Insira o módulo **[!UICONTROL Google Sheets] >[!UICONTROL Get a cell]** para obter o resultado calculado.
1. Configure o módulo, usando a mesma ID de célula que você usou na etapa 4.

   ![Usar funções do Google Sheets](assets/exploit-google-sheet-functions-2-350x187.png)
