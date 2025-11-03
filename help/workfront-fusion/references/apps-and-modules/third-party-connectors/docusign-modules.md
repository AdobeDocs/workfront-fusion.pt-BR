---
title: Módulos do DocuSign
description: Os  [!DNL Adobe Workfront Fusion DocuSign] módulos permitem que você monitore e recupere o status do envelope, pesquise e recupere envelopes, ou baixe e envie um documento para entrar em sua  [!DNL DocuSign] conta.
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2250'
ht-degree: 0%

---

# Módulos do DocuSign

Os módulos do Adobe Workfront Fusion [!DNL DocuSign] permitem monitorar e recuperar o status do envelope, pesquisar e recuperar envelopes, ou baixar e enviar um documento para entrar em sua conta do [!DNL DocuSign].

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Para usar módulos [!DNL DocuSign], você deve ter uma conta [!DNL DocuSign].

## Informações da API do DocuSign

O conector DocuSign usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!DNL DocuSign] ao Workfront Fusion {#connect-docusign-to-workfront-fusion}

Para criar uma conexão para seus módulos do [!DNL DocuSign]:

1. Clique em **[!UICONTROL Adicionar]** ao lado da caixa [!UICONTROL Conexão] ao começar a configurar o primeiro módulo [!DNL DocuSign].
1. Insira o seguinte:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Nome da Conexão]</p> </td> 
      <td>Insira um nome para a nova conexão [!DNL DocuSign].</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Ambiente]</p> </td> 
      <td>Selecione se você está se conectando a uma produção em um ambiente de não produção.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Nome da Conexão]</p> </td> 
      <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Tipo de conta]</td> 
      <td>Selecione se a conta à qual deseja se conectar é uma conta de produção ou uma conta de demonstração.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **Continuar** para salvar a conexão e retornar ao módulo.

## [!DNL DocuSign] módulos e seus campos

Ao configurar módulos do [!DNL DocuSign], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL DocuSign] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)

### Acionadores

#### [!UICONTROL Assistir a envelopes]

