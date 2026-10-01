---
title: Configurar o servidor MCP do Adobe Workfront Fusion
description: Conecte o Adobe Workfront Fusion a uma plataforma de agente de IA compatível com MCP ou ao Co-worker (independente ou no painel direito do Fusion).
source-git-commit: 5f3bd6b7b8837632af245ea2c172205625e4ecba
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 0%
---

# Configurar o servidor MCP do Adobe Workfront Fusion

O servidor MCP do Adobe Workfront Fusion permite trabalhar com os cenários, as execuções, as conexões, os webhooks, os armazenamentos de dados e muito mais da sua organização do Fusion, por meio de conversações em linguagem natural em uma plataforma de agente de IA compatível.

Para obter uma lista de ferramentas disponíveis no servidor MCP do Adobe Workfront Fusion, consulte [Ferramentas de servidor MCP do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md).

## Plataformas de IA compatíveis

O servidor Fusion MCP funciona com qualquer plataforma de IA agêntica que suporte servidores MCP (Protocolo de Contexto de Modelo) e MCP remotos (HTTP de transmissão) com OAuth.

>[!NOTE]
>
> Atualmente, a Adobe não publica um conector do Workfront Fusion no diretório Claude connectors ou no diretório app/plugin do ChatGPT. Para usar o Fusion com Claude, ChatGPT ou Microsoft Copilot, adicione-o como um **servidor MCP personalizado** por URL, conforme descrito neste artigo.

Este artigo aborda as etapas de conexão para:

