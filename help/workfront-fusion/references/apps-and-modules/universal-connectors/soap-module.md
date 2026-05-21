---
title: Módulo SOAP
description: Você pode usar o módulo SOAP para se conectar às APIs do SOAP no Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
TQID: https://experienceleague.adobe.com/MIMXln44-LWfrQf0w-lZXfZJ3020Flty2CgwSC3JI9c
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 647
ht-degree: 27%

---

# Módulo [!UICONTROL SOAP]

Você pode usar o módulo [!UICONTROL SOAP] para se conectar às APIs do [!UICONTROL SOAP] no [!UICONTROL Adobe Workfront Fusion].

## Módulo SOAP e seus campos

O conector do SOAP inclui apenas um módulo, a ação Executar SOAP

### Executar ação do SOAP

Esse módulo de ação executa a ação do SOAP especificada.



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
   <td role="rowheader">Licença do Adobe Workfront Fusion</td> 
   <td>
   <p>Baseado em operação: nenhum requisito de licença do Workfront Fusion</p>
   <p>Baseado em conector (legado): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [Licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Módulo SOAP e seus campos

Ao configurar módulos do SOAP, o Workfront Fusion exibe os campos listados abaixo.  Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Botão de alternância Mapear](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Executar ação do SOAP

Este módulo de ação executa uma ação SOAP, baseada no WSDL especificado por você.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL WSDL]</td> 
   <td> Selecione o WSDL que você deseja que o módulo use. Para criar um WSDL, clique em <b>Adicionar</b> ao lado do campo e preencha os campos. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL cabeçalhos HTTP]</td> 
   <td> Para cada cabeçalho HTTP que você deseja adicionar, clique em <b>Adicionar item</b> e insira o nome e o valor do cabeçalho.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL cabeçalhos SOAP]</td> 
   <td> Para cada cabeçalho do SOAP que você deseja adicionar, clique em <b>Adicionar item</b> e insira o nome, valor, namespace e XMLNS do cabeçalho.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Forçar cabeçalhos SOAP]</td> 
   <td> Habilite essa opção para configurar cabeçalhos para o SOAP 1.2. </td> 
  </tr> 
  </tbody> 
</table>

## Limitações do módulo [!UICONTROL SOAP]

>[!NOTE]
>
>Os redirecionamentos são desativados durante o carregamento WDSL. Esse é um recurso de segurança, mas pode significar que redirecionamentos não verificados serão bloqueados quando o módulo for executado.

O módulo [!UICONTROL SOAP] está atualmente na versão beta e não oferece suporte a:

* Redefinir elementos
* Restrições de dígitos de fração
* Restrições de dígitos totais
* Restrições de espaço em branco
* Várias partes nas mensagens de entrada e saída. Somente mensagens de parte única são suportadas
* Elementos personalizados do esquema XML definidos com a ajuda de esquemas e elementos de codificação do SOAP.

>[!BEGINSHADEBOX]

**Exemplo:**

O seguinte não seria reconhecido corretamente pelo [!UICONTROL Workfront Fusion]:

```
<complexType name="ArrayOfFloat">
   <complexContent>
      <restriction base="soapenc:Array">
         <attribute ref="soapenc:arrayType"
            wsdl:arrayType="xsd:integer[]"/>
      </restriction>
   </complexContent>
</complexType>
```

Este exemplo inclui as referências `soapenc:Array`, `soapenc:arrayType` e `wsdl:arrayType`, que ainda não têm suporte no [!UICONTROL Workfront Fusion].

>[!ENDSHADEBOX]

## Solução alternativa

Se o módulo [!UICONTROL SOAP] se recusar a processar o arquivo WSDL ou lançar vários erros na configuração do módulo, você poderá tentar usar o módulo universal **[!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação]**:

1. No Workfront Fusion, crie um novo cenário.
1. Insira o módulo **[!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação]** no cenário.
1. Abra a configuração do módulo e preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method]</td> 
      <td> <p>[!UICONTROL POST]</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td role="rowheader">[!UICONTROL Tipo de corpo]</td> 
      <td> <p>[!UICONTROL Bruto]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Tipo de conteúdo]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Analisar resposta]</td> 
      <td>[!UICONTROL Habilitado]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![Workaround](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. Abra uma nova janela ou guia do navegador da Web.
1. Cole o URL WSDL na barra de endereços do navegador da Web e busque o arquivo XML.

   A URL WSDL geralmente termina com `?wsdl`, mas não necessariamente, por exemplo `http://voip.ms/api/v1/server.wsdl`.

1. Se o arquivo WSDL não for exibido diretamente no navegador da Web, abra o arquivo baixado em um editor de texto.
1. Pesquisar a marca `<service>` ou `<wsdl:service>`:

   <!--![Service](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. Depois de localizado, copie a URL do atributo `location`.
1. No Workfront Fusion, cole a URL no campo **Solicitar conteúdo** do módulo HTTP.
1. Forneça valores para os parâmetros selecionados substituindo os pontos de interrogação pelos valores reais.

   >[!NOTE]
   >
   > Para obter valores específicos do arquivo WSDL, use um visualizador WSDL online.

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Feche a configuração do módulo clicando em **[!UICONTROL OK]**.
1. Execute o cenário ou módulo.
