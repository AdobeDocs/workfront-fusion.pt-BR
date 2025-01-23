---
title: Módulos do CloudConvert
description: Módulos do CloudConvert
author: Becky
feature: Workfront Fusion
exl-id: 52c4d18a-8bee-44d6-9a2c-cc9e157e1dde
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '2486'
ht-degree: 0%

---

# [!DNL CloudConvert] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o CloudConvert, bem como conectá-lo a vários aplicativos e serviços de terceiros. Os módulos do [!DNL CloudConvert] permitem monitorar e gerenciar trabalhos, tarefas e importar e exportar arquivos na sua conta do [!DNL CloudConvert].

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano [!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Adobe Workfront], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

## Informações da API CloudConvert

O conector CloudConvert usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
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

## Conectar [!DNL CloudConvert] a [!DNL Workfront Fusion] {#connect-cloudconvert-to-workfront-fusion}

Para conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], você precisa obter a Chave de API da sua conta do [!DNL CloudConvert].

1. Faça logon em sua conta do [!DNL CloudConvert] e abra o [!UICONTROL Dashboard].
1. Abra a seção **[!UICONTROL Authorization]>[!UICONTROL API Keys]**.
1. Clique em **[!UICONTROL Create New API key]**.
1. Insira o nome da chave de API, habilite os escopos que deseja usar e clique em **[!UICONTROL Create]**.
1. Copie o token fornecido e armazene-o em um local seguro.
1. Em [!DNL Workfront Fusion], comece a criar um cenário e abra a caixa de diálogo **[!UICONTROL Create a connection]** do módulo [!DNL CloudConvert].

   Para obter instruções, consulte [Criar um cenário [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

1. Insira o token salvo na etapa 5 e clique em **[!UICONTROL Continue]** para estabelecer a conexão.

## [!DNL CloudConvert] módulos e seus campos {#cloudconvert-modules-and-their-fields}

Ao configurar módulos do [!DNL CloudConvert], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL CloudConvert] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Tarefas comuns](#common-tasks)
* [Trabalhos](#jobs)
* [Tarefas](#tasks)
* [Outro](#other)

### Tarefas comuns

* [Capturar um site](#capture-a-website)
* [[!UICONTROL Convert a file]](#convert-a-file)
* [Criar um Arquivo Morto](#create-an-archive)
* [Mesclar arquivos](#merge-files)
* [Otimizar um arquivo](#optimize-a-file)

#### [!UICONTROL Capture a Website]

Este módulo de ação captura um site especificado e o salva no formato PDF, JPG ou PNG.

Especifique o URL do site e outras informações, como onde deseja armazenar as informações.

O módulo retorna a ID do arquivo e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira o URL do site que você deseja capturar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>Selecione se deseja salvar o site capturado no formato PNG, JPG ou PDF. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td>Insira um nome de arquivo (incluindo a extensão) para o arquivo de saída de destino.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>(Opcional) Defina os cabeçalhos de solicitação. </p> <p>Isso é útil, por exemplo, quando o URL especificado requer autorização. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Convert a file]

Converte um arquivo em um formato de saída selecionado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input file]</td> 
   <td>Selecione se deseja carregar um arquivo usando [!DNL Workfront Fusion] ou forneça a URL da qual o arquivo será carregado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a File from URL]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Insira o URL do arquivo que você deseja converter.</p> </li> 
     <li> <p><strong>[!UICONTROL Headers]</strong></p> <p>Definir cabeçalhos de solicitação (opcional). Isso é útil, por exemplo, quando o URL especificado requer a autorização.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Format]</td> 
   <td>Selecione se deseja especificar o formato de entrada do arquivo que deseja converter. Se não especificado, a extensão do arquivo de entrada é usada como o formato de entrada.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Input Format]</td> 
   <td>Selecione o formato atual do arquivo.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td>Selecione o formato de arquivo de destino para o qual deseja converter o arquivo.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL File Name]</td> 
   <td>Escolha um nome de arquivo (incluindo a extensão) para o arquivo de saída de destino.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an Archive]

Permite adicionar um ou vários arquivos ao arquivo ZIP, RAR, 7Z, TAR, TAR.GZ ou TAR.BZ2.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>Especifique os arquivos que deseja adicionar ao arquivo morto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Insira o URL do arquivo que deseja arquivar.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>Definir cabeçalhos de solicitação (opcional). Isso é útil, por exemplo, quando o URL especificado requer a autorização.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> Selecione o formato de destino do arquivo arquivado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> Insira o nome do arquivo (incluindo a extensão) para o arquivo de saída de destino.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Merge Files]

Mescla pelo menos dois arquivos em um PDF. Se os arquivos de entrada não forem PDF, eles serão convertidos automaticamente em PDF.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>Especifique os arquivos que deseja mesclar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Insira o URL do arquivo que deseja arquivar.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>Definir cabeçalhos de solicitação (opcional). Isso é útil, por exemplo, quando o URL especificado requer a autorização.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> Selecione o formato de destino do arquivo mesclado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> Insira o nome do arquivo (incluindo a extensão) para o arquivo de saída de destino.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Optimize a File]

