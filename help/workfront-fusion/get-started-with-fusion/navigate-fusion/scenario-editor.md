---
title: O editor de cenários
description: O editor de cenários permite criar e editar cenários em uma interface visual.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: 70d715dad3122683b1cf4411c118868c745ca7ff
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 18%

---

# O editor de cenários

O editor de cenários permite criar e editar cenários em uma interface visual.

![Editor de cenários](assets/scenario-editor.jpg)

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

## Abra o editor de cenários e adicione um módulo:

1. Clique em **[!UICONTROL Cenários]** ![Ícone de cenários](assets/scenarios-icon.png) no painel esquerdo.
1. Clique no ícone de ponto de interrogação ![ícone de pergunta](assets/question-mark-full-size.png), localize e clique no aplicativo ou serviço com o qual deseja começar. Para obter informações detalhadas sobre como configurar um módulo, consulte [Configurar um módulo](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

## Ações disponíveis do editor de cenário

### Executar seu cenário

![botão executar cenário](assets/run-your-scenario.png)

| Ação | Detalhes |
|----------|----------|
| Testar o cenário | Verifique se o cenário é executado como esperado antes de ativá-lo. Uma vez ativado, o cenário será executado de acordo com seu cronograma. Se tudo não funcionar conforme o esperado, consulte [Adicionar tratamento de erros](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) para saber como lidar com erros. |

### Agendamento

![painel de agendamento](assets/scheduling-scenario-editor.png)

| Ação | Detalhes |
| ---------- | ---------- |
| Agendar o cenário | Por padrão, um cenário é executado a cada 15 minutos. Você pode alterar isso definindo quando e com que frequência um cenário ativado é executado. Os cenários de fusão podem ser agendados para execução com uma frequência de até 5 minutos. Para obter mais informações, consulte [Agendar um cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

### Controles

Talvez seja necessário clicar no ícone de três pontos na área Controles para exibir alguns desses controles.

![painel de controles](assets/controls-editor-scenario.png)

| Ação | Detalhes |
| ---------- | ---------- |
| Salvar <p>![Ícone Salvar](assets/save-icon.png)</p> | Depois de salvar o cenário, uma nova versão estará disponível no menu de três pontos, caso você precise acessá-lo no futuro. As versões de cenários salvas anteriormente ficam disponíveis somente por 60 dias. |
| Configurações de cenário <p>![Ícone de configurações do cenário](assets/scenario-settings-icon.png)</p> | O painel Configurações de cenário contém configurações avançadas para o cenário. Para obter mais informações sobre as configurações disponíveis, consulte [Definir configurações de cenário](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md). |
| Notas  <p>![Ícone de Notas](assets/notes-icon.png)</p> | Faça observações sobre o cenário. Outros usuários podem exibir essas notas quando estão no cenário. |
| Alinhamento automático <p>![Ícone de alinhamento automático](assets/auto-align-icon.png)</p> | Alinhe automaticamente os módulos no seu cenário. |
| Módulos de pesquisa <p>![Pesquisar módulos](assets/search-modules-icon.png)  </p> | Insira um termo de pesquisa para localizar um módulo e, em seguida, clique nos resultados da pesquisa a serem levados para esse módulo. Você pode pesquisar por nome do módulo, ID, tipo ou aplicativo. |
| Explicar fluxo  <p>![Ícone Explicar Fluxo](assets/explain-flow-icon.png) </p> | Exibir uma animação em que os pontos móveis mostram como os dados fluem pelo cenário. |
| DevTool <p>![Ícone DevTool](assets/devtool-icon.png)</p> | Usando a DevTool, você pode verificar todas as execuções manuais do seu cenário, revisar todas as operações realizadas e ver os detalhes de cada chamada de API realizada. Você pode ver qual módulo, operação ou única resposta causou o erro e usar esse conhecimento para refinar seu cenário. Para obter mais informações, consulte [Depurar um cenário](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Exportar blueprint  <p>![Ícone Exportar Blueprint](assets/export-blueprint-icon.png) </p> | Exportar um blueprint do cenário atual. |
| Importar blueprint  <p>![Ícone Importar Blueprint](assets/import-blueprint-icon.png) </p> | Importe um blueprint de cenário exportado anteriormente. |
| Versão anterior  <p>![Ícone da versão anterior](assets//previous-version-icon.png) </p> | Exibir versões anteriores deste cenário. |

### Ferramentas

![painel de ferramentas](assets/tools-scenario-editor.png)

| Ação | Detalhes |
|---------- | ---------- |
| Controle de fluxo | Defina as configurações para controlar como os dados fluem através dele. Para obter mais informações, [consulte o link necessário]. |
| Ferramentas | A seção de ferramentas contém vários módulos úteis que podem aprimorar seus cenários. Para obter mais informações, [consulte o link necessário]. |
| Analisador de texto | Use a ferramenta Analisador de texto para analisar o texto para uso em outros módulos de cenário. O analisador de Texto não requer uma conexão. Para obter mais informações, [consulte o link necessário]. |

### Favoritos

![Painel Favoritos](assets/favorites-scenario-editor.png)

Você pode usar o ícone Favoritos para adicionar módulos usados com frequência.

