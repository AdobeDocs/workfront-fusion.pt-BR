---
title: Módulos do CloudConvert
description: Módulos do CloudConvert
author: Becky
feature: Workfront Fusion
exl-id: 52c4d18a-8bee-44d6-9a2c-cc9e157e1dde
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '3161'
ht-degree: 0%

---

# [!DNL CloudConvert] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o CloudConvert, bem como conectá-lo a vários aplicativos e serviços de terceiros. Os módulos do [!DNL CloudConvert] permitem monitorar e gerenciar trabalhos, tarefas e importar e exportar arquivos na sua conta do [!DNL CloudConvert].

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
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (herdado): automação e integração do Workfront Fusion for Work </p>
   </td> 
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

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Informações da API CloudConvert

O conector CloudConvert usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td> https://api.cloudconvert.com/v2/</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2.14.22</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL CloudConvert] ao Workfront Fusion {#connect-cloudconvert-to-workfront-fusion}

Para conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, você precisa obter a Chave de API da sua conta do [!DNL CloudConvert].

1. Faça logon em sua conta do [!DNL CloudConvert] e abra seu [!UICONTROL Painel].
1. Abra a seção **[!UICONTROL Autorização] > [!UICONTROL Chaves de API]**.
1. Clique em **[!UICONTROL Criar nova chave de API]**.
1. Insira o nome da chave de API, habilite os escopos que deseja usar e clique em **[!UICONTROL Criar]**.
1. Copie o token fornecido e armazene-o em um local seguro.
1. No Workfront Fusion, comece criando um cenário e abra a caixa de diálogo [!DNL CloudConvert]Criar uma conexão **[!UICONTROL do módulo]**.

   Para obter instruções, consulte [Criar um cenário no Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

1. Insira o token salvo na etapa 5 e clique em **[!UICONTROL Continuar]** para estabelecer a conexão.

## [!DNL CloudConvert] módulos e seus campos {#cloudconvert-modules-and-their-fields}

Ao configurar módulos do [!DNL CloudConvert], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL CloudConvert] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Tarefas comuns](#common-tasks)
* [Trabalhos](#jobs)
* [Tarefas](#tasks)
* [Outras](#other)

### Tarefas comuns

* [Capturar um site](#capture-a-website)
* [[!UICONTROL Converter um arquivo]](#convert-a-file)
* [Criar um Arquivo Morto](#create-an-archive)
* [Mesclar arquivos](#merge-files)
* [Otimizar um arquivo](#optimize-a-file)

#### [!UICONTROL Capturar um site]

Este módulo de ação captura um site especificado e o salva no formato PDF, JPG ou PNG.

Especifique o URL do site e outras informações, como onde deseja armazenar as informações.

O módulo retorna a ID do arquivo e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira o URL do site que você deseja capturar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de Saída] </td> 
   <td>Selecione se deseja salvar o site capturado no formato PNG, JPG ou PDF. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Arquivo] </td> 
   <td>Insira um nome de arquivo (incluindo a extensão) para o arquivo de saída de destino.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos] </td> 
   <td> <p>(Opcional) Defina os cabeçalhos de solicitação. </p> <p>Isso é útil, por exemplo, quando o URL especificado requer autorização. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Opções específicas de conversão e mecanismo] </p> </td> 
   <td>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Baixar um arquivo] </td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Converter um arquivo]

Converte um arquivo em um formato de saída selecionado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivo de entrada]</td> 
   <td>Selecione se deseja fazer upload de um arquivo usando o Workfront Fusion ou forneça o URL do qual o arquivo será carregado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carregar um arquivo]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importar um Arquivo da URL]</td> 
   <td> 
    <ul> 
     <li> <p><strong></strong> </p> <p>Insira o URL do arquivo que você deseja converter.</p> </li> 
     <li> <p><strong>[!UICONTROL Cabeçalhos]</strong></p> <p>Definir cabeçalhos de solicitação (opcional). Isso é útil, por exemplo, quando o URL especificado requer a autorização.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formatar]</td> 
   <td>Selecione se deseja especificar o formato de entrada do arquivo que deseja converter. Se não especificado, a extensão do arquivo de entrada é usada como o formato de entrada.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Input Format]</td> 
   <td>Selecione o formato atual do arquivo.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Formato de Saída]</td> 
   <td>Selecione o formato de arquivo de destino para o qual deseja converter o arquivo.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Nome do Arquivo]</td> 
   <td>Escolha um nome de arquivo (incluindo a extensão) para o arquivo de saída de destino.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Opções específicas de conversão e mecanismo] </p> </td> 
   <td>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Baixar um arquivo] </td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar um Arquivo Morto]

