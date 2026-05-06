---
title: Módulos de áudio e vídeo do Adobe Firefly
description: Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam Adobe Firefly Audio and Video, bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: f54338aa35b8453ac991c9e16974f2b61fd30168
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 14%

---

# Módulos de áudio e vídeo do Adobe Firefly

Em um cenário do Adobe Workfront Fusion, é possível automatizar workflows que usam Adobe Firefly Audio and Video, bem como conectá-los a vários aplicativos e serviços de terceiros.

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso da funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote do Adobe Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Os pacotes Workfront Prime e Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Padrão</p><p>Trabalho ou maior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Pré-requisitos

Antes de usar o conector de áudio e vídeo do Adobe Firefly, verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta ativa de Áudio e Vídeo do Adobe Firefly.

## Criar uma conexão com Áudio e Vídeo do Adobe Firefly

Para criar uma conexão para os módulos de áudio e vídeo do Adobe Firefly:

1. Em qualquer módulo, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Nome da conexão</td>
        <td>
          <p>Insira um nome para essa conexão.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Ambiente</td>
        <td>Selecione se você está se conectando a um ambiente de produção ou não produção.</td>
        </tr>
        <tr>
        <td role="rowheader">Tipo</td>
        <td>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</td>
        </tr>
        <tr>
        <td role="rowheader">ID do cliente</td>
        <td>Insira a ID do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Segredo do cliente</td>
        <td>Insira o segredo do cliente do Adobe. Isso pode ser encontrado na seção Detalhes das credenciais do Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.


## Módulos de áudio e vídeo do Adobe Firefly e seus campos

Ao configurar os módulos de Áudio e Vídeo do Adobe Firefly, o Workfront Fusion exibe os campos listados abaixo. Além disso, campos adicionais de áudio e vídeo do Adobe Firefly podem ser exibidos, dependendo de fatores como nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Ações

