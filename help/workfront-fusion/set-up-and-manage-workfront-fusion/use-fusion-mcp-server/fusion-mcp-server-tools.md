---
title: Ferramentas de servidor do Adobe Workfront Fusion MCP
description: Lista de referência das ferramentas que o servidor MCP do Adobe Workfront Fusion expõe às plataformas de agente de IA e ao Colaborador.
source-git-commit: 322a34df48a5218bc045e6cac6a5a8b3837e8c2e
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 7%
---

# Ferramentas de servidor do Adobe Workfront Fusion MCP


Este artigo lista as ferramentas que o servidor MCP do Adobe Workfront Fusion expõe a um agente de IA conectado. O agente chama essas ferramentas em seu nome quando você solicita que elas localizem, inspecionem, criem, executem, atualizem ou excluam itens do Fusion.

As mesmas ferramentas estão disponíveis em todas as superfícies suportadas: conexões MCP personalizadas em Claude, ChatGPT, Copilot ou no seu próprio agente; e Coworker, ambos independentes e no painel direito do Fusion. Para instalação, consulte [Configurar o servidor MCP do Adobe Workfront Fusion](configure-fusion-mcp-server.md).

O agente atua no Fusion usando suas funções de Adobe ID, organização do Fusion e equipe. Uma ferramenta só funciona se você tiver a permissão correspondente no Fusion. A Adobe não se responsabiliza pelas alterações que o agente faz nos dados do Fusion.

## Ações de leitura e gravação

Cada ferramenta é classificada como:

* **Leitura**: recupera informações sem alterar nada, como listar cenários ou obter uma execução.
* **Gravação**: cria, altera, executa ou exclui dados do Fusion, como clonar um cenário ou limpar uma fila de webhook.

## Ferramentas da organização

A organização ativa se aplica a todas as outras ferramentas na sessão atual.

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Listar organizações | `fusion_orgs_list` | Ler | Lista as organizações do Fusion que você pode acessar, com ID, região (zona) e rótulo. |
| Definir organização ativa | `fusion_orgs_set` | Session | Alterna a organização ativa para a sessão atual. Não altera nenhum dado do Fusion. |

## Ferramentas de Cenário

### Cenários

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Listar cenários | `fusion_scenarios_list` | Ler | Lista cenários na organização. |
| Obter cenário | `fusion_scenarios_get` | Ler | Retorna um cenário, incluindo seu blueprint completo. |
| Obter dependências de cenário | `fusion_scenarios_getDependencies` | Ler | Retorna as conexões, as chaves, os armazenamentos de dados, as estruturas de dados e os webhooks das referências de blueprint do cenário. |
| Localizar cenários dependentes | `fusion_scenarios_dependents` | Ler | Localiza cenários que fazem referência a um determinado webhook, armazenamento de dados, estrutura de dados, conexão, chave ou cenário. Útil para análise de impacto antes de alterar ou excluir um recurso. |
| Validar blueprint | `fusion_scenarios_validate_blueprint` | Ler | Valida estruturalmente um blueprint em relação a uma equipe (referências de módulo, conexões, campos obrigatórios) sem salvar nada. |
| Criar cenário | `fusion_scenarios_create` | Gravar | Cria um cenário em uma equipe a partir de um blueprint, com nome, descrição, pasta, agendamento e processamento sequencial opcionais. |
| Clonar cenário | `fusion_scenarios_clone` | Gravar | Clona um cenário no mesmo grupo ou em um grupo diferente. Ao clonar entre equipes, você mapeia cada conexão, webhook, armazenamento de dados, estrutura de dados e chave para um recurso de destino. Opcionalmente, continua a partir do último registro processado. |
| Atualizar cenário | `fusion_scenarios_update` | Gravar | Altera o nome, a descrição, a pasta, o agendamento ou o estado ativo (ativar/desativar). Também pode restaurar um cenário excluído. |
| Executar cenário uma vez | `fusion_scenarios_execute` | Gravar | Executa um cenário uma vez e aguarda (até um tempo limite) o resultado, retornando o status e qualquer mensagem de erro. Não compatível com cenários instantâneos (acionados por webhook). |
| Excluir cenário | `fusion_scenarios_delete` | Gravar | Exclui um cenário. Os cenários excluídos podem ser restaurados com **Atualizar cenário**. |

