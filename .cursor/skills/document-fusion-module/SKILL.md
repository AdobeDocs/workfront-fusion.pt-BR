---
name: document-fusion-module
description: Documente um novo módulo do conector Adobe Workfront Fusion adicionando-o ao artigo do conector apropriado em help/workfront-fusion/references/apps-and-modules/. Use quando o usuário solicitar adicionar, documentar ou descrever um novo módulo do Fusion, ou quando o usuário fornecer capturas de tela de um painel de configuração do módulo do Fusion e quiser que o artigo correspondente seja atualizado.
source-git-commit: 976db79104d226a16a35dc04e8c8cb111eb745db
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 0%

---


# Documentar um módulo do conector Fusion

Use esta habilidade para adicionar um ou mais novos módulos a um artigo do Workfront Fusion Connector (por exemplo, `adobe-firefly-modules.md`, `adobe-photoshop-modules.md`, `azure-dev-ops.md`).

## Entradas necessárias (por módulo)

Antes de preencher os campos de qualquer módulo, o usuário **deve** fornecer todos os itens a seguir. Se algum estiver ausente, pare e solicite-o antes de continuar.

1. **O nome do módulo** — exatamente como aparece na interface do Fusion (por exemplo, `Generate adaptive composite`).
2. **Caminho do artigo do conector** — o agente localiza isso e confirma com o usuário (consulte a Fase 1).
3. **A URL da API** para a operação de API subjacente. Isso é necessário para que a finalidade de cada campo possa ser cruzada com a especificação da API.
4. **Uma captura de tela do painel de configuração do módulo na exibição padrão** (`Show advanced settings` **desmarcado**).
5. **Uma captura de tela do painel de configuração do módulo na exibição avançada** (`Show advanced settings` **marcada**) ou uma declaração explícita de que o módulo não tem campos avançados.

## Fluxo de trabalho (WRK)

Este é um processo de várias fases. O ritmo é importante — trabalhe *com* o usuário, não antes dele. Confirme o progresso em cada limite da fase e mantenha-se aberto a correções a qualquer momento.

### Fase 1 — Âmbito dos trabalhos

1. **Pergunte se este é um ou vários módulos**: *&quot;Você está adicionando um único módulo ou vários módulos a um artigo de conector?&quot;*

2. **Colete cada nome de módulo antecipadamente**, com base na resposta:
   - **Módulo único**: solicite seu nome exato como ele aparece na interface do usuário do Fusion.
   - **Vários módulos**: peça todos os nomes de uma vez OU peça uma captura de tela do conector que os liste (por exemplo, a tela de visão geral do conector no Fusion que mostra rótulos de bloco para cada módulo). De qualquer maneira, encerre esta etapa com uma lista confirmada de cada novo módulo a ser adicionado.

3. **Localize você mesmo o artigo sobre o conector** pesquisando `help/workfront-fusion/references/apps-and-modules/` com base no nome do conector implícito no(s) módulo(s). Use as ferramentas `Glob` ou `Grep`.

4. **Confirme o caminho do artigo com o usuário**: *&quot;Com base no(s) nome(s) do módulo, isso deve ir para `help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-firefly-modules.md`. Está correto?&quot;*

5. **Leia o artigo sobre o conector** para conhecer sua estrutura e convenções existentes. Preste atenção a:
   - Estilo do cabeçalho (normalmente `### Module name` em maiúsculas e minúsculas)
   - Ordenação do módulo existente (normalmente em ordem alfabética)
   - Como as linhas `Connection` são redigidas
   - Como os campos aninhados são gravados (por exemplo, `Image > Source`)
   - Quaisquer convenções de nota de rodapé ou anotação existentes

### Fase 2 — Coloque espaços reservados para cada módulo na frente

Mesmo que haja apenas um novo módulo, isso oferece ao usuário um roteiro visual claro. Se houver vários módulos novos, coloque todos eles agora.

Para cada novo módulo, insira uma seção de espaço reservado em posição alfabética:

```markdown
### Module name

<!-- PLACEHOLDER: Add description of the Module name module here. -->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Connector Name], see <a href="#create-a-connection-to-connector-name" class="MCXref xref" >Create a connection to [!DNL Connector Name]</a> in this article.</td> 
  </tr> 
  <!-- PLACEHOLDER: Add field rows for the Module name module here. -->
 </tbody> 
</table>
```

Mostre ao usuário a lista de espaços reservados que foram adicionados (por exemplo, &quot;Espaços reservados adicionados para: Gerar composto adaptável, Gerar imagens com Imagem5, Gerar composto preciso, Gerar vídeo&quot;). Em seguida, pergunte com qual começar: *&quot;Com qual você gostaria de começar?&quot;*

### Fase 3 — Loop de documentação por módulo

