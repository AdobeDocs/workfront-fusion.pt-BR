---
title: Módulos do Veeva Vault
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Veeva Vault, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 2ef967b6-0a69-4801-8574-5f17c9ce991d
source-git-commit: d64d894cfb0e1905c135cdf5ea39f11cd7a6e5f2
workflow-type: tm+mt
source-wordcount: '4125'
ht-degree: 13%

---

# Módulos do Veeva Vault

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Veeva Vault, bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Para usar os módulos do Veeva Vault, você deve ter uma conta do Veeva Vault.

## Conectar o Veeva Vault ao Workfront Fusion

Você pode criar uma conexão com sua conta do Veeva Vault diretamente de dentro de um módulo do Veeva Vault.

Ao criar uma conexão, você pode selecionar se deseja usar uma senha ou se deseja usar a autenticação OAuth2.

### Conecte-se ao Veeva Vault usando um nome de usuário e senha

1. Em qualquer módulo do Veeva Vault, clique em **Adicionar** ao lado do campo Conexão.
1. No campo **Tipo de conexão**, selecione `Veeva Username Password`.
1. Preencha os campos a seguir.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">Nome da conexão</td> 
       <td> <p>Insira um nome para a conexão.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">Nome de usuário</td>
        <td>
          <p>Insira o nome de usuário da conta do Veeva Vault.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Senha</td>
        <td>
          <p>Digite a senha da conta do Veeva Vault.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">DNS do Vault</td> 
       <td>Insira seu DNS do Veeva Vault (nome de domínio).</p><p>Para localizar o DNS do Veeva Vault, examine o URL que você usa para acessar o Veeva Vault.</p>Por exemplo, na URL <code>https://my-dns.veevavault.com</code>, o DNS é <code>my-dns</code>. Não é necessário inserir o URL inteiro.</td> 
      </tr> 
     </tbody> 
    </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.

### Conectar-se ao Veeva Vault usando a autenticação OAuth2

1. Em qualquer módulo do Veeva Vault, clique em **Adicionar** ao lado do campo Conexão.
1. No campo **Tipo de conexão**, selecione `Veeva Oauth 2`.
1. Preencha os campos a seguir.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">Nome da conexão</td> 
       <td> <p>Insira um nome para a conexão.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader">Provedor de Servidor de Autorização</td> 
       <td> <p>Selecione o provedor que deseja usar para esta autenticação.</p> 
       <p><b>OBSERVAÇÃO:</b> O Veeva Vault usa credenciais de cliente do Azure AD quando o Azure é selecionado como o Provedor de Servidor de Autorização.</p>
       </td> 
      </tr> 
      <tr> 
       <td role="rowheader">Executar ping no host</td> 
       <td> <p>Se você estiver usando o PingFederate, insira o host do ping.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">Escopo</td>
        <td>
          <p>Insira o escopo desta conexão. O escopo deve ser formatado como <code>{Application ID URI}/.default</code>. O URI da ID do aplicativo deve pertencer ao recurso ou aplicativo que está expondo permissões.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">ID do inquilino</td>
        <td>
          <p>Se você estiver usando o Azure AD/Microsoft Entra ID para o seu provedor de servidor de autorização, insira a ID do locatário para esta conexão.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">ID do cliente</td>
        <td>
          <p>Insira a ID do cliente do aplicativo Veeva Vault que essa conexão usará.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Segredo do cliente</td>
        <td>
          <p>Insira o Segredo do cliente para o aplicativo Veeva Vault que essa conexão usará.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">ID do perfil</td>
        <td>
          <p>Insira a ID do seu perfil OAuth2 / Open ID Connect.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">DNS do Vault</td> 
       <td>Insira seu DNS do Veeva Vault (nome de domínio).</p><p>Para localizar o DNS do Veeva Vault, examine o URL que você usa para acessar o Veeva Vault.</p>Por exemplo, na URL <code>https://my-dns.veevavault.com</code>, o DNS é <code>my-dns.veevavault.com</code>. </td> 
      </tr> 
      <tr>
        <td role="rowheader">O tempo de expiração da sua sessão em minutos</td>
        <td>
          <p>Insira o tempo de expiração da sua sessão, em minutos.</p>
        </td>
      </tr>
     </tbody> 
    </table>

1. Clique em **[!UICONTROL Continuar]** para criar a conexão e voltar para o módulo.


