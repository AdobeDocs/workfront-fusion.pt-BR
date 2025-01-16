---
title: Módulos do OpenAI (ChatGPT)
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam OpenAIT(ChatGPT), bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion
exl-id: c8138d82-fa5a-4e69-b3cb-aa232099cb33
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1240'
ht-degree: 0%

---

# [!DNL OpenAI (ChatGPT & DALL-E)] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL OpenAI (ChatGPT & DALL-E)], bem como conectá-los a vários aplicativos e serviços de terceiros.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td> <p>[!UICONTROL [!DNL Workfront Fusion] para Automação e integração do trabalho] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>Sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</td> 
  </tr> 
 </tbody> 
</table>

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Pré-requisitos

Para usar módulos do [!DNL OpenAI (ChatGPT & DALL-E)], você deve ter uma conta do [!DNL OpenAI], incluindo uma chave de API e ID da organização.

## Informações da API do OpenAI (ChatGPT e DALL-E)

O conector OpenAI (ChatGPT &amp; DALL-E) usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.11.1</td> 
  </tr>
 </tbody> 
 </table>

## Conectando [!DNL OpenAI (ChatGPT & DALL-E)] a [!DNL Workfront Fusion]

Você pode criar uma conexão com sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] diretamente de dentro de um módulo [!DNL OpenAI (ChatGPT & DALL-E)].

1. Em qualquer módulo [!DNL OpenAI (ChatGPT & DALL-E)], clique em **[!UICONTROL Add]** ao lado do campo [!UICONTROL Connection].
1. Insira as seguintes informações:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Insira um nome para a nova conexão.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td>Você pode localizar sua chave de API nas configurações de usuário do OpenAI.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Organization ID] </td> 
      <td>É possível localizar a ID da organização na página Configurações da organização no OpenAI.</td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continue]** para criar a conexão e voltar para o módulo.


## [!DNL OpenAI (ChatGPT & DALL-E)] módulos e seus campos

Ao configurar módulos do [!DNL OpenAI (ChatGPT & DALL-E)], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL OpenAI (ChatGPT & DALL-E)] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Criar uma conclusão

>[!IMPORTANT]
>
>Este módulo foi substituído.

<!--

This action module creates a completion for the provided prompt or chat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Enter or map the ID of the model to use. You can use the Get models module to see all of your available models. </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Temperature]</td> 
   <td> This value must be between 0 and 2, and determines the randomness of the output. Higher values produce output that is more random, while lower values produce more focused output. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating completions in the <a href="https://platform.openai.com/docs/api-reference/completions/create" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Criar uma moderação

Este módulo de ação determina se o texto viola a Política de conteúdo do OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> Para cada amostra de texto que você deseja incluir, clique em <b>Adicionar item</b> e insira ou mapeie o texto. Inclua toda a amostra de texto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Insira ou mapeie a ID do modelo a ser usado. Você pode usar o módulo Obter modelos para ver todos os modelos disponíveis. </td> 
  </tr> 
 </tbody> 
</table>

### Criar uma edição

Este módulo de ação retorna uma versão editada de um prompt fornecido, seguindo suas instruções.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Insira ou mapeie a ID do modelo a ser usado. Você pode usar o módulo Obter modelos para ver todos os modelos disponíveis. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> Insira ou mapeie o texto que deseja editar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Instruction]</td> 
   <td> Insira ou mapeie as instruções para a edição. Exemplo: "Corrigir os erros de ortografia". </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Para obter informações sobre as configurações avançadas opcionais deste módulo, consulte as informações sobre a criação de edições na <a href="https://platform.openai.com/docs/api-reference/edits/create" class="MCXref xref">Documentação da API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Criar uma incorporação

Esse módulo de ação cria um vetor de incorporação que representa o texto de entrada.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Insira ou mapeie a ID do modelo a ser usado. Você pode usar o módulo Obter modelos para ver todos os modelos disponíveis. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input text to embed]</td> 
   <td> Insira ou mapeie o texto que deseja incorporar. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User ID]</td> 
   <td> Insira ou mapeie um identificador exclusivo que represente seu usuário final, o que pode ajudar o OpenAI a monitorar e detectar abusos </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Insira ou mapeie o número máximo de edições com as quais você deseja que o módulo funcione durante cada ciclo de execução do cenário.</td> 
  </tr> 
 </tbody> 
</table>

### Criar Conclusão de Chat