Exemplo de prompts:

* _Quais cenários ativos na equipe de marketing não são editados há 6 meses?_
* _Que conexões o cenário &quot;Salesforce → Workfront sync&quot; utiliza?_
* _Clonar &quot;Entrada de clientes potenciais&quot; na equipe de Vendas e trocar na conexão Salesforce de Vendas._
* _Validar este blueprint antes de eu importá-lo._
* _Execute o &quot;Relatório noturno&quot; uma vez e diga-me se ele for bem-sucedido._

### Versões de cenário

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Listar versões de cenário | `fusion_scenario_versions_list` | Ler | Lista as versões salvas de um cenário. Filtrar por `version`, `createdAt`, `comment`. |
| Obter versão do cenário | `fusion_scenario_versions_get` | Ler | Retorna o blueprint e os metadados de uma versão específica. |

Exemplo de prompts:

* _O que mudou entre a versão 12 e a versão 14 deste cenário?_

### Pastas

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Listar pastas | `fusion_folders_list` | Ler | Lista pastas de cenários, com contagens de cenários. |
| Criar pasta | `fusion_folders_create` | Gravar | Cria uma pasta em uma equipe. |
| Renomear pasta | `fusion_folders_update` | Gravar | Renomeia uma pasta. |
| Excluir pasta | `fusion_folders_delete` | Gravar | Exclui uma pasta. |

## Ferramentas de execução

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Listar execuções | `fusion_executions_list` | Ler | Lista as execuções de um cenário ou de uma execução incompleta. Filtrar por `status` (por exemplo `status==3` para erros, `status==2` para avisos), `timestamp`, `duration`, `bundles`, `operations`, `transfer`. Opcionalmente, inclui execuções de verificação. |
| Obter execução | `fusion_executions_get` | Ler | Retorna uma única execução e metadados sobre seu cenário ou execução incompleta. |

Exemplo de prompts:

* _Mostrar minhas execuções com falha de &quot;Sincronização de fatura&quot; de ontem e resumir os erros._
* _Qual execução deste cenário usou mais operações esta semana?_

## Ferramentas de operações (uso)

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Obter operações | `fusion_operations_get` | Ler | Retorna uma série temporal de operações (por dia ou mês) para um intervalo de datas de até 1 ano. Filtre por grupo, cenário ou pacote; agrupe por módulo, pacote, cenário ou grupo. |
| Obter resumo de operações | `fusion_operations_summary_by_org` | Ler | Retorna o total de operações por cenário e equipe para um intervalo de datas, mais o total geral. |

Exemplo de prompts:

* _Os 10 principais cenários por operações no mês passado._
* _Quantas operações o aplicativo Salesforce usou no terceiro trimestre?_

## Ferramentas de conexão e de chave

Essas ferramentas retornam somente metadados. Eles não retornam credenciais, tokens ou valores secretos.

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Pesquisar conexões | `fusion_connections_search` | Ler | Lista conexões. Filtrar por `name`, `accountName`, `accountType`, `expire`, `teamId`, `scopesCount`, `editable`, `environmentType`, `authenticationType`. |
| Obter conexão | `fusion_connections_get` | Ler | Retorna detalhes de uma única conexão. |
| Pesquisar chaves | `fusion_keys_search` | Ler | Lista as chaves. Filtrar por `name`, `typeName`, `teamId`. |
| Obter chave | `fusion_keys_get` | Ler | Retorna detalhes de uma única chave. |

Exemplo de prompts:

* _Quais conexões expiram nos próximos 30 dias e quais cenários as usam?_

## Ferramentas do Webhook

