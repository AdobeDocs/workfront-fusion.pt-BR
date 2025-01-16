---
title: Módulos JWT
description: O aplicativo  [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] fornece um módulo que cria tokens JWT com base no algoritmo fornecido.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Módulo [!UICONTROL JWT]

O aplicativo [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] fornece um módulo que cria tokens JWT com base no algoritmo fornecido.

## Requisitos de acesso

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plano*</td>
  <td> <p>[!UICONTROL Pro] ou superior</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licença*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licença**</td> 
   <td>
   <p>Requisito de licença atual: nenhum requisito de licença [!DNL Workfront Fusion].</p>
   <p>Ou</p>
   <p>Requisito de licença herdada: [!UICONTROL [!DNL Workfront Fusion] para Automação e Integração do Trabalho, [!UICONTROL [!DNL Workfront Fusion] para Automação do Trabalho</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Requisito atual do produto: se você tiver o Plano [!UICONTROL Select] ou [!UICONTROL Prime] [!DNL Adobe Workfront], sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo. [!DNL Workfront Fusion] está incluído no plano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Ou</p>
   <p>Requisito de produto herdado: sua organização deve comprar o [!DNL Adobe Workfront Fusion] e o [!DNL Adobe Workfront] para usar a funcionalidade descrita neste artigo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Para saber que plano, tipo de licença ou acesso você tem, contate o administrador do [!DNL Workfront].

Para obter informações sobre [!DNL Adobe Workfront Fusion] licenças, consulte [[!DNL Adobe Workfront Fusion] licenças](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Informações da API JWT

O conector JWT usa o seguinte:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
   <tr> 
   <td role="rowheader">Tag da API</td> 
   <td>v1.1.5</td> 
  </tr>
 </tbody> 
 </table>

## Módulo JWT e seus campos

### Gerar JWT

Esse módulo gera um JWT com base no algoritmo selecionado.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algorithm]</td> 
   <td> <p>Selecione o algoritmo com o qual deseja gerar o JWT.</p> <ul>
   <li><b>HS256</b>: HMAC usando algoritmo de hash SHA-256</li>
   <li><b>HS384</b>: HMAC usando algoritmo de hash SHA-384</li>
   <li><b>HS512</b>: HMAC usando algoritmo de hash SHA-512</li>
   <li><b>RS256</b>: RSASSA-PKCS1-v1_5 usando algoritmo de hash SHA-256</li>
   <li><b>RS384</b>: RSASSA-PKCS1-v1_5 usando algoritmo de hash SHA-384</li>
   <li><b>RS512</b>: RSASSA-PKCS1-v1_5 usando algoritmo de hash SHA-512</li>
   <li><b>PS256</b>: RSASSA-PSS usando o algoritmo de hash SHA-256 (somente Nó ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b>PS384</b>: RSASSA-PSS usando o algoritmo de hash SHA-384 (somente Nó ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b>PS512</b>: RSASSA-PSS usando o algoritmo de hash SHA-512 (somente Nó ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b>ES256</b>: ECDSA usando curva P-256 e algoritmo de hash SHA-256</li>
   <li><b>ES384</b>: ECDSA usando curva P-384 e algoritmo de hash SHA-384</li>
   <li><b>ES512</b>: ECDSA usando curva P-521 e algoritmo de hash SHA-512</li>
   </ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload] </td> 
   <td> <p>Para cada item de carga que você deseja adicionar, clique em <b>Adicionar item</b> e insira a chave e o valor do item.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Options] </td> 
   <td> <p>Para cada item de opção que você deseja adicionar, clique em <b>Adicionar item</b> e insira a chave e o valor do item.</p> <p>As seguintes chaves estão disponíveis:
   <ul>
   <li><b>algoritmo</b>: (padrão: RS256)</li>
   <li><b>expiresIn</b>: expresso em segundos ou em uma cadeia de caracteres que descreve um período (por exemplo, 2 dias, 10h, 7d). Um valor numérico é interpretado como uma contagem de segundos. Se você usar uma sequência de caracteres, forneça as unidades de tempo (dias, horas etc.); caso contrário, a unidade de milissegundos será usada por padrão (120 é igual a 120 ms).</li>
   <li><b>notBefore</b>: expresso em segundos ou em uma sequência que descreve um período (por exemplo, 2 dias, 10h, 7d). Um valor numérico é interpretado como uma contagem de segundos. Se você usar uma sequência de caracteres, forneça as unidades de tempo (dias, horas etc.); caso contrário, a unidade de milissegundos será usada por padrão (120 é igual a 120 ms).
</li>
   <li><b>público</b></li>
   <li><b>emissor</b></li>
   <li><b>jwtid</b></li>
   <li><b>assunto</b></li>
   <li><b>noTimestamp</b></li>
   <li><b>cabeçalho</b></li>
   <li><b>keyid</b></li>
   <li><b>mutatePayload</b>: se <code>true</code>, a função sign modificará diretamente o objeto de carga. Isso é útil se você precisar de uma referência bruta à carga após a aplicação das declarações a ela, mas antes de ela ser codificada em um token.</li>
   <li><b>allowInsecureKeySizes</b>: Se <code>true</code>, permite que chaves privadas com um módulo abaixo de 2048 sejam usadas para RSA.</li>
   <li><b>allowInvalidAsymmetricKeyTypes</b>: se <code>true</code>, permite chaves assimétricas que não correspondem ao algoritmo especificado. Essa opção destina-se apenas à compatibilidade com versões anteriores e deve ser evitada.</li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>
