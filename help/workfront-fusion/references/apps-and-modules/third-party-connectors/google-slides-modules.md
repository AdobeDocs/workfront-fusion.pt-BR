---
title: Módulos do Google Slides
description: Os módulos do Adobe Workfront Fusion Google Slides permitem criar, atualizar, listar e/ou excluir apresentações e fazer upload de imagens para apresentações em sua conta do Google Slides.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 0%

---

# [!DNL Google Slides] módulos

Os módulos do Adobe Workfront Fusion [!DNL Google Slides] permitem criar, atualizar, listar e/ou excluir apresentações e carregar imagens para apresentações em sua conta do [!DNL Google Slides].

Para usar o [!DNL Google Slides] com o Workfront Fusion, é necessário ter uma conta [!DNL Google]. Se você ainda não tiver uma conta [!DNL Google], crie uma na página de ajuda da Conta [!DNL Google].

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

Para usar módulos [!DNL Google Slides], você deve ter uma conta [!DNL Google].

## Informações da API de slides do Google

O conector de slides do Google usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
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
* [Outras](#other)

### Apresentação

* [[!UICONTROL Adicionar/Excluir um Slide]](#adddelete-a-slide)
* [[!UICONTROL Criar uma Apresentação de um Modelo]](#create-a-presentation-from-a-template)
* [[!UICONTROL Obter uma Página/Miniatura]](#get-a-pagethumbnail)
* [[!UICONTROL Obter uma Apresentação]](#get-a-presentation)
* [[!UICONTROL Listar Apresentações]](#list-presentations)
* [[!UICONTROL Atualizar um Gráfico]](#refresh-a-chart)
* [[!UICONTROL Carregar uma Imagem para uma Apresentação]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Assistir a Apresentações]](#watch-presentations)

#### [!UICONTROL Adicionar/Excluir um Slide]

Este módulo de ação cria um slide ou exclui um slide existente na apresentação especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar o método]</td> 
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
   <td role="rowheader">[!UICONTROL Tipo de layout predefinido]</td> 
   <td> <p> Selecione o layout de slide predefinido a ser usado pelo slide adicionado. Especifique valores para quaisquer campos adicionais (como [!UICONTROL Título]).</p> 
    <ul> 
     <li>[!UICONTROL Layout em branco, sem espaços reservados]</li> 
     <li>[!UICONTROL Layout com uma legenda na parte inferior]</li> 
     <li>[!UICONTROL Layout com um título e subtítulo]</li> 
     <li>[!UICONTROL Layout com um título e um corpo]</li> 
     <li>[!UICONTROL Layout com um título e duas colunas]</li> 
     <li>[!UICONTROL Layout com apenas um título]</li> 
     <li>[!UICONTROL Layout com um título de seção]</li> 
     <li>[!UICONTROL Layout com título e subtítulo em um lado e descrição no outro]</li> 
     <li>[!UICONTROL Layout com um título e um corpo, organizados em uma única coluna]</li> 
     <li>[!UICONTROL Layout com um ponto principal]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>Este campo estará disponível se você selecionou adicionar um slide.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Content]</td> 
   <td> <p>Insira ou mapeie o conteúdo do texto do slide. Os campos estão disponíveis com base no modelo selecionado.</p> <p>Este campo estará disponível se você selecionou adicionar um slide.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Criar uma Apresentação de um Modelo]

Este módulo de ação cria uma nova apresentação copiando uma apresentação e substituindo todas as marcas como `{{Name}}`, `{{Email}}` por dados fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Título] </td> 
   <td> <p>Insira um nome para a nova apresentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copiar uma Apresentação]</td> 
   <td> <p> Selecione a opção se estiver copiando uma apresentação existente:</p> 
    <ul> 
     <li>[!UICONTROL Por Mapeamento]</li> 
     <li>[!UICONTROL Por Lista Suspensa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cópia de ID de Apresentação Existente]</td> 
   <td> <p> Insira o Caminho ou a ID de uma apresentação existente que você deseja copiar. Este campo aparecerá se você estiver criando a apresentação [!UICONTROL Por Mapeamento].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher uma unidade]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado Comigo]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade Compartilhada]</li> 
    </ul> <p>Este campo aparecerá se você estiver criando a apresentação [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Apresentação]</td> 
   <td> <p> Selecione a apresentação ou insira ou mapeie a ID da Apresentação que você deseja usar como modelo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valores] </td> 
   <td> <p>Adicione os valores:</p> 
    <ul> 
     <li><strong>[!UICONTROL Marca]</strong>: Insira a marca que você deseja substituir na apresentação. Por exemplo, <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Valor Substituído]</strong>: Insira o valor pelo qual a marca existente será substituída. Por exemplo, se uma cadeia de caracteres <code>&#123;&#123;Name&#125;&#125;</code> na apresentação e o valor substituído for Amostra, então <code>&#123;&#123;Name&#125;&#125;</code> é substituído por <code>Sample</code>.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Local da Nova Unidade]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde deseja armazenar ou adicione a nova apresentação:</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado Comigo]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade Compartilhada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Local do Novo Documento]</p> </td> 
   <td> <p>Selecione a pasta onde deseja armazenar ou adicione a apresentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compartilhado] </td> 
   <td> <p>Selecione se deseja compartilhar a apresentação.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compartilhando com o Endereço de Email de Outro Usuário]</td> 
   <td> <p> Insira o endereço de email com o qual deseja compartilhar a apresentação. Se você ativar a opção Compartilhado sem inserir um email neste campo, a apresentação será compartilhável com qualquer pessoa.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma Página/Miniatura]

