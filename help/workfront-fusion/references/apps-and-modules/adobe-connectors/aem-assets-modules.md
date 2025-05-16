---
title: Módulos do Adobe Experience Manager Assets
description: Com o  [!DNL Adobe Experience Manager Assets] conector para  [!DNL Adobe Workfront Fusion], você pode criar, carregar e atualizar ativos, além de copiar ou mover pastas e ativos.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: 40470e5d2183f690ad65f5e1170f78c37dee8603
workflow-type: tm+mt
source-wordcount: '1727'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager Assets] módulos

Com o conector [!DNL Adobe Experience Manager Assets] para [!DNL Adobe Workfront Fusion], você pode criar, carregar e atualizar ativos, além de copiar ou mover pastas e ativos.

Para obter uma introdução ao vídeo sobre o conector do Adobe Experience Manager Assets, consulte:

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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
   <p>Herdados: Workfront Fusion para Automação e Integração </p>
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

* Você deve ter uma conta [!DNL Adobe Experience Manager Assets] para usar esses módulos.
* Você deve configurar o fluxo de [!UICONTROL servidor para servidor] no [!DNL Adobe Developer console].

  Para obter instruções sobre como configurar o fluxo de [!UICONTROL servidor para servidor] no [!DNL Adobe Developer console], consulte [Gerando tokens de acesso para APIs do lado do servidor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
* Sua conta técnica do Adobe Experience Manager deve ter permissões de gravação.

  Para obter instruções sobre como adicionar permissões de gravação à sua conta técnica da Adobe Experience Manager, consulte [Credenciais de serviço](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) na documentação da Adobe Experience Manager.

## Informações da API do Adobe Experience Manager Assets

O conector do Adobe Experience Manager Assets usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Conectar [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion] {#connect-adobe-experience-manager-assets-to-workfront-fusion}

Para criar uma conexão para seus módulos do [!DNL Adobe Experience Manager Assets]:

1. Clique em [!UICONTROL Adicionar] ao lado da caixa [!UICONTROL Conexão].

2. Selecione o tipo de conexão que você está criando:

   * **[!DNL AEM Assets as a Cloud Service]**

     Esta configuração requer informações do [!DNL Adobe Admin Console].

   * **[!DNL AEM Assets Basic] ([!DNL Adobe Managed Services])**

     Esta configuração requer um nome de usuário e senha.

3. Preencha os campos para o tipo de conexão que você está criando.

   Para [!DNL AEM Assets as a Cloud Service], consulte [Configurar a conexão para [!DNL AEM Assets as a Cloud Service]](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   Para o [!UICONTROL AEM Assets Basic] ([!DNL Adobe Managed Services]), consulte [Configurar a conexão para o [!UICONTROL AEM Assets Basic]](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Clique em **[!UICONTROL Continuar]** para salvar a conexão e retornar ao módulo.


### Configurar a conexão para [!DNL AEM Assets as a Cloud Service]

>[!NOTE]
>
>* As informações destes campos são geradas como parte da configuração do fluxo [!UICONTROL servidor para servidor] no [!DNL Adobe Developer Console]. Você pode encontrar esses valores no arquivo JSON de credenciais de serviço gerado como parte dessa configuração.
>
>   Para obter instruções sobre como configurar o fluxo de [!UICONTROL servidor para servidor] no [!UICONTROL Adobe Developer Console], consulte [Gerar tokens de acesso para APIs do lado do servidor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
>
>* Sua conta técnica do Adobe Experience Manager deve ter permissões de gravação.
>
>   Para obter instruções sobre como adicionar permissões de gravação à sua conta técnica da Adobe Experience Manager, consulte [Credenciais de serviço](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) na documentação da Adobe Experience Manager.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">[!UICONTROL Nome da Conexão]</td>
                  <td>
                      <p>Insira um nome para esta conexão.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL URL da instância sem barra à direita]</td>
                  <td>Insira a URL da instância [!DNL Adobe Experience Manager]. Não inclua uma barra <code>/</code> ao final da URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Opções de preenchimento de detalhes da conta]</td>
                  <td>Selecione se deseja fornecer JSON descrevendo os detalhes da conta ou se deseja inserir os detalhes manualmente.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Detalhes da conta técnica em formato JSON]</td>
                  <td>Se estiver fornecendo JSON, insira ou cole o JSON que descreve os detalhes da sua conta.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL ID do Cliente]</td>
                  <td>Se você inserir detalhes manualmente, insira a ID do cliente gerada na configuração de [!UICONTROL Servidor para servidor].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Segredo do Cliente]</td>
                  <td>Se estiver inserindo detalhes manualmente, insira o Segredo do Cliente gerado na configuração [!UICONTROL Servidor para servidor].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL ID da conta técnica]</td>
                  <td>Se inserir detalhes manualmente, insira a ID da conta técnica. Este é o campo "[!UICONTROL id]" no arquivo JSON de credenciais do cliente.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL ID da Organização]</td>
                  <td class="">Se você inserir detalhes manualmente, insira a ID da organização. Este é o campo "[!UICONTROL org]" no arquivo JSON de credenciais do cliente.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Metaescopos]</td>
                  <td>Insira os Metaescopos gerados na configuração do [!UICONTROL Servidor para servidor].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Chave privada]</td>
                  <td>Insira a chave privada gerada na configuração do [!UICONTROL Server-to-server]. Para extrair a chave privada, clique em [!UICONTROL Extract] e insira o arquivo a ser extraído e a senha do arquivo.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL URL de Autenticação]</td>
                  <td>Digite a URL de autenticação desta conta.</td>
              </tr>
          </tbody>
      </table>


