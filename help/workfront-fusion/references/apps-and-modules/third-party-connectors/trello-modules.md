---
title: Módulos do Trello
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam o Trello, bem como conectá-lo a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '5217'
ht-degree: 0%

---

# [!UICONTROL Trello] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam o [!UICONTROL Trello], bem como conectá-lo a vários aplicativos e serviços de terceiros.

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

Para usar módulos [!DNL Trello], você deve ter uma conta [!UICONTROL Trello].

## Informações da API do Trello

O conector Trello usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## Conectar o [!UICONTROL Trello] a [!DNL Workfront Fusion]

Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte [Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!UICONTROL Trello] módulos e seus campos

Ao configurar módulos do [!UICONTROL Trello], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos adicionais do [!UICONTROL Trello] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Quadros](#boards)
* [Listas](#lists)
* [Cartões](#cards)
* [Membros](#members)
* [Listas de verificação](#checklists)
* [Rótulos](#labels)
* [Comentários](#comments)

### Quadros

+++ **[!UICONTROL Arquivar ou Desarquivar um Quadro]**

Esse módulo de ação fecha (arquiva) ou reabre (desarquiva) um quadro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Quadro]</td> 
   <td> <p> Informe ou mapeie a ID do quadro que você deseja fechar ou reabrir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivar ou desarquivar]</td> 
   <td> <p> Selecione se deseja fechar (arquivar) ou reabrir (desarquivar) o quadro.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Atribuir um membro a um painel]**

Esse módulo de ação atribui um membro a um quadro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Quadro]</td> 
   <td> <p> Selecione o painel em que deseja adicionar um membro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Endereço de email]</td> 
   <td> <p> Insira ou mapeie o endereço de email do membro que deseja adicionar ao quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo de membro]</p> </td> 
   <td> <p>Selecione o tipo de membro que deseja que o novo membro seja.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: um administrador de quadro pode executar qualquer ação de quadro no quadro.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: Um membro normal é simplesmente um membro do quadro.</li> 
     <li><strong>[!UICONTROL Observador]</strong>: Um observador é um membro com acesso somente leitura ao quadro. <br>Os observadores só estão disponíveis para equipes com o [!UICONTROL Trello Business Class].</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome completo]</td> 
   <td> <p> Insira ou mapeie o nome completo do usuário que deseja adicionar ao quadro.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar um painel]**

