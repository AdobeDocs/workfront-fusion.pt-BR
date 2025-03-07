---
title: Módulos do Microsoft OneDrive
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o OneDrive, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: d21eafad-9c67-4f42-b718-0aa4223846e6
source-git-commit: 632128bdcb6f8b8361f5a28e4a5fb527eb274d54
workflow-type: tm+mt
source-wordcount: '4087'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL OneDrive], bem como conectá-los a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!DNL OneDrive], você deve ter uma conta [!DNL Microsoft OneDrive].



## Informações de API do OneDrive

O conector do OneDrive usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://graph.microsoft.com/v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>


## Conectando o serviço [!DNL OneDrive] a [!DNL Workfront Fusion]

Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!UICONTROL Workfront Fusion], consulte [Criar uma conexão com o [!UICONTROL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alguns aplicativos do Microsoft usam a mesma conexão, que está vinculada a permissões de usuário individuais. Portanto, ao criar uma conexão, a tela de consentimento de permissões exibe todas as permissões que foram concedidas anteriormente à conexão deste usuário, além de todas as novas permissões necessárias para o aplicativo atual.
>
>Por exemplo, se um usuário tiver permissões de &quot;Tabela de leitura&quot; concedidas por meio do conector do Excel e criar uma conexão no conector do Outlook para ler emails, a tela de consentimento de permissões mostrará a permissão &quot;Tabela de leitura&quot; já concedida e a permissão &quot;Gravar email&quot; recém-necessária.

## [!DNL Microsoft OneDrive] módulos e seus campos

Ao configurar módulos do [!DNL OneDrive], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL OneDrive] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Arquivo/Pasta](#filefolder)
* [Outro](#other)

### Arquivo/Pasta

* [[!UICONTROL Copiar um Arquivo]](#copy-a-file)
* [[!UICONTROL Criar uma Pasta]](#create-a-folder)
* [[!UICONTROL Excluir um Arquivo/Pasta]](#delete-a-filefolder)
* [[!UICONTROL Baixar um arquivo]](#download-a-file)
* [[!UICONTROL Obter um arquivo]](#get-a-file)
* [[!UICONTROL Obter um Link de Compartilhamento]](#get-a-share-link)
* [[!UICONTROL Mover um Arquivo/Pasta]](#move-a-filefolder)
* [[!UICONTROL Pesquisar Arquivos/Pastas]](#search-filesfolders)
* [[!UICONTROL Carregar um arquivo]](#upload-a-file)
* [[!UICONTROL Observar arquivos/pastas]](#watch-filesfolders)

#### [!UICONTROL Copiar um Arquivo]

Este módulo de ação copia um arquivo em um novo local de pasta

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (ID de Arquivo e Caminho do Arquivo)]</td> 
   <td>Selecione se deseja identificar o arquivo pela ID do Arquivo ou pelo Caminho do Arquivo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID de Arquivo] / [!UICONTROL Caminho do Arquivo]</td> 
   <td> <p>Selecione como deseja inserir a ID do arquivo ou o Caminho do arquivo:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Inserir Manualmente]</b> </p> <p>Selecione esta opção se desejar inserir a ID ou o caminho diretamente ou mapeá-lo a partir de um módulo anterior.</p> </li> 
     <li> <p><b>[!UICONTROL Selecionar de uma lista]</b> </p> <p>Selecione essa opção se desejar selecionar em uma lista de arquivos ou caminhos disponíveis. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local que contém o arquivo que você deseja copiar:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Insira a ID da unidade que contém o arquivo ou pasta que você deseja copiar.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o site do SharePoint que contém o arquivo que você deseja mover. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade contém o arquivo que você deseja copiar.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione ou mapeie a unidade que contém o arquivo a ser copiado. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL Arquivo] / [!UICONTROL ID Arquivo] / [!UICONTROL Caminho do Arquivo]</p> </td> 
   <td> <p>Se você selecionou [!UICONTROL Inserir Manualmente], insira ou mapeie a ID ou o caminho do arquivo que deseja copiar.</p> <p>Se você selecionou Selecionar na lista, selecione o arquivo que deseja copiar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir um Novo Local de Pasta]</td> 
   <td> <p>Selecione como você deseja inserir o local para o qual deseja copiar o arquivo:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Inserir Manualmente]</b> </p> <p>Selecione esta opção se desejar inserir a ID ou o caminho diretamente ou mapeá-lo a partir de um módulo anterior.</p> </li> 
     <li> <p><b>[!UICONTROL Selecionar de uma lista]</b> </p> <p>Selecione essa opção se desejar selecionar em uma lista de pastas disponíveis. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Novo local do OneDrive]</td> 
   <td> <p>Selecione o local para onde deseja copiar o filtro. Essa opção estará disponível se você optar por selecionar o novo local de pasta em uma lista.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Insira a ID da unidade na qual você deseja copiar o arquivo.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o Site [!DNL SharePoint] para o qual deseja copiar o arquivo. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo no qual deseja copiar o arquivo.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione ou mapeie a unidade que contém a pasta para a qual você deseja copiar o arquivo. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> <p>Se você deixar isso em branco, o arquivo ou pasta só poderá ser copiado no mesmo [!UICONTROL OneDrive].</p> <p>Você pode copiar arquivos e pastas da [!UICONTROL Minha Unidade] para uma [!UICONTROL Unidade do Site] ou para uma [!UICONTROL Unidade do Grupo]. </p> <p>Você pode copiar arquivos de uma unidade do [!UICONTROL Site's Drive] somente para a mesma unidade no mesmo site.</p> <p>Você pode copiar arquivos de uma [!UICONTROL Group's Drive] somente para a mesma unidade no mesmo grupo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td>Insira ou mapeie a pasta para onde deseja mover a cópia ou pasta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Novo Nome de Arquivo Copiado]</td> 
   <td> <p>Insira ou mapeie um nome para a nova cópia do arquivo. Você pode deixar isso em branco se não quiser alterar o nome do arquivo original.</p> <p>O nome deve incluir a extensão de arquivo. Exemplo: <code>file.txt</code></p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- Start audit here-->

#### [!UICONTROL Criar uma Pasta]

Este módulo de ação cria uma nova pasta na unidade especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local onde deseja criar uma pasta:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Selecione a unidade na qual deseja criar uma pasta.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o Site [!DNL SharePoint] onde deseja criar uma pasta. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo que é proprietário da unidade em que você deseja criar uma pasta.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione a unidade na qual deseja criar uma pasta. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td>Se quiser que a nova pasta seja uma subpasta, navegue até a pasta na qual você deseja que ela seja uma subpasta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome da Nova Pasta]</td> 
   <td> <p>Insira ou mapeie um nome para a nova pasta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Se Existir uma Pasta com o Mesmo Nome]</td> 
   <td>Selecione como proceder se um arquivo com o mesmo nome já existir.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Excluir um Arquivo/Pasta]

Este módulo de ação exclui o arquivo selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (ID de Arquivo/Pasta e Caminho)]</td> 
   <td>Selecione se deseja identificar o arquivo pela ID do Arquivo ou pelo Caminho do Arquivo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de Arquivo/Pasta /Inserir um Caminho de Arquivo/Pasta]</td> 
   <td> <p>Selecione como deseja inserir a ID do arquivo ou o Caminho do arquivo:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Inserir Manualmente]</b> </p> <p>Selecione esta opção se desejar inserir a ID ou o caminho diretamente ou mapeá-lo a partir de um módulo anterior.</p> </li> 
     <li> <p><b>[!UICONTROL Selecionar de uma lista]</b> </p> <p>Selecione essa opção se desejar selecionar em uma lista de arquivos ou caminhos disponíveis. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local que deseja pesquisar:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Digite a ID da unidade que contém o arquivo ou pasta que você deseja excluir.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o Site [!DNL SharePoint] que contém o arquivo ou pasta que você deseja excluir. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade contém o arquivo ou pasta que você deseja excluir.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione ou mapeie a unidade que contém o arquivo ou pasta que deseja excluir. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Selecionar [!UICONTROL Arquivo/Pasta]</td> 
   <td>Selecione se deseja excluir um arquivo ou uma pasta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivo] / [!UICONTROL ID Arquivo] / [!UICONTROL Caminho do Arquivo]</td>
   <td> <p>Se você selecionou [!UICONTROL Inserir Manualmente], insira ou mapeie a ID de arquivo ou o caminho do arquivo que deseja excluir.</p> <p>Se você selecionou [!UICONTROL Selecionar] na lista, selecione o arquivo que deseja excluir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Baixar um arquivo]

