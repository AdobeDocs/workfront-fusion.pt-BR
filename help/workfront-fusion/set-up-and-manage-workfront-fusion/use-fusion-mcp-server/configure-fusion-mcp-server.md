---
title: Configurar o servidor MCP do Adobe Workfront Fusion
description: Conecte o Adobe Workfront Fusion a uma plataforma de agente de IA compatível com MCP ou ao Co-worker (independente ou no painel direito do Fusion).
source-git-commit: d5861015b3bb0e9c176fcf4fd71db426671764dd
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 7%
---

# Configurar o servidor MCP do Adobe Workfront Fusion

O servidor MCP do Adobe Workfront Fusion permite trabalhar com os cenários, as execuções, as conexões, os webhooks, os armazenamentos de dados e muito mais da sua organização do Fusion, por meio de conversações em linguagem natural em uma plataforma de agente de IA compatível.

Para obter uma lista de ferramentas disponíveis no servidor MCP do Adobe Workfront Fusion, consulte [Ferramentas de servidor MCP do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md).

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

## Pré-requisitos

Antes de conectar o Fusion a uma plataforma de agente de IA, é necessário:

* Ter uma licença ativa do Adobe Workfront Fusion e acesso a pelo menos uma organização do Fusion.
* Ter uma função de usuário e funções de equipe do Fusion que concedem acesso aos dados com os quais você deseja trabalhar.
* Faça logon com uma Adobe ID (Adobe Identity Management System, IMS).
* Ter acesso a uma plataforma de agente de IA compatível com MCP ou a um colaborador.

## Aplicativos MCP compatíveis

O servidor Fusion MCP funciona com os seguintes aplicativos.

**Aplicativos de chat**

* Claude Antrópico
* OpenAI ChatGPT
* Microsoft 365 Copilot

**Ferramentas para desenvolvedores**

* Código Claude Antrópico
* Cursor
* GitHub Copilot
* Código VS
* OpenAI Codex
* Inspetor de MCP, mcp-remoto e outras ferramentas que usam um retorno de chamada local

**Plataformas de automação e IA**

* Adobe Workfront Fusion
* Pesquisa com IA Google Vertex
* Glean
* Writer AI Studio
* Postman

### Limitações

* Somente os aplicativos listados nesta seção podem se conectar ao servidor do Fusion MCP.
* Aplicativos da área de trabalho e interfaces de linha de comando (CLIs) funcionam se receberem o retorno de chamada de entrada em seu próprio computador (`localhost`).
* Não é possível adicionar seus próprios aplicativos. Para solicitar suporte para um novo aplicativo, contate a equipe do Fusion em [fusiondev@adobe.com](mailto:fusiondev@adobe.com).

<!-- BECKY CHECK ME: Other parts of this article might conflict with these limitations. See the comments in the important note below, in the section Connect Fusion to a custom MCP solution, and in the troubleshooting table. -->

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
>Se você usar uma plataforma compatível com MCP diferente, siga a documentação dessa plataforma para adicionar um servidor MCP personalizado. Quando for solicitado o URL do servidor MCP, insira:
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## Usar Fusão com Colaborador

O colega é o agente de IA da Adobe. O Fusion é integrado ao Coworker, de modo que você não precisa inserir um URL MCP ou registrar um aplicativo OAuth. Você pode usar o Colaborador com o Fusion em dois lugares:

* Colaborador (independente): trabalhe com o Fusion junto com seus outros aplicativos da Adobe.
* Colaborador no painel direito do Fusion: abra o Colaborador em um painel dentro da interface do Fusion.

Ambos usam as mesmas ferramentas do Fusion MCP, seu Adobe ID e suas permissões do Fusion. As configurações das ferramentas de Leitura ou Gravação de MCP se aplicam em ambos. Ações destrutivas, como excluir, limpar fila ou substituir, sempre pedem confirmação.

### Usar Fusão no Colaborador

1. Abra o Colaborador. Você pode encontrá-lo em https://experience.adobe.com/#/coworker.
1. Abrir **Personalizações** > **Integrações**
1. Procure ou localize **fusion-mcp** e clique nele.
1. Na janela que abre, clique em **Testar**.
1. Se você tiver acesso a mais de uma organização do Fusion, ela será selecionada automaticamente. Se necessário, você pode solicitar que o Colaborador alterne a organização posteriormente.

### Usar Colaborador no painel direito do Fusion

No Fusion, o Colaborador abre no painel direito

1. Faça logon no Workfront Fusion.
1. Clique no ícone **Colaborador** no painel direito.
1. Faça uma pergunta no painel.

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
1. No menu esquerdo, selecione **Personalizar**.
1. Selecione **Conectores**.
1. Selecione **+**, depois **Adicionar conector personalizado**.
1. Insira um nome (por exemplo, &quot;Workfront Fusion&quot;) e o URL do servidor MCP:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

1. Clique em **Conectar**.
1. Login. Selecione um perfil e uma organização do Fusion.

Para o código Claude, é possível adicionar o servidor a partir da linha de comando:

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## Conectar o Fusion ao ChatGPT

Adicione o Fusion como um servidor MCP personalizado.

### ChatGPT Desktop ou Codex

1. No ChatGPT, abra **Configurações**.
1. Clique em **Plug-ins**.
1. Clique em **Adicionar servidor**.
1. Insira um nome para o servidor.
1. Para o tipo, selecione **HTTP transmissível**.
1. Digite o URL do servidor MCP:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

1. Clique em **Salvar**.
1. Clique em **Autenticar** para o novo servidor e entre.
1. Verifique se o botão ao lado do servidor está ativado.

### ChatGPT na Web

1. Entre no [ChatGPT](https://chatgpt.com).
1. Ir para [https://chatgpt.com/plugins](https://chatgpt.com/plugins). (Talvez seja necessário habilitar o modo de desenvolvedor em **Configurações**; em planos Business/Enterprise, o administrador deve permitir conectores personalizados.)
1. Clique em **+**.
1. Insira um **Nome**.
1. Para **Conexão**, selecione **URL do Servidor** e insira a URL do servidor MCP.
1. Deixe **Autenticação** definido como **OAuth**.
1. Leia a mensagem de risco e marque a caixa de seleção.
1. Clique em **Criar** e entre com.

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
| O Fusion não está listado no Co-worker ou o Co-worker está ausente no painel direito do Fusion. | Recurso não habilitado para sua organização. | Entre em contato com o administrador do Fusion. |

## Perguntas frequentes

### Existe um conector oficial Fusion para Claude ou ChatGPT?

Não neste momento. Use o URL do servidor MCP personalizado. O colega de trabalho (independente e no painel direito do Fusion) tem o Fusion integrado.

### Posso usar mais de uma organização do Fusion?

Sim. Você pode alternar a organização ativa durante uma conversa sem se reconectar.

### O que o agente pode fazer em meu nome?

O agente atua como você, usando suas permissões de função e equipe do Fusion. Ele não pode acessar nada que você não possa acessar no Fusion. Ações destrutivas exigem confirmação explícita.

### O agente vê meus segredos de conexão?

Não. A conexão e as ferramentas de chave retornam metadados (nome, tipo, escopos, expiração), não credenciais ou valores secretos.

