---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Usar modelos para conectar o Adobe Workfront Fusion e o Jira
description: Use esses modelos para automatizar workflows entre o Adobe Workfront Fusion e o Jira.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: c3d1abb898eec6fc84dc1de0fb7799d13d9e3571
workflow-type: tm+mt
source-wordcount: '4171'
ht-degree: 3%

---

# Usar modelos para conectar o Adobe Workfront Fusion e o Jira

O Adobe workfront Fusion oferece modelos que podem automatizar fluxos de trabalho comuns entre o Fusion e o Jira.

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
   <p>Workfront: se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, sua organização deverá comprar o Adobe Workfront Fusion.</p><p>Jira: você deve ter uma licença do Jira Cloud</p>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Configurações de nível de acesso</td> 
   <td> <p>Workfront: permissão para criar usuários, formulários personalizados e campos personalizados.</p> <p>Jira: permissões para criar usuários e campos personalizados, além de modificar telas e webhooks.</td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Pré-requisitos

### Workfront

* Você deve ter uma conta técnica no Adobe Developer Console.

  Para obter informações e instruções, consulte [Configuração da conta técnica](https://developer.adobe.com/cloud-storage/guides/getting-started/technical-account-setup) na documentação da Adobe.
* Você deve aplicar permissões de Administrador do sistema à conta técnica na área Perfis de produto do Adobe Admin Console.

  Para obter informações e instruções, consulte [Criar administradores do sistema no Workfront com a Adobe Admin Console](https://experienceleague.adobe.com/pt-br/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console#create-system-administrators-in-workfront-with-the-adobe-admin-console)

### Jira

Se você estiver usando a autorização OAuth2 para Jira (recomendado), é necessário configurar um aplicativo OAuth2 em [https://developer.atlassian.com/console](https://developer.atlassian.com/console). Para obter informações e instruções, consulte [Criar uma conexão OAuth2 com o Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#create-an-oauth2-connection-to-jira) no artigo Módulos do Jira.

<!--

When configuring this application, you will need the following scopes:

* `read:jira-work` 
* `read:jira-user`
* `write:jira-work`

-->

## Suposições

Esses módulos pressupõem o seguinte:

* O Workfront é a fonte da verdade sobre o projeto geral de campanha de marketing
* A Jira está sendo usada por equipes técnicas, cumprindo parte de um projeto que começou no Workfront.
* Nem todos os usuários do Jira têm acesso ao Workfront ou vice-versa.
* O Workfront e o Jira estão hospedados na nuvem.

## Modelo de dados (mapeamentos de campo)


| Workfront | Jira | Direção | Notas |
|---|---|---|---|
| IdObj | ID do WF * | WF → Jira | Após a criação do problema do Jira |
| Chave Jira * | Chave do problema | Jira → FQ | Após a criação do problema do Jira |
| URL do Jira * | - | Jira → FQ | Link clicável pelo usuário no WF para Jira |
| - | Link WF * | WF → Jira | Link clicável do usuário no Jira para o WF |
| Nome | Resumo | WF → Jira |  |
| Descrição | Descrição | WF → Jira |  |
| Status | Status do WF | WF → Jira | Status do WF |
| Status do Jira * | Status | Jira → FQ | Status do Jira |
| Data de conclusão planejada | Data vencida | WF → Jira | Data de conclusão planejada |
| Notas | Comentários | Jira do WF | Cópia bidirecional |
| Documento | Anexo | WF → Jira | Como anexos na criação de problemas e comentários em novos documentos após a criação. |

\* Esses campos são configurados como parte dessa configuração de integração. Para obter instruções, consulte [Configurar pré-requisitos no Workfront, Jira e Workfront Fusion](/help/workfront-fusion/create-and-manage-templates/use-jira-scenario-templates.md#configure-prerequisites-in-workfront-jira-and-workfront-fusion).

## Configurar pré-requisitos no Workfront, Jira e Workfront Fusion

Para usar os templates de integração do Jira, você deve executar as seguintes configurações:

* [Configurar Jira](#configure-jira)
* [Configurar Workfront](#configure-workfront)
* [Configurar conexões no Workfront Fusion](#configure-connections-in-workfront-fusion)

### Configurar Jira

Para usar esses módulos, é necessário criar o seguinte no Jira:

* Um usuário de integração do sistema
* Três campos personalizados específicos

#### Criar um usuário de integração do sistema no Jira

1. No Jira, crie um usuário específico chamado Usuário de integração do sistema. Esse usuário deve ser usado somente pelo Workfront Fusion e não deve representar um usuário humano. As credenciais deste usuário serão usadas pelas conexões do Workfront Fusion.

#### Criar campos personalizados necessários no Jira

Essa integração espera três campos específicos na conta Jira à qual se conecta. Sem esses campos, a integração não terá sucesso

1. No Jira, vá para **Configurações** (ícone de engrenagem) e selecione **Itens de Trabalho**.
1. Na navegação à esquerda, selecione **Campos personalizados**.
1. No canto superior direito da tela, clique em **Criar campo personalizado.**
1. Crie os seguintes campos:

   | Nome do campo | Tipo de campo |
   |---|---|
   | ID do WF | Campo de texto (linha única) |
   | Status do WF | Campo de texto (linha única) |
   | Link WF | Campo de URL |

   Para obter informações sobre como criar links no Jira, consulte a documentação do Jira sobre criação de campos.
1. Adicione os campos recém-criados à tela associada ao projeto Jira.

   Para obter informações sobre telas no Jira, consulte a documentação do Jira sobre configuração de telas de itens de trabalho.


### Configurar Workfront

Para usar esses módulos, o seguinte deve ser criado no Workfront:

* Um usuário de integração do sistema
* Um formulário personalizado específico

#### Criar um usuário de integração do sistema no Workfront

1. No Workfront, crie um usuário de Integração do sistema. Esse usuário é usado somente pelo Workfront Fusion e não representa um usuário humano. As tarefas atribuídas a esse usuário acionarão o cenário que sincroniza o Workfront com o Jira.

   Para obter instruções, consulte [Adicionar usuários](https://experienceleague.adobe.com/pt-br/docs/workfront/using/administration-and-setup/add-users/create-manage-users/add-users) na documentação do Workfront.

#### Criar um formulário personalizado no Workfront

1. No Workfront, comece criando um formulário personalizado.

   Para obter instruções, consulte [Criar um formulário personalizado](https://experienceleague.adobe.com/pt-br/docs/workfront/using/administration-and-setup/customize/custom-forms/design-a-form/design-a-form) na documentação do Workfront.
1. Nomeie o formulário &quot;**JIRA Fields**&quot;.
1. Incluir os seguintes campos no formulário personalizado:

| Nome do campo | Tipo de campo |
|---|---|
| Chave Jira | Campo de texto de linha única |
| URL do Jira | Campo de texto de linha única |
| Status do Jira | Campo de texto de linha única |

1. Adicione outros campos que você desejará mapear entre Jira e Workfront.
1. Salve o formulário personalizado.

>[!NOTE]
>
>Recomendamos impedir que este formulário seja editado por outros usuários. Você pode fazer isso garantindo que todos os usuários adicionados ao formulário personalizado tenham acesso Somente visualização.
>
>Para obter instruções, consulte [Compartilhar um formulário personalizado](https://experienceleague.adobe.com/pt-br/docs/workfront/using/administration-and-setup/customize/custom-forms/manage-custom-forms/share-access-to-a-custom-form) na documentação do Workfront.

### Configurar conexões no Workfront Fusion

Você deve ter criado os usuários da Integração do sistema no Jira e no Workfront antes de criar conexões.

Ao criar essas conexões, certifique-se de usar as credenciais dos usuários da Integração do sistema criados.

Se desejar, você pode criar essas conexões como parte da configuração dos templates.

* Para obter instruções sobre como criar uma conexão com o Workfront, consulte [Conectar o Workfront ao Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#connect-workfront-to-workfront-fusion) no artigo Módulos do Workfront.
* Para obter instruções sobre como criar uma conexão com o Jira, consulte [Conectar o Jira ao Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) no artigo Módulos do Jira Software.


## Cenários

Oito modelos prontos para uso do Jira ajudam a replicar fluxos de trabalho comuns e acelerar a implementação. Os modelos são totalmente personalizáveis para atender às necessidades específicas dos negócios e podem ser estendidos à medida que os requisitos evoluem.

Não é necessário implementar todos os cenários. A implementação mínima exigiria o Cenário 1, que criaria uma integração de direção única para um problema de JIRA de uma atribuição no Workfront.  Você pode adicionar os cenários adicionais para adicionar robustez e mais interconectividade bidirecional entre o Workfront e o JIRA.  Você também pode criar cenários adicionais para lidar com casos como integração de projeto a épico ou problema de JIRA para problema ou tarefas do Workfront.

Qualquer uso desses modelos ou extensões é considerado configuração personalizada, e recomendamos utilizar o Adobe Professional Services ou um parceiro da Adobe para suporte e implementação.

* **[Workfront para Jira: criar problema de JIRA a partir da tarefa ou atribuição de problema do Workfront](#scenario-1-workfront-to-jira-create-jira-issue-from-workfront-task-or-issue-assignment)**
* [JIRA para o Workfront: JIRA para o Workfront: envie atualizações sobre problemas e comentários de volta para o Workfront a partir de Jira](#scenario-2-jira-to-workfront-send-updates-on-issues-and-comments-back-to-workfront-from-jira)
* [Workfront para Jira: alterações na tarefa do Workfront para problema de JIRA](#scenario-3-workfront-to-jira-changes-to-workfront-task-to-jira-issue)
* [Workfront para Jira: alterações no problema do Workfront para o problema JIRA](#scenario-4-workfront-to-jira-changes-to-workfront-issue-to-jira-issue)
* [Workfront para Jira: criar comentário no JIRA quando uma nova observação sobre uma tarefa ou problema do Workfront](#scenario-5-workfront-to-jira-create-comment-in-jira-when-new-note-on-workfront-task-or-issue)
* [Workfront para Jira: Criar comentário em JIRA em nota excluída na tarefa ou problema do Workfront](#scenario-6-workfront-to-jira-create-comment-in-jira-on-deleted-note-on-workfront-task-or-issue)
* [Workfront para Jira: criar comentário em JIRA quando um novo documento sobre uma tarefa ou problema do Workfront](#scenario-7-workfront-to-jira-create-comment-in-jira-when-new-document-on-workfront-task-or-issue)
* [Workfront para Jira: criar comentário em JIRA em documento excluído na tarefa ou problema do Workfront](#scenario-8-workfront-to-jira-create-comment-in-jira-on-deleted-document-on-workfront-task-or-issue)

### Parâmetros gerais

Ao configurar esses templates, use os seguintes parâmetros gerais:

* **JiraBaseURL**: a URL base da instância Jira. Exemplo: `https://myjira.atlassian.net/`
* **wfBaseURL**: a URL base da instância do Workfront.  Geralmente: `https://<domain>.my.workfront.com` onde `<domain>` é o nome de domínio específico do Workfront.
* **defaultJIRAReporterID**: a ID do usuário no JIRA que cria problemas. (Exemplo: `557058:5aedf933-2312-40bc-b328-0c21314167f0`)
Você pode obter essa ID seguindo um destes procedimentos:
   * Clique no perfil do usuário no JIRA e verifique o URL no navegador.
(Exemplo`https://myjira.atlassian.net/jira/people/<JiraUserID>`)
   * Execute a seguinte chamada de API na instância JIRA para obter a ID da conta específica no JIRA:
     `GET /rest/api/3/user/search?query=email@example.com`


### Cenário 1: Workfront para Jira: criar problema JIRA a partir da tarefa ou atribuição de problema do Workfront

Esse cenário cria um problema do Jira quando uma tarefa ou problema do Workfront é atribuído ao usuário de integração do sistema. O cenário preenche os campos Resumo, Descrição, Data de Vencimento, Status WF e ID WF. Após a criação do problema, esse cenário também faz upload da lista de anexos e do histórico de notas relacionadas à tarefa ou problema original no Workfront.

Se uma tarefa do Workfront for atribuída, o problema no Jira será uma Tarefa. Se um problema do Workfront for atribuído, o problema do Jira será um bug.

+++**Expanda para exibir instruções para configurar o Cenário 1:Workfront para Jira: criar problema JIRA a partir da tarefa do Workfront ou da atribuição de problema**

#### Configurar o módulo do acionador

1. Clique na guia **Modelos** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Procure o modelo usando a barra de pesquisa próxima ao canto superior esquerdo da tela. Você pode pesquisar por nome de modelo ou aplicativos incluídos.
1. Clique no modelo **Workfront para Jira: criar problema de JIRA a partir de tarefa do Workfront ou atribuição de problema**.

   Uma visualização do modelo é aberta, mostrando informações e uma animação do fluxo de dados.
1. No primeiro módulo, comece adicionando um webhook.
1. Selecione a conexão do Workfront criada em [Configurar conexões no Workfront Fusion](#configure-connections-in-workfront-fusion).
1. No campo **Tipo de Registro**, selecione `Assignment`.
1. No campo **Estado**, selecione `New state`.
1. Configure o filtro com as seguintes operações, usando a opção **And**:

   | Campo | Operador | Valor |
   |---|---|---|
   | assignedToID | Igual a | (Insira a Workfront ID do usuário da Integração do sistema) |
   | TaskID | Existe |  |
   | projectID | Igual a | (Insira a ID do projeto ou projetos que você deseja que o webhook assista) |

1. Habilite a opção **Excluir atualizações feitas por esta conexão**.
1. No campo **Origem do Registro**, selecione Somente Novo Registro.
1. Clique em **Salvar** para salvar o webhook e em **OK** para salvar o módulo de acionador.
1. Prossiga para [Conectar módulos de modelo ao Workfront e Jira](#connect-template-modules-to-workfront-and-jira)

#### Conectar módulos de modelo ao Workfront e Jira

1. No módulo Workfront **each**, no campo Conexão, selecione a conexão do Workfront que você criou em [Configurar conexões no Workfront Fusion](#configure-connections-in-workfront-fusion) e clique em **OK** para salvar a conexão com esse módulo.
1. No módulo Jira **each**, no campo Conexão, selecione a conexão do Workfront que você criou em [Configurar conexões no Workfront Fusion](#configure-connections-in-workfront-fusion) e clique em **OK** para salvar a conexão com esse módulo.
1. Continue para [Atualizar o módulo de Parâmetros Gerais](#update-the-general-parameters-module).

#### Atualizar o módulo de Parâmetros Gerais

1. No segundo módulo do modelo (Definir Detalhes do Ambiente), para cada uma das seguintes variáveis, clique em **Adicionar item** e insira o nome e o valor da variável

   | Nome da variável | Valor da variável |
   |---|---|
   | defaultJiraReporterID | Insira a ID do usuário padrão quando o Usuário criador não existe no Jira. Você pode encontrar essa ID de usuário clicando no perfil do usuário e verificando o URL do navegador. Exemplo: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Insira o URL base da conta Jira à qual você está se conectando. |
   | wfBaseURL | Insira o URL de base da conta do Workfront à qual você está se conectando. |

1. Continue para [Mapear campos personalizados no Jira](#map-custom-fields-in-jira)

<!--#### Map custom fields in Jira. 

Awaiting feedback-->

+++

### Cenário 2: JIRA para Workfront: enviar atualizações sobre problemas e comentários de volta para o Workfront a partir de Jira

Esse cenário cria uma tarefa ou problema do Workfront quando um problema é criado no Jira.

>[!NOTE]
>
>Este cenário requer uma conexão OAuth2 para Jira.
>Para usar a autorização OAuth2 para Jira, você deve configurar um aplicativo OAuth2 em [https://developer.atlassian.com/console](https://developer.atlassian.com/console). Para obter informações e instruções, consulte a documentação do Jira.

+++**Expanda para exibir instruções para configurar o Cenário 2: JIRA para o Workfront: enviar atualizações sobre problemas e comentários de volta para o Workfront a partir do Jira**

1. Clique na guia **Modelos** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Procure o modelo usando a barra de pesquisa próxima ao canto superior esquerdo da tela. Você pode pesquisar por nome de modelo ou aplicativos incluídos.
1. Clique na **Parte 2: JIRA para o Workfront: envie atualizações sobre problemas e comentários de volta para o Workfront a partir do modelo Jira**.

   Uma visualização do modelo é aberta, mostrando informações e uma animação do fluxo de dados.
1. No primeiro módulo, comece adicionando um webhook.
1. Selecione uma conexão que use as credenciais para o usuário da Integração do sistema ou crie uma conexão com o Jira com as credenciais da Integração do sistema.

* Para obter instruções sobre como criar uma conexão com o Jira, consulte [Conectar o Jira ao Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) no artigo Módulos do Jira Software.

1. Configurar o filtro de webhook

1. Continue para [Configurar um webhook no Jira](#configure-a-webhook-in-jira)

#### Configurar um webhook no Jira

1. No Jira, crie um webhook.

   Para obter instruções, consulte [Webhooks](https://developer.atlassian.com/server/jira/platform/webhooks/) na documentação do Jira.

1. Ao configurar o webhook, use os seguintes valores:

   * **JQL**: project = &quot;yourProjectName&quot; (onde yourProjectName = o nome do seu projeto JIRA)
   * **Problema**: criado, atualizado
   * **Comentário**: criado, excluído


1. Prossiga para [Conectar módulos de modelo ao Workfront e Jira (Módulo 2)](#connect-template-modules-to-workfront-and-jira-module-2)

#### Conectar módulos de modelo ao Workfront e Jira (Módulo 2)

1. No módulo Workfront **each**, no campo Conexão, selecione a conexão do Workfront que você criou em [Configurar conexões no Workfront Fusion](#configure-connections-in-workfront-fusion) e clique em **OK** para salvar a conexão com esse módulo.
1. No módulo Jira **each**, no campo Conexão, selecione a conexão do Workfront que você criou em [Configurar conexões no Workfront Fusion](#configure-connections-in-workfront-fusion) e clique em **OK** para salvar a conexão com esse módulo.
   <!--#### Map custom fields-->

+++

### Cenário 3: Workfront para Jira: alterações na tarefa do Workfront para problema de JIRA

+++**Expanda para exibir instruções para configurar o Cenário 3: Alterações de WF para Jira (Tarefas)**

1. Clique na guia **Modelos** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Procure o modelo usando a barra de pesquisa próxima ao canto superior esquerdo da tela. Você pode pesquisar por nome de modelo ou aplicativos incluídos.
1. Clique no modelo **Part 3: Workfront to Jira: Changes to Workfront task to JIRA issue**.

   Uma visualização do modelo é aberta, mostrando informações e uma animação do fluxo de dados.

1. Clique no template para entrar no editor.
1. Selecione a organização e a equipe que serão proprietárias deste cenário.
1. No primeiro módulo, comece adicionando um webhook.
1. No campo Conexão, selecione a conexão do Workfront que usa as credenciais de Integração do sistema.
1. No campo **Tipo de Registro**, selecione `Task`.
1. No campo **Estado**, selecione `New state`.
1. Configure o filtro com as seguintes operações, usando a opção **And**:

   | Campo | Operador | Valor |
   |---|---|---|
   | assignedToID | Igual a | Insira a Workfront ID do usuário da Integração do sistema |
   | projectID | Igual a | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |
   | DE: Chave Jira | Existe |  |

1. Habilite a opção **Excluir atualizações feitas por esta conexão**.
1. No campo **Origem do Registro**, selecione `Updated record only`.
1. Clique em **Salvar** para salvar o webhook e em **OK** para salvar o módulo de acionador.
1. No módulo **Definir variáveis JIRA**, defina as variáveis a seguir e clique em **OK** para salvar o módulo.

   | Nome da variável | Valor da variável |
   |---|---|
   | defaultJiraReporterID | Essa é a ID do usuário padrão quando o Usuário criador não existe no Jira. Você pode encontrar essa ID de usuário clicando no perfil do usuário e verificando o URL do navegador. Exemplo: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | O URL base da conta Jira à qual você está se conectando. |
   | wfBaseURL | O URL de base da conta do Workfront à qual você está se conectando. |

1. Em **cada** módulo Workfront, no campo Conexão, selecione a conexão Workfront que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.
1. Em **cada** módulo Jira, no campo Conexão, selecione a conexão Jira que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.

+++

### Cenário 4: Workfront para Jira: alterações no problema do Workfront para o problema JIRA

Esse cenário envia atualizações de problemas do Workfront para problemas de JIRA previamente conectados.

+++**Expanda para exibir instruções de configuração do Cenário 4: Workfront para Jira: alterações no problema do Workfront para problema de JIRA**

1. Clique na guia **Modelos** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Procure o modelo usando a barra de pesquisa próxima ao canto superior esquerdo da tela. Você pode pesquisar por nome de modelo ou aplicativos incluídos.
1. Clique no modelo **Cenário 4: Alterações de WF para Jira (Problemas)**.

   Uma visualização do modelo é aberta, mostrando informações e uma animação do fluxo de dados.

1. Clique no template para entrar no editor.
1. Selecione a organização e a equipe que serão proprietárias deste cenário.
1. No primeiro módulo, comece adicionando um webhook.
1. No campo Conexão, selecione a conexão do Workfront que usa as credenciais de Integração do sistema.
1. No campo **Tipo de Registro**, selecione `Issues`.
1. No campo **Estado**, selecione `New state`.
1. Configure o filtro com as seguintes operações, usando a opção **And**:

   | Campo | Operador | Valor |
   |---|---|---|
   | assignedToID | Igual a | Insira a Workfront ID do usuário da Integração do sistema |
   | projectID | Igual a | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |
   | DE: Chave Jira | Existe |  |

1. Habilite a opção **Excluir atualizações feitas por esta conexão**.
1. No campo **Origem do Registro**, selecione `Updated record only`.
1. Clique em **Salvar** para salvar o webhook e em **OK** para salvar o módulo de acionador.
1. No módulo **Definir variáveis JIRA**, defina as variáveis a seguir e clique em **OK** para salvar o módulo.

   | Nome da variável | Valor da variável |
   |---|---|
   | defaultJiraReporterID | Essa é a ID do usuário padrão quando o Usuário criador não existe no Jira. Você pode encontrar essa ID de usuário clicando no perfil do usuário e verificando o URL do navegador. Exemplo: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | O URL base da conta Jira à qual você está se conectando. |
   | wfBaseURL | O URL de base da conta do Workfront à qual você está se conectando. |

1. Em **cada** módulo Workfront, no campo Conexão, selecione a conexão Workfront que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.
1. Em **cada** módulo Jira, no campo Conexão, selecione a conexão Jira que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.

+++

### Cenário 5: Workfront para Jira: criar comentário no JIRA quando uma nova observação sobre uma tarefa ou problema do Workfront

+++**Expanda para exibir instruções para configurar o Cenário 5: Workfront para Jira: criar comentário em JIRA quando nova observação sobre tarefa ou problema do Workfront**

1. Clique na guia **Modelos** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Procure o modelo usando a barra de pesquisa próxima ao canto superior esquerdo da tela. Você pode pesquisar por nome de modelo ou aplicativos incluídos.
1. Clique no modelo **Cenário 5: WF para Jira Novas notas (Tarefas e Problemas)**.

   Uma visualização do modelo é aberta, mostrando informações e uma animação do fluxo de dados.
1. No primeiro módulo, comece adicionando um webhook.
1. No campo Conexão, selecione a conexão do Workfront que usa as credenciais de Integração do sistema.
1. No campo **Tipo de Registro**, selecione `Note`.
1. No campo **Estado**, selecione `New state`.
1. Configure o filtro com as seguintes operações:

   | Campo | Operador | Valor |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Igual a <br><br>Existe | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |
   | OR |  |  |
   | projectID<br>AND<br>OpTaskID | Igual a <br><br>Existe | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |

1. Habilite a opção **Excluir atualizações feitas por esta conexão**.
1. No campo **Origem do Registro**, selecione `New record only`.
1. Clique em **Salvar** para salvar o webhook e em **OK** para salvar o módulo de acionador.
1. No módulo **Definir variáveis**, defina as variáveis a seguir e clique em **OK** para salvar o módulo.

   | Nome da variável | Valor da variável |
   |---|---|
   | defaultJiraReporterID | Essa é a ID do usuário padrão quando o Usuário criador não existe no Jira. Você pode encontrar essa ID de usuário clicando no perfil do usuário e verificando o URL do navegador. Exemplo: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | O URL base da conta Jira à qual você está se conectando. |
   | wfBaseURL | O URL de base da conta do Workfront à qual você está se conectando. |

1. Em **cada** módulo Workfront, no campo Conexão, selecione a conexão Workfront que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.
1. Em **cada** módulo Jira, no campo Conexão, selecione a conexão Jira que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.

+++

### Cenário 6: Workfront para Jira: criar comentário em JIRA em observação excluída em tarefa ou problema do Workfront

+++**Expanda para exibir instruções para configurar o Cenário 6: Workfront para Jira: criar comentário em JIRA em observação excluída em tarefa ou problema do Workfront**

1. Clique na guia **Modelos** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Procure o modelo usando a barra de pesquisa próxima ao canto superior esquerdo da tela. Você pode pesquisar por nome de modelo ou aplicativos incluídos.
1. Clique no modelo **Cenário 6: WF para Jira Remover notas (Tarefas e Problemas)**.

   Uma visualização do modelo é aberta, mostrando informações e uma animação do fluxo de dados.
1. No primeiro módulo, comece adicionando um webhook.
1. No campo Conexão, selecione a conexão do Workfront que usa as credenciais de Integração do sistema.
1. No campo **Tipo de Registro**, selecione `Note`.
1. No campo **Estado**, selecione `New state`.
1. Configure o filtro com as seguintes operações:

   | Campo | Operador | Valor |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Igual a <br><br>Existe | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |
   | OR |  |  |
   | projectID<br>AND<br>OpTaskID | Igual a <br><br>Existe | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |

1. Habilite a opção **Excluir atualizações feitas por esta conexão**.
1. No campo **Origem do Registro**, selecione `Deleted record only`.
1. Clique em **Salvar** para salvar o webhook e em **OK** para salvar o módulo de acionador.
1. No segundo módulo, defina as variáveis a seguir e clique em **OK** para salvar o módulo.

   | Nome da variável | Valor da variável |
   |---|---|
   | defaultJiraReporterID | Essa é a ID do usuário padrão quando o Usuário criador não existe no Jira. Você pode encontrar essa ID de usuário clicando no perfil do usuário e verificando o URL do navegador. Exemplo: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | O URL base da conta Jira à qual você está se conectando. |
   | wfBaseURL | O URL de base da conta do Workfront à qual você está se conectando. |

1. Em **cada** módulo Workfront, no campo Conexão, selecione a conexão Workfront que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.
1. Em **cada** módulo Jira, no campo Conexão, selecione a conexão Jira que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.

+++

### Cenário 7: Workfront para Jira: criar comentário no JIRA quando um novo documento sobre uma tarefa ou problema do Workfront

+++**Expanda para exibir instruções para configurar o Cenário 7: Workfront para Jira: criar comentário em JIRA quando novo documento na tarefa ou problema do Workfront**

1. Clique na guia **Modelos** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Procure o modelo usando a barra de pesquisa próxima ao canto superior esquerdo da tela. Você pode pesquisar por nome de modelo ou aplicativos incluídos.
1. Clique no modelo **Cenário 7: WF para Jira Novos Anexos (Tarefas e Problemas)**.

   Uma visualização do modelo é aberta, mostrando informações e uma animação do fluxo de dados.
1. No primeiro módulo, comece adicionando um webhook.
1. No campo Conexão, selecione a conexão do Workfront que usa as credenciais de Integração do sistema.
1. No campo **Tipo de Registro**, selecione `Document`.
1. No campo **Estado**, selecione `New state`.
1. Configure o filtro com as seguintes operações, usando a opção **And**:

   | Campo | Operador | Valor |
   |---|---|---|
   | assignedToID | Igual a | Insira a Workfront ID do usuário da Integração do sistema |
   | projectID | Igual a | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |

1. No segundo módulo, defina as variáveis a seguir.

   | Nome da variável | Valor da variável |
   |---|---|
   | defaultJiraReporterID | Essa é a ID do usuário padrão quando o Usuário criador não existe no Jira. Você pode encontrar essa ID de usuário clicando no perfil do usuário e verificando o URL do navegador. Exemplo: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | O URL base da conta Jira à qual você está se conectando. |
   | wfBaseURL | O URL de base da conta do Workfront à qual você está se conectando. |

1. Habilite a opção **Excluir atualizações feitas por esta conexão**.
1. No campo **Origem do Registro**, selecione `New record only`.
1. Clique em **Salvar** para salvar o webhook e em **OK** para salvar o módulo de acionador.
1. Em **cada** módulo Workfront, no campo Conexão, selecione a conexão Workfront que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.
1. Em **cada** módulo Jira, no campo Conexão, selecione a conexão Jira que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.

+++

### Cenário 8: Workfront para Jira: criar comentário em JIRA em documento excluído na tarefa ou problema do Workfront

+++**Expanda para exibir instruções para configurar o Cenário 8: Workfront para Jira: criar comentário em JIRA em documento excluído na tarefa ou problema do Workfront**

1. Clique na guia **Modelos** ![ícone Modelos](assets/templates-icon.png) no painel de navegação esquerdo.
1. Procure o modelo usando a barra de pesquisa próxima ao canto superior esquerdo da tela. Você pode pesquisar por nome de modelo ou aplicativos incluídos.
1. Clique no modelo **Cenário 8: remover anexos de WF para Jira (tarefas e problemas)**.

   Uma visualização do modelo é aberta, mostrando informações e uma animação do fluxo de dados.
1. No primeiro módulo, comece adicionando um webhook.
1. No campo Conexão, selecione a conexão do Workfront que usa as credenciais de Integração do sistema.
1. No campo **Tipo de Registro**, selecione `Document`.
1. No campo **Estado**, selecione `New state`.
1. Configure o filtro com as seguintes operações:

   | Campo | Operador | Valor |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Igual a <br><br>Existe | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |
   | OR |  |  |
   | projectID<br>AND<br>OpTaskID | Igual a <br><br>Existe | Insira a ID do projeto ou projetos que você deseja que o webhook assista. |

1. No módulo **Definir variáveis**, defina as variáveis a seguir.

   | Nome da variável | Valor da variável |
   |---|---|
   | defaultJiraReporterID | Essa é a ID do usuário padrão quando o Usuário criador não existe no Jira. Você pode encontrar essa ID de usuário clicando no perfil do usuário e verificando o URL do navegador. Exemplo: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | O URL base da conta Jira à qual você está se conectando. |
   | wfBaseURL | O URL de base da conta do Workfront à qual você está se conectando. |

1. Habilite a opção **Excluir atualizações feitas por esta conexão**.
1. No campo **Origem do Registro**, selecione `Deleted record only`.
1. Clique em **Salvar** para salvar o webhook e em **OK** para salvar o módulo de acionador.
1. Em **cada** módulo Workfront, no campo Conexão, selecione a conexão Workfront que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.
1. Em **cada** módulo Jira, no campo Conexão, selecione a conexão Jira que usa as credenciais de Integração do Sistema e clique em **OK** para salvar o módulo.


+++

