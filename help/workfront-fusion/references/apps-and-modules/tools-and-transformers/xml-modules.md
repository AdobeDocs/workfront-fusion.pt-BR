---
title: XML
description: O aplicativo XML permite analisar um texto XML formatado por meio do módulo XML &gt; Analisar XML e convertê-lo em um pacote para disponibilizar os dados para outros módulos. Também é possível converter um pacote em um texto XML formatado por meio do módulo XML &gt; Criar XML
author: Becky
feature: Workfront Fusion
exl-id: ab323361-cd04-4dcc-ab02-0fb468334fdb
source-git-commit: 5351c2386ed6f2d030df1df01fcf9ea0de7d813f
workflow-type: tm+mt
source-wordcount: '1292'
ht-degree: 2%

---

# XML

O aplicativo [!UICONTROL XML] permite analisar um texto XML formatado por meio do módulo [!UICONTROL XML] > [!UICONTROL Parse XML] e convertê-lo em um pacote para disponibilizar os dados para outros módulos. Também é possível converter um pacote em um texto formatado XML por meio do módulo [!UICONTROL XML] > [!UICONTROL Create XML]

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

## Criar XML

O módulo [!UICONTROL XML] > [!UICONTROL Create XML] converte um pacote em um texto XML formatado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>A estrutura de dados descreve a estrutura do XML resultante. Se você tiver uma amostra do XML que deseja criar, poderá usá-la para gerar a estrutura de dados:</p> 
    <ol> 
     <li value="1">Clique no botão <strong>[!UICONTROL Add]</strong>.</li> 
     <li value="2">Clique no botão <strong>[!UICONTROL Generator]</strong>.</li> 
     <li value="3">Copie e cole a amostra XML no campo Dados de amostra.</li> 
     <li value="4">Clique no botão <strong>[!UICONTROL Save]</strong>.</li> 
     <li value="5">Verifique se a estrutura de dados foi gerada com êxito.</li> 
     <li value="6">Clique em <strong>[!UICONTROL Save]</strong> para salvar a estrutura de dados.</li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Root element name]</td> 
   <td>Insira o nome do elemento raiz do XML. O valor padrão é <code>root</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype SYSTEM ID]</td> 
   <td>Insira o nome de arquivo a ser usado na declaração <code>!DOCTYPE SYSTEM</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype PUBLIC ID]</td> 
   <td>Insira o nome de arquivo a ser usado na declaração <code>!DOCTYPE PUBLIC</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strip Xml Declaration]</td> 
   <td>Habilite esta opção para remover a Declaração XML <code>&lt;?xml ... ?&gt;</code> e <code>&lt;!DOCTYPE ... &gt;</code> e deixar apenas o elemento raiz XML e seu conteúdo.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Exemplo:**

Um caso de uso típico é transformar dados de uma planilha [!DNL Google] em XML.

1. Coloque o módulo [!DNL Google Sheets] > [!UICONTROL Select rows] no seu cenário para buscar os dados. Configure o módulo para recuperar linhas da planilha [!DNL Google]. Defina o&#x200B;**[!UICONTROL Maximum number of returned rows]** como um número pequeno, mas maior que um para fins de teste (Exemplo, três). Execute o módulo [!DNL Google Sheets] clicando com o botão direito do mouse nele e escolhendo &quot;**[!UICONTROL Run this module only]**&quot;. Verifique a saída do módulo.
1. Conecte o módulo [!UICONTROL Array Aggregator] após o módulo [!DNL Google Sheets]. Na configuração do módulo, escolha o módulo [!DNL Google Sheets] no campo **[!UICONTROL Source node]**. Deixe os outros campos como estão para o momento.
1. Conecte o módulo [!UICONTROL XML] > [!UICONTROL Create XML] após o módulo [!UICONTROL Array Aggregator].

   A configuração do módulo requer uma estrutura de dados que descreva a estrutura da saída XML. Clique no botão **[!UICONTROL Add]** para abrir a configuração da estrutura de dados. A maneira mais fácil de criar essa estrutura de dados é gerá-la automaticamente a partir de uma amostra XML.

1. Clique no botão **[!UICONTROL Generator]** e cole sua amostra XML no campo [!UICONTROL Sample data]:

   ![Campo de dados de exemplo](/help/workfront-fusion/references/apps-and-modules/assets/sample-data-field-350x146.png)

