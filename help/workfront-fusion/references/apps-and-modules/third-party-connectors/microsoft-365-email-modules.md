---
title: Email do Microsoft Office 365
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o Microsoft Office 365 Email, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 5d4072ba-c598-4347-a42f-c59c7add0a1b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2915'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Email] módulos

Em um cenário do Adobe Workfront Fusion, você pode automatizar fluxos de trabalho que usam o [!UICONTROL Email do Microsoft Office 365], bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

## Pré-requisitos

Para usar módulos [!DNL Microsoft Office 365 Email], você deve ter uma conta [!DNL Microsoft Office 365 Email].

## Informações da API de email do Microsoft Office 365

O conector de email do Microsoft Office 365 usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2.6.5</td> 
  </tr>
 </tbody> 
 </table>

## Conectando o serviço [!DNL Office 365 Email] ao Workfront Fusion

Para obter instruções sobre como conectar sua conta do [!DNL Office 365 Email] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alguns aplicativos do Microsoft usam a mesma conexão, que está vinculada a permissões de usuário individuais. Portanto, ao criar uma conexão, a tela de consentimento de permissões exibe todas as permissões que foram concedidas anteriormente à conexão deste usuário, além de todas as novas permissões necessárias para o aplicativo atual.
>
>Por exemplo, se um usuário tiver permissões de &quot;Tabela de leitura&quot; concedidas por meio do conector do Excel e criar uma conexão no conector do Outlook para ler emails, a tela de consentimento de permissões mostrará a permissão &quot;Tabela de leitura&quot; já concedida e a permissão &quot;Gravar email&quot; recém-necessária.

## [!DNL Microsoft Office 365 Email] módulos e seus campos

Ao configurar módulos do [!DNL Microsoft Office 365 Email], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Microsoft Office 365 Email] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Mensagem](#message)
* [Mensagem de rascunho](#draft-message)
* [Anexo](#attachment)
* [Outras](#other)

### Mensagem

* [[!UICONTROL Criar e Enviar uma Mensagem (herdada)]](#create-and-send-a-message)
* [[!UICONTROL Excluir uma Mensagem]](#delete-a-message)
* [[!UICONTROL Obter uma mensagem]](#get-a-message)
* [[!UICONTROL Mover uma Mensagem]](#move-a-message)
* [[!UICONTROL Pesquisar mensagens]](#search-messages)
* [[!UICONTROL Assistir Mensagens]](#watch-messages)



#### [!UICONTROL Criar e Enviar uma Mensagem (herdada)]

Esse módulo de ação cria e envia uma mensagem de email.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assunto]</td> 
   <td> <p>Insira ou mapeie a linha de assunto da mensagem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conteúdo do corpo]</td> 
   <td> <p>Insira ou mapeie o texto do corpo da mensagem do email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importância]</td> 
   <td> <p>Selecionar a importância do email</p> 
    <ul> 
     <li>[!UICONTROL Baixo]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Para Destinatários]</p> </td> 
   <td> <p>Para cada destinatário para o qual deseja enviar o email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Para cada destinatário para o qual deseja enviar uma cópia do email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Destinatários Cco]</p> </td> 
   <td> <p>Para cada destinatário para o qual você deseja enviar uma cópia do email, sem permitir que outros destinatários vejam seus nomes ou endereços de email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anexos]</p> </td> 
   <td> <p>Para cada anexo que você deseja adicionar ao email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL arquivo Source]</strong> </p> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos de Mensagens da Internet]</td> 
   <td> <p>Para cada cabeçalho que você deseja adicionar ao email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do cabeçalho</p> </li> 
     <li> <p><strong>[!UICONTROL Valor]</strong> </p> <p>Insira um valor para o cabeçalho.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma Mensagem]

Este módulo de ação exclui uma mensagem de email existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Selecione ou mapeie a ID da mensagem que deseja excluir.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma mensagem]

Este módulo de ação obtém os metadados de uma mensagem específica

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Selecione ou mapeie a ID da mensagem para a qual deseja recuperar metadados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Obter conteúdo MIME]</td> 
   <td>Habilite esta opção para recuperar dados sobre o conteúdo MIME da mensagem. O conteúdo [!UICONTROL MIME] pode incluir imagens, áudio, vídeo ou outros tipos de arquivos.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mover uma Mensagem]