Esse módulo de ação otimiza e compacta um arquivo no formato PDF, PNG ou JPG.

Especifique o arquivo e os parâmetros para otimizá-lo e armazená-lo.

O módulo retorna a ID do arquivo e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input File]</td> 
   <td>Selecione se deseja fazer upload de um arquivo usando o Workfront Fusion ou forneça o URL do qual o arquivo será carregado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Upload a File]</p> </td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a file from URL] </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: digite o URL do arquivo que deseja converter.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (Opcional) Defina os cabeçalhos de solicitação. Isso é útil, por exemplo, quando o URL especificado requer autorização.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optimization for] </td> 
   <td> <p>Selecione o perfil de otimização para as necessidades do público-alvo específicas.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Web]</strong>: Otimização para a Web (padrão)</p> 
      <ul> 
       <li>Remover dados redundantes e desnecessários para a Web</li> 
       <li>Diminua a resolução, corte e compacte imagens de forma inteligente</li> 
       <li>Mesclar e subdefinir fontes</li> 
       <li>Converter cores em RGB</li> 
      </ul> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Print]</strong>: otimização para impressão</p> 
      <ul> 
       <li> <p>Remova dados redundantes e desnecessários para impressão</p> </li> 
       <li> <p>Diminua a resolução, corte e compacte imagens de forma inteligente</p> </li> 
       <li> <p>Mesclar e subdefinir fontes</p> </li> 
       <li> <p>Converter cores em CMYK</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Archive]</strong>: otimização para fins de arquivamento</p> 
      <ul> 
       <li> <p>Remova dados redundantes e desnecessários para arquivamento</p> </li> 
       <li> <p>Compactar imagens de forma inteligente</p> </li> 
       <li> <p>Mesclar e subdefinir fontes</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Scanned images]</strong>: otimização para imagens digitalizadas</p> 
      <ul> 
       <li> <p>Perfil otimizado para PDF que consistem principalmente em imagens rasterizadas</p> </li> 
       <li> <p>Compactar as imagens sem reduzir significativamente a qualidade visual</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL maximal size reduction]</strong>: otimização para redução máxima do tamanho</p> 
      <ul> 
       <li> <p>Usar a compactação máxima possível</p> </li> 
       <li> <p>Pode reduzir a qualidade visual</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input format] </td> 
   <td>Selecione o formato do arquivo de entrada que deseja otimizar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p>Insira um nome de arquivo (incluindo a extensão) para o arquivo de saída de destino.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options]</td> 
   <td> <p>Especifique opções específicas de conversão e mecanismo. Para exibir as opções disponíveis, consulte a documentação da API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] </a> para <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file]</td> 
   <td> <p>Ative esta opção se você também quiser incluir dados de arquivo na saída do módulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Trabalhos