Este módulo de ação baixa o arquivo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (ID de Arquivo e Caminho do Arquivo)]</td> 
   <td>Selecione se deseja identificar o arquivo pela ID do Arquivo ou pelo Caminho do Arquivo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Insira uma ID de arquivo/Caminho de arquivo</td> 
   <td> <p>Selecione como deseja inserir a ID do arquivo ou o Caminho do arquivo:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Inserir Manualmente]</b> </p> <p>Selecione esta opção se desejar inserir a ID ou o caminho diretamente ou mapeá-lo a partir de um módulo anterior.</p> </li> 
     <li> <p><b>[!UICONTROL Selecionar de uma lista]</b> </p> <p>Selecione essa opção se desejar selecionar em uma lista de arquivos ou caminhos disponíveis. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local que deseja que contenha o arquivo a ser baixado:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Insira a ID da unidade que contém o arquivo que você deseja baixar.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o site do SharePoint que contém o arquivo que você deseja baixar. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade contém o arquivo que você deseja baixar.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione ou mapeie a unidade que contém o arquivo a ser baixado. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivo] / [!UICONTROL ID Arquivo] / [!UICONTROL Caminho do Arquivo]</td>
   <td> <p>Se você selecionou [!UICONTROL Inserir Manualmente], insira ou mapeie a ID do arquivo ou o caminho do arquivo que deseja baixar.</p> <p>Se você selecionou [!UICONTROL Selecionar na lista], selecione o arquivo que deseja baixar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Converter em PDF]</td> 
   <td> <p>Habilite esta opção para converter o arquivo em um arquivo PDF. Você pode converter dos seguintes tipos de arquivos:</p> 
    <table style="table-layout:auto"> 
     <col> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td> 
        <ul> 
         <li> <p> <p>CSV</p> </p> </li> 
         <li> <p> <p>DOC</p> </p> </li> 
         <li> <p> <p>DOCX</p> </p> </li> 
         <li> <p> <p>ODP</p> </p> </li> 
         <li> <p> <p>ODS</p> </p> </li> 
         <li> <p> <p>ODT</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p> <p>VASO</p> </p> </li> 
         <li> <p> <p>POTM</p> </p> </li> 
         <li> <p> <p>POTX</p> </p> </li> 
         <li> <p> <p>PPS</p> </p> </li> 
         <li> <p> <p>PPSX</p> </p> </li> 
         <li> <p> <p>PPSXM</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p>PPT</p> </li> 
         <li> <p>PPTM</p> </li> 
         <li> <p>PPTX</p> </li> 
         <li> <p>RTF</p> </li> 
         <li> <p>XLS</p> </li> 
         <li> <p>XLSX</p> </li> 
        </ul> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um arquivo]

