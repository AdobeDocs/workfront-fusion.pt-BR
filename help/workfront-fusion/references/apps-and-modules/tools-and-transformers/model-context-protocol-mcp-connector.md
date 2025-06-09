---
title: Módulos do protocolo de contexto de modelo (MCP)
description: O módulo Protocolo de Contexto de Modelo (MCP) permite processar um prompt de usuário usando MCP.
author: Becky
feature: Workfront Fusion
source-git-commit: d8ae176db714d2b9f041b74a62e8276171745c4b
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---

# Módulos do protocolo de contexto de modelo (MCP)

O protocolo de contexto de modelo (MCP) é uma maneira de conectar com segurança modelos de idioma de IA a outros aplicativos. Você configura servidores MCP, que permitem que o modelo de IA acesse o aplicativo. Em seguida, você pode enviar um prompt para o modelo de IA, que pode retornar informações do aplicativo.

Por exemplo, você pode configurar um servidor MCP para conectar um modelo de IA ao Gmail. Quando você envia o prompt &quot;Me dê meus últimos 5 emails do Gmail&quot;, ele pode acessar seu Gmail e retornar os emails.

O módulo Protocolo de Contexto de Modelo (MCP) permite processar um prompt de usuário usando um modelo de idioma e servidores MCP.

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
   <p>Herdados: Automação e integração do Workfront Fusion for Work </p>
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

## Módulo do protocolo de contexto do modelo e seus campos

Ao configurar o módulo MCP, [!DNL Adobe Workfront Fusion] exibe os campos listados abaixo. Um título em negrito em um módulo indica um campo obrigatório.

### Processar prompt de usuário

Esse módulo de ação processa um prompt, usando o modelo de idioma e os servidores MCP especificados.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chave do modelo de linguagem grande (LLM)]</td> 
   <td> <p>Insira ou mapeie a chave da API do modelo de idioma grande que você deseja usar para este prompt. </p> <p>Atualmente, somente a chave da API Anthropic é compatível.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL servidores MCP]</td> 
   <td> <p>Para cada servidor MCP que você deseja disponibilizar para esse prompt, clique em <b>Adicionar item</b> e insira o nome e o host do servidor. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserir seu prompt]</td> 
   <td> <p>Insira ou mapeie o prompt para o modelo de idioma grande. </p> </td> 
  </tr> 
 </tbody> 
</table>