Este módulo de ação move uma mensagem de email para uma pasta selecionada na caixa de correio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Selecione ou mapeie a ID da mensagem que deseja mover para uma pasta diferente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta de Email] </td> 
   <td> <p>Selecione ou mapeie a ID da pasta para onde deseja mover a mensagem.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar mensagens]

Este módulo de pesquisa procura mensagens com base em critérios específicos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Pasta de Email]</td> 
   <td> <p>Selecione a pasta que contém as mensagens que você deseja pesquisar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pesquisar]</td> 
   <td>Insira sua consulta de pesquisa. Para obter informações sobre como gravar uma consulta de pesquisa, consulte o artigo de suporte do [!DNL Microsoft] <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">Pesquisar Emails e Pessoas no [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordenar por]</td> 
   <td> <p>Selecione como deseja ordenar os resultados:</p> 
    <ul> 
     <li>[!UICONTROL Assunto (Crescente ou Decrescente)]</li> 
     <li>[!UICONTROL Data Hora de Criação (Crescente ou Decrescente)]</li> 
     <li>[!UICONTROL Data e hora da última modificação (crescente ou decrescente)]</li> 
     <li>[!UICONTROL Data Hora de Recebimento (Crescente ou Decrescente)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira o número máximo de mensagens que o Workfront Fusion deve retornar durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assistir Mensagens]

Esse módulo de acionamento inicia um cenário quando uma nova mensagem de email é enviada ou recebida.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Observar Mensagens]</p> </td> 
   <td> <p>Selecione as mensagens que deseja assistir:</p> 
    <ul> 
     <li>[!UICONTROL Somente Não Lido]</li> 
     <li>[!UICONTROL Somente leitura]</li> 
     <li>[!UICONTROL Tudo]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta de Email]</td> 
   <td> <p>Selecione a pasta que contém as mensagens que você deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pesquisar]</td> 
   <td>Insira sua consulta de pesquisa. O módulo retorna mensagens que correspondem a esta consulta. Para obter informações sobre como gravar uma consulta de pesquisa, consulte o artigo de suporte do [!DNL Microsoft] <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">Pesquisar Emails e Pessoas no [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira o número máximo de mensagens que o Workfront Fusion deve retornar durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Mensagem de rascunho

* [Criar uma mensagem de rascunho](#create-a-draft-message)
* [Enviar uma mensagem de rascunho](#send-a-draft-message)
* [Atualizar uma mensagem](#update-a-message)

#### [!UICONTROL Criar uma mensagem de rascunho]

Esse módulo de ação cria uma nova mensagem de email como rascunho.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assunto]</td> 
   <td> <p>Insira a linha de assunto da mensagem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Conteúdo do Corpo]</td> 
   <td>Selecione se o conteúdo do corpo da mensagem é HTML ou Text.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conteúdo do corpo]</td> 
   <td> <p>Insira ou mapeie o texto do corpo da mensagem do email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importância]</td> 
   <td> <p>Selecionar a importância do email</p> 
    <ul> 
     <li>[!UICONTROL Baixo]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Para Destinatários]</p> </td> 
   <td> <p>Para cada destinatário para o qual deseja enviar o email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Para cada destinatário para o qual deseja enviar uma cópia do email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Destinatários Cco]</p> </td> 
   <td> <p>Para cada destinatário para o qual você deseja enviar uma cópia do email, sem permitir que outros destinatários vejam seus nomes ou endereços de email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anexos]</p> </td> 
   <td> <p>Para cada anexo que você deseja adicionar ao email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL arquivo Source]</strong> </p> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Enviar uma mensagem de rascunho]

Esse módulo de ação envia uma mensagem de email que está atualmente em rascunho.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem de Rascunho]</td> 
   <td> <p> Selecione ou mapeie a ID da mensagem do rascunho que deseja enviar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar uma Mensagem]

