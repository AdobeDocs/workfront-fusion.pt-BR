---
title: Módulos do Adobe Photoshop
description: Com os módulos do Adobe Photoshop, você pode iniciar um cenário do Adobe Workfront Fusion com base em eventos em sua conta do Adobe Photoshop, criar, ler ou atualizar contratos e outros registros, pesquisar registros usando critérios definidos e fazer upload de documentos.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
TQID: https://experienceleague.adobe.com/RratZmko93V0LMxJ6qTy6cNvRqgPNvNgHTflRngE6BI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ce3fb5604ac4ed85af1bcc51143732499dfb0404
workflow-type: tm+mt
source-wordcount: 7285
ht-degree: 12%

---

# Módulos do [!DNL Adobe Photoshop]

Em um cenário do Adobe Workfront Fusion, é possível automatizar fluxos de trabalho que usam [!DNL Adobe Photoshop], bem como conectá-lo a vários aplicativos e serviços de terceiros.

Se você precisar de instruções sobre como criar um cenário, consulte os artigos em [Criar um cenário: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>O Adobe Photoshop descontinuou alguns elementos de sua API, que o Fusion usa para executar ações no Photoshop.
>
>**Portanto, alguns dos módulos existentes do Photoshop não funcionarão após 30 de julho de 2026.**
>
>Recomendamos atualizar todos os cenários que usam esses módulos para os módulos atualizados o mais rápido possível.
>
>Para obter uma lista de módulos afetados, consulte [atualizações de descontinuação da API do Adobe Photoshop](#adobe-photoshop-api-deprecation-updates).
>
>Para obter uma explicação de como as alterações na API afetam o Workfront Fusion, consulte [Visão geral das APIs no Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md).

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

Antes de usar o conector [!DNL Adobe Photoshop], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!DNL Adobe Photoshop] ativa.
* Você deve ter uma licença do Firefly Services.
* Você deve ter uma ID de cliente e um Segredo do cliente. Você pode adquiri-los na Adobe Developer Console.

## Atualizações de descontinuação da API do Adobe Photoshop

O Adobe Photoshop descontinuou alguns elementos de sua API, que o Fusion usa para executar ações no Photoshop.

**Portanto, alguns dos módulos existentes do Photoshop não funcionarão após 30 de julho de 2026.**

Esta tabela documenta quais módulos foram afetados por essa descontinuação e para qual módulo você deve atualizar.

| Módulo herdado obsoleto | Atualizar para o novo módulo |
|---|---|
| Aplicar edições no PSD | Criar ou editar um composto |
| Converter formato de imagem | Criar ou editar um composto |
| Criar um composto | Criar ou editar um composto |
| Criar uma nova PSD | Criar ou editar um composto |
| Criar representações | Criar ou editar um composto |
| Editar camadas de texto | Executar ações, scripts e transformações do Photoshop |
| Editar camadas de texto 2 | Executar ações, scripts e transformações do Photoshop |
| Executar uma ação JSON | Executar ações, scripts e transformações do Photoshop |
| Executar desfoque de profundidade | (Não Disponível) |
| Executar ações do Photoshop | Executar ações, scripts e transformações do Photoshop |
| Executar corte do produto | Executar ações, scripts e transformações do Photoshop |
| Obter informações da camada | Gerar um manifesto |
| Redimensionar uma imagem | Criar ou editar um composto |
| Substituir objeto inteligente | Criar ou editar um composto |
| Substituir objeto inteligente 2 | Criar ou editar um composto |
| Girar uma imagem | Executar ações, scripts e transformações do Photoshop |
| Marca d&#39;água em uma imagem | Criar ou editar um composto |

## Informações da API do Adobe Photoshop

O conector do Adobe Photoshop usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL básica</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## Criar uma conexão com [!DNL Adobe Photoshop]

Para criar uma conexão para os módulos do [!DNL Adobe Photoshop]:

1. Em qualquer módulo, clique em **[!UICONTROL Adicionar]** ao lado da caixa Conexão.

1. Preencha os seguintes campos:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Selecione se deseja usar uma conexão JWT ou uma conexão de servidor para servidor.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Insira um nome para essa conexão.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Insira sua [!UICONTROL Adobe] [!UICONTROL ID do cliente]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Insira o [!UICONTROL Client Secret] do [!DNL Adobe]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID da conta técnica]</td>
        <td>Se você estiver usando uma conexão JWT, digite sua [!DNL Adobe] [!UICONTROL ID da conta técnica]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID da Organização]</td>
        <td>Se estiver usando uma conexão JWT, insira sua [!DNL Adobe] [!UICONTROL ID da organização]. Isso pode ser encontrado na seção de detalhes [!UICONTROL Credentials] do [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Se você estiver usando uma conexão JWT, insira a chave privada que foi gerada quando suas credenciais foram criadas no [!DNL Adobe Developer Console]. </p>
          <p>Para extrair a chave privada ou o certificado:</p>
          <ol>
            <li value="1">
              <p>Clique em <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selecione o tipo de arquivo que você está extraindo.</p>
            </li>
            <li value="3">
              <p>Selecione o arquivo que contém a chave privada ou o certificado.</p>
            </li>
            <li value="4">
              <p>Insira a senha do arquivo.</p>
            </li>
            <li value="5">
              <p>Clique em <b>Salvar</b> para extrair o arquivo e retornar à configuração de conexão.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.

## Módulos do [!DNL Adobe Photoshop] e seus campos

Ao configurar módulos do [!DNL Adobe Photoshop], o Workfront Fusion exibe os campos listados abaixo. Junto com eles, outros campos do [!DNL Adobe Photoshop] podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Ações

* [Converter HEX em RGB](#convert-hex-to-rgb)
* [Criar uma prancheta](#create-an-artboard)
* [Criar ou editar um composto](#create-or-edit-a-composite)
* [Edição de uma imagem com vários ajustes](#edit-an-image-with-various-adjustments)
* [Executar ações, scripts e transformações do Photoshop](#execute-photoshop-actions-scripts-and-transformations)
* [Gerar um manifesto](#generate-a-manifest)
* [Remover plano de fundo](#remove-background)

#### Converter HEX em RGB

Este módulo converte um código de cor HEX em cor RGB.



Esse módulo faz ajustes de estilo do Lightroom em uma imagem.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL HEX]</td>
      <td>Insira ou mapeie o código HEX que deseja converter para o RGB.</td>
    </tr>
    </tbody>
</table>

#### Criar uma prancheta

Este módulo cria uma nova prancheta no Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Imagens]</td>
      <td>
        <p>Para cada imagem que você deseja adicionar a esta prancheta, clique em <b>Adicionar item</b> e insira o tipo de origem e o local da imagem.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaçamento entre pranchetas]</p>
      </td>
   <td>Insira ou mapeie o espaçamento, em pixels, que você deseja ter entre cada prancheta.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo convertido que deseja criar, clique em Add item e insira o armazenamento, o local e outras opções conforme listado.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Criar ou editar um composto

Este módulo cria ou edita uma composição no Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Imagens]</td>
      <td>
        <p>Para cada imagem que você deseja adicionar a esta prancheta, clique em <b>Adicionar item</b> e insira o tipo de origem e o local da imagem.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Largura]</p>
      </td>
   <td>Se estiver criando uma imagem, insira a largura da imagem em pixels.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Altura]</td>
      <td>
        <p>Se estiver criando uma imagem, insira a altura da imagem em pixels.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Modo]</td>
      <td>
        <p>Selecione o modo de cores para esta imagem.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Preenchimento]</td>
      <td>
        <p>Selecione o tipo de preenchimento para a camada de plano de fundo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>
        <p>Insira ou mapeie um nome para a nova imagem.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fator de escala de pixels]</td>
      <td>
        <p>Insira ou mapeie o fator de escala de pixels. Este valor deve ser um número entre 0,1 e 1.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Resolução]</td>
      <td>
        <p>No campo <b>Valor</b>, insira o valor da resolução em unidades de densidade (pixels por polegada). O valor padrão é 72.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo de Perfil]</td>
      <td>
        <p>Se desejar substituir o perfil de cores padrão, selecione um tipo de perfil e insira os detalhes conforme listados.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Recortar &gt; Superior/Esquerda/Inferior/Direita]</td>
      <td>
        <p>Insira os limites para os quais você deseja cortar a imagem.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ocultar]</td>
      <td>
        <p>Selecione sim para ocultar pixels fora dos limites de corte. SE definido como falso, os pixels fora dos limites de corte serão excluídos. O padrão é false.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Redimensionar &gt; Largura]</td>
      <td>
        <p>Selecione a unidade que deseja usar para a largura e selecione o valor que representa a largura desejada. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Redimensionar &gt; Altura]</td>
      <td>
        <p>Selecione a unidade que deseja usar para a altura e selecione o valor que representa a altura desejada. </p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Resolução]</td>
      <td>
        <p>Selecione a unidade que deseja usar para a resolução e, em seguida, selecione o valor que representa a resolução desejada.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Reamostragem]</td>
      <td>
        <p>Selecione o método de reamostragem a ser usado ao redimensionar.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Restringir proporções]</td>
      <td>
        <p>Selecione Sim para manter a proporção entre largura e altura. Selecione Não para permitir o ajuste independente da largura e da altura.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Rasterizar]</td>
      <td>
        <p>Selecione se deseja rasterizar a imagem.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Estilos de escala]</td>
      <td>
        <p>Selecione se deseja aplicar a escala a estilos ao redimensionar a imagem.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Cortar em]</td>
      <td>
        <p>Selecione se deseja cortar em pixels transparentes.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Camadas]</td>
      <td>
        <p>Para cada item que deseja adicionar posteriormente, clique em <b>Adicionar item</b> e insira os detalhes da camada. </p><p>Para obter detalhes, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">Criar ou editar um composto</a> na documentação do Adobe.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Fonte padrão PostScript name]</td>
      <td>
        <p>Insira ou mapeie o nome PostScript da fonte padrão que deseja usar.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Estratégia de fonte ausente]</td>
      <td>
        <p>Selecione se deseja que a criação ou edição falhe ou use a fonte padrão se uma fonte não estiver disponível.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Fontes adicionais]</td>
      <td>
        <p>Para cada fonte que você deseja adicionar, clique em <b>Adicionar item</b> e insira a URL de origem da fonte. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo editado que você deseja criar, clique em Adicionar item e insira os detalhes da saída. </p><p>Para obter detalhes, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">Criar ou editar um composto</a> na documentação do Adobe.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Número máximo de resultados]</td>
      <td>
        <p>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante um ciclo de execução.</p>
      </td>
      </tr>
      </tbody>