* [[!UICONTROL Create a Job (advanced)]](#create-a-job-advanced)
* [[!UICONTROL New Job Event]](#new-job-event)
* [[!UICONTROL List Jobs]](#list-jobs)
* [[!UICONTROL Get a Job]](#get-a-job)
* [[!UICONTROL Delete a Job]](#delete-a-job)

#### [!UICONTROL Create a Job (advanced)]

Este módulo cria uma tarefa. Um trabalho pode ser uma ou várias tarefas identificadas no campo [!UICONTROL Name] e vinculadas entre si usando o campo [!UICONTROL Input].

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input Files]</td> 
   <td> <p>Selecione se deseja carregar um arquivo usando [!DNL Workfront Fusion] ou forneça a URL da qual o arquivo será carregado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a File from URL]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: digite o URL do arquivo que deseja processar.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (Opcional) Defina os cabeçalhos de solicitação. Isso é útil, por exemplo, quando o URL especificado requer autorização.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tasks]</p> </td> 
   <td> <p>Adicione tarefas que serão executadas dentro do trabalho.</p> <p>Encontre as descrições dos campos de operações na seção correspondente.</p> 
    <ul> 
     <li><a href="#convert-a-file" class="MCXref xref">[!UICONTROL Convert a file]</a> </li> 
     <li><a href="#capture-a-website" class="MCXref xref">[!UICONTROL Capture a Websit]e</a> </li> 
     <li><a href="#optimize-a-file" class="MCXref xref">[!UICONTROL Optimize a File]</a> </li> 
     <li><a href="#create-an-archive" class="MCXref xref">[!UICONTROL Create an Archive]</a> </li> 
     <li><a href="#merge-files" class="MCXref xref">[!UICONTROL Merge Files]</a> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Execute a Command]</strong> </p> <p>Para obter mais informações sobre como executar um comando, consulte a <a href="https://cloudconvert.com/api/v2/command#command-tasks">[!DNL CloudConvert] documentação da API</a>.</p> </li> 
     <li> <p><strong>[!UICONTROL Export a File to Temporary URL]</strong> </p> <p> Especifique o nome da tarefa e o nome da tarefa de entrada (por exemplo, Conversão).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag] </td> 
   <td> <p>Insira uma tag. Tags são strings arbitrárias para identificar o trabalho. Elas não têm efeito e podem ser usadas para associar o trabalho a uma ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Job]

Este módulo exclui um trabalho, incluindo todas as tarefas e dados.

>[!NOTE]
>
>As tarefas são excluídas automaticamente 24 horas após terem terminado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>Informe ou mapeie a ID do job que deseja deletar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Job]

Este módulo recupera detalhes do job.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>Informe ou mapeie a ID do job sobre o qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Jobs]

Este módulo recupera todas as tarefas que foram executadas em sua conta.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Selecione o status do trabalho pelo qual filtrar os trabalhos retornados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Defina o número de trabalhos que o Workfront Fusion 2.0 retornará durante um ciclo de execução.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL New Job Event]

Acionado quando um trabalho em sua conta ou tarefa é criado, concluído ou falha.

>[!NOTE]
>
>* O trabalho criado pelo módulo [!UICONTROL Create a Job (advanced)] consiste em *várias* tarefas.
>* O gatilho [!UICONTROL New Job Event] também é acionado quando uma tarefa *individual* é criada, é concluída ou falha.
>

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhhook name]</td> 
   <td>Insira o nome do webhook. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>Selecione se deseja salvar o site capturado no formato PNG, JPG ou PDF. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event]</td> 
   <td>Selecione se o módulo será acionado quando a tarefa ou o trabalho for criado, concluído ou falhar.</td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Se estiver trabalhando com o Agregador de Matrizes (por exemplo, você tem muitos arquivos em diferentes formatos para converter), use a opção **[!UICONTROL I don't know the input format]** na caixa de diálogo [!UICONTROL Add a task]. Caso contrário, o erro será retornado.
>* Vincular tarefas no trabalho (nome > entrada, nome > entrada,...):
>
>  ![](/help/workfront-fusion/references/apps-and-modules/assets/linking-name-across-jobs-350x808.png)>

### Tarefas

* [[!UICONTROL Get a Task]](#get-a-task)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL List Tasks]](#list-tasks)
* [[!UICONTROL Retry a Task]](#retry-a-task)
* [[!UICONTROL Cancel a Task]](#cancel-a-task)
* [[!UICONTROL Delete a Task]](#delete-a-task)

#### [!UICONTROL Cancel a Task]

Este módulo cancela uma tarefa que tem um status de espera ou processamento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Insira ou mapeie a ID da tarefa que deseja cancelar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Task]

Excluir uma tarefa, incluindo todos os dados.

>[!NOTE]
>
>As tarefas são excluídas automaticamente 24 horas após terem terminado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Insira (mapeie) a ID da tarefa que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Este módulo recupera o nome do arquivo e os dados do arquivo da tarefa especificada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Insira ou mapeie a ID da tarefa da qual deseja baixar o arquivo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Task]

Este módulo recupera detalhes da tarefa.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p>Insira ou mapeie a ID da tarefa sobre a qual deseja recuperar detalhes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Tasks]

Este módulo recupera todas as tarefas em sua conta com base nas configurações de filtro.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Selecione o status da tarefa pelo qual filtrar as tarefas retornadas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID] </td> 
   <td> <p>Insira ou mapeie a ID do trabalho para retornar somente tarefas dentro do trabalho especificado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>Informe o tipo de operação para retornar somente tarefas com a operação especificada. </p> <p>Observação: use o módulo [!UICONTROL List Possible Operations] para recuperar operações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Retry a Task]