Este módulo de ação cria um novo quadro com as configurações selecionadas.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome] </td> 
   <td> <p>Informe ou mapeie um nome para o novo quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrição]</td> 
   <td> <p>Informe ou mapeie a descrição do quadro, se necessário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID da Organização]</p> </td> 
   <td> <p>Insira ou mapeie a ID da organização. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nível de permissão]</p> </td> 
   <td> <p>Os painéis têm regras de votação e comentário diferentes para cada nível de permissão. Por exemplo, se o seu painel for [!UICONTROL Privado] e você definir as regras de votação e comentários como [!UICONTROL Tudo], você receberá um erro. </p> <p>A votação e os comentários são limitados aos seguintes grupos para cada nível de permissão:</p> 
    <ul> 
     <li><strong>[!UICONTROL Privado]</strong>: 
      Membros, Membros e Observadores</li> 
     <li><strong>[!UICONTROL Para a organização]</strong>: 
      Membros, Membros e Observadores, Membros da Organização</li> 
     <li><strong>[!UICONTROL Público]</strong>: 
      Membros, Membros e Observadores, Membros da Organização, Todos</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Votação]</p> </td> 
   <td> <p>Selecione uma opção para especificar quem pode votar neste painel. Consulte o campo [!UICONTROL Nível de permissão] para ver as limitações de votação em níveis de permissão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comentários]</p> </td> 
   <td> <p>Selecione uma opção para especificar quem pode comentar em cartões para este quadro. Consulte o campo [!UICONTROL Nível de permissão] para comentar limitações em níveis de permissão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Convites]</p> </td> 
   <td> <p>Selecione quem pode convidar outras pessoas para este painel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL AutoJunção]</p> </td> 
   <td> <p>Selecione se os membros da equipe podem ingressar no painel ou se precisam ser convidados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Rótulos padrão]</p> </td> 
   <td> <p>Selecione se deseja usar o conjunto padrão de rótulos para o novo quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Listas padrão]</p> </td> 
   <td> <p>Selecione se o conjunto padrão de listas deve ser adicionado ao quadro ([!UICONTROL Para Fazer], [!UICONTROL Para Fazer], [!UICONTROL Concluído]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de origem da placa]</p> </td> 
   <td> <p>Selecione ou mapeie a ID do quadro que você deseja copiar para o novo quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tampas de Cartão]</p> </td> 
   <td> <p>Selecione <strong>[!UICONTROL Sim]</strong> se quiser habilitar capas de cartão para o quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Plano de Fundo]</p> </td> 
   <td> <p>Selecione a cor do plano de fundo ou do plano de fundo personalizado.</p> <p>Observação: planos de fundo personalizados estão disponíveis somente para assinantes do [!UICONTROL Trello Gold e Business Class].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Plano de Fundo]</td> 
   <td> <p> Se você optou por usar um plano de fundo personalizado no campo [!UICONTROL Plano de Fundo], digite ou mapeie a ID do plano de fundo que deseja usar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Duração da Placa]</p> </td> 
   <td> <p>Selecione entre dois modos de amadurecimento de cartão. </p> 
    <ul> 
     <li><strong>[!UICONTROL Modo pirata]</strong>: cartões rasgarão, ficarão amarelos e quebrarão como um mapa de pirata antigo à medida que envelhecerem.</li> 
     <li><strong>[!UICONTROL Modo regular &#x200B;]</strong>: Os cartões tornam-se progressivamente mais transparentes à medida que envelhecem. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Editar um painel]**

Este módulo de ação edita as configurações de um quadro existente.

>[!SUCCESS]
>
><table style="table-layout:auto">
><col> 
> <col> 
> <tbody> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Conexão] </td> 
>   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL ID do Quadro]</p> </td> 
>   <td> <p>Insira ou mapeie a ID exclusiva do [!UICONTROL Trello] da placa que você deseja que o módulo crie. Você pode recuperar a ID da placa usando outro módulo, como o módulo Watch Boards</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Novo nome]</td> 
>   <td> <p> Informe ou mapeie um novo nome para o quadro.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Nova descrição]</td> 
>   <td> <p> Informe ou mapeie uma nova descrição do painel de discussão.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL ID da Organização]</p> </td> 
>   <td> <p>Insira ou mapeie a ID exclusiva do [!UICONTROL Trello] do quadro que você deseja que o módulo edite.  </p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Assinar] </td> 
>   <td> <p>Selecione uma opção para especificar se o usuário proprietário da conexão usada por esse módulo está inscrito no quadro.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Nível de permissão]</p> </td> 
>   <td> <p>Os painéis têm regras de votação e comentário diferentes para cada nível de permissão. Por exemplo: se o seu painel for [!UICONTROL Privado] e você definir as regras de votação e comentários como [!UICONTROL Tudo], você receberá um erro. </p> <p>A votação e os comentários são limitados aos seguintes grupos para cada nível de permissão:</p> 
>    <ul> 
>     <li><strong>[!UICONTROL Privado]</strong>: 
>      Membros, Membros e Observadores</li> 
>     <li><strong>[!UICONTROL Para a organização]</strong>: 
>      Membros, Membros e Observadores, Membros da Organização</li> 
>     <li><strong>[!UICONTROL Público]</strong>: 
>      Membros, Membros e Observadores, Membros da Organização, Todos</li> 
>    </ul> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Votação]</p> </td> 
>   <td> <p>Selecione uma opção para especificar quem pode votar neste painel. Consulte o campo [!UICONTROL Nível de permissão] para ver as limitações de votação em níveis de permissão.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Comentários]</p> </td> 
>   <td> <p>Selecione uma opção para especificar quem pode comentar em cartões para este quadro. Consulte o campo [!UICONTROL Nível de permissão] para comentar limitações em níveis de permissão.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Convites] </td> 
>   <td> <p>Selecione quem pode convidar pessoas para este painel.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL AutoJunção]</td> 
>   <td> <p> Selecione se os membros da equipe podem ingressar no painel ou se precisam ser convidados.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Cartão cobre]</td> 
>   <td> <p> Selecione se as capas de cartão devem ser exibidas neste quadro.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Plano de Fundo] </td> 
>   <td> <p>Selecione a cor do plano de fundo ou do plano de fundo personalizado.</p> <p>Observação: planos de fundo personalizados estão disponíveis somente para assinantes do [!UICONTROL Trello Gold e Business Class].</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL ID de Plano de Fundo]</td> 
>   <td> <p> Se você optou por usar um plano de fundo personalizado no campo [!UICONTROL Plano de Fundo], digite ou mapeie a ID do plano de fundo que deseja usar.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Duração da Placa]</p> </td> 
>   <td> <p>Selecione entre dois modos de amadurecimento de cartão. </p> 
>    <ul> 
>     <li><strong>[!UICONTROL Modo pirata]</strong>: cartões rasgarão, ficarão amarelos e quebrarão como um mapa de pirata antigo à medida que envelhecerem.</li> 
>     <li><strong>[!UICONTROL Modo regular]</strong>: os cartões tornam-se progressivamente mais transparentes à medida que envelhecem. </li> 
>    </ul> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Feed de calendário habilitado]</td> 
>   <td> <p> Selecione se o feed de calendário está habilitado ou não.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL &lt;Cor&gt; nome do rótulo]</td> 
>   <td> <p> Atribua um nome ao rótulo de cor desejado.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Arquivo Morto] </td> 
>   <td> <p>Selecione uma opção para indicar se deseja arquivar (fechar) o quadro. </p> </td> 
>  </tr> 
> </tbody> 
></table>


