---
title: Módulos do Box
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Box, bem como conectá-lo a vários aplicativos e serviços de terceiros. monitora uma pasta especificada para verificar alterações em arquivos, modificar e excluir arquivos existentes ou fazer upload de novos arquivos para uma pasta.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: f02c4df01c7fad6bb9cdf4911512eef97e71c82b
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 1%

---

# Módulos do Box

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Box], bem como conectá-los a vários aplicativos e serviços de terceiros. monitora uma pasta especificada para verificar alterações em arquivos, modificar e excluir arquivos existentes ou fazer upload de novos arquivos para uma pasta.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Para usar módulos [!DNL Box], você deve ter uma conta [!DNL Box].

## Informações da API de caixa

O conector Box usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] módulos e seus campos

Ao configurar módulos do [!DNL Box], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Box] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Acionadores](#triggers)
* [Ações](#actions)

### Acionadores

* [[!UICONTROL Novo evento]](#new-event)
* [[!UICONTROL Observar arquivos]](#watch-files)

#### [!UICONTROL Novo evento]

Esse módulo de acionador instantâneo inicia um cenário quando um arquivo é adicionado, movido, copiado, excluído, bloqueado ou desbloqueado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecione o webhook que deseja usar para assistir mensagens de saída. Para adicionar um webhook, clique em <strong>[!UICONTROL Adicionar]</strong> e insira o nome e a conexão do webhook.</p> <p> Para obter instruções sobre como conectar sua conta da [!UICONTROL Box] ao [!UICONTROL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Conectar-se a um serviço - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Número máximo de eventos retornados]</p> </td> 
   <td> <p>Insira o maior número de eventos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar arquivos]

Este módulo de acionamento inicia um cenário quando um novo arquivo é adicionado ou um arquivo existente é atualizado em uma pasta que está sendo observada.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Box] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Pasta</td> 
   <td> <p>Selecione a pasta que deseja observar. Um cenário pode observar uma única pasta.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Observar</td> 
   <td> <p>Selecione o tipo de arquivo que deseja observar.</p> 
    <ul> 
     <li> <p><strong>Somente arquivos novos</strong> </p> <p>O cenário será iniciado quando um novo arquivo for adicionado.</p> </li> 
     <li> <p><strong>Novos arquivos e todas as alterações</strong> </p> <p>O cenário começa quando um arquivo é adicionado ou quando o conteúdo do arquivo ou um atributo de arquivo (como seu nome) é modificado.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Número máximo de arquivos baixados</p> </td> 
   <td> <p>Insira o maior número de arquivos que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Excluir um arquivo]](#delete-a-file)
* [[!UICONTROL Obter um arquivo]](#get-a-file)
* [[!UICONTROL Atualizar um arquivo]](#update-a-file)
* [[!UICONTROL Carregar] um arquivo](#upload-a-file)

#### [!UICONTROL Excluir um arquivo]

Este módulo de ação exclui um arquivo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Box] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td>Insira ou mapeie o identificador exclusivo do arquivo que você deseja que o módulo exclua.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um arquivo]

Este módulo de ação baixa um arquivo.

Especifique a ID do arquivo.

>[!NOTE]
>
>Esse módulo é útil para fornecer arquivos aos módulos subsequentes.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Box] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td>Insira ou mapeie o ID exclusivo do arquivo que você deseja que o módulo recupere.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um arquivo]

Este módulo de ação atualiza um arquivo.

Especifique a ID do arquivo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Box] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Arquivo]</td> 
   <td>Insira ou mapeie o identificador exclusivo do arquivo que você deseja que o módulo atualize.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um arquivo]

Este módulo de ação carrega um arquivo.

Especifique o arquivo. Você também pode fornecer um novo nome para o arquivo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Box] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td> <p>Selecione a pasta na qual deseja fazer upload do arquivo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Se esse módulo não for bem-sucedido, considere o seguinte:
>
>* O tamanho do arquivo pode exceder o limite máximo de tamanho de arquivo para o plano [!DNL Box], ou você pode ter usado toda a cota de armazenamento da sua conta [!DNL Box]. Para obter mais espaço de armazenamento, exclua arquivos existentes do [!DNL Box] ou atualize sua conta do [!DNL Box].
>* [!DNL Box] não carrega mais de um arquivo com o mesmo nome em uma única pasta. Se a pasta de destino contiver um arquivo com o mesmo nome do arquivo que está sendo carregado, a execução do cenário será encerrada com um erro. Para evitar isso, renomear o arquivo. Se quiser atualizar o arquivo, use o módulo **[!UICONTROL Atualizar um arquivo]**.