</table>

#### Edição de uma imagem com vários ajustes

Esse módulo faz ajustes de estilo do Lightroom em uma imagem.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Imagens]</td>
      <td>
        <p>Insira ou mapeie o tipo de origem e o local da imagem.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Outros campos]</p>
      </td>
   <td><p>Para obter detalhes, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/edit">Editar uma imagem com vários ajustes</a> na documentação do Adobe.</p></td> 
    </tr>
    </tbody>
</table>

#### Executar ações, scripts e transformações do Photoshop

Esse módulo executa ações, scripts e transformações disponíveis na API Photoshop do Firefly.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Imagens]</td>
      <td>
        <p>Insira ou mapeie o tipo de origem e o local da imagem.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ações]</p>
      </td>
   <td><p>Para cada ação que você deseja adicionar, clique em <b>Adicionar item</b> e insira a origem, a URL e o nome da ação.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL UXP origem]</p>
      </td>
   <td><p>Se estiver usando um script UXP, selecione se você está fornecendo um URL ou conteúdo em linha e, em seguida, insira ou mapeie o URL ou conteúdo.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Conteúdo adicional]</p>
      </td>
   <td><p>Adicione até 25 arquivos referenciados da ação ou UXP.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo editado que você deseja criar, clique em Adicionar item e insira o formato, o destino e o padrão de saída.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Número máximo de resultados]</td>
      <td>
        <p>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante um ciclo de execução.</p>
      </td>
      </tr>
    </tbody>