Permite adicionar um ou vários arquivos ao arquivo ZIP, RAR, 7Z, TAR, TAR.GZ ou TAR.BZ2.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Arquivos de Entrada]</p> </td> 
   <td> <p>Especifique os arquivos que deseja adicionar ao arquivo morto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carregar um Arquivo]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Importar um arquivo da URL]</p> </td> 
   <td> <p><strong></strong> </p> <p>Insira o URL do arquivo que deseja arquivar.</p> <p><strong>[!UICONTROL Cabeçalhos]</strong> </p> <p>Definir cabeçalhos de solicitação (opcional). Isso é útil, por exemplo, quando o URL especificado requer a autorização.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de Saída]</td> 
   <td> <p> Selecione o formato de destino do arquivo arquivado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do arquivo]</td> 
   <td> <p> Insira o nome do arquivo (incluindo a extensão) para o arquivo de saída de destino.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Opções específicas de conversão e mecanismo] </td> 
   <td> <p>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Baixar um Arquivo]</td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mesclar arquivos]

Mescla pelo menos dois arquivos em uma PDF. Se os arquivos de entrada não forem PDFs, serão convertidos automaticamente para o PDF.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Arquivos de Entrada]</p> </td> 
   <td> <p>Especifique os arquivos que deseja mesclar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carregar um Arquivo]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Importar um arquivo da URL]</p> </td> 
   <td> <p><strong></strong> </p> <p>Insira o URL do arquivo que deseja arquivar.</p> <p><strong>[!UICONTROL Cabeçalhos]</strong> </p> <p>Definir cabeçalhos de solicitação (opcional). Isso é útil, por exemplo, quando o URL especificado requer a autorização.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de Saída]</td> 
   <td> <p> Selecione o formato de destino do arquivo mesclado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do arquivo]</td> 
   <td> <p> Insira o nome do arquivo (incluindo a extensão) para o arquivo de saída de destino.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Opções específicas de conversão e mecanismo] </td> 
   <td> <p>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Baixar um Arquivo]</td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Otimizar um Arquivo]

Esse módulo de ação otimiza e compacta um arquivo no formato PDF, PNG ou JPG.

Especifique o arquivo e os parâmetros para otimizá-lo e armazená-lo.

O módulo retorna a ID do arquivo e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivo de Entrada]</td> 
   <td>Selecione se deseja fazer upload de um arquivo usando o Workfront Fusion ou forneça o URL do qual o arquivo será carregado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Carregar um Arquivo]</p> </td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importar um arquivo da URL] </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: Insira a URL do arquivo que você deseja converter.</li> 
     <li><strong>[!UICONTROL Cabeçalhos]</strong>: (Opcional) Define cabeçalhos de solicitação. Isso é útil, por exemplo, quando o URL especificado requer autorização.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Otimização para] </td> 
   <td> <p>Selecione o perfil de otimização para as necessidades do público-alvo específicas.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Web]</strong>: Otimização para a Web (Padrão)</p> 
      <ul> 
       <li>Remover dados redundantes e desnecessários para a Web</li> 
       <li>Diminua a resolução, corte e compacte imagens de forma inteligente</li> 
       <li>Mesclar e subdefinir fontes</li> 
       <li>Conversão de cores em RGB</li> 
      </ul> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Imprimir]</strong>: Otimização para impressão</p> 
      <ul> 
       <li> <p>Remova dados redundantes e desnecessários para impressão</p> </li> 
       <li> <p>Diminua a resolução, corte e compacte imagens de forma inteligente</p> </li> 
       <li> <p>Mesclar e subdefinir fontes</p> </li> 
       <li> <p>Converter cores em CMYK</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Arquivo Morto]</strong>: Otimização para fins de arquivamento</p> 
      <ul> 
       <li> <p>Remova dados redundantes e desnecessários para arquivamento</p> </li> 
       <li> <p>Compactar imagens de forma inteligente</p> </li> 
       <li> <p>Mesclar e subdefinir fontes</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Imagens digitalizadas]</strong>: Otimização de imagens digitalizadas</p> 
      <ul> 
       <li> <p>Perfil otimizado para PDFs que consistem principalmente em imagens rasterizadas</p> </li> 
       <li> <p>Compactar as imagens sem reduzir significativamente a qualidade visual</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL redução de tamanho máximo]</strong>: Otimização para redução de tamanho máximo</p> 
      <ul> 
       <li> <p>Usar a compactação máxima possível</p> </li> 
       <li> <p>Pode reduzir a qualidade visual</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de entrada] </td> 
   <td>Selecione o formato do arquivo de entrada que deseja otimizar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do arquivo]</td> 
   <td> <p>Insira um nome de arquivo (incluindo a extensão) para o arquivo de saída de destino.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Opções específicas de conversão e mecanismo]</td> 
   <td> <p>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Baixar um arquivo]</td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Trabalhos

