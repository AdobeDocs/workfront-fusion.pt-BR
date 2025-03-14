---
title: Módulos do Google Slides
description: Os módulos do Adobe Workfront Fusion Google Slides permitem criar, atualizar, listar e/ou excluir apresentações e fazer upload de imagens para apresentações em sua conta do Google Slides.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: c9c2957aad4c885a622a80b9f25303517db0c506
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 0%

---

# [!DNL Google Slides] módulos

Os módulos do [!DNL Adobe Workfront Fusion] [!DNL Google Slides] permitem criar, atualizar, listar e/ou excluir apresentações e carregar imagens para apresentações em sua conta do [!DNL Google Slides].

Para usar [!DNL Google Slides] com [!DNL Workfront Fusion], é necessário ter uma conta [!DNL Google]. Se você ainda não tiver uma conta [!DNL Google], crie uma na página de ajuda da Conta [!DNL Google].

Você também precisa de [!DNL Google Slides] em seu [!DNL Google Drive].

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

Para usar módulos [!DNL Google Slides], você deve ter uma conta [!DNL Google].

## Informações da API de slides do Google

O conector de slides do Google usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td> https://slides.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.5.9</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Slides] módulos e seus campos

Ao configurar módulos do [!DNL Google Slides], o Workfront Fusion exibe os campos listados abaixo. Junto com esses, campos [!DNL Google Slides] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Apresentação](#presentation)
* [Outro](#other)

### Apresentação

* [[!UICONTROL Add/Delete a Slide]](#adddelete-a-slide)
* [[!UICONTROL Create a Presentation From a Template]](#create-a-presentation-from-a-template)
* [[!UICONTROL Get a Page/Thumbnail]](#get-a-pagethumbnail)
* [[!UICONTROL Get a Presentation]](#get-a-presentation)
* [[!UICONTROL List Presentations]](#list-presentations)
* [[!UICONTROL Refresh a Chart]](#refresh-a-chart)
* [[!UICONTROL Upload an Image To a Presentation]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Watch Presentations]](#watch-presentations)

#### [!UICONTROL Add/Delete a Slide]

Este módulo de ação cria um slide ou exclui um slide existente na apresentação especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the method]</td> 
   <td> <p>Escolha se deseja adicionar um novo slide ou excluir um slide.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Enter a Slide ID]</td> 
   <td> <p>Se você estiver excluindo um slide, selecione se deseja inserir a ID do slide manualmente ou selecionar o slide em uma lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>Selecione a apresentação ou mapeie a ID da apresentação da apresentação para a qual deseja adicionar ou excluir um slide.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Slide Object ID]</td> 
   <td> <p>Se você estiver excluindo um slide e optar por inseri-lo manualmente, insira ou mapeie a ID do slide. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Predefined layout type]</td> 
   <td> <p> Selecione o layout de slide predefinido a ser usado pelo slide adicionado. Especifique valores para quaisquer campos adicionais (como [!UICONTROL Title]).</p> 
    <ul> 
     <li>[!UICONTROL Blank layout, with no placeholders]</li> 
     <li>[!UICONTROL Layout with a caption at the bottom]</li> 
     <li>[!UICONTROL Layout with a title and subtitle]</li> 
     <li>[!UICONTROL Layout with a title and body]</li> 
     <li>[!UICONTROL Layout with a title and two columns]</li> 
     <li>[!UICONTROL Layout with only a title]</li> 
     <li>[!UICONTROL Layout with a section title]</li> 
     <li>[!UICONTROL Layout with a title and subtitle on one side and description on the other]</li> 
     <li>[!UICONTROL Layout with one title and one body, arranged in a single column]</li> 
     <li>[!UICONTROL Layout with a main point]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>Este campo estará disponível se você selecionou adicionar um slide.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Content]</td> 
   <td> <p>Insira ou mapeie o conteúdo do texto do slide. Os campos estão disponíveis com base no modelo selecionado.</p> <p>Este campo estará disponível se você selecionou adicionar um slide.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Presentation From a Template]

Este módulo de ação cria uma nova apresentação copiando uma apresentação e substituindo todas as marcas como `{{Name}}`, `{{Email}}` por dados fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Insira um nome para a nova apresentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy a Presentation]</td> 
   <td> <p> Selecione a opção se estiver copiando uma apresentação existente:</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy of Existing Presentation ID]</td> 
   <td> <p> Insira o Caminho ou a ID de uma apresentação existente que você deseja copiar. Este campo aparecerá se você estiver criando a apresentação [!UICONTROL By Mapping].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade compartilhada]</li> 
    </ul> <p>Este campo aparecerá se você estiver criando a apresentação [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selecione a apresentação ou insira ou mapeie a ID da Apresentação que você deseja usar como modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>Adicione os valores:</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: digite a tag que deseja substituir na apresentação. Por exemplo, <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong>: digite o valor pelo qual a tag existente deve ser substituída. Por exemplo, se uma cadeia de caracteres <code>&#123;&#123;Name&#125;&#125;</code> na apresentação e o valor substituído for Amostra, então <code>&#123;&#123;Name&#125;&#125;</code> é substituído por <code>Sample</code>.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Drive Location]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde deseja armazenar ou adicione a nova apresentação:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade compartilhada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Document's Location]</p> </td> 
   <td> <p>Selecione a pasta onde deseja armazenar ou adicione a apresentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared] </td> 
   <td> <p>Selecione se deseja compartilhar a apresentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sharing with Other's Email Address]</td> 
   <td> <p> Insira o endereço de email com o qual deseja compartilhar a apresentação. Se você ativar a opção Compartilhado sem inserir um email neste campo, a apresentação será compartilhável com qualquer pessoa.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Page/Thumbnail]