</table>

#### Gerar um manifesto

Esse módulo gera um manifesto PSD para a imagem de entrada fornecida.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source]</td>
      <td>
        <p>Insira ou mapeie o tipo de origem e o local da imagem.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo editado que deseja criar, clique em Adicionar item e insira os detalhes do destino.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Incluir miniaturas de camada]</p>
      </td>
   <td><p>Selecione Sim se desejar que o módulo gere uma representação de miniatura para cada camada no manifesto.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Profundidade máxima de miniatura]</p>
      </td>
   <td><p>Insira ou mapeie a profundidade máxima para representações em miniatura. Para nenhuma profundidade máxima, digite <code>0</code>.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Formato de miniatura da camada]</p>
      </td>
   <td><p>Selecione se deseja que as miniaturas estejam no formato JPEG ou PNG.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Extrair dados do Objeto Inteligente]</td>
      <td>
        <p>Selecione se deseja extrair objetos inteligentes incorporados e incluir um URL pré-assinado no manifesto.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cortar para transparência]</td>
      <td>
        <p>Selecione se deseja cortar cada miniatura de camada para remover os pixels transparentes.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Número máximo de resultados]</td>
      <td>
        <p>Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante um ciclo de execução.</p>
      </td>
      </tr>
    </tbody>
</table>