+++

+++ **[!UICONTROL Obter um painel]**

Este módulo de ação recupera os detalhes de um quadro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID do Quadro]</p> </td> 
   <td> <p>Informe ou mapeie o ID do quadro sobre o qual deseja recuperar informações.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

Este módulo de pesquisa recupera informações sobre um quadro especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Consulta] </td> 
   <td> <p>Informe ou mapeie o nome (ou parte do nome) do quadro sobre o qual deseja obter informações.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de quadros retornados]</td> 
   <td> <p> Insira o número máximo de painéis que [!DNL Workfront Fusion] retornará durante um ciclo de execução. Este valor deve ser menor ou igual a 1000.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parcial] </p> </td> 
   <td> <p>Por padrão, esse módulo pesquisa o conteúdo do membro para correspondências exatas de cada palavra na sua consulta. Quando [!UICONTROL Parcial] está habilitado, o módulo procura conteúdo que comece com qualquer palavra na consulta.</p> <p> Por exemplo, se você estiver usando a palavra "desenvolvimento" para procurar um quadro chamado "Meu relatório de status de desenvolvimento", por padrão, seria necessário pesquisar a palavra inteira. Se [!UICONTROL Parcial] estiver habilitado, você poderá pesquisar por "dev", mas não por "desenvolvimento".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quadros] </td> 
   <td> <p>Insira "meu" ou mapeie uma lista separada por vírgulas de IDs de cartão.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Cancelar atribuição de um membro a um painel]**

Este módulo de ação remove um membro de um quadro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Quadro]</td> 
   <td> <p> Insira (mapeie ou selecione) a ID do quadro do qual deseja remover o usuário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Membro] </td> 
   <td> <p>Selecione o membro que deseja remover do painel.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Quadros de Interesse]**

Este módulo de acionamento inicia um cenário quando uma nova placa é adicionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira ou mapeie o número máximo de quadros que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Listas

+++ **[!UICONTROL Criar uma Lista]**

Esse módulo de ação cria uma lista em um quadro que você especifica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Quadro]</td> 
   <td> <p> Insira ou mapeie a ID do quadro em que deseja criar uma lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome] </td> 
   <td> <p>Insira ou mapeie um nome para a nova lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Posição] </td> 
   <td> <p>Selecione se deseja adicionar a lista à parte superior ou anexá-la à parte inferior do cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copiar lista]</td> 
   <td> <p> Se estiver copiando uma lista, selecione como deseja inserir a ID da lista que deseja copiar.</p> 
    <ul> 
     <li> <p><strong>Inserir manualmente</strong> </p> <p>No campo <strong>[!UICONTROL ID de Lista]</strong>, insira ou mapeie a ID da lista que deseja copiar.<br></p> </li> 
     <li> <p><strong>Selecionar</strong> </p> <p>Selecione o quadro que contém a lista que você deseja copiar e selecione a lista.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Editar uma Lista]**

