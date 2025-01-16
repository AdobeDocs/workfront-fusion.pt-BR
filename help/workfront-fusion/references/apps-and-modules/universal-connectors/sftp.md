---
title: Módulos SFTP
description: Os  [!DNL Adobe Workfront Fusion SFTP] módulos permitem monitorar as alterações de arquivo em uma pasta/subpasta selecionada, carregar novos arquivos na pasta desejada, modificar ou excluir arquivos existentes que já estejam em uma pasta ou alterar permissões de arquivo.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 0%

---

# Módulos SFTP

Os módulos SFTP do [!DNL Adobe Workfront Fusion] permitem monitorar as alterações de arquivos em uma pasta/subpasta selecionada, carregar novos arquivos na pasta desejada, modificar ou excluir arquivos existentes que já estejam em uma pasta ou alterar permissões de arquivos.

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

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

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Pré-requisitos

Para usar o SFTP com [!DNL Workfront Fusion], é necessário ter uma conta SFTP (como hospedagem na Web [!DNL GoDaddy]).

## Conectar SFTP a [!DNL Workfront Fusion] {#connect-sftp-to-workfront-fusion}

Para conectar sua conta SFTP ao [!DNL Workfront Fusion], você precisa inserir o Host de destino e as credenciais SFTP (nome de usuário e senha ou nome de usuário e chave) para a caixa de diálogo [!UICONTROL Create a connection] do módulo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection name]</td> 
   <td> <p> Insira o nome da conexão SFTP.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
   <td> <p>Digite o nome de host do servidor SFTP que deseja conectar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Port] </td> 
   <td> <p>Insira a porta do servidor SFTP. Por exemplo, 22.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Auth type]</p> </td> 
   <td> <p>Selecione o método de autorização que deseja usar para a conexão com o servidor SFTP.</p> 
    <ul> 
     <li><strong>[!UICONTROL User name and password]</strong>: Insira suas credenciais.</li> 
     <li> <p><strong>[!UICONTROL User name and key]</strong>: Insira seu nome de usuário e a chave privada/certificado</p> <p>Carregue a chave privada para usar a autorização do lado do cliente ou carregue seu certificado (arquivo P12 ou PFX) se quiser usar TLS usando seu certificado autoassinado. Se você estiver usando a autorização de certificado do lado do cliente, insira seu certificado de autoridade de certificação aqui.</p> <p>[!DNL Workfront Fusion] O não retém nem armazena dados (arquivos, senhas) que você fornecer aqui. O arquivo e a senha são usados apenas para extrair uma chave/certificado privado.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Depois de inserir as informações de conexão, clique em **[!UICONTROL Continue]** para estabelecer uma conexão.

## [!UICONTROL SFTP] módulos e seus campos

Ao configurar módulos do [!UICONTROL SFTP], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!UICONTROL SFTP] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Triggers

#### [!UICONTROL Watch Files in a Folder]

Retorna arquivos com detalhes quando um arquivo é criado ou alterado em uma pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Insira ou mapeie a pasta que deseja observar. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Tamanho do buffer [B]</td> 
   <td> <p> Insira o tamanho do buffer em bytes. O valor define o tamanho das partes transferidas do servidor. Alguns servidores podem causar problemas ou corromper arquivos quando o valor é muito alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Defina o número máximo de arquivos com os quais [!DNL Workfront Fusion] trabalhará durante um ciclo</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Subfolders in a Folder]

Retorna pastas com detalhes quando uma pasta é criada ou alterada em uma pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Insira ou mapeie a pasta que deseja observar. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Defina o número máximo de pastas que [!DNL Workfront Fusion] retornará durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

#### [!UICONTROL List a folder's content]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Selecione se deseja recuperar arquivos, pastas ou ambos.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Insira ou mapeie a pasta que contém os arquivos ou pastas que deseja listar. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Insira ou mapeie o termo de pesquisa. Por exemplo, se você deseja procurar arquivos com a extensão .txt, digite <code>.txt</code>.Você também pode inserir ou mapear o nome do arquivo que deseja procurar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Selecione se deseja classificar os resultados por nome de arquivo, tamanho, data do último acesso ou data da última modificação.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order] </td> 
   <td> <p>Selecione se o resultado deve ser retornado em ordem crescente ou decrescente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Ative essa opção para garantir que esse módulo não interrompa o cenário se não retornar resultados.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p> Defina o número máximo de resultados que [!DNL Workfront Fusion] retornará durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Files]

