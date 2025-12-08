---
title: Glossário do Adobe Workfront Fusion
description: O glossário a seguir explica alguns termos comuns no Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 7f098ec2-8594-4e5d-9ce7-d1738a05f9a6
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: ht
source-wordcount: '924'
ht-degree: 100%

---

# Glossário do Adobe Workfront Fusion

O glossário a seguir explica alguns termos comuns no Adobe Workfront Fusion.


<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Ação</p> </td> 
   <td>Um módulo que permite executar uma ação, como ler ou gravar dados de ou em um aplicativo ou serviço selecionado.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Agregador</p> </td> 
   <td> <p>Um tipo de módulo que mescla vários pacotes (várias coleções de dados) em um único pacote. </p><p>Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/aggregator-module.md" class="MCXref xref">Módulo Agregador</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API</td> 
   <td>As APIs (Application Programming Interfaces, interfaces de programação de aplicativos) são uma maneira de aplicativos e serviços se comunicarem entre si. O Fusion usa APIs para se comunicar com o aplicativo ao qual você está se conectando. Cada aplicativo tem uma API separada. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chave de API</td> 
   <td>Um código exclusivo que identifica o usuário, o desenvolvedor ou o programa que está chamando a API de um software, usado para autenticação. Como os módulos do Fusion funcionam conectando APIs, as chaves de API às vezes são necessárias. As chaves de API são distribuídas pelo aplicativo que precisa delas. Por exemplo, se você precisar de uma chave de API para conectar o Fusion ao Adobe Lightroom, solicite-a por meio da conta do Adobe Lightroom.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aplicativo ou serviço</td> 
   <td> <p>Um aplicativo de software. O Fusion pode se conectar à maioria dos aplicativos, mesmo que não tenha um conector dedicado para esse aplicativo.</p> <p>Um aplicativo também pode ser uma função especial que manipula dados, como um iterador ou agregador. </p> <p>Um serviço é uma fonte de dados que pode incluir uma API da Web, uma página da Web, diferentes tipos de servidores (FTP, SMTP, IMAP) e assim por diante. </p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Pacote</p> </td> 
   <td> <p>Um pacote é uma unidade básica de dados retornada ou recebida por módulos. Por exemplo, um módulo Pesquisa que retorna três registros resulta em três pacotes de dados, um para cada registro. Um pacote consiste em itens.</p> </td> 
  </tr> 
  <tr>
   <td role="rowheader"> <p>Conexão</p> </td> 
   <td> <p>Uma conexão representa um conjunto de credenciais para se conectar a determinado serviço. Você pode configurar conexões dentro de qualquer módulo e, em seguida, pode usar essa conexão em qualquer outro módulo. Cada módulo deve ter uma conexão selecionada, para que o Fusion possa usar essas credenciais para acessar as informações de que o módulo precisa. </p><p>Para obter mais informações, consulte <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md" class="MCXref xref">Visão geral de conexão</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Conector</td> 
   <td>Um conector é o conjunto de módulos de determinado aplicativo. O Workfront Fusion oferece conectores para muitos aplicativos de trabalho comuns, como Workfront, Salesforce e Jira.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ciclo</p> </td> 
   <td> <p>Um ciclo consiste em duas fases da execução do cenário: operação e confirmação. O cenário pode consistir em um ou mais ciclos. Para obter informações mais detalhadas, consulte <a href="/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md" class="MCXref xref">Execução do cenário, ciclos e fases</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Armazenamento de dados</p> </td> 
   <td> <p>Um armazenamento de dados armazena dados de cenários ou permite transferir dados entre cenários individuais ou execuções de cenário. </p><p>Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/map-data/data-stores.md" class="MCXref xref">Armazenamentos de dados</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Filtro</p> </td> 
   <td> <p> Um filtro pode ser aplicado entre dois módulos e permite que você trabalhe somente com os pacotes que atendam a critérios específicos. Há vários filtros diferentes que podem ser aplicados. </p><p>Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md" class="MCXref xref">Adicionar filtro a um cenário</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID </p> </td> 
   <td> <p>Um nome usado para identificar exclusivamente um pacote. Uma ID geralmente é usada para diferenciar um pacote que deve ser atualizado ou excluído de determinado serviço. As IDs podem ser mapeadas da saída de um módulo anterior.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Itens</p> </td> 
   <td> <p>Uma parte de um pacote. Os pacotes podem consistir em vários itens. Há vários tipos diferentes de itens: texto, número, booliano (sim/não), data, hora, buffer (dados binários), coleções, menu de seleção, matriz e validação.</p><p> Para obter mais informações, consulte <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipos de dados de item</a>.</p> </td> 
  </tr>
  <tr> 
   <td role="rowheader"> <p>Iterador</p> </td> 
   <td> <p>Um tipo de módulo que permite pegar um pacote de dados (uma coleção de dados) e dividir em pacotes separados. Em seguida, esses pacotes podem ser processados individualmente pelos módulos posteriores. </p><p>Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">Módulo [!UICONTROL Iterator]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Módulo</p> </td> 
   <td> <p>Uma única etapa em um cenário que executa uma função, como criar um registro, no aplicativo ou serviço associado.</p> <p>Cada aplicativo ou serviço tem vários módulos que definem como ele responde a uma solicitação.</p>  <p> <img src="assets/module.png"> </p> <p>Para obter mais informações, consulte <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">Visão geral do módulo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Operação</p> </td> 
   <td> <p>Uma tarefa executada por um módulo, como recuperar um registro ou fazer upload de um arquivo.</p><p>Para obter mais informações, consulte <a href="/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md" class="MCXref xref">Operações</a>.</p>
  </tr> 
  <tr> 
   <td role="rowheader">Chaves públicas/privadas</td> 
   <td>As chaves públicas e privadas são usadas para criptografar e descriptografar dados. A chave pública pode ser distribuída e qualquer pessoa com ela pode criptografar dados, mas somente a chave privada pode descriptografá-los. De maneira similar, um usuário com uma chave privada pode criptografar dados que qualquer pessoa com a chave pública pode descriptografar. A criptografia de chave privada garante que os dados vieram do proprietário da chave privada e servem como validação da fonte de dados.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Roteador</p> </td> 
   <td>Um roteador permite duplicar dados ou adicionar novas rotas a um cenário, a fim de redirecionar dados e tratar grupos diferentes de dados separadamente.</p><p> Para obter mais informações, consulte <a href="/help/workfront-fusion/create-scenarios/add-modules/router-module.md" class="MCXref xref">Módulo [!UICONTROL Router]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Cenário</p> </td> 
   <td> <p>Uma série criada pelo usuário de etapas automatizadas, cada uma representada e executada por um módulo. A finalidade de um cenário é mover e manipular dados.</p> <p> <img src="assets/entire-scenario-blank.png" style="width: 350;height: 178;"> </p> <p> Para obter mais informações, consulte <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md" class="MCXref xref">Visão geral do cenário</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Segmento de cenário</p> </td> 
   <td> <p> Um segmento de cenário é uma seção de um cenário que consiste em uma série de módulos que se conectam ao mesmo aplicativo. Os segmentos de cenário geralmente representam um fluxo de trabalho curto no aplicativo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Acionador</p> </td> 
   <td> <p>Um acionador é um tipo de módulo que monitora dados novos e atualizados e inicia o cenário quando determinadas condições configuradas no módulo são aplicadas. Os acionadores podem ser configurados para iniciar um cenário em uma programação (sondagem) ou sempre que ocorrerem alterações de dados (acionador instantâneo ou webhook).</p> <p>Para obter mais informações, consulte <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">Acionadores</a> no artigo Visão geral do módulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Webhook</p> </td> 
   <td> <p>Um tipo especial de acionador que permite executar um cenário imediatamente após a disponibilização de um novo pacote. </p><p>Para obter mais informações, consulte <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Acionadores instantâneos (webhooks)</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
