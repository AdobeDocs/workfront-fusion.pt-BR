---
title: Módulos do protocolo de contexto de modelo (MCP)
description: O módulo Protocolo de Contexto de Modelo (MCP) permite processar um prompt de usuário usando MCP.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 748055ad-d305-4513-9a5c-9c970b74a96e
source-git-commit: 44f4fc5de94898e817172a2a83f922776086549f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 18%

---

# Módulo do agente MCP

<!--SET UP REDIRECTS-->

O protocolo de contexto de modelo (MCP) é uma maneira de conectar com segurança modelos de idioma de IA a outros aplicativos. Você configura servidores MCP, que permitem que o modelo de IA acesse o aplicativo. Em seguida, você pode enviar um prompt para o modelo de IA, que pode retornar informações do aplicativo.

Por exemplo, você pode configurar um servidor MCP para conectar um modelo de IA ao Gmail. Quando você envia o prompt &quot;Me dê meus últimos 5 emails do Gmail&quot;, ele pode acessar seu Gmail e retornar os emails.

O módulo Protocolo de Contexto de Modelo (MCP) permite processar um prompt de usuário usando um modelo de idioma e servidores MCP.

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
   <p>Se sua organização tiver um pacote Workfront Select ou Prime, ele não inclui o Workfront Automation and Integration. É necessário comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações contidas nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Pré-requisitos

* Você deve ter configurado todos os servidores MCP aos quais pretende se conectar.
* Você deve ter uma chave LLM para o LLM selecionado (Modelo de idioma grande).

## Módulo do protocolo de contexto do modelo e seus campos

### Processar prompt de usuário

Esse módulo de ação processa um prompt, usando o modelo de idioma e os servidores MCP especificados.

>[!NOTE]
>
>Este módulo deve retornar um objeto. Ele não retorna saída como sequências ou números.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Chave LLM</td> 
   <td> Selecione uma chave LLM existente ou crie uma nova clicando em <b>Adicionar</b> e inserindo as seguintes informações: 
     <ul>
       <li><b>Nome da chave</b>: insira um nome para a nova chave.</li>
       <li><b>LLM</b>: selecione o modelo de idioma grande ao qual esta chave está associada.</li>
       <li><b>Chave</b>: insira ou mapeie sua chave de API para o modelo selecionado.</li>
       <li><b>Modelo</b>: selecione o modelo LLM que a chave usará.</li>
       <li><b>Máximo de Tokens</b>: insira ou mapeie o número máximo de tokens que o LLM pode gerar em sua resposta.<p>Um token geralmente equivale a quatro caracteres, ou 0,75 de uma palavra em inglês. "Olá, mundo" seria igual a dois tokens e "Autenticação" seria igual a um ou dois tokens.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Servidores MCP</td> 
   <td> <p>Para cada servidor MCP ao qual você deseja se conectar, clique em <b>Adicionar</b> e insira as seguintes informações: </p> 
     <ul>
       <li><b>Conexão</b>: selecione a conexão que o Fusion usará para se conectar ao servidor MCP.</li>
       <li><b>Host do Servidor MCP</b>: insira a URL do servidor MCP.</li>
       <li><b>Nome do Servidor MCP</b>: insira ou mapeie um nome para este servidor MCP.</li>
       <li><b>Cabeçalhos</b>: adicione quaisquer cabeçalhos aplicáveis.</li>
       <li><b>Tipo de Servidor MCP</b>: selecione o tipo de servidor.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Insira seu prompt </td> 
   <td> <p>Insira ou mapeie o prompt que deseja processar.</p> </td> 
  </tr> 
 </tbody> 
</table>


