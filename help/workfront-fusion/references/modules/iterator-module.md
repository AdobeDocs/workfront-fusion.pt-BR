---
title: Módulo Iterador
description: Um módulo Iterador é um tipo especial de módulo que converte uma matriz em uma série de pacotes. Cada item de matriz é emitido como um pacote separado.
author: Becky
feature: Workfront Fusion
exl-id: 43d39955-3dd7-453d-8eb0-3253a768e114
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%

---

# Módulo [!UICONTROL Iterador]

Um [!UICONTROL Iterador] é um tipo de módulo que converte uma matriz em uma série de conjuntos. Cada item de matriz é emitido como um pacote separado.

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
   <td> Novo: Padrão<p>Ou</p><p>Atual: trabalho ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licença do [!UICONTROL Adobe Workfront Fusion]</td> 
   <td>
   <p>Atual: nenhum requisito de licença do Workfront Fusion.</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo menu:</p> <ul><li>Plano do Workfront para [!UICONTROL Select] ou [!UICONTROL Prime]: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Workfront do [!UICONTROL Ultimate]: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>


Para descobrir seu plano, tipo de licença ou acesso, entre em contato com o administrador do Workfront.

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Configuração do módulo [!UICONTROL Iterador]

O módulo Iterador geral tem um único campo, O campo [!UICONTROL Matriz]. Este campo contém a matriz a ser convertida ou dividida em pacotes separados.

![Configurar iterador](assets/set-up-iterator.jpg)

Outros conectores podem incluir módulos do iterador específicos a esse iterador. Eles contêm um campo do módulo Source, que permite selecionar o módulo que gera a matriz que você deseja iterar.

![Iteradores especializados](assets/specialized-iterators.jpg)

Para obter mais informações, consulte [Configurar um módulo](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

>[!BEGINSHADEBOX]

**Exemplos:**

* O cenário abaixo mostra como recuperar emails com anexos e salvar os anexos como arquivos únicos em uma pasta [!DNL Dropbox] selecionada.

  Os e-mails podem conter uma matriz de anexos. O módulo [!UICONTROL Iterador] após o primeiro módulo permite que o cenário trate cada anexo separadamente. O módulo [!UICONTROL Iterador] divide a matriz de anexos em conjuntos únicos. Cada pacote, com um anexo, é salvo um de cada vez em uma pasta [!DNL Dropbox] selecionada. O campo [!UICONTROL Matriz] no módulo Iterador deve conter a matriz `Attachments`.

  ![Matriz de anexos](assets/attachments-array.jpg)

>[!ENDSHADEBOX]


## Solução de problemas

### Problema: o painel Mapeamento não exibe itens mapeáveis no módulo [!UICONTROL Iterador]

Quando um módulo [!UICONTROL Iterador] não tem informações sobre a estrutura dos itens da matriz, o painel de mapeamento nos módulos após o módulo [!UICONTROL Iterador] exibe apenas dois itens sob o módulo [!UICONTROL Iterador]: `Total number of bundles` e `Bundle order position`.

![O painel de mapeamento não é exibido](assets/mapping-panel-doesnt-display.png)

Isso ocorre porque cada módulo é responsável por fornecer informações sobre os itens gerados, para que esses itens possam ser exibidos corretamente no painel de mapeamento nos módulos subsequentes. No entanto, em alguns casos, vários módulos podem não ser capazes de fornecer essas informações. Por exemplo, os módulos [!UICONTROL JSON] > [!UICONTROL Parse JSON] ou [!UICONTROL Webhooks] > [!UICONTROL Webhook personalizado] com estrutura de Dados ausente não forneceriam as informações.

#### Solução

A solução é executar o cenário manualmente. Isso força o módulo a criar a saída. O Fusion pode aplicar o formato dessa saída em módulos posteriores no cenário.

Por exemplo, um cenário inclui um módulo [!UICONTROL JSON] > [!UICONTROL Parse JSON] sem uma estrutura de dados.

![Analisar JSON](assets/json-parse-json.png)

Um módulo [!UICONTROL Iterador] conectado a este módulo JSON não pode mapear a saída do módulo para o campo Matriz no painel de configuração do módulo [!UICONTROL Iterador].

![Conectar módulo iterador](assets/connect-iterator-module.png)

Para resolver isso:

Iniciar o cenário manualmente no editor de cenários.

>[!NOTE]
>
>Para evitar que todo o cenário seja executado, é possível:
>
>* Desvincule os módulos após o módulo [!UICONTROL JSON] > [!UICONTROL Parse JSON] para impedir que o fluxo continue.
>  >   Ou
>* Clique com o botão direito do mouse no módulo [!UICONTROL JSON] > [!UICONTROL Parse JSON] e escolha **[!UICONTROL Executar somente este módulo]** no menu de contexto para executar somente o módulo [!UICONTROL JSON] > [!UICONTROL Parse JSON].

Depois que o [!UICONTROL JSON] > [!UICONTROL Parse JSON] for executado, ele poderá fornecer informações sobre suas saídas para todos os módulos subsequentes, incluindo o módulo Iterador. O painel de mapeamento na configuração do Iterador exibe os itens:

![O painel de mapeamento exibe itens](assets/mapping-panel-displays-items.png)

além disso, o painel de mapeamento nos módulos conectados após o módulo [!UICONTROL Iterador] exibe os itens contidos na matriz:

![Itens contidos na matriz](assets/items-contained-in-array.png)