### Webhooks

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Listar webhooks | `fusion_hooks_list` | Ler | Lista os webhooks (ganchos). Filtrar por `name`, `teamId`, `type`, `enabled`, `gone`, `typeName`, `scenarioId`, `priority`, `detached` e muito mais. |
| Obter webhook | `fusion_hooks_get` | Ler | Retorna a configuração de um webhook, a associação do proprietário e as referências externas. |
| Localizar webhooks dependentes | `fusion_hooks_dependents` | Ler | Localiza webhooks que fazem referência a uma determinada conexão. |

### Fila do Webhook

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | -------- | --- |
| Obter estatísticas da fila | `fusion_queue_stats` | Ler | Retorna o número de eventos na fila, o limite da fila e se o webhook está habilitado. |
| Listar fila | `fusion_queue_list` | Ler | Lista eventos de webhook recebidos aguardando para serem processados. |
| Obter item da fila | `fusion_queue_get` | Ler | Retorna um único evento na fila, incluindo sua carga decodificada. |
| Excluir itens da fila | `fusion_queue_delete` | Gravar | Exclui eventos enfileirados específicos (até 50) ou limpa a fila, excluindo alguns eventos opcionalmente. Os eventos que estão sendo processados não podem ser excluídos. |

Exemplo de prompts:

* _O webhook &quot;Envios de formulário&quot; está fazendo backup?_
* _Mostrar a carga do evento mais antigo na fila._

## Ferramentas de armazenamento e estrutura de dados

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Listar armazenamentos de dados | `fusion_datastores_list` | Ler | Lista os armazenamentos de dados com a contagem, o tamanho e o tamanho máximo do registro. |
| Obter armazenamento de dados | `fusion_datastores_get` | Ler | Retorna os metadados e o uso de um armazenamento de dados, a estrutura de dados vinculada e a configuração de validação estrita. |
| Listar registros de armazenamento de dados | `fusion_data_list` | Ler | Lê registros (chave + dados JSON) de um armazenamento de dados, com paginação de deslocamento. |
| Localizar armazenamentos de dados dependentes | `fusion_datastores_dependents` | Ler | Localiza armazenamentos de dados que usam uma determinada estrutura de dados. |
| Pesquisar estruturas de dados | `fusion_data_structures_search` | Ler | Lista as estruturas de dados. Filtrar por `name`, `strict`, `teamId`. |
| Obter estrutura de dados | `fusion_data_structures_get` | Ler | Retorna uma estrutura de dados, incluindo a especificação de campo completa. |

Exemplo de prompts:

* _Quais armazenamentos de dados estão mais de 80% cheios?_
* _Mostre-me os primeiros 20 registros no repositório de dados do &quot;Mapa do cliente&quot;._

## Ferramentas de registro de atividades

| Ferramenta | Nome | Ação | Descrição |
| --- | --- | --- | --- |
| Listar logs de atividades | `fusion_activity_logs_list` | Ler | Lista os eventos de auditoria da organização (quem fez o quê, para qual entidade e quando). Filtrar por `entity` (por exemplo, `scenario`, `connection`, `webhook`, `data store`, `user`), `action` (por exemplo, `created`, `deleted`, `updated`, `transferred ownership`), usuário, equipe e carimbo de data/hora. |
| Exportar logs de atividades | `fusion_activity_logs_export` | Ler | Exporta logs de atividades como CSV ou XLSX, usando os mesmos filtros. |

Exemplo de prompts:

* _Quem excluiu cenários nos últimos 7 dias?_
* _Exportar todas as alterações de conexão deste trimestre para o Excel._

## Colaborador

Todas as ferramentas deste artigo estão disponíveis no Co-worker, independente e no painel direito do Fusion, sujeitas às mesmas configurações de Leitura/Gravação e suas permissões.

## Como as ferramentas são atualizadas

Quando o Adobe lança uma nova versão do servidor Fusion MCP, os agentes conectados selecionam automaticamente o conjunto de ferramentas atualizado. Você não precisa se reconectar.

