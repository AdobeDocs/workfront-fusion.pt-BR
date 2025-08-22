---
title: Módulos de drive Google
description: Os  [!DNL Adobe Workfront Fusion Google Drive] módulos permitem que você monitore, pesquise, crie, atualize, exclua e gerencie seus arquivos, pastas ou unidades compartilhadas em seu  [!DNL Google Drive].
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2096'
ht-degree: 0%

---

# [!DNL Google Drive] módulos

Os módulos do Adobe Workfront Fusion [!DNL Google Drive] permitem monitorar, pesquisar, criar, atualizar, excluir e gerenciar arquivos, pastas ou unidades compartilhadas no [!DNL Google Drive].

Em um cenário do Adobe Workfront Fusion, você pode conectar sua conta do [!DNL Google Drive] a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion</p>
   <p>Ou</p>
   <p>Herdados: Automação e integração do Workfront Fusion for Work </p>
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

## Informações da API do Google Drive

O conector da unidade Google usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td> https://www.googleapis.com/drive/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v4.1.22</td> 
  </tr>
 </tbody> 
 </table>



## Conectando o [!DNL Google Drive] ao Workfront Fusion

Se você usa [!DNL @gmail.com] ou [!DNL @googlemail.com] usuário, deve criar um cliente OAuth no [!DNL Google Cloud Platform] para obter sua [!UICONTROL ID do Cliente] e [!UICONTROL Segredo do Cliente].

Para obter instruções passo a passo sobre como criar o cliente OAuth (e obter a [!UICONTROL ID do Cliente] e o [!UICONTROL Segredo do Cliente]), consulte [Conectar o Adobe Workfront Fusion ao [!DNL Google Services] usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL Google Drive] módulos e seus campos

Ao configurar módulos do [!DNL Google Drive], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Google Drive] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [Acionadores](#triggers)
* [Ações](#actions)

### Acionadores

* [[!UICONTROL Assistir a todos os arquivos]](#watch-all-files)
* [[!UICONTROL Assistir comentários]](#watch-comments)
* [[!UICONTROL Observar arquivos na pasta]](#watch-files-in-folder)
* [[!UICONTROL Observar arquivos compartilhados]](#watch-shared-files)

#### [!UICONTROL Assistir a todos os arquivos]

Este módulo de acionador inicia um cenário quando um arquivo em seu [!DNL Google Drive] é adicionado ou modificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Quais arquivos observar]</td> 
   <td> <p>Selecione o tipo de arquivo que deseja observar.</p> 
    <ul> 
     <li>[!UICONTROL Tudo]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Converter [!DNL Google Documents] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Spreadsheets] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Slides] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Drawings] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Drawings].</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Observar]</td> 
   <td>Selecione se deseja observar novos arquivos e todas as alterações ou somente novos arquivos.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de arquivos baixados]</td> 
   <td>Defina o número máximo de resultados que o Workfront Fusion baixará durante um ciclo (o número de repetições por execução de cenário).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assistir Comentários]

Esse módulo de acionamento inicia um cenário quando um comentário é adicionado ou modificado no arquivo selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Arquivo]</td> 
   <td>Selecione o arquivo que deseja observar para comentários.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Observar]</td> 
   <td>Selecione se você deseja observar todas as alterações ou somente os novos comentários</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de comentários retornados]</td> 
   <td>Defina o número máximo de comentários que o Workfront Fusion retornará durante um ciclo (o número de repetições por execução de cenário).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar arquivos na pasta]

Este módulo de acionamento inicia um cenário quando um arquivo é adicionado ou modificado na pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Selecionar a pasta a ser observada]</td>
    <td >Selecione a pasta na unidade em que deseja observar os arquivos.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Quais arquivos observar]</td>
   <td> <p>Selecione o tipo de arquivo que deseja observar.</p> 
    <ul> 
     <li>[!UICONTROL Tudo]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Converter [!DNL Google Documents] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Spreadsheets] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Slides] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Drawings] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Drawings].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Observar]</td>
    <td>Selecione se deseja observar novos arquivos e todas as alterações ou somente novos arquivos.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Número máximo de arquivos baixados]</td>
    <td>Defina o número máximo de resultados que o Workfront Fusion baixará durante um ciclo (o número de repetições por execução de cenário).</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar arquivos compartilhados]

