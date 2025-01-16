---
title: Resolver erros tratados pela diretiva Break
description: Às vezes, é útil executar novamente um módulo com falha se houver uma chance de o motivo da falha ser resolvido rapidamente.
author: Becky
feature: Workfront Fusion
exl-id: d568942c-2cd5-430c-bdbf-e1496da25b50
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Resolver erros tratados pela diretiva Break

Quando um erro é tratado pela diretiva Break, um registro é criado na pasta Incomplete executions. Esse registro armazena o estado da execução do cenário, juntamente com os dados dos módulos anteriores. O registro faz referência ao módulo em que o erro se originou e contém informações sobre os dados recebidos pelo módulo como entrada. Para cada pacote de dados que causa o erro, um registro separado é criado.

Para obter mais informações, consulte [Exibir e resolver execuções incompletas](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

## Resolver erros resultantes da diretiva de Interrupção

Você pode resolver o erro manualmente atualizando o cenário (se necessário) e executando-o uma vez.

Você também pode configurar o cenário para processar automaticamente uma execução incompleta reexecutando o cenário. Para configurar o módulo para processar execuções incompletas:

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário no qual deseja adicionar a solução alternativa.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no ícone **Controle de Fluxo** ![Controle de fluxo](assets/flow-control-icon.png) e selecione **Quebra**.
1. No módulo Break, habilite a opção [!UICONTROL **Concluir execução automaticamente**].
1. No campo **Número de tentativas**, insira ou mapeie o número máximo de tentativas que o módulo deverá repetir a execução

   Este número deve estar entre 1 e 100.
1. No campo **Intervalo entre tentativas**, digite ou mapeie o número de minutos entre cada nova tentativa.

Com essa opção habilitada, quando ocorre um erro, a execução incompleta é recuperada (após o tempo especificado no campo [!UICONTROL Interval between attempts]) e executada com os dados de entrada originais. Isso se repetirá até que a execução do módulo seja concluída sem erros ou até que o Número de tentativas especificado seja atingido.

>[!NOTE]
>
>Se a tentativa inicial falhar, o intervalo entre as tentativas aumenta exponencialmente a cada duas tentativas.


Quando a opção Execução automática está habilitada, a execução do cenário é marcada como &quot;Sucesso&quot; porque a repetição automática do manipulador de erros de Interrupção está lidando com o problema automaticamente. Nesse caso, os usuários não recebem um email sobre a execução com falha.

Quando a opção Automatically complete execution está desativada, a execução é marcada como &quot;Aviso&quot;.

Há algumas exceções para execuções que estão sendo armazenadas em Execuções incompletas e, com alguns tipos de erro, a repetição automática de uma execução de cenário não é possível.

## Recursos

Para obter mais informações, consulte [Permitir o armazenamento de execuções incompletas](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) no artigo Definir configurações de cenário.