#### Remover plano de fundo

Este módulo de ação identifica o assunto principal da imagem e remove o plano de fundo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo do qual você deseja remover o plano de fundo está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo do qual deseja remover o plano de fundo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de cor]</p>
      </td>
   <td>Selecione se a imagem de saída usa cores RGB ou RGBA. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Formato de máscara]</p>
      </td>
   <td>Selecione se as bordas da imagem devem ser suaves (difusas) ou binárias. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Otimizar]</p>
      </td>
   <td>Selecione Desempenho para otimizar a velocidade ou Lote para permitir o tempo de espera. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Pós-processamento]</p>
      </td>
   <td>Selecione se deseja habilitar o pós-processamento.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>O padrão é 4,0</td> 
    </tr> 
    </tbody>
</table>


### Legado

* [Aplicar edições do PSD (herdado)](#apply-psd-edits-legacy)
* [Correção automática de cor de uma imagem (Herdado)](#auto-color-correct-an-image-legacy)
* [Converter formato de imagem (Herdado)](#convert-image-format-legacy)
* [Criar uma máscara (herdada)](#create-a-mask-legacy)
* [Criar um novo PSD (herdado)](#create-a-new-psd-legacy)
* [Criar representações (Herdado)](#create-renditions-legacy)
* [Editar camadas de texto (herdado)](#edit-text-layers-legacy)
* [Editar camadas de texto 2 (herdado)](#edit-text-layers-2-legacy)
* [Executar uma ação JSON (Herdado)](#execute-an-action-json-legacy)
* [Executar Desfoque de Profundidade (Herdado)](#execute-depth-blur-legacy)
* [Executar ações do Photoshop (Herdado)](#execute-photoshop-actions-legacy)
* [Executar corte do produto (herdado)](#execute-product-crop-legacy)
* [Obter informações da camada (herdada)](#get-layer-info-legacy)
* [Fazer uma chamada de API personalizada (herdado)](#make-a-custom-api-call-legacy)
* [Remover plano de fundo (Herdado)](#remove-background-legacy)
* [Substituir um objeto inteligente (herdado)](#replace-a-smart-object-legacy)
* [Substituir um objeto inteligente 2 (herdado)](#replace-a-smart-object-2-legacy)
* [Redimensionar uma imagem (herdada)](#resize-an-image-legacy)
* [Marca d&#39;água de uma imagem (herdada)](#watermark-an-image-legacy)

#### Aplicar edições do PSD (herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o [Crie ou edite um módulo &#x200B;](#create-or-edit-a-composite) composto.

Esse módulo de ação aplica uma variedade de edições de documento e nível de camada.

Este módulo suporta arquivos grandes. Para obter mais informações sobre arquivos grandes, consulte [Trabalhando com arquivos grandes](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da imagem) Altura]</p>
      </td>
      <td> Insira ou mapeie a altura da imagem em pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da imagem) Largura]</p>
      </td>
      <td> Insira ou mapeie a largura da imagem em pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da tela de desenho) Superior]</p>
      </td>
   <td> Insira ou mapeie, em pixels, a coordenada y do canto superior esquerdo do documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da tela de desenho) Inferior]</p>
      </td>
   <td> Insira ou mapeie, em pixels, a coordenada y do canto inferior direito do documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da tela de desenho) à esquerda]</p>
      </td>
   <td> Insira ou mapeie, em pixels, a coordenada x do canto superior esquerdo do documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da tela de desenho) Direita]</p>
      </td>
   <td> Insira ou mapeie, em pixels, a coordenada x do canto inferior direito do documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento) Cortar]</p>
      </td>
   <td> Selecione Pixels transparentes para basear o corte em pixels transparentes na imagem. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Fonte padrão]</p>
      </td>
   <td> Digite o nome completo do postscript da fonte a ser usada como padrão global para o documento. Essa fonte será usada para qualquer camada de texto que tenha uma fonte ausente e nenhuma outra fonte tenha sido especificamente fornecida para essa camada. Se esta fonte estiver ausente, a opção especificada em Gerenciar fontes ausentes entrará em vigor. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Fontes]</p>
      </td>
   <td> Para cada fonte que o documento precisa, clique em Adicionar item e insira o local de armazenamento e o local do arquivo da fonte. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Gerenciar fontes ausentes]</p>
      </td>
   <td> Selecione a ação a ser tomada se houver uma ou mais fontes ausentes no documento. <ul><li><code>fail</code>: A tarefa não será bem-sucedida e o status será definido como Falha, com os detalhes do erro fornecidos na seção de detalhes no status.</li><li><code>useDefault</code>: A tarefa será bem-sucedida e todas as fontes ausentes serão substituídas por ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Camadas]</p>
      </td>
   <td> Para cada camada que deseja adicionar, clique em Adicionar item e preencha os detalhes da camada. <p>Para obter detalhes sobre opções de camada, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/modifyDocumentAsync">Aplicar edições de PSD</a> na documentação do Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo editado que você deseja criar, clique em Add item (Adicionar item) e insira o armazenamento, o local e o tipo conforme listado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Cortar para Tela]</p>
      </td>
   <td>Selecione se as representações devem ser do tamanho da Tela de Pintura. Verdadeiro corta as representações para o tamanho da Tela de Pintura, enquanto Falso faz com que a camada de representações tenha o Tamanho</td> 
    </tr>
    </tbody>
</table>

#### Correção automática de cor de uma imagem (Herdado)

Essa cor automática do módulo de ação corrige a imagem especificada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o arquivo que você deseja corrigir as cores está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo cuja cor você deseja corrigir. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Converter formato de imagem (Herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o [Crie ou edite um módulo &#x200B;](#create-or-edit-a-composite) composto.

Esse módulo de ação converte um arquivo em JPEG, PNG, PSD ou TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo do qual você deseja remover o plano de fundo está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo do qual deseja remover o plano de fundo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo convertido que deseja criar, clique em Adicionar item e insira o armazenamento, o local e o tipo conforme listado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Criar uma máscara (herdada)

Este módulo de ação retorna um arquivo PNG com uma máscara aplicada ao redor do assunto.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo do qual você deseja criar uma máscara está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo a partir do qual deseja criar uma máscara. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo de máscara seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo de máscara será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espaço de cor]</p>
      </td>
   <td>Selecione se a imagem de saída usa cores RGB ou RGBA. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Formato de máscara]</p>
      </td>
   <td>Selecione se a máscara deve ser suave (difusa) ou binária. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Otimizar]</p>
      </td>
   <td>Selecione Desempenho para otimizar a velocidade ou Lote para permitir o tempo de espera. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Pós-processamento]</p>
      </td>
   <td>Selecione se deseja habilitar o pós-processamento.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>O padrão é 4,0</td> 
    </tr> 
    </tbody>
