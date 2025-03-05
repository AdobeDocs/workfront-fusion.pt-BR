---
title: Módulos FTP
description: Os módulos FTP permitem monitorar as alterações de arquivos em uma pasta selecionada, fazer upload de novos arquivos para a pasta desejada e modificar ou excluir arquivos existentes que já estão em uma pasta.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: 85cd8dbf70dff220f593fa669b447bf5df2a21a2
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 0%

---

# Módulos FTP

Os módulos FTP permitem monitorar as alterações de arquivos em uma pasta selecionada, fazer upload de novos arquivos para a pasta desejada e modificar ou excluir arquivos existentes que já estão em uma pasta.

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
   <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
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

Para usar módulos FTP, você deve ter uma conta com um serviço FTP.

## Criar uma conexão em um módulo FTP {#create-a-connection}

1. Em qualquer módulo FTP, clique em **Adicionar** ao lado da caixa de conexão.
1. Preencha os campos a seguir.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Nome da Conexão]</td> 
      <td> <p> Insira o nome da conexão FTP.</p> </td> 
     </tr> 
     <tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Ambiente]</p> </td> 
      <td> <p>Selecione se você está usando um ambiente de produção ou não produção.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Tipo]</p> </td> 
      <td> <p>Selecione se você está usando uma conta de serviço ou uma conta pessoal.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Host] </td> 
      <td> <p>Insira o nome de host do servidor FTP. Exemplo: <code>myftp123.server.com</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Porta] </td> 
      <td> <p>Insira o número da porta do servidor FTP. Exemplo: <code>21</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Nome de Usuário] </td> 
      <td> <p>Digite o nome de usuário da sua conta FTP.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Senha] </td> 
      <td> <p>Digite a senha da sua conta FTP.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Usar uma conexão segura (TLS)</p> </td> 
      <td> <p>Selecione se deseja usar uma conexão segura.</p> <ul><li><p><b>[!UICONTROL Não]</b></p> <p>A conexão não é segura.</p></li><li> <p><b>Criptografia explícita</b> ou <b>Criptografia implícita</b></p> <p>A conexão é protegida por SSL.</p> </td> 
     </tr> 
    <tr> 
   <td> <p>[!UICONTROL Rejeitar certificados não autorizados]</p> </td> 
   <td> <p>Habilite essa opção para verificar o certificado do servidor FTP. Se a verificação falhar, a conexão não será criada. Para ser aprovado na verificação, o certificado deve atender a um dos seguintes critérios:</p> 
    <ul> 
     <li>ser assinado por uma autoridade de certificação raiz</a></li> 
     <li>ser assinada por uma autoridade de certificação intermediária. Nesse caso, todos os certificados intermediários devem ser instalados no servidor FTP.</li> 
     <li>ser um Certificado Autoassinado fornecido no campo [!UICONTROL Self-signed certificate] (veja abaixo)</li> </ul>
     <p>Se essa opção estiver desativada, o certificado do servidor FTP não será verificado. Recomendamos não desativar a opção, pois ela torna a conexão insegura e representa um sério risco de segurança.</p></td>
    </tr> 
    <tr> 
     <td> <p>[!UICONTROL Certificado autoassinado]</p> </td> 
     <td> <p>Clique no botão <b>[!UICONTROL Extract]</b> para abrir a caixa de diálogo de carregamento.</p> <p>Faça upload do certificado para usar o TLS com seu certificado autoassinado. [!DNL Workfront Fusion] não retém nem armazena dados que você fornece, como arquivos e senhas. O arquivo e a senha são usados somente para extrair o certificado.</p> </td> 
    </tr> 
   </tbody> 
   </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## Módulos FTP e seus campos