Esse módulo de ação obtém a versão mais recente da página especificada ou da miniatura de uma página na apresentação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Presentation and Page ID]</td> 
   <td> <p> Escolha se deseja inserir uma Apresentação e uma ID de Página manualmente ou selecione-as em uma lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selecione a ID de apresentação que deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page Object ID]</td> 
   <td> <p> Selecione o slide para o qual deseja exibir os detalhes do objeto da página.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Page Thumbnail]</td> 
   <td> <p> Marque a caixa de seleção se desejar exibir as informações de miniatura da página.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Presentation]

Este módulo de ação obtém a versão mais recente de uma apresentação especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade compartilhada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selecione a apresentação que deseja recuperar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Presentations]

Este módulo recupera uma lista de todas as apresentações no local determinado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive location]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade compartilhada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p>Escolha o local da pasta das apresentações que deseja listar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de apresentações que você deseja que o módulo retorne durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Refresh a Chart]

Este módulo de ação atualiza os dados do gráfico armazenados em uma apresentação especificada pela ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Presentation ID]</td> 
   <td> <p> Escolha se deseja inserir uma ID de apresentação manualmente ou selecioná-la em uma lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Se estiver selecionando a apresentação em uma lista, selecione a [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade compartilhada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Selecione a apresentação ou insira ou mapeie a ID de Apresentação da apresentação que inclui o gráfico que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chart Object ID]</td> 
   <td> <p> Se estiver inserindo dados manualmente, insira ou mapeie a ID do gráfico que deseja atualizar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an Image To a Presentation]

Carrega uma imagem com os dados fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Escolha como deseja selecionar a apresentação na qual você está fazendo upload de uma imagem.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Se estiver escolhendo em uma lista suspensa, selecione a [!DNL Google Drive] onde está localizada a apresentação à qual deseja adicionar uma imagem:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade compartilhada]</li> 
    </ul>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selecione a ID da Apresentação da apresentação na qual você está fazendo upload de uma imagem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the Method]</td> 
   <td> <p> Selecione como deseja substituir a imagem.</p>
   <ul>
   <li><p><b>Fazer upload de uma imagem substituindo a tag de texto</b></p><p>No campo Valores, para cada imagem que você deseja carregar, clique em <b>Adicionar item</b> e insira a marca da imagem e a URL da nova imagem.</p></li>
   <li><p><b>Fazer upload de uma imagem substituindo a imagem</b></p><p>No campo Valores, para cada imagem que você deseja carregar, clique em <b>Adicionar item</b> e insira a ID de objeto da imagem, o método de substituição e a URL da nova imagem.</p></li>
   </ul>
  <p>Observação: as imagens devem ter menos de 50 MB, não podem exceder 25 megapixels e devem estar no formato PNG, JPEG ou GIF.</p>   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Presentations]

Esse módulo de acionamento inicia um cenário quando uma nova apresentação é criada ou atualizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch] </td> 
   <td> <p>Selecione a opção para assistir às apresentações:</p> 
    <ul> 
     <li> <p>[!UICONTROL Created Date]</p> </li> 
     <li> <p>[!UICONTROL Modified Date]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Insira ou mapeie o número máximo de apresentações que o Workfront Fusion deve retornar durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outro

* [[!UICONTROL Insert Links in a Presentation]](#insert-links-in-a-presentation)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Insert Links in a Presentation]

Esse módulo torna clicáveis todos os links em uma apresentação ou insere um link em todos os textos de entrada correspondentes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Escolha como deseja selecionar a apresentação na qual você está fazendo upload de uma imagem.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade compartilhada]</li> 
    </ul> <p>Este campo aparecerá se você estiver criando a apresentação [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Escolha o local da pasta das apresentações que deseja listar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select]</td> 
   <td> <p>Selecione se deseja tornar clicáveis todos os links em uma apresentação ou se deseja inserir um link em todos os textos de entrada de correspondência.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text Inputs]</td> 
   <td>Se você estiver inserindo um link, para cada item de texto ao qual deseja adicionar um link, clique em <b>Adicionar item</b> e insira o texto e seu link associado. Toda vez que o item aparece na apresentação, ele é vinculado automaticamente ao site especificado.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Executa uma chamada de API autorizada arbitrária.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao [!DNL Workfront Fusion], consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o [!DNL Adobe Workfront Fusion] - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Insira um caminho relativo para <code>https://developers.google.com/slides/</code>. Por exemplo, Apresentação.</p> <p>Para obter a lista de pontos de extremidade disponíveis, consulte a <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides] Documentação da API</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Insira os cabeçalhos de solicitação desejados. Você não precisa adicionar cabeçalhos de autorização.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Insira a string de consulta da solicitação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Adicione o conteúdo do corpo para a chamada à API na forma de um objeto JSON padrão.</p> <p>Nota:  <p>Ao usar instruções condicionais como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Exemplo:** usando uma chamada de API, você pode obter os detalhes da apresentação para a ID de apresentação inserida. Você pode encontrar a ID da apresentação na URL ao abrir a apresentação em [!DNL Google Slides].

![Exemplo de chamada de API](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)

A chamada de API a seguir retorna os detalhes da apresentação:

![Detalhes da apresentação](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)

Correspondências da pesquisa podem ser encontradas na Saída do módulo em [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL presentationId].

Em nosso exemplo, os detalhes da apresentação solicitada foram retornados:

![Detalhes da apresentação](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

>[!ENDSHADEBOX]