* [[!UICONTROL Criar um Trabalho (avançado)]](#create-a-job-advanced)
* [[!UICONTROL Novo Evento de Trabalho]](#new-job-event)
* [[!UICONTROL Listar Trabalhos]](#list-jobs)
* [[!UICONTROL Obter um Trabalho]](#get-a-job)
* [[!UICONTROL Excluir um Trabalho]](#delete-a-job)

#### [!UICONTROL Criar um Trabalho (avançado)]

Este módulo cria uma tarefa. Um trabalho pode ser uma ou várias tarefas identificadas no campo [!UICONTROL Nome] e vinculadas entre si usando o campo [!UICONTROL Entrada].

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivos de Entrada]</td> 
   <td> <p>Selecione se deseja fazer upload de um arquivo usando o Workfront Fusion ou forneça o URL do qual o arquivo será carregado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carregar um Arquivo]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Importar um Arquivo da URL]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: Digite a URL do arquivo que você deseja processar.</li> 
     <li><strong>[!UICONTROL Cabeçalhos]</strong>: (Opcional) Define cabeçalhos de solicitação. Isso é útil, por exemplo, quando o URL especificado requer autorização.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tarefas]</p> </td> 
   <td> <p>Adicione tarefas que serão executadas dentro do trabalho.</p> <p>Encontre as descrições dos campos de operações na seção correspondente.</p> 
    <ul> 
     <li><a href="#convert-a-file" class="MCXref xref">[!UICONTROL Converter arquivo]</a> </li> 
     <li><a href="#capture-a-website" class="MCXref xref">[!UICONTROL Capturar um Site]e</a> </li> 
     <li><a href="#optimize-a-file" class="MCXref xref">[!UICONTROL Otimizar Arquivo]</a> </li> 
     <li><a href="#create-an-archive" class="MCXref xref">[!UICONTROL Criar um Arquivo]</a> </li> 
     <li><a href="#merge-files" class="MCXref xref">[!UICONTROL Mesclar Arquivos]</a> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Executar um Comando]</strong> </p> <p>Para obter mais informações sobre como executar um comando, consulte a <a href="https://cloudconvert.com/api/v2/command#command-tasks">[!DNL CloudConvert] documentação da API</a>.</p> </li> 
     <li> <p><strong>[!UICONTROL Exportar um Arquivo para URL Temporária]</strong> </p> <p> Especifique o nome da tarefa e o nome da tarefa de entrada (por exemplo, Conversão).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Marca] </td> 
   <td> <p>Insira uma tag. Tags são strings arbitrárias para identificar o trabalho. Elas não têm efeito e podem ser usadas para associar o trabalho a uma ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um Trabalho]

Este módulo exclui um trabalho, incluindo todas as tarefas e dados.

>[!NOTE]
>
>As tarefas são excluídas automaticamente 24 horas após terem terminado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Trabalho]</td> 
   <td> <p>Informe ou mapeie a ID do job que deseja deletar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um Trabalho]

Este módulo recupera detalhes do job.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Trabalho]</td> 
   <td> <p>Informe ou mapeie a ID do job sobre o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar Trabalhos]

Este módulo recupera todas as tarefas que foram executadas em sua conta.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Selecione o status do trabalho pelo qual filtrar os trabalhos retornados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Defina o número de trabalhos que o Workfront Fusion 2.0 retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Novo Evento de Trabalho]

Acionado quando um trabalho em sua conta ou tarefa é criado, concluído ou falha.