Esse módulo de acionamento inicia um cenário quando um envelope é enviado, entregue, assinado, concluído ou recusado.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao Workfront Fusion, consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar Documentação ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conta] </td> 
   <td> <p>Selecione a conta que contém os registros que você deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de evento]</td> 
   <td> <p> Selecione o tipo de evento que deseja assistir.</p> 
    <ul> 
     <li>[!UICONTROL Documento concluído]</li> 
     <li>[!UICONTROL Documento recusado]</li> 
     <li>[!UICONTROL Documento enviado]</li> 
     <li>[!UICONTROL Documento assinado]</li> 
     <li>[!UICONTROL Novo documento na Caixa de Entrada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Saídas]</p> </td> 
   <td> <p>Selecione os campos que deseja incluir na saída do módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de registros com os quais você deseja que o módulo funcione durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Adicionar um campo personalizado]](#add-a-custom-field)
* [[!UICONTROL Adicionar Destinatário ao Envelope]](#add-recipient-to-envelope)
* [[!UICONTROL Criar um novo envelope]](#create-a-new-envelope)
* [[!UICONTROL Chamada de API personalizada]](#custom-api-call)
* [[!UICONTROL Baixar um documento]](#download-a-document)
* [[!UICONTROL Modificar campo personalizado]](#modify-custom-field)
* [[!UICONTROL Ler um envelope]](#read-an-envelope)
* [[!UICONTROL Enviar envelope]](#send-envelope)
* [[!UICONTROL Carregar um arquivo em um envelope]](#upload-a-file-to-an-envelope)

#### [!UICONTROL Adicionar um campo personalizado]

Este módulo de ação adiciona um campo personalizado ao documento

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao Workfront Fusion, consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao Workfront Fusion</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conta] </td> 
   <td> <p>Selecione a conta que contém o documento ao qual você deseja adicionar um campo personalizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Envelope]</td> 
   <td> <p> Insira ou mapeie a ID do envelope que contém o documento ao qual você deseja adicionar um campo personalizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do campo]</td> 
   <td>Insira ou mapeie um nome para o novo campo que deseja adicionar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Necessário]</td> 
   <td>Ative essa opção se desejar que o campo adicionado seja um campo obrigatório.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostrar campo]</td> 
   <td>Ative essa opção se desejar que o campo fique visível.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valor]</td> 
   <td>Insira ou mapeie o valor (conteúdo) do campo adicionado. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Adicionar Destinatário ao Envelope]

Este módulo de ação adiciona um ou mais destinatários a um envelope existente. Se o envelope já tiver sido enviado, o recipient receberá um email. Este módulo não é válido para envelopes que já foram concluídos.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Conexão] </td>
   <td> <p>Para obter instruções sobre como conectar sua conta do DocuSign ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Conta] </td>
   <td> <p>Selecione a conta que contém o envelope no qual deseja adicionar recipients.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID de Envelope]</td>
    <td>Selecione ou mapeie a ID do envelope ao qual deseja adicionar o recipient.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Tipo de destinatário]</td>
   <td> <p> Selecione o tipo de destinatário que deseja adicionar ao envelope.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Cópia carbono]</p> </li> 
     <li> <p>[!UICONTROL Entrega certificada]</p> </li> 
     <li> <p>[!UICONTROL Assinante presencial]</p> </li> 
     <li> <p>[!UICONTROL Intermediário]</p> </li> 
     <li> <p>[!UICONTROL Signatário]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>Insira ou mapeie o endereço de email do destinatário que deseja adicionar ao envelope.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Nome]</td>
   <td>Insira ou mapeie o nome do destinatário que deseja adicionar ao envelope.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Ordem de roteamento]</td>
   <td> <p>Insira ou mapeie o número do roteamento do recipient. O número do banco determina a ordem na qual os destinatários recebem e assinam seus documentos.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL corpo do email]</td>
   <td>Insira ou mapeie o corpo (conteúdo) do email enviado ao destinatário.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Assunto do email]</td>
   <td>Insira ou mapeie o assunto do email enviado ao recipient.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Mensagem privada]</td>
   <td> Se desejar enviar uma mensagem privada para o recipient, insira ou mapeie o texto da mensagem. <p>Somente o recipient selecionado vê a mensagem privada, bem como a mensagem geral. A mensagem privada é limitada a 1000 caracteres.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Autenticação]</td> 
   <td> <p>Selecione o método de autenticação que deseja usar para confirmar a identidade do recipient.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nenhum]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Código de acesso]</strong> </p> <p>Insira ou mapeie o código de acesso.</p> </li> 
     <li> <p><strong>[!UICONTROL Telefone]</strong> </p> <p>Insira ou mapeie o número de telefone.</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>Insira ou mapeie o número de telefone.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar um novo envelope]

Este módulo de ação cria um novo envelope a partir de um modelo. Ele retorna a ID do novo envelope, bem como o status do novo envelope.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conexão] </td>