</table>

#### Criar um novo PSD (herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o [Crie ou edite um módulo &#x200B;](#create-or-edit-a-composite) composto.

Esse módulo de ação cria uma nova PSD com camadas opcionais e gera representações ou salva como um PSD.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da imagem) Altura]</p>
      </td>
      <td> Insira ou mapeie a altura da imagem em pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento &gt; Tamanho da imagem) Largura]</p>
      </td>
      <td> Insira ou mapeie a largura da imagem em pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento) Resolução]</p>
      </td>
   <td> Insira ou mapeie, em pixels por polegada, a resolução da imagem. Deve estar entre 72 e 300. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Modo Documento)]</p>
      </td>
   <td> Selecione o modo da imagem. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento) Preencher]</p>
      </td>
   <td> Selecione se deseja que o preenchimento da camada de plano de fundo seja transparente, branco ou a cor do plano de fundo da imagem. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções &gt; Documento) profundidade]</p>
      </td>
   <td> Selecione a profundidade de bits da imagem. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Camadas]</p>
      </td>
   <td> Para cada camada que deseja adicionar, clique em Adicionar item e preencha os detalhes da camada. <p>Para obter detalhes sobre opções de camada, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">Criar PSD</a> na documentação do Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Fonte global]</p>
      </td>
   <td> Digite o nome completo do postscript da fonte a ser usada como padrão global para o documento. Essa fonte será usada para qualquer camada de texto que tenha uma fonte ausente e nenhuma outra fonte tenha sido especificamente fornecida para essa camada. Se esta fonte estiver ausente, a opção especificada em Gerenciar fontes ausentes entrará em vigor. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Fontes]</p>
      </td>
   <td> Para cada fonte que o documento precisa, clique em Adicionar item e insira o local de armazenamento e o local do arquivo da fonte. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Gerenciar fontes ausentes]</p>
      </td>
   <td> Selecione a ação a ser tomada se houver uma ou mais fontes ausentes no documento. <ul><li><code>fail</code>: A tarefa não será bem-sucedida e o status será definido como Falha, com os detalhes do erro fornecidos na seção de detalhes no status.</li><li><code>useDefault</code>: A tarefa será bem-sucedida e todas as fontes ausentes serão substituídas por ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo que deseja criar, clique em Adicionar item e insira o armazenamento, o local e o tipo conforme listado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Outros campos]</td>
      <td>
        <p><p>Para obter detalhes sobre opções de saída, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">Criar PSD</a> na documentação do Adobe Photoshop.  </p>
      </td>
    </tr>
    </tbody>