Dispara quando um novo arquivo é compartilhado com você ou um arquivo compartilhado existente é atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Selecionar a pasta a ser observada]</td> 
   <td>Selecione a pasta compartilhada na qual você deseja observar os arquivos.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Quais arquivos observar]</td> 
   <td> <p>Selecione o tipo de arquivo que deseja observar.</p> 
    <ul> 
     <li>[!UICONTROL Tudo]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Converter [!DNL Google Documents] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Spreadsheets] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Slides] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converter [!DNL Google Drawings] arquivos no formato]</td>
    <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Drawings].</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Observar]</td> 
   <td>Selecione se deseja observar novos arquivos e todas as alterações ou somente novos arquivos.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de arquivos baixados]</td> 
   <td>Defina o número máximo de resultados que o Workfront Fusion baixará durante um ciclo (o número de repetições por execução de cenário).</td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Copiar um arquivo]](#copy-a-file)
* [[!UICONTROL Criar uma fFolder]](#create-a-folder)
* [[!UICONTROL Excluir um arquivo]](#delete-a-file)
* [[!UICONTROL Obter um arquivo]](#get-a-file)
* [[!UICONTROL Obter um link de compartilhamento]](#get-a-share-link)
* [[!UICONTROL Mover um arquivo para a lixeira]](#move-a-filefolder-to-trash)
* [[!UICONTROL Procurar Arquivos/Pastas]](#search-for-filesfolders)
* [[!UICONTROL Atualizar um Arquivo]](#update-a-file)
* [[!UICONTROL Carregar um arquivo]](#upload-a-file)

#### [!UICONTROL Copiar um arquivo]

Este módulo de ação copia um arquivo para o novo local.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destino]</td> 
   <td> <p>Selecione o destino para o qual deseja copiar um arquivo.</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado comigo]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta de Destino]</td> 
   <td>Selecione a pasta que contém o arquivo a ser copiado.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Arquivo]</td> 
   <td>Mapeie a ID do arquivo que você deseja copiar.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL O nome da cópia]</td> 
   <td>Insira um título para o novo arquivo. Deixe esse campo em branco se não quiser alterar o nome do arquivo original.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar uma pasta]

Este módulo de ação cria uma pasta no local especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destino]</td> 
   <td> <p>Selecione o destino no qual deseja criar uma pasta.</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado comigo]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Novo local de pasta]</td> 
   <td>Navegue até o local onde deseja criar uma nova pasta.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL O nome da nova pasta]</td> 
   <td>Insira um nome para a pasta que está sendo criada.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Compartilhar pasta]</td> 
   <td>Selecione esta opção se desejar compartilhar a pasta com qualquer pessoa com o link [!UICONTROL Compartilhar]. Caso contrário, o link de compartilhamento será somente para o proprietário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um arquivo]

Este módulo de ação exclui permanentemente um arquivo ou pasta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Arquivo]</td> 
   <td>Mapeie a ID do arquivo que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um arquivo]

Este módulo de ação recupera o arquivo com a ID especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converter [!DNL Google Documents] arquivos no formato]</td> 
   <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Documents].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converter [!DNL Google Spreadsheets] arquivos no formato]</td> 
   <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Spreadsheets].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converter [!DNL Google Slides] arquivos no formato]</td> 
   <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Slides].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converter [!DNL Google Drawings] arquivos no formato]</td> 
   <td>Selecione o formato de arquivo para o qual você deseja converter [!DNL Google Drawings].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Arquivo]</td> 
   <td>Mapeie a ID do arquivo que você deseja recuperar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um link de compartilhamento]

Este módulo de ação recupera o link de compartilhamento de um arquivo no Google Drive.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Arquivo]</td> 
   <td>Mapeie a ID do arquivo para o qual você deseja obter o link de compartilhamento.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mover um arquivo para a lixeira]

Este módulo de ação move um arquivo ou pasta para o lixo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Arquivo]</td> 
   <td>Mapeie a ID do arquivo que você deseja mover para a lixeira.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Procurar Arquivos/Pastas]