Este módulo cria uma nova tarefa, baseada nas configurações (carga útil) de outra tarefa.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Digite ou mapeie a ID da tarefa da qual deseja criar uma nova tarefa.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outro

* [[!UICONTROL Get My Info]](#get-my-info)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Get My Info]

Recupera detalhes da conta autenticada sobre o usuário atual.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL CloudConvert] ao [!DNL Workfront Fusion], consulte <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Conectar [!DNL CloudConvert] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [Fusion App] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Insira um caminho relativo para <code>https://api.cloudconvert.com/</code>. Por exemplo: <code>/v2/tasks</code></p> <p>Para obter a lista de pontos de extremidade disponíveis, consulte a <a href="https://cloudconvert.com/api/v2">[!DNL CloudConvert] Documentação da API v2</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion 2.0 adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão. Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo:** Tarefas de Lista

A chamada de API a seguir retorna todas as tarefas da conta do CloudFront:

URL: `/v2/tasks`

Método: `GET`

![](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-input.png)

Correspondências da pesquisa podem ser encontradas na Saída do módulo em [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL data].

No nosso exemplo, 6 tarefas foram retornadas:

![](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-output.png)

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
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL The output file size exceeds the limit allowed for your scenario.]</span> </p> </td> 
   <td> <p>Consulte os limites de tamanho de arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL You have exceeded the maximum conversion time.]</span> </p> </td> 
   <td> <p>O plano [!DNL CloudConvert] gratuito oferece 25 minutos de conversão diariamente. Se o seu uso exceder o limite do plano gratuito, você poderá alternar para um pacote (pré-pago) ou assinatura.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Failed to read frame size: Could not seek to 1508. �/output/JLIADSA00137P0.mp3: Invalid argument.]</span> </p> </td> 
   <td> <p>Esse erro é lançado, por exemplo, ao converter arquivos de MP3 para WAV. Verifique se você selecionou a região correta porque ela encontrará referências a arquivos, mas não apenas ao arquivo correto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL RuntimeError:] </p> <p><span style="font-weight: normal;">[!UICONTROL Maximum number of repeats exceeded.]</span> </p> </td> 
   <td> <p>Localize o trabalho [!DNL CloudConvert] correspondente na lista de trabalhos do painel [!DNL CloudConvert] e verifique a duração do trabalho:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-duration-350x177.png" style="width: 350;height: 177;"> </p> <p>O tempo limite do módulo [!DNL CloudConvert] &gt; [!UICONTROL Convert a File] está definido como 3 minutos. Se a duração do trabalho exceder 3 minutos (possivelmente devido a uma sobrecarga temporária do serviço [!DNL CloudConvert]), o módulo acionará o erro mencionado acima.</p> <p>Nesse caso, considere uma destas opções:</p> 
    <ul> 
     <li>Habilite a opção <strong>[!UICONTROL Allow storing of Incomplete Executions]</strong> nas configurações do cenário para armazenar as execuções incompletas para resolução manual posterior. Opcionalmente, você pode anexar uma rota de tratamento de erros ao módulo [!DNL CloudConvert] com a diretiva [!UICONTROL Break] para resolver as execuções incompletas automaticamente.</li> 
     <li>Desabilite a opção <strong>[!UICONTROL Download a file] </strong> no módulo [!DNL CloudConvert] &gt; [!UICONTROL Convert a file]. Nesse caso, o módulo não aguardará o resultado da conversão. Para obter o resultado da conversão, crie um novo cenário e use o gatilho [!DNL CloudConvert] &gt; [!UICONTROL New Job Event].</li> 
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
>1. Clique em **[!UICONTROL Select File]** e escolha seu arquivo MOV de exemplo.
>1. Clique na lista suspensa, ao lado de **[!UICONTROL Convert to]** e escolha **[!UICONTROL MP4]**.
>
>1. Clique no ícone **[!UICONTROL wrench]**.
>1. Defina as configurações de compactação MP4 conforme desejar.
>1. Clique em **[!UICONTROL Convert]**.
>1. Quando a conversão estiver concluída, clique em **[!UICONTROL Download]**.
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
>   ![](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-mp4-example.png)
>
>1. Certifique-se de incluir todas as configurações no campo Opções específicas de conversão e mecanismo: para cada configuração da etapa 5, localize o parâmetro correspondente da etapa 13 e seu valor correspondente.