1. Clique em **[!UICONTROL Save]**.

   O campo Specification na estrutura Data agora contém a estrutura gerada.
1. Altere o nome da estrutura de Dados para algo mais específico e clique em **[!UICONTROL Save]**.

   Um campo correspondente ao atributo de matriz raiz aparece como um campo mapeável na configuração do módulo JSON.
1. Clique no botão **[!UICONTROL Map]** ao lado do campo e mapeie o item `Array[]` da saída [!UICONTROL Array aggregator] para ele:
1. Clique em **[!UICONTROL OK]** para fechar a configuração do módulo XML.
1. Abra a configuração do módulo [!UICONTROL Array Aggregator]. Altere o **[!UICONTROL Target structure]** de Personalizado para um campo do módulo XML correspondente ao elemento XML pai.Mapeie os itens do módulo [!DNL Google Sheets] para os campos apropriados.
1. Clique em **[!UICONTROL OK]** para fechar a configuração do módulo Agregador de Matriz.
1. Execute o cenário.

   O módulo XML gera o arquivo XML correto.

1. Abra a configuração do módulo [!DNL Google Sheets] e aumente o número [!UICONTROL Maximum number of returned rows] para que seja maior que o número de linhas na planilha para processar todos os dados.

   O XML resultante pode ser salvo em [!DNL Dropbox], enviado como um anexo por email, carregado via FTP em um servidor e assim por diante.

>[!ENDSHADEBOX]

### Adição de atributos XML

Se quiser adicionar atributos a um nó complexo (um nó que conterá outros nós), adicione uma coleção com o nome `_attributes` para a observação complexa na estrutura de dados personalizada. Esta coleção será mapeada para atributos de nó. Se quiser adicionar atributos a um nó de texto (por exemplo: `<node attr="1">abc</node>`), você deve adicionar uma coleção `_attributes` para atributos e uma propriedade de texto `_value` para o valor do nó para esse nó na estrutura de dados personalizada.

```
{
   "name": "node",
   "type": "collection",
   "spec": [
      {
         "name": "_attributes",
         "type": "collection"
         "spec": [
            {
               "name": "attr1",
               "type": "text"
            }
         ]
      },
      {
         "name": "_value",
         "type": "text"
      }
   ]
}
```

## [!UICONTROL Parse XML]

O módulo [!UICONTROL XML] > [!UICONTROL Parse XML] analisa um texto formatado XML e gera um único pacote contendo todas as informações extraídas do XML.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>A estrutura de dados descreve a estrutura do XML para disponibilizar a saída do módulo no painel de mapeamento dos seguintes módulos.</p> <p>Se você tiver uma amostra do XML que deseja analisar, poderá usá-la para gerar a estrutura de dados:</p> 
    <ol> 
     <li value="1">Clique no botão <strong>[!UICONTROL Add]</strong>.</li> 
     <li value="2">Clique no botão <strong>[!UICONTROL Generator]</strong>.</li> 
     <li value="3">Copie e cole a amostra XML no campo <strong>[!UICONTROL Sample data]</strong>.</li> 
     <li value="4">Clique em <strong>[!UICONTROL Save]</strong>.</li> 
     <li value="5">Verifique se a estrutura de dados foi gerada com êxito.</li> 
     <li value="6"> <p>Clique no botão <strong>[!UICONTROL Save]</strong> para salvar a estrutura de dados.</p> <p>É possível ignorar as etapas 2 a 5 para fornecer uma estrutura de dados vazia. Se a estrutura de dados estiver vazia, a saída do módulo não estará disponível no painel de mapeamento até que o módulo tenha sido executado pelo menos uma vez.</p> </li> 
    </ol> <p>Para obter mais informações, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Estruturas de dados</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve numbers as text]</td> 
   <td>Habilite essa opção para garantir que os números permaneçam como valores de texto (sequência de caracteres). Caso contrário, os números serão convertidos em valores numéricos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL XML]</p> </td> 
   <td> <p>Insira ou mapeie o texto XML formatado que deseja analisar.</p> <p>Se você usar uma fórmula, verifique se o tipo de valor do resultado é (ou pode ser automaticamente forçado a) o tipo de dados [!UICONTROL Text]. </p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/if-you-use-a-formula-350x164.png" style="width: 350;height: 164;"> </p> <p>Se o tipo de valor do resultado for [!UICONTROL Buffer] (dados binários) use a função <code>toString()</code> para convertê-lo no tipo de dados Text. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a> e <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipos de dados de item</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Exemplo:**

