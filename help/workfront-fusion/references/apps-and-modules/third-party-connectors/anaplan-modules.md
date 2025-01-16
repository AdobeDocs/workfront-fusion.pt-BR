---
description: Em um cenário  [!DNL Adobe Workfront Fusion] , você pode automatizar fluxos de trabalho que usam Anaplan, bem como conectá-los a vários aplicativos e serviços de terceiros.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: 99f2e558db3d2b126adf748d7e013a4a39735bcd
workflow-type: tm+mt
source-wordcount: '1617'
ht-degree: 0%

---

# [!DNL Anaplan] Módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode automatizar fluxos de trabalho que usam [!DNL Anaplan], bem como conectá-los a vários aplicativos e serviços de terceiros.

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
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano [!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Adobe Workfront], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Pré-requisitos

Antes de usar o conector [!DNL Anaplan], verifique se os seguintes pré-requisitos foram atendidos:

* Você deve ter uma conta [!UICONTROL Anaplan] ativa.
* Você deve configurar Espaços de Trabalho, Modelos e outros objetos do [!DNL Anaplan] em sua conta do [!UICONTROL Anaplan] antes que o [!DNL Workfront Fusion] possa interagir com eles.

## Informações da API Anaplan

O conector Anaplan usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL base</td> 
   <td>https://api.anaplan.com/2/0/
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versão da API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.11.5/td&gt; 
 </tbody> 
</table>

## Conectar [!DNL Anaplan] a [!DNL Workfront Fusion] {#connect-anaplan-to-workfront-fusion}

Para criar uma conexão para seus módulos do [!DNL Anaplan]:

1. Clique em **[!UICONTROL Add]** ao lado da caixa [!UICONTROL Connection].
1. Selecione o tipo de conexão.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>Uma conexão [!DNL Anaplan] [!UICONTROL Basic] requer somente um endereço de email e senha para criar a conexão. </p> <p>Digite um nome para a conexão e seu endereço de email e a senha da conta [!DNL Anaplan].</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>Uma conexão [!DNL Anaplan] [!UICONTROL CA Certificate] requer [!UICONTROL Certificate Key], [!UICONTROL Encoded Data] e [!UICONTROL Encoded Signed Data]. Você pode gerá-los na sua conta [!DNL Anaplan]. Para obter instruções, consulte a documentação do [!DNL Anaplan].</p> <p>Insira um nome para a conexão e, em seguida, insira os [!UICONTROL Certificate Key], [!UICONTROL Encoded Data] e [!UICONTROL Encoded Signed Data] que você gerou em sua conta do [!DNL Anaplan].</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Continue]** para salvar a conexão e retornar ao módulo.

## [!DNL Anaplan] módulos e seus campos

Ao configurar módulos do [!DNL Anaplan], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Anaplan] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Ações](#actions)
* [Pesquisas](#searches)

### Triggers

#### [!DNL Watch records]

Esse módulo de acionamento inicia um cenário quando um registro do tipo escolhido é criado ou atualizado.

>[!NOTE]
>
>Este módulo retorna os dados de novos registros. Ele não retorna os dados dos registros existentes modificados.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Anaplan] a [!DNL Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo de objeto a ser observado</td> 
   <td>Selecione o tipo de item que deseja observar. O cenário começa quando esse tipo de registro é criado ou atualizado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID do &lt;Object&gt;</td> 
   <td>Informe a ID do objeto em Anaplan, como um Modelo ou Módulo, que está associado aos objetos que você deseja observar</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limite</td> 
   <td> <p>Insira ou mapeie o número máximo de registros para o qual deseja que o módulo [action] durante cada ciclo de execução do cenário.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ações

* [[!UICONTROL Create a list item]](#create-a-list-item)
* [[!UICONTROL Make a custom API Call]](#make-a-custom-api-call)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Run an action]](#run-an-action)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a file]](#upload-a-file)

#### [!UICONTROL Create a list item]

Este módulo de ação adiciona um novo item a uma lista no Anaplan.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Connection]</td>
        <td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Anaplan] a [!DNL Workfront Fusion]</a> neste artigo.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Workspace ID]</td>
        <td>Selecione ou mapeie a ID da Workspace Anaplan que contém a lista à qual você deseja adicionar um item.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Model ID]</td>
        <td>Selecione ou mapeie a ID do Modelo que contém a lista à qual você deseja adicionar um item.</td>
    </tr>
    <tr>
        <td>[!UICONTROL List ID]</td>
        <td>Selecione ou mapeie a ID da Lista onde deseja criar um item.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Name]</td>
        <td>Insira um nome para o novo item.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Code]</td>
        <td>Insira o código do novo item. Códigos são códigos gerados pelo usuário que permitem distinguir entre itens de linha com o mesmo nome.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Parent]</td>
        <td>Informe o nome do item-pai sob o qual deseja criar o novo item.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Properties]</td>
        <td>Se a lista que você deseja adicionar um item tiver propriedades personalizadas, selecione as propriedades para as quais deseja adicionar valores e, em seguida, adicione os valores.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Subsets]</td>
        <td>Se a lista a qual você deseja adicionar itens tiver subconjuntos personalizados, selecione os subconjuntos aos quais você deseja adicionar o item e selecione <b>[!UICONTROL Yes]</b> para adicionar o novo item a esse subconjunto.</td>
    </tr>