Este módulo de ação edita uma lista existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Lista]</td> 
   <td> <p> Insira ou mapeie a ID da lista que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome] </td> 
   <td> <p>Insira ou mapeie um novo nome para a lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Quadro]</td> 
   <td> <p> Mapeie ou selecione o quadro para onde deseja mover a lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Posição] </td> 
   <td> <p>Selecione se deseja adicionar a lista à parte superior ou anexá-la à parte inferior do cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assinado]</td> 
   <td> <p>Ative esta opção se quiser inscrever o membro ativo na lista.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obter uma Lista]**

Este módulo de ação recupera detalhes sobre uma lista específica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID de Lista]</p> </td> 
   <td> <p>Insira ou mapeie a ID da lista da qual deseja recuperar informações.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Cartões de visita movidos para uma lista]**

Esse módulo acionador é ativado quando um cartão é movido para uma lista específica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board]</td> 
   <td>Selecione o quadro que contém a lista que você deseja observar para os cartões.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lista]</td> 
   <td>Selecione a lista que deseja observar com relação aos cartões.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Cartões

+++ **[!UICONTROL Adicionar Anexo]**

Esse módulo de ação adiciona um anexo ao cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID do cartão]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão ao qual deseja adicionar um anexo.</p> 
    <ul> 
     <li> <p><strong>Inserir manualmente</strong> </p> <p>No campo <strong>[!UICONTROL ID de Cartão]</strong>, digite ou mapeie a ID do cartão ao qual deseja adicionar um anexo.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar um anexo e selecione a lista que contém o cartão e, em seguida, selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo de anexo]</p> </td> 
   <td> <p>Selecione se deseja fazer upload do arquivo diretamente ou fornecer um URL para o arquivo.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Arquivo]</strong> </p> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </li> 
     <li> <p><strong></strong> </p> <p>Insira a URL do arquivo e forneça um nome para o anexo.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Arquivar ou Desarquivar um Cartão]**

Esse módulo de ação arquiva ou envia um cartão de volta para a placa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Cartão]</td> 
   <td> <p> Insira ou mapeie a ID do cartão que deseja arquivar ou enviar de volta para o quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivar ou desarquivar]</td> 
   <td> <p> Selecione se deseja fechar o cartão (arquivar) ou enviá-lo de volta para o quadro (desarquivar).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar um cartão]**

Esse módulo de ação cria um cartão em uma lista selecionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de lista]</td> 
   <td> <p> Selecione como você deseja inserir a ID da lista à qual deseja adicionar um cartão.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Lista]</strong>, digite ou mapeie a ID da lista à qual deseja adicionar um cartão.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém a lista à qual deseja adicionar um cartão e selecione a lista.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rótulos] </td> 
   <td> <p>Para cada rótulo que você deseja adicionar ao cartão, clique em <b>Adicionar item</b> e insira a ID do rótulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Membros]</td> 
   <td>Para cada membro que você deseja adicionar ao cartão, clique em <b>Adicionar item</b> e insira a ID do membro. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome] </td> 
   <td> <p>Insira um nome para o novo cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Descrição]</p> </td> 
   <td> <p>Insira a descrição do cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Posição] </td> 
   <td> <p>Selecione se deseja adicionar o cartão à parte superior ou anexá-lo à parte inferior da lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data de vencimento]</td> 
   <td> <p> Insira uma data de vencimento para o cartão. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conclusão de conclusão]</td> 
   <td> <p> Habilite essa opção para marcar o cartão como concluído na data de vencimento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL do Arquivo]</td> 
   <td> <p>Insira ou mapeie o URL de um arquivo que você deseja adicionar como anexo ao cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL arquivo Source]</p> </td> 
   <td> <p>Insira ou mapeie informações para um arquivo que deseja adicionar como anexo ao cartão. Selecione um arquivo de um módulo anterior ou mapeie o nome e os dados do arquivo</p> 
     <p>Observação: há um limite de upload de arquivo de 10 MB por anexo. No entanto, os membros da [!UICONTROL Business Class] e do [!UICONTROL Trello Gold] têm um limite de carregamento de arquivo de 250 MB por anexo.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copiar cartão]</td> 
   <td> <p> Se estiver criando um novo cartão como uma cópia de um cartão existente, selecione como deseja inserir a ID do cartão que deseja copiar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Cartão]</strong>, digite ou mapeie a ID do cartão que você deseja copiar.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão que deseja copiar, selecione a lista que contém o cartão e selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Editar um cartão]**