Este módulo de pesquisa procura por arquivos ou pastas com base nos critérios de pesquisa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destino]</td> 
   <td> <p>Selecione a unidade de destino que deseja pesquisar.</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado comigo]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Listar uma pasta]</td> 
   <td>Navegue até a pasta na qual deseja pesquisar os arquivos ou pastas.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recuperar]</td> 
   <td> <p> Selecione se deseja pesquisar arquivos, pastas ou ambos.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Pesquisar]</p> </td> 
   <td> <p>Selecione o tipo de pesquisa que deseja realizar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Pesquisar em nomes de arquivo/pasta]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Consulta]</strong> </p> <p>Insira uma parte do nome do arquivo ou o nome completo do arquivo (incluindo o sufixo) que deseja pesquisar.</p> </li> 
       <li> <p><strong>[!UICONTROL Opções de Pesquisa]</strong> </p> <p>Selecione se deseja pesquisar o termo exato ou se deseja pesquisar nomes contendo o termo de pesquisa.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Texto Completo] pesquisa</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Consulta]</strong> </p> <p>Digite qualquer termo de pesquisa que você deseja pesquisar em seu [!DNL Google Drive].</p> </li> 
      </ul> </li> 
     <li> <p><strong>Inserir consulta de pesquisa personalizada</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Consulta]</strong> </p> <p>Insira a consulta de pesquisa personalizada. Para obter mais detalhes, consulte a seção [!UICONTROL Pesquisar Arquivos] deste artigo.</p> </li> 
       <li> <p><strong>Adicionar a pasta selecionada acima à consulta</strong> </p> <p>Pesquisa a pasta na coleção pai. Isso encontrará todos os arquivos e pastas localizados diretamente na pasta selecionada acima.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de resultados retornados]</td> 
   <td>Defina o número máximo de arquivos ou pastas que o Workfront Fusion retornará durante um ciclo de execução.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continuar a execução da rota mesmo se o módulo não retornar resultados]</td> 
   <td>Ative essa opção para garantir que o cenário não seja interrompido se o módulo não retornar resultados.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um Arquivo]

Esse módulo de ação atualiza os metadados ou o conteúdo de um arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destino]</td> 
   <td> <p>Selecione o destino que contém o arquivo que você deseja atualizar.</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado comigo]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mover para uma pasta]</td> 
   <td>Se desejar mover o arquivo para uma pasta específica, selecione a pasta para onde deseja mover o arquivo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Arquivo]</td> 
   <td>Mapeie a ID do arquivo que você deseja atualizar.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Título]</td> 
   <td>Insira um título para o arquivo atualizado.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Alterar um conteúdo de arquivo]</td> 
   <td>Selecione se deseja substituir o conteúdo do arquivo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL arquivo Source]</td> 
   <td>Se você estiver substituindo o conteúdo, selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converter um arquivo]</td> 
   <td>Habilite esta opção para converter o arquivo para o formato de arquivo Google correspondente.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um arquivo]

Carrega um arquivo no [!DNL Google Drive].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Drive] ao Workfront Fusion, consulte <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL Google Drive] ao [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Destination]</td> 
   <td> <p>Selecione o destino para o qual deseja fazer upload de um arquivo.</p> 
    <ul> 
     <li>[!DNL My Drive]</li> 
     <li>[!DNL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta de Destino]</td> 
   <td>Selecione a pasta na qual deseja fazer upload de um arquivo. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL arquivo Source]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Título]</td> 
   <td>Insira um título para o novo arquivo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converter um arquivo]</td> 
   <td>Habilitar essa opção permite que o módulo converta arquivos no formato [!DNL Google] correspondente.</td> 
  </tr> 
 </tbody> 
</table>

## Solução de problemas

### Não é possível carregar ou atualizar um arquivo

Há vários motivos pelos quais o upload ou a atualização de um arquivo falha:

* O arquivo carregado é muito grande e excede o limite de tamanho máximo de arquivo permitido para o plano [!DNL Google Drive] ou você excedeu o limite de armazenamento de [!DNL Google Drive]. Você pode atualizar seu plano de armazenamento ou excluir arquivos existentes do serviço [!DNL Google Drive].
* A pasta selecionada para onde o arquivo deveria ser carregado não existe mais. Nesse caso, o cenário é interrompido e você deve selecionar uma pasta de destino diferente no módulo.

<!-- Not present February 2025

## Search for files

In the module List files in a folder you can use your own query which consists of these parts:

* **[!UICONTROL Field]** - Attribute of the file that is being searched, for example, the attribute `name` of the file.

* **[!UICONTROL Operator]** - Test that is performed on the data to provide a match, for example, `contains`.

* **[!UICONTROL Value]** - The content of the attribute that is tested, for example, the name of the file `My cool document`.

Combine clauses with the conjunctions `and` or `or`, and negate the query with `not`.

