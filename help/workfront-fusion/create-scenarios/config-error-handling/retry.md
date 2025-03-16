---
title: Configurar solução alternativa para o tratamento de erros de nova tentativa
description: Às vezes, é útil executar novamente um módulo com falha se houver uma chance de o motivo da falha ser resolvido rapidamente.
author: Becky
feature: Workfront Fusion
exl-id: 08e19a1a-7ca9-4c79-a165-f200048a5cda
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Configurar solução alternativa de tratamento de erros `retry`

Às vezes, é útil executar novamente um módulo com falha se houver uma chance de o motivo da falha ser resolvido rapidamente.

Atualmente, o Adobe Workfront Fusion não oferece a diretiva de manipulação de erros `retry`, mas há duas soluções alternativas disponíveis para simular a funcionalidade `retry`.

## Requisitos de acesso

+++ Expanda para visualizar os requisitos de acesso para a funcionalidade neste artigo.

Você deve ter o seguinte acesso para usar a funcionalidade neste artigo:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacote do Adobe Workfront 
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
   <p>Herdados: Qualquer um </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produto</td> 
   <td>
   <p>Novo:</p> <ul><li>Selecione ou Prime Workfront Plan: sua organização deve comprar o Adobe Workfront Fusion.</li><li>Plano do Ultimate Workfront: o Workfront Fusion está incluído.</li></ul>
   <p>Ou</p>
   <p>Atual: sua organização deve comprar o Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Para obter mais detalhes sobre as informações nesta tabela, consulte [Requisitos de acesso na documentação](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Para obter informações sobre licenças do Adobe Workfront Fusion, consulte [licenças do Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Soluções alternativas para a diretiva de manipulação de erros [!UICONTROL Repetir]

Atualmente, o Workfront Fusion não oferece a diretiva de manipulação de erros `retry`. Use uma das soluções alternativas a seguir para mimetizar a funcionalidade de nova tentativa.

Para obter instruções, consulte [Diretivas para tratamento de erros](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

* [Usar a diretiva Break](#use-the-break-directive)
* [Usar o módulo Repetidor](#use-the-repeater-module)

### Usar a diretiva Break

Quando a diretiva Break é executada, o estado da execução do cenário é armazenado na fila de execuções incompletas. Se isso ocorrer, você poderá resolver a execução incompleta manualmente.

Para obter instruções, consulte [Resolver erros manipulados pela diretiva Break](/help/workfront-fusion/create-scenarios/config-error-handling/resolve-error-from-break-directive.md)

Para obter instruções sobre como resolver execuções incompletas, consulte [Exibir e resolver execuções incompletas](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

#### Desvantagens

* O intervalo mínimo de novas tentativas é de um minuto.
* Se o módulo estiver processando vários pacotes e o processamento de um pacote falhar, a execução parcial (somente o pacote que causou o erro) será movida para a pasta de execuções incompletas e agendada para novas tentativas de acordo com as configurações da diretiva [!UICONTROL Break]. No entanto, a execução atual continua e o módulo continua a processar os pacotes subsequentes.

  Para impedir que o cenário seja executado novamente até que a execução armazenada na pasta Execuções incompletas seja resolvida com êxito, habilite a opção &quot;[!UICONTROL Processamento sequencial]&quot; nas [!UICONTROL Configurações de cenário].

Para obter mais informações sobre execuções incompletas, consulte [Exibir e resolver execuções incompletas](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

### Usar o módulo Repetidor

A solução alternativa do módulo Repetidor é mais complexa, mas mais personalizável.

#### Configurar a rota do manipulador de erros

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário no qual deseja adicionar a solução alternativa.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique no ícone **Controle de Fluxo** ![Controle de fluxo](assets/flow-control-icon.png) e selecione **Repetidor**.
1. No módulo Repetidor, defina o campo **[!UICONTROL Repetições]** para o número máximo de vezes que você deseja que o cenário seja repetido.
1. Anexe o módulo com falha potencial após o módulo **[!UICONTROL Repetidor]**.
1. Anexe uma rota de manipulador de erros ao módulo com falha potencial.

   Para obter instruções, consulte [Adicionar tratamento de erros](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).
1. Adicione o módulo **[!UICONTROL Tools] > [!UICONTROL Sleep]** à rota do manipulador de erros e defina seu campo **[!UICONTROL Delay]** como o número de segundos entre tentativas de repetição.

1. Adicione a diretiva **[!UICONTROL Ignore]** após o módulo **[!UICONTROL Tools] > [!UICONTROL Sleep]**.
1. Continue para [Configurar a rota padrão](#configure-the-default-route).

#### Configurar a rota padrão

1. Adicione o módulo **[!UICONTROL Tools] > [!UICONTROL Set variable]** em uma rota separada (manipulador sem erros) após o módulo com falha potencial, e configure-o para armazenar o resultado do módulo em uma variável nomeada, como `Result`.

1. Adicione o módulo **[!UICONTROL Array aggregator]** após **[!UICONTROL Tools] > [!UICONTROL Set variable]** e selecione o módulo **[!DNL Repeater]** em seu campo Source Module.

1. Adicione o módulo **[!UICONTROL Tools] > [!UICONTROL Get variable]** após o módulo **[!UICONTROL Array aggregator]** e mapeie o valor da variável `Result` a ele.

1. Insira o módulo **[!UICONTROL Ferramentas] > [!UICONTROL Obter variável]** entre o módulo **[!UICONTROL Repetidor]** e o módulo com falha potencial, e mapeie o valor da variável `Result` para ele.

1. Insira um filtro entre este módulo **[!UICONTROL Ferramentas] > [!UICONTROL Obter variável]** e o módulo com falha potencial para continuar somente se a variável `Result` não existir.

>[!BEGINSHADEBOX]

**Exemplo:**

Neste exemplo de cenário, o módulo [!UICONTROL HTTP] > [!UICONTROL Fazer uma solicitação] representa o módulo com falha potencial:

![HTTP Fazer uma solicitação](assets/http-make-request.png)

>[!ENDSHADEBOX]

Se o resultado do módulo com falha potencial for muito complexo para ser armazenado em uma variável simples, você poderá usar um armazenamento de dados para armazenar e recuperar o resultado. O armazenamento de dados conteria apenas um registro. A chave do registro pode ser, por exemplo, `Result`.

Para obter mais informações sobre armazenamentos de dados, consulte [Armazenamentos de Dados](/help/workfront-fusion/create-scenarios/map-data/data-stores.md).

#### Desvantagens

* Essa solução alternativa é mais complexa.
* Essa solução alternativa usa mais operações.

## Recursos

* Para obter mais informações sobre módulos Repetidores e diretivas de quebra, consulte [Controle de fluxo](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/flow-control.md).
* Para obter mais informações sobre os módulos Obter Variável, consulte [Ferramentas](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/tools-modules.md).