Para baixar um arquivo XML de um URL e analisar seu conteúdo:

1. Crie um novo cenário.
1. Adicionar o módulo [!UICONTROL HTTP] > [!UICONTROL Get a file]
1. Abra a configuração do módulo e configure-o da seguinte maneira:

   **URL**: URL do arquivo XML (por exemplo, `https://siftrss.com/f/rqLy05ayMBJ`)

   ![URL do exemplo de arquivo XML](/help/workfront-fusion/references/apps-and-modules/assets/url-of-xml-file-350x184.png)

1. Clique em **[!UICONTROL OK]** para salvar e fechar a configuração do módulo.
1. Adicione o módulo [!UICONTROL XML] > [!UICONTROL Parse XML], conecte-o após o módulo [!UICONTROL HTTP] > [!UICONTROL Get a file] e configure-o da seguinte maneira:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Data structure]</td> 
      <td> 
       <ol> 
        <li value="1">Clique no botão <strong>[!UICONTROL Add]</strong>.</li> 
        <li value="2">Clique no botão <strong>[!UICONTROL Generator]</strong>.</li> 
        <li value="3">No navegador da Web, abra uma nova guia ou janela.</li> 
        <li value="4">Coloque o URL usado na terceira etapa na barra de endereços e busque o arquivo XML.</li> 
        <li value="5">Selecione todo o texto XML e copie-o para a área de transferência.</li> 
        <li value="6">Feche a guia ou janela e retorne ao seu cenário.</li> 
        <li value="7">Cole o texto XML copiado no campo Dados de amostra.</li> 
        <li value="8">Clique em <strong>[!UICONTROL Save]</strong>.</li> 
        <li value="9">Verifique se a estrutura de dados foi gerada com êxito.</li> 
        <li value="10">Clique em <strong>[!UICONTROL Save]</strong> para salvar a estrutura de dados.</li> 
       </ol> <p>Você pode pular as etapas de 2 a 9 para fornecer uma estrutura de dados vazia. Se a estrutura de dados estiver vazia, a saída do módulo não estará disponível no painel de mapeamento até que o módulo tenha sido executado pelo menos uma vez.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL XML]</td> 
      <td> <p>Mapeie o <code>Data </code>item da saída do módulo [!UICONTROL HTTP] &gt; [!UICONTROL Get a file] para o campo. Use a função <code>toString()</code> para converter seu valor do tipo de dados [!UICONTROL Buffer] (dados binários) no tipo de dados [!UICONTROL Text].</p> <p>Você pode copiar e colar o código da fórmula no campo: <code>&#123;&#123;toString(1.data)&#125;&#125;</code></p> <p>Para obter mais informações sobre os tipos de dados Buffer e Text, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipos de dados de item</a>.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/paste-formula-code-350x99.png"> </p> </td> 
     </tr> 
    </tbody> 
   </table>

>[!ENDSHADEBOX]

### [!UICONTROL Parsing XML attributes]

Por padrão, o módulo [!UICONTROL XML] > [!UICONTROL Parse XML] coloca atributos em uma coleção especial `_attributes` como filho do nó que tem esses atributos. Se o nó for um nó de texto e tiver atributos, duas propriedades especiais serão adicionadas: `_attributes` para atributos e `_value` para o conteúdo de texto do nó.

>[!BEGINSHADEBOX]

**Exemplo:** Este XML:

```
<root attr="1">
<node attr="ABC">Hello, World</node>
</root>
```

é convertido neste pacote:

![XML convertido em pacote](/help/workfront-fusion/references/apps-and-modules/assets/xml-converted-to-bundle.png)

>[!ENDSHADEBOX]

## Solução de problemas: não é possível mapear dados do módulo [!UICONTROL Parse XML]

Verifique se a estrutura de dados está definida corretamente. Como alternativa, você pode usar uma estrutura de dados vazia e executar o módulo pelo menos uma vez para processar uma entrada XML.
