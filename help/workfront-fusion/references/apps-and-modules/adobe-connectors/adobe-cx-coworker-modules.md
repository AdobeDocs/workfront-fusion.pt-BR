---
title: Módulos do Adobe CX Enterprise Coworker
description: Use o conector do Adobe CX Enterprise Coworker no Adobe Workfront Fusion para enviar um prompt em linguagem natural ao Co-worker e usar sua resposta em um cenário.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 6efe84af0487893a3c33ba2bf6e3db5200f25446
workflow-type: tm+mt
source-wordcount: '1974'
ht-degree: 6%
---
# Módulos do Adobe CX Enterprise Coworker

Use o conector do Adobe CX Enterprise Coworker no Adobe Workfront Fusion para enviar um prompt em linguagem natural ao Co-worker e usar sua resposta em um cenário. O colega interpreta a sua solicitação e pode usar as ferramentas disponíveis na sua conta para realizar o trabalho.

O conector fornece dois módulos:

* **[!UICONTROL Executar um Prompt]** inicia uma nova solicitação e, por padrão, aguarda o resultado.
* **[!UICONTROL Obter Status de Execução]** verifica uma solicitação iniciada anteriormente.

## Requisitos de acesso

<!-- BECKY CHECK ME: This table is copied from other Fusion connector articles. The source material does not list access requirements, but says you need an Adobe account that has access to Coworker. Confirm the requirements and whether Coworker needs its own license or entitlement. -->

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

## Pré-requisitos

Você deve ter uma conta do Adobe com acesso ao Adobe CX Enterprise Coworker.

## Conectar o Adobe CX Enterprise Coworker ao Workfront Fusion

Entre com uma conta da Adobe que tenha acesso ao Colaborador e a todos os serviços necessários para a sua solicitação.

Para criar uma conexão:

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
      <tr>
        <td role="rowheader">ID do cliente</td>
        <td>
          <p>Insira ou mapeie uma substituição opcional para esta conexão. Caso contrário, use a clientId gerenciada pela plataforma desse tipo de conta. Registre o URL de retorno de chamada do Fusion exibido para a conta de Colaborador dedicada.</p>
        </td>
      <tr>
        <td role="rowheader">Segredo do cliente</td>
        <td>
          <p>Insira ou mapeie uma substituição opcional para esta conexão. Caso contrário, use o clientSecret gerenciado por plataforma desse tipo de conta. Use credenciais emitidas para o ambiente IMS configurado.</p>
        </td>
    </tbody>
   </table>

1. Clique em **[!UICONTROL Continuar]**.

Se não conseguir fazer logon ou usar um serviço necessário, entre em contato com o administrador.

## Módulos do Adobe CX Enterprise Coworker e seus campos

>[!WARNING]
>
>Nunca inclua senhas ou outras credenciais em um prompt.

### Obter Status de Execução

Este módulo de ação verifica o estado atual de uma tarefa iniciada por **[!UICONTROL Executar um prompt]**.

Este módulo verifica a tarefa uma vez. Ela não inicia uma nova tarefa ou continua verificando até que a tarefa seja concluída. Se o resultado ainda estiver pendente, verifique novamente mais tarde.

>[!NOTE]
>
>Não converta a ID da tarefa em um número, arredonde-a ou reformate-a. Se o Colaborador responder ao prompt original imediatamente sem uma ID de tarefa, não será necessário verificar o status.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Incluir resultado bruto] <i>(Opcional, avançado)</i></td> 
   <td> <p>Essa opção está desativada por padrão. Inclua a resposta completa do colaborador na saída. A resposta pode conter informações confidenciais.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Selecione a mesma conexão usada na execução original <b>[!UICONTROL Executar um Prompt]</b>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de Tarefa]</td> 
   <td> <p>Mapeie a ID de Tarefa retornada por <b>[!UICONTROL Executar um Prompt]</b>. Manter como texto exatamente como retornado.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Executar um prompt

Esse módulo de ação envia uma instrução ao Colaborador, como o resumo de texto ou a coleta de informações usando as ferramentas disponíveis para sua conta.