</table>

#### [!UICONTROL Make a custom API Call]

Este módulo permite executar uma chamada de API personalizada para a API [!DNL Anaplan].

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Anaplan] a [!DNL Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo a <code>https://api.anaplan.com/2/0/</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP em [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Insira a string de consulta da solicitação.</p> </td> 
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

#### [!UICONTROL Delete a record]

Este módulo de ação exclui um registro existente.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Anaplan] a [!DNL Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecione ou mapeie a ID do Workspace Anaplan que contém o objeto que você deseja excluir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>Insira ou mapeie a ID do modelo que contém o objeto que você deseja excluir.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Excluir</td> 
   <td> <p>Selecione o tipo de objeto a ser excluído.</p> 
    <ul> 
     <li> <p><b>Ação</b> </p> <p>Selecione ou mapeie a ação a ser excluída.</p> </li> 
     <li> <p><b>Listar item</b> </p> <p>Selecione a lista da qual deseja excluir um item e, em seguida, insira ou mapeie a ID ou o código do item que deseja excluir</p>  </li> 
     <li> <p><b>[!UICONTROL File]</b> </p> <p>Selecione ou mapeie o arquivo a ser excluído.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Esse módulo de ação lê um único registro.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Anaplan] a [!DNL Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecione o tipo de registro a ser lido.</p> 
    <ul> 
     <li> <p><b>Modelo</b> </p> <p>Selecione ou mapeie a ID do modelo que deseja ler</p> </li> 
     <li> <p><b>Lista de modelos</b> </p> <p>Selecione ou mapeie as IDs da Workspace e do Modelo que contêm a Lista que você deseja ler e selecione a Lista. No campo [!UICONTROL Data type], selecione se deseja ler dados ou metadados.</p> </li> 
     <li> <p><b>Versão do modelo</b> </p> <p>Selecione ou mapeie a ID do modelo que deseja ler.</p> </li> 
     <li> <p><b>Usuário</b> </p> <p>Selecione se deseja retornar dados sobre o proprietário da conta que está sendo usada ou outro usuário. Se você selecionar outro usuário, selecione o nome dele.</p> </li> 
     <li> <p><b>Workspace</b> </p> <p>Selecione ou mapeie a ID da Workspace que deseja ler.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Run an action]

Esse módulo de ação importa, exporta, exclui ou processa uma ação.

<table style="table-layout:auto"> 
     <col/>
     <col/>
     <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect Anaplan to Workfront Fusion]</a> neste artigo.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Workspace ID]</td>
        <td>Selecione ou mapeie a ID do Workspace [!DNL Anaplan] em que deseja executar a ação</td>
      </tr>
      <tr >
        <td role="rowheader">[!UICONTROL Model ID]</td>
        <td>Selecione ou mapeie a ID do modelo em que deseja executar a ação.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Action type]</td>
        <td>
          <p>Selecione a ação que deseja executar</p>
            <ul>
              <li>
                <p><b>[!UICONTROL Delete]</b>
                </p>
                <p>Insira ou mapeie a ID da ação que deseja excluir.</p>
              </li>
              <li>
                <p><b>[!UICONTROL Export]</b>
                </p>
                <p>Insira ou mapeie a ID da definição de exportação que você deseja usar. É possível exportar para os seguintes formatos de arquivo:</p>
                  <ul>
                    <li>
                      <p>XLS</p>
                    </li>
                    <li>
                      <p>XLSX</p>
                    </li>
                    <li>
                      <p>CSV</p>
                    </li>
                  </ul>
                </li>
                <li>
                  <p><b>[!UICONTROL Import] </b>
                  </p>
                  <p style="font-weight: normal;">Insira ou mapeie a ID da definição de importação que você deseja usar.</p>
                </li>
                <li>
                 <p><b>[!UICONTROL Process]</b>
                 </p>
                  <p>Insira ou mapeie a ID do processo que deseja usar. </p>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>


#### [!UICONTROL Update a record]