* [Fields](#fields)
* [Value types](#value-types)
* [Operators](#operators)
* [Examples](#examples)

### Fields 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Field </th> 
   <th>Value Type </th> 
   <th>Operators</th> 
   <th> <p> Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>string</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Name of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>string </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> Full text of the file including name, description, content, and indexable text.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> string</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> MIME type of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date of the last modification to the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date that the user last viewed a file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Whether the file is in the trash or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Whether the file is starred or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Whether the [!UICONTROL parents] collection contains the specified ID.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who own the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to modify the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to read the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Files that are in the user's "Shared with me" collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>collection</td> 
   <td><code>has </code> </td> 
   <td> <p> Public custom file properties.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consider the following about operators in these fields:

* The `contains` operator only performs prefix matching for a `title`.

   For example, the title "HelloWorld" matches for `title contains 'Hello'` but not for `title contains 'World'`.

* The `contains` operator only performs matching on entire string tokens for `fullText`.

   For example, if the full text of a doc contains the string "HelloWorld" only the query `fullText contains 'HelloWorld'` returns a result. Queries such as `fullText contains 'Hello'` would not return results in this scenario.

* The `contains` operator matches on an exact alphanumeric phrase if it is surrounded by double quotes.

   For example, if the `fullText` of a doc contains the string "Hello there world", then the query `fullText contains '"Hello there"'` returns a result, but the query `fullText contains '"Hello world"'` does not.

   Furthermore, because the search is alphanumeric, if the `fullText` of a doc contains the string "Hello_world", then the query `fullText contains '"Hello world"'` returns a result.

* Fields of `type` date are currently not comparable to each other, only to constant dates.

### Value types

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Value Type</th> 
   <th> <p> Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>String </td> 
   <td> <p>Surround with single quotes '. Escape single quotes in queries with <code>\'</code>, e.g.,<code> 'Valentine\'s Day'</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolean </td> 
   <td> <p><code>true </code>or <code>false</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td> <p>RFC 3339 format, default timezone is UTC, e.g., <code>2012-06-04T12:00:00-08:00</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Operators

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Operator </th> 
   <th> <p>Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>The content of one string is present in the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> The content of a string or boolean is equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> The content of a string or boolean is not equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> A date is earlier than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> A date is earlier than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> A date is later than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> A date is later than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>An element is contained within a collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Return files that match both clauses.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Return files that match either clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Negates a search clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>A collection contains an element matching the parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

For compound clauses, you can use parentheses to group clauses together. For example:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` This search returns all files with an image or video MIME type that their last modification was after June 4, 2012. Because `and` and `or` operators are evaluated from left to right, without parentheses, the above example would return only images modified after June 4, 2012, but would return all videos, even those before June 4, 2012.

### Examples 

All examples on this page show the unencoded `<q>q</q>` parameter, where `title = 'hello'` is encoded as `title+%3d+%27hello%27`. Client libraries handle this encoding automatically.

* Search for files with the name "hello"
   <pre>title = 'hello'</pre>
* Search for folders using the folder-specific MIME type
   <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Search for files that are not folders
   <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Search for files with a name containing the words "hello" and "goodbye"
   <pre>title contains 'hello' and [!UICONTROL name] contains 'goodbye'</pre>
* Search for files with a name that does not contain the word "hello"
   <pre>not title contains 'hello'</pre>
* Search for files containing the word "hello" in the content
   <pre>fullText contains 'hello'</pre>
* Search for files not containing the word "hello" in the content
   <pre>not fullText contains 'hello'</pre>
* Search for files containing the exact phrase "hello world" in the content
   <pre>fullText contains '"hello world"'fullText contains '"hello_world"'</pre>
* Search for files with a query containing the "\" character (e.g., "\authors")
   <pre>fullText contains '\\authors'</pre>
* Search for files writeable by the user `test@example.org`
   <pre>'test@example.org' in [!DNL writers]</pre>
* Search for the ID `1234567` in the `parents` collection. This finds all files and folders located directly in the folder whose ID is `1234567`.
   <pre>'1234567' in [!UICONTROL parents]</pre>
* Search for the alias ID `appDataFolder` in the `parents` collection. This finds all files and folders located directly under the [Application Data folder](https://developers.google.com/drive/api/v2/appdata).
   <pre>'appDataFolder' in parents</pre>
* Search for files writeable by the users `test@example.org` and `test2@example.org`
   <pre>'test@example.org' in writers and 'test2@example.org' in writers</pre>
* Search for files containing the text "important" which are in the trash
   <pre>fullText contains 'important' and trashed = true</pre>
* Search for files modified after June 4th 2012
   <pre>modifiedDate > '2012-06-04T12:00:00' // default time zone is UTC</pre><pre>modifiedDate > '2012-06-04T12:00:00-08:00'</pre>
* Search for files shared with the authorized user with "hello" in the name
   <pre>sharedWithMe and title contains 'hello'</pre>
* Search for files with a [custom file property](https://developers.google.com/drive/api/v2/properties) named `additionalID` with the value `8e8aceg2af2ge72e78`.
   <pre>properties has { key='additionalID' and value='8e8aceg2af2ge72e78' and visibility='PRIVATE' }</pre>

Source of this guide is [[!DNL Google Drive] documentation](https://developers.google.com/drive/api/v2/search-shareddrives).

-->