Cada execução envia o prompt uma vez e inicia uma nova conversa. Não é necessário selecionar um modelo de IA ou fornecer uma chave separada do provedor de IA.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Selecione sua conexão com o Colaborador. Para obter instruções, consulte <a href="#connect-adobe-cx-coworker-to-workfront-fusion" class="MCXref xref">Conectar o Adobe CX Enterprise Coworker ao Workfront Fusion</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Prompt de usuário]</td> 
   <td> <p>Digite sua instrução. Você pode usar várias linhas e mapear informações de módulos anteriores.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aguardar conclusão] <i>(Opcional, avançado)</i></td> 
   <td> <p>Essa opção está ativada por padrão. Ative essa opção se desejar que o módulo aguarde a conclusão da tarefa ou exigir atenção. Desative para retornar o resultado inicial imediatamente.</p><p>Para obter mais informações, consulte <a href="#wait-for-completion">Aguardar a conclusão</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Incluir resultado bruto] <i>(Opcional, avançado)</i></td> 
   <td> <p>Essa opção está desativada por padrão. Ative essa opção se desejar que o módulo inclua a resposta completa do colaborador na saída. A resposta pode conter informações confidenciais.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
> Recomendamos deixar **[!UICONTROL Incluir resultado bruto]** desativado, a menos que você precise da resposta completa para uma finalidade específica. Os resultados brutos podem conter informações confidenciais e não são um registro completo garantido de cada ação. Analise o que um resultado bruto contém antes de salvá-lo, compartilhá-lo ou passá-lo para outro serviço.

#### Aguardar a conclusão

Quando **[!UICONTROL Aguardar a conclusão]** está ativado, o módulo verifica a tarefa após uma espera de cinco segundos. Se a tarefa ainda estiver pendente, o módulo aguardará mais cinco segundos antes de verificar novamente. Cada verificação também leva tempo para receber uma resposta. A verificação de status não envia o prompt novamente.

A espera para quando a tarefa é concluída, falha, é cancelada ou rejeitada ou precisa da sua entrada ou autorização. Se o Colaborador fornecer uma resposta imediata, o módulo a retornará sem outras verificações.

Quando **[!UICONTROL Aguardar a conclusão]** estiver desativado, o módulo retornará o primeiro resultado sem esperar a conclusão da tarefa. Inspecionar **[!UICONTROL Estado]**, **[!UICONTROL Concluído]** e **[!UICONTROL Requer atenção]** para decidir o que fazer em seguida. Uma tarefa já pode ser concluída quando o primeiro resultado chegar.

A espera está sujeita ao tempo limite do módulo do Fusion. Se o módulo atingir o tempo limite ou parar, o Colaborador pode continuar trabalhando. Nesse caso, talvez você não receba uma saída ou uma ID de tarefa.

Para trabalho mais demorado, desative a espera e salve a **[!UICONTROL ID da Tarefa]** inicial para poder verificar a tarefa mais tarde. Não executar automaticamente o prompt novamente após um tempo limite. A primeira solicitação pode já estar em andamento e repeti-la pode duplicar as alterações.


## Saída do módulo

Ambos os módulos retornam as seguintes informações quando terminam sem erros.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Tarefa]</td> 
   <td> <p>Identifica a tarefa. Isso fica vazio quando o Colaborador fornece uma resposta imediata sem criar uma tarefa. Use este valor com <b>[!UICONTROL Obter Status de Execução]</b>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de Contexto]</td> 
   <td> <p>Identifica a conversa. Não é uma entrada para continuar a conversa.</p><p>Para obter mais informações, consulte <a href="#use-previous-answers">Usar respostas anteriores</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td> <p>O estado atual da tarefa. Consulte <a href="#task-states" class="MCXref xref">Estados da tarefa</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Concluído]</td> 
   <td> <p>Verdadeiro quando a tarefa é concluída ou o Colaborador fornece uma resposta imediata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Requer atenção]</td> 
   <td> <p>Verdadeiro quando o Colaborador precisa de entrada ou autorização.</p><p>Para obter mais informações, consulte <a href="#requests-that-need-attention">Solicitações que precisam de atenção</a> neste artigo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Texto do assistente final]</td> 
   <td> <p>A resposta final quando a tarefa for concluída. Está vazio enquanto a tarefa está pendente ou requer atenção. Uma resposta concluída também não pode ter texto de resposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artefatos de texto (podem incluir texto intermediário)]</td> 
   <td> <p>Texto retornado durante o trabalho. Cada item pode incluir uma ID de artefato, um Nome e um Texto. Esses itens não são necessariamente respostas finais.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resultado bruto (aceitação)]</td> 
   <td> <p>A resposta completa. Isso é incluído somente quando <b>[!UICONTROL Incluir resultado bruto]</b> está ativado.</p> </td> 
  </tr> 
 </tbody> 