Dada uma lista de mensagens que descrevem uma conversa, esse módulo de ação retorna uma resposta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Insira ou mapeie a ID do modelo a ser usado. Você pode usar o módulo Obter modelos para ver todos os modelos disponíveis. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>As mensagens descrevem a conversa até agora. Para cada mensagem que você deseja adicionar, clique em <b>Adicionar item</b> e preencha o seguinte:
   <ul>
   <li> <b>Função</b>: selecione a função do autor desta mensagem.</li>
   <li> <b>Conteúdo</b>: inserir ou mapear o conteúdo desta mensagem.</li>
   <li> <b>Nome</b>: insira ou mapeie o nome do autor desta mensagem. O nome pode conter letras maiúsculas e minúsculas, números e sublinhados. O comprimento máximo do nome é de 64 caracteres.</li>
   </ul>
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Para obter informações sobre as configurações avançadas opcionais deste módulo, consulte as informações sobre como criar conclusões de chat na <a href="https://platform.openai.com/docs/api-reference/chat/create" class="MCXref xref">documentação da API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Edit image

This action module makes edits or creates variations of existing images.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to create edits or variations of the image.
   <p>NOTE: Images must be a valid PNG file, less than 4MB, and square. If mask is not provided, the image must have transparency, which will be used as the mask.</p> 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Text description of desired image]</td> 
   <td> <p>If editing an image, enter or map a description of the edits you want to create. Maximum length is 1000 characters.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating image edits or variations in the <a href="https://platform.openai.com/docs/api-reference/images/createEdit" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Gerar imagens

Esse módulo de ação gera ou manipula imagens com modelos Dall-E.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text description of the desire image]</td> 
   <td> Insira ou mapeie uma descrição da imagem desejada. O comprimento máximo da descrição é de 1000 caracteres. 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Para obter informações sobre as configurações avançadas opcionais deste módulo, consulte as informações sobre a criação de imagens na <a href="https://platform.openai.com/docs/api-reference/images/create" class="MCXref xref">Documentação da API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Obter Modelos

Este módulo lista e descreve os vários modelos disponíveis na API OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> Selecione se deseja obter uma lista de todos os modelos ou recuperar um modelo específico.
    <ul>
    <li><p><b>Listar modelos </b></p><p>Esta ação lista os modelos disponíveis no momento e fornece informações básicas sobre cada um, como o proprietário e a disponibilidade.</p></li>
    <li><p><b>Recuperar modelo </b></p><p>Insira ou mapeie a ID do modelo que deseja recuperar. </p></li>
   </ul>
 </td> 
  </tr>
 </tbody> 
</table>

### Fazer uma chamada de API personalizada

Esse módulo de ação cria uma solicitação HTTP personalizada para a API OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Digite um caminho relativo para <code>https://api.openai.com/v1/</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>O Workfront Fusion adiciona os cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Adicione a consulta da chamada à API na forma de um objeto JSON padrão.</p> <p>Por exemplo: <code>{"name":"something-urgent"}</code></p> </td> 
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

<!--

### Manage Audio

This action modules converts audio to text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to transcribe the audio into the input language, or into English.
   <p>If transcribing into the input language, you can select the language in this module's advanced settings. </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Enter or map the maximum number of edits you want the module to work with during each scenario execution cycle.</td> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating transcriptions in the <a href="https://platform.openai.com/docs/api-reference/audio/createTranscription" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

-->

### Gerenciar arquivos

Este módulo de ação lista, exclui ou recupera arquivos ou conteúdo de arquivo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> Selecione a ação que deseja executar. 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> Se você estiver excluindo um arquivo ou recuperando um arquivo ou conteúdo de arquivo, insira ou mapeie a ID do arquivo. 
  </tr> 
</tbody>
</table>

### Gerenciar Ajustes

Gerencie tarefas de ajuste para adaptar um modelo aos seus dados de treinamento específicos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL OpenAI (ChatGPT & DALL-E)] ao Workfront Fusion, consulte <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Conectando o [!DNL OpenAI (ChatGPT & DALL-E)] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Selecione a ação que deseja executar.
   <ul>
   <li><p>Ajustar um modelo de um conjunto de dados</p><p>Insira ou mapeie uma descrição para a imagem desejada.</p>
     <li><p>Obter informações sobre um trabalho de ajuste</p><p>Insira ou mapeie a ID do trabalho.</p>
   <li><p>Cancelar um trabalho de ajuste</p><p>Insira ou mapeie a ID do trabalho.</p>
   <li><p>Cancelar um trabalho de ajuste</p><p>Insira ou mapeie a ID do trabalho.</p>
   <li><p>Obter atualizações de status para um trabalho de ajuste</p><p>Insira ou mapeie a ID do trabalho e selecione se deseja transmitir essas atualizações.</p>
   <li><p>Excluir um modelo ajustado</p><p>Insira ou mapeie a ID do modelo que deseja excluir.</p>
 </ul> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> Se você estiver excluindo um arquivo ou recuperando um arquivo ou conteúdo de arquivo, insira ou mapeie a ID do arquivo. 
  </tr> 
</tbody>