Este módulo de ação atualiza um único registro em [!UICONTROL Anaplan].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Anaplan] a [!DNL Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecione o tipo de registro que deseja atualizar.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL List item]</b> </p> <p>Para campos, consulte <a href="#create-a-list-item" class="MCXref xref">Criar um item de lista</a> neste artigo.</p> </li> 
     <li> <p><b>[!UICONTROL Module cell data]</b> </p> <p>Quando você atualiza os dados da célula, todos os cálculos downstream que usam esses dados também são atualizados.</p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Model ID]</b> </p> <p>Selecione ou mapeie o Modelo que contém a célula que você deseja atualizar.</p> </li> 
       <li> <p><b>[!UICONTROL Module ID]</b> </p> <p>Selecione ou mapeie o módulo que contém a célula que você deseja atualizar</p> </li> 
       <li> <p><b>[!UICONTROL Line item name]</b> </p> <p>Selecione ou mapeie o item de linha da célula que deseja atualizar</p> </li> 
       <li> <p style="font-weight: bold;">[!UICONTROL Dimension ID]</p> <p>Selecione ou mapeie a dimensão que está no item de linha.</p> 
       <p><b>Nota: </b> 
       <ul>
       <li> A chave Dimension (valor) deve ser <code>dimensionName</code> (próximo) ou <code>dimensionId</code> (ID).</li>
       <li>A chave do item (valor) deve ser <code>itemName</code> (texto), <code>itemCode</code> (texto) ou <code>itemId</code> (ID).</li>
       <li>As chaves de Dimension e item devem ser do mesmo tipo (texto ou ID).
       </ul>
        </p> 
        <p>Para obter informações sobre dimensões, pesquise por Dimension no [!DNL Anaplan Anapedia].</p> </li> 
       <li> <p><b>[!UICONTROL Value]</b> </p> <p>Insira ou mapeie o novo valor para a célula.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Model current fiscal year]</b> </p> <p>Informe o ID da Workspace e o ID do Modelo para o qual deseja atualizar o ano fiscal e, em seguida, informe ou mapeie o novo ano para o modelo.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

Este módulo de ação carrega um arquivo para Anaplan. O arquivo já deve ter sido carregado para Anaplan. Você pode usar este módulo para carregá-lo em locais adicionais dentro do Anaplan.
<table style="table-layout:auto">
<col>
<col>
<tbody>
<tr>
<td role="rowheader">[!UICONTROL Connection]</td>
<td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Anaplan] a [!DNL Workfront Fusion]</a> neste artigo.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Workspace ID]</td>
<td>Selecione ou mapeie a ID do Workspace [!DNL Anaplan] para onde deseja carregar um arquivo.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Model ID]</td>
<td>Selecione ou mapeie a ID do modelo em que deseja fazer upload de um arquivo.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL File ID]</td>
<td>Selecione ou mapeie a ID do arquivo que você deseja fazer upload.</td>
</tr>
</tbody>
</table>
</div>

### Pesquisas

#### [!UICONTROL Get record]

Este módulo de pesquisa retorna todos os registros acessíveis do tipo selecionado.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Para obter instruções sobre como criar uma conexão com [!DNL Anaplan], consulte <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Anaplan] a [!DNL Workfront Fusion]</a> neste artigo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record types]</td> 
   <td> <p>Selecione o tipo de registro que deseja recuperar.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Workspaces]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Models]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Line items]</b> </p> <p>Selecione ou mapeie a ID do Modelo que contém os [!DNL line] itens que você deseja recuperar.</p> </li> 
       <li> <p><b>[!UICONTROL Model lists]</b> </p> <p>Selecione ou mapeie a ID da Workspace e a ID do modelo que contém as listas de modelos que você deseja recuperar.</p> </li> 
       <li> <p><b>[!UICONTROL Model calendar]</b> </p> <p>Selecione ou mapeie a ID da Workspace que contém o calendário Modelo que você deseja recuperar.</p> </li> 
       <li> <p><b>[!UICONTROL Model versions]</b> </p> </li> 
       <li> <p>Selecione ou mapeie a ID do Modelo que contém as versões do Modelo que você deseja recuperar.</p> </li> 
       <li> <p><b>[!UICONTROL Users]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Views]</b> </p> <p>Selecione se deseja escolher a visualização por módulo ou por modelo e, em seguida, selecione ou mapeie a ID do módulo ou modelo que contém a visualização que deseja recuperar.</p> </li> 
      </ul> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Return workspace size]</td> 
   <td>Ative essa opção para retornar uma estimativa do tamanho atual do espaço de trabalho. Essa estimativa é baseada nos tamanhos de todos os módulos contidos no espaço de trabalho.</td> 
  </tr> 
 </tbody> 
</table>