</table>

Use **[!UICONTROL Texto do assistente final]** para a resposta em vez de combinar todos os artefatos de texto. Os artefatos podem incluir descrições de progresso ou outro texto intermediário.

### Solicitações que precisam de atenção

O colaborador pode precisar de mais informações ou autorização antes de continuar. Quando isso ocorrer, **[!UICONTROL Requer atenção]** é verdadeiro e **[!UICONTROL Concluído]** é falso. Direcionar o resultado para uma pessoa em vez de tratá-lo como trabalho concluído.

Esses módulos não podem responder a uma pergunta de acompanhamento ou aprovar uma ação em seu nome. **[!UICONTROL Obter Status de Execução]** pode verificar se o estado da tarefa foi alterado, mas não resolve a solicitação de entrada ou autorização.

### Usar respostas anteriores

A cada **[!UICONTROL Executar um Prompt]**, a execução inicia uma nova conversa. Para consultar uma resposta anterior, inclua a pergunta e a resposta relevantes como texto no novo prompt. Isso fornece o contexto do Colaborador, mas não retoma a conversa anterior.

**[!UICONTROL A ID de Contexto]** identifica a conversa associada ao resultado. Você não pode fornecê-lo a esses módulos para continuar uma conversa.

>[!IMPORTANT]
>
>**[!UICONTROL Concluído]** não garante que a ação comercial solicitada foi bem-sucedida. Por exemplo, o Colaborador pode terminar explicando que uma ferramenta necessária não estava disponível. Revise a resposta e verifique qualquer resultado necessário antes de executar a próxima ação.

### Estados da tarefa

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><code>submitted</code>, <code>working</code></td> 
   <td> <p>A tarefa está pendente. <b>[!UICONTROL Concluído]</b> é falso. <b>[!UICONTROL Executar um Prompt]</b> continua aguardando quando a espera está ativada. Caso contrário, salve a ID da tarefa e verifique mais tarde.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>completed</code></td> 
   <td> <p><b>[!UICONTROL Concluído]</b> é verdadeiro. Revise <b>[!UICONTROL Texto do assistente final]</b> e o resultado esperado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>input-required</code>, <code>auth-required</code></td> 
   <td> <p>A tarefa precisa de atenção. <b>[!UICONTROL Concluído]</b> é falso e <b>[!UICONTROL Requer atenção]</b> é verdadeiro. A espera para. Direcionar o resultado para análise humana.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>failed</code>, <code>canceled</code>, <code>rejected</code></td> 
   <td> <p>O módulo relata um erro em vez de um resultado normal.</p> </td> 
  </tr> 
 </tbody> 
</table>

Um resultado pendente ou que requer atenção não é uma conclusão bem-sucedida, mesmo que o módulo retorne sem erro.

## Exemplos

### Resumir uma atualização

1. Adicione **[!UICONTROL Executar um Prompt]** e selecione sua conexão.
1. Digite o seguinte no campo **[!UICONTROL Prompt do usuário]**:

   ```text
   Summarize the following project update in three bullet points.
   Use only the supplied text; do not call tools or change any records.
   
   The planning workshop is complete. Two dependencies need confirmation.
   The team will review the delivery estimate on Friday.
   ```

1. Deixe **[!UICONTROL Aguardar conclusão]** ativado e **[!UICONTROL Incluir resultado bruto]** desativado.
1. Se **[!UICONTROL Requer atenção]** for verdadeiro, encaminhe o resultado para revisão humana. Se **[!UICONTROL Concluído]** for verdadeiro, mapeie **[!UICONTROL Texto do assistente final]** para a próxima etapa.