* [Descrever modelo](#describe-template)
* [Áudio ou vídeo duplo](#dub-audio-or-video)
* [Gerar vídeo de avatar a partir de texto ou áudio](#generate-avatar-video-from-text-or-audio)
* [Gerar fala a partir do texto](#generate-speech-from-text)
* [Reestruturar vídeo](#reframe-video)
* [Renderizar modelo](#render-template)
* [Transcrever mídia](#transcribe-media)

#### Descrever modelo

Este módulo de ação analisa um arquivo MOGRT (template de vídeo) e retorna um manifesto de controles editáveis, fontes, imagens, áudio, vídeo e outros valores compatíveis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly, consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o Adobe Firefly</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Insira ou mapeie o URL pré-assinado que aponta para o arquivo de modelo de entrada.</td> 
  </tr>
 </tbody> 
</table>

#### Áudio ou vídeo duplo

Esse módulo de ação gera áudio ou vídeo dublado. Ele também pode incluir sincronização labial no vídeo gerado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly, consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o Adobe Firefly</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de dublagem</td> 
   <td>Selecione se deseja gerar um dub de áudio ou vídeo.</td> 
  </tr>
  <tr> 
   <td role="rowheader">URL pré-assinado</td> 
   <td>Insira ou mapeie o URL pré-assinado que o módulo usará para entrada.<p>Os seguintes domínios para armazenamento de mídia são aceitos pelo Firefly Audio and Video</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo de mídia</td> 
   <td>Selecione o tipo de mídia do arquivo de entrada</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sincronização labial</td> 
   <td>Selecione se deseja gerar uma sincronização labial composta de alta qualidade para a saída de vídeo.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Códigos de localidade de destino</td> 
   <td>Para cada código de localidade que você deseja adicionar, clique em <b>Adicionar item</b> e selecione o código de localidade.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Transcrições</td> 
   <td>Para cada transcrição que deseja adicionar, clique em <b>Adicionar item</b> e insira ou mapeie as URLs pré-assinadas para a transcrição.</td> 
  </tr>
 </tbody> 
</table>

#### Gerar vídeo de avatar a partir de texto ou áudio

Esse módulo de ação gera um vídeo de avatar a partir de uma transcrição ou arquivo de áudio fornecido por você.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly, consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o Adobe Firefly</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Insira ou mapeie o URL pré-assinado que o módulo usará para entrada.   </td> 
  </tr>
  <tr> 
  <tr> 
   <td role="rowheader">Código da localidade</td> 
   <td>Selecione o código de localidade que representa o idioma que você deseja usar no resultado.</td> 
  </tr>
   <td role="rowheader">Tipo de mídia (Source)</td> 
   <td>Selecione o tipo de mídia do arquivo de entrada</td> 
  </tr>
  <tr> 
   <td role="rowheader">Avatar</td> 
   <td>Selecione o avatar que deseja usar para o vídeo gerado.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo de mídia</td> 
   <td>Selecione o tipo de mídia de saída para o vídeo gerado.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Largura</td> 
   <td>Insira ou mapeie a largura do vídeo gerado.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Altura</td> 
   <td>Insira ou mapeie a altura do vídeo gerado.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Histórico</td> 
   <td>Selecione o tipo de plano de fundo que deseja usar para o vídeo gerado:
   <ul>
   <li><b>Vídeo</b>: insira ou mapeie a URL do vídeo em segundo plano.</li> 
   <li><b>Imagem</b>: insira ou mapeie a URL da imagem de plano de fundo.</li>
   <li><b>Cor</b>: insira ou mapeie o valor hexadecimal da cor que deseja usar para o plano de fundo do vídeo.</li> 
   </ul>
   </td>
  </tr>
 </tbody> 
</table>

#### Gerar fala a partir do texto

Esse módulo de ação gera fala de uma transcrição. Você pode fornecer uma transcrição em texto simples ou um URL pré-assinado. A resposta inclui uma ID de tarefa e um URL de status para rastrear a tarefa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly, consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o Adobe Firefly</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Script</td> 
   <td>Selecione o tipo de script que deseja fornecer.
   <ul>
   <li><b>Texto</b>: insira ou mapeie o texto de origem no campo Texto.</li>
   <li><b>Arquivo de texto</b>: insira ou mapeie a URL do arquivo de texto no campo URL.</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Código da localidade</td> 
   <td>Selecione o código de localidade que representa o idioma que você deseja usar no resultado.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo de mídia</td> 
   <td>Este deve ser <code>text/plain</code>.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Voz</td> 
   <td>Selecione a voz que deseja usar. As vozes disponíveis são do catálogo de vozes da Adobe Firefly.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Saída</td> 
   <td>Este deve ser <code>audio/wav</code>.</td> 
  </tr>
 </tbody> 
</table>

#### Reestruturar vídeo

Esse módulo reestrutura a mídia fornecida. A mídia é fornecida por meio de um URL pré-assinado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly, consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o Adobe Firefly</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL pré-assinado</td> 
   <td>Insira ou mapeie o URL pré-assinado que o módulo usará para entrada.<p>Os seguintes domínios para armazenamento de mídia são aceitos pelo Firefly Audio and Video</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Detecção de edição de cena</td> 
   <td>Selecione se deve ser aplicada a detecção de edição de cena antes da redefinição. </td> 
  </tr>
  <tr> 
   <td role="rowheader">Ponto focal</td> 
   <td>Para cada ponto focal que você deseja adicionar, clique em <b>Adicionar item</b> e insira ou o identificador de palavra-chave para o ponto focal.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sobreposições</td> 
   <td>Para cada sobreposição que você deseja adicionar, clique em <b>Adicionar item</b> e insira as informações de sobreposição.
   <ul>
   <li><b>Source</b>: insira ou mapeie a URL que aponta para a mídia de origem.</li> 
   <li><b>Hora de início</b>: insira ou mapeie a hora de início.</li>
   <li><b>Duração</b>: insira ou mapeie a duração da sobreposição.</li> 
   <li><b>Largura</b>: insira ou mapeie a largura da sobreposição dimensionada.</li> 
   <li><b>Altura</b>: insira ou mapeie a altura da sobreposição dimensionada.</li> 
   <li><b>Ponto de ancoragem</b>: selecione o ponto de ancoragem da sobreposição.</li> 
   <li><b>Deslocamento X</b>: insira ou mapeie o deslocamento horizontal da sobreposição.</li> 
   <li><b>Deslocamento Y</b>: insira ou mapeie o deslocamento vertical para a sobreposição.</li> 
   <li><b>Repetir</b>: insira <code>loop</code> para fazer com que um GIF execute um loop.</li> 
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Formato da mídia</td> 
   <td>Selecione o formato do vídeo reformulado.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Formato Sidecar</td> 
   <td>Selecione o formato para metadados adicionais.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Representações</td> 
   <td>Para adicionar mais representações, clique em <b>Adicionar item</b> e insira as informações de representação.<!--add additional info--></td> 
  </tr>
 </tbody> 
</table>

#### Renderizar modelo

Esse módulo renderiza uma ou mais variações de vídeo aplicando substituições e predefinições de exportação.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly, consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o Adobe Firefly</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL do arquivo de modelo de entrada</td> 
   <td>Insira ou mapeie o URL pré-assinado que representa o modelo que você deseja renderizar.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Fontes</td> 
   <td>Para cada fonte que você deseja adicionar, clique em <b>Adicionar item</b> e insira o nome do postscript da fonte e a URL do arquivo da fonte.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Quando uma fonte estiver ausente</td> 
   <td>Selecione se deseja falhar o renderizador ou usar a fonte padrão se uma fonte estiver ausente.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Ativos de mídia</td> 
   <td>Para cada ativo de mídia que você deseja adicionar, clique em <b>Adicionar item</b> e insira ou mapeie a URL pré-assinada que representa o ativo.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Exportar predefinições</td> 
   <td>Para cada predefinição de exportação que deseja adicionar, clique em <b>Adicionar item</b>, selecione a predefinição de vídeo e insira ou mapeie a URL pré-assinada que representa a predefinição.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Variações</td> 
   <td>Para cada variação que você deseja adicionar, clique em <b>Adicionar item</b> e insira os detalhes da variação. Você deve inserir detalhes para pelo menos uma variação.<!--add data here--></td> 
  </tr>
  <tr> 
   <td role="rowheader">Definições de saída</td> 
   <td>Defina saídas clicando em <b>Adicionar item</b>, selecionando quais das variações e predefinições adicionadas você deseja usar e adicionando um nome de arquivo. As variações e predefinições são indexadas a 0 (o primeiro item na lista de variações é 0, o próximo é 1 e assim por diante).</td> 
  </tr>
 </tbody> 
</table>

#### Transcrever mídia

Este módulo transcreve áudio ou vídeo.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Conexão</td> 
   <td>Para obter instruções sobre como criar uma conexão com o Adobe Firefly, consulte <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Criar uma conexão com o Adobe Firefly</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de transcrição</td> 
   <td>Selecione se deseja transcrever áudio ou vídeo.   </td> 
  </tr>
  <tr> 
   <td role="rowheader">URL pré-assinado</td> 
   <td>Insira ou mapeie o URL pré-assinado que o módulo usará para entrada.   </td> 
  </tr>
  <tr> 
  </tr>
   <td role="rowheader">Tipo de mídia </td> 
   <td>Selecione o tipo de mídia do arquivo de entrada</td> 
  </tr>
  <tr> 
   <td role="rowheader">Códigos de localidade de destino</td> 
   <td>Para cada código de localidade que você deseja adicionar, clique em <b>Adicionar item</b> e selecione o código de localidade que representa o idioma que você deseja usar no resultado.</td> 
  <tr> 
   <td role="rowheader">Formato da legenda</td> 
   <td>Insira <code>SRT</code> para incluir legendas ou deixe em branco se não quiser legendas.</td> 
  </tr>
 </tbody> 
</table>



