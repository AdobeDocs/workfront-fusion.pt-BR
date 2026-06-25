---
name: writing-quality
description: Revise e melhore a qualidade da escrita técnica para artigos explicativos e documentação geral do Workfront. Aplica o Guia de estilo da documentação do Workfront e os princípios de Desenvolvimento de informações técnicas de qualidade. Use ao editar, revisar ou escrever artigos explicativos, artigos de visão geral, artigos de referência ou documentação geral. Não usar para notas de versão — use a habilidade release-notes-formatter.
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 1%

---


# Qualidade de gravação

Revisa e melhora a documentação do Workfront usando o Guia de estilo da documentação do Workfront e os princípios do DQTI.

## Fluxo de trabalho (WRK)

Ao revisar ou editar conteúdo:

1. Ler o arquivo de destino
2. Aplicar as regras abaixo — corrigir problemas diretamente ou sinalizá-los
3. Preservar a intenção e a precisão técnica do autor
4. Para obter terminologia, pontuação e regras de procedimento detalhadas, consulte .claude/commands/_writing-quality-reference.md

## Voz e ponto de vista

- Use **segunda pessoa** (&quot;Você pode...&quot;) ao endereçar o leitor
- Use contrações para um tom de conversação (não, não pode, é, eles são)
- Use &quot;Recomendamos&quot; para práticas recomendadas — não &quot;Recomenda-se&quot; ou &quot;Você deveria&quot;
- Ao escrever para um grupo de usuários, faça referência a outras funções em terceira pessoa (&quot;Você pode visualizar... No entanto, o administrador do Workfront pode restringir...&quot;)
- Nunca use pronomes de gênero — reestruturar a frase ou usar &quot;eles&quot;
- Não há barra para escolhas — use &quot;ou&quot; (&quot;ele&quot; e não &quot;ele/ela&quot;)

## Clareza (DQTI)

- Uma ideia por frase
- Sempre que possível, mantenha as frases abaixo de ~25 palavras
- Iniciar com a ação ou o resultado, não o contexto do plano de fundo
- Use a palavra mais simples que transmita o significado (&quot;use&quot; não &quot;utilize&quot;, &quot;start&quot; não &quot;initiate&quot;, &quot;about&quot; não &quot;concern&quot;)
- Evite nomeações (&quot;criar&quot; não &quot;a criação de&quot;, &quot;configurar&quot; não &quot;a configuração de&quot;)
- Use uma linguagem específica e concreta — evite termos vagos (&quot;vários&quot;, &quot;vários&quot;, &quot;alguns&quot;)
- Evite negativos duplos
- Use pronomes opcionais (&quot;that&quot;, &quot;who&quot;) para adicionar clareza à estrutura da frase

## Grau de concretude (DQTI)

- Use exemplos específicos em vez de descrições abstratas
- Incluir valores realistas em exemplos
- Nomeie os elementos, campos e áreas exatos da interface do usuário

## Orientação de tarefa (DQTI)

- Concentre-se no que o usuário pode *fazer*, não no que o sistema *é*
- Instruir procedimentos com verbos imperativos (&quot;Criar uma tarefa&quot;, &quot;Configurar notificações&quot;)
- Forneça contexto suficiente para o usuário agir, mas não mais
- Incluir um link para a ajuda detalhada (&quot;Para obter mais informações, consulte o [artigo].&quot;)

## Uso de letras maiúsculas

- **Cabeçalhos**: primeira letra maiúscula sempre (&quot;Criar uma tarefa&quot; e não &quot;Criar uma tarefa&quot;)
- **Termos do Workfront**: use letras maiúsculas somente ao fazer referência direta a um elemento da interface do usuário
   - Referência direta: &quot;Preencha o campo Data de conclusão planejada&quot;.
   - Referência indireta: &quot;Cada tarefa deve ter uma data de conclusão planejada&quot;.
   - Dica: se você puder colocar &quot;o&quot; ou &quot;a&quot; na frente do termo, geralmente deverá estar em minúsculas
- **Botões**: seguir capitalização da interface, exceto botões com maiúsculas → caso da frase
- **Funções**: &quot;Administrador do Sistema&quot; para a função na interface do usuário; &quot;Administrador do Workfront&quot; para a pessoa

## Cabeçalhos

- Use o comando imperativo no caso da sentença (&quot;Criar uma tarefa&quot;, &quot;Configurar níveis de acesso&quot;)
- Os títulos devem ser baseados em tarefas — descreva o que o usuário realizará
- Os artigos de visão geral terminam com &quot;visão geral&quot; (&quot;Visão geral dos projetos&quot;)
- Quebrar seções longas em vários cabeçalhos com submetas claras

## Referências cruzadas e links

Use estes padrões exatos:

| Situação | Formato |
|-----------|--------|
| Vincular após fornecer informações | &quot;Para obter mais informações, consulte [Nome do artigo].&quot; |
| Link sem informações anteriores | &quot;Para obter informações, consulte [Nome do artigo].&quot; |
| Link para uma seção em outro artigo | &quot;Para obter mais informações, consulte [Nome da seção] em [Nome do artigo].&quot; |
| Link para uma seção no mesmo artigo | &quot;Para obter mais informações, consulte [Nome da seção] neste artigo.&quot; |

- Em um parágrafo: em linha com o texto
- Em uma etapa de procedimento: em uma nova linha após a etapa
- Vários links: use uma lista com marcadores
- Usar &quot;canto superior direito&quot; / &quot;canto superior esquerdo&quot; para posições de tela

## Negrito e Itálico

