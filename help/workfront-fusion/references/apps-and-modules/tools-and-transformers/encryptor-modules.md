---
title: Criptografador
description: Os módulos do Adobe Workfront Fusion Encryptor permitem criptografar quaisquer dados de texto. Atualmente, eles suportam criptografia de mensagens via AES256 e PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 0%

---

# Criptografador

Os módulos [!DNL Adobe Workfront Fusion] [!UICONTROL Criptografador] permitem criptografar quaisquer dados de texto. Atualmente, eles oferecem suporte à criptografia de mensagens via AES256 e PGP ([!UICONTROL OpenPGP]).

Esses módulos exigem alguma familiaridade com processos de criptografia.

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
   <p>Nenhum requisito de licença do Workfront Fusion</p>
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

## Criptografia e descriptografia de mensagens usando PGP

Ao criptografar e descriptografar via PGP, é necessário usar um chaveiro e criar uma chave privada ou pública (ou ambas).

Para obter mais informações sobre chaves públicas e privadas, consulte o [glossário do Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).

Para obter mais informações sobre chaves, consulte [Chaves](/help/workfront-fusion/references/modules/keys.md).

## [!UICONTROL Módulos &lbrace;Encryptor] e seus campos

Ao configurar os módulos do [!UICONTROL Encryptor], os campos a seguir são exibidos. Um título em negrito em um módulo indica um campo obrigatório.

### Descriptografia AES (avançada)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chave]</td>
        <td>Selecione a chave que deseja que o módulo use. Para criar uma chave, clique em <b>Adicionar</b> e insira o nome, a chave e o tipo de codificação da chave.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td>Selecione se deseja que o módulo use criptografia de 128 ou 256 bits.</td>
    </tr>
    <tr>
        <td>Codificação de entrada</td>
        <td>Selecione o tipo de codificação de entrada que deseja usar:
        <ul>
        <li>Binário</li>
        <li>Base 64</li>
        <li>Hexadecimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dados</td>
        <td>Insira ou mapeie os dados que deseja descriptografar.</td>
    </tr>
    <tr>
        <td>Codificação de saída</td>
        <td>Selecione o tipo de codificação de saída que deseja usar:
        <ul>
        <li>ASCII</li>
        <li>Binário</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Algoritmo de codificação</td>
        <td>Selecione o algoritmo de criptografia que deseja usar:
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codificação de vetor de inicialização</td>
        <td>Selecione a codificação de vetor de inicialização que deseja usar:
        <ul>
        <li>UTF-8</li>
        <li>Binário</li>
        <li>Base 64</li>
        <li>Hexadecimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codificação de tag de autenticação</td>
        <td>Selecione a codificação de tag de autenticação que deseja usar:
        <ul>
        <li>UTF-8</li>
        <li>Binário</li>
        <li>Base 64</li>
        <li>Hexadecimal</li>
        </ul>
        </td>
    </tr>
</table>

### Descriptografia AES (simples)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chave]</td>
        <td>Selecione a chave que deseja que o módulo use. Para criar uma chave, clique em <b>Adicionar</b> e insira o nome, a chave e o tipo de codificação da chave.</td>
    </tr>
   <tr>
        <td>Codificação de entrada</td>
        <td>Selecione o tipo de codificação de entrada que deseja usar:
        <ul>
        <li>Binário</li>
        <li>Base 64</li>
        <li>Hexadecimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dados</td>
        <td>Insira ou mapeie os dados que deseja descriptografar.</td>
    </tr>
    <tr>
        <td>Codificação de saída</td>
        <td>Selecione o tipo de codificação de saída que deseja usar:
        <ul>
        <li>ASCII</li>
        <li>Binário</li>
        <li>UTF-8</li>
        </ul>
        </td>
     </tr>
    <tr>
        <td>Chave secreta</td>
        <td>Insira ou mapeie a chave secreta que deseja usar.</td>
    </tr>
</table>