Para cada módulo, conclua este loop completamente antes de passar para o próximo:

#### 3-A. Obter o URL da API

Peça ao usuário a URL da API: *&quot;Compartilhe a URL da API para a operação de API subjacente de `<module name>`.&quot;*

Quando você tiver:
- Tente `WebFetch` no URL.
- Se a página estiver vazia/renderizada por JS (comum com documentos do Adobe Developer), procure uma página de guia de recurso relacionada — normalmente em uma URL `.../guides/how-tos/...` — e busque-a.
- Se ainda não tiver sorte, volte para `WebSearch` para obter o nome da operação.

Use o que você aprender como contexto de plano de fundo para descrições de campo mais tarde. Não despeje no usuário; apenas confirme-o brevemente: *&quot;Obtive o contexto da API — pronto para a captura de tela de exibição padrão.&quot;*

#### 3-B. Obter a captura de tela padrão

Pergunte: *&quot;Compartilhe uma captura de tela do painel de configuração do módulo com `Show advanced settings`**desmarcado**. Depois que trabalharmos nos campos padrão, solicitarei a exibição avançada, mas ainda não a enviarei.&quot;*

#### 3-C. Documentar os campos padrão

Trabalhando na captura de tela da exibição padrão, capture todos os campos visíveis de cima para baixo. Para cada campo:

1. Use o rótulo exato da interface do usuário do campo como o cabeçalho da linha. Para campos agrupados, associe com ` > `:

   ```
   [!UICONTROL Background > Image > Source]
   ```
2. Leia o texto de ajuda sob o campo na captura de tela (a legenda cinza/amarela). Use-a como base para a descrição.
3. Faça referência cruzada do contexto da API da etapa 3a para identificar o que o campo representa (por exemplo, `background.fillAreaMask` é &quot;a área do plano de fundo em que o objeto será colocado&quot;).
4. Escreva a descrição combinando **o que é o campo** (da API) com **como fornecê-lo** (do texto auxiliar da interface e do tipo de campo).

Ignore qualquer campo que não esteja visível na captura de tela, mesmo que a API ofereça suporte a ele. Não invente campos.

Depois que os campos padrão estiverem implementados, resuma-os brevemente ao usuário (por exemplo, &quot;Campos padrão adicionados: Conexão, Prompt, Taxa de proporção, ...&quot;) e vá para a etapa 3d.

#### 3-D. Obter a captura de tela de visualização avançada

Pergunte: *&quot;Agora compartilhe uma captura de tela do painel de configuração do módulo com `Show advanced settings`**marcado**. Se o módulo não tiver campos avançados, digamos que sim, e nós vamos continuar.&quot;*

#### 3-E. Documentar os campos avançados

Trabalhando na captura de tela da visualização avançada:

1. Identifique os campos que *ainda não* no modo de exibição padrão — esses são os campos avançados.
2. Para cada campo avançado, siga o mesmo processo de descrição da etapa 3c.
3. Acrescentar `*` ao nome do campo dentro de `<td role="rowheader">`:

   ```html
   <td role="rowheader">[!UICONTROL Seeds]*</td>
   ```
4. Após o fechamento de `</table>`, adicione esta nota de rodapé em sua própria linha:

   ```markdown
   * These fields are advanced fields, and do not display unless you select **[!UICONTROL Show advanced settings]**.
   ```

Se o usuário disse que o módulo não tem campos avançados, ignore as etapas 3d e 3e inteiramente.

#### 3-F. Elaborar a descrição do módulo

Agora (não antes), substitua o espaço reservado de descrição na parte superior da seção por um rascunho de uma frase com base no contexto da API e no que os campos implicam. Sempre o ofereça como rascunho para revisão pelo usuário:

> *&quot;Eu rascunhei esta descrição: &#39;...&#39;. Deseja usá-lo, editá-lo ou substituí-lo?&quot;*

#### 3G. Encapsulamento por módulo

Forneça ao usuário um resumo final dos campos documentados do módulo (padrão + avançado) e faça perguntas abertas:

- Houve algum campo cortado nas capturas de tela?
- A descrição do módulo é aceitável?
- Alguma coisa deve ser sinalizada como obsoleta ou digna de nota?

Aguarde a confirmação antes de dizer que o módulo foi concluído. Em seguida, pergunte: *&quot;Pronto para ir para o próximo módulo?&quot;* (ou &quot;Concluímos este artigo de conector.&quot;)

### Fase 4 — Verificação final

Depois que todos os módulos forem documentados, execute esta lista de verificação para cada um:

