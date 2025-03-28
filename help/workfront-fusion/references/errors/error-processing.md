---
content-type: reference
title: Tipos de erro
description: Às vezes, um erro pode ocorrer durante a execução de um cenário. Isso geralmente acontece se um serviço estiver indisponível devido a uma falha na conexão com um serviço ou se uma validação falhar. Este artigo discute os erros comuns que você pode encontrar.
author: Becky
feature: Workfront Fusion
exl-id: abf5f844-d13b-416e-a8b8-2d4ee1786262
source-git-commit: d618d5c4b2306a3b940af7e402f93ced988095a3
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 1%

---

# Tipos de erro

Às vezes, um erro pode ocorrer durante a execução de um cenário. Isso geralmente acontece se um serviço estiver indisponível devido a uma falha de conexão com o serviço ou se uma validação falhar.

[!DNL Adobe Workfront Fusion] distingue entre vários tipos de erro básicos. O tipo de erro determina as próximas ações do cenário do Fusion.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] pacote</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença</td> 
   <td> Novo: Padrão<p>Ou</p><p>Atual: trabalho ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licença</td> 
   <td>
   <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou plano do [!UICONTROL Prime] [!DNL Workfront]: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plano: [!DNL Workfront Fusion] está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>


Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre as licenças do Adobe Workfront Fusion, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Erro de conexão

`ConnectionError`

Erros de conexão são um dos erros mais comuns. Normalmente, elas são causadas pela indisponibilidade do serviço de terceiros por vários motivos, como sobrecarga, manutenção ou interrupção. A manipulação padrão desse erro depende de qual módulo encontrou o erro.

* Se o erro ocorrer no primeiro módulo, a execução do cenário será encerrada com uma mensagem de aviso. [!DNL Workfront Fusion] então tenta executar novamente o cenário em intervalos de tempo crescentes. Se todas as tentativas falharem, [!DNL Workfront Fusion] desativará o cenário.
* Se o erro de conexão ocorrer em outro módulo que não o primeiro, as etapas subsequentes dependerão da opção Permitir armazenamento de execuções incompletas nas configurações avançadas do cenário:

   * Se esta opção estiver habilitada, a execução do cenário será movida para a pasta [!UICONTROL Incomplete executions], onde [!DNL Workfront Fusion] tenta executar novamente o cenário em intervalos de tempo crescentes. Se todas as tentativas falharem, a execução permanecerá na pasta Incomplete executions aguardando resolução manual pelo usuário.

     Para obter mais informações sobre execuções incompletas, consulte [Exibir e resolver execuções incompletas](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).
   * Se essa opção estiver desativada, a execução do cenário terminará com um erro seguido de uma fase de reversão. [!DNL Workfront Fusion] então tenta executar novamente o cenário em intervalos de tempo crescentes. Se todas as tentativas falharem, [!DNL Workfront Fusion] desativará o cenário.

  Para obter mais informações sobre a configuração Permitir o armazenamento de execuções incompletas, consulte [Permitir o armazenamento de execuções incompletas](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) no artigo Definir configurações de cenário.

### Aumento dos intervalos de tempo

O algoritmo para aumentar os intervalos de tempo entre tentativas quando ocorre um erro é conhecido como retrocesso exponencial. Os intervalos de tempo crescentes são definidos da seguinte maneira:

1. 10 minutos
1. 1 hora
1. 3 horas
1. 12 horas
1. 24 horas

O aumento dos intervalos de tempo ajuda a impedir que cenários executados com frequência usem operações em tentativas com falha repetida.

>[!BEGINSHADEBOX]

**Exemplo:**

Um cenário contém o gatilho [!DNL Google Sheets] [!UICONTROL Watch Rows]. [!DNL Google Sheets] fica indisponível por 30 minutos devido a uma manutenção quando [!DNL Workfront Fusion] inicia o cenário, portanto, não é possível recuperar novas linhas. O cenário é interrompido e tenta novamente em 10 minutos. Como [!DNL Google Sheets] ainda está indisponível, [!DNL Workfront Fusion] ainda não pode obter informações sobre novas linhas. A próxima execução do cenário é agendada em 1 hora. [!DNL Google Sheets] está disponível novamente neste momento e o cenário foi executado com êxito.

>[!ENDSHADEBOX]

## Erro de dados

`DataError`

Um erro de dados é gerado quando um item é mapeado incorretamente e não passa na validação executada no lado [!DNL Workfront Fusion] ou no lado do serviço de terceiros.