### Configurar a conexão para o AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">[!UICONTROL Nome da Conexão]</td>
                <td>
                    <p>Insira um nome para esta conexão.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL URL da instância sem barra à direita]</td>
                <td>Insira a URL da instância [!DNL Adobe Experience Manager]. Não inclua uma barra <code>/</code> ao final da URL.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Nome de Usuário]</td>
                <td>Insira o nome de usuário para a conta [!DNL AEM Assets] que esta conexão usa.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Senha]</td>
                <td>Digite a senha da conta [!DNL AEM Assets] que esta conexão usa.</td>
            </tr>
        </tbody>
    </table>


## [!DNL Adobe Experience Manager Assets] módulos e seus campos

Ao configurar módulos do [!DNL Adobe Experience Manager Essentials], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!DNL Adobe Experience Manager Essentials] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Copiar uma pasta ou um ativo](#copy-a-folder-or-asset)
* [Criar um registro](#create-a-record)
* [Excluir uma pasta, ativo ou representação](#delete-a-folder-asset-or-rendition)
* [Obter uma lista de pastas](#get-a-folder-listing)
* [Fazer uma chamada de API personalizada](#make-a-custom-api-call)
* [Mover uma pasta ou um ativo](#move-a-folder-or-asset)
* [Atualizar um registro](#update-a-record)
* [Fazer upload de um ativo](#upload-an-asset)

### [!UICONTROL Copiar uma pasta ou um ativo]

Este módulo de ação copia uma pasta ou um ativo para outro local em sua conta da Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion], consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de registro]</td> 
   <td> <p>Selecione se deseja copiar uma pasta ou um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta] / [!UICONTROL Ativo]</td> 
   <td>Selecione ou mapeie a pasta ou o ativo que deseja copiar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Caminho de destino]</td> 
   <td>Selecione ou mapeie o caminho para o local da nova pasta ou ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome da pasta copiada] / [!UICONTROL ativo]</td> 
   <td>Insira um nome para a nova pasta ou ativo. O nome da pasta que é exibido em [!DNL Adobe Experience Manager Assets] é igual ao nome original. O nome inserido aqui aparece no URL da nova pasta ou ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copiar filhos]</td> 
   <td>Se estiver copiando uma pasta, ative essa opção para copiar quaisquer subpastas ou ativos dentro da pasta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Substituir]</td> 
   <td>Habilite essa opção para substituir qualquer pasta ou ativo no local de destino que tenha o mesmo nome da pasta ou do ativo que está sendo copiado.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Criar um registro]

Esse módulo de ação cria uma pasta ou um comentário de ativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion], consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de objeto]</td> 
   <td> <p>Selecione se deseja criar uma pasta ou um comentário em um ativo.</p> 
    <ul> 
     <li> <p>[!UICONTROL Pasta]</p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p>[!UICONTROL Nome]</p> <p>Insira um nome para a pasta. Esse nome aparecerá no caminho do arquivo, portanto, não deve incluir espaços ou outros caracteres. </p> </li> 
       <li> <p>[!UICONTROL Título]</p> <p>Insira um título para a pasta, que pode ser exibido em vez do nome.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Comentário do ativo]</p> <p>Preencha os seguintes campos:</p> 
      <ul> 
       <li> <p>[!UICONTROL Seleção de ativo]</p> <p>Selecione ou mapeie a ID do ativo ao qual deseja adicionar um comentário.</p> </li> 
       <li> <p>[!UICONTROL Comentário]</p> <p>Insira o texto do comentário.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Excluir uma pasta, ativo ou representação]

