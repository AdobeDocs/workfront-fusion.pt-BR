---
title: Módulo SOAP
description: Você pode usar o módulo SOAP para se conectar às APIs do SOAP no Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Módulo [!UICONTROL SOAP]

Você pode usar o módulo [!UICONTROL SOAP] para se conectar às APIs do [!UICONTROL SOAP] no [!UICONTROL Adobe Workfront Fusion].

## Módulo SOAP e seus campos

O conector do SOAP inclui apenas um módulo, a ação Executar SOAP

### Executar ação do SOAP

Esse módulo de ação executa a ação do SOAP especificada.



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

## Módulo SOAP e seus campos

Ao configurar módulos do SOAP, o [!DNL Workfront Fusion] exibe os campos listados abaixo.  Um título em negrito em um módulo indica um campo obrigatório.

Se você vir o botão de mapa acima de um campo ou função, poderá usá-lo para definir variáveis e funções para esse campo. Para obter mais informações, consulte [Mapear informações de um módulo para outro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Alternância de mapa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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

1. Em [!DNL Workfront Fusion], crie um novo cenário.
1. Insira o módulo **[!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação]** no cenário.
1. Abra a configuração do módulo e preencha os seguintes campos:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Método]</td> 
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
1. Em [!DNL Workfront Fusion], cole a URL no campo de URL do módulo HTTP.
1. Abra o [Cliente [!UICONTROL SOAP] do &lbrace;Online](https://wsdlbrowser.com/) em uma nova janela/guia do navegador da Web.
1. Cole o URL do WSDL no campo URL do WSDL.
1. Clique em **[!UICONTROL Procurar]**.
1. Escolha na lista de funções à esquerda, por exemplo `getLanguages`.
1. Copie o conteúdo da área de texto [!UICONTROL Solicitar XML].
1. No [!UICONTROL Workfront Fusion], cole o conteúdo copiado no campo de URL do módulo.
1. Forneça valores para os parâmetros selecionados substituindo os pontos de interrogação pelos valores reais:

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Feche a configuração do módulo clicando em **[!UICONTROL OK]**.
1. Execute o cenário ou módulo.
