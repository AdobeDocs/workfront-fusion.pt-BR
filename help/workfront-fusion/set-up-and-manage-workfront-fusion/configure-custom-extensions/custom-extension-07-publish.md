---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Publicar sua extensão personalizada
description: Publicar sua extensão personalizada
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 1%

---

# Publicar sua extensão personalizada

>[!NOTE]
>
>Este artigo presume alguma familiaridade com ferramentas de desenvolvimento de software.

Sua extensão é executada no Fusion somente depois que ela é **criada**, **implantada** na Adobe e **aprovada** para sua organização. Os procedimentos dessa página mostram como publicar sua extensão e como verificar o resultado.

Essas informações são adaptadas da documentação oficial do Adobe e se aplicam especificamente ao Workfront Fusion. Para obter informações gerais sobre o Adobe, consulte [Fluxo de desenvolvimento de extensões da interface do usuário](https://developer.adobe.com/uix/docs/guides/development-flow/) e [Gerenciamento de extensões da interface do usuário](https://developer.adobe.com/uix/docs/guides/publication/) na documentação do Adobe.

## Espaços de trabalho

Todo projeto do App Builder tem um espaço de trabalho **Estágio** e **Produção**. Pense neles como ambientes:

* **Estágio** é para desenvolvimento e teste. Implante aqui enquanto itera. Nenhuma aprovação é necessária e o resultado é visível somente pelo switch de Teste de preparo descrito abaixo (ou pré-visualização local).
* **A produção** é para liberar para todos. Depois de implantar para produção, você envia uma **solicitação de aprovação** e, uma vez aprovada, a extensão é registrada no Registro de aplicativos da Adobe e mostrada para toda a organização.

>[!NOTE]
>
> **Funções:** criar e implantar precisa da função **Desenvolvedor**; enviar a solicitação de aprovação para publicação precisa de uma função **Administrador do Sistema**.
>Para obter mais informações, consulte:
>
> * [Configurar ferramentas e conta de extensão da interface do usuário](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)
> * [Como obter acesso](https://developer.adobe.com/uix/docs/guides/get-access/) na documentação do Adobe.

Por padrão, o Fusion mostra somente **extensões publicadas**. Essas são extensões que você implantou no espaço de trabalho **Produção** e enviou para **aprovação**. Esse é o padrão seguro, portanto, uma implantação em andamento nunca aparece para toda a organização por acidente.

Uma implantação no espaço de trabalho **Preparo** não foi publicada, portanto, ela não aparece no Fusion sozinha. Há duas maneiras de tentar uma extensão antes de publicá-la:

* **Visualize localmente** com `aio app run` (consulte [Visualização local das extensões da interface do usuário](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/) na documentação do Adobe). Nada é implantado e somente você o vê.
* **Carregue-o do Stage dentro do Fusion** ativando uma opção de teste por usuário em seu perfil do Fusion. Isso é descrito em [Testar uma compilação de preparo no Fusion](#test-a-stage-build-in-fusion) neste artigo.

## Testar um build de preparo no Fusion

Use esse fluxo para ver uma implantação de Estágio no Fusion antes de publicá-lo.

### Etapa 1: selecionar o espaço de trabalho Preparo

```sh
aio console where                  # shows current org / project / workspace
aio console workspace select       # choose Stage
```

### Etapa 2: criação

```sh
aio app build
```

Isso compila o front-end e executa o gancho de metadados (que gera `app-metadata.json`). Corrija todos os erros relatados antes de continuar.

### Etapa 3: implantar

```sh
aio app deploy
```

`deploy` faz duas coisas:

* **Hospeda sua interface** na rede de entrega de conteúdo da Adobe, em uma URL como `https://<project>-stage.adobeio-static.net`. A CLI imprime esta **URL do ponto de extremidade de extensão** quando termina. Este é o URL que o Fusion carrega em seu iframe.
* **Registra os pontos de extremidade de sua extensão** para o ponto de extensão (`fusion/nav-organization/1`) no espaço de trabalho de Preparo.

>[!TIP]
>
> **Se a implantação falhar com &quot;Ponto de extensão &#39;fusion/nav-organization/1&#39; não existe&quot; (erro 1060):** o ponto de extensão do Fusion ainda não está habilitado para sua organização. Essa é uma etapa de integração, não um erro no código.
>Para obter mais informações, consulte [O ponto de extensão não existe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md#error-1060-extension-point-does-not-exist) no artigo de solução de problemas.

### Etapa 4: ativar o Teste de preparo no seu perfil do Fusion

O Fusion carrega extensões de Preparo somente quando você opta por, por usuário:

1. Entre no Fusion com uma conta na **mesma organização** em que você implantou.
1. Abra o menu de avatar do usuário no canto superior e vá para **Configurações do Produto** > **Perfil do Fusion** > **Preferências**.
1. Ative a opção **Extensões de preparo**.

   O Fusion solicita que você recarregue.
1. Confirme a recarga.

Após o recarregamento, o Fusion carrega extensões do espaço de trabalho do Stage em vez do conjunto publicado, e rotula cada um **(Stage)** na navegação para que você possa separá-los.

Essa opção é uma configuração de teste pessoal armazenada no navegador, não uma configuração da organização. Desative-a (e recarregue) para voltar às extensões publicadas. Como é armazenado localmente, ele não o segue para outro navegador ou computador.

### Etapa 5: verificar no Fusion

1. Abra a seção que corresponde ao seu ponto de extensão:
   * `fusion/nav-organization/1` → a área **Organização** da navegação à esquerda.
   * `fusion/nav-team/1` → a área **Equipe** (selecione uma equipe primeiro).

   Um botão com o título definido em `getWidget()` é exibido, marcado como **(Estágio)**.
1. Clique no botão exibido.

Sua interface carrega e recebe o [contexto do Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

Se o botão não aparecer ou o painel mostrar um erro, consulte [Solução de problemas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Versão na produção

Quando sua extensão funcionar no Stage e você estiver pronto para todos os usuários:

### Etapa 1: alternar para o espaço de trabalho Produção

```sh
aio console workspace select       # choose Production
```

Quando a CLI perguntar sobre o arquivo `.env`, selecione **Mesclar** para manter suas variáveis de ambiente.

### Etapa 2: criar e implantar na produção

```sh
aio app build
aio app deploy
```

### Etapa 3: enviar a solicitação de aprovação

A publicação é uma **solicitação de aprovação enviada do espaço de trabalho de Produção**:

1. Abra o [Adobe Developer Console](https://developer.adobe.com/console), selecione sua **Organização**, abra seu **Projeto** e alterne para o espaço de trabalho **Produção**.
1. Envie seu aplicativo para **aprovação/publicação** (isso requer a função de **Administrador do Sistema**).
1. Após a aprovação, sua extensão será adicionada ao **Registro de Aplicativos Adobe** e ficará disponível na [Adobe Experience Cloud](https://experience.adobe.com), incluindo o Fusion, para sua organização.

Para obter instruções detalhadas, consulte [Gerenciamento de extensões da interface do usuário](https://developer.adobe.com/uix/docs/guides/publication/) na documentação do Adobe Developer.

## Status e atualizações

Vale a pena conhecer alguns comportamentos para que você possa diferenciar &quot;ainda está trabalhando nisso&quot; de &quot;algo está errado&quot;:

* **Implantado na Produção não é o mesmo que visível.** O `aio app deploy` para Produção carrega seu aplicativo, mas não faz com que a extensão apareça. Ela é exibida somente após a solicitação de aprovação ser enviada e aprovada. Se você implantou a Produção e ainda não a viu no Fusion, o motivo normal é que ela ainda não foi aprovada.
* **As atualizações somente de código não precisam de uma nova aprovação.** Se sua extensão já tiver sido publicada e você alterar apenas seu código (a interface do usuário ou as ações de tempo de execução), implante novamente no mesmo URL com:

  ```sh
  aio app deploy --force-deploy
  ```

  Os usuários obtêm a nova versão na próxima vez que abrirem a extensão. Não há nada para eles instalarem. Você só precisa enviar uma nova solicitação de aprovação quando alterar o próprio **registro**, por exemplo, adicionar um novo ponto de extensão ou alterar o que `getWidget()` anuncia.
* **Uma extensão revogada ou cancelada desaparece.** Se uma extensão for revogada por você ou cancelada, ela deixará de aparecer no Fusion sem nenhuma mensagem de erro. Se uma extensão em funcionamento anteriormente desaparecer para todos, verifique se ela foi revogada antes de procurar um problema de código.

## Remover (revogar) uma extensão

A remoção de uma extensão publicada é feita por **revogação** no Adobe Exchange:

1. Entrar no **Adobe Exchange**.
1. Vá para **Gerenciar** > **Aplicativos App Builder**.
1. Selecione **Revogar** ao lado da extensão que você deseja remover e confirme.

Após a revogação, a extensão mostra um status *revogado* no Extension Manager e não aparece mais no Fusion. Para removê-lo completamente, exclua o projeto na Developer Console. Um projeto não pode ser excluído até que sua extensão seja revogada.

Para uma implantação somente de teste de Preparo, é possível remover a implantação com:

```sh
aio app undeploy
```

## Recursos adicionais

Os seguintes recursos estão disponíveis na documentação do Adobe:

* [Fluxo de desenvolvimento de extensão da interface do usuário](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [Gerenciamento de extensões da interface do usuário (publicar/aprovar/revogar)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Criar um projeto no Developer Console](https://developer.adobe.com/uix/docs/guides/creating-project-in-dev-console/)
* [Como obter acesso (funções)](https://developer.adobe.com/uix/docs/guides/get-access/)
* [Visualização local das extensões da interface do usuário](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)