Este módulo de ação exclui uma pasta, ativo ou representação.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion], consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de registro]</td> 
   <td> <p>Selecione se deseja excluir uma pasta, ativo ou representação.</p> 
    <ul> 
     <li> <p>[!UICONTROL Pasta]</p> <p>Selecione a pasta a ser excluída selecionando as pastas em seu caminho.</p> </li> 
     <li> <p>[!UICONTROL Ativo] </p> <p>Selecione o ativo, selecionando as pastas em seu caminho e, em seguida, o ativo que deseja excluir.</p> </li> 
     <li> <p>[!UICONTROL Representação]</p> <p>Selecione a representação selecionando as pastas em seu caminho.</p> <p>Insira ou mapeie o nome da representação.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Obter uma lista de pastas]

Este módulo de ação recupera uma representação de uma pasta existente e de suas entidades filhas (pastas ou ativos).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion], consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta]</td> 
   <td>Selecione ou mapeie a pasta que deseja recuperar. Para adicionar subpastas ao caminho, clique no ícone de adição e selecione a subpasta.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Fazer uma chamada de API personalizada]

Este módulo de ação faz uma chamada de API personalizada para a API [!DNL Adobe Experience Manager Assets].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion], consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Insira um caminho relativo para sua URL de base [!DNL Adobe Experience Manager].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Método]</p> </td> 
   <td> <p>Selecione o método de solicitação HTTP necessário para configurar a chamada de API. Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Métodos de solicitação HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cabeçalhos]</td> 
   <td> <p>Adicione os cabeçalhos da solicitação no formulário de um objeto JSON padrão.</p> <p>Por exemplo, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] O adiciona cabeçalhos de autorização automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cadeia de Consulta] </td> 
   <td> <p>Insira a string de consulta da solicitação. Para cada par Chave/Valor, clique em <b>[!UICONTROL Adicionar item]</b> e insira a [!UICONTROL Chave] e o [!UICONTROL Valor].</p> </td> 
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

### [!UICONTROL Mover uma pasta ou um ativo]

Este módulo de ação move o ativo ou pasta no caminho fornecido para um novo local.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion], consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de registro]</td> 
   <td> <p>Selecione se deseja mover uma pasta ou um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pasta] / [!UICONTROL Ativo]</td> 
   <td>Selecione ou mapeie a pasta ou o ativo que deseja mover.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Caminho de destino]</td> 
   <td>Selecione ou mapeie o caminho para o local para o qual deseja mover a pasta ou ativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome da pasta movida] / [!UICONTROL ativo]</td> 
   <td>Insira um novo nome para a pasta ou o ativo movido. O nome da pasta que é exibido em [!DNL Adobe Experience Manager Assets] é igual ao nome original. O nome inserido aqui aparece no URL da pasta ou do ativo movido.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Substituir]</td> 
   <td>Habilite essa opção para substituir qualquer pasta ou ativo no local de destino que tenha o mesmo nome da pasta ou do ativo que está sendo movido.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Atualizar um registro]

Este módulo de ação atualiza um registro existente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion], consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo de registro]</td> 
   <td> <p>Selecione se deseja excluir metadados de ativos ou uma representação de ativos.</p> 
    <ul> 
     <li> <p>[!UICONTROL Metadados de ativos]</p> 
      <ul> 
       <li> <p>Selecione o ativo para o qual deseja atualizar metadados.</p> </li> 
       <li> <p>Insira o novo título do ativo.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Representação de ativo]</p> 
      <ul> 
       <li> <p>Selecione o ativo para o qual deseja atualizar a representação.</p> </li> 
       <li> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Carregar um ativo]

Este módulo de ação carrega um ativo para sua conta do [!DNL Adobe Experience Manager Assets].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Para obter instruções sobre como conectar sua conta do [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion], consulte <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Conectar [!DNL Adobe Experience Manager Assets] ao [!DNL Workfront Fusion]</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destino]</td> 
   <td> <p>Selecione a pasta na qual deseja fazer upload de um ativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL arquivo Source]</td> 
   <td>Insira ou mapeie o nome e os dados do arquivo de origem.</td> 
  </tr> 
 </tbody> 
</table>
