---
title: Trabalhar com arquivos grandes
description: Atualmente, há suporte para arquivos grandes nos conectores Workfront e HTTP.
author: Becky
feature: Workfront Fusion
exl-id: 6df81943-e70c-42b3-aa44-d82343598a51
source-git-commit: 4422a0d9236c4fe783b3b8d2757a86c91bcca748
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---

# Trabalhar com arquivos grandes

>[!IMPORTANT]
>
>O recurso de arquivos grandes está disponível somente para clientes do Workfront Ultimate e é uma implantação em fases. Todas as organizações do Fusion com um plano Workfront Ultimate terão um grande recurso de arquivos até janeiro de 2025.

Os recursos aprimorados de transferência de dados agora estão disponíveis no Workfront Fusion, permitindo que os cenários processem arquivos significativamente maiores.

Para lidar com arquivos maiores, seus cenários devem ser atualizados.

>[!NOTE]
>
>Essa funcionalidade está disponível somente para usuários no pacote Ultimate Workfront.

## Conectores compatíveis com arquivos grandes

Na versão inicial, os seguintes conectores são compatíveis com arquivos grandes.

* Workfront > Fazer upload de documento
* Adobe Experience Manager Assets > Fazer upload de documento
* Workfront Proof > Fazer upload de arquivo
* Adobe Authenticator > Fazer uma chamada de API personalizada
* HTTP

Outros conectores serão compatíveis em versões futuras.

## Atualize seus cenários para lidar com arquivos grandes

O módulo Workfront > Carregar documento foi modificado para lidar com arquivos maiores. A versão anterior deste módulo agora exibe `(Legacy)` anexado ao nome do módulo. Na maioria dos casos, o módulo herdado continuará a funcionar.

Se você planeja trabalhar com arquivos maiores, recomendamos substituir o módulo herdado pelo novo módulo Carregar documento. O novo módulo Carregar documento evita tempos limite e outros erros.

![Carregar documento](assets/new-upload-document.png)

## Perguntas frequentes

### Qual é o novo limite de tamanho de arquivo?

Os usuários agora podem processar arquivos que excediam o limite anterior de 1 GB, aumentando a eficiência e a produtividade.  Embora a plataforma possa oferecer suporte a arquivos individuais de até 15 GB para uma única ação (como o upload de um arquivo), há outros fatores que afetam a transferência de dados. O limite de tamanho de arquivo de uma única ação depende do serviço Web ao qual o Fusion se conecta. A transferência de dados é o processamento total de uma única execução. Isso significa que várias ações em uma única execução contribuem para a transferência total de dados.

O Fusion processa arquivos até que o limite de execução de 40 minutos seja atingido. Arquivos grandes podem levar algum tempo para carregar, baixar ou processar em seu cenário do Fusion. Embora não haja limite para o tamanho de arquivo individual, há um limite de 40 minutos no tempo de execução do cenário. Portanto, se arquivos grandes fazem com que a execução demore mais de 40 minutos, o cenário falha. O tempo de execução do cenário também pode ser afetado pelo tamanho do cenário, pela complexidade do módulo e pela velocidade da rede. Portanto, recomendamos que você considere esses aspectos de seus cenários ao usar arquivos grandes.

### Como funciona a nova transferência de arquivos do Fusion?

Quando o Fusion processa arquivos, arquivos maiores são adicionados ao armazenamento persistente (Armazenamento S3 Bucket ou Armazenamento Azure Blob). Quando um módulo Fusion executa uma ação de arquivo, como upload ou download, o Fusion usa o arquivo no armazenamento persistente como origem, em vez da memória ativa.

### Posso trabalhar com arquivos maiores usando execuções incompletas?

Sim, o Fusion suporta execuções incompletas com arquivos maiores. Observe que as execuções incompletas são limitadas em tamanho para uma organização e devem ser gerenciadas ativamente.

### Posso usar arquivos maiores com qualquer conector?

Cada conector Fusion deve ser atualizado para oferecer suporte a arquivos maiores. Os conectores compatíveis incluem Workfront, HTTP e AEM Assets. Os conectores Fusion ainda são limitados pelo tamanho do arquivo aceito pelo serviço da Web. Normalmente, os limites de tamanho de arquivo são incluídos na documentação da API para pontos de acesso de serviço da Web que baixam e carregam arquivos.

### Isso afeta as operações?

Não, o número de operações executadas por um módulo é o mesmo.

### Quando a interface do usuário do Fusion será atualizada para exibir dados de transferência de arquivos?

Estamos trabalhando ativamente em atualizações na interface do usuário do Fusion para transferência de arquivos na página de detalhes de execução do painel e do cenário, com uma versão direcionada para o primeiro trimestre de 2025.