</table>

#### Criar representações (Herdado)

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo que deseja criar, clique em Adicionar item e insira a opção de armazenamento, local, tipo e substituição conforme listado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) Tipo]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
      </tbody>
</table>

#### Editar camadas de texto (herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o módulo [Executar ações, scripts e transformações do Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Esse módulo de ação edita camadas de texto em um arquivo do Photoshop. É possível inserir detalhes de edição separados para várias camadas no mesmo arquivo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gerenciar fontes ausentes]</td>
      <td>
        <p>Selecione a ação a ser tomada se houver uma ou mais fontes ausentes no documento. Se a fonte não for fornecida, o módulo usará a fonte padrão.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fonte padrão]  </td>
      <td>
        <p>Digite o nome completo do postscript da fonte a ser usada como padrão global para o documento. Essa fonte será usada para qualquer camada de texto que tenha uma fonte ausente e nenhuma outra fonte tenha sido especificamente fornecida para essa camada. Se esta fonte estiver ausente, a opção especificada em Gerenciar fontes ausentes entrará em vigor.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Fontes]</p>
      </td>
   <td> Insira o local de armazenamento e o local do arquivo da fonte. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Camadas]</td>
   <td> <p>Para cada camada de texto que você deseja editar, clique em <b>Adicionar item</b> e insira as opções de camada.<p>Para obter detalhes sobre opções de camada, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">Editar texto</a> na documentação do Adobe Photoshop.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Editar camadas de texto 2 (herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o módulo [Executar ações, scripts e transformações do Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Esse módulo de ação edita uma camada de texto em um arquivo do Photoshop.

Para editar várias camadas, use o módulo [Editar camadas de texto](#edit-text-layers).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gerenciar fontes ausentes]</td>
      <td>
        <p>Selecione a ação a ser tomada se houver uma ou mais fontes ausentes no documento. Se a fonte não for fornecida, o módulo usará a fonte padrão.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fonte padrão]  </td>
      <td>
        <p>Digite o nome completo do postscript da fonte a ser usada como padrão global para o documento. Essa fonte será usada para qualquer camada de texto que tenha uma fonte ausente e nenhuma outra fonte tenha sido especificamente fornecida para essa camada. Se esta fonte estiver ausente, a opção especificada em Gerenciar fontes ausentes entrará em vigor.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opções) Fontes]</p>
      </td>
   <td> Insira o local de armazenamento e o local do arquivo da fonte. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Camadas]</td>
   <td> <p>Para obter detalhes sobre opções de camada, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">Editar camada de texto</a> na documentação do Adobe Photoshop.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de saída]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
  </tbody>
</table>


#### Executar uma ação JSON (Herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o módulo [Executar ações, scripts e transformações do Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Esse módulo de ação executa ações do Photoshop usando comandos JSON.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ação JSON]</td>
      <td>
        <p>Insira o comando JSON para a ação que deseja realizar.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fontes / Padrões / Pincéis / Imagens adicionais]</td>
      <td>
        <p>Para cada fonte, padrão, pincel ou imagem adicional que você deseja usar nesta ação, clique em Adicionar item e insira o armazenamento e o local do arquivo do item.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Fonte / Padrão / URL do arquivo de Pincel]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja usar. </td> 
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo que deseja criar, clique em Adicionar item e insira a opção de armazenamento, local, tipo e substituição conforme listado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) URL do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) Tipo]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
      </tbody>
</table>

#### Executar Desfoque de Profundidade (Herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.

