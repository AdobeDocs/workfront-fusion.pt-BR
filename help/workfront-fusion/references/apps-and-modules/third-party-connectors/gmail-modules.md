---
title: Módulos do Gmail
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam o Gmail, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1858'
ht-degree: 0%

---

# [!DNL Gmail] módulos

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam o [!DNL Gmail], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Para usar módulos [!DNL Gmail], você deve ter uma conta [!DNL Gmail].

## Conectar o [!DNL Gmail] ao Workfront Fusion {#connect-gmail-to-workfront-fusion}

* [Conectar [!DNL Gmail] ao Workfront Fusion usando [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usinggoogle-workspace)
* [Conecte-se [!DNL Gmail] ao Workfront Fusion usando o [!DNL gmail.com] or [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Conecte o [!DNL Gmail] ao Workfront Fusion usando o [!DNL &#x200B; Google Workspace]

Para obter instruções sobre como conectar sua conta do [!DNL Google Workspace] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

### Conecte o [!DNL Gmail] ao Workfront Fusion usando o [!DNL gmail.com] ou o [!DNL googlemail].com

Se você for [!DNL @gmail.com] ou usuário [!DNL @googlemail.com], deve criar um cliente OAuth em [the [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) para obter uma [!UICONTROL ID do Cliente] e um [!UICONTROL Segredo do Cliente].

Para obter instruções passo a passo sobre como criar o cliente OAuth e obter uma [!UICONTROL ID do Cliente] e um [!UICONTROL Segredo do Cliente], consulte [Conectar o Adobe Workfront Fusion ao Google Services usando um cliente OAuth personalizado](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## [!DNL Gmail] módulos e seus campos

Ao configurar módulos do [!DNL Gmail], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Gmail] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)
* [Iteradores](#iterators)

### Acionadores

#### [!UICONTROL Assistir emails]

Esse módulo de acionamento executa um cenário quando um novo email é recebido para ser processado.

O módulo retorna todos os campos padrão associados ao registro ou aos registros, juntamente com quaisquer campos e valores personalizados que a conexão acesse. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta de e-mail que deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo de filtro] </td> 
   <td> <p>Selecione o tipo de filtro que deseja usar para assistir a emails</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Filtro simples]</strong> </p> <p>Preencha os campos [!UICONTROL Critérios], [!UICONTROL Endereço de email do remetente], [!UICONTROL Assunto] e [!UICONTROL Frase de Pesquisa]</p> </li> 
     <li> <p> <strong>[!UICONTROL Filtro Gmail]</strong> </p> <p>No campo [!UICONTROL Consulta], insira a consulta que deseja usar para filtrar emails.</p> <p>Para obter mais informações sobre [!DNL Gmail] filtros, consulte <a href="https://support.google.com/mail/answer/7190">Refinar pesquisas</a> na documentação [!DNL Gmail].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Critério]</td> 
   <td>Selecione se deseja assistir a emails do [!UICONTROL todos os emails], do [!UICONTROL somente emails lidos] ou do [!UICONTROL somente emails não lidos].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Endereço de email do remetente]</td> 
   <td> <p> Digite um endereço de e-mail para ver apenas os e-mails enviados a partir desse endereço.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Assunto]</td> 
   <td>Digite uma sequência de texto para ver somente os emails que tenham essa sequência de texto no assunto.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pesquisar frase]</td> 
   <td>Digite uma sequência de texto para ver somente os emails que possuem essa sequência de texto em qualquer lugar do email.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Marcar mensagens de email como lidas quando buscadas]</td> 
   <td> <p> Ative esta opção para marcar os e-mails recuperados como lidos.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Número máximo de resultados]</td> 
   <td> <p> Defina o número máximo de resultados com os quais o Workfront Fusion funcionará durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

<!--* [Add labels](#add-labels)-->
* [[!UICONTROL Copiar um email]](#copy-an-email)
* [[!UICONTROL Criar um rascunho]](#create-a-draft)
* [[!UICONTROL Excluir um email]](#delete-an-email)
  <!--* [Delete labels](#delete-labels)-->
* [[!UICONTROL Marcar um email como lido]](#mark-an-email-as-read)
* [[!UICONTROL Marcar um email como não lido]](#mark-an-email-as-unread)
* [[!UICONTROL Mover um email]](#move-an-email)
* [[!UICONTROL Modificar rótulos de email]](#modify-email-labels)
* [[!UICONTROL Enviar um email]](#send-an-email)
  <!--* [Set labels](#set-labels)-->

<!--#### Add labels-->

#### [!UICONTROL Copiar um email]

Esse módulo de ação copia um email ou rascunho de email para uma pasta especificada por você.

Você especifica a pasta, a pasta de destino e a ID do email.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta de origem [!DNL Gmail] que contém o email que você deseja copiar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta de destino]</td> 
   <td> <p>Selecione a pasta de destino [!DNL Gmail] para a qual você deseja copiar o email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID DE E-MAIL (UID)]</td> 
   <td> <p>Insira ou mapeie a ID de e-mail do e-mail que deseja copiar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar um rascunho]

Esse módulo de ação cria um novo rascunho de email e o adiciona a uma pasta especificada por você.

Você especifica a pasta na qual deseja criar um rascunho.

O módulo retorna a ID do rascunho do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta [!DNL Gmail] na qual deseja criar um rascunho.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Para] </td> 
   <td> <p>Clique em <strong>[!UICONTROL Adicionar]</strong> e digite ou mapeie o endereço de email de cada destinatário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Assunto] </td> 
   <td> <p>Insira ou mapeie o assunto do email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conteúdo] </td> 
   <td> <p>Insira ou mapeie o conteúdo do email (corpo da mensagem). Tags do HTML são permitidas.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anexos] </td> 
   <td> <p>Clique em <strong>[!UICONTROL Adicionar]</strong> para adicionar um anexo. Você pode mapear um arquivo dos módulos anteriores.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copiar destinatários]</td> 
   <td> <p> Clique em <strong>[!UICONTROL Adicionar]</strong> e, em seguida, insira ou mapeie o endereço de email para cada destinatário de cópia.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destinatários de cópia oculta]</td> 
   <td> <p> Clique em <strong>[!UICONTROL Adicionar]</strong> e, em seguida, insira ou mapeie o endereço de email para cada destinatário de cópia oculta.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um email]

Esse módulo de ação remove um email ou um rascunho de email de uma pasta especificada.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] ID da Mensagem]</p> </td> 
   <td> <p>Insira ou mapeie a ID de e-mail do e-mail que deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanentemente] </td> 
   <td> <p>Ative esta opção para permitir que o módulo exclua permanentemente o e-mail, em vez de movê-lo para a pasta de lixo.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Delete labels-->