Esse módulo de ação edita um cartão existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID de Cartão]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão que deseja editar.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Cartão]</strong>, digite ou mapeie a ID do cartão que deseja editar.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão que deseja editar, selecione a lista que contém o cartão e selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Novo nome]</td> 
   <td> <p>Insira ou mapeie um novo nome para o cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nova descrição]</p> </td> 
   <td> <p>Insira ou mapeie uma nova descrição para o cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Mover um cartão]</p> </td> 
   <td> <p>Selecione o quadro ou o quadro e a lista para onde deseja mover o cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rótulos] </td> 
   <td> <p>Para cada rótulo que você deseja adicionar ao cartão, clique em <b>Adicionar item</b> e insira a ID do rótulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Posição] </td> 
   <td> <p>Selecione se deseja adicionar o cartão à parte superior ou [!UICONTROL append] o cartão à parte inferior da lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data de vencimento]</td> 
   <td> <p> Insira uma data de vencimento para o cartão. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conclusão de conclusão]</td> 
   <td> <p> Habilite essa opção para marcar o cartão como concluído na data de vencimento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Membros] </td> 
   <td> <p>Para cada membro que você deseja adicionar ao cartão, clique em <b>Adicionar item</b> e insira ou mapeie a ID do membro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID da capa do anexo]</p> </td> 
   <td> <p>Insira ou mapeie a ID do anexo de imagem que você deseja que o cartão use como capa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assinar] </td> 
   <td> <p>Selecione se o membro deve assinar o cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arquivo Morto] </td> 
   <td> <p>Selecione uma opção para indicar se deseja arquivar (fechar) o cartão. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obter um Cartão]**

Esse módulo de ação recupera os detalhes de um cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID do Quadro]</td> 
   <td> <p>Insira a ID do quadro que contém o cartão sobre o qual deseja recuperar detalhes. Isso permite que você veja os nomes dos campos personalizados do quadro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID do cartão]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão sobre o qual deseja recuperar detalhes.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Cartão]</strong>, digite ou mapeie a ID do cartão sobre o qual deseja recuperar detalhes.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão do qual deseja recuperar detalhes e selecione a lista que contém o cartão e, em seguida, selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Procurar Cartões]**