A redação gerada por IA pode variar. Analise os resultados onde a precisão é importante.

### Verificar uma tarefa mais longa mais tarde

1. Adicione **[!UICONTROL Executar um Prompt]**, selecione sua conexão e insira sua instrução.
1. Desative **[!UICONTROL Aguardar a conclusão]**.
1. Inspecione o resultado inicial.

   * Se a tarefa estiver concluída, processe o resultado.
   * Se a tarefa exigir atenção, encaminhe o resultado para revisão.
   * Se a tarefa estiver pendente, salve a **[!UICONTROL ID da Tarefa]** como texto e anote qual conexão você usou.

1. Mais tarde, use **[!UICONTROL Obter Status de Execução]** com essa conexão e essa ID de Tarefa.
1. Se a tarefa ainda estiver pendente, organize outra verificação dentro dos limites do seu cenário. Processe o resultado uma vez ao concluir e trate a atenção ou os erros separadamente.

Não execute o prompt original novamente apenas para verificar seu progresso.

## Considerações de uso

* O colega de trabalho pode usar as ferramentas e executar ações permitidas pela sua conta, incluindo alterações nos registros. Use prompts confiáveis e uma conta com acesso apropriado.
* Esses módulos não fornecem uma maneira de restringir ferramentas individuais. Instruções como &quot;não altere nada&quot; descrevem sua intenção, mas não são um modo obrigatório somente leitura.
* As ferramentas e habilidades disponíveis variam de acordo com a conta. O conector não fornece um seletor de habilidades ou garante uma ação específica, como criar uma jornada ou atualizar um projeto. Não presuma que as solicitações que precisam de aprovação serão concluídas de forma autônoma.
* O conector é iniciado e verifica as solicitações do Colaborador. Ele não monitora alterações em projetos nem salva respostas automaticamente em outro aplicativo. Adicione os módulos de acionamento, armazenamento e acompanhamento apropriados ao seu cenário, conforme necessário.
* As respostas geradas por IA podem estar incompletas ou imprecisas. Valide resultados importantes antes de usá-los para fazer alterações ou tomar decisões.
* O conector não repete automaticamente uma solicitação com falha. Certifique-se de que o tratamento de erros do seu cenário não repita um prompt cujo resultado seja incerto.

## Solução de problemas

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Um campo obrigatório está ausente</td> 
   <td> <p>Selecione uma conexão e insira o prompt ou a ID da tarefa necessário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Falha de entrada ou acesso negado</td> 
   <td> <p>Faça logon novamente e verifique se sua conta da Adobe tem acesso ao Colaborador e aos serviços necessários. Entre em contato com o administrador, se necessário.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tarefa não encontrada</td> 
   <td> <p>Verifique se a ID da tarefa não foi alterada e se você está usando a conexão original. Uma nova tarefa pode não estar visível imediatamente. Verifique o status posteriormente em vez de enviar o prompt novamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Uma verificação de status falha</td> 
   <td> <p>Se o erro incluir a ID de Tarefa aceita, use <b>[!UICONTROL Obter Status de Execução]</b> para investigar essa tarefa. Não reinicie o prompt automaticamente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Executar um prompt atinge o tempo limite ou perde a resposta</td> 
   <td> <p>A tarefa pode ter sido iniciada mesmo se você não tiver recebido a ID dela. Investigue antes de repetir a solicitação para evitar trabalho duplicado.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">A fusão expira enquanto aguarda</td> 
   <td> <p>O colega de trabalho ainda pode estar trabalhando. Verifique a tarefa se tiver sua ID. Para tarefas longas futuras, desative a espera e salve a ID inicial primeiro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Colaborador ou um serviço necessário não está disponível</td> 
   <td> <p>Compartilhe o erro exibido com o administrador, sem credenciais ou conteúdo de resultado confidencial.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: Confirm the exact module and field labels in the UI (Run a Prompt, Get Execution Status, User prompt, Wait for completion, Include raw result, Task ID, and the output item names). Also confirm that the module is listed under "Adobe CX Enterprise Coworker" in the app picker. -->
