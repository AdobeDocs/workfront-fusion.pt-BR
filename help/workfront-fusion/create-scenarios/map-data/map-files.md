---
title: Mapear um arquivo entre módulos
description: Alguns módulos têm a capacidade de processar arquivos. Esses módulos podem retornar um arquivo de saída para ser enviado para processamento adicional ou exigir que um arquivo seja passado a eles para processamento. Antes que esses módulos possam trabalhar em conjunto para processar arquivos, eles devem ser mapeados uns para os outros.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# Mapear um arquivo entre módulos

Alguns módulos podem processar arquivos. Esses módulos podem retornar um arquivo de saída para ser enviado para processamento adicional ou exigir que um arquivo seja passado a eles para processamento. Os arquivos podem ser mapeados, de modo que uma saída de arquivo por um módulo possa ser processada por outro.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacote</td> 
   <td> <p>Qualquer</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença</td> 
   <td> <p>Novo: [!UICONTROL Standard]</p><p>Ou</p><p>Atual: [!UICONTROL Work] ou superior</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>[!UICONTROL Select] ou plano do [!UICONTROL Prime] [!DNL Workfront]: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plano: [!DNL Workfront Fusion] está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurações de nível de acesso*</td> 
   <td> 
     <p>Você deve ser um administrador do [!DNL Workfront Fusion] para sua organização.</p>
     <p>Você deve ser um administrador [!DNL Workfront Fusion] para sua equipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Mapear arquivos dos módulos de origem para os módulos de destino

Os módulos podem processar arquivos que exigem duas informações:

* Nome do arquivo
* Conteúdo do arquivo (dados)

Se qualquer módulo anterior produzir um arquivo, você poderá selecionar o módulo de origem, e o nome e os dados do arquivo emitido por esse módulo serão mapeados para o módulo de destino.

Você também pode inserir esse nome e dados manualmente ou mapeá-los de módulos anteriores. Isso pode ser conveniente quando, por exemplo, renomear um arquivo.

>[!NOTE]
>
>Se você precisar processar um arquivo de uma URL, recomendamos usar o módulo `HTTP > Get a File` para baixar o arquivo da URL e, em seguida, mapear o arquivo do módulo `HTTP > Get a File` para o campo do módulo desejado em seu cenário.
>
>![Arquivo de mapa](assets/map-source-file.png)

Para mapear um arquivo:

1. Clique na guia **[!UICONTROL Scenarios]** no painel esquerdo.
1. Selecione o cenário no qual deseja mapear um arquivo.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. No módulo de destino, que é o destino para o qual você está mapeando, localize a área **arquivo do Source**.
1. Para mapear uma saída de arquivo por um módulo anterior, selecione o módulo que produz o arquivo.

   ![Documento de download do Workfront](assets/wf-download-document.png)

1. Para mapear o nome e os dados manualmente, selecione Mapear e, em seguida, insira ou mapeie o nome e os dados do arquivo.

   ![Usar a opção de mapa](assets/use-the-map-option.png)

1. Continue a configurar o módulo ou clique em **OK**.