Esse módulo de ação executa o Desfoque de Profundidade no arquivo selecionado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) URL do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) Tipo]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Outros campos]</td>
      <td>
        <p>Para obter detalhes sobre outras opções de Desfoque de Profundidade, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Executar Desfoque de Profundidade </a>na documentação da API do Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Executar ações do Photoshop (herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o módulo [Executar ações, scripts e transformações do Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Esse módulo de ação executa uma ação Photoshop na imagem selecionada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que você deseja editar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja editar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ações armazenamento de arquivo]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o arquivo de ações está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de ações]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo de ações. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nome da ação]</p>
      </td>
   <td> Se desejar executar apenas uma ação específica, você pode especificar qual ação executar a partir do ActionSet. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de fonte / padrão / pincel]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo que deseja usar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Fonte / Padrão / URL do arquivo de Pincel]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que deseja usar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) URL do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) Tipo]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Outros campos]</td>
      <td>
        <p>Para obter detalhes sobre outras opções de Desfoque de Profundidade, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Executar Desfoque de Profundidade </a>na documentação da API do Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Executar corte do produto (herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o módulo [Executar ações, scripts e transformações do Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Esse módulo de ação executa o Recorte de produto na imagem selecionada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o arquivo que você deseja cortar está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que você deseja cortar. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Unidade]</p>
      </td>
   <td> Selecione se deseja descrever o ajuste de altura e largura em pixels ou como uma porcentagem. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Largura]</p>
      </td>
   <td> Insira ou mapeie a quantidade de preenchimento de largura que deseja adicionar. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Altura]</p>
      </td>
   <td> Insira ou mapeie a quantidade de preenchimento de altura que deseja adicionar. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo editado seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) URL do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo editado será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) Tipo]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saídas) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Outros campos]</td>
      <td>
        <p>Para obter detalhes sobre outras opções de Desfoque de Profundidade, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Executar Desfoque de Profundidade </a>na documentação da API do Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Obter informações da camada (herdada)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o módulo [Gerar um manifesto](#generate-a-manifest).

Esse módulo de ação recupera informações de camada do arquivo PSD especificado.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento de arquivo de entrada]</td>
      <td>
        <p>Selecione o serviço de arquivo no qual o arquivo do qual você deseja recuperar as informações de camada é armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL do arquivo de entrada]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo do qual deseja recuperar as informações da camada. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Miniaturas]</p>
      </td>
   <td> Selecione o tipo de arquivo que deseja que as miniaturas sejam. Miniaturas são pequenas visualizações para qualquer camada renderizável.</td> 
    </tr>
  </tbody>
</table>

#### Fazer uma chamada de API personalizada

Esse módulo de ação faz uma chamada personalizada para a API do Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Insira um caminho relativo a <code>https://image.adobe.io/pie/psdService</code>. Exemplo: <code>/photoshopActions</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Métodos de solicitação HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p>
        <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p>
        <p>O Workfront Fusion adiciona cabeçalhos de autorização automaticamente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Insira a string de consulta da solicitação.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Adicione o conteúdo do corpo para a chamada de API na forma de um objeto JSON padrão.</p> <p>Observação:  <p>Ao usar instruções condicionais, como <code>if</code> em seu JSON, coloque as aspas fora da instrução condicional.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### Substituir um objeto inteligente (herdado)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o [Crie ou edite um módulo &#x200B;](#create-or-edit-a-composite) composto.

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o [Crie ou edite um módulo &#x200B;](#create-or-edit-a-composite) composto.

Esse módulo de ação substitui um Objeto inteligente em uma camada do PSD e gera novas representações.

Este módulo usa a API de objeto inteligente versão 2.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o Objeto Inteligente está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do Objeto inteligente. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Camadas]</p>
      </td>
   <td>Para cada camada que você deseja adicionar ao Objeto inteligente, clique em Adicionar item e Insira o nome ou ID do objeto, o serviço de arquivos onde o Objeto inteligente está armazenado e o URL ou caminho da camada.<p>Para obter descrições das configurações avançadas nesta área, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">Substituir um objeto inteligente</a> na documentação da API do Photoshop </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Redimensionar imagem durante o local]</p>
      </td>
   <td> Selecione se deseja redimensionar a imagem.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada nova representação que você deseja que o módulo produza, clique em Adicionar item e preencha os campos a seguir. Você pode ter no máximo 25 arquivos de saída.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saídas) Tipo]</p>
      </td>
   <td> Selecione o tipo de arquivo para o arquivo editado. </td> 
    </tr>
     </tbody>
</table>

#### Substituir um objeto inteligente 2 (herdado)

Esse módulo de ação substitui um Objeto inteligente em uma camada do PSD e gera novas representações.