Este módulo de ação retorna cartões que correspondem à consulta de pesquisa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board] </td> 
   <td> <p>Selecione os painéis de discussão que deseja pesquisar. Se nenhum painel for selecionado, todos os painéis serão pesquisados.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Consulta]</p> </td> 
   <td> <p>Insira a consulta de pesquisa. Você pode refinar sua pesquisa usando os seguintes operadores de pesquisa:</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>Você pode adicionar "-" a qualquer operador para fazer uma pesquisa negativa, como <code>[!UICONTROL -has:members]</code> para procurar cartões sem nenhum membro atribuído.</p> </li> 
     <li><code><strong>@name</strong></code> <p>Retorna cartões atribuídos a um membro. Você também pode usar <code>member:</code>. Use o <code>@me</code> para incluir apenas seus cartões.</p> </li> 
     <li><code><strong>#label</strong></code> <p>Retorna cartões rotulados. Você também pode usar <code>label:</code>. Por exemplo, <code>label:"FIX IT"</code> retornará cartões com o rótulo chamado "CORRIGIR".</p> </li> 
     <li><code><strong>board:id</strong></code> <p>Retorna cartões em um quadro específico. Por exemplo, <code>board:Trello</code> retornará cartões em quadros com [!UICONTROL Trello] no nome do quadro.</p> </li> 
     <li><code><strong>list:name</strong></code> <p>Retorna cartões dentro da lista chamada "nome".</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>Retorna cartões com anexos. O operador <code>has</code>: também pode ser usado com outros atributos, como <code>has:description</code>, <code>has:cover</code>, <code>has:members</code> ou <code>has:stickers</code>.</p> </li> 
     <li><code><strong>due:day</strong></code> <p>Retorna cartões com vencimento em 24 horas. O operador <code>due:</code> também pode ser usado com outros períodos, como <code>due:week</code>, <code>due:month</code> ou <code>due:overdue</code>. Você também pode procurar um intervalo de dias específico. Por exemplo, adicionar <code>due:14</code> à pesquisa inclui cartões com vencimento nos próximos 14 dias.</p> </li> 
     <li><code><strong>created:day</strong></code> <p>Retorna cartões criados nas últimas 24 horas. O operador <code> created:</code> também pode ser usado com outros cronogramas, como <code>created:week</code> ou <code>created:month</code>. Você também pode procurar um intervalo de dias específico. Por exemplo, adicionar <code>created:14</code> à pesquisa inclui cartões criados nos últimos 14 dias.</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>Retorna cartões editados nas últimas 24 horas. O operador <code>edited:</code> também pode ser usado com outros intervalos de tempo, como <code>edited:week</code> ou <code>edited:month</code>. Você também pode procurar um intervalo de dias específico. Por exemplo, adicionar <code>edited:21</code> à pesquisa inclui cartões editados nos últimos 21 dias.</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>Retorna cartões que correspondem ao texto de descrições, listas de verificação, comentários ou nomes de cartões. Por exemplo, <code>comment:"FIX IT"</code> retornará cartões com "CORRIGIR" em um comentário.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>Retorna cartões abertos ou arquivados. Se nenhum dos dois for especificado, o [!UICONTROL Trello] retornará os dois tipos.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>Inclui apenas cartões em quadros estrelados.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de cartões retornados]</td> 
   <td> <p> Insira ou mapeie o número máximo de cartões que você deseja que [!DNL Workfront Fusion] retorne durante um ciclo de execução. Este valor deve ser menor ou igual a 1000.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parcial] </td> 
   <td> <p>Por padrão, esse módulo pesquisa o conteúdo do membro para correspondências exatas de cada palavra na sua consulta. Quando [!UICONTROL Parcial] está habilitado, o módulo procura conteúdo que comece com qualquer palavra na consulta.</p> <p> Por exemplo, se você estiver usando a palavra "desenvolvimento" para procurar um quadro chamado "Meu relatório de status de desenvolvimento", por padrão, seria necessário pesquisar a palavra inteira. Se [!UICONTROL Parcial] estiver habilitado, você poderá pesquisar por "dev", mas não por "desenvolvimento".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cartões] </td> 
   <td> <p>Para pesquisar cartões específicos, clique em <b>Adicionar item</b> e adicione a ID do cartão.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assistir cartões]**

Esse módulo de acionamento inicia um cenário quando uma nova placa é adicionada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL objeto Observado]</td> 
   <td> <p>Selecione o local que deseja observar para os cartões.</p> 
    <ul> 
     <li><strong>[!UICONTROL Todos os cartões]</strong> </li> 
     <li> <p><strong>Cartões no painel específico</strong> </p> <p>Selecione o painel que deseja observar para os cartões</p> </li> 
     <li> <p><strong>[!UICONTROL Cartões na lista específica]</strong> </p> <p>Selecione o quadro que contém a lista que você deseja observar para os cartões e selecione a lista.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Membros

+++ **[!UICONTROL Adicionar um membro a um cartão]**

Esse módulo de ação adiciona o membro especificado ao cartão especificado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserir ID do cartão e ID do membro]</p> </td> 
   <td> <p>Escolha como você deseja inserir a ID do cartão e a ID do membro.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>Insira ou mapeie a <strong>[!UICONTROL ID de Cartão]</strong> e a <strong>[!UICONTROL ID de Membro]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o painel que contém o cartão ao qual deseja adicionar um membro e selecione a lista que contém o cartão, o próprio cartão e o membro que deseja adicionar ao cartão.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Atribuir um membro a um painel]**