- [ O cabeçalho do módulo ] é `### ` (H3) e usa letra da sentença em maiúscula.
- [ O módulo ] aparece em ordem alfabética em relação aos seus módulos irmãos.
- [ ] A primeira linha é `Connection` e usa a redação padrão do link de conexão.
- [ ] Todos os campos documentados estão visíveis nas capturas de tela do usuário.
- [ ] Campos avançados estão marcados com `*` e existe uma única nota de rodapé abaixo da tabela.
- [ ] Nenhum campo inventado somente da API.
- [ As descrições suspensas do Source ] usam os rótulos exatos de opção da interface do usuário (consulte &quot;Convenção de campo do Source&quot; abaixo).
- [ A descrição do módulo ] é um resumo em uma frase que descreve o que o módulo faz.

## Convenção de campo do Source

Os campos de origem de imagem em conectores do Fusion normalmente apresentam uma lista suspensa com duas opções. **Use os rótulos exatos mostrados na captura de tela do usuário** — diferentes gerações de módulos usam diferentes palavras:

| Se a lista suspensa mostrar... | Usar este formato |
|---|---|
| **Carregar Imagem** e **URL da Imagem** (módulos mais recentes) | `<ul><li><b>Upload Image</b><p>Upload the image, or map the image file from a previous module.</p></li><li><b>Image URL</b><p>Enter or map the URL of the image.</p></li></ul>` |
| **Arquivo** e **URL pré-assinada** (módulos mais antigos) | `<ul><li><b>File</b><p>Select a source file from a previous module, or map the source file's reference image file name and reference image file.</p></li><li><b>Presigned URL</b><p>Enter or map the URL of the source image.</p></li></ul>` |

Se a captura de tela não mostrar as opções suspensas abertas, peça ao usuário para compartilhá-las.

## Estilo de descrição do campo

- Combine a voz e a estrutura das entradas do módulo existentes no mesmo artigo.
- Mantenha as descrições breves: geralmente, uma ou duas frases por campo são suficientes.
- Use a marcação `[!UICONTROL ...]` para qualquer nome de campo da interface do usuário referenciado de outro campo.
- Use `<code>...</code>` para valores literais (`<code>en-US</code>`, `<code>0.0</code>`).
- Para campos de intervalo numérico, defina o intervalo permitido explicitamente: *&quot;Digite um número entre 0 e 1...&quot;*.
- Para menus suspensos com opções discretas, enumere-os como um `<ul>` com `<b>Option</b>` seguido pela descrição `<p>`.

## Campos comuns e descrições recomendadas

Reutilize-os para obter consistência entre módulos:

**Sementes** (quando o campo permite vários valores de semente por meio do item Adicionar):
> Clique em **Adicionar item** para adicionar um valor de propagação e, em seguida, insira ou mapeie um inteiro. Use uma seed por variação. A contagem de valores de propagação deve corresponder ao valor **Número de Variações** se ambos forem fornecidos.

**Número de Variações** (substitua o intervalo pelo intervalo real da captura de tela):
> Insira um número entre [min] e [max]. O módulo gera este número de [variações de tipo de saída].

**Limite** (o limite do ciclo de execução do Fusion padrão; inclua apenas se estiver visível na captura de tela):
> Insira ou mapeie o número máximo de resultados com os quais você deseja que o módulo funcione durante um ciclo de execução.

**Localidade**:
> Insira ou mapeie um idioma e código de região para adaptar o conteúdo gerado a um país e idioma específicos. A localidade deve ser fornecida no código de idioma ISO 639-1 e na região ISO 3166-1. Exemplo: `en-US`

## Estar aberto a correções a qualquer momento

O usuário pode corrigir o fluxo intermediário do trabalho anterior — texto de seeds, rótulos suspensos, posicionamento de campo, divisão avançada/padrão etc. Tratar qualquer correção como autoritativa e atualizar sem retrocesso. Após a correção, resuma brevemente o que foi alterado.

Se o usuário introduzir um novo mid-flow de convenção (por exemplo, &quot;vamos marcar campos avançados com `*` e adicionar uma nota de rodapé&quot;), adote-o para o restante da sessão e aplique-o retroativamente a qualquer módulo já documentado.

## O que fazer se as informações estiverem em conflito

Quando a especificação da API e a interface do usuário discordarem (isso acontece com frequência):

1. **Confie na interface**, pois é isso que o usuário realmente vê no Fusion.
2. **Anote a discrepância** em sua resposta ao usuário para que ele possa decidir se deseja investigar mais detalhadamente.
3. **Não inventar uma explicação** no corpo do artigo — mantenha-a de acordo com o que está na interface.

Se duas capturas de tela do usuário se contradizerem (por exemplo, uma mostra `Blend`, outra mostra `Harmonization` para o mesmo módulo), pare e pergunte qual delas está correta antes de gravar. Identifique qual captura de tela provavelmente pertence a um módulo diferente, fazendo referência cruzada à especificação da API.
