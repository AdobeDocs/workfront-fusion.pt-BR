---
title: Analisador de texto
description: Você pode usar a ferramenta Analisador de texto para analisar o texto para uso em outros módulos de cenário do Adobe Workfront Fusion. O analisador de Texto não requer uma conexão.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 885d714e-fc09-41a2-89dc-ebe29a355e43
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 0%

---

# [!UICONTROL Analisador de texto]

Você pode usar a [!UICONTROL Ferramenta de análise de texto] para analisar o texto a ser usado em outros módulos de cenário do Adobe Workfront Fusion. O [!UICONTROL analisador de texto] não requer uma conexão.

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
   <p>Nenhum requisito de licença do Workfront Fusion</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo menu:</p> <ul><li>Selecionar ou pacote do Prime Workfront: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Pacote do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Informações da API do analisador de texto

O conector do analisador de texto usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2</td> 
  </tr>
 </tbody> 
 </table>

## Módulos [!UICONTROL Analisador de texto] e seus campos

Ao configurar módulos do [!UICONTROL Analisador de texto], o Adobe Workfront Fusion exibe os campos listados abaixo. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Transformadores

* [[!UICONTROL Obter Elementos do HTML]](#get-elements-from-html)
* [[!UICONTROL Obter Elementos do texto]](#get-elements-from-text)
* [[!UICONTROL HTML para texto]](#html-to-text)
* [[!UICONTROL Corresponder Padrão]](#match-pattern)
* [[!UICONTROL Replace]](#replace)

#### [!UICONTROL Obter Elementos do HTML]

Recupera os elementos desejados do código HTML.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Continuar a execução da rota mesmo se o módulo não encontrar correspondências]</td> 
   <td> <p>Ative essa opção para garantir que o módulo não interrompa o cenário se não retornar resultados.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de elemento]</td> 
   <td> <p> Selecione o tipo de elemento que deseja recuperar do código HTML. </p> 
    <ul> 
     <li>[!UICONTROL Imagem]</li> 
     <li>[!UICONTROL Link]</li> 
     <li>[!UICONTROL elemento(s) iFrame]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Insira ou mapeie o código HTML do qual deseja recuperar os tipos de elemento especificados.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter Elementos do texto]

Analisa os elementos do texto com base no padrão fornecido.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Texto de entrada]</td> 
   <td> <p>Insira ou mapeie o texto que deseja analisar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Padrão]</td> 
   <td> <p>Selecione o padrão que reflete os elementos que você deseja analisar do texto.</p> <p>Para inserir expressões regulares personalizadas, selecione Personalizado na lista e, em seguida, insira a expressão personalizada no campo Regex personalizado.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ignorar Ocorrências Duplicadas]</td> 
   <td> <p>Marque essa caixa para ignorar ocorrências duplicadas de um elemento de texto.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL HTML para texto]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Insira o código HTML que deseja converter em texto sem formatação.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Quebra de linha] </td> 
   <td> <p>Selecione o tipo de nova linha (quebra de linha).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Cabeçalhos em maiúsculas]</p> </td> 
   <td> <p>Habilite esta opção para converter o texto delimitado nas marcas de cabeçalho (como &lt;h2&gt; &lt;/h2&gt;) em texto em maiúsculas.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Corresponder Padrão]

O módulo [!UICONTROL Padrão de correspondência] permite localizar e extrair elementos de cadeia de caracteres correspondentes a um padrão de pesquisa de um determinado texto. Esse módulo usa expressões regulares (também conhecidas como regex ou regexp).

Uma expressão regular é uma sequência de caracteres na qual cada caractere é um metacaractere, com um significado especial, ou um caractere regular que tem um significado literal. Esses caracteres e metacaracteres identificam um padrão que pode ser usado para pesquisar texto. Por exemplo, se você deseja pesquisar nomes, é possível configurar uma expressão regular para pesquisar um padrão que consiste em duas palavras consecutivas que começam com letras maiúsculas. As expressões regulares são uma ferramenta poderosa para pesquisar e manipular texto.

Uma discussão de expressões regulares está fora do escopo deste artigo. Recomendamos os seguintes recursos:

