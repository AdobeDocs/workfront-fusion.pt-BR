---
title: Módulos JSONata
description: O conector JSONata do Adobe Workfront Fusion fornece um módulo para processar dados no formato JSON, para que o Adobe Workfront Fusion possa trabalhar ainda mais com o conteúdo de dados.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Módulos [!UICONTROL JSONata]

O conector [!UICONTROL JSONata] do Adobe Workfront Fusion permite consultar objetos JSON. Este módulo não requer uma conexão.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront</td> 
   <td> <p>Qualquer pacote de fluxo de trabalho do Adobe Workfront e qualquer pacote de Automação e Integração do Adobe Workfront</p><p>Workfront Ultimate</p><p>Workfront Prime e pacotes Select, com uma compra adicional do Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenças do Adobe Workfront</td> 
   <td> <p>Standard</p><p>Trabalhar ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Se sua organização tiver um pacote Select ou Prime Workfront que não inclua a Automação e Integração do Workfront, ela deverá comprar o Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Módulos JSONata e seus campos

### Avaliar

Esse módulo de ação consulta um objeto JSON e retorna uma matriz.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expressão]</td> 
   <td>Insira a expressão que deseja usar para avaliar o objeto JSON. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dados] </td> 
   <td> Insira o objeto JSON a ser avaliado.  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringify saída] </td> 
   <td> Habilite esta opção para converter a saída em uma string.  </td> 
  </tr> 
  </tbody>
  </table>

>[!BEGINSHADEBOX]

**Exemplo**:

A meta é retornar uma matriz de nomes do seguinte objeto JSON:

```JSON
{
  "people": [
    { "name": "Alice", "age": 30 },
    { "name": "Bob", "age": 25 },
    { "name": "Charlie", "age": 35 }
  ]
}
```

1. No campo de expressão, digite `people.name`.
1. No campo de dados, insira o objeto JSON.

O módulo retorna uma matriz de nomes extraídos do objeto JSON.

>[!ENDSHADEBOX]



### MCP JSONata

Esse módulo de ação gera expressões JSONata analisando os esquemas de entrada e saída especificados. Você fornece os esquemas, que o protocolo de contexto de modelo (MCP) usa para gerar a expressão que transforma a entrada na saída.




<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conexão]</td> 
   <td> <p>Selecione a conexão usada para se conectar ao modelo de idioma grande (LLM) que você deseja usar para este módulo.</p> <p>Atualmente, somente a chave da API Anthropic é compatível.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Esquema de entrada]</td> 
   <td> <p>Insira ou mapeie o schema de entrada a ser usado para esta expressão.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Esquema de saída]</td> 
   <td> <p>Insira ou mapeie o schema de saída a ser usado para esta expressão.</p> </td> 
  </tr> 
 </tbody> 
</table>
