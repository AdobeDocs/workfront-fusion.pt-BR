---
title: Módulos de arquivamento
description: Em um cenário  [!DNL Adobe Workfront Fusion] , é possível conectar um arquivo, como um arquivo compactado, a vários aplicativos e serviços de terceiros. Por exemplo, você pode configurar um cenário que
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# [!UICONTROL Archive] módulos

Em um cenário [!DNL Adobe Workfront Fusion], você pode usar um arquivo morto, como um arquivo zipado, em seu cenário, permitindo que você o use em suas automações ou integrações.

Para obter instruções sobre como criar um cenário, consulte os artigos em [Criar cenários: índice do artigo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Para obter informações sobre módulos, consulte os artigos em [Módulos: índice do artigo](/help/workfront-fusion/references/modules/modules-toc.md).

## [!UICONTROL Archive] módulos e seus campos

Ao configurar módulos do [!UICONTROL Archive], o [!DNL Workfront Fusion] exibe os campos listados abaixo. Junto com esses, campos [!UICONTROL Archive] adicionais podem ser exibidos, dependendo de fatores como seu nível de acesso no aplicativo ou serviço. Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Extract an archive]](#extract-an-archive)
* [[!UICONTROL Create an archive]](#create-an-archive)
* [[!UICONTROL Inflate]](#inflate)
* [[!UICONTROL Deflate]](#deflate)

## [!UICONTROL Extract an archive]

Esse módulo de ação extrai um arquivo identificado de um arquivamento.

O módulo retorna a ID do arquivo e quaisquer campos associados, juntamente com quaisquer campos e valores personalizados que a conexão acessa. Você pode mapear essas informações em módulos subsequentes no cenário.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p> Selecione o arquivo que deseja extrair. Este arquivo pode ser mapeado de um módulo anterior (como o módulo [!DNL Workfront] &gt;[!UICONTROL Download a document]).</p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemplo:** Obtenha o arquivo ZIP da pasta [!DNL Dropbox] definida (por exemplo, Arquivos), extraia-o usando o módulo [!UICONTROL Archive] e envie arquivos extraídos para o endereço de email desejado como anexos com o módulo [!UICONTROL Email] ou [!DNL Gmail].
>
>![Exemplo de Dropbox](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

## [!UICONTROL Create an archive]

Este módulo agregador adiciona os arquivos desejados a um arquivo morto [!UICONTROL ZIP] ou [!UICONTROL TAR].

Ao configurar esse módulo, os campos a seguir são exibidos.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module]</td> 
   <td> <p> Selecione o módulo do qual deseja recuperar os arquivos.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Selecione se deseja adicionar arquivos a um arquivo [!UICONTROL ZIP] ou a um arquivo [!UICONTROL TAR].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Insira um comentário que deseja adicionar ao arquivo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Group by]</td> 
   <td> <p>Defina uma expressão pela qual você deseja agrupar a saída agregada. Esta expressão pode conter um ou mais itens mapeados. Os dados agregados serão, então, separados em grupos usando o valor dessa expressão. Cada grupo gera um pacote separado com uma chave (a expressão avaliada) e um valor (o texto agregado). Você pode usar a chave como um filtro nos módulos subsequentes.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Selecione esta opção para interromper o cenário quando não houver resultados.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Archive name]</td> 
   <td> <p> Insira um nome para o arquivo criado. Não adicione uma extensão.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecione um arquivo de origem de um módulo anterior ou mapeie o nome e os dados do arquivo de origem.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemplo:** Assista a emails de entrada usando o módulo [!DNL Gmail] >[!UICONTROL Watch emails]. Se um email for recebido, seus anexos serão iterados em pacotes individuais e, em seguida, arquivados no arquivo [!DNL ZIP] e salvos na pasta Dropbox definida.
>
>![Exemplo Do Gmail](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

## [!UICONTROL Inflate]

Esse módulo de transformador descompacta dados binários usando um algoritmo de inflação.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Insira ou mapeie os dados que deseja descompactar usando a função inflate.</p> </td> 
  </tr> 
 </tbody> 
</table>

## [!UICONTROL Deflate]

Esse módulo de transformador compacta dados binários usando um algoritmo de deflação.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Insira ou mapeie os dados que deseja compactar usando a função deflate.</p> </td> 
  </tr> 
 </tbody> 
</table>
