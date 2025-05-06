---
title: Módulos SFTP
description: Os  [!DNL Adobe Workfront Fusion SFTP] módulos permitem monitorar as alterações de arquivo em uma pasta/subpasta selecionada, carregar novos arquivos na pasta desejada, modificar ou excluir arquivos existentes que já estejam em uma pasta ou alterar permissões de arquivo.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: 26c599a9887ad931763b787813153bb7791ce5d1
workflow-type: tm+mt
source-wordcount: '2121'
ht-degree: 0%

---

# Módulos SFTP

Os módulos SFTP do [!DNL Adobe Workfront Fusion] permitem monitorar as alterações de arquivos em uma pasta/subpasta selecionada, carregar novos arquivos na pasta desejada, modificar ou excluir arquivos existentes que já estejam em uma pasta ou alterar permissões de arquivos.

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

## Pré-requisitos

Para usar o SFTP com [!DNL Workfront Fusion], é necessário ter uma conta SFTP (como hospedagem na Web [!DNL GoDaddy]).

## Conectar SFTP a [!DNL Workfront Fusion] {#connect-sftp-to-workfront-fusion}

Para conectar sua conta SFTP ao [!DNL Workfront Fusion], você precisa criar uma conexão que especifique o Host de destino e as credenciais SFTP (nome de usuário e senha ou nome de usuário e chave).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome da Conexão]</td> 
   <td> <p> Insira o nome da conexão SFTP.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Ambiente]</td>
    <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Tipo]</td>
    <td>Selecione se você deseja se conectar a uma conta de serviço ou a uma conta pessoal.</td>
  </tr>
  <tr>
   <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
   <td> <p>Digite o nome de host do servidor SFTP que deseja conectar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Porta] </td> 
   <td> <p>Insira a porta do servidor SFTP. Por exemplo, 22.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo de autenticação]</p> </td> 
   <td> <p>Selecione o método de autorização que deseja usar para a conexão com o servidor SFTP.</p> 
    <ul> 
     <li><strong>[!UICONTROL Nome de usuário e senha]</strong>: digite suas credenciais.</li> 
     <li> <p><strong>[!UICONTROL Nome de usuário e chave]</strong>: digite seu nome de usuário e a chave privada/certificado</p> <p>Carregue a chave privada para usar a autorização do lado do cliente ou carregue seu certificado (arquivo P12 ou PFX) se quiser usar TLS usando seu certificado autoassinado. Se você estiver usando a autorização de certificado do lado do cliente, insira seu certificado de autoridade de certificação aqui.</p> <p>[!DNL Workfront Fusion] O não retém nem armazena dados (arquivos, senhas) que você fornecer aqui. O arquivo e a senha são usados apenas para extrair uma chave/certificado privado.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algoritmos de troca de chaves] </td> 
   <td> <p>Você pode inserir um conjunto de algoritmos para troca de chaves. O módulo prioriza algoritmos com base na ordem em que foram adicionados. Para cada algoritmo que deseja adicionar, clique em <b>Adicionar item</b> e selecione o algoritmo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cifras] </td> 
   <td> <p>Você pode inserir um conjunto de cifras para troca de chaves. O módulo prioriza cifras com base na ordem em que foram adicionadas. Para cada cifra que você deseja adicionar, clique em <b>Adicionar item</b> e selecione a cifra.</p> </td> 
  </tr> 
 </tbody> 
</table>

Depois de inserir as informações de conexão, clique em **[!UICONTROL Continuar]** para estabelecer uma conexão.

## Módulos [!UICONTROL SFTP] e seus campos

Ao configurar módulos [!UICONTROL SFTP], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com eles, campos [!UICONTROL SFTP] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Acionadores

* [Observar arquivos em uma pasta](#watch-files-in-a-folder)
* [Observar subpastas em uma pasta](#watch-subfolders-in-a-folder)

#### [!UICONTROL Observar arquivos em uma pasta]

Retorna arquivos com detalhes quando um arquivo é criado ou alterado em uma pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Insira a pasta que deseja observar. Você pode especificar um caminho absoluto, como <code>/home/user/</code>, ou pode especificar um caminho relativo apontando para uma pasta específica do usuário logado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Tamanho do buffer [B]</td> 
   <td> <p> Insira o tamanho do buffer em bytes. O valor define o tamanho das partes transferidas do servidor. Alguns servidores podem causar problemas ou corromper arquivos quando o valor é muito alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de arquivos retornados]</td> 
   <td> <p> Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar Subpastas em uma Pasta]

