---
title: Módulos do Adobe Content Tagger
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o Adobe Content Tagger, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: 801e8cb1a4c807aaa4275382c2d6211cf3cd6d1f
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 20%

---

# Módulos do Adobe Content Tagger

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o Adobe Content Tagger, bem como conectá-lo a vários aplicativos e serviços de terceiros.

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: disponível para organizações com licenças baseadas em operação</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Criar uma conexão com o Adobe Content Tagger

Para criar uma conexão para os módulos do Adobe Content Tagger:

1. Em qualquer módulo, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Nome da conexão</td>
        <td>
          <p>Insira um nome para essa conexão.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Ambiente</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">Tipo</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
        <td role="rowheader">ID do cliente</td>
        <td>Insira a ID do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Segredo do cliente</td>
        <td>Insira o segredo do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.


## Módulos do Adobe Content Tagger e seus campos

Ao configurar os módulos do Adobe Content Tagger, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Marcador de conteúdo do Adobe podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Ações

* [Cores da marca](#tag-colors)
* [Palavras-chave de tag](#tag-keywords)
* [Adicionar marcas de formatação ao texto em uma imagem](#tag-text-in-an-image)

#### Cores da marca

Este módulo retorna a porcentagem de uma imagem coberta por cores de pixel diferentes, classificadas em 40 categorias de cores.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Content Tagger, consulte <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Criar uma conexão com o Adobe Content Tagger</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do arquivo de imagem</td> 
   <td>Insira ou mapeie o nome de arquivo da imagem para a qual você deseja marcar as cores.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dados da imagem</td> 
   <td>Insira ou mapeie os dados do arquivo da imagem para a qual deseja marcar as cores.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Formato da imagem</td> 
    <td>Selecione o tipo da imagem para a qual você deseja marcar cores.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número de cores</td> 
    <td>Insira ou mapeie o número de cores para retornar. Para retornar todos os resultados, digite 0.</p></td> 
  </tr> 
 <tr> 
   <td role="rowheader">Cobertura mínima</td> 
   <td>Insira ou mapeie a cobertura mínima para a qual você deseja marcar as cores. Serão retornadas somente as cores que cubram pelo menos essa quantidade da imagem. Um valor de 1 representa 100% da imagem e um valor de 0,5 representa 50% da imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Redimensionar imagem antes da extração.</td> 
   <td>Selecione Sim para redimensionar a imagem para 320x320 antes de extrair as cores. Selecione Não para extrair cores da imagem em tamanho real.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ativar máscara de primeiro plano/segundo plano</td> 
   <td>Selecione Sim se desejar relatar as cores separadamente para a imagem geral, o primeiro plano e o plano de fundo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recuperar tons</td> 
   <td>Selecione Sim se quiser recuperar dados sobre tons quentes, neutros e frios, além de cores.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de cores retornadas</td> 
   <td>Insira ou mapeie o número máximo de cores que o módulo com retorno para um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>



#### Palavras-chave de tag

Este módulo extrai palavras-chave ou frases-chave que descrevem melhor o assunto do documento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Content Tagger, consulte <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Criar uma conexão com o Adobe Content Tagger</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do arquivo de documento</td> 
   <td>Insira ou mapeie o nome de arquivo do documento do qual deseja extrair palavras-chave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dados da imagem</td> 
   <td>Insira ou mapeie os dados do arquivo do documento do qual você deseja extrair as palavras-chave.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Formato da imagem</td> 
    <td>Selecione o formato do documento do qual você deseja extrair palavras-chave.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do aplicativo</td> 
   <td>Insira ou mapeie a ID do aplicativo para o documento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número de frases-chave</td> 
   <td>Insira ou mapeie o número de frases-chave que você deseja que o módulo retorne. Para retornar todos os resultados, digite 0.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Relevância mínima</td> 
   <td>Insira ou mapeie o limite de pontuação abaixo do qual os resultados não serão retornados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Comprimento mínimo da frase-chave (palavras)</td> 
   <td>Insira ou mapeie o número mínimo de palavras necessárias em frases-chave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tamanho máximo da frase-chave (palavras)</td> 
   <td>Insira ou mapeie o número máximo de palavras necessárias em frases-chave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profundidade da unidade semântica</td> 
   <td>Selecione a profundidade desejada para as respostas hierárquicas.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipos de entidade</td> 
   <td>Para cada tipo de entidade ao qual você deseja restringir frases-chave, clique em <b>Adicionar item</b> e insira as informações para o tipo de entidade.</td> 
  </tr> 
 </tbody> 
</table>

#### Adicionar marcas de formatação ao texto em uma imagem

Este módulo indica se o texto está presente em uma imagem e retorna o texto se presente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Content Tagger, consulte <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Criar uma conexão com o Adobe Content Tagger</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do arquivo de imagem</td> 
   <td>Insira ou mapeie o nome de arquivo do documento do qual deseja extrair o texto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dados da imagem</td> 
   <td>Insira ou mapeie os dados do arquivo do documento do qual deseja extrair o texto.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Formato da imagem</td> 
    <td>Selecione o formato do documento do qual deseja extrair o texto.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtrar com dicionário</td> 
   <td>Selecione se deseja retornar somente palavras que estejam no dicionário de inglês.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Probabilidade mínima</td> 
   <td>Insira ou mapeie a probabilidade mínima, em que o módulo retornará apenas palavras reconhecidas com pelo menos essa probabilidade. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Relevância mínima</td> 
   <td>Insira a porcentagem mínima da imagem que o texto retornado deve cobrir. A relevância é calculada como a fração da área da caixa delimitadora do texto extraído em comparação com a imagem completa. 0,01 seria traduzido como um texto que ocupa pelo menos 1% da imagem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de resultados que o módulo retornará para um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>