## Módulos do Veeva Vault e seus campos

Ao configurar os módulos do Veeva Vault, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Veeva Vault podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Documento](#document)
* [Objeto](#object)
* [Extração de vários arquivos](#multi-file-extract)
* [Carregamento de vários arquivos](#multi-file-load)
* [Estágios de arquivo](#file-staging)
* [Outras](#other)

### Documento

* [Criar um único documento](#create-a-single-document)
* [Criar um relacionamento de documento único](#create-a-single-document-relationship)
* [Criar várias anotações](#create-multiple-annotations)
* [Criar vários documentos](#create-multiple-documents)
* [Criar vários relacionamentos de documento](#create-multiple-document-relationships)
* [Excluir um único documento](#delete-a-single-document)
* [Excluir um único relacionamento de documento](#delete-a-single-document-relationship)
* [Excluir várias anotações](#delete-multiple-annotations)
* [Excluir vários relacionamentos entre documentos](#delete-multiple-document-relationships)
* [Baixar um arquivo](#download-file)
* [Exportar documentos](#export-documents)
* [Obter um único documento](#get-a-single-document)
* [Obter anotações do documento](#get-document-annotations)
* [Obter relacionamentos entre documentos](#get-document-relationships)
* [Iniciar ação do usuário](#initiate-user-action)
* [Listar documentos](#list-documents)
* [Recuperar resultados da exportação de documentos](#retrieve-document-export-results)
* [Atualizar um único documento](#update-a-single-document)
* [Atualizar várias anotações](#update-multiple-annotations)
* [Atualizar vários documentos](#update-multiple-documents)

#### Criar um único documento

Este módulo cria um único documento, binder ou modelo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar um documento, um binder ou um modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Selecionar campos</p> </td> 
   <td> <p>Selecione os campos para os quais deseja inserir dados e, em seguida, insira os dados nesses campos.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar um relacionamento de documento único

Este módulo de ação cria uma relação entre dois documentos

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do Documento</p> </td> 
   <td> <p>Insira ou mapeie a ID do documento de onde deseja que o relacionamento se origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versão</p> </td> 
   <td> <p>Selecione ou mapeie a ID da versão para a qual você deseja criar uma relação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do documento de destino</p> </td> 
   <td> <p>Insira a ID do documento para o qual o relacionamento aponta.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Versão principal de destino</p> </td> 
   <td> <p>Insira a versão principal do documento de destino. Este é o número antes do ponto.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Versão secundária de destino</p> </td> 
   <td> <p>Insira a versão principal do documento de destino. Este é o número depois do ponto.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Tipo de relacionamento</p> </td> 
   <td> <p>Insira ou mapeie o tipo de relacionamento que deseja criar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Criar várias anotações

Esse módulo de ação permite criar até 500 anotações.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Anotações</p> </td> 
   <td> <p>Para cada anotação que você deseja adicionar, clique em <b>Adicionar item</b> e preencha os dados descritos em <a href="#annotation-fields" class="MCXref xref">Campos de anotação</a> neste artigo.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Campos de anotação

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tipo de anotação </td> 
   <td> <p>Selecione o tipo de anotação que deseja criar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Insira ou mapeie o tipo de marcador de posição que deseja usar para esta anotação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Número de páginas</p> </td> 
   <td> <p>Insira ou mapeie o número da página em que deseja que essa anotação apareça.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Coordenada X</p> </td> 
   <td> <p>Insira ou mapeie a coordenada X do marcador.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Coordenada Y</p> </td> 
   <td> <p>Insira ou mapeie a coordenada Y do marcador.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Largura</p> </td> 
   <td> <p>Insira ou mapeie a largura do marcador.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Altura</p> </td> 
   <td> <p>Insira ou mapeie a altura do marcador de posição.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Estilo</p> </td> 
   <td> <p>Insira ou mapeie o estilo do marcador de posição.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Referência</p> </td> 
   <td> <p>Uma referência permite que a anotação se refira a uma fonte externa. Para cada referência que você deseja adicionar à anotação, clique em <b>Adicionar item</b> e insira o tipo da referência, a ID da versão do documento e uma anotação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Selecionar campos</p> </td> 
   <td> <p>Selecione os campos para os quais deseja fornecer valores e insira os valores em cada campo. Os campos disponíveis dependem do tipo de anotação.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Criar vários documentos

Este módulo cria vários documentos ou modelos usando um arquivo CSV.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar modelos ou documentos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dados do arquivo</p> </td> 
   <td> <p>Mapeie o arquivo CSV que será usado para criar os documentos.</td> 
  </tr> 
 </tbody> 
</table>

#### Criar vários relacionamentos de documento

Esse módulo de ação configura vários relacionamentos de documentos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo de entrada</p> </td> 
   <td> <p>Selecione o tipo de entrada que você está fornecendo para criar esses relacionamentos.</p> <ul><li>CSV</li><li>JSON</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dados do arquivo</p> </td> 
   <td> <p>Se estiver usando um arquivo CSV, insira ou mapeie os dados do arquivo CSV.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dados de relacionamentos</p> </td> 
   <td> <p>Se você estiver usando JSON, para cada relação que deseja adicionar, clique em <b>Adicionar item</b> e preencha os dados descritos em <a href="#relationship-fields" class="MCXref xref">Campos de relação</a> neste artigo.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Campos de relacionamento

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">ID do documento do Source </td> 
   <td> <p>Insira ou mapeie a ID do documento de onde deseja que o relacionamento se origine.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Versão principal do Source</p> </td> 
   <td> <p>Informe a versão principal do documento de origem. Este é o número antes do ponto.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Versão secundária do Source</p> </td> 
   <td> <p>Informe a versão principal do documento de origem. Este é o número depois do ponto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do documento de destino</p> </td> 
   <td> <p>Insira a ID do documento para o qual o relacionamento aponta.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Versão principal de destino</p> </td> 
   <td> <p>Insira a versão principal do documento de destino. Este é o número antes do ponto.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Versão secundária de destino</p> </td> 
   <td> <p>Insira a versão principal do documento de destino. Este é o número depois do ponto.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Tipo de relacionamento</p> </td> 
   <td> <p>Insira ou mapeie o tipo de relacionamento que deseja criar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um único documento

Este módulo exclui um único documento, binder ou modelo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja excluir um documento, um binder ou um modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID do documento / ID do associador / Nome do modelo</p> </td> 
   <td> <p>Selecione o item que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um único relacionamento de documento

Este módulo de ação exclui uma relação de um documento

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do Documento</p> </td> 
   <td> <p>Informe ou mapeie a ID do documento de origem para o relacionamento que deseja deletar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versão</p> </td> 
   <td> <p>Selecione ou mapeie a ID da versão para a qual você deseja excluir uma relação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID do relacionamento</p> </td> 
   <td> <p>Insira ou mapeie a ID do relacionamento que deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir várias anotações

Esse módulo de ação exclui anotações. O usuário deve ter permissões para excluir anotações no Veeva Vault. É possível excluir até 500 anotações.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Anotações</p> </td> 
   <td> <p>Para cada anotação que você deseja excluir, clique em <b>Adicionar item</b> e insira os seguintes campos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID</p> </td> 
   <td> <p>Insira ou mapeie a ID da anotação que você deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID da versão do documento</p> </td> 
   <td> <p>Insira ou mapeie o número de versão do documento que contém a anotação que você deseja excluir.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir vários relacionamentos entre documentos

Este módulo de ação exclui relacionamentos de vários documentos

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo de entrada</p> </td> 
   <td> <p>Selecione o tipo de entrada que você está fornecendo para excluir esses relacionamentos.</p> <ul><li>CSV</li><li>JSON</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dados do arquivo</p> </td> 
   <td> <p>Se estiver usando um arquivo CSV, insira ou mapeie os dados do arquivo CSV.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dados de relacionamentos</p> </td> 
   <td> <p>Se você estiver usando JSON, para cada relação que deseja adicionar, clique em <b>Adicionar item</b> e insira a ID da relação.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Baixar arquivo

Este módulo baixa um documento, versão de documento ou modelo do Veeva Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja baixar um documento ou modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo de download</p> </td> 
   <td> <p>Selecione se deseja baixar um documento ou uma versão do documento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID do documento / Nome do modelo</p> </td> 
   <td> <p>Insira ou mapeie a ID do documento ou o nome do modelo que deseja baixar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Fazer check-out do documento</p> </td> 
   <td> <p>Se você estiver baixando um documento, ative essa opção para fazer check-out do documento antes de baixá-lo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versão</p> </td> 
   <td> <p>Se você estiver baixando uma versão do documento, selecione a versão a ser baixada.</td> 
  </tr> 
 </tbody> 
</table>

#### Exportar documentos

Este módulo exporta documentos que você especificar, incluindo origens, representações e texto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja excluir um documento, um binder ou um modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Origem</p> </td> 
   <td> <p>Habilite essa opção para incluir arquivos de origem na exportação.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Representações</p> </td> 
   <td> <p>Habilite essa opção para incluir arquivos de representação na exportação.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Todas as versões</p> </td> 
   <td> <p>Habilite esta opção para incluir todas as versões dos arquivos de documento na exportação.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Texto</p> </td> 
   <td> <p>Habilite esta opção para incluir o texto do documento de origem na exportação.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Obter um único documento

Este módulo recupera metadados para um único documento, binder ou modelo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja recuperar dados de um documento, binder ou modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID do documento / ID do associador / Nome do modelo</p> </td> 
   <td> <p>Selecione os campos para os quais deseja recuperar dados.</td> 
  </tr> 
 </tbody> 
</table>

#### Obter anotações do documento

Este módulo recupera anotações de uma versão específica do documento. Você pode recuperar todas as anotações ou optar por recuperar apenas determinados tipos de anotação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do Documento</p> </td> 
   <td> <p>Selecione ou mapeie o documento para o qual deseja recuperar anotações. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versão</p> </td> 
   <td> <p>Selecione ou mapeie a ID da versão para a qual você deseja recuperar anotações.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de anotações retornadas</td> 
   <td>Insira ou mapeie o número máximo de anotações que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### Obter relacionamentos entre documentos

Este módulo recupera todos os relacionamentos de um documento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do Documento</p> </td> 
   <td> <p>Selecione ou mapeie o documento para o qual deseja recuperar relacionamentos. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versão</p> </td> 
   <td> <p>Selecione ou mapeie a ID da versão para a qual você deseja recuperar os relacionamentos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de relações retornadas</td> 
   <td>Insira ou mapeie o número máximo de relacionamentos que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### Iniciar ação do usuário

Este módulo inicia ações em documentos e binders, como enviar um documento para revisão ou alterar seu estado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se você deseja executar uma ação em um documento ou um binder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Documento / Fichário</p> </td> 
   <td> <p>Selecione o documento ou o binder no qual deseja executar a ação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versão do documento/Versão do fichário</p> </td> 
   <td> <p>Selecione o documento ou o binder no qual deseja executar a ação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Ação</p> </td> 
   <td> <p>Selecione a ação a ser executada no documento ou binder.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar documentos

Este módulo lista todos os documentos do tipo selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja listar documentos, binders ou modelos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### Recuperar resultados da exportação de documentos

Este módulo retorna os resultados de uma exportação de documento solicitada anteriormente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do trabalho</p> </td> 
   <td> <p>Insira ou mapeie a ID do trabalho para o qual deseja retornar resultados. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Atualizar várias anotações

Esse módulo de ação atualiza até 500 anotações.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Anotações</p> </td> 
   <td> <p>Para cada anotação que você deseja atualizar, clique em <b>Adicionar item</b> e preencha os dados descritos em <a href="#annotation-fields" class="MCXref xref">Campos de anotação</a> neste artigo.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### Atualizar vários documentos

Este módulo atualiza vários documentos ou modelos usando um arquivo CSV.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar modelos ou documentos</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dados do arquivo</p> </td> 
   <td> <p>Mapeie o arquivo CSV que será usado para criar os documentos.</td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um único documento

Este módulo atualiza um único documento, binder ou modelo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar um documento, uma versão do documento, um binder ou um modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID / Nome</p> </td> 
   <td> <p>Se você estiver atualizando um modelo, digite um novo nome para ele.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Nome do novo modelo</p> </td> 
   <td> <p>Insira ou mapeie a ID ou o nome do objeto que você deseja atualizar.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Selecionar campos</p> </td> 
   <td> <p>Selecione os campos para os quais deseja inserir dados e, em seguida, insira os dados nesses campos.</td> 
  </tr> 
 </tbody> 
</table>

### Objeto

* [Criar um único registro de objeto](#create-a-single-object-record)
* [Excluir um único registro de objeto](#delete-a-single-object-record)
* [Obter um único objeto](#get-a-single-object)
* [Listar registros de objetos](#list-objects-records)
* [Atualizar um único registro de objeto](#update-a-single-object-record)

#### Criar um único registro de objeto

Este módulo cria, copia ou copia profundas de um único registro de objeto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar ou copiar um registro ou se deseja fazer uma cópia profunda de um registro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Modo de migração</td> 
   <td>Se estiver criando ou copiando um registro, habilite essa opção para criar ou atualizar registros de objeto em um estado não inicial e com validação mínima, criar registros inativos e definir campos padrão e gerenciados pelo sistema, como <code>createdby_v</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nenhum acionador</td> 
   <td>Se definido como verdadeiro e o modo de migração estiver ativado, o módulo ignorará todos os acionadores do SDK padrão, personalizados e do sistema e Acionadores de ação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do objeto</td> 
   <td>Insira ou mapeie o valor do campo nome do objeto__v, como <code>product__v</code>, <code>country__v</code> ou <code>custom_object__c</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do registro</td> 
   <td>Se você estiver copiando um registro em profundidade, selecione o registro a ser copiado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Campos de registro</td> 
   <td>Se você estiver copiando um registro em profundidade, selecione os campos para os quais deseja fornecer valores e, em seguida, forneça esses valores.</td> 
  </tr> 
 </tbody> 
</table>

#### Excluir um único registro de objeto

Este módulo exclui ou exclui em cascata um único registro de objeto. A exclusão em cascata de um registro exclui o registro e todos os seus objetos filho.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja excluir um registro ou excluir um registro em cascata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do objeto</td> 
   <td>Selecione o objeto que deseja deletar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do registro</td> 
   <td>Selecione a ID do registro que deseja excluir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID externa</td> 
   <td>Em vez da ID de registro, você pode usar essa ID externa de documento definida pelo usuário.</td> 
  </tr> 
 </tbody> 
</table>

#### Obter um único objeto

Esse módulo recupera metadados configurados em um registro de objeto específico no Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do objeto</td> 
   <td>Selecione o objeto para o qual deseja recuperar metadados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do registro</td> 
   <td>Selecione a ID do registro para o qual deseja recuperar metadados.</td> 
  </tr> 
 </tbody> 
</table>

#### Listar registros de objetos

Este módulo recupera todos os objetos do Vault no Vault autenticado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Recuperar rótulos localizados</p> </td> 
   <td> <p>Selecione Sim para recuperar strings localizadas (traduzidas) para os campos label e label_plural.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Update a single object record-->

Este módulo atualiza campos em um registro de objeto existente.

Este módulo cria, copia ou copia profundas de um único registro de objeto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar ou copiar um registro ou se deseja fazer uma cópia profunda de um registro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Modo de migração</td> 
   <td>Habilite esta opção para criar ou atualizar registros de objeto em um estado não inicial e com validação mínima, criar registros inativos e definir campos padrão e gerenciados pelo sistema como <code>createdby_v</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nenhum acionador</td> 
   <td>Se o modo de migração estiver ativado, é possível ativar essa opção para ignorar todos os acionadores padrão e personalizados do SDK e Acionadores de ação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do objeto</td> 
   <td>Insira ou mapeie o valor do campo nome do objeto__v, como <code>product__v</code>, <code>country__v</code> ou <code>custom_object__c</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do registro</td> 
   <td>Selecione a ID do registro a ser atualizado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Estado</td> 
   <td>Especifique o estado do ciclo de vida do registro quando <code>X-VaultAPI-MigrationMode</code> estiver definido como verdadeiro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Rótulo de estado</td> 
   <td>Especifique o tipo de estado do ciclo de vida do registro quando <code>X-VaultAPI-MigrationMode</code> estiver definido como verdadeiro. Use o formato <code>base:object_lifecycle:</code> seguido pelo tipo de estado do objeto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Campos de registro</td> 
   <td>Se você estiver copiando um registro em profundidade, selecione os campos para os quais deseja fornecer valores e, em seguida, forneça esses valores.</td> 
  </tr> 
 </tbody> 
</table>

### Extração de vários arquivos

* [Extrair vários arquivos](#extract-multiple-files)
* [Recuperar resultados de extração](#retrieve-extract-results)

#### Extrair vários arquivos

Esse módulo de ação cria um trabalho de carregamento para extrair um ou mais arquivos de dados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Arquivos de dados</td> 
   <td>Para cada arquivo que você deseja extrair, clique em <b>Adicionar item</b> e insira o seguinte:
   <ul>
   <li>Tipo de objeto</li>
   <li>Critérios de VQL (Opcional): para filtrar o conjunto de dados de modo a incluir somente arquivos que atendam a critérios específicos, insira os critérios em Idioma de Consulta do Vault (VQL).</li>
   </ul>
    </td> 
  </tr> 
 </tbody> 
</table>

#### Recuperar resultados de extração

Este módulo de ação recupera os resultados de uma solicitação de extração especificada.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do trabalho</p> </td> 
   <td> <p>Informe ou mapeie o job cujos resultados você deseja recuperar. Você pode mapear isso no módulo Extrair arquivos de dados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da Tarefa</td> 
   <td> <p>Insira ou mapeie a tarefa para a qual deseja recuperar os resultados. Você pode mapear isso no módulo Extrair arquivos de dados.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Carregamento de vários arquivos

* [Carregar vários arquivos](#load-multiple-files)
* [Recuperar resultados do log](#retrieve-log-results)

#### Carregar vários arquivos

Esse módulo cria um trabalho do carregador e carrega um conjunto de arquivos de dados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Arquivo</td> 
   <td>Insira ou mapeie o caminho do arquivo para o arquivo CSV que esse trabalho usará.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordem</td> 
   <td>Insira ou mapeie a ordem para a lista de arquivos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nenhum acionador</td> 
   <td>Selecione Sim para ignorar disparadores de registros ou documentos.</td> 
  </tr> 
 </tbody> 
</table>

#### Recuperar resultados do log

Este módulo de ação recupera um log de resultados do trabalho do carregador.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID do trabalho</p> </td> 
   <td> <p>Informe ou mapeie o job cujos resultados você deseja recuperar. Você pode mapear isso no módulo Carregar arquivos de dados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da Tarefa</td> 
   <td> <p>Insira ou mapeie a tarefa para a qual deseja recuperar os resultados. Você pode mapear isso no módulo Carregar arquivos de dados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo</td> 
   <td> <p>Selecione se deseja recuperar jobs bem-sucedidos ou com falha.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Estágios de arquivo

#### Listar itens no caminho

Este módulo retorna uma lista de arquivos e pastas para o caminho especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Escolha seu diretório inicial</td> 
   <td>Selecione o diretório base do qual deseja listar os itens.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordem</td> 
   <td>Insira ou mapeie a ordem para a lista de arquivos.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nenhum acionador</td> 
   <td>Selecione Sim para ignorar disparadores de registros ou documentos.</td> 
  </tr> 
 </tbody> 
</table>

### Outras

* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Criar uma consulta VQL](#make-a-vql-query)
* [Ler logs](#read-logs)

#### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada personalizada para a API do Veeva Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Insira um caminho relativo a <code>baseurl/api/v</code>.  Por exemplo: <code>/objects/documents</code>. Não inclua <code>baseurl/api/v/</code>, pois ele já está incluído.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Método</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cabeçalhos</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">String de consulta</td> 
   <td> <p>Adicione a consulta para a chamada de API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Criar uma consulta VQL

Esse módulo faz uma consulta usando o VQL (Vault Query Language).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selecione se deseja criar modelos ou documentos</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dados do arquivo</p> </td> 
   <td> <p>Mapeie o arquivo CSV que será usado para criar os documentos.</td> 
  </tr> 
 </tbody> 
</table>

#### Ler logs

Este módulo retorna dados de trilhas de auditoria

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Veeva Vault ao Workfront Fusion, consulte <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Conectar o Veeva Vault ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo de auditoria</p> </td> 
   <td> <p>Selecione o tipo de auditoria para o qual deseja recuperar dados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data inicial</p> </td> 
   <td> <p>Informe ou mapeie a data inicial das auditorias que deseja recuperar.</p><p>Para obter uma lista de formatos de data e hora compatíveis, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data final</p> </td> 
   <td> <p>Informe ou mapeie a data final das auditorias que deseja recuperar.</p><p>Para obter uma lista de formatos de data e hora compatíveis, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL de resultado </p> </td> 
   <td> <p>Selecione CSV se desejar obter o URL para baixar um CSV do resultado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Número máximo de resultados retornados</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>