Esse módulo de ação obtém os metadados de um arquivo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (ID de Arquivo e Caminho do Arquivo)]</td> 
   <td>Selecione se deseja identificar o arquivo pela ID do Arquivo ou pelo Caminho do Arquivo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID de Arquivo] / [!UICONTROL Caminho do Arquivo]</td> 
   <td> <p>Selecione como deseja inserir a ID do arquivo ou o Caminho do arquivo:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Inserir Manualmente]</b> </p> <p>Selecione esta opção se desejar inserir a ID ou o caminho diretamente ou mapeá-lo a partir de um módulo anterior.</p> </li> 
     <li> <p><b>[!UICONTROL Selecionar de uma lista]</b> </p> <p>Selecione essa opção se desejar selecionar em uma lista de arquivos ou caminhos disponíveis. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local que deseja pesquisar:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Insira a ID da unidade que contém o arquivo que você deseja obter.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o site do SharePoint que contém o arquivo que você deseja obter. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade contém o arquivo que você deseja obter.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione ou mapeie a unidade que contém o arquivo que você deseja obter. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivo] / [!UICONTROL ID Arquivo] / [!UICONTROL Caminho do Arquivo]</td> 
   <td> <p>Se você selecionou [!UICONTROL Inserir Manualmente], insira ou mapeie a ID de arquivo ou o caminho do arquivo que deseja obter.</p> <p>Se você selecionou [!UICONTROL Selecionar na lista], selecione o arquivo que deseja obter.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter um Link de Compartilhamento]