>[!NOTE]
>
>* O trabalho criado pelo módulo [!UICONTROL Criar um Trabalho (avançado)] consiste em *várias* tarefas.
>* O gatilho [!UICONTROL Novo Evento de Trabalho] também é acionado quando uma tarefa *individual* é criada, é concluída ou falha.
>

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do Webhook]</td> 
   <td>Insira o nome do webhook. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato de Saída] </td> 
   <td>Selecione se deseja salvar o site capturado no formato PNG, JPG ou PDF. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evento]</td> 
   <td>Selecione se o módulo será acionado quando a tarefa ou o trabalho for criado, concluído ou falhar.</td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Se estiver trabalhando com o Agregador de Matrizes (por exemplo, você tem muitos arquivos em diferentes formatos para converter), use a opção **[!UICONTROL Desconheço o formato de entrada]** na caixa de diálogo [!UICONTROL Adicionar uma tarefa]. Caso contrário, o erro será retornado.
>* Vincular tarefas no trabalho (nome > entrada, nome > entrada,...):
>
>  ![Vinculando nome entre trabalhos](/help/workfront-fusion/references/apps-and-modules/assets/linking-name-across-jobs-350x808.png)>

### Tarefas

* [[!UICONTROL Obter uma tarefa]](#get-a-task)
* [[!UICONTROL Baixar um Arquivo]](#download-a-file)
* [[!UICONTROL Listar Tarefas]](#list-tasks)
* [[!UICONTROL Repetir uma tarefa]](#retry-a-task)
* [[!UICONTROL Cancelar uma tarefa]](#cancel-a-task)
* [[!UICONTROL Excluir uma tarefa]](#delete-a-task)

#### [!UICONTROL Cancelar uma tarefa]

Este módulo cancela uma tarefa que tem um status de espera ou processamento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Tarefa]</td> 
   <td> <p> Insira ou mapeie a ID da tarefa que deseja cancelar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma tarefa]

Excluir uma tarefa, incluindo todos os dados.

>[!NOTE]
>
>As tarefas são excluídas automaticamente 24 horas após terem terminado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Tarefa]</td> 
   <td> <p> Insira (mapeie) a ID da tarefa que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Baixar um Arquivo]

Este módulo recupera o nome do arquivo e os dados do arquivo da tarefa especificada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Tarefa]</td> 
   <td> <p> Insira ou mapeie a ID da tarefa da qual deseja baixar o arquivo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma tarefa]

Este módulo recupera detalhes da tarefa.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Tarefa]</td> 
   <td> <p>Insira ou mapeie a ID da tarefa sobre a qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar Tarefas]

Este módulo recupera todas as tarefas em sua conta com base nas configurações de filtro.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Selecione o status da tarefa pelo qual filtrar as tarefas retornadas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Trabalho] </td> 
   <td> <p>Insira ou mapeie a ID do trabalho para retornar somente tarefas dentro do trabalho especificado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operação] </td> 
   <td> <p>Informe o tipo de operação para retornar somente tarefas com a operação especificada. </p> <p>Observação: use o módulo [!UICONTROL Listar Operações Possíveis] para recuperar operações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Repetir uma tarefa]

Este módulo cria uma nova tarefa, baseada nas configurações (carga útil) de outra tarefa.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Tarefa]</td> 
   <td> <p> Digite ou mapeie a ID da tarefa da qual deseja criar uma nova tarefa.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outras