#### [!UICONTROL Marcar um email como lido]

Este módulo de ação marca um email como lido.

Especifique a ID do email e sua pasta.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta [!DNL Gmail] que contém o email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID DE E-MAIL (UID)]</td> 
   <td> <p> Insira ou mapeie a ID de email.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Marcar um email como não lido]

Este módulo de ação marca um email ou rascunho de email como não lido.

Especifique a ID do email e sua pasta.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta [!DNL Gmail] que contém o email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID DE E-MAIL (UID)] </td> 
   <td> <p>Insira ou mapeie a ID de e-mail do e-mail que você deseja marcar como não lido.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modificar rótulos de email]

Esse módulo de ação modifica o rótulo em uma mensagem de email especificada.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] ID da Mensagem]</td> 
   <td> <p> Insira ou mapeie a ID de e-mail do e-mail que deseja excluir.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Rótulos a serem adicionados]</p> </td> 
   <td> <p>Selecione ou mapeie o rótulo que deseja adicionar à mensagem de email selecionada.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Rótulos a serem removidos]</td> 
   <td> <p> Selecione ou mapeie o rótulo que deseja remover da mensagem de email selecionada.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL Rótulo para adicionar] e [!UICONTROL Rótulo para remover] campos carregam apenas rótulos criados pelo usuário.

#### [!UICONTROL Mover um email]

Esse módulo de ação move um email ou rascunho de email para uma pasta especificada por você.

Você especifica a pasta, a pasta de destino e a ID do email.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao [!UICONTROL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta de origem [!DNL Gmail] que contém o email que você deseja mover.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta de destino]</td> 
   <td> <p> Selecione a pasta de destino [!DNL Gmail] para a qual você deseja mover o email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID DE E-MAIL (UID)]</td> 
   <td> <p> Insira ou mapeie a ID de email do email que você deseja mover.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Enviar um email]

Esse módulo de ação envia um novo email.

Especifique o recipient do email.

O módulo retorna a ID do email e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Gmail] ao Workfront Fusion, consulte <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Gmail] ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL De]</td> 
   <td> <p>Insira ou mapeie um endereço de email de remetente.</p> <p>Observação: se você inserir um endereço de email incorreto, poderá ocorrer um erro ao enviar uma mensagem porque sua conta talvez não tenha permissão para enviar emails de um endereço diferente do seu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Para] </td> 
   <td> <p>Clique em <strong>[!UICONTROL Adicionar]</strong> e digite ou mapeie o endereço de email de cada destinatário.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Assunto] </td> 
   <td> <p>Insira ou mapeie o assunto do email.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conteúdo] </td> 
   <td> <p>Insira ou mapeie o conteúdo do email (corpo da mensagem). Tags do HTML são permitidas.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anexos] </td> 
   <td> <p>Clique em <strong>[!UICONTROL Adicionar]</strong> para adicionar um anexo. Você pode mapear um arquivo dos módulos anteriores.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copiar destinatários]</td> 
   <td> <p> Clique em <strong>[!UICONTROL Adicionar]</strong> e, em seguida, insira ou mapeie o endereço de email para cada destinatário de cópia.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destinatários de cópia oculta]</td> 
   <td> <p> Clique em <strong>[!UICONTROL Adicionar]</strong> e, em seguida, insira ou mapeie o endereço de email para cada destinatário de cópia oculta.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Set labels-->

### Iteradores

#### [!UICONTROL Iterar anexos]

Você pode iterar anexos de email. Cada anexo é um conjunto separado na saída do módulo. Para obter mais informações, consulte [Módulo Iterador](/help/workfront-fusion/references/modules/iterator-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL módulo Source] </td> 
   <td> <p>Selecione o módulo do qual deseja iterar anexos. </p> </td> 
  </tr> 
 </tbody> 
</table>