<td> <p>Para obter instruções sobre como conectar sua conta do DocuSign ao Workfront Fusion, consulte os artigos em <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Conta] </td>
   <td> <p>Selecione a conta que contém o envelope no qual você deseja carregar um arquivo.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Modelo]</td>
   <td> <p> Selecione o modelo a partir do qual deseja criar o novo envelope. Os modelos estão disponíveis com base na [!UICONTROL Account] selecionada.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Após criação]
   </td> 
   <td> <p>Selecione se deseja salvar o envelope como rascunho ou enviá-lo para assinatura.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Destinatários do modelo]</td>
    <td>Para cada destinatário que você deseja adicionar a este envelope, clique em <b>Adicionar item</b> e insira os seguintes detalhes:
    <ul>
    <li><b>Código de acesso</b><p>Insira ou mapeie o código que o destinatário usa para acessar o envelope.<p></li>
    <li><b>Email</b><p>Insira ou mapeie o endereço de email do recipient.<p></li>
    <li><b>Nome</b><p>Insira ou mapeie o nome do recipient.<p></li>
    <li><b>Nome da função</b><p>Insira ou mapeie o nome da função do recipient.<p></li>
    <li><b>Ordem de roteamento</b><p>Insira ou mapeie o número do roteamento do recipient. O número do banco determina a ordem na qual os destinatários recebem e assinam seus documentos.<p></li>
    </ul>
    </td>
    </tr>
  <tr> 
   <td role="rowheader">
     [!UICONTROL Permitir Impressão e Assinatura]
   </td> 
   <td> <p>Habilite esta opção para permitir que o destinatário imprima o documento e assine o papel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Permitir Reatribuição]
   </td> 
   <td> <p>Ative essa opção se desejar que o recipient possa reatribuir os documentos a outro usuário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Permitir Recursão de Destinatário]
   </td> 
   <td> <p>Habilite esta opção para permitir a recursão do destinatário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Cópia Autoritativa]
   </td> 
   <td> <p>Habilite esta opção para marcar os documentos deste envelope como cópias autoritativas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Navegação Automática]
   </td> 
   <td> <p>Habilite esta opção para definir a navegação automática para o recipient.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Identificação da Marca]
   </td> 
   <td> <p>Insira ou mapeie a ID da marca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Marcação Habilitada]
   </td> 
   <td> <p>Habilite esta opção para habilitar a Marcação do documento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Expirar Habilitado]
   </td> 
   <td> <p>Habilite esta opção para definir uma expiração para este envelope. Se você ativar essa opção, preencha os seguintes campos:<ul><li><b>Expirar após</b><p>Insira ou mapeie o número de dias após o qual este envelope expira.</p></li><li><b>Aviso de expiração</b><p>Insira ou mapeie o número de dias antes da expiração em que um email de lembrete é enviado ao destinatário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Corpo]
   </td> 
   <td> <p>Insira ou mapeie o corpo (conteúdo) do email que acompanha este envelope.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Assunto]
   </td> 
   <td> <p>Insira ou mapeie o assunto do email que acompanha este envelope.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chamada de API personalizada]

Esse módulo de ação permite executar uma chamada de API personalizada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao Workfront Fusion, consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conta]</td> 
   <td>Insira ou mapeie a conta que deseja usar para acessar a API [!DNL DocuSign].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Insira ou mapeie um caminho relativo a <code>https://&lt;BASE_URI>/v2/accounts/&lt;ACCOUNT_ID>.</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Método]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Isso determina o tipo de conteúdo da solicitação.</p> <p>Por exemplo,<code> {"Content-type":"application/json"}</code></p> <p>Observação: se você estiver recebendo erros e for difícil determinar sua origem, considere modificar cabeçalhos com base na documentação do Workfront. Se sua chamada de API personalizada retornar um erro de solicitação HTTP 422, tente usar um cabeçalho "Content-Type":"text/plain".</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de resultados com os quais trabalhar durante um ciclo de execução.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Exemplo:** Envelopes de Lista

A chamada de API a seguir retorna envelopes a partir da data especificada em sua conta [!DNL DocuSign]:

**URL**: `/v2.1/accounts/{accountId}/envelopes/`

**Método**: `GET`

**Cadeia de Caracteres de Consulta**:

* **Chave**: `from_date`

* **Valor**: `YYYY-MM-DD`

Especifica quando a solicitação começa a verificar alterações de status para envelopes na conta.

![Exemplo de configuração de Documentação](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)

O resultado pode ser encontrado na Saída do módulo em Pacote > Corpo > envelopes.

No nosso exemplo, 6 envelopes foram retornados:

![Exemplo de saída de documento](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

>[!ENDSHADEBOX]

#### [!UICONTROL Baixar um documento]

Este módulo de ação baixa um único documento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao Workfront Fusion, consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao Workfront Fusion</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conta] </td> 
   <td> <p>Selecione a conta que contém o documento que você deseja baixar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Envelope]</td> 
   <td> <p> Insira ou mapeie a ID do envelope que deseja baixar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Documento]</p> </td> 
   <td> <p>Insira ou mapeie a ID do documento que deseja baixar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Certificado]</td> 
   <td>Habilite esta opção para incluir o certificado de assinatura do envelope no download.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documentos por ID de Usuário]</td> 
   <td>Habilite esta opção para permitir que os destinatários recuperem documentos por ID de usuário. Por exemplo, se um usuário estiver incluído em duas ordens de roteiro diferentes com visibilidades diferentes, o uso dessa opção retornará todos os documentos de ambos os roteiros.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criptografar]</td> 
   <td>Habilite esta opção se quiser que os bytes do PDF retornados na resposta sejam criptografados para todos os gerenciadores de chaves configurados na sua conta [!DNL DocuSign].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Idioma]</td> 
   <td>Selecione o idioma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostrar Alterações]</td> 
   <td>Habilite esta opção para realçar quaisquer campos alterados para o PDF retornado são realçados em amarelo, e destacar assinaturas opcionais ou iniciais em vermelho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Marca D'Água]</td> 
   <td> <p>Habilite essa opção para habilitar o recurso de marca d'água. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modificar campo personalizado]

Esse módulo de ação modifica um campo personalizado usando o nome do campo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao Workfront Fusion, consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao Workfront Fusion</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conta] </td> 
   <td> <p>Selecione a conta que contém o documento no qual você deseja modificar um campo personalizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Envelope]</td> 
   <td> <p> Insira ou mapeie a ID do envelope que contém o documento no qual você deseja modificar um campo personalizado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Campo]</td> 
   <td>Insira ou mapeie a ID do campo que você deseja modificar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome do campo]</td> 
   <td>Insira ou mapeie o nome do campo que você deseja modificar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Necessário]</td> 
   <td>Habilite essa opção se desejar que o campo modificado seja obrigatório.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostrar campo]</td> 
   <td>Ative essa opção se desejar que o campo fique visível.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valor]</td> 
   <td>Insira ou mapeie o valor (conteúdo) do campo modificado. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ler um envelope]

Este módulo de ação lê informações sobre um envelope em [!DNL DocuSign] usando a ID de envelope.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao Workfront Fusion, consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao Workfront Fusion</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conta] </td> 
   <td> <p>Selecione a conta que contém o documento do qual deseja ler informações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Envelope]</td> 
   <td> <p> Insira ou mapeie a ID do envelope que contém o documento do qual você deseja ler as informações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saídas]</td> 
   <td>Selecione as propriedades que você deseja que apareçam na saída do módulo. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Enviar envelope]

Esse módulo de ação envia um envelope de rascunho para seus recipients.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao Workfront Fusion, consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao Workfront Fusion</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conta] </td> 
   <td> <p>Selecione a conta que contém o envelope de rascunho que você deseja enviar aos recipients.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Envelope]</td> 
   <td> <p> Insira ou mapeie a ID do envelope de rascunho que você deseja enviar aos recipients.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um arquivo em um envelope]

Este módulo carrega um arquivo especificado em um envelope existente no DocuSign.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL DocuSign] ao Workfront Fusion, consulte <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Conectar [!DNL DocuSign] ao Workfront Fusion</a> neste artigo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conta] </td> 
   <td> <p>Selecione a conta que contém o envelope no qual você deseja carregar um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Envelope]</td> 
   <td> <p> Insira ou mapeie a ID do envelope no qual deseja fazer upload de um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td>Selecione um arquivo de origem de um módulo anterior ou insira o nome e os dados do arquivo de origem.</td> 
  </tr> 
 </tbody> 
</table>