Este módulo de ação atualiza uma mensagem existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de mensagem]</td> 
   <td> <p>Selecione como deseja identificar a mensagem a ser atualizada:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir Manualmente]</strong> </p> <p>Insira ou mapeie a ID da mensagem.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar na lista]</strong> </p> <p>Selecione a pasta que contém a mensagem que você deseja atualizar e selecione a mensagem</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assunto]</td> 
   <td> <p>Insira a linha de assunto da mensagem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conteúdo do corpo]</td> 
   <td> <p>Insira o texto do corpo da mensagem de email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importância]</td> 
   <td> <p>Selecionar a importância do email</p> 
    <ul> 
     <li>[!UICONTROL Baixo]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Para Destinatários]</p> </td> 
   <td> <p>Para cada destinatário para o qual deseja enviar o email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Para cada destinatário para o qual deseja enviar uma cópia do email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Destinatários Cco]</p> </td> 
   <td> <p>Para cada destinatário para o qual você deseja enviar uma cópia do email, sem permitir que outros destinatários vejam seus nomes ou endereços de email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anexos]</p> </td> 
   <td> <p>Para cada anexo que você deseja adicionar ao email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL arquivo Source]</strong> </p> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Marcá-lo como Lido]</td> 
   <td>Habilite esta opção para marcar a mensagem atualizada como lida.</td> 
  </tr> 
 </tbody> 
</table>

### Anexo

* [[!UICONTROL Baixar um Anexo]](#download-an-attachment)
* [[!UICONTROL Listar anexos]](#list-attachments)

#### [!UICONTROL Baixar um Anexo]

Este módulo baixa o anexo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Selecione ou mapeie a ID da mensagem que contém o anexo que você deseja baixar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Anexo]</td> 
   <td> <p>Insira ou mapeie a ID do anexo que deseja baixar. Você pode localizar essa ideia usando o módulo Listar anexos.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar anexos]

Este módulo recupera uma lista de anexos pertencentes à mensagem especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Selecione ou mapeie a ID da mensagem da qual deseja recuperar anexos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de anexos que você deseja que o módulo retorne durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outras

* [[!UICONTROL Adicionar Anexo]](#add-an-attachment)
* [Criar e enviar uma mensagem](#create-and-send-a-message)
* [[!UICONTROL Fazer uma chamada de API]](#make-an-api-call)

#### [!UICONTROL Adicionar Anexo]

Este módulo adiciona um grande anexo a uma mensagem.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Mensagem]</td> 
   <td> <p> Selecione ou mapeie a ID da mensagem à qual deseja adicionar um anexo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar e Enviar uma Mensagem]

Esse módulo de ação cria e envia uma mensagem de email.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assunto]</td> 
   <td> <p>Insira ou mapeie a linha de assunto da mensagem.</p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Conteúdo do corpo]</td> 
   <td> <p>Insira ou mapeie o texto do corpo da mensagem do email.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importância]</td> 
   <td> <p>Selecionar a importância do email</p> 
    <ul> 
     <li>[!UICONTROL Baixo]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Para Destinatários]</p> </td> 
   <td> <p>Para cada destinatário para o qual deseja enviar o email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Para cada destinatário para o qual deseja enviar uma cópia do email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Destinatários Cco]</p> </td> 
   <td> <p>Para cada destinatário para o qual você deseja enviar uma cópia do email, sem permitir que outros destinatários vejam seus nomes ou endereços de email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira o endereço de email do contato.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do contato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anexos]</p> </td> 
   <td> <p>Para cada anexo que você deseja adicionar ao email, clique em <b>Adicionar item</b> e insira o seguinte:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL arquivo Source]</strong> </p> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos de Mensagens da Internet]</td> 
   <td> <p>Adicione os cabeçalhos de mensagem para o email.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Insira o nome do cabeçalho</p> </li> 
     <li> <p><strong>[!UICONTROL Endereço de Email]</strong> </p> <p>Insira um valor para o cabeçalho.</p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Do endereço de email]</td> 
   <td> <p> Para usar um endereço de email compartilhado, insira o endereço aqui. O usuário cujas credenciais são usadas na conexão usada para este módulo deve ter acesso à pasta compartilhada.<p>Deixe este campo em branco para usar o endereço de email do proprietário da conexão.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fazer uma chamada de API]

Este módulo permite executar uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo para <code>https://graph.microsoft.com</code>. Exemplo:<code> /v1.0/me/messages</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Método]</p> </td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão. Por exemplo, <code>{"Content-type":"application/json"}</code>. O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p> Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