Esse módulo de ação obtém a versão mais recente da página especificada ou da miniatura de uma página na apresentação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma Apresentação e uma ID de Página]</td> 
   <td> <p> Escolha se deseja inserir uma Apresentação e uma ID de Página manualmente ou selecione-as em uma lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Apresentação]</td> 
   <td> <p> Selecione a ID de apresentação que deseja recuperar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Objeto de Página]</td> 
   <td> <p> Selecione o slide para o qual deseja exibir os detalhes do objeto da página.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostrar Miniatura de Página]</td> 
   <td> <p> Marque a caixa de seleção se desejar exibir as informações de miniatura da página.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obter uma Apresentação]

Este módulo de ação obtém a versão mais recente de uma apresentação especificada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher uma unidade]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado Comigo]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade Compartilhada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Apresentação]</td> 
   <td> <p> Selecione a apresentação que deseja recuperar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listar Apresentações]

Este módulo recupera uma lista de todas as apresentações no local determinado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher um local de unidade]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado Comigo]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade Compartilhada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Pasta]</td> 
   <td> <p>Escolha o local da pasta das apresentações que deseja listar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de apresentações que você deseja que o módulo retorne durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Atualizar um Gráfico]

Este módulo de ação atualiza os dados do gráfico armazenados em uma apresentação especificada pela ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir uma ID de Apresentação]</td> 
   <td> <p> Escolha se deseja inserir uma ID de apresentação manualmente ou selecioná-la em uma lista.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher uma unidade]</td> 
   <td> <p>Se estiver selecionando a apresentação em uma lista, selecione a [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado Comigo]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade Compartilhada]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Apresentação]</td> 
   <td> <p>Selecione a apresentação ou insira ou mapeie a ID de Apresentação da apresentação que inclui o gráfico que você deseja atualizar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Objeto de Gráfico]</td> 
   <td> <p> Se estiver inserindo dados manualmente, insira ou mapeie a ID do gráfico que deseja atualizar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carregar uma Imagem para uma Apresentação]

Carrega uma imagem com os dados fornecidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher uma Apresentação]</td> 
   <td> <p>Escolha como deseja selecionar a apresentação na qual você está fazendo upload de uma imagem.</p> 
    <ul> 
     <li>[!UICONTROL Por Mapeamento]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher uma unidade]</td> 
   <td> <p>Se estiver escolhendo em uma lista suspensa, selecione a [!DNL Google Drive] onde está localizada a apresentação à qual deseja adicionar uma imagem:</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado Comigo]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade Compartilhada]</li> 
    </ul>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Apresentação]</td> 
   <td> <p> Selecione a ID da Apresentação da apresentação na qual você está fazendo upload de uma imagem.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar o Método]</td> 
   <td> <p> Selecione como deseja substituir a imagem.</p>
   <ul>
   <li><p><b>Fazer upload de uma imagem substituindo a tag de texto</b></p><p>No campo Valores, para cada imagem que você deseja carregar, clique em <b>Adicionar item</b> e insira a marca da imagem e a URL da nova imagem.</p></li>
   <li><p><b>Fazer upload de uma imagem substituindo a imagem</b></p><p>No campo Valores, para cada imagem que você deseja carregar, clique em <b>Adicionar item</b> e insira a ID de objeto da imagem, o método de substituição e a URL da nova imagem.</p></li>
   </ul>
  <p>Observação: as imagens devem ter menos de 50 MB, não podem exceder 25 megapixels e devem estar no formato PNG, JPEG ou GIF.</p>   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assistir a Apresentações]

