---
title: Adicionar filtro a um cenário
description: Em alguns cenários, é necessário trabalhar somente com pacotes que atendam a critérios específicos. Os filtros permitem selecionar esses pacotes.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 17%

---

# Adicionar filtro a um cenário

Em alguns cenários, é necessário trabalhar somente com pacotes que atendam a critérios específicos. Os filtros permitem selecionar esses pacotes.

Por exemplo, você pode criar um cenário com o acionador [!UICONTROL Registros de observação] para que o Workfront capture apenas tarefas atribuídas a um usuário específico.

Você pode adicionar um filtro entre dois módulos e verificar se os pacotes recebidos dos módulos anteriores atendem a condições de filtro específicas:

* Se isso acontecer, os pacotes serão transmitidos para o próximo módulo no cenário.
* Caso contrário, o processamento dos pacotes será encerrado.

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

Para obter mais detalhes sobre as informações desta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Pré-requisitos

Você deve adicionar ambos os módulos a um cenário antes de poder adicionar um filtro entre eles.

## Adicione um filtro entre dois módulos:

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário ao qual deseja adicionar um filtro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no ícone de chave inglesa ![Ícone de chave inglesa](assets/wrench-icon.png) entre os módulos aos quais deseja adicionar um filtro e selecione **Configurar um filtro**.
1. Na caixa que é exibida, digite um **[!UICONTROL Rótulo]** para o filtro.
1. Defina o filtro **[!UICONTROL Condição]**.

   Insira o campo pelo qual você deseja filtrar no primeiro campo, o operador e (se necessário) o valor ao qual você deseja comparar o campo.

   >[!TIP]
   >
   >É possível inserir valores em campos de filtro no painel de mapeamento
   >Para obter mais informações sobre mapeamento, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Por exemplo, se você deseja que o filtro passe arquivos no Adobe Workfront terminando em XML, digite **[!UICONTROL Nome do arquivo]** na primeira caixa e .**[!UICONTROL xml]** na segunda caixa. No menu suspenso entre elas, você selecionaria **[!UICONTROL Termina com (sem distinção entre maiúsculas e minúsculas)]**. Esse filtro se aplicaria aos pacotes recebidos do primeiro módulo (Workfront). Somente pacotes contendo arquivos XML passariam para o módulo seguinte.

   ![Configurar um filtro](assets/set-up-filter-box.png)

1. Clique em **[!DNL OK]**.

## Copiar um filtro

Atualmente, o editor de cenários inclui um recurso para copiar um filtro.

>[!NOTE]
>
>Se você copiar os módulos em ambos os lados do filtro, o filtro também será copiado.
>
>Para obter mais informações sobre como copiar módulos, consulte [Copiar módulos ou cenários no Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

Para copiar um filtro sem copiar módulos, é possível usar a Ferramenta de Desenvolvimento Fusion

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário ao qual deseja adicionar um filtro.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Abra o Fusion DevTool clicando no ícone DevTool ![ícone DevTool](assets/debugger-icon.png) próximo à parte inferior da tela.

   Se você não vir o ícone DevTool, consulte [Depurar um cenário](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) para obter instruções sobre como abrir a DevTool.

1. Clique no ícone **[!UICONTROL Ferramentas]** ![Ferramentas de Desenvolvimento](assets/devtools-tools-icon.png) na barra lateral esquerda.

1. Clique em **[!UICONTROL Copiar Filtro]** e configure a ferramenta **[!UICONTROL Copiar Filtro]** no painel direito:

   1. Defina o **[!UICONTROL Módulo Source]** como o módulo diretamente após o filtro que você deseja copiar.
   1. Defina o **[!UICONTROL Módulo de Destino]** como o módulo após o qual você deseja colocar o filtro.

1. Clique em **[!UICONTROL Executar]**.