Retorna pastas com detalhes quando uma pasta é criada ou alterada em uma pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Insira ou mapeie a pasta que deseja observar. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de arquivos retornados]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [Criar uma pasta](#create-a-folderr)
* [Excluir um arquivo](#delete-a-file)
* [Excluir uma pasta](#delete-a-folder)
* [Obter um arquivo](#get-a-file)
* [Obter arquivos](#get-files)
* [Listar o conteúdo de uma pasta](#list-a-folders-content)
* [Mover um arquivo](#move-a-file)
* [Renomear um arquivo](#rename-a-file)
* [Atualizar permissões de arquivo](#update-file-permissions)
* [Carregar um arquivo](#upload-a-file)

#### [!UICONTROL Criar uma pasta]

Este módulo de ação cria uma nova pasta no local especificado.

>[!NOTE]
>
>Se a pasta já existir, o módulo emitirá um erro. Para continuar o fluxo sem interrupções, anexe uma rota de manipulador de erros ao módulo para capturar o erro e empregue a diretiva [!UICONTROL Resume] para continuar o fluxo. Para obter informações sobre como anexar uma rota de manipulador de erros, consulte [Tratamento de erros [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md). Para obter informações sobre a rota do manipulador de erros, consulte [Diretivas para manipulação de erros em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Especifique uma pasta existente como local de armazenamento para a nova pasta. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nome da Pasta]</td> 
   <td> <p> Insira o nome da pasta.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissões]</p> </td> 
   <td> <p>Defina as permissões de pasta desejadas. Use parâmetros chmod. Por exemplo, <code>777</code> ou <code>-rwxrwxrwx</code>.</p> <p>Essas permissões devem corresponder ao padrão <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Para obter mais informações sobre chmod, consulte a <a href="https://ss64.com/bash/chmod.html">documentação de chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um arquivo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Caminho do Arquivo]</td> 
   <td> <p> Insira o caminho para o arquivo que deseja excluir. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma pasta]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> Especifique o caminho para a pasta que deseja excluir. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um arquivo]

Este módulo recupera detalhes do arquivo, incluindo dados do arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tamanho do Buffer [B]]</td> 
   <td> <p> Insira o tamanho do buffer em bytes. O valor define o tamanho das partes transferidas do servidor. Alguns servidores podem causar problemas ou corromper arquivos quando o valor é muito alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Caminho do Arquivo] </td> 
   <td> <p>Insira o caminho para o arquivo. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter arquivos]

Este módulo retorna arquivos de uma pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tamanho do Buffer [B]]</td> 
   <td> <p> Insira o tamanho do buffer em bytes. O valor define o tamanho das partes transferidas do servidor. Alguns servidores podem causar problemas ou corromper arquivos quando o valor é muito alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Insira ou mapeie a pasta que contém os arquivos ou pastas que deseja listar. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar] </td> 
   <td> <p>Insira ou mapeie o termo de pesquisa. Por exemplo, se você deseja procurar arquivos com a extensão .txt, digite <code>.txt</code>.Você também pode inserir ou mapear o nome do arquivo que deseja procurar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Classificar por]</td> 
   <td> <p> Selecione se deseja classificar os resultados pelo nome do arquivo, tamanho, data do último acesso ou data da última modificação.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordem de Classificação]</td> 
   <td> <p> Selecione se o resultado deve ser retornado em ordem crescente ou decrescente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continuar a execução da rota mesmo se o módulo não retornar resultados]</p> </td> 
   <td>Ative essa opção para garantir que esse módulo não interrompa o cenário se não retornar resultados.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de resultados retornados]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar o conteúdo de uma pasta]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mostrar] </td> 
   <td> <p>Selecione se deseja recuperar arquivos, pastas ou ambos.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Insira ou mapeie a pasta que contém os arquivos ou pastas que deseja listar. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar] </td> 
   <td> <p>Insira ou mapeie o termo de pesquisa. Por exemplo, se você deseja procurar arquivos com a extensão .txt, digite <code>.txt</code>.Você também pode inserir ou mapear o nome do arquivo que deseja procurar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Classificar por]</td> 
   <td> <p> Selecione se deseja classificar os resultados por nome de arquivo, tamanho, data do último acesso ou data da última modificação.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordem de Classificação] </td> 
   <td> <p>Selecione se o resultado deve ser retornado em ordem crescente ou decrescente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continuar a execução da rota mesmo se o módulo não retornar resultados]</p> </td> 
   <td>Ative essa opção para garantir que esse módulo não interrompa o cenário se não retornar resultados.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de resultados retornados]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mover um Arquivo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Caminho do Arquivo]</td> 
   <td> <p> Insira o caminho para o arquivo que deseja mover. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nova Pasta]</td> 
   <td> <p> Insira o caminho para o novo local do arquivo. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Renomear um Arquivo]

Renomeia um arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Caminho do Arquivo]</td> 
   <td> <p> Insira o caminho para o arquivo que você deseja renomear. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Novo nome de arquivo]</td> 
   <td> <p> Insira o novo nome do arquivo, incluindo a extensão.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar permissões de arquivo]

Permite alterar as permissões do arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Caminho do Arquivo]</td> 
   <td> <p> Insira o caminho para o arquivo que deseja mover. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissões]</p> </td> 
   <td> <p>Defina as permissões de arquivo desejadas. Use parâmetros chmod. Por exemplo, <code>777</code> ou <code>-rwxrwxrwx</code>.</p> <p>Essas permissões devem corresponder ao padrão <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Para obter mais informações sobre chmod, consulte a <a href="https://ss64.com/bash/chmod.html">documentação de chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um arquivo]

Esse módulo permite fazer upload de um arquivo para o servidor SFTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Especifique uma pasta existente como local de armazenamento para o arquivo. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Arquivo Source]</td> 
   <td> <p> Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissões]</p> </td> 
   <td> <p>Defina as permissões desejadas para o arquivo ou pasta. Use parâmetros chmod. Por exemplo, <code>777</code> ou <code>-rwxrwxrwx</code>.</p> <p>Essas permissões devem corresponder ao padrão <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Para obter mais informações sobre chmod, consulte a <a href="https://ss64.com/bash/chmod.html">documentação de chmod</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tamanho do buffer (B)]</p> </td> 
   <td> <p>Defina o tamanho (em bytes) de cada bloco ao fazer upload do arquivo. Isso é útil para arquivos grandes ou quando os limites de memória do servidor exigem uploads menores. Se esse valor não for definido, o arquivo será gravado em uma única operação.</p> </td> 
  </tr> 
 </tbody> 
</table>