### Criptografia AES (avançada)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chave]</td>
        <td>Selecione a chave que deseja que o módulo use. Para criar uma chave, clique em <b>Adicionar</b> e insira o nome, a chave e o tipo de codificação da chave.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td>Selecione se deseja que o módulo use criptografia de 128 ou 256 bits.</td>
    </tr>
    <tr>
        <td>Codificação de entrada</td>
        <td>Selecione o tipo de codificação de entrada que deseja usar:
        <ul>
        <li>Binário</li>
        <li>ASCII</li>
        <li>Hexadecimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dados</td>
        <td>Insira ou mapeie os dados que deseja criptografar.</td>
    </tr>
    <tr>
        <td>Codificação de saída</td>
        <td>Selecione o tipo de codificação de saída que deseja usar:
        <ul>
        <li>ASCII</li>
        <li>Binário</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Algoritmo de codificação</td>
        <td>Selecione o algoritmo de criptografia que deseja usar:
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codificação de vetor de inicialização</td>
        <td>Selecione a codificação de tag de autenticação que deseja usar:
        <ul>
        <li>UTF-8</li>
        <li>Binário</li>
        <li>Base 64</li>
        <li>Hexadecimal</li>
        </ul>
        </td>
    </tr>
</table>

### Criptografia AES (simples)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chave]</td>
        <td>Selecione a chave que deseja que o módulo use. Para criar uma chave, clique em <b>Adicionar</b> e insira o nome, a chave e o tipo de codificação da chave.</td>
    </tr>
   <tr>
        <td>Codificação de entrada</td>
        <td>Selecione o tipo de codificação de entrada que deseja usar:
        <ul>
        <li>Binário</li>
        <li>ASCII</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dados</td>
        <td>Insira ou mapeie os dados que deseja criptografar.</td>
    </tr>
    <tr>
        <td>Codificação de saída</td>
        <td>Selecione o tipo de codificação de saída que deseja usar:
        <ul>
        <li>Base 64</li>
        <li>Binário</li>
        <li>Hexadecimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Chave secreta</td>
        <td>Insira ou mapeie a chave secreta que deseja usar.</td>
    </tr>
</table>


### Criar assinatura digital

Este módulo permite descriptografar uma mensagem usando chaves públicas e privadas.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chave privada]</td>
        <td>Selecione a chave privada a ser usada para esta assinatura. Para adicionar uma chave privada, clique em <b>Adicionar</b> e insira o nome da chave, o texto da chave e a senha.</td>
    </tr>
    <tr>
        <td>Algoritmo </td>
        <td>Selecione se deseja usar RSA-SHA1 ou RSA-SHA256. </td>
    </tr>
   <tr>
        <td>Codificação de entrada</td>
        <td>Selecione o tipo de codificação de entrada que deseja usar:
        <ul>
        <li>ASCII</li>
        <li>Binário</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codificação de saída</td>
        <td>Selecione o tipo de codificação de saída que deseja usar:
        <ul>
        <li>Base 64</li>
        <li>Hexadecimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dados</td>
        <td>Insira ou mapeie os dados a partir dos quais deseja criar a assinatura.</td>
    </tr>
</table>

### Descriptografar uma mensagem PGP

Este módulo permite descriptografar uma mensagem usando chaves públicas e privadas.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chave privada]</td>
        <td>Selecione a chave privada do destinatário para usar nesta mensagem. Para adicionar uma chave privada, clique em <b>Adicionar</b> e insira o nome da chave, o texto da chave e a senha.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Chave pública]</td>
        <td>Insira a chave pública do remetente. Isso pode autenticar a identidade do remetente.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Mensagem]</td>
        <td>Mapeie a mensagem que deseja descriptografar.</td>
    </tr>
</table>

### Criptografar uma mensagem PGP

Esse módulo permite criptografar uma mensagem usando chaves públicas e privadas.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chave privada]</td>
        <td>Insira a chave privada do remetente. Isso pode autenticar a identidade do remetente.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Chave pública]</td>
        <td>Insira a chave pública do recipient.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Mensagem]</td>
        <td>Informe a mensagem que deseja criptografar.</td>
    </tr>
    </table>