Esse módulo de acionamento inicia um cenário quando uma nova apresentação é criada ou atualizada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Observar] </td> 
   <td> <p>Selecione a opção para assistir às apresentações:</p> 
    <ul> 
     <li> <p>[!UICONTROL Data de Criação]</p> </li> 
     <li> <p>[!UICONTROL Data de Modificação]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Insira ou mapeie o número máximo de apresentações que o Workfront Fusion deve retornar durante um ciclo de execução de cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Outras

* [[!UICONTROL Inserir Links em uma Apresentação]](#insert-links-in-a-presentation)
* [[!UICONTROL Fazer uma chamada de API]](#make-an-api-call)

#### [!UICONTROL Inserir Links em uma Apresentação]

Esse módulo torna clicáveis todos os links em uma apresentação ou insere um link em todos os textos de entrada correspondentes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher uma Apresentação]</td> 
   <td> <p>Escolha como deseja selecionar a apresentação na qual você está fazendo upload de uma imagem.</p> 
    <ul> 
     <li>[!UICONTROL Por Mapeamento]</li> 
     <li>[!UICONTROL Por Lista Suspensa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Escolher uma unidade]</td> 
   <td> <p>Selecione o [!DNL Google Drive] onde estão localizadas as apresentações que deseja listar:</p> 
    <ul> 
     <li>[!UICONTROL Minha Unidade]</li> 
     <li>[!UICONTROL Compartilhado Comigo]</li> 
     <li>[!UICONTROL [!DNL Google] Unidade Compartilhada]</li> 
    </ul> <p>Este campo aparecerá se você estiver criando a apresentação [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID da Apresentação]</td> 
   <td> <p>Escolha o local da pasta das apresentações que deseja listar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selecionar]</td> 
   <td> <p>Selecione se deseja tornar clicáveis todos os links em uma apresentação ou se deseja inserir um link em todos os textos de entrada de correspondência.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entradas de Texto]</td> 
   <td>Se você estiver inserindo um link, para cada item de texto ao qual deseja adicionar um link, clique em <b>Adicionar item</b> e insira o texto e seu link associado. Toda vez que o item aparece na apresentação, ele é vinculado automaticamente ao site especificado.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fazer uma chamada de API]

Executa uma chamada de API autorizada arbitrária.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão] </td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Google Slides] ao Workfront Fusion, consulte <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Criar uma conexão com o Adobe Workfront Fusion - Instruções básicas</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Insira um caminho relativo para <code>https://developers.google.com/slides/</code>. Por exemplo, Apresentação.</p> <p>Para obter a lista de pontos de extremidade disponíveis, consulte a <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides] Documentação da API</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Método]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Insira os cabeçalhos de solicitação desejados. Você não precisa adicionar cabeçalhos de autorização.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta]</td> 
   <td> <p> Insira a string de consulta da solicitação.</p> </td> 
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

>[!BEGINSHADEBOX]

**Exemplo:** usando uma chamada de API, você pode obter os detalhes da apresentação para a ID de apresentação inserida. Você pode encontrar a ID da apresentação na URL ao abrir a apresentação em [!DNL Google Slides].

![Exemplo de chamada de API](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)

A chamada de API a seguir retorna os detalhes da apresentação:

![Detalhes da apresentação](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)

Correspondências da pesquisa podem ser encontradas na Saída do módulo em [!UICONTROL Pacote] > [!UICONTROL Corpo] > [!UICONTROL presentationId].

Em nosso exemplo, os detalhes da apresentação solicitada foram retornados:

![Detalhes da apresentação](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

>[!ENDSHADEBOX]