- **Negrito** ações clicáveis e elementos da interface do usuário somente nas etapas de procedimento
- Não colocar em negrito elementos da interface fora das etapas do procedimento
- Não coloque em negrito nomes de caixas de diálogo, nomes de páginas, nomes de ícones ou nomes de menus fora das etapas
- Use *itálico* para o texto que o usuário deve digitar (&quot;Digite *my.workfront.com* na caixa de URL&quot;)
- Nunca use itálico para ênfase — reestruturar a frase em vez disso

## Notas, dicas e avisos

Use com moderação — o uso excessivo os torna invisíveis para os leitores.

- Máximo de uma nota/dica/aviso por seção
- Nunca empilhar várias notas
- Combinar notas relacionadas em uma nota com uma lista com marcadores
- Não use anotações para anunciar novas funcionalidades — retrabalhe o texto do artigo

| Tipo | Finalidade |
|------|---------|
| `>[!NOTE]` | Informações que não se encaixam no parágrafo; evitar frustração; controle de versão/compatibilidade |
| `>[!TIP]` | Sugestões interessantes que facilitam a vida do usuário |
| `>[!IMPORTANT]` | Informações vitais para a etapa ou procedimento |
| `>[!WARNING]` | Alertar o usuário sobre possível perda de dados |

## Procedimentos

- Usar cabeçalhos de comando imperativos (&quot;Criar uma tarefa&quot;)
- Introduções apenas quando necessário — o título deve ser suficiente
- Formato de introdução preferencial: frase infinitiva + dois pontos (&quot;Para criar uma senha temporária:&quot;)
- Os procedimentos de etapa única ainda usam uma lista numerada
- Use &quot;type&quot; ou &quot;select&quot; — evite palavras vagas como &quot;set&quot; ou &quot;specified&quot;
- Etapas condicionais: &quot;(Condicional) Se você for membro de mais de uma equipe, selecione...&quot;
- Etapas opcionais: &quot;(Opcional) Para adicionar um emoji, clique em...&quot;
- Descreva a resposta do sistema antes que ocorra ou imediatamente depois
- Vários métodos: documente primeiro a maneira mais simples e, em seguida, use &quot;Ou&quot;

### Colchetes Angulares à Direita em Procedimentos

- Use `>` para mostrar a navegação de menu/guia: &quot;Clique em **Email** > **Notificações**&quot;
- Negrito nos nomes dos botões, não nos colchetes
- Incluir espaços ao redor dos colchetes
- Não usar colchetes para navegação no menu principal — usar o trecho do menu principal

## Referência rápida de pontuação

| Regra | Exemplo |
|------|---------|
| Vírgula de Oxford sempre | &quot;motivo, meios e oportunidade&quot; |
| Vírgula antes de &quot;then&quot; em procedimentos | &quot;Clique em Configurar e depois em Interface.&quot; |
| Vírgula após ano em uma data no meio da frase | &quot;A edição de 2 de janeiro de 2016 do...&quot; |
| Sem vírgula com mês-ano apenas | &quot;Janeiro de 2016&quot; |
| Dois pontos antes de uma lista, minúsculas depois de | &quot;Selecione uma das opções a seguir: opção A&quot; |
| Nenhum sinal de dois pontos após os cabeçalhos do procedimento | &quot;Criar uma tarefa&quot; (não &quot;Criar uma tarefa:&quot;) |
| Traços eme com moderação | Reestruturar a sentença, se possível |
| Períodos em extensões de arquivo | &quot;Carregar um arquivo PDF&quot; |

Para obter regras completas de pontuação e terminologia, consulte .claude/commands/_writing-quality-reference.md.

## Integridade (DQTI)

- Inclua todas as informações que o usuário precisa entender e agir
- Não inclua informações desnecessárias para o usuário
- Sempre forneça um link &quot;Para obter mais informações&quot; para a documentação detalhada
- Padrões do sistema de documentos: &quot;(Padrão)&quot; em listas ou descreva na sentença

## Organização (DQTI)

- Estrutura lógica com divulgação progressiva (visão geral → detalhes → referência)
- Conteúdo mais recente primeiro para páginas ordenadas por tempo (por exemplo, notas de versão)
- Um tópico por seção
- Usar listas para mais de 3 itens paralelos
- Usar tabelas para comparações estruturadas ou descrições de campo
- Evitar parágrafos na parede do texto — dividir em partes digeríveis

## Tipos de artigo

| Tipo | Finalidade | Convenção do título |
|------|---------|-----------------|
| Visão geral | Contexto, diagramas, como as coisas funcionam — sem procedimentos | Termina com &quot;visão geral&quot; |
| Como | Tarefa específica com etapas claras | Verbo imperativo |
| Introdução | Informações de configuração + links para novos usuários | &quot;Introdução a...&quot; |
| Referência | Descrições de campo em tabelas | Frase substantiva descritiva |

## Lista de verificação de validação

Após a edição, verifique:

- [ ] Segunda pessoa (&quot;você&quot;), contrações usadas
- [ ] Primeira letra da sentença em maiúscula em todos os cabeçalhos
- [ ] termos do Workfront escritos corretamente em maiúsculas (referência direta ou indireta)
- [ ] Negrito somente em ações clicáveis nas etapas de procedimento
- [ ] As referências cruzadas usam o formato padrão (&quot;Para obter mais informações, consulte...&quot;)
- [ ] Notas/dicas/avisos não empilhados, máx. um por seção
- [ ] Vírgula de Oxford usada consistentemente
- [ ] As etapas do procedimento usam verbos específicos (digitar, selecionar, clicar — não &quot;definir&quot; ou &quot;especificar&quot;)
- [ ] Etapas condicionais/opcionais rotuladas corretamente
- [ ] Nenhum pronome de gênero
- [ ] Frases são claras, concretas e orientadas a tarefas