* [Colaborador do Adobe](#use-fusion-with-coworker): Colaborador como independente e Colaborador no painel direito do Fusion
* [Claude](#connect-fusion-to-claude): conector personalizado
* [ChatGPT](#connect-fusion-to-chatgpt): servidor MCP personalizado
* [Uma solução MCP personalizada](#connect-fusion-to-a-custom-mcp-solution)

>[!IMPORTANT]
>
>Se você usar uma plataforma compatível com MCP diferente, como Gemini, Cursor ou Código VS, siga a documentação dessa plataforma para adicionar um servidor MCP personalizado. Quando for solicitado o URL do servidor MCP, insira:
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## Pré-requisitos

Antes de conectar o Fusion a uma plataforma de agente de IA, é necessário:

* Ter uma licença ativa do Adobe Workfront Fusion e acesso a pelo menos uma organização do Fusion.
* Ter uma função de usuário e funções de equipe do Fusion que concedem acesso aos dados com os quais você deseja trabalhar.
* Faça logon com uma Adobe ID (Adobe Identity Management System, IMS).
* Ter acesso a uma plataforma de agente de IA compatível com MCP ou a um colaborador.

## Usar Fusão com Colaborador

O colega é o agente de IA da Adobe. O Fusion é integrado ao Coworker, de modo que você não precisa inserir um URL MCP ou registrar um aplicativo OAuth. Você pode usar o Colaborador com o Fusion em dois lugares:

* [Colaborador (autônomo)](#use-fusion-in-coworker): trabalhe com o Fusion junto com seus outros aplicativos da Adobe.
* [Colaborador no painel direito do Fusion](#use-coworker-in-the-fusion-right-rail): abra o Colaborador em um painel dentro da interface do Fusion.

Ambos usam as mesmas ferramentas do Fusion MCP, seu Adobe ID e suas permissões do Fusion. As configurações das ferramentas de Leitura ou Gravação de MCP se aplicam em ambos. Ações destrutivas, como excluir, limpar fila ou substituir, sempre pedem confirmação.

### Usar Fusão no Colaborador

1. Abra o Colaborador.
2. Abrir **Personalização** > **Integrações**
3. Localize **fusion-mcp** e clique em **Testar**.
4. Se você tiver acesso a mais de uma organização do Fusion, ela será selecionada automaticamente. Se necessário, você pode solicitar que o Colaborador alterne a organização posteriormente.

### Usar Colaborador no painel direito do Fusion

No Fusion, o Colaborador abre no painel direito

1. Faça logon no Workfront Fusion.
2. Clique no ícone **Colaborador** no painel direito.
3. Faça uma pergunta no painel.

### Exemplo de prompts

* *Mostre-me todos os cenários com falha de execução nas últimas 24 horas.*
* *Lista todos os cenários criados ou excluídos esta semana, classificados por mais recentes primeiro.*
* *O que este cenário está fazendo?*
* *Por que esta execução falhou?*

## Conectar o Fusion ao Claude

Adicione o Fusion como um conector personalizado.

>[!NOTE]
>
> No Claude Team/Enterprise, você deve ser um proprietário para adicionar um conector personalizado. Para obter informações, consulte [Introdução a conectores personalizados usando MCP remoto](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp) na documentação do Claude.

1. Entre em [Claude](https://claude.ai).
2. No menu esquerdo, selecione **Personalizar**.
3. Selecione **Conectores**.
4. Selecione **+**, depois **Adicionar conector personalizado**.
5. Insira um nome (por exemplo, &quot;Workfront Fusion&quot;) e o URL do servidor MCP:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

6. Clique em **Conectar**.
7. Login. Selecione um perfil e uma organização do Fusion.

Para o código Claude, é possível adicionar o servidor a partir da linha de comando:

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## Conectar o Fusion ao ChatGPT

Adicione o Fusion como um servidor MCP personalizado.

### ChatGPT Desktop ou Codex

1. No ChatGPT, abra **Configurações**.
2. Clique em **Plug-ins**.
3. Clique em **Adicionar servidor**.
4. Insira um nome para o servidor.
5. Para o tipo, selecione **HTTP transmissível**.
6. Digite o URL do servidor MCP:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

7. Clique em **Salvar**.
8. Clique em **Autenticar** para o novo servidor e entre.
9. Verifique se o botão ao lado do servidor está ativado.

### ChatGPT na Web

1. Entre no [ChatGPT](https://chatgpt.com).
2. Ir para [https://chatgpt.com/plugins](https://chatgpt.com/plugins). (Talvez seja necessário habilitar o modo de desenvolvedor em **Configurações**; em planos Business/Enterprise, o administrador deve permitir conectores personalizados.)
3. Clique em **+**.
4. Insira um **Nome**.
5. Para **Conexão**, selecione **URL do Servidor** e insira a URL do servidor MCP.
6. Deixe **Autenticação** definido como **OAuth**.
7. Leia a mensagem de risco e marque a caixa de seleção.
8. Clique em **Criar** e entre com.

## Conectar o Fusion a uma solução MCP personalizada

Se você estiver criando seu próprio aplicativo ou agente, conecte-se diretamente ao servidor do Fusion MCP.

## Alternar para uma organização diferente do Fusion

Você não precisa se desconectar para alterar organizações. O servidor Fusion MCP pode alternar a organização ativa em uma sessão:

* _Quais organizações do Fusion eu tenho?_
* _Alternar para a organização 1234._

O agente usa `fusion_orgs_list` e `fusion_orgs_set`. O switch se aplica somente à conversa/sessão atual. Organizações em diferentes zonas do centro de dados (por exemplo, EUA e UE) estão disponíveis por meio do mesmo URL de MCP.

## Solução de problemas de configuração e autenticação

| Problema | Causa provável | Corrigir |
| --- | --- | --- |
| Você não pode encontrar um conector Fusion no diretório Claude ou ChatGPT. | A Adobe não publica um conector de diretório para Fusion. | Adicione o Fusion como um servidor MCP personalizado usando o URL neste artigo. |
| Você não pode adicionar um conector personalizado no Claude ou no ChatGPT. | Seu plano restringe conectores personalizados a proprietários ou administradores. | Peça ao seu administrador do Claude ou do ChatGPT para adicionar o conector ou permitir servidores MCP personalizados. |
| Você conectou o, mas não vê dados ou os dados errados. | A organização incorreta do Fusion está ativa. | Solicite ao agente que liste suas organizações e alterne para a correta. |
| A autenticação falhou ou a conexão parou de funcionar. | Sessão expirada ou erro de conexão. | Desconecte e reconecte o servidor. |
| Você verá uma mensagem informando que o acesso ao MCP está desativado. | O acesso ao MCP está desativado para sua organização Fusion. | Peça ao administrador do Fusion para habilitá-lo. |
| O agente pode ler os cenários, mas não pode criá-los, executá-los, atualizá-los ou excluí-los. | As ferramentas Gravar MCP estão desabilitadas ou a função da equipe não permite. | Peça ao administrador do Fusion para habilitar as ferramentas de gravação ou para conceder a função de equipe necessária. |
| A autenticação personalizada do aplicativo foi rejeitada. | A URL de retorno não está na lista autorizada. | Peça ao administrador para adicionar o URL de retorno de chamada exato. |
| O Fusion não está listado no Co-worker ou o Co-worker está ausente no painel direito do Fusion. | Recurso não habilitado para sua organização. <!-- BECKY CHECK ME: confirm whether this is the correct admin guidance before publishing. --> | Entre em contato com o administrador do Fusion. |

## Perguntas frequentes

### Existe um conector oficial Fusion para Claude ou ChatGPT?

Não neste momento. Use o URL do servidor MCP personalizado. O colega de trabalho (independente e no painel direito do Fusion) tem o Fusion integrado.

### Posso usar mais de uma organização do Fusion?

Sim. Você pode alternar a organização ativa durante uma conversa sem se reconectar.

### O que o agente pode fazer em meu nome?

O agente atua como você, usando suas permissões de função e equipe do Fusion. Ele não pode acessar nada que você não possa acessar no Fusion. Ações destrutivas exigem confirmação explícita.

### O agente vê meus segredos de conexão?

Não. A conexão e as ferramentas de chave retornam metadados (nome, tipo, escopos, expiração), não credenciais ou valores secretos.