### Quais são algumas maneiras de pensar sobre os novos limites de processamento de arquivos que me ajudarão a projetar cenários?

Projetar um cenário para funcionar dentro do limite de execução de 40 minutos pode parecer complicado. Recomendamos considerar o seguinte ao criar um cenário:

* **Entenda seus requisitos de negócios para o tempo de execução**: o limite do tempo de execução da plataforma Fusion é de 40 minutos, mas espera-se que a maioria das automações do processo de negócios seja executada muito mais rapidamente. Por exemplo, seria esperado que as automações iniciadas pelo usuário com continuidade dependente de resultados fossem bem concluídas abaixo do limite de 40 minutos.
* **Considere o tempo de execução ao criar**: ao criar seu cenário, é essencial entender o tempo de execução do módulo para ações de arquivo individuais, como carregamentos e downloads. Esse conhecimento ajuda a planejar cenários que envolvem várias ações de arquivo.  Para garantir a precisão em seu design, recomendamos arredondar o tempo de execução do módulo para cima para incluir um buffer.
Por exemplo, se o Fusion baixar um documento em 144 segundos (2,4 minutos), você pode prever que uma única execução pode executar ações semelhantes várias vezes. Neste exemplo, a execução do módulo leva 144 segundos e você deve planejar a execução por 3 minutos para o download. Se seus requisitos incluírem um upload e um download, o tempo de execução esperado seria de aproximadamente 6 minutos. Observe que os tempos de execução do Fusion são limitados a 40 minutos.

* **Consolidar ações de arquivo**: o exemplo mais comum de ações de arquivo em um cenário do Fusion é um download e um upload. A maioria dos cenários com apenas essas duas ações será executada em alguns minutos. Quando possível, os designers do Fusion devem restringir seus cenários a um download e um upload.

* **Calcule o tamanho usando o painel de mapeamento**: o Workfront e outros serviços da Web incluem o tamanho de um arquivo na saída do módulo de download. Você pode usar esses dados para filtrar arquivos muito grandes para um upload de módulo ou muito grandes para o tempo de execução do cenário.

* **Isolar ações de arquivo em seu próprio cenário ao trabalhar com vários arquivos**: os designers do Fusion devem considerar isolar ações de arquivo em cenários separados. Por exemplo, um cenário do Fusion acionado por uma nova solicitação do Workfront com vários arquivos anexados pode precisar acomodar até 30 arquivos. Dado que o upload e download de cada arquivo poderia levar até 3 minutos, o processamento de todos os arquivos em uma única execução ultrapassaria o limite de execução de 40 minutos do Fusion. A solução é criar um cenário de ações de arquivo dedicado a lidar com o upload e o download de arquivos individuais. O cenário acionado por solicitação iteraria por meio dos arquivos anexados, chamando o cenário de ações de arquivo para cada arquivo usando o módulo HTTP. Essa abordagem garante que cada arquivo seja processado dentro dos limites de tempo de execução.

<!--
## Connectors that do not support large files

Some Fusion connectors do not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

The following connectors do **not** support large files. 

* Archive
* Box
* Convert
* CSV
* Datastores
* Flow control
* FTP
* JSON
* JWT
* Markdown
* Math
* Microsoft Word templates
* MIME
* Microsoft SQL
* SFTP
* Adobe Acrobat Sign
* SOAP
* Tools
* XML

If a connector is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.-->






<!--## Connectors that support large files

The following connectors support large files.

Workfront
HTTP
Webhooks
Salesforce
Microsoft Email
Workfront Proof
AEM Assets
Email
Slack
Jira
Microsoft Excel
SharePoint
Frame.io
Adobe PDF Services
Marketo
Azure Devops 
Google Email
Jira Server
Google Sheets
Microsoft OneDrive
ServiceNow 
AWS S3
Bynder
OneDrive Business
Adobe Authenticator
Google Drive
Microsoft Dynamics
Google Docs
NetSuite
Airtable
Azure AD
QuickBase 
Adobe Target
Adobe Campaign Classic
Microsoft Calendar
Workfront Planning
HubSpot CRM  
DropBox
Cloud Convert
Egnyte
Adobe Firefly
OpenAI / Chat GPT
Allocadia
Cvent
GitLab 
Google Team Drive
Google Calendar
Workfront SDL Managed Translation
Widen
Workfront Boards
Google Slides
Qualtrics
Microsoft Power BI
Adobe Photoshop
Anaplan
DocuSign 
MariaDB
Adobe Creative Cloud Libraries
Figma
AEM Forms
Datadog
GitHub 
Google Forms
Adobe I/O Events
Trello
Workday
Adobe Journey Optimizer
Adobe Lightroom


If a file is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

-->