Este módulo usa a versão herdada dos Objetos Inteligentes.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos onde o Objeto Inteligente está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Entrada) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do Objeto inteligente. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Camadas]</p>
      </td>
   <td>Para cada camada que você deseja adicionar ao Objeto inteligente, clique em Adicionar item e Insira o nome ou ID do objeto, o serviço de arquivos onde o Objeto inteligente está armazenado e o URL ou caminho da camada.<p>Para obter descrições das configurações avançadas nesta área, consulte <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">Substituir um objeto inteligente</a> na documentação da API do Photoshop </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada nova representação que você deseja que o módulo produza, clique em Adicionar item e preencha os campos a seguir. Você pode ter no máximo 25 arquivos de saída.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Largura de Saída)]</p>
      </td>
   <td> A largura, em pixels, do arquivo de saída. O módulo preservará a proporção original. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tbody>
</table>

#### Redimensionar uma imagem (herdada)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o [Crie ou edite um módulo &#x200B;](#create-or-edit-a-composite) composto.

Essa ação redimensiona uma imagem usando a mesma proporção.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivo onde o arquivo que você deseja redimensionar está armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Local do arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo que você deseja redimensionar.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Para cada arquivo convertido que deseja criar, clique em Add item e insira o armazenamento, o local e outras opções conforme listado.</p>
      </td>
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o novo arquivo seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Local do arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho onde o novo arquivo será armazenado.  Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Largura]</p>
      </td>
   <td> A largura, em pixels, do arquivo de saída. O módulo preservará a proporção original. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Largura máxima]</p>
      </td>
   <td>Quando a largura for 0, Max com poderá ser fornecido para obter o tamanho. A largura máxima tem precedência sobre uma largura menor que a largura do documento.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Aparar na tela]</p>
      </td>
   <td>Selecione Sim para recortar as representações para o tamanho da Tela de Pintura ou Não para criar o Tamanho da Camada de representações.</td> 
    </tr>
    </tbody>
</table>

#### Marca d&#39;água de uma imagem (herdada)

>[!NOTE]
>
>Este módulo foi substituído e não funcionará mais após 30 de julho de 2026.
>Atualize este módulo para o [Crie ou edite um módulo &#x200B;](#create-or-edit-a-composite) composto.

Esse módulo de ação adiciona uma marca d&#39;água à imagem selecionada.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Para obter instruções sobre como criar uma conexão com o [!DNL Adobe Photoshop], consulte <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Criar uma conexão com o [!DNL Adobe Photoshop]</a> neste artigo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Base &gt; Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual o arquivo ao qual você deseja adicionar uma marca d'água está armazenado.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Base &gt; Entrada) Local do arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho do arquivo ao qual você deseja adicionar uma marca d'água. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Marca D'Água &gt; Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual a marca d'água que você deseja adicionar está armazenada.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Marca D'Água &gt; Entrada) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual a marca d'água que você deseja adicionar está armazenada.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Marca D'Água &gt; Limites) Altura]</p>
      </td>
   <td>Insira ou mapeie a altura desejada da marca d'água em pixels.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Marca D'Água &gt; Limites) Largura]</p>
      </td>
   <td> Insira ou mapeie a largura desejada da marca d'água em pixels. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Marca D'Água &gt; Limites) À Esquerda]</p>
      </td>
   <td> Insira ou mapeie a distância em pixels do lado esquerdo da imagem que a marca d'água deve estar.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Marca D'Água &gt; Limites) Superior]</p>
      </td>
   <td> Insira ou mapeie a distância em pixels a partir da parte superior da imagem que a marca d'água deve estar.</td> 
    </tr>  
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Armazenamento]</td>
      <td>
        <p>Selecione o serviço de arquivos no qual você deseja que o arquivo de marca d'água seja armazenado.</p><p>A seleção do armazenamento interno do Fusion disponibiliza o arquivo para módulos posteriores, mas não o disponibiliza fora do cenário.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Saída) Local do Arquivo]</p>
      </td>
   <td> Insira ou mapeie o URL ou o caminho de onde o arquivo de marca d'água será armazenado. Isso só será necessário se você não tiver escolhido o armazenamento interno do Fusion para o armazenamento de saída.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Tipo de Saída)]</p>
      </td>
   <td>Selecione o tipo de arquivo para o qual deseja converter o arquivo. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Largura de Saída)]</p>
      </td>
   <td> A largura, em pixels, do arquivo de saída. O módulo preservará a proporção original. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Saída) Substituir]</td>
      <td>
        <p>Selecione se o arquivo recém-editado substituirá qualquer arquivo de saída existente. Isso se aplica somente a arquivos no armazenamento do Adobe.</p>
      </td>
    </tbody>
</table>