Consulte &quot;[!UICONTROL Atribuir um membro a um painel]&quot; em [painéis](#boards).

+++

+++ **[!UICONTROL Procurar Membros]**

Este módulo de ação recupera informações sobre membros do [!UICONTROL Trello].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Consulta] </td> 
   <td> <p>Informe o nome ou o nome de usuário do usuário que deseja localizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parcial] </td> 
   <td> <p>Por padrão, esse módulo pesquisa o conteúdo do membro para correspondências exatas de cada palavra na sua consulta. Quando [!UICONTROL Parcial] está habilitado, o módulo procura conteúdo que comece com qualquer palavra na consulta.</p> <p> Por exemplo, se você estiver usando a palavra "desenvolvimento" para procurar um quadro chamado "Meu relatório de status de desenvolvimento", por padrão, seria necessário pesquisar a palavra inteira. Se [!UICONTROL Parcial] estiver habilitado, você poderá pesquisar por "dev", mas não por "desenvolvimento".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de membros retornados]</td> 
   <td> <p>Insira ou mapeie o número máximo de registros que deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Cancelar atribuição de um membro a um painel]**

Consulte &quot;[!UICONTROL Cancelar atribuição de um membro de um painel]&quot; em [painéis](#boards).

+++

### Listas de verificação

+++ **[!UICONTROL Criar uma Lista de Verificação]**

Esse módulo de ação cria uma lista de verificação no cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de cartão]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão no qual deseja adicionar uma lista de verificação.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Cartão]</strong>, digite ou mapeie a ID do cartão ao qual deseja adicionar uma lista de verificação.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar uma lista de verificação, selecione a lista que contém o cartão e selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome] </td> 
   <td> <p>Insira ou mapeie um nome para a lista de verificação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Posição] </td> 
   <td> <p>Selecione se deseja adicionar a lista de verificação à parte superior ou anexar a lista de verificação à parte inferior do cartão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserir ID de lista de verificação]</p> </td> 
   <td> <p>Se você estiver criando a lista de verificação copiando uma lista de verificação existente, informe ou mapeie o ID de uma lista de verificação de origem que você deseja copiar para a nova.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Criar um Item da Lista de Verificação]**

Este módulo de ação adiciona um item a uma lista de verificação específica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID de lista de verificação]</td> 
   <td> <p> Se você estiver criando uma nova lista de verificação copiando uma lista de verificação existente, selecione como deseja informar o ID da lista de verificação à qual deseja adicionar um item.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID da Lista de Verificação]</strong>, digite ou mapeie a ID do cartão no qual deseja adicionar uma lista de verificação.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar uma lista de verificação e selecione a lista que contém o cartão, em seguida, selecione o cartão e selecione a lista de verificação.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nome do Item]</p> </td> 
   <td> <p>Insira ou mapeie um nome para o novo item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Posição]</p> </td> 
   <td> <p>Selecione se deseja adicionar o item à parte superior ou [!UICONTROL append] à parte inferior da lista de verificação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verificado]</p> </td> 
   <td> <p>Habilite esta opção se você deseja adicionar o item como já selecionado.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Editar um Item da Lista de Verificação]**

Este módulo de ação edita uma lista de verificação existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de Cartão e uma ID de Item de Lista de Verificação]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão e a lista de verificação onde deseja editar um item.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID da Lista de Verificação]</strong>, digite ou mapeie a ID do cartão no qual deseja adicionar uma lista de verificação.</p> <p>No campo <strong>[!UICONTROL ID do Item da Lista de Verificação]</strong>, insira ou mapeie a ID da lista de verificação.</p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar uma lista de verificação e selecione a lista que contém o cartão, em seguida, selecione o cartão e selecione a lista de verificação.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Lista de Verificação]</td> 
   <td>Selecione ou mapeie a lista de verificação para a qual você deseja mover o item da lista.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nome do Item]</p> </td> 
   <td> <p>Insira ou mapeie um nome para o novo item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Posição]</p> </td> 
   <td> <p>Selecione se deseja adicionar o item à parte superior ou anexar à parte inferior da lista de verificação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Estado]</p> </td> 
   <td> <p>Selecione se o item da lista de verificação está completo ou incompleto.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Rótulos

