---
title: Módulos do Microsoft OneDrive for Business
description: Em um cenário  [!DNL Adobe Workfront Fusion] , é possível automatizar fluxos de trabalho que usam  [!DNL Microsoft OneDrive for Business], bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 657bea46-064e-4333-8e86-81678bb1c3bd
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive for Business] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Microsoft OneDrive for Business], bem como conectá-los a vários aplicativos e serviços de terceiros.

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

Para usar [!DNL Microsoft OneDrive for Business] com [!DNL Adobe Workfront Fusion], você precisará de uma conta [!DNL Microsoft].

## Conectando o serviço [!DNL Microsoft OneDrive for Business] a [!DNL Workfront Fusion]

Para obter instruções sobre como conectar sua conta do [!DNL Microsoft OneDrive for Business] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alguns aplicativos do Microsoft usam a mesma conexão, que está vinculada a permissões de usuário individuais. Portanto, ao criar uma conexão, a tela de consentimento de permissões exibe todas as permissões que foram concedidas anteriormente à conexão deste usuário, além de todas as novas permissões necessárias para o aplicativo atual.
>
>Por exemplo, se um usuário tiver permissões de &quot;Tabela de leitura&quot; concedidas por meio do conector do Excel e criar uma conexão no conector do Outlook para ler emails, a tela de consentimento de permissões mostrará a permissão &quot;Tabela de leitura&quot; já concedida e a permissão &quot;Gravar email&quot; recém-necessária.

## [!DNL Microsoft OneDrive for Business] módulos e seus campos

Ao configurar módulos do [!DNL Microsoft OneDrive for Business], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Microsoft OneDrive for Business] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)

### Acionadores

* [[!UICONTROL Observar arquivos]](#watch-files)
* [[!UICONTROL Observar pastas]](#watch-folders)

#### [!UICONTROL Observar arquivos]

Esse módulo acionador é ativado quando um novo arquivo é adicionado ou atualizado em uma pasta que está sendo observada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID da Unidade]</p> </td> 
   <td> <p>Selecione a unidade que deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td> <p> Selecione a pasta que deseja observar. Em um cenário, só é possível monitorar uma pasta.</p> <p>Dica: para observar várias pastas, crie um cenário independente para cada uma delas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL que eu quero assistir]</p> </td> 
   <td> <p>Selecione se você deseja observar novos arquivos e todas as alterações ou somente novos arquivos.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de linhas retornadas]</td> 
   <td> <p> Defina o número máximo de resultados que você deseja que o módulo retorne durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar pastas]

Esse módulo acionador é ativado quando uma nova pasta é adicionada à pasta que está sendo monitorada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conexão]</p> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID da Unidade]</p> </td> 
   <td> <p>Selecione a unidade que deseja observar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td> <p> Selecione a pasta que deseja observar. Em um cenário, só é possível monitorar uma pasta.</p> <p>Dica: para rastrear várias pastas, crie um cenário independente para cada uma delas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL que eu quero assistir]</p> </td> 
   <td> <p>Selecione se deseja observar novas pastas e todas as alterações ou somente novas pastas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de linhas retornadas]</td> 
   <td> <p> Defina o número máximo de resultados que você deseja que o módulo retorne durante um ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Criar uma pasta]](#create-a-folder)
* [[!UICONTROL Excluir um arquivo]](#delete-a-file)
* [[!UICONTROL Excluir uma pasta]](#delete-a-folder)
* [[!UICONTROL Obter um arquivo]](#get-a-file)
* [[!UICONTROL Obter um link de compartilhamento]](#get-a-sharing-link)
* [[!UICONTROL Carregar um arquivo]](#upload-a-file)

#### [!UICONTROL Criar uma pasta]

Cria uma pasta dentro da pasta pai especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><strong>[!UICONTROL Conexão]</strong> </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL ID da Unidade]</strong> </td> 
   <td> <p>Selecione a unidade na qual deseja criar uma nova pasta.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL pasta]</strong> </td> 
   <td> <p>Selecione a pasta na qual deseja criar uma nova pasta.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Nome da Pasta]</strong> </td> 
   <td>Insira ou mapeie um nome para a nova pasta.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um arquivo]

Este módulo de ação move o arquivo especificado para a lixeira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione a unidade da qual deseja excluir um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Arquivo]</td> 
   <td> <p>Informe a ID do arquivo que deseja deletar. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir uma pasta]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione a unidade da qual deseja excluir um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID da Pasta]</td> 
   <td> <p>Insira ou mapeie a ID da pasta que deseja excluir. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um arquivo]

Este módulo de ação recupera o arquivo com a ID fornecida.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione a unidade da qual deseja recuperar um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Arquivo]</td> 
   <td> <p>Insira a ID do arquivo que você deseja recuperar. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um link de compartilhamento]

Este módulo recupera um link que você pode compartilhar para dar acesso ao arquivo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione a unidade na qual deseja fazer upload de um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enter]</td> 
   <td> <p>Selecione se deseja escolher um arquivo usando a ID do arquivo ou o caminho do Arquivo. Insira a ID do arquivo ou o caminho no campo exibido.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo de permissão]</p> </td> 
   <td> <p>Selecione se você deseja que as pessoas que recebem o link tenham permissões de leitura/gravação ou somente leitura.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Escopo]</td> 
   <td> <p> Selecione se você deseja que o arquivo seja acessível por qualquer pessoa que tenha o link ou acessível somente aos membros da organização.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um arquivo]

Este módulo de ação faz upload de um arquivo binário ou de texto para uma pasta especificada

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Office 365] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Criar uma conexão - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione a unidade na qual deseja fazer upload de um arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pasta] </td> 
   <td> <p>Selecione a pasta na unidade.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Arquivo Source]</p> </td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Se existir um arquivo com o mesmo nome]</td> 
   <td> <p> Selecione o que deseja fazer se um arquivo com o mesmo nome do arquivo do qual você está tentando fazer upload já existir.</p> 
    <ul> 
     <li>[!UICONTROL Substituir o arquivo existente]</li> 
     <li>[!UICONTROL Renomear o novo arquivo]</li> 
     <li>[!UICONTROL Encerra com erro]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