* Para obter a lista completa de metacaracteres, consulte [Expressões regulares](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) em documentos da Web do MDN.
* Para um tutorial sobre como criar expressões regulares, recomendamos [RegexOne](https://regexone.com/).
* Para experimentar expressões regulares, recomendamos o site [Expressões regulares 101](https://regex101.com/). Selecione a VARIÁVEL ECMAScript (JavaScript) no painel esquerdo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Padrão] </td> 
   <td> <p>Insira o padrão de expressão regular. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemplo: </b></span></span> <code>[+-]?(\d+(\.\d+)?|\.\d+)([eE][+-]?\d+)?</code> extrai todos os numerais no texto fornecido.</p> <p>Observação:  <p>O padrão deve conter pelo menos um grupo de captura entre parênteses <code>()</code>. Se o padrão não contiver nenhum grupo de captura, o pacote de saída estará vazio.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Correspondência global]</td> 
   <td> <p>Habilite esta opção para recuperar todas as correspondências no texto. Cada correspondência é gerada em um pacote separado. Se essa opção estiver desativada, o módulo recuperará somente a primeira entrada.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Diferencia maiúsculas de minúsculas]</td> 
   <td> <p> Habilite esta opção para que este módulo trate o texto como sensível a maiúsculas e minúsculas.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Várias Linhas] </td> 
   <td> <p>Habilite esta opção para garantir que os metacaracteres de início e término (<code>^</code> e <code>$</code>) correspondam ao início ou ao fim de cada linha, não apenas ao início ou ao fim de toda a cadeia de caracteres de entrada.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Linha Simples]</td> 
   <td>Habilite esta opção para garantir que o ponto (.) corresponda aos caracteres de nova linha (<code>\n</code>).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continuar a execução da rota mesmo se o módulo não retornar resultados]</td> 
   <td> <p>Ative essa opção para garantir que o módulo não interrompa o cenário se não retornar resultados.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Texto] </td> 
   <td> <p>Insira ou mapeie o texto que deseja corresponder ao padrão.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Replace]

Pesquisa no texto inserido um valor especificado ou uma expressão regular e substitui o resultado pelo novo valor.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Padrão] </td> 
   <td> <p>Insira o termo de pesquisa. Você também pode usar uma expressão regular. Para obter mais detalhes sobre a expressão regular, consulte o módulo <a href="#match-pattern" class="MCXref xref">[!UICONTROL Padrão de Correspondência]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Novo valor]</td> 
   <td> <p> Insira o valor que você deseja substituir o termo de pesquisa.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Correspondência global]</td> 
   <td> <p>Habilite esta opção para recuperar todas as correspondências no texto. Cada correspondência é gerada em um pacote separado. Se essa opção estiver desativada, o módulo recuperará somente a primeira entrada.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Diferencia maiúsculas de minúsculas]</td> 
   <td> <p> Habilite esta opção para que este módulo trate o texto como sensível a maiúsculas e minúsculas.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Várias Linhas] </td> 
   <td> <p>Habilite esta opção para garantir que os metacaracteres de início e término (<code>^</code> e <code>$</code>) correspondam ao início ou ao fim de cada linha, não apenas ao início ou ao fim de toda a cadeia de caracteres de entrada.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Linha Simples]</td> 
   <td>Habilite esta opção para garantir que o ponto (.) corresponda aos caracteres de nova linha (<code>\n</code>).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Texto] </td> 
   <td> <p>Insira o texto a ser pesquisado.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Rascunho de dados

O raspamento de dados, às vezes chamado de raspagem da Web, extração de dados ou coleta da Web, é o processo de coletar dados de sites e armazená-los no banco de dados ou planilhas locais. Se quiser extrair dados de um site e não estiver familiarizado com expressões regulares, você poderá usar uma ferramenta de raspagem de dados.

Se a ferramenta de raspagem de dados fornecer uma REST API, você poderá se conectar a ela por meio de nossos módulos universais [[!UICONTROL HTTP]](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors) e [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

## Solução de problemas do analisador de texto

Use essas informações se você não conseguir que um analisador de texto produza nenhuma saída.

>[!BEGINSHADEBOX]

Exemplo:

O módulo deve analisar o tipo de arquivo de um documento de arquivo &quot;filename.docx&quot;, e a extensão do nome do arquivo varia de DOCX para PDF para CSV.

A expressão que você pode escolher usar neste caso é [!DNL \..+]

Normalmente, essa expressão regular resultaria em uma correspondência completa.

No entanto, a implementação dessa expressão no analisador de texto não resulta em uma correspondência:

![Sem correspondência](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-you-dont-get-a-match-350x365.png)

O motivo para isso é que o &quot;i&quot; mostra apenas o número de correspondências por correspondência, portanto, neste caso, temos 2 correspondências, portanto, depois do &quot;i&quot;, há um valor numérico 1 e 2. O caso de uso para isso é que, se você precisar corresponder ou transmitir dados por um filtro somente o segundo valor correspondente, poderá especificar qual valor é representado pelo valor numérico.

![Correspondência](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-matches-350x355.png)

Para obter os valores de correspondência necessários para adicionar colchetes à parte que deseja analisar (por exemplo, para extrair somente de &quot;filename.docx&quot; - &quot;docx&quot;), de acordo com a expressão regex que estamos usando para esse cenário de caso, os colchetes devem ser aplicados em \.(.+)

Isso captura o DOCX, coloca-o em um grupo e deixa o &quot;.&quot; fora dele.

![Obter correspondências](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-get-matches-350x592.png)

Na saída mostrada na figura abaixo, o grupo de captura corresponderá a qualquer caractere (exceto para terminadores de linha).

![Saída](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-output-350x389.png)

Outra solução alternativa que também incorpora o regex é usar a função de substituição

`{{replace("abcdefghijklmno pqr stuvw xyz.docx"; "/.\./"; ".")}}`

Em seguida, substitua `abcdefghijklmno pqr stuvw xyz.docx` pela variável de nome de arquivo real.

>[!ENDSHADEBOX]