+++ **[!UICONTROL Adicionar um Rótulo a um Cartão]**

Esse módulo de ação adiciona um rótulo a um cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir ID do cartão]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão no qual deseja adicionar uma lista de verificação.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Cartão]</strong>, digite ou mapeie a ID do cartão ao qual deseja adicionar uma lista de verificação. No campo<strong>[!UICONTROL ID de Rótulo]</strong>, digite ou mapeie a ID do rótulo que deseja adicionar.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar uma lista de verificação, selecione a lista que contém o cartão e selecione o cartão. </p> <p>Selecione o rótulo que deseja adicionar ao cartão.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Comentários

+++ **[!UICONTROL Criar um Comentário em um Cartão]**

Esse módulo de ação adiciona um comentário a um cartão selecionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de cartão]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão ao qual deseja adicionar um comentário.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Cartão]</strong>, digite ou mapeie a ID do cartão ao qual deseja adicionar um comentário.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar um comentário e selecione a lista que contém o cartão e, em seguida, selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comentário] </td> 
   <td> <p>Insira ou mapeie o comentário que deseja adicionar ao cartão selecionado.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Listar comentários em um cartão]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de cartão]</td> 
   <td> <p> Selecione como você deseja inserir a ID do cartão ao qual deseja adicionar um comentário.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Inserir manualmente]</strong> </p> <p>No campo <strong>[!UICONTROL ID de Cartão]</strong>, digite ou mapeie a ID do cartão ao qual deseja adicionar um comentário.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Selecionar]</strong> </p> <p>Selecione o quadro que contém o cartão ao qual deseja adicionar um comentário e selecione a lista que contém o cartão e, em seguida, selecione o cartão.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Número máximo de comentários retornados]</td> 
   <td> <p> Insira o número máximo de comentários que [!DNL Workfront Fusion] retornará durante um ciclo de execução.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Desde] </td> 
   <td> <p>Defina a data de início do período em que o comentário foi criado. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Antes] </td> 
   <td> <p>Defina a data final do período em que o comentário foi criado. Para obter uma lista de formatos de data e hora com suporte, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coerção de tipo em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assistir Comentários]**

Esse módulo de acionador inicia um cenário quando um comentário é adicionado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!UICONTROL Trello] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL objeto Observado]</td> 
   <td> <p>Selecione o local que deseja observar para comentários.</p> 
    <ul> 
     <li><strong>[!UICONTROL Todos os cartões] em todos os lugares</strong> </li> 
     <li> <p><strong>[!UICONTROL Board]</strong> </p> <p>Selecione o painel que deseja observar para comentários</p> </li> 
     <li> <p><strong>[!UICONTROL Lista]</strong> </p> <p>Selecione o painel que contém a lista que você deseja observar para comentários e, em seguida, selecione a lista.</p> </li> 
     <li><strong>[!UICONTROL Card]</strong> </li> 
     <li>Selecione o quadro que contém o cartão que você deseja observar para comentários, selecione a lista que contém o cartão e selecione o cartão.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite] </td> 
   <td> <p>Insira ou mapeie o número máximo de comentários que você deseja que o módulo retorne durante cada ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL Trello] IDs de Objeto

* [Como localizar a ID ou o link curto de um cartão no  [!DNL Trello]](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [Como localizar IDs de outros objetos no  [!DNL Trello]](#how-to-find-ids-of-other-objects-in-trello)

### Como encontrar a ID ou o link curto de um cartão no [!DNL Trello]

Se quiser editar um cartão ou criar um novo comentário, é necessário saber a ID do cartão ou seu link curto. Essas informações podem ser obtidas na saída do acionador [!UICONTROL Novo cartão]. O link curto para um cartão também pode ser obtido abrindo o cartão e clicando no botão [!UICONTROL Compartilhar]. O link curto pode ser encontrado na caixa [!UICONTROL Link para este cartão], no final da URL após `https://trello.com/c/`.

![Compartilhar e muito mais](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### Como encontrar IDs de outros objetos em [!DNL Trello]

As IDs de quadro, lista e comentário só podem ser obtidas usando acionadores. O site do [!DNL `trello.com`] não mostra essas IDs.