Se esse erro ocorrer, o cenário, até o qual o módulo falhou, será movido para a pasta de execuções incompletas, onde você poderá solucionar o problema. No entanto, o cenário não pára e continua a ser executado de acordo com seu cronograma. Para interromper a execução do cenário quando Erro de dados for exibido, ative a opção Processamento sequencial no painel Configurações do cenário.

Se você não tiver habilitado a opção [!UICONTROL Allow storing incomplete executions] nas configurações do cenário, a execução do cenário será encerrada com o erro e uma reversão será executada.

## Erro de dados duplicados

`DuplicateDataError`

Se [!DNL Workfront Fusion] tentar inserir o mesmo pacote duas vezes em um serviço que não permite dados duplicados, um erro de dados duplicados será gerado. Se este erro ocorrer, [!DNL Workfront Fusion] continuará da mesma forma que para o erro de dados.

Para obter mais informações, consulte [Erro de Dados](#data-error) neste artigo.


## Erro de token de acesso inválido

`InvalidAccessTokenError`

Ocorre um erro de token de acesso inválido quando o [!DNL Workfront Fusion] não pode acessar sua conta registrada com um serviço de terceiros. Isso geralmente acontece quando você revoga direitos de acesso para [!DNL Workfront Fusion] na administração de um determinado serviço, mas os cenários que usam esse serviço continuam sendo executados de acordo com o agendamento.

Se esse erro ocorrer, a execução do cenário será interrompida imediatamente. O restante do cenário que começa no módulo em que o erro ocorreu é movido para a pasta de execuções incompletas.

## Erro de limite de taxa

`RateLimitError`

Se um limite definido por um determinado serviço for excedido, um erro de limite de taxa será gerado. Se este erro ocorrer, [!DNL Workfront Fusion] continuará da mesma forma que para o Erro de Conexão.

Para obter mais informações, consulte [Erro de conexão](#connection-error) neste artigo.

## Erro de dados incompletos

`IncompleteDataError`

Um erro de dados incompleto ocorre somente com acionadores. Esse erro é gerado se um acionador falha ao baixar os dados necessários de um determinado serviço.

Se um cenário terminar com `IncompleteDataError`, seu comportamento adicional dependerá de sua configuração de [!UICONTROL Max number of consecutive errors].

Para obter mais informações, consulte [Número de erros consecutivos](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) no artigo Definir configurações de cenário.

>[!BEGINSHADEBOX]

**Exemplo:**

Um cenário tem o gatilho [!DNL Workfront] [!UICONTROL Watch Record] definido para observar documentos. O cenário é executado enquanto você faz upload de um documento grande, como um vídeo longo. Como [!UICONTROL Workfront Fusion] tenta baixar o vídeo enquanto ele ainda está carregando no Workfront, o cenário termina com `IncompleteDataError`.

>[!ENDSHADEBOX]

## Erro de tempo de execução

`RuntimeError`

Qualquer erro que apareça durante a execução do cenário e não seja um desses tipos de erro é relatado como um `RunTimeError`.

Se um cenário terminar com `RuntimeError`, seu comportamento dependerá da configuração [!UICONTROL Max number of consecutive errors].

Para obter mais informações, consulte [Número de erros consecutivos](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) no artigo Definir configurações de cenário.


>[!NOTE]
>
>Se um cenário iniciar com um gatilho instantâneo e encontrar esse erro, a configuração [!UICONTROL Max number of consecutive errors] será ignorada e o cenário será desativado imediatamente.
>Para obter mais informações, consulte [Acionadores instantâneos](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) no artigo Visão geral de módulos.

## Erro de inconsistência

`InconsistencyError`

Se qualquer um desses erros ocorrer durante a fase de confirmação ou reversão, o cenário será encerrado com um Erro de inconsistência.

Se esse erro aparecer em um cenário, a execução do cenário será imediatamente interrompida.

## Advertência

Ao executar um cenário, você pode receber um aviso informando sobre um problema. Um aviso não impede que o cenário seja concluído com êxito.

Por exemplo, um aviso pode aparecer quando o tamanho máximo de arquivo permitido for excedido e a opção [!UICONTROL Enable data loss] estiver desabilitada.

## Recursos

Para obter mais informações sobre mapeamento, consulte [Visão geral do mapeamento](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

Para obter informações sobre execuções incompletas, consulte [Exibir e resolver execuções incompletas](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Para obter informações sobre o painel de configurações de cenário, consulte [Definir configurações de cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

Para obter informações sobre agendamentos, consulte [Agendar um cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Para obter informações sobre fases do cenário, consulte [Execução do cenário, ciclos e fases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

Para obter informações sobre a opção Habilitar perda de dados, consulte [Habilitar perda de dados](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) no artigo Definir configurações de cenário.
