---
title: Módulos MCP do Adobe Fusion
description: Com o módulo MCP do Adobe Fusion, é possível enviar um prompt em inglês simples para o servidor MCP do Adobe Fusion e permitir que um modelo de IA execute a solicitação.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 06ba1c54288fff09f866bffa5c3fce7381c71ad2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 14%
---
# Módulos MCP do Adobe Fusion

O conector MCP do Adobe Fusion envia um prompt em inglês simples para o servidor MCP (Adobe Fusion Model Context Protocol). Um modelo de IA interpreta sua solicitação e chama as ferramentas do Fusion necessárias para concluí-la.

O conector funciona somente com o servidor Adobe Fusion MCP hospedado. Você não pode apontá-lo para outro servidor MCP.

Para obter mais informações sobre o MCP em cenários do Fusion, consulte [Adicionar um prompt de IA ao seu cenário](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conectar o Adobe Fusion MCP ao Workfront Fusion

Você pode criar uma conexão diretamente do módulo MCP do Adobe Fusion.

1. No módulo MCP do Adobe Fusion, clique em **[!UICONTROL Adicionar]** ao lado do campo **Conexão**.
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
        <td>
          <p>Selecione se você está se conectando a um ambiente de produção ou não produção.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Tipo</td>
        <td>
          <p>Selecione se você está se conectando a uma conta de serviço ou a uma conta pessoal.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Clique em **[!UICONTROL Continuar]**.

Você é redirecionado para a página de logon do Adobe. Faça logon com sua conta da Adobe e aprove o acesso. Você será redirecionado de volta para o Workfront Fusion e a nova conexão estará disponível no módulo.

## Módulo MCP do Adobe Fusion e seus campos

### Processar um prompt de usuário

Esse módulo de ação envia um prompt em inglês simples para o servidor MCP do Adobe Fusion. Um modelo de IA interpreta o prompt, chama as ferramentas do Fusion necessárias para concluí-lo e retorna o resultado.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Chave LLM <i>(Opcional, avançada)</i></td> 
   <td> <p>Por padrão, esse módulo processa seu prompt usando a IA gerenciada da Adobe e você não precisa selecionar uma chave.</p> <p>Para usar seu próprio provedor de IA, selecione uma chave LLM existente ou crie uma nova clicando em <b>Adicionar</b> e inserindo as seguintes informações:</p>
     <ul>
       <li><b>Nome da chave</b>: insira um nome para a nova chave.</li>
       <li><b>LLM</b>: selecione o modelo de idioma grande ao qual esta chave está associada. Os provedores compatíveis são OpenAI, Anthropic e Amazon Bedrock.</li>
       <li><b>Chave</b>: insira ou mapeie sua chave de API para o provedor selecionado.</li>
       <li><b>Modelo</b>: selecione o modelo LLM que a chave usará.</li>
       <li><b>Outros campos</b>: insira valores para quaisquer outros campos exigidos pelo seu LLM.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Para obter instruções sobre como conectar o Adobe Fusion MCP ao Workfront Fusion, consulte <a href="#connect-adobe-fusion-mcp-to-workfront-fusion" class="MCXref xref">Connect Adobe Fusion MCP to Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>Ferramentas somente leitura <i>(Opcional)</i></td> 
   <td> <p>Selecione ferramentas específicas somente leitura para restringir a IA. Se nenhuma for selecionada, todas as ferramentas somente leitura nesta categoria serão permitidas.</p> </td> 
  </tr> 
  <tr> 
   <td>Ferramentas de gravação/exclusão <i>(Opcional)</i></td> 
   <td> <p>Selecione ferramentas específicas de gravação ou exclusão para restringir a IA. Se nenhuma for selecionada, todas as ferramentas de gravação e exclusão nesta categoria serão permitidas.</p> <p>Para garantir que um cenário autônomo nunca execute uma ação destrutiva, recomendamos deixar esse campo definido como uma seleção deliberadamente vazia, em vez de deixá-lo irrestrito.</p> </td> 
  </tr> 
  <tr> 
   <td>Insira seu prompt</td> 
   <td> <p>Insira ou mapeie a instrução, em inglês simples, que você deseja que a IA execute.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Restringir as ferramentas que a IA pode chamar

Você pode limitar quais ferramentas do Fusion a IA pode chamar selecionando ferramentas nos campos Ferramentas somente leitura e Ferramentas de gravação/exclusão.

* Se você deixar um campo vazio, a IA poderá chamar cada ferramenta nessa categoria.
* Se você deixar ambos os campos vazios, a IA poderá chamar cada ferramenta no servidor do Fusion MCP.

Para impedir que um cenário autônomo execute uma ação de gravação ou exclusão, selecione somente as ferramentas que deseja permitir no campo Ferramentas somente leitura e selecione pelo menos uma ferramenta no campo Ferramentas de gravação/exclusão que você não ache mais confortável com a chamada de IA.

Os nomes das ferramentas nas listas vêm do servidor Fusion MCP.

#### Como o módulo processa seu prompt

* O módulo não tem uma curva de acompanhamento. Se o seu prompt não estiver claro, a IA faz uma suposição razoável e a declara na resposta em vez de fazer uma pergunta.
* A IA verifica as informações que podem mudar usando as ferramentas.
* A IA não executa nenhuma ação de gravação ou exclusão além do que seu prompt solicita.
* O módulo requer uma conexão válida. Ele não é executado sem um.

#### Saída

O módulo retorna as seguintes informações, que você pode mapear nos módulos subsequentes no cenário:

* **Resposta**: a resposta final da IA, como texto.
* **Trilha de Auditoria**: um registro da sessão, incluindo as ferramentas chamadas, seus argumentos e resultados, além dos tempos.
* **Resumo**: totais da sessão, incluindo o número de chamadas de ferramenta bem-sucedidas e o status final.
