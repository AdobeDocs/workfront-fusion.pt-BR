---
title: Módulos do Adobe Express
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Adobe Express.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: eab04db9a38020ed973f98d7f8f290ccd183251c
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 17%

---

# Módulos do Adobe Express

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Adobe Express, bem como conectá-lo a vários aplicativos e serviços de terceiros.

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
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
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

## Pré-requisitos

Antes de usar o conector do Adobe Express, você deve garantir que os seguintes pré-requisitos sejam atendidos:

* Você deve ter uma conta ativa do Adobe Express.

## Criar uma conexão com o Adobe Express

Para criar uma conexão para os módulos do Adobe Express:

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


## Módulos do Adobe Express e seus campos

Ao configurar módulos do Adobe Express, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Adobe Express podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Ações

#### Exportar uma representação

Esse módulo exporta um documento para o formato JPG ou PNG. Ele pode fornecer URLs pré-assinados para as representações de página, que são válidos por quatro horas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Express, consulte <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Criar uma conexão com o Adobe Express</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Documento</td> 
   <td>Selecione o documento para o qual deseja exportar uma representação.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Números de página</td> 
   <td>Insira ou mapeie os números de página que deseja incluir na representação. Uma string separada por vírgulas com números de página para a qual a solicitação de representação é feita. Por exemplo, "1,2,3". Intervalos de páginas também podem ser especificados. Por exemplo, "1-3" inclui as páginas 1, 2 e 3. Outro exemplo é "1,3-5", que inclui as páginas 1, 3, 4 e 5. "1-" pode ser usado para especificar todas as páginas, enquanto "5-" indica a página 5 até a última página. Se não for fornecida, a primeira página será considerada por padrão. Os números de página começam em 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo de representação</td> 
   <td>Selecione o tipo de representação que deseja exportar: imagem, vídeo ou PDF</td> 
  </tr>
  <tr> 
   <td role="rowheader">Formato</td> 
   <td>Selecione o formato de arquivo para sua representação.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo de PDF</td> 
   <td>Se estiver exportando um PDF, selecione se deseja exportar um PDF padrão ou impresso.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tamanho</td> 
   <td>Se estiver exportando uma imagem ou vídeo, insira ou mapeie o tamanho, em pixels, do lado mais longo. A taxa de proporção é mantida. Para imagens, o tamanho mínimo suportado é 1px e o tamanho máximo suportado é 8192px. Se não for fornecido, o tamanho padrão da página será considerado.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Baixar arquivos PDF individuais</td> 
   <td>Se estiver exportando uma PDF, selecione se o download das páginas será feito como arquivos PDF separados. Quando verdadeiro, cada página é baixada como seu próprio arquivo PDF. Quando falso, todas as páginas são combinadas em um único arquivo do PDF.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Configuração</td> 
   <td>Se estiver exportando uma PDF, selecione se deseja a PDF na configuração padrão ou de impressão.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Estágio de acessibilidade</td> 
   <td>Se estiver exportando um PDF padrão, selecione se deseja incluir tags de acessibilidade no PDF.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sangria</td> 
   <td>Se estiver exportando um PDF de impressão, selecione se deseja incluir configurações de sangria na exportação</td> 
  </tr>
  <tr> 
   <td role="rowheader">Configurações de sangria &gt; Quantidade</td> 
   <td>Insira a quantidade da margem de sangria.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Configurações de sangria &gt; Unidades</td> 
   <td>Selecione se a quantidade se refere a polegadas ou milímetros.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Cortar</td> 
   <td>Se estiver exportando um PDF de impressão, selecione se deseja incluir configurações de corte na exportação</td> 
  </tr>
  <tr> 
   <td role="rowheader">Configurações de corte &gt; Quantidade</td> 
   <td>Insira a quantidade da margem de corte.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Configurações de corte &gt; Unidades</td> 
   <td>Selecione se a quantidade se refere a polegadas ou milímetros.</td> 
  </tr>
 </tbody> 
</table>

#### Gerar variações

Este módulo cria uma variação de documento com base nos parâmetros de entrada fornecidos. Após o processamento, ele armazena temporariamente o documento gerado e o disponibiliza para o usuário em uma pasta designada. O documento permanece acessível por 30 dias, após os quais o sistema o remove automaticamente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Express, consulte <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Criar uma conexão com o Adobe Express</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Documento</td> 
   <td>Selecione o documento para o qual deseja gerar variações.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Números de página</td> 
   <td>Insira ou mapeie os números de página que deseja incluir na representação. Uma string separada por vírgulas com números de página para a qual a solicitação de variação é feita. Por exemplo, "1,2,3". Intervalos de páginas também podem ser especificados. Por exemplo, "1-3" inclui as páginas 1, 2 e 3. Outro exemplo é "1,3-5", que inclui as páginas 1, 3, 4 e 5. "1-" pode ser usado para especificar todas as páginas, enquanto "5-" indica a página 5 até a última página. Se não for fornecida, a primeira página será considerada por padrão. Os números de página começam em 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Nome do documento preferencial.</td> 
   <td>Insira ou mapeie um nome para o novo documento. Se você não fornecer um nome ou o nome já estiver em uso, o sistema gerará um nome exclusivo.</td> 
  </tr>
  <tr> 
   <td role="rowheader">ID do projeto</td> 
   <td>Insira a ID do projeto onde as variações serão armazenadas.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Outros campos</td> 
   <td>Insira valores para outros campos. Os campos disponíveis se baseiam no documento selecionado.</td> 
  </tr>
 </tbody> 
</table>


### Pesquisas

#### Recuperar documentos marcados

Esse módulo recupera uma lista de documentos marcados, juntamente com metadados relevantes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Express, consulte <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Criar uma conexão com o Adobe Express</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Índice inicial</td> 
   <td>Insira ou mapeie o índice de início da paginação. Use isso quando tiver recuperado outra lista de resultados e quiser continuar essa lista. O índice padrão é 0.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de resultados que você deseja que o módulo retorne para cada ciclo de execução.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Ordenar por</td> 
   <td>Selecione o atributo pelo qual deseja classificar os resultados.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Direção</td> 
   <td>Selecione se deseja classificar os resultados em ordem crescente ou decrescente.</td> 
  </tr>
 </tbody> 
</table>

#### Recuperar detalhes do documento

Esse módulo recupera detalhes das páginas e dos elementos marcados em um documento especificado. Ele retorna uma lista paginada das páginas do documento e os metadados sobre cada página. Se o documento tiver elementos marcados, a API incluirá seus respectivos detalhes, como tamanho e posição. Se o documento não tiver elementos com tags, ele retornará uma matriz vazia. A resposta inclui informações de paginação para ajudar os usuários a navegar pelas páginas do documento. Um máximo de 10 páginas pode ser retornado em 1 ciclo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Express, consulte <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Criar uma conexão com o Adobe Express</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Documento</td> 
   <td>Selecione o documento para o qual você deseja retornar páginas e detalhes.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Página inicial</td> 
   <td>Insira ou mapeie o número da primeira página da qual os detalhes serão recuperados.</td>

#### Recuperar o status de um trabalho

Este módulo recupera o status de um job pela ID do job. Dependendo do tipo de job, a resposta poderá incluir detalhes específicos do job.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Express, consulte <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Criar uma conexão com o Adobe Express</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do trabalho</td> 
   <td>Informe ou mapeie a ID do job para o qual deseja recuperar detalhes.</td> 
  </tr>

