---
title: Módulos do Adobe Experience Manager Assets
description: Com o conector do Adobe Experience Manager Assets para Adobe Workfront Fusion, é possível criar, fazer upload e atualizar ativos, além de copiar ou mover pastas e ativos.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: tm+mt
source-wordcount: '3734'
ht-degree: 2%

---

# Módulos do Adobe Experience Manager Assets

Com o conector do Adobe Experience Manager Assets para Adobe Workfront Fusion, é possível criar, fazer upload e atualizar ativos, além de copiar ou mover pastas e ativos.

Para obter uma introdução ao vídeo sobre o conector do Adobe Experience Manager Assets, consulte:

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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

## Pré-requisitos

* Você deve ter uma conta do Adobe Experience Manager Assets para usar esses módulos.
* Você deve configurar o fluxo de servidor para servidor no console do Adobe Developer.

  Para obter instruções sobre como configurar o fluxo de servidor para servidor no console do Adobe Developer, consulte [Gerando tokens de acesso para APIs do lado do servidor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=pt-BR#the-server-to-server-flow).
* Sua conta técnica do Adobe Experience Manager deve ter permissões de gravação.

  Para obter instruções sobre como adicionar permissões de gravação à sua conta técnica da Adobe Experience Manager, consulte [Credenciais de serviço](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) na documentação da Adobe Experience Manager.

## Informações da API do Adobe Experience Manager Assets

O conector do Adobe Experience Manager Assets usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o Adobe Experience Manager Assets ao Workfront Fusion {#connect-adobe-experience-manager-assets-to-workfront-fusion}

Para criar uma conexão para os módulos do Adobe Experience Manager Assets:

1. Clique em Adicionar ao lado da caixa Conexão.

2. Selecione o tipo de conexão que você está criando:

   * **AEM Assets as a Cloud Service**

     Essa configuração requer informações da Adobe Admin Console.

   * **AEM Assets Basic (Adobe Managed Services)**

     Esta configuração requer um nome de usuário e senha.

3. Preencha os campos para o tipo de conexão que você está criando.

   Para o AEM Assets as a Cloud Service, consulte [Configurar a conexão para o AEM Assets as a Cloud Service](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   Para o AEM Assets Basic (Adobe Managed Services), consulte [Configurar a conexão para o AEM Assets Basic](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Clique em **Continuar** para salvar a conexão e retornar ao módulo.


### Configurar a conexão para o AEM Assets as a Cloud Service

>[!NOTE]
>
>* As informações desses campos são geradas como parte da configuração do fluxo de servidor para servidor no Adobe Developer Console. Você pode encontrar esses valores no arquivo JSON de credenciais de serviço gerado como parte dessa configuração.
>
>   Para obter instruções sobre como configurar o fluxo de servidor para servidor no Adobe Developer Console, consulte [Gerando tokens de acesso para APIs do lado do servidor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=pt-BR#the-server-to-server-flow).
>
>* Sua conta técnica do Adobe Experience Manager deve ter permissões de gravação.
>
>   Para obter instruções sobre como adicionar permissões de gravação à sua conta técnica da Adobe Experience Manager, consulte [Credenciais de serviço](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) na documentação da Adobe Experience Manager.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">Nome da conexão</td>
                  <td>
                      <p>Insira um nome para esta conexão.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">URL da instância sem uma barra à direita</td>
                  <td>Insira o URL da sua instância do Adobe Experience Manager. Não inclua uma barra <code>/</code> ao final da URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">Opções de preenchimento dos detalhes da conta</td>
                  <td>Selecione se deseja fornecer JSON descrevendo os detalhes da conta ou se deseja inserir os detalhes manualmente.</td>
              </tr>
              <tr>
                  <td role="rowheader">Detalhes técnicos da conta no formato JSON</td>
                  <td>Se estiver fornecendo JSON, insira ou cole o JSON que descreve os detalhes da sua conta.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID do cliente</td>
                  <td>Se estiver inserindo detalhes manualmente, insira a ID do cliente gerada na configuração de servidor para servidor.</td>
              </tr>
              <tr>
                  <td role="rowheader">Segredo do cliente</td>
                  <td>Se estiver inserindo detalhes manualmente, insira o Segredo do cliente gerado na configuração de Servidor para Servidor.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID da conta técnica</td>
                  <td>Se inserir detalhes manualmente, insira a ID da conta técnica. Este é o campo "id" no arquivo JSON de credenciais do cliente.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID da organização</td>
                  <td class="">Se você inserir detalhes manualmente, insira a ID da organização. Este é o campo "org" no arquivo JSON de credenciais do cliente.</td>
              </tr>
              <tr>
                  <td role="rowheader">Escopos do Meta</td>
                  <td>Insira os escopos do Meta gerados na configuração de servidor para servidor.</td>
              </tr>
              <tr>
                  <td role="rowheader">Chave privada</td>
                  <td>Insira a chave privada gerada na configuração de servidor para servidor. Para extrair a chave privada, clique em Extract (Extrair) e, em seguida, insira o arquivo a ser extraído e a senha do arquivo.</td>
              </tr>
              <tr>
                  <td role="rowheader">URL de autenticação</td>
                  <td>Digite a URL de autenticação desta conta.</td>
              </tr>
          </tbody>
      </table>


### Configurar a conexão para o AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">Nome da conexão</td>
                <td>
                    <p>Insira um nome para esta conexão.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">URL da instância sem uma barra à direita</td>
                <td>Insira o URL da sua instância do Adobe Experience Manager. Não inclua uma barra <code>/</code> ao final da URL.</td>
            </tr>
            <tr>
                <td role="rowheader">Nome de usuário</td>
                <td>Insira o nome de usuário da conta do AEM Assets que essa conexão usa.</td>
            </tr>
            <tr>
                <td role="rowheader">Senha</td>
                <td>Digite a senha da conta do AEM Assets que essa conexão usa.</td>
            </tr>
        </tbody>
    </table>


## Módulos do Adobe Experience Manager Assets e seus campos

Ao configurar módulos do Adobe Experience Manager Assets, o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos adicionais do Adobe Experience Manager Assets podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Operações de arquivos](#files-operations)
* [Outras](#other)
* [Assets (API do autor)](#assets-author-api)
* [Eventos (API do autor)](#events-author-api)
* [Metadados (API do autor)](#metadata-author-api)
* [Importar (API do autor)](#import-author-api)
* [Relações (API do autor)](#relations-author-api)
* [Pastas (API Pastas)](#folders-folders-api)

### Operações de arquivos

* [Carregamento completo](#complete-upload)
* [Obter armazenamento pré-assinado](#get-presigned-storage)
* [Iniciar upload](#initiate-upload)
* [Fazer upload de um ativo](#upload-an-asset)

#### Carregamento completo

Esse módulo de ação conclui um upload iniciado depois que todas as partes do arquivo são carregadas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do arquivo</td> 
   <td> <p>Insira ou mapeie um nome para o arquivo carregado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Carregar token</td> 
   <td>Insira ou mapeie o token de upload para o binário, conforme fornecido pela iniciação.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo MIME</td> 
   <td>Insira ou mapeie o tipo de MIME para o arquivo concluído.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URI completo</td> 
   <td>Insira ou mapeie o URI completo do arquivo.</td> 
  </tr> 
 </tbody> 
</table>


#### Obter armazenamento pré-assinado

Esse módulo de ação cria um URL pré-assinado temporário para carregar ou baixar arquivos do AEM com segurança, sem exigir credenciais diretas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de pesquisa</td> 
   <td> <p>Selecione se deseja pesquisar o ativo pelo caminho ou pela ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ativo</td> 
   <td>Selecione o caminho para o ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>Insira ou mapeie o UDID do ativo.</td> 
  </tr> 
 </tbody> 
</table>

#### Iniciar upload

Este módulo de ação inicia um upload.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destino</td> 
   <td> <p>Selecione a pasta na qual deseja fazer upload de um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome do arquivo</td> 
   <td> <p>Insira ou mapeie um nome para o arquivo carregado</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tamanho máximo do arquivo</td> 
   <td>Insira ou mapeie o tamanho, em bytes, do arquivo carregado.</td> 
  </tr> 
 </tbody> 
</table>


#### Fazer upload de um ativo

Esse módulo de ação faz upload de um ativo para sua conta da Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destino</td> 
   <td> <p>Selecione a pasta na qual deseja fazer upload de um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Arquivo Source</td> 
   <td>Insira ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
 </tbody> 
</table>

### Outras


* [Copiar uma pasta ou um ativo](#copy-a-folder-or-asset)
* [Criar um registro](#create-a-record)
* [Excluir uma pasta, ativo ou representação](#delete-a-folder-asset-or-rendition)
* [Obter uma lista de pastas](#get-a-folder-listing)
* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Mover uma pasta ou um ativo](#move-a-folder-or-asset)
* [Atualizar um registro](#update-a-record)



#### Copiar uma pasta ou um ativo

Este módulo de ação copia uma pasta ou um ativo para outro local em sua conta da Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione se deseja copiar uma pasta ou um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pasta/ativo</td> 
   <td>Selecione ou mapeie a pasta ou o ativo que deseja copiar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Caminho de destino</td> 
   <td>Selecione ou mapeie o caminho para o local da nova pasta ou ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome da pasta/ativo copiado</td> 
   <td>Insira um nome para a nova pasta ou ativo. O nome da pasta exibido no Adobe Experience Manager Assets é igual ao nome original. O nome inserido aqui aparece no URL da nova pasta ou ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Copiar secundário</td> 
   <td>Se estiver copiando uma pasta, ative essa opção para copiar quaisquer subpastas ou ativos dentro da pasta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Substituir</td> 
   <td>Habilite essa opção para substituir qualquer pasta ou ativo no local de destino que tenha o mesmo nome da pasta ou do ativo que está sendo copiado.</td> 
  </tr> 
 </tbody> 
</table>



#### Criar um registro

Esse módulo de ação cria uma pasta ou um comentário de ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de objeto</td> 
   <td> <p>Selecione se deseja criar uma pasta ou um comentário em um ativo.</p> 
    <ul> 
     <li> <p>Pasta</p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p>Nome</p> <p>Insira um nome para a pasta. Esse nome aparecerá no caminho do arquivo, portanto, não deve incluir espaços ou outros caracteres. </p> </li> 
       <li> <p>Título</p> <p>Insira um título para a pasta, que pode ser exibido em vez do nome.</p> </li> 
      </ul> </li> 
     <li> <p>Comentário do ativo</p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p>Seleção de ativos</p> <p>Selecione ou mapeie a ID do ativo ao qual deseja adicionar um comentário.</p> </li> 
       <li> <p>Comentário</p> <p>Insira o texto do comentário.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Excluir uma pasta, ativo ou representação

Este módulo de ação exclui uma pasta, ativo ou representação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione se deseja excluir uma pasta, ativo ou representação.</p> 
    <ul> 
     <li> <p>Pasta</p> <p>Selecione a pasta a ser excluída selecionando as pastas em seu caminho.</p> </li> 
     <li> <p>Ativo</p> <p>Selecione o ativo, selecionando as pastas em seu caminho e, em seguida, o ativo que deseja excluir.</p> </li> 
     <li> <p>Representação</p> <p>Selecione a representação selecionando as pastas em seu caminho.</p> <p>Insira ou mapeie o nome da representação.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Obter uma lista de pastas

Este módulo de ação recupera uma representação de uma pasta existente e de suas entidades filhas (pastas ou ativos).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pasta</td> 
   <td>Selecione ou mapeie a pasta que deseja recuperar. Para adicionar subpastas ao caminho, clique no ícone de adição e selecione a subpasta.</td> 
  </tr> 
 </tbody> 
</table>

#### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada de API personalizada para a API do Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>Insira um caminho relativo ao URL base do Adobe Experience Manager.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Método</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cabeçalhos</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p> O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sequência de consulta</td> 
   <td> <p>Insira a string de consulta da solicitação. Para cada par Chave/Valor, clique em <b>Adicionar item</b> e insira a Chave e o Valor.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Mover uma pasta ou um ativo

Este módulo de ação move o ativo ou pasta no caminho fornecido para um novo local.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione se deseja mover uma pasta ou um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pasta/ativo</td> 
   <td>Selecione ou mapeie a pasta ou o ativo que deseja mover.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Caminho de destino</td> 
   <td>Selecione ou mapeie o caminho para o local para o qual deseja mover a pasta ou ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome da pasta/ativo movido</td> 
   <td>Insira um novo nome para a pasta ou o ativo movido. O nome da pasta exibido no Adobe Experience Manager Assets é igual ao nome original. O nome inserido aqui aparece no URL da pasta ou do ativo movido.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Substituir</td> 
   <td>Habilite essa opção para substituir qualquer pasta ou ativo no local de destino que tenha o mesmo nome da pasta ou do ativo que está sendo movido.</td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar um registro

Este módulo de ação atualiza um registro existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de registro</td> 
   <td> <p>Selecione se deseja excluir metadados de ativos ou uma representação de ativos.</p> 
    <ul> 
     <li> <p>Metadados do ativo</p> 
      <ul> 
       <li> <p>Selecione o ativo para o qual deseja atualizar metadados.</p> </li> 
       <li> <p>Insira o novo título do ativo.</p> </li> 
      </ul> </li> 
     <li> <p>Representação do ativo</p> 
      <ul> 
       <li> <p>Selecione o ativo para o qual deseja atualizar a representação.</p> </li> 
       <li> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Assets (API do autor)

* [Excluir ativo](#delete-asset)
* [Obter status do trabalho](#get-job-status)

#### Excluir ativo

Este módulo de ação exclui um único ativo por sua ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do ativo</td> 
   <td> <p>Insira ou mapeie a ID do ativo que deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Forçar</td> 
   <td>Ative essa opção para forçar a exclusão do ativo, mesmo que ele seja referenciado.</td> 
  </tr> 
 </tbody> 
</table>

#### Obter status do trabalho

Este módulo de ação obtém o status atual de um trabalho assíncrono.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da tarefa</td> 
   <td> <p>Insira ou mapeie a ID do trabalho para o qual você deseja obter o status.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Eventos (API do autor)

#### Assistir a eventos

Esse módulo de acionamento inicia um cenário quando um evento ocorre no AEM Assets.

O módulo contém um único campo: Webhook. Selecione um webhook existente para usar para esses eventos ou crie um novo.

Para criar um novo webhook:

1. Clique em **Adicionar** ao lado do campo Webhook.
1. Preencha os seguintes campos:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">Nome do Webhook</td>
        <td>Insira um nome para este webhook.</td>
       </tr>
       <tr>
         <td role="rowheader">Conexão</td>
        <td>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</td>
       </tr>
     </tbody>
   </table>

1. Clique em Salvar para salvar o webhook e retornar ao módulo.


### Metadados (API do autor)

* [Obter metadados de ativos](#get-asset-metadata)
* [Atualizar metadados de ativos](#update-asset-metadata)

#### Obter metadados de ativos

Este módulo de ação recupera metadados sobre o ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do ativo</td> 
   <td> <p>Insira ou mapeie a ID do ativo para o qual deseja obter os metadados.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Atualizar metadados de ativos

Esse módulo de ação atualiza os metadados do ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do ativo</td> 
   <td> <p>Insira ou mapeie a ID do ativo para o qual deseja atualizar os metadados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Atualizações</td> 
   <td> <p>Para cada item de metadados que você deseja atualizar, clique em <b>Adicionar item</b> e selecione a operação. Outros campos na caixa Adicionar item dependem da operação selecionada.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Importar (API do autor)

* [Obter resultados do trabalho de importação](#get-import-job-results)
* [Obter status do trabalho de importação](#get-import-job-status)
* [Fazer upload de um ativo de um URL](#upload-an-asset-from-a-url)

#### Obter resultados do trabalho de importação

Este módulo de ação recupera resultados para o trabalho de importação especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Importar ID do trabalho</td> 
   <td> <p>Informe ou mapeie a ID do job para o qual deseja recuperar os resultados.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obter status do trabalho de importação

Este módulo de ação recupera o status do trabalho de importação especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Importar ID do trabalho</td> 
   <td> <p>Informe ou mapeie a ID do job do qual deseja recuperar o status.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Fazer upload de um ativo de um URL

Este módulo de ação faz upload de um novo ativo importando arquivos dos URLs especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Título</td> 
   <td> <p>Insira ou mapeie um título para o ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Descrição</td> 
   <td> <p>Insira ou mapeie uma descrição para o ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Assunto</td> 
   <td> <p>Insira ou mapeie um assunto para o ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Criador</td> 
   <td> <p>Insira ou mapeie o criador do ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Data de expiração</td> 
   <td> <p>Insira ou mapeie a data de expiração do ativo.</p><p>Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Metadados personalizados</td> 
   <td> <p>Para cada item de metadados personalizados que você deseja adicionar ao ativo, clique em <b>Adicionar item</b> e insira o nome e o valor dos metadados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Caminho ou ID da pasta</td> 
   <td> <p>Selecione se deseja especificar a pasta de destino pelo caminho ou ID e, em seguida, selecione o caminho ou insira a ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Arquivos a serem importados</td> 
   <td> <p>Para cada arquivo que você deseja importar, clique em <b>Adicionar item&lt;/&gt; e preencha os detalhes do arquivo. <code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### Relações (API do autor)

* [Criar relações de ativos](#create-asset-relations)
* [Excluir relação de ativo](#create-asset-relations)
* [Obter tipos de relação de ativos](#get-asset-relation-types)
* [Obter relações de ativos](#get-asset-relations)

#### Criar relações de ativos

Esse módulo de ação cria novas relações de ativos para o ativo selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do ativo</td> 
   <td> <p>Insira ou mapeie o ativo de ID ao qual você deseja relacionar outros ativos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ativos relacionados</td> 
   <td> <p>Para cada ativo que você deseja relacionar ao ativo selecionado, clique em <b>Adicionar item</b> e insira ou mapeie a ID do ativo e o tipo de relação.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Excluir relação de ativo

Esse módulo de ação exclui uma relação de ativo para um ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do ativo</td> 
   <td> <p>Insira ou mapeie o ativo de ID do qual você deseja excluir uma relação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ativos relacionados</td> 
   <td> <p>Informe ou mapeie o tipo de relação que deseja deletar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Forneça a ID específica do ativo relacionado que será excluído</td> 
   <td> <p>Marque essa caixa se desejar deletar uma relação específica. Se essa caixa não estiver marcada, todas as relações do tipo selecionado serão excluídas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ativo relacionado</td> 
   <td> <p>Se você estiver deletando uma relação específica, informe ou mapeie a ID da relação que deseja deletar.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Obter tipos de relação de ativos

Este módulo lista os tipos de relação do ativo que existem para o ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do ativo</td> 
   <td> <p>Insira ou mapeie o ativo de ID para o qual você deseja listar os tipos de relação.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obter relações de ativos

Este módulo lista as relações de ativos para o ativo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do ativo</td> 
   <td> <p>Insira ou mapeie o ativo de ID para o qual você deseja listar relações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipos de relação</td> 
   <td> <p>Insira ou mapeie uma lista separada por vírgulas dos tipos de relações para os quais você deseja listar as relações.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Pastas (API Pastas)

* [Criar pastas](#create-folders)
* [Excluir uma pasta por ID](#delete-a-folder-by-id)
* [Excluir pastas por caminho](#delete-folders-by-path)
* [Obter resultados do trabalho de pastas](#get-folders-job-results)
* [Obter status do trabalho das pastas](#get-folders-job-status)
* [Listar pastas](#list-folders)

#### Criar pastas

Este módulo de ação cria uma nova pasta no Adobe Experience Manager Assets.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pastas para criar</td> 
   <td> <p>Para cada pasta que você deseja criar, clique em <b>Adicionar item</b> e insira as seguintes informações:</p>
   <ul>
   <li><b>Novo local da pasta</b><p>Selecione o caminho para o local onde deseja criar a nova pasta.</p></li>
       <li> <b>Nome</b> <p>Insira um nome para a pasta. Esse nome aparecerá no caminho do arquivo, portanto, não deve incluir espaços ou outros caracteres. </p> </li> 
       <li> <b>Title</b> <p>Insira um título para a pasta, que pode ser exibido em vez do nome.</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Excluir uma pasta por ID

Esse módulo de ação exclui a pasta Adobe Experience Manager Assets com a ID especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da Pasta</td> 
   <td> Insira ou mapeie a ID da pasta que deseja excluir.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Excluir subpastas</td> 
   <td> Ative essa opção para excluir a pasta e todas as suas subpastas.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Forçar</td> 
   <td> Habilite essa opção para forçar a exclusão de pastas, mesmo que ela seja mencionada.</td>
  </tr> 
 </tbody> 
</table>

#### Excluir pastas por caminho

Esse módulo de ação exclui as pastas do Adobe Experience Manager Assets nos caminhos especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Caminhos de pasta</td> 
   <td>Para cada pasta que você deseja excluir, clique em <b>Adicionar item</b> e selecione o caminho da pasta.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Excluir subpastas</td> 
   <td> Ative essa opção para excluir a pasta e todas as suas subpastas.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Forçar</td> 
   <td> Ative essa opção para forçar a exclusão do ativo, mesmo que ele seja referenciado.</td>
  </tr> 
 </tbody> 
</table>

#### Obter resultados do trabalho de pastas

Este módulo recupera os resultados de um trabalho assíncrono criado pela API da pasta do Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da tarefa</td> 
   <td> Informe ou mapeie a ID do job para o qual deseja recuperar os resultados.</td>
  </tr> 
 </tbody> 
</table>

#### Obter status do trabalho das pastas

Este módulo recupera o status de um trabalho assíncrono criado pela API da pasta do Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID da tarefa</td> 
   <td> Informe ou mapeie a ID do job para o qual deseja recuperar o status.</td>
  </tr> 
 </tbody> 
</table>


#### Listar pastas

Este módulo lista as subpastas da pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do Adobe Experience Manager Assets ao Workfront Fusion, consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar o Adobe Experience Manager Assets ao Workfront Fusion</a> neste artigo.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Caminho ou ID da pasta</td> 
   <td> <p>Selecione se deseja especificar a pasta de destino pelo caminho ou ID e, em seguida, selecione o caminho ou insira a ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
i! I added a lot of modules to the AEM Assets connector and we need new documentation for them. The connector is available in the QA environment. Heres the added modules and a brief description of them, more info about them can be found in the Assets Author Api docs and the Folders Api docs. Im not fully confident that i kept all the best practices for naming things :sweat_smile:, i hope you can take a look at that as well. Let me know if theres anything i can tell about the modules and thanks again in advance!
Author API
Assets
Delete Asset
Deletes an asset when provided an Asset ID, There is a force parameter that when toggled will delete the folder regardless if it's referenced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get assets job status
Given an assets job ID will return the state that the job is currently in (PROCESSING, COMPLETED, etc.)
Events
AEM Assets events
The costumer can create a web hook in this module and register it in the Adobe admin console
Metadata
Get asset metadata
Given asset ID returns assets metadata.
Update asset metadata
Given asset ID, there are 6 patch operations that can be done with the metadata. The operations are visible in the module as well as the documentation.
Import
Get import job results
Given Job ID returns it's result.
Get import job status
Given Job ID returns its status.
Upload an asset from url
Takes global metadata which applies to all the assets and local ones which apply individually.In both it is also possible to specify custom metadata.
Also takes the folder path or folder ID to place the assets there and url-s of the assets.
Relations
Create asset relation
Given asset ID and a list of related asset ID as well as the relation types creates those relationships.
Delete asset relations
Given asset ID and relation type deletes all relations of that type. Can also specify a related asset to target only that.
 there is a checkbox that is checked by default and when unchecked reveals a field where the user can specify the related user ID.
Get asset relation types
Given asset ID returns all the relation types that the asset has.
Get asset relations
Given asset ID returns all relations. Can also specify a specific type of relation.
Folders API
Create folders
Given a list of folders with their path, name, title, creates them.
Delete a folder by ID
Given Folder ID deletes the folder. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Delete folders by path
Given a list of paths, deletes everything in them. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get folders job results
Given job ID returns its result.
Get folders job status
Given job ID returns its status.
List Folders
List folders under the given folder. In the module you can choose the root folder either by ID or by Path.
-->

