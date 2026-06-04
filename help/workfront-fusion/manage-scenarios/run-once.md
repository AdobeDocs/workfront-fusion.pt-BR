---
title: Usar Executar uma vez para testar um cenário
description: Você pode testar um cenário sem um acionador externo usando o botão Executar uma vez.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 9c05aa1111fd571ea6f0ff86943b2849a39e4973
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 0%

---

# Usar Executar uma vez para testar um cenário

Ao criar, atualizar ou refinar um cenário, você pode usar o botão &quot;Executar uma vez&quot; para acionar o cenário sob demanda. Dessa forma, você pode testar o cenário sem esperar pela lógica do acionador, como eventos específicos ou intervalos de polling.

Também é possível executar um cenário uma vez para configurar as estruturas de dados

>[!TIP]
>
>Recomendamos testes com frequência à medida que você cria e refina cenários.

## Usar a funcionalidade Executar uma vez

O recurso Executar uma vez é encontrado no editor de cenários.

1. Clique na guia **[!UICONTROL Cenários]** no painel esquerdo.
1. Selecione o cenário em que deseja executar o Especialista em Pontuação de Cenários.
1. Clique em qualquer lugar no cenário para entrar no editor de cenários.
1. Clique em **Executar uma vez** no canto inferior esquerdo do Editor de cenários.
1. (Condicional) Se o cenário for acionado por um webhook ou for um cenário filho, selecione a entrada para a execução de teste.

   * **Aguardar uma chamada de webhook externo**: o cenário começará a escutar uma chamada de webhook recebida. Você deve acionar o webhook do sistema externo para fornecer o webhook.

     Por exemplo, se o webhook estiver escutando uma nova solicitação no Workfront, você deve criar uma nova solicitação no Workfront para acioná-la para concluir a funcionalidade &quot;Executar uma vez&quot;.

     >[!NOTE]
     >
     >Essa opção está disponível somente para cenários de webhook.

   * **Usar uma entrada de execução anterior**: você deve selecionar uma execução anterior. A execução &quot;Run once&quot; usa os dados de entrada que acionaram a execução selecionada.

     Para selecionar uma execução anterior, selecione-a e clique em **Executar**.

     Para examinar os dados de entrada da execução antes de selecioná-los, clique em **Visualizar entrada** para essa execução.

     >[!NOTE]
     >
     >O cenário deve ter concluído as execuções anteriores antes que essa opção esteja disponível.

   * **Fornecer entrada manualmente**: você deve fornecer a carga do webhook para a entrada do cenário. Deve estar no formato JSON.

     Para fornecer a entrada, insira o texto na caixa **Conteúdo do Webhook** e clique em **Executar**.