Este módulo de ação retorna um link de compartilhamento para o arquivo especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (ID de Arquivo e Caminho do Arquivo)]</td> 
   <td>Selecione se deseja identificar o arquivo pela ID do Arquivo ou pelo Caminho do Arquivo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID de Arquivo] / [!UICONTROL Caminho do Arquivo]</td> 
   <td> <p>Selecione como deseja inserir a ID do arquivo ou o Caminho do arquivo:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Inserir Manualmente]</b> </p> <p>Selecione esta opção se desejar inserir a ID ou o caminho diretamente ou mapeá-lo a partir de um módulo anterior.</p> </li> 
     <li> <p><b>[!UICONTROL Selecionar de uma lista]</b> </p> <p>Selecione essa opção se desejar selecionar em uma lista de arquivos ou caminhos disponíveis. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local para o qual deseja recuperar um link de compartilhamento:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Digite a ID da unidade que contém o arquivo para o qual você deseja recuperar um link de compartilhamento.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o site do SharePoint que contém o arquivo para o qual deseja recuperar um link de compartilhamento. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade contém o arquivo para o qual deseja recuperar um link de compartilhamento.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione ou mapeie a unidade que contém o arquivo para o qual você deseja recuperar um link de compartilhamento. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivo] / [!UICONTROL ID Arquivo] / [!UICONTROL Caminho do Arquivo]</td> 
   <td> <p>Se você selecionou [!UICONTROL Inserir Manualmente], insira ou mapeie a ID de arquivo ou o caminho do arquivo para o qual deseja recuperar um link de compartilhamento.</p> <p>Se você selecionou [!UICONTROL Selecionar] na lista, selecione o arquivo para o qual deseja recuperar um link de compartilhamento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de Permissão]</td> 
   <td> <p>Selecione se você deseja que as pessoas com o link possam ler e gravar no arquivo ou somente leitura.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escopo]</td> 
   <td>Selecione se deseja que o arquivo fique disponível para qualquer pessoa com o link ou somente para membros de sua organização que tenham o link.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mover um Arquivo/Pasta]

