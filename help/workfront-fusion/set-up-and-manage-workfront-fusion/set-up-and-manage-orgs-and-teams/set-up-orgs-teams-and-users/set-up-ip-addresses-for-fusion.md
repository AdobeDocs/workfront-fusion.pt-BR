---
title: Configurar endereços IP do Fusion no arquivo de inclui na lista de permissões da sua organização
description: O Fusion usa endereços IP e domínios específicos para comunicação na Web. Eles devem ser adicionados ao arquivo de inclui na lista de permissões da sua organização antes de você poder usar o Workfront na organização.
author: Becky
feature: Workfront Fusion
exl-id: 406dd45c-0863-4270-a80e-c1c115e0b367
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Configurar endereços IP do Fusion no arquivo de inclui na lista de permissões da sua organização

Como o Adobe Workfront Fusion se comunica com a rede da sua organização, o firewall da organização deve ser configurado para permitir essa comunicação. Os firewalls são medidas de segurança altamente eficazes que funcionam ao separar a rede de uma organização da Internet. Eles garantem que somente os dados e o tráfego de rede selecionados possam ser movidos para dentro ou para fora da rede da organização. O firewall permite ou bloqueia dados com base no site que está enviando ou recebendo os dados. Como administrador do Fusion, você deve garantir que os dados enviados para o Fusion ou provenientes dele possam passar pelo firewall da sua organização.

Isso é feito por meio de uma inclui na lista de permissões, que é essencialmente uma &quot;lista&quot; de sites que têm &quot;permissão&quot; para enviar ou receber dados por meio do firewall. Os sites podem ser identificados de uma das duas formas a seguir:

* **Endereço IP**: uma série de números como 52.31.132.175
* **Domínio**: parte de uma URL, como `thisdomain` em `www.thisdomain.com`

O Fusion usa endereços IP e domínios específicos para comunicação na Web. Eles devem ser adicionados ao arquivo de inclui na lista de permissões da sua organização antes de você poder usar o Workfront na organização.

Geralmente, uma inclui na lista de permissões é configurada por um administrador de rede. Trabalhe com o administrador de rede de sua organização para garantir que o firewall permita esses endereços IP. Se você não souber quem é o administrador da rede, o departamento de TI da sua organização poderá orientá-lo na direção certa.

>[!IMPORTANT]
>
>Como administrador do Fusion, você deve garantir que esses endereços IP e domínios sejam adicionados ao incluo na lista de permissões da sua organização. Isso é verdade mesmo se você não adicioná-los você mesmo. O Fusion não pode configurar o arquivo de inclui na lista de permissões da sua organização.

Você pode adicionar todos os domínios e endereços IP do Fusion ao seu incluo na lista de permissões do ou localizar o cluster do Fusion e adicionar apenas os domínios e endereços IP desse cluster.

## Adicionar todos os domínios e endereços IP do Fusion

Adicione os seguintes endereços IP ao incluo na lista de permissões:

* 52.30.133.50
* 54.220.93.204
* 34.254.76.122
* 54.244.142.219
* 52.39.217.230
* 44.241.82.96
* 100.20.126.137
* 34.223.32.4
* 52.39.176.220
* 20.36.133.48/28
* 20.81.156.240/28
* 172.172.84.48/28

Incluir na lista de permissões Além disso, se a sua organização usar filtragem de rede de saída, adicione o seguinte domínio ao seu arquivo de pesquisa para permitir que o sistema acesse o Workfront Fusion.

* hook.app.workfrontfusion.com
* hook.app-eu.workfrontfusion.com
* hook.app-az.workfrontfusion.com

## Adicionar domínios e endereços IP do Fusion somente para o cluster

### Identificar o data center

Os endereços IP variam de acordo com o local onde seus dados são armazenados.

Se você acessar o Fusion por meio de um URL, poderá examinar o URL para localizar seu data center.

| URL | Data center |
| --- | --- |
| `https://app.workfrontfusion.com` | Data center dos EUA |
| `https://app-eu.workfrontfusion.com` | Data center da UE |
| `https://app-az.workfrontfusion.com` | Cluster do Azure |

Se você acessar o Fusion por meio do `experience.adobe.com`, poderá verificar a guia Rede no navegador para identificar o data center.

| URL | Data center |
| --- | --- |
| Chamadas para `https://fusion.adobe.com` | Data center dos EUA |
| Chamadas para `https://eu.fusion.adobe.com` | Data center da UE |
| Chamadas para `https://az.fusion.adobe.com` | Cluster do Azure |

### Adicione endereços IP e domínios para o seu data center

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront EU Datacenter</td> 
   <td> 
    <ul> 
     <li>52.30.133.50</li> 
     <li>54.220.93.204</li> 
     <li>34 254 76 122</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront US Datacenter</p> </td> 
   <td> 
    <ul> 
     <li>54 244 142 219</li> 
     <li>52.39.217.230</li> 
     <li>44 241 82 96</li>
     <li>100.20.126.137</li>
     <li>34.223.32.4</li>
     <li>52.39.176.220</li>
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion no cluster do Microsoft Azure</td> 
   <td> 
    <ul> 
     <li>20.36.133.48/28</li> 
     <li>20.81.156.240/28</li> 
     <li>172.172.84.48/28</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Incluir na lista de permissões Além disso, se a sua organização usar filtragem de rede de saída, adicione o seguinte domínio ao seu arquivo de pesquisa para permitir que o sistema acesse o Workfront Fusion. Eles são usados para webhooks

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront EU Datacenter</td> 
   <td> <p> hook.app-eu.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront US Datacenter</p> </td> 
   <td> <p>hook.app.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront Fusion no cluster do Microsoft Azure</p> </td> 
   <td> <p>hook.app-az.workfrontfusion.com </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Filtragem de rede de saída incomum. Consulte o administrador da rede para verificar se é necessário atualizar a inclui na lista de permissões do para acomodá-la.