* [Acionadores](#triggers)
* [Ações](#actions)

### Acionadores

#### [!UICONTROL Observar arquivos]

[!UICONTROL Arquivos de observação] é o único módulo de acionador para FTP. Monitora o conteúdo do arquivo da pasta selecionada. O disparador é executado quando um novo arquivo é adicionado à pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#create-a-connection" class="MCXref xref">[!UICONTROL Criar uma conexão] em um módulo FTP</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Pasta]</p> </td> 
   <td> <p>Selecione a pasta que deseja observar.</p> <p><b>Observação:</b> somente uma pasta por cenário é permitida. Subpastas são ignoradas.</p> <p><b>Dica:</b> Para observar várias pastas, crie um cenário separado para cada uma delas.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de arquivos retornados] </td> 
   <td> <p>Defina o número máximo de resultados com os quais você deseja que o módulo funcione durante um ciclo. Se o valor for definido como muito alto, a conexão pode ser interrompida no lado do servidor FTP. [!DNL Workfront Fusion] não tem nenhuma influência sobre isso. Recomendamos que você defina um valor mais baixo e defina um valor mais alto para o número máximo de ciclos ou execute o cenário com mais frequência.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Alterar permissões]](#change-permissions)
* [[!UICONTROL Criar uma pasta]](#create-a-folder)
* [[!UICONTROL Excluir um arquivo]](#delete-a-file)
* [[!UICONTROL Excluir uma pasta]](#delete-a-folder)
* [[!UICONTROL Obter um arquivo]](#get-a-file)
* [[!UICONTROL Lista de arquivos em uma pasta]](#list-of-files-in-a-folder)
* [[!UICONTROL Mover um arquivo ou uma pasta]](#move-a-file-or-folder)
* [[!UICONTROL Carregar] um arquivo](#upload-a-file)

#### [!UICONTROL Alterar permissões]

Este módulo de ação altera as configurações de permissão de um arquivo ou pasta.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Conexão]</td>
            <td>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#Create" class="MCXref xref" >[!UICONTROL Criar uma conexão] em um módulo FTP</a> neste artigo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Alterar configurações de permissão de]</td>
            <td>
               <p>Selecione se deseja alterar as configurações de um arquivo ou pasta.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL Caminho do arquivo]</td>
            <td>Insira ou mapeie o caminho do arquivo para a pasta ou o arquivo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Permissões]</td>
            <td>
               <p>Defina as permissões desejadas para arquivos ou pastas. Use os parâmetros chmod. Por exemplo: <code>777 </code>ou <code>-rwxrwxrwx</code>.</p>
               <p>As permissões devem corresponder ao padrão <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code>.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Criar uma pasta]

Este módulo de ação cria uma nova pasta.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Conexão]</td>
            <td>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#Create" class="MCXref xref" >[!UICONTROL Criar uma conexão] em um módulo FTP</a> neste artigo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Caminho da pasta]</td>
            <td>Insira ou mapeie o caminho do arquivo para a nova pasta.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Novo nome de pasta]</td>
            <td>
               <p>Insira ou mapeie um nome para a nova pasta.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Excluir um arquivo]

Este módulo de ação exclui um arquivo da pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
            <td>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#Create" class="MCXref xref" >[!UICONTROL Criar uma conexão] em um módulo FTP</a> neste artigo.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta FTP da qual deseja excluir um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nome do arquivo]</td> 
   <td> <p> Insira o nome do arquivo, incluindo a extensão do nome do arquivo. Exemplo: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma pasta]

Este módulo de ação exclui permanentemente a pasta especificada.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Conexão]</td>
            <td>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#Create" class="MCXref xref" >[!UICONTROL Criar uma conexão] em um módulo FTP</a> neste artigo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Pasta]</td>
            <td>
               <p>Selecione a pasta FTP da qual deseja excluir um arquivo.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Obter um arquivo]

Este módulo de ação recupera um arquivo do servidor FTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#creating-the-ftp-connection" class="MCXref xref">Criando a conexão FTP</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Caminho do arquivo]</td> 
   <td> <p> Insira o caminho do arquivo que deseja obter.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lista de arquivos em uma pasta]

Este módulo de ação recupera informações de arquivos e/ou pastas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#creating-the-ftp-connection" class="MCXref xref">Criando a conexão FTP</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta FTP na qual deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mostrar] </td> 
   <td> <p>Selecione se deseja recuperar informações sobre arquivos ou pastas, ou ambos.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar] </td> 
   <td> <p>Insira o termo de pesquisa. Se nenhum termo de pesquisa for inserido, todos os arquivos ou pastas da pasta especificada serão recuperados.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de arquivos retornados]</td> 
   <td> <p>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mover um arquivo ou uma pasta]

Este módulo de ação move um arquivo ou pasta para um local diferente.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Conexão]</td>
            <td>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#Create" class="MCXref xref" >[!UICONTROL Criar uma conexão] em um módulo FTP</a> neste artigo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Caminho de arquivo antigo]</td>
            <td>
               <p>Insira o caminho do qual deseja mover o arquivo. Exemplo: <code>/folder1/document.txt</code>.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL Novo caminho de arquivo]</td>
            <td>
               <p>Insira o caminho para o qual deseja mover o arquivo. Exemplo: <code>/folder2/document.txt</code>.</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Carregar um arquivo]

Faz upload de um arquivo para o servidor FTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td>Para obter instruções sobre como estabelecer uma conexão com a conta FTP, consulte <a href="#creating-the-ftp-connection" class="MCXref xref">Criando a conexão FTP</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta FTP na qual deseja fazer upload do arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL arquivo Source] </td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anexar a um arquivo já existente]</td> 
   <td> <p>Se essa opção estiver ativada e o arquivo já existir no servidor FTP, o conteúdo do arquivo será anexado ao arquivo existente. Se essa opção não estiver habilitada, o conteúdo do arquivo será substituído.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criar pastas se não existir] </td> 
   <td> <p>Se essa opção estiver ativada e a pasta inserida no campo Pasta não existir no servidor FTP, o módulo criará a pasta</p> </td> 
  </tr> 
 </tbody> 
</table>

## Solução de problemas {#troubleshooting}

Se tiver problemas com o aplicativo FTP durante a criação da conexão ou durante a operação de um módulo, tente usar um dos clientes FTP populares e tente executar a mesma ação (por exemplo, criar uma conexão ou listar arquivos em uma pasta). com o cliente FTP. Se você estiver tendo os mesmos problemas com o cliente FTP, o motivo pode ser uma configuração incorreta do servidor FTP.