Este módulo de ação move um arquivo ou pasta para um novo local de pasta

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (ID de Arquivo e Caminho do Arquivo)]</td> 
   <td>Selecione se deseja identificar o arquivo pela ID do Arquivo ou pelo Caminho do Arquivo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de Arquivo/Caminho de Arquivo]</td> 
   <td> <p>Selecione como deseja inserir a ID do arquivo ou o Caminho do arquivo:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Inserir Manualmente]</b> </p> <p>Selecione esta opção se desejar inserir a ID ou o caminho diretamente ou mapeá-lo a partir de um módulo anterior.</p> </li> 
     <li> <p><b>[!UICONTROL Selecionar de uma lista]</b> </p> <p>Selecione essa opção se desejar selecionar em uma lista de arquivos ou caminhos disponíveis. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local que contém o arquivo ou pasta que você deseja mover:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Insira a ID da unidade que contém o arquivo ou pasta que você deseja mover.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o Site [!DNL SharePoint] que contém o arquivo ou pasta que você deseja mover. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade contém o arquivo ou pasta que você deseja mover.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione ou mapeie a unidade que contém o arquivo ou pasta que você deseja mover. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Selecionar [!UICONTROL Arquivo/Pasta]</td> 
   <td>Selecione se deseja mover um arquivo ou uma pasta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL Arquivo] / [!UICONTROL ID Arquivo] / [!UICONTROL Caminho do Arquivo]</p> <p role="rowheader">[!UICONTROL Pasta] / [!UICONTROL ID da Pasta] / [!UICONTROL Caminho da Pasta]</p> </td> 
   <td> <p>Se você selecionou [!UICONTROL Inserir Manualmente], insira ou mapeie a ID ou o caminho do arquivo ou pasta que deseja mover.</p> <p>Se você selecionou [!UICONTROL Selecionar] na lista, selecione o arquivo ou pasta que deseja mover.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir um Novo Local de Pasta]</td> 
   <td> <p>Selecione como você deseja inserir o local para onde deseja mover o arquivo ou pasta:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Inserir Manualmente]</b> </p> <p>Selecione esta opção se desejar inserir a ID ou o caminho diretamente ou mapeá-lo a partir de um módulo anterior.</p> </li> 
     <li> <p><b>[!UICONTROL Selecionar de uma lista]</b> </p> <p>Selecione essa opção se desejar selecionar em uma lista de arquivos ou caminhos disponíveis. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local para onde deseja mover o arquivo ou pasta:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Insira a ID da unidade para onde você deseja mover o arquivo ou pasta.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o Site [!DNL SharePoint] para onde deseja mover o arquivo ou pasta. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo para o qual você deseja mover o arquivo ou pasta.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione ou mapeie a unidade que contém a pasta para a qual você deseja mover o arquivo ou pasta. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> <p>Se você deixar isso em branco, o arquivo ou pasta só poderá ser movido dentro do mesmo [!DNL OneDrive].</p> <p>Você pode mover arquivos e pastas da [!UICONTROL Minha Unidade] para uma [!UICONTROL Unidade do Site] ou uma [!UICONTROL Unidade do Grupo]. </p> <p>Você pode mover arquivos de uma unidade do [!UICONTROL Site's Drive] somente para a mesma unidade no mesmo site.</p> <p>Você pode mover arquivos de uma [!UICONTROL Group's Drive] somente para a mesma unidade no mesmo grupo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td>Insira ou mapeie a pasta para onde deseja mover o arquivo ou pasta.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pesquisar Arquivos/Pastas]

Este módulo de pesquisa retorna arquivos e pastas com base nos critérios definidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local que deseja pesquisar:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Insira a ID da unidade que você deseja que o módulo pesquise.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> <p>Navegue até a pasta na qual deseja que o módulo pesquise. Você também pode inserir uma consulta para filtrar os resultados retornados.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Compartilhado Comigo]</b> </p> <p>O módulo pesquisa arquivos que foram compartilhados com o proprietário da unidade.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o Site [!DNL SharePoint] que você deseja que o módulo pesquise. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade você deseja que o módulo pesquise.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher um Tipo de Item]</td> 
   <td> <p>Selecione se deseja pesquisar arquivos, pastas ou ambos.</p> <p>Observação: não é possível pesquisar pastas em uma unidade [!UICONTROL Compartilhado Comigo].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar um arquivo]