Este módulo lista os arquivos de uma pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Insira o tamanho do buffer em bytes. O valor define o tamanho das partes transferidas do servidor. Alguns servidores podem causar problemas ou corromper arquivos quando o valor é muito alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Insira ou mapeie a pasta que contém os arquivos ou pastas que deseja listar. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Insira ou mapeie o termo de pesquisa. Por exemplo, se você deseja procurar arquivos com a extensão .txt, digite <code>.txt</code>.Você também pode inserir ou mapear o nome do arquivo que deseja procurar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Selecione se deseja classificar os resultados pelo nome do arquivo, tamanho, data do último acesso ou data da última modificação.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order]</td> 
   <td> <p> Selecione se o resultado deve ser retornado em ordem crescente ou decrescente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Ative essa opção para garantir que esse módulo não interrompa o cenário se não retornar resultados.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p> Defina o número máximo de arquivos que [!DNL Workfront Fusion] retornará durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File]

Este módulo recupera detalhes do arquivo, incluindo dados do arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Insira o tamanho do buffer em bytes. O valor define o tamanho das partes transferidas do servidor. Alguns servidores podem causar problemas ou corromper arquivos quando o valor é muito alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path] </td> 
   <td> <p>Insira o caminho para o arquivo. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

Esse módulo permite fazer upload de um arquivo para o servidor SFTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Especifique uma pasta existente como local de armazenamento para o arquivo. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td> <p> Mapeie o arquivo de origem de um módulo anterior, como [!UICONTROL Dropbox] &gt; [!UICONTROL Get File]. Você também pode inserir ou mapear o nome do arquivo e os dados do arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Defina as permissões desejadas para o arquivo ou pasta. Use parâmetros chmod. Por exemplo: <code>777 </code>ou <code>-rwxrwxrwx</code>.</p> <p>Para obter mais detalhes sobre chmod, consulte a <a href="https://ss64.com/bash/chmod.html">documentação sobre chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rename a File]

Renomeia um arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Insira o caminho para o arquivo que você deseja renomear. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New file name]</td> 
   <td> <p> Insira o novo nome do arquivo, incluindo a extensão.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Insira o caminho para o arquivo que deseja mover. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New Folder]</td> 
   <td> <p> Insira o caminho para o novo local do arquivo. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Insira o caminho para o arquivo que deseja excluir. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update file permissions]

Permite alterar as permissões do arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Insira o caminho para o arquivo que deseja mover. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Defina as permissões de arquivo desejadas. Use os parâmetros chmod. Por exemplo, <code>777 </code>ou <code>-rwxrwxrwx</code>.</p> <p>Deve corresponder ao padrão <code> /(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Para obter mais detalhes sobre chmod, consulte a <a href="https://ss64.com/bash/chmod.html">documentação sobre chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Folder]

Cria uma nova pasta no local especificado.

>[!NOTE]
>
>Se a pasta já existir, o módulo emitirá um erro. Para continuar o fluxo sem interrupções, anexe uma rota de manipulador de erros ao módulo para capturar o erro e empregue a diretiva [!UICONTROL Resume] para continuar o fluxo. Para obter informações sobre como anexar uma rota de manipulador de erros, consulte [Tratamento de erros [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md). Para obter informações sobre a rota do manipulador de erros, consulte [Diretivas para manipulação de erros em [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Especifique uma pasta existente como local de armazenamento para a nova pasta. Você pode especificar um caminho absoluto, como <code>/home/user/file.txt</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário logado, como <code>./</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name]</td> 
   <td> <p> Insira o nome da pasta.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Defina as permissões de pasta desejadas. Use parâmetros chmod. Por exemplo, <code>777 </code>ou <code>-rwxrwxrwx</code>.</p> <p>Deve corresponder ao padrão <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Para obter mais detalhes sobre chmod, consulte a <a href="https://ss64.com/bash/chmod.html">Página do manual chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Folder]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta SFTP ao [!DNL Workfront Fusion], consulte <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Conectar SFTP ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> Especifique o caminho para a pasta que deseja excluir. Você pode especificar um caminho absoluto, como <code>/home/user/</code>. Ou você pode especificar um caminho relativo que aponte para uma pasta específica do usuário conectado, como <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