* [[!UICONTROL Obter Minhas Informações]](#get-my-info)
* [[!UICONTROL Fazer uma chamada de API]](#make-an-api-call)

#### [!UICONTROL Obter Minhas Informações]

Recupera detalhes da conta autenticada sobre o usuário atual.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao Workfront Fusion, consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fazer uma chamada de API]

Permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do CloudConvert ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Insira um caminho relativo para <code>https://api.cloudconvert.com/</code>. Por exemplo: <code>/v2/tasks</code></p> <p>Para obter a lista de pontos de extremidade disponíveis, consulte a <a href="https://cloudconvert.com/api/v2">[!DNL CloudConvert] Documentação da API v2</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion 2.0 adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão. Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo:** Tarefas de Lista

A chamada de API a seguir retorna todas as tarefas da conta do CloudFront:

URL: `/v2/tasks`

Método: `GET`

![Exemplo de entrada da API](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-input.png)

Correspondências da pesquisa podem ser encontradas na Saída do módulo em [!UICONTROL Pacote] > [!UICONTROL Corpo] > [!UICONTROL dados].

No nosso exemplo, 6 tarefas foram retornadas:

![Saída de exemplo de API](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-output.png)

## Solução de problemas {#troubleshooting}

Consulte a tabela a seguir para ver possíveis erros e suas soluções:

<table style="table-layout:auto">
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> <p>Erro</p> </th> 
   <th>Próximas etapas</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL O tamanho do arquivo de saída excede o limite permitido para o seu cenário.]</span> </p> </td> 
   <td> <p>Consulte os limites de tamanho de arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Você excedeu o tempo máximo de conversão.]</span> </p> </td> 
   <td> <p>O plano [!DNL CloudConvert] gratuito oferece 25 minutos de conversão diariamente. Se o seu uso exceder o limite do plano gratuito, você poderá alternar para um pacote (pré-pago) ou assinatura.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Falha ao ler o tamanho do quadro: Não foi possível buscar em 1508. �/output/JLIADSA00137P0.mp3: argumento inválido.]</span> </p> </td> 
   <td> <p>Esse erro é lançado, por exemplo, ao converter arquivos de MP3 para WAV. Verifique se você selecionou a região correta porque ela encontrará referências a arquivos, mas não apenas ao arquivo correto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL RuntimeError:] </p> <p><span style="font-weight: normal;">[!UICONTROL Número máximo de repetições excedido.]</span> </p> </td> 
   <td> <p>Localize o trabalho [!DNL CloudConvert] correspondente na lista de trabalhos do painel [!DNL CloudConvert] e verifique a duração do trabalho:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-duration-350x177.png" style="width: 350;height: 177;"> </p> <p>O tempo limite do módulo [!DNL CloudConvert] &gt; [!UICONTROL Converter um Arquivo] está definido como 3 minutos. Se a duração do trabalho exceder 3 minutos (possivelmente devido a uma sobrecarga temporária do serviço [!DNL CloudConvert]), o módulo acionará o erro mencionado acima.</p> <p>Nesse caso, considere uma destas opções:</p> 
    <ul> 
     <li>Habilite a opção <strong>[!UICONTROL Permitir armazenamento de Execuções Incompletas]</strong> nas configurações do cenário para armazenar as execuções incompletas para resolução manual posterior. Opcionalmente, você pode anexar uma rota de tratamento de erros ao módulo [!DNL CloudConvert] com a diretiva [!UICONTROL Break] para resolver as execuções incompletas automaticamente.</li> 
     <li>Desabilite a opção <strong>[!UICONTROL Baixar um arquivo]</strong> no módulo [!DNL CloudConvert] &gt; [!UICONTROL Converter um arquivo]. Nesse caso, o módulo não aguardará o resultado da conversão. Para obter o resultado da conversão, crie um novo cenário e use o gatilho [!DNL CloudConvert] &gt; [!UICONTROL Novo Evento de Trabalho].</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo de fluxo de trabalho para o conector [!DNL CloudConvert]

>[!INFO]
>
>**Exemplo:** Conversão de um vídeo do formato MOV para MP4
>
>1. Visitar [https://cloudconvert.com/video-converter](https://>cloudconvert.com/video-converter)
>1. Clique em **[!UICONTROL Selecionar arquivo]** e escolha seu arquivo MOV de exemplo.
>1. Clique na lista suspensa, ao lado de **[!UICONTROL Converter em]** e escolha **[!UICONTROL MP4]**.
>
>1. Clique na **[!UICONTROL chave inglesa]**.
>1. Defina as configurações de compactação MP4 conforme desejar.
>1. Clique em **[!UICONTROL Converter]**.
>1. Quando a conversão estiver concluída, clique em **[!UICONTROL Baixar]**.
>1. Revise o vídeo convertido.
>1. Repita as etapas de 1 a 8 até encontrar as configurações ideais de conversão para a etapa 5.
>1. Visitar [https://cloudconvert.com/api/v2/convert#convert-tasks](https://cloudconvert.com/api/v2/convert#convert-tasks)
>1. Escolha **[!UICONTROL mov]** para o campo **[!UICONTROL input_format]**.
>
>1. Escolha **[!UICONTROL mp4]** para o campo **[!UICONTROL output_format]**.
>
>1. Uma lista de todos os parâmetros possíveis como video_codec, crf, etc. será exibida.
>1. No Workfront Fusion 2.0, insira o módulo **[!UICONTROL CloudConvert]** > **[!UICONTROL Convert a File]** no seu cenário.
>
>1. Abra as configurações do módulo.
>1. Configure o módulo conforme mostrado abaixo:
>
>   ![Exemplo de CloudConvert](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-mp4-example.png)
>
>1. Certifique-se de incluir todas as configurações no campo Opções específicas de conversão e mecanismo: para cada configuração da etapa 5, localize o parâmetro correspondente da etapa 13 e seu valor correspondente.
