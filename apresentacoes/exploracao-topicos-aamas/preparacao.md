---
titulo: "Preparação — apresentação dos tópicos AAMAS 2027 (19/11/2026)"
status: rascunho
fontes: [sumers2024coala, wu2025longmemeval, cemri2025multiagent, chen2023fireact, ross2011dagger, yao2022react, huyen2025aiengineering]
---

# Preparação para o encontro de 19/11/2026

Encontro **PDC 1 – Agentes Inteligentes**, quinta, **19/11/2026, 14h–15h**. Apresentação de
**até 3 minutos, sem slides**, com os três tópicos enviados no formulário.
`[Material: enunciado da atividade PDC]`

O roteiro da fala está no [README desta pasta](README.md). Este arquivo diz **o que ler, o que
aprender e o que anotar** antes do encontro.

## Objetivo

Não dá para ler quatro papers inteiros até amanhã, e não precisa. A meta é conseguir responder
as perguntas que cada justificativa vai provocar. Por isso cada leitura abaixo é **parcial**:
só as seções que sustentam o que eu disse no formulário.

## Etapas

| Etapa | Quando | Tempo | O que fazer | Pronto quando |
| --- | --- | --- | --- | --- |
| 1. Ler | Hoje à noite | ~2h | As leituras parciais da seção [Leituras](#leituras), na ordem da tabela | Li as seções marcadas de cada paper |
| 2. Anotar | Hoje à noite | ~40min | Preencher as fichas rápidas e a coluna "Resposta curta" das [perguntas prováveis](README.md#perguntas-prováveis) | Cada pergunta tem uma resposta de 1–2 frases com as minhas palavras |
| 3. Ensaiar | Amanhã de manhã | ~1h | Falar o [roteiro](README.md#roteiro-de-fala) 3–4 vezes com cronômetro, sem ler. Registrar cada ensaio | Fico abaixo de 3:00 duas vezes seguidas |
| 4. Revisar | Amanhã, ~13h30 | 15min | Reler só as respostas curtas e a frase do fio condutor | — |
| 5. Registrar | Depois do encontro | 20min | Preencher a [reunião 07](../../reunioes/07-apresentacao-topicos-aamas.md): o que o orientador comentou e o que ficou em aberto | Próximos passos escritos |

## Leituras

Ordem sugerida: primeiro o que sustenta o tópico 1 (maior interesse), depois o tópico 2, por
fim o tópico 3. As seções foram conferidas nas versões do arXiv indicadas em cada ficha.

| # | Paper | O que ler | Tempo | Ficha |
| --- | --- | --- | --- | --- |
| 1 | Sumers et al. (2024), **CoALA** | Seção 4.1 (Memory), 4.3 (Retrieval actions), 4.5 (Learning actions) e Figura 4 | 30min | [ficha](../../notas/exploracao-aamas-2027/fichas/2024-sumers-coala.md) |
| 2 | Wu et al. (2025), **LongMemEval** | Abstract, Introdução, Tabela 1, Seção 4.1 e Figura 4 | 30min | [ficha](../../notas/exploracao-aamas-2027/fichas/2025-wu-longmemeval.md) |
| 3 | Cemri et al. (2025), **MAST** | Abstract, Introdução, Seção 4 e Figura 1 (a taxonomia) | 30min | [ficha](../../notas/exploracao-aamas-2027/fichas/2025-cemri-mast.md) |
| 4 | Chen et al. (2023), **FireAct** | Abstract, Tabela 2 e o parágrafo de limitações da Seção 8 | 20min | [ficha](../../notas/exploracao-aamas-2027/fichas/2023-chen-fireact.md) |
| 5 | Ross, Gordon & Bagnell (2011), **DAgger** | Só o abstract e o primeiro parágrafo da Introdução | 10min | [ficha](../../notas/exploracao-aamas-2027/fichas/2011-ross-dagger.md) |

O ReAct e o capítulo 6 da Huyen já estão lidos ([análise do ReAct](../../papers/2022-yao-react.md),
[nota de memória](../../notas/agentes/04-memoria.md),
[nota de falhas](../../notas/agentes/05-modos-de-falha-e-avaliacao.md)). Só reler se sobrar tempo.

## Tópico 1 — Memória de longo prazo

**GAAI — Memory, state, context, long-lived interaction, and other architectural patterns for
generative and agentic AI systems**

### O que aprender

- **As quatro memórias do CoALA.** A memória de trabalho guarda a informação ativa do ciclo de
  decisão atual. A episódica guarda experiências de ciclos anteriores, como trajetórias. A
  semântica guarda conhecimento sobre o mundo e sobre o próprio agente. A procedural está nos
  pesos do LLM e no código do agente. `[Material: Sumers et al. 2024, seção 4.1]`
- **Ações sobre a memória.** Recuperação lê da memória de longo prazo para a de trabalho;
  aprendizado escreve na memória de longo prazo. `[Material: Sumers et al. 2024, seções 4.3 e 4.5]`
- **Onde o RAG se encaixa.** O RAG do HerpIA é recuperação de memória semântica escrita por
  quem montou a base; o agente não escreve nela. Memória episódica exige uma ação de
  aprendizado: o próprio agente decide o que gravar. `[Interpretação]`
- **As cinco habilidades do LongMemEval:** extração de informação, raciocínio entre sessões,
  raciocínio temporal, atualização de conhecimento e abstenção. `[Material: Wu et al. 2025]`
- **As três etapas de um sistema de memória:** indexação, recuperação e leitura.
  `[Material: Wu et al. 2025, seção 4 e Figura 4]`
- "Atualização de conhecimento" é o nome técnico da minha dúvida sobre informação
  desatualizada no HerpIA. `[Interpretação]`

### O que anotar

- Na ficha do CoALA: uma frase minha para cada tipo de memória, com um exemplo do HerpIA.
- Na ficha do LongMemEval: qual das cinco habilidades eu testaria primeiro no HerpIA e por quê.
- Os termos novos ("working memory", "learning action", "abstention") na seção "Conceitos
  desconhecidos" das fichas. Só levar para o [glossário](../../glossario.md) depois de
  entender.

## Tópico 2 — Detecção e recuperação de falhas

**GAAI — Failure handling, recovery, and resilience in agentic AI**

### O que aprender

- **A taxonomia MAST:** 14 modos de falha em três categorias: problemas de especificação/design
  do sistema (FC1), desalinhamento entre agentes (FC2) e verificação da tarefa (FC3).
  `[Material: Cemri et al. 2025, seção 4]`
- **Como ela foi construída:** anotação de traces por especialistas, com concordância medida
  pelo kappa de Cohen (0,88), e depois um LLM-as-a-judge validado para escalar a anotação.
  `[Material: Cemri et al. 2025]`
- **O ponto fraco da minha justificativa:** o MAST foi feito para sistemas **multiagente** e o
  paper não testa nem discute sistemas de um agente só. `[Material: Cemri et al. 2025]` Meu
  tópico fala em "agentes baseados em SLMs", que podem ser um agente só. FC2 não se aplica a um
  agente só; parte de FC1 e FC3 parece aplicável (repetição de passos, término prematuro,
  verificação incompleta). `[Interpretação]` Para um agente só, a divisão da Huyen
  (planejamento, ferramenta, eficiência) se encaixa melhor. `[Material: Huyen 2025, livro]`
- **Ligação com o tópico 1:** um dos modos do MAST é a perda do histórico da conversa
  (FM-1.4). Falha de memória já aparece como modo de falha catalogado. `[Material: Cemri et al. 2025]`
- **A conta do erro composto, com mais cuidado.** Se 95% for a chance de acertar cada passo
  **dado que os anteriores deram certo**, então 0,95¹⁰ ≈ 0,60 vale pela regra da cadeia, sem
  precisar supor independência. A suposição de independência só entra se 95% for uma média de
  acerto por passo medida sem esse condicionamento. Na prática, o número muda porque passos
  diferentes têm dificuldades diferentes e porque o agente às vezes corrige um erro depois.
  `[Interpretação]` (complementa a seção "Erro composto" da
  [nota de falhas](../../notas/agentes/05-modos-de-falha-e-avaliacao.md))

### O que anotar

- Na ficha do MAST: os 3 grupos e, de cada um, o modo de falha que eu já vi acontecer num
  projeto meu (HerpIA, RAG ANEEL ou TCC).
- Uma resposta curta para "o MAST serve para um agente só?".
- `[Hipótese]` a ser escrita com as minhas palavras: SLMs locais falham mais, então geram mais
  casos de falha a custo baixo. Risco: as falhas de um SLM podem ser de outro tipo (por
  exemplo, tool call malformada) e não se parecer com as de modelos grandes.

## Tópico 3 — Imitation learning

**LEARN — Imitation learning**

### O que aprender

- **O resultado do FireAct:** ajustar o Llama-2-7B com 500 trajetórias geradas pelo GPT-4
  aumenta o desempenho no HotpotQA em 77%. `[Material: Chen et al. 2023]` Esse ganho é
  **relativo**: em exact match, o Llama-2-7B passa de 14,8 (ReAct com prompting) para 26,2
  (FireAct), +11,4 pontos. `[Material: Chen et al. 2023, Tabela 2]`
- **Como os autores enquadram o próprio trabalho:** como destilação de conhecimento do GPT-4.
  O FireAct não usa o termo "imitation learning" nem "behavioral cloning".
  `[Material: Chen et al. 2023]` Chamar isso de imitation learning é leitura minha.
  `[Interpretação]`
- **Behavioral cloning:** treinar um modelo para prever a ação do especialista em cada estado,
  como num problema supervisionado comum. É a forma mais simples de imitation learning.
  `[Externo]`
- **Por que behavioral cloning não basta:** em imitation learning as observações futuras
  dependem das ações anteriores, o que viola a suposição i.i.d. do aprendizado estatístico, e
  isso leva a desempenho ruim na teoria e na prática. `[Material: Ross et al. 2011]` A ideia
  do DAgger é coletar novos dados nos estados que a própria política visita e pedir ao
  especialista a ação certa nesses estados. `[Externo]` `[A verificar]` conferir na seção 3
  do paper antes de citar.
- **Resposta para "onde termina o fine-tuning supervisionado":** enquanto o modelo só aprende
  com demonstrações fixas, é aprendizado supervisionado. Passa a ser aprendizado de agente
  quando os dados dependem das ações do próprio agente (DAgger) ou quando ele aprende com
  recompensa ao interagir (RL). `[Interpretação]`
- **Limitações declaradas no FireAct:** uma única tarefa (QA) e uma única ferramenta (busca
  Google); só três métodos (ReAct, CoT, Reflexion). `[Material: Chen et al. 2023, seção 8]`

### O que anotar

- Na ficha do FireAct: o ganho absoluto e o relativo lado a lado, e a frase "os autores chamam
  de destilação".
- Na ficha do DAgger: o problema em uma frase minha (por que copiar o especialista não basta).
- No [arquivo da área LEARN](../../notas/exploracao-aamas-2027/areas/learn.md), em "Conceitos
  que ainda não domino": política, MDP, distribution shift.

## O fio condutor

Os três tópicos tratam de **como erros se propagam ao longo do tempo**:

- pela memória (tópico 1): uma informação errada gravada é recuperada depois, possivelmente
  por outros agentes;
- pelos passos de uma tarefa (tópico 2): o erro composto;
- pelo aprendizado (tópico 3): um modelo que só imitou o especialista não sabe sair dos
  estados que o especialista nunca visitou.

`[Interpretação]` Só usar essa ligação na fala se eu concordar com ela depois das leituras.