Este módulo de ação faz upload de um arquivo para a pasta especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Inserir (ID e caminho do local da pasta)</td> 
   <td>Selecione se deseja identificar a pasta de destino por ID ou por caminho.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local no qual deseja fazer upload de um arquivo:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Selecione a unidade que contém o arquivo que você deseja obter.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o Site [!DNL SharePoint] que contém a pasta na qual você deseja carregar um arquivo. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade contém a pasta na qual você deseja fazer upload de um arquivo.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Unidade]</td> 
   <td> <p>Selecione a unidade que contém a pasta na qual você deseja fazer upload de um arquivo. Este campo não estará disponível se você tiver selecionado [!UICONTROL Não] no campo [!UICONTROL Habilitar para Inserir uma ID de Unidade].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Se Existir um Arquivo com o Mesmo Nome]</td> 
   <td>Selecione como proceder se um arquivo com o mesmo nome já existir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td>Adicione uma descrição ao arquivo carregado.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observar arquivos/pastas]

Este módulo de acionamento inicia um cenário quando um arquivo ou pasta é criado ou atualizado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Observar Arquivos/Pastas]</td> 
   <td> <p>Selecione como deseja observar arquivos ou pastas:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL por Hora de Criação]</b> </p> <p>Fique atento a novos arquivos ou pastas.</p> </li> 
     <li> <p><b>[!UICONTROL por Tempo Atualizado]</b> </p> <p>Fique atento a arquivos ou pastas existentes atualizados.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher seu local [!DNL OneDrive]]</td> 
   <td> <p>Selecione o local que deseja observar:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Minha Unidade]</b> </p> <p>Selecione se deseja habilitar o módulo para inserir uma ID de unidade.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Sim]</b> </p> <p>Insira a ID da unidade que você deseja que o módulo assista.</p> </li> 
       <li> <p><b>[!UICONTROL Não]</b> </p> <p>Navegue até a pasta que você deseja que o módulo assista. Você também pode inserir uma consulta para filtrar os resultados retornados.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Compartilhado Comigo]</b> </p> <p>O módulo observa os arquivos que foram compartilhados com o proprietário da unidade.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Site]</b> </p> <p>Selecione o site do SharePoint que você deseja que o módulo assista. Sites disponíveis são Sites seguidos pelo usuário conectado.</p> </li> 
     <li> <p><b>[!UICONTROL Unidade do Grupo]</b> </p> <p>Selecione o grupo cuja unidade você deseja que o módulo assista.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher um Tipo de Item]</td> 
   <td> <p>Selecione se deseja observar arquivos, pastas ou ambos.</p> <p>Observação: não é possível procurar pastas em uma unidade [!UICONTROL Compartilhado Comigo].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Outro

#### [!UICONTROL Fazer uma chamada de API]

Este módulo executa uma chamada de API personalizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td>Para obter instruções sobre como conectar sua conta do [!DNL OneDrive] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Insira um caminho relativo para <code>https://graph.microsoft.com</code>. Exemplo:<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   td&gt; <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização para você.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>



## Caso não seja possível fazer upload ou atualizar um arquivo

Há vários problemas possíveis ao carregar ou atualizar um arquivo que falha:

* O arquivo carregado é muito grande e excede o limite de tamanho máximo de arquivo para o plano [!DNL OneDrive] ou você usou toda a cota de armazenamento da sua conta [!DNL OneDrive]. Para obter mais espaço de armazenamento, exclua arquivos existentes do [!DNL OneDrive] ou atualize sua conta do [!DNL OneDrive].
* O OneDrive não permite carregar dois arquivos com o mesmo nome para uma única pasta. Se a pasta de destino contiver um arquivo com o mesmo nome do arquivo que está sendo carregado, a execução do cenário será encerrada com um erro. A solução é simplesmente renomear o arquivo que está sendo carregado. Se o objetivo for atualizar um arquivo, use a ação [!UICONTROL Atualizar um arquivo].
* A pasta selecionada anteriormente, para a qual o arquivo está sendo carregado, não existe mais. O cenário é interrompido e será necessário selecionar a pasta de destino novamente.
