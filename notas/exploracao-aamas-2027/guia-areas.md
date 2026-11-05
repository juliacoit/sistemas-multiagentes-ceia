---
titulo: "Guia das 11 áreas da AAMAS 2027"
status: rascunho — expandir com os materiais
fontes: [chamada AAMAS 2027 (main track), guia AAMAS 2027 (gerado por IA)]
---

# Guia das 11 áreas da AAMAS 2027

Referência da [exploração de tópicos](README.md). Reorganiza o "Guia dos tópicos da AAMAS
2027",
escrito por um assistente de IA ([referencias/materiais.md](../../referencias/materiais.md)), e
foi
conferido contra a [chamada da trilha
principal](https://warwick.ac.uk/fac/sci/dcs/aamas2027/calls/call-for-main-track/) em
05/11/2026.

## Origem de cada parte

| Parte | Origem | Rótulo |
| --- | --- | --- |
| Nomes das áreas e dos subtópicos | Chamada | `[Material: chamada AAMAS 2027]` |
| Trechos em inglês citados em "Quando vai para esta área" | Chamada | `[Material: chamada AAMAS 2027]` |
| Descrições, resumo da regra, "o que é", exemplos de pergunta, leituras e glossário | Assistente de IA | `[Material: guia AAMAS 2027 (gerado por IA)]` |

As explicações e os exemplos de pergunta servem para orientar a leitura. Não são definições
oficiais nem afirmações sobre o que a literatura já resolveu. `[Material: guia AAMAS 2027
(gerado por IA)]`

## Notas sobre os nomes

- Nomes dos subtópicos **sempre no original em inglês**, na forma completa da chamada. O guia
  original encurtava 31 deles (por exemplo, "Hybrid classic-generative agents" sem ", with a
focus
  on how generative AI agents use classical tools, models, and protocols").
- A própria página da chamada é inconsistente em dois nomes de área: a lista do topo traz
  "Representation, and Reasoning" e "Modelling and Simulation of Societies"; os títulos das
  seções trazem "Representation and Reasoning" e "Modeling and Simulation of Artificial
  Societies". Aqui uso os títulos das seções. `[Material: chamada AAMAS 2027]`
- A tradução automática do site tem erros: *Search* virou "Pesquisa" e *prompt engineering*
  virou "engenharia rápida". Em SOPS, *Search* é busca algorítmica. `[Material: guia AAMAS 2027
(gerado por IA)]`

## Como usar

Primeiro leia a descrição de cada área e marque as que despertam curiosidade; só então desça
para os subtópicos. `[Material: mensagem do orientador, 04/11/2026]`
As anotações pessoais ficam em [areas/](areas/), um arquivo por área.

| Sigla | Área | Subtópicos | Minhas anotações |
| --- | --- | --- | --- |
| [LEARN](#learn--learning-and-adaptation) | Learning and Adaptation | 13 | [areas/learn.md](areas/learn.md) |
| [GAAI](#gaai--generative-and-agentic-ai) | Generative and Agentic AI | 23 | [areas/gaai.md](areas/gaai.md) |
| [GTEP](#gtep--game-theory-and-economic-paradigms) | Game Theory and Economic Paradigms | 17 | [areas/gtep.md](areas/gtep.md) |
| [COINE](#coine--coordination-organizations-institutions-norms-and-ethics) | Coordination, Organizations, Institutions, Norms, and Ethics | 15 | [areas/coine.md](areas/coine.md) |
| [SOPS](#sops--search-optimization-planning-and-scheduling) | Search, Optimization, Planning, and Scheduling | 14 | [areas/sops.md](areas/sops.md) |
| [RR](#rr--representation-and-reasoning) | Representation and Reasoning | 12 | [areas/rr.md](areas/rr.md) |
| [EMAS](#emas--engineering-and-analysis-of-multiagent-systems) | Engineering and Analysis of Multiagent Systems | 18 | [areas/emas.md](areas/emas.md) |
| [SIM](#sim--modeling-and-simulation-of-artificial-societies) | Modeling and Simulation of Artificial Societies | 12 | [areas/sim.md](areas/sim.md) |
| [HAI](#hai--human-agent-interaction) | Human-Agent Interaction | 14 | [areas/hai.md](areas/hai.md) |
| [ROBOT](#robot--robotics-and-control) | Robotics and Control | 17 | [areas/robot.md](areas/robot.md) |
| [IASI](#iasi--innovative-applications-and-societal-impact) | Innovative Applications and Societal Impact | 12 | [areas/iasi.md](areas/iasi.md) |

## LEARN — Learning and Adaptation

Estuda como agentes **melhoram o próprio comportamento** a partir de dados, experiência ou
feedback, sozinhos ou junto com outros agentes que também aprendem. É a ponte entre Machine
Learning e agentes. `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando a contribuição principal é um método de aprendizado, uma
análise teórica de aprendizado ou um estudo empírico de aprendizado em agentes. Se o foco for a
arquitetura, o workflow ou a avaliação de agentes baseados em LLM, a chamada manda para GAAI.
`[Material: guia AAMAS 2027 (gerado por IA)]`

Texto da chamada:

> Papers should be submitted to LEARN when the main contribution is a learning method,
> learning-theoretic analysis, or empirical study of learning in agent or multiagent settings.
> Papers focused primarily on generative-model-based agent architectures, workflows, or
> evaluation should be submitted to GAAI.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Reasoning and learning under uncertainty | Decidir e aprender quando o agente não sabe tudo sobre o mundo e os resultados das ações são probabilísticos | Como um agente decide bem quando só observa parte do ambiente? |
| Supervised learning | Aprender a partir de exemplos rotulados (entrada → resposta certa) | Que dados rotulados ensinam um agente a classificar situações? |
| Unsupervised and representation learning | Descobrir estrutura em dados sem rótulos e aprender boas representações (vetores) do que o agente percebe | Que representação do ambiente torna o aprendizado mais fácil? |
| Reinforcement learning | Aprender por tentativa e erro, maximizando uma recompensa acumulada ao longo do tempo | Como o agente aprende uma estratégia só recebendo pontos por acertos? |
| Multiagent learning | Vários agentes aprendendo ao mesmo tempo; o ambiente muda porque os outros também mudam | Agentes que aprendem juntos convergem para cooperação ou competição? |
| Evolutionary and biologically inspired algorithms | Métodos inspirados em evolução e na natureza (populações, mutação, seleção, enxames) | Uma população de agentes evolui estratégias melhores que um agente treinado sozinho? |
| Learning agent capabilities | Aprender novas habilidades ou ações que o agente ainda não tinha | Como o agente adquire uma habilidade nova sem esquecer as antigas? |
| Learning agent-to-agent interactions, including learning to communicate and emergent communication | Agentes aprendem a interagir e até a inventar uma "linguagem" própria a partir da recompensa | Que protocolo de comunicação surge quando dois agentes precisam cooperar? |
| Human-in-the-loop learning | Humanos fornecem feedback, correções ou preferências que viram sinal de treino (é de onde vem o RLHF) | Quanto feedback humano é necessário para alinhar o comportamento do agente? |
| Few-shot learning | Aprender uma tarefa nova com pouquíssimos exemplos | Um agente generaliza para uma tarefa nova vendo três exemplos? |
| Distributionally robust learning | Aprender modelos que continuam funcionando quando os dados mudam em relação ao treino | O agente mantém o desempenho num ambiente diferente do de treino? |
| Adversarial learning | Aprender na presença de um adversário que tenta enganar ou atacar o modelo | Como treinar um agente que resiste a entradas manipuladas? |
| Imitation learning | Aprender copiando demonstrações de um especialista, em vez de explorar sozinho | Quantas demonstrações boas bastam para um agente imitar um especialista? |

**Leitura introdutória:** [Multiagent Systems: A Survey from a Machine Learning
Perspective](https://jmvidal.cse.sc.edu/library/stone00a.pdf), de Peter Stone e Manuela Veloso
(Autonomous Robots, 2000). `[Material: guia AAMAS 2027 (gerado por IA)]`

Identificação: DOI [10.1023/A:1008942012299](https://doi.org/10.1023/A:1008942012299). Chave
`stone2000multiagent` em [referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** foi escrita como introdução ao campo de SMA do ponto de vista de Machine
  Learning. Organiza os sistemas por dois eixos simples: se os agentes são iguais ou
  diferentes, e quanto eles se comunicam.
- **O que ler primeiro:** introdução e a seção que apresenta essa organização.
- **Atenção:** é anterior ao deep learning; vale pelos conceitos, não pelos métodos.
- **Complemento:** capítulo 1 do livro *Reinforcement Learning: An Introduction*, de Sutton e
  Barto, disponível gratuitamente no site dos autores. Não tem matemática.

Conferência:

- `[A verificar]` Que o capítulo 1 de Sutton & Barto "não tem matemática".

Minhas anotações: [areas/learn.md](areas/learn.md).

## GAAI — Generative and Agentic AI

Estuda agentes e sistemas multiagentes que **dependem de modelos generativos** (LLMs, SLMs,
modelos multimodais) para agir, raciocinar, interagir e decidir. É a área mais nova da chamada
e a mais próxima do projeto do PDC. `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando a contribuição central é sobre agentes cujas capacidades
dependem substancialmente de modelos generativos. Avanços só no modelo de linguagem, engenharia
de prompt, uso genérico de ferramentas ou tarefas generativas quaisquer ficam **fora** do
escopo, a menos que contribuam claramente para agentes. Se o núcleo for um método geral de
aprendizado, planejamento, engenharia ou interação humana, vai para a área correspondente.
`[Material: guia AAMAS 2027 (gerado por IA)]`

Texto da chamada:

> Papers should be submitted to GAAI when the central technical contribution concerns agents
> whose capabilities, architecture, reasoning, interaction, learning, evaluation, or deployment
> substantially rely on generative AI models. Papers whose main contribution is a general
> learning, planning, engineering, governance, or human-interaction method should instead be
> submitted to the corresponding AAMAS area, unless the generative-agent aspect is central.
>
> Submissions where the core contribution is not specifically about agents or multiagent
> systems are out of scope. Advances in language models, prompt engineering, generic tool use,
> or arbitrary generative tasks are outside the scope of this area unless they make a clear
> contribution to autonomous agents or multiagent systems.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Memory, state, context, long-lived interaction, and other architectural patterns for generative and agentic AI systems | Como o agente guarda e recupera informação além da janela de contexto e ao longo de muitas sessões (memória episódica, semântica, procedural) | O que o agente deve lembrar ou esquecer entre conversas? |
| Orchestration and workflows of agents and tools | Como se organiza quem faz o quê: pipeline fixo, supervisor/worker, hierarquia, agentes em paralelo | Quando vale ter vários agentes em vez de um só com as mesmas ferramentas? |
| Runtime support, infrastructure, and engineering for generative and agentic AI systems | A infraestrutura que executa agentes: estado, filas, isolamento, escalonamento (ideia de "LLM OS") | Como executar centenas de agentes com estado sem perder informação? |
| Embodied, multimodal, and grounded generative AI agents | Agentes que percebem e agem num ambiente (físico ou virtual) com imagens, áudio, sensores | Um agente consegue usar o que vê na tela para operar um aplicativo? |
| Open-ended, autonomous, and self-improving agents based on generative AI | Agentes que definem os próprios objetivos, exploram sem tarefa fixa ou melhoram a si mesmos com o tempo | Um agente consegue melhorar as próprias ferramentas sem supervisão? |
| Planning, reasoning, and long-horizon agentic workflows | Tarefas de muitos passos, em que pequenos erros se acumulam | Por que agentes falham mais à medida que a tarefa fica mais longa? |
| Agency and learning in generative and agentic AI | Como agentes generativos aprendem com experiência: fine-tuning com trajetórias, RL sobre LLMs, aprender a usar ferramentas | Treinar um SLM com trajetórias de sucesso reduz erros de chamada de ferramenta? |
| Interaction protocols for agentic AI | Padrões de comunicação agente–ferramenta e agente–agente (por exemplo, MCP e A2A) | Que garantias de segurança um protocolo de ferramentas precisa oferecer? |
| Coordination, cooperation, and negotiation in generative AI agents | Como agentes LLM dividem trabalho, cooperam ou negociam entre si | Agentes LLM conseguem chegar a um acordo justo numa negociação? |
| Normative reasoning and institutional constraints for generative AI agents | Fazer agentes respeitarem regras, normas e restrições de uma organização | Como garantir que o agente siga uma política interna mesmo sob pressão do usuário? |
| Theory of mind, user modeling, and social reasoning in generative AI agents | O agente modelar o que outros (pessoas ou agentes) sabem, querem ou acreditam | O agente percebe que o usuário entendeu errado e corrige? |
| Hybrid classic-generative agents, with a focus on how generative AI agents use classical tools, models, and protocols | Agentes LLM que usam componentes clássicos: planejadores, solvers, regras, arquiteturas BDI | Um planejador clássico verificando o plano do LLM aumenta a taxa de sucesso? |
| Failure handling, recovery, and resilience in agentic AI | Detectar que o agente errou, impedir que o erro se propague e se recuperar | Um agente consegue perceber que a ferramenta devolveu lixo e tentar de outro jeito? |
| Modeling and analysis of generative AI agents | Modelar formal ou empiricamente o comportamento de agentes para entendê-lo | Dá para prever em que tipo de tarefa um agente vai falhar? |
| Instruction following and multi-turn agent behavior in generative AI agents | Seguir instruções corretamente ao longo de muitas trocas de mensagem | O agente mantém as restrições dadas no início após 20 turnos? |
| Human-agent interaction for delegation, feedback, and task collaboration in generative AI agents | Como humanos delegam tarefas a agentes LLM, dão feedback e colaboram | Quando o agente deve pedir confirmação antes de agir? |
| Agentic decision support and decision boundaries | Agentes que apoiam decisões humanas e os limites do que podem decidir sozinhos | Que decisões nunca devem ser tomadas pelo agente sem um humano? |
| Alignment, learning from human feedback, and controllability of generative and agentic AI systems | Fazer o agente agir de acordo com intenções e valores humanos e permanecer controlável | Como garantir que o agente pare quando mandado parar? |
| Explainability, introspection, and debugging for generative AI agents and systems | Entender por que o agente fez algo e depurar suas decisões | Dá para rastrear qual passo da trajetória causou a resposta errada? |
| Assurance, verification, and safety in generative and agentic AI systems | Garantias sobre o comportamento: proteção contra prompt injection, ações proibidas, limites | Como impedir que um texto malicioso numa página faça o agente executar uma ação? |
| Benchmarks, evaluation, and metrics for generative and agentic AI systems | Como medir o desempenho de agentes: sucesso, custo, consistência, qualidade da trajetória | O agente acerta a mesma tarefa se rodar cinco vezes? |
| Generative AI-supported specification and implementation of agents and multiagent systems | Usar IA generativa para especificar ou programar outros agentes e SMAs | Um LLM consegue gerar um SMA correto a partir de uma descrição em texto? |
| Agentic AI applications in science, software, education, and critical domains | Aplicações de agentes generativos em domínios concretos, com ênfase no agente | Um agente consegue apoiar pesquisadores na revisão de literatura com segurança? |

**Leitura introdutória:** [A Survey on Large Language Model based Autonomous
Agents](https://arxiv.org/abs/2308.11432), de Lei Wang e colegas (Frontiers of Computer
Science, 2024). `[Material: guia AAMAS 2027 (gerado por IA)]`

Identificação: DOI [10.1007/s11704-024-40231-1](https://doi.org/10.1007/s11704-024-40231-1);
arXiv [2308.11432](https://arxiv.org/abs/2308.11432). Chave `wang2024survey` em
[referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** propõe um framework unificado para construir agentes com LLM e depois passa
  por aplicações e por como esses agentes são avaliados. Dá vocabulário para quase todos os
  subtópicos acima.
- **O que ler primeiro:** abstract, introdução e a seção de construção de agentes (perfil,
  memória, planejamento, ação).
- **Atenção:** é um survey de um campo que muda rápido; muitos trabalhos citados são preprints
  sem revisão por pares.

Conferência:

- `[A verificar]` Que GAAI é "a área mais nova da chamada".

Minhas anotações: [areas/gaai.md](areas/gaai.md).

## GTEP — Game Theory and Economic Paradigms

Estuda agentes que têm **interesses próprios e agem estrategicamente**: cada um tenta obter o
melhor resultado sabendo que os outros fazem o mesmo. Usa teoria dos jogos, economia e escolha
social para analisar e projetar essas interações. `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando o modelo estratégico, econômico, de teoria dos jogos ou
de escolha social é central. Se o foco for normas, instituições, ética ou governança, vai para
COINE, a menos que o modelo estratégico seja o centro. `[Material: guia AAMAS 2027 (gerado por
IA)]`

Texto da chamada:

> Papers should be submitted to GTEP when the strategic, economic, game-theoretic, or
> social-choice model is central to the contribution. Papers focused mainly on norms,
> institutions, ethics, or organizational governance should be submitted to COINE unless the
> strategic or economic model is central.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Auctions and mechanism design | Projetar as regras de uma interação (como um leilão) para que agentes egoístas produzam um bom resultado coletivo | Que regra de leilão faz os agentes revelarem quanto realmente valorizam o item? |
| Economic foundations and market design for economics of AI agents | Modelos econômicos para mercados em que agentes de IA compram, vendem ou contratam serviços | Como precificar serviços quando quem compra e vende são agentes? |
| Bargaining and negotiation | Dois ou mais agentes dividindo algo de valor e chegando (ou não) a um acordo | Que estratégia de negociação leva a acordos justos e rápidos? |
| Behavioural game theory | Como pessoas (ou agentes) jogam de fato, com vieses e racionalidade limitada, em vez do comportamento "ideal" | Agentes LLM jogam como humanos ou como a teoria prevê? |
| Evolutionary game theory | Estratégias que se espalham ou desaparecem numa população ao longo do tempo, como na evolução | A cooperação sobrevive numa população de agentes egoístas? |
| Non-cooperative games: equilibrium concepts | Definições de "estado estável" de um jogo, como o equilíbrio de Nash (ninguém ganha mudando sozinho de estratégia) | Que tipo de equilíbrio descreve melhor esta interação? |
| Non-cooperative games: computational issues | Quão difícil é calcular um equilíbrio e como fazer isso com algoritmos eficientes | Dá para encontrar o equilíbrio deste jogo em tempo razoável? |
| Non-cooperative games: theory and applications | Uso de jogos não cooperativos para modelar problemas reais (segurança, tráfego, mercados) | Como modelar patrulhas de segurança como um jogo contra um atacante? |
| Voting and preference aggregation | Combinar as preferências de muitos agentes numa decisão coletiva | Que regra de votação é mais resistente à manipulação? |
| Social choice and social networks | Decisões coletivas quando os agentes estão ligados por uma rede e se influenciam | Como a estrutura da rede altera o resultado de uma votação? |
| Judgment aggregation and forecasting | Combinar opiniões ou previsões de vários agentes numa resposta única e consistente | Como agregar previsões de vários modelos para errar menos? |
| Fair allocation and matching | Dividir recursos de forma justa e formar pares (alunos–escolas, médicos–hospitais) | Como dividir tarefas entre agentes sem que nenhum inveje a parte do outro? |
| Tournaments and agent evaluation | Comparar e ranquear agentes por meio de competições e torneios | Como ranquear agentes de forma justa quando cada um enfrentou adversários diferentes? |
| Digital and liquid democracy | Formas de votação digital, incluindo delegar o voto a outra pessoa de confiança | A delegação de votos melhora ou piora a qualidade das decisões? |
| Strategic coalition formation | Agentes egoístas decidindo com quem se aliar para ganhar mais | Que coalizões se formam quando cada agente busca o maior ganho próprio? |
| Cooperative games | Jogos em que grupos de agentes agem juntos e o problema é dividir o ganho do grupo | Como dividir o lucro de uma parceria de forma justa entre os membros? |
| Persuasion and information design | Escolher que informação revelar para influenciar a decisão de outro agente | Que informação uma plataforma deve mostrar para orientar o comportamento dos usuários? |

**Leitura introdutória:** [Multiagent Systems: Algorithmic, Game-Theoretic, and Logical
Foundations](https://masfoundations.org/), de Yoav Shoham e Kevin Leyton-Brown (Cambridge
University Press, 2009). É um livro, com versão em PDF gratuita para leitura no site dos
autores. `[Material: guia AAMAS 2027 (gerado por IA)]`

Identificação: Livro, Cambridge University Press; PDF gratuito em
[masfoundations.org](https://www.masfoundations.org/). Chave `shoham2009multiagent` em
[referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** cobre teoria dos jogos, escolha social, desenho de mecanismos e leilões com
  exemplos antes das provas. Também tem um apêndice com a base de probabilidade e MDPs.
- **O que ler primeiro:** a introdução e o capítulo inicial sobre jogos não cooperativos (jogos
  na forma normal e equilíbrio de Nash).
- **Atenção:** é rigoroso; pule as demonstrações na primeira leitura.

Conferência:

- `[A verificar]` Conteúdo do apêndice (probabilidade e MDPs) e qual é o "capítulo inicial
  sobre jogos não cooperativos".

Minhas anotações: [areas/gtep.md](areas/gtep.md).

## COINE — Coordination, Organizations, Institutions, Norms, and Ethics

Estuda o **lado social** dos sistemas multiagentes: como agentes coordenam trabalho, se
organizam em equipes e instituições, seguem normas, constroem confiança e agem de forma ética e
responsável. `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando as dimensões social, institucional, normativa,
organizacional, de governança ou ética são centrais. Estudos de interação com pessoas vão para
HAI; arquiteturas de agentes generativos vão para GAAI. `[Material: guia AAMAS 2027 (gerado por
IA)]`

Texto da chamada:

> Papers should be submitted to COINE when social, institutional, normative, organizational,
> governance, or ethical dimensions are central to the contribution. Papers focused primarily
> on human-subject interaction design or evaluation should be submitted to HAI; papers focused
> primarily on generative-agent architectures should be submitted to GAAI.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Coordination and teamwork | Como agentes combinam ações para atingir um objetivo comum sem se atrapalhar | Como agentes dividem uma tarefa sem duplicar trabalho? |
| Social network analysis | Analisar a rede de relações entre agentes (quem fala com quem, quem influencia quem) | Que agentes são centrais para o fluxo de informação no sistema? |
| Norms and normative systems | Regras de comportamento (obrigações, proibições, permissões) e como os agentes as seguem ou violam | Como um agente decide o que fazer quando duas normas entram em conflito? |
| Multiagent organizations and institutions | Estruturas formais (papéis, hierarquias, regras de grupo) que organizam o sistema | Como definir papéis e responsabilidades num SMA aberto? |
| Non-strategic coalition or team formation | Formar equipes de agentes cooperativos (sem interesse egoísta) para cumprir tarefas | Qual combinação de agentes forma a melhor equipe para uma tarefa? |
| Communication, including communication using natural language | Como agentes trocam mensagens, inclusive em linguagem natural | Que estrutura de mensagem reduz mal-entendidos entre agentes? |
| Policy, regulation, and accountability | Regras externas (leis, políticas) e como atribuir responsabilidade pelo que agentes fazem | Quem responde quando um sistema de agentes causa um dano? |
| Safety, robustness, trust, and reputation | Modelos de confiança e reputação entre agentes; o sistema continuar seguro se alguns agentes falharem | Como um agente decide em quem confiar quando outros podem errar ou mentir? |
| Ethical considerations, including bias, equity, fairness, privacy, safety, security, and transparency | Questões éticas no projeto e no comportamento dos agentes | O sistema trata grupos diferentes de usuários de forma justa? |
| Values and preferences | Representar valores humanos e preferências e fazer agentes agirem de acordo | Como um agente pondera valores conflitantes, como privacidade e utilidade? |
| Agreement technologies: negotiation and argumentation | Agentes chegando a acordos trocando propostas ou argumentos estruturados | Agentes conseguem resolver uma discordância trocando argumentos? |
| Responsible socio-technical systems | Sistemas que misturam pessoas e agentes e precisam ser responsáveis como um todo | Como projetar um sistema humano-agente que seja auditável? |
| Explainability and interpretability of norms and ethics in human-agent teams | Explicar a humanos por que o agente seguiu ou violou uma norma | O agente consegue justificar por que recusou uma ordem? |
| Ethical and governance challenges of LLM-based agents in coordination, organizations, institutions, and normative systems | Problemas éticos e de governança específicos de agentes LLM operando em grupo | Que mecanismos de governança evitam que agentes LLM conspirem para burlar uma regra? |
| Rebellion and disobedience in AI | Quando e como um agente deve recusar uma ordem (por exemplo, por ser antiética ou perigosa) | Em que situações é desejável que um agente desobedeça? |

**Leitura introdutória:** [Multi-Agent Systems: A
Survey](https://openaccess.library.uitm.edu.my/Record/doaj-c0be898bdea54259bc13171be6109dc9),
de Ali Dorri, Salil Kanhere e Raja Jurdak (IEEE Access, 2018), em acesso aberto. `[Material:
guia AAMAS 2027 (gerado por IA)]`

Identificação: DOI [10.1109/ACCESS.2018.2831228](https://doi.org/10.1109/ACCESS.2018.2831228).
Chave `dorri2018multiagent` em [referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** visão geral acessível de SMA, incluindo como agentes se organizam e
  coordenam, sem exigir base formal.
- **O que ler primeiro:** introdução e as seções sobre características e organização de SMAs.
- **Atenção:** é amplo; não aprofunda normas, confiança ou ética. Se um desses subtópicos te
  atrair, peça uma leitura específica.

Minhas anotações: [areas/coine.md](areas/coine.md).

## SOPS — Search, Optimization, Planning, and Scheduling

Estuda **algoritmos para decidir o que fazer e em que ordem**: buscar soluções num espaço de
possibilidades, otimizar sob restrições, montar planos de ação e agendar tarefas no tempo.
Atenção: *Search* aqui é **busca algorítmica**, não "pesquisa científica". `[Material: guia
AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando a contribuição principal é um método de busca,
otimização, planejamento, agendamento ou teoria da decisão, mesmo que aplicado a robôs, humanos
ou com apoio de LLMs (modelos de fundação). `[Material: guia AAMAS 2027 (gerado por IA)]`

Texto da chamada:

> Papers should be submitted to SOPS when the primary contribution is a search, optimization,
> planning, scheduling, or decision-theoretic method, even if the method is applied to
> multiagent, robotic, human-aware, or foundation-model-assisted settings.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Single-agent planning and scheduling | Um agente encontrando a sequência de ações que leva ao objetivo e organizando-a no tempo | Qual a sequência mínima de ações para completar a tarefa? |
| Multiagent planning and scheduling | Planejar ações de vários agentes ao mesmo tempo, evitando conflitos | Como planejar rotas de vários robôs sem colisões? |
| Decentralized planning and scheduling | Cada agente planeja com informação local, sem um planejador central | Agentes conseguem se coordenar sem um controlador central? |
| Planning under uncertainty | Planejar quando os efeitos das ações são incertos ou o estado não é totalmente observável | Como planejar quando uma ação pode falhar com 20% de chance? |
| Decision-theoretic planning | Planejar maximizando a utilidade esperada, com modelos como MDPs e POMDPs | Qual política maximiza o ganho esperado a longo prazo? |
| Temporal reasoning and scheduling | Lidar com prazos, durações e ordem temporal entre tarefas | Como agendar tarefas com prazos e dependências entre si? |
| Combinatorial optimization | Escolher a melhor combinação entre um número enorme de opções discretas | Qual a melhor forma de distribuir 100 tarefas entre 10 agentes? |
| Constraint programming | Resolver problemas descrevendo restrições que a solução deve satisfazer | Existe uma escala de trabalho que respeite todas as restrições? |
| Distributed constraint reasoning | Vários agentes resolvem juntos um problema de restrições, cada um com uma parte | Como agentes acham uma solução comum sem revelar todos os seus dados? |
| Resource and task allocation | Decidir que agente recebe qual tarefa ou recurso | Que subtarefa deve ir para um modelo pequeno e qual exige um modelo grande? |
| Non-strategic coalition formation | Agrupar agentes cooperativos para executar tarefas da melhor forma | Que grupos de agentes cumprem o conjunto de tarefas mais rápido? |
| Plan and goal recognition | Inferir o objetivo ou o plano de outro agente observando suas ações | Observando as ações de um usuário, dá para prever o que ele quer fazer? |
| Human-aware planning and scheduling | Planejar levando em conta pessoas: suas preferências, expectativas e o que conseguem entender | Como gerar planos que um humano consiga acompanhar e confiar? |
| Knowledge representation methods for search, optimization, planning, and scheduling | Formas de representar o problema que tornam a busca ou o planejamento mais eficientes | Que representação do domínio deixa o planejador mais rápido? |

**Leitura introdutória:** [Multi-Agent Pathfinding: Definitions, Variants, and
Benchmarks](https://ojs.aaai.org/index.php/SOCS/article/view/18510), de Roni Stern e colegas
(SoCS, 2019). `[Material: guia AAMAS 2027 (gerado por IA)]`

Identificação: DOI [10.1609/socs.v10i1.18510](https://doi.org/10.1609/socs.v10i1.18510). Chave
`stern2019mapf` em [referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** apresenta um problema clássico de planejamento multiagente, planejar rotas
  de vários agentes sem colisão, com terminologia unificada e figuras claras. Dois dos autores,
  Roni Stern e Nathan Sturtevant, são chairs da área SOPS da AAMAS 2027.
- **O que ler primeiro:** introdução e a definição do problema clássico com os tipos de
  conflito.
- **Atenção:** foca em um único problema; serve para entender como a área formula e compara
  métodos.

Conferência:

- Conferido: Stern e Sturtevant são coautores (Crossref) e estão entre os chairs da área SOPS
  (chamada).

Minhas anotações: [areas/sops.md](areas/sops.md).

## RR — Representation and Reasoning

Estuda como **representar formalmente o que um agente sabe, acredita e quer**, e como
raciocinar sobre isso de forma rigorosa, geralmente com lógica. Inclui a verificação formal:
provar matematicamente que um sistema se comporta como deveria. `[Material: guia AAMAS 2027
(gerado por IA)]`

**Quando vai para esta área:** quando a contribuição principal é um formalismo, método ou
análise de representação ou raciocínio para agentes. Se o núcleo for planejamento ou
otimização, vai para SOPS, salvo se o formalismo for central. `[Material: guia AAMAS 2027
(gerado por IA)]`

Texto da chamada:

> Papers should be submitted to RR when the primary contribution is a representation or
> reasoning framework, method, analysis, or formalism for agents or multiagent systems. Papers
> whose primary contribution is planning, scheduling, or optimization should be submitted to
> SOPS, unless the representation or reasoning formalism is central.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Neurosymbolic approaches | Combinar redes neurais (aprendem com dados) com raciocínio simbólico (regras e lógica explícitas) | Um LLM com um verificador lógico erra menos em raciocínio? |
| Argumentation | Representar argumentos e contra-argumentos e decidir quais "vencem" | Como um agente decide entre duas conclusões conflitantes com base em argumentos? |
| Agent theories and models | Teorias formais do que é um agente e de como ele funciona (por exemplo, o modelo BDI: crenças, desejos, intenções) | Que modelo formal descreve bem um agente baseado em LLM? |
| Explainability | Gerar explicações sobre o raciocínio e as decisões do agente | Como explicar por que o agente escolheu este plano e não outro? |
| Logics for agent reasoning | Lógicas especiais para falar de conhecimento, crença, tempo, obrigação e ação | Que lógica captura "o agente sabe que o outro não sabe"? |
| Ontologies for agents | Vocabulários formais de conceitos e relações de um domínio, compartilhados entre agentes | Como dois agentes de origens diferentes passam a entender os mesmos termos? |
| Reasoning about knowledge, beliefs, goals, actions, plans, and change in multiagent systems | Raciocinar sobre o estado mental próprio e dos outros e sobre como o mundo muda com as ações | Como um agente atualiza suas crenças quando recebe informação contraditória? |
| Reasoning and problem solving in agent-based systems | Técnicas gerais de raciocínio e resolução de problemas aplicadas a agentes | Como um agente resolve um problema dividindo-o em subproblemas? |
| Verification of agents and multiagent systems | Provar (ou testar exaustivamente) que o sistema satisfaz uma propriedade, como "nunca executa ação proibida" | Dá para garantir que este SMA nunca entra num estado inseguro? |
| Autoformalization | Traduzir automaticamente texto em linguagem natural para uma representação formal (lógica, código) | Um LLM consegue transformar uma regra escrita em português numa fórmula lógica correta? |
| Logic-constrained learning | Aprendizado de máquina obrigado a respeitar regras lógicas conhecidas | Como treinar um modelo que nunca viole uma restrição conhecida? |
| Strategic reasoning and strategy logics | Lógicas para raciocinar sobre o que agentes conseguem garantir agindo estrategicamente | Este grupo de agentes consegue garantir o objetivo, não importa o que os outros façam? |

**Leitura introdutória:** [BDI Agents: From Theory to
Practice](https://apice.unibo.it/xwiki/bin/view/Publication/BdiIcmas95?language=), de Anand Rao
e Michael Georgeff (ICMAS, 1995). `[Material: guia AAMAS 2027 (gerado por IA)]`

Identificação: ICMAS 1995, pp. 312–319. Chave `rao1995bdi` em
[referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** texto clássico e curto (8 páginas) que liga a teoria de agentes com
  crenças, desejos e intenções à sua implementação, usando uma aplicação de controle de tráfego
  aéreo como exemplo.
- **O que ler primeiro:** introdução e a parte que explica por que os três estados mentais são
  necessários.
- **Atenção:** tem trechos de lógica formal; pule-os na primeira leitura.

Conferência:

- Conferido: pp. 312–319 nos anais, ou seja, 8 páginas (página da publicação no APICe/Unibo).

Minhas anotações: [areas/rr.md](areas/rr.md).

## EMAS — Engineering and Analysis of Multiagent Systems

Estuda **como construir, testar, implantar e manter** agentes e sistemas multiagentes como
software. A pergunta central não é "o agente é inteligente?", e sim "como garanto que este
sistema funciona e continua funcionando?". `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando a contribuição principal são métodos, ferramentas,
linguagens, plataformas ou processos para engenharia de agentes. Se o LLM faz a tarefa
principal e a engenharia de SMA é só pano de fundo, o artigo vai para outra área. `[Material:
guia AAMAS 2027 (gerado por IA)]`

Texto da chamada:

> Papers should be submitted to EMAS when the primary contribution concerns methods, tools,
> languages, platforms, infrastructures, or processes for engineering, deploying, testing,
> validating, maintaining, or analyzing agent and multiagent systems. Papers in which LLMs or
> other AI technologies perform the primary task while MAS engineering plays only a background
> role should be submitted to another area.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Requirements capture and formal specification of multiagent systems | Levantar e escrever, de forma precisa, o que o sistema deve fazer | Como especificar o comportamento esperado de um SMA antes de implementá-lo? |
| Programming paradigms and languages for autonomous agents | Linguagens e estilos de programação feitos para agentes (por exemplo, Jason, baseada em BDI) | Que abstrações de programação tornam agentes mais fáceis de escrever? |
| Runtime infrastructures and deployment platforms for scalable MAS, including cloud, edge, and hybrid settings | Plataformas que executam muitos agentes na nuvem, na borda ou em ambientes mistos | Como rodar um SMA parte num servidor e parte num dispositivo local? |
| Testing, debugging, verification, validation, certification, and DevOps for multiagent systems | Como testar e depurar sistemas não determinísticos e manter um ciclo de entrega contínua (inclui AgentOps) | Como escrever testes automatizados para um agente que responde diferente a cada execução? |
| Scalability, fault tolerance, and performance engineering of MAS platforms | O sistema aguentar crescer e continuar funcionando quando partes falham | O que acontece com o SMA se um agente trava no meio da tarefa? |
| Engineering self-adaptive agents, including lifecycle management, continuous evolution, and deployment pipelines | Agentes que mudam de comportamento em produção, e como gerenciar isso com segurança | Como atualizar um agente em produção sem quebrar o resto do sistema? |
| Interoperability, business agreements, and agent-to-agent protocols | Agentes de fornecedores diferentes conseguirem trabalhar juntos | Como dois agentes de empresas diferentes negociam um contrato de serviço? |
| Declarative, logic-based, and BDI agent programming and architectures | Programar agentes descrevendo crenças, objetivos e planos em vez de código passo a passo | Uma arquitetura BDI torna um agente LLM mais previsível? |
| Engineering MAS-based simulations for rigorous analysis and experimentation | Construir simulações com agentes que sirvam de experimento confiável | Como garantir que uma simulação com agentes seja reproduzível? |
| Sociotechnical governance tools for norms, ethics, and accountability | Ferramentas de software para aplicar e auditar regras e responsabilidade | Como registrar automaticamente quem (ou que agente) decidiu cada ação? |
| Human-centered engineering for usability, transparency, and explainability | Projetar o sistema para que pessoas consigam usá-lo e entender o que ele faz | Como mostrar ao usuário o que o SMA está fazendo em tempo real? |
| Open-source toolchains, benchmarks, and reproducible MAS testbeds | Ferramentas abertas e ambientes de teste padronizados para comparar sistemas | Existe um ambiente aberto para comparar SMAs de forma justa? |
| Engineering learning agents, including platform design and online adaptation | Infraestrutura para agentes que aprendem durante a operação | Como monitorar um agente que continua aprendendo depois de implantado? |
| Engineering MAS with LLM methods | Usar LLMs como componentes ou ferramentas na engenharia de SMAs | Onde, num SMA, um LLM deve entrar e onde não deve? |
| Hybrid symbolic-subsymbolic agent systems, including engineering architectures and platforms for neurosymbolic reasoning | Plataformas que juntam componentes simbólicos (regras, lógica) e aprendidos (redes neurais) | Como integrar um planejador simbólico com um LLM numa mesma arquitetura? |
| Benchmarks, evaluation methodologies, and reproducible workflows for MAS | Métodos para avaliar SMAs de forma comparável e repetível | Como relatar resultados de SMA de modo que outro grupo consiga reproduzir? |
| Data-driven engineering processes for design, testing, and adaptation of agent systems | Usar dados de execução (logs, traces) para melhorar projeto e testes | Os logs de falhas em produção podem gerar novos casos de teste automaticamente? |
| Engineering MAS-based autonomous systems | Engenharia de sistemas autônomos completos construídos como SMA | Como certificar um sistema autônomo composto por vários agentes? |

**Leitura introdutória:** [Agent Programming in the Cognitive
Era](https://repositorio.pucrs.br/dspace/handle/10923/20079), de Rafael Bordini e colegas
(Autonomous Agents and Multi-Agent Systems, 2020), com PDF no repositório da PUCRS. `[Material:
guia AAMAS 2027 (gerado por IA)]`

Identificação: DOI [10.1007/s10458-020-09453-y](https://doi.org/10.1007/s10458-020-09453-y).
Chave `bordini2020agent` em [referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** revisa a programação de agentes baseada em BDI e discute formas de integrar
  técnicas de IA e Machine Learning a esses agentes. É uma ponte direta entre o EMAS clássico e
  os agentes com LLM.
- **O que ler primeiro:** abstract, introdução e a parte que lista as formas de integrar IA a
  agentes BDI.
- **Contexto:** o primeiro autor é da PUCRS e um dos criadores da linguagem Jason, mostrando a
  tradição brasileira nesta área.

Conferência:

- `[A verificar]` Afiliação do primeiro autor (PUCRS) e o papel dele na criação da linguagem
  Jason.

Minhas anotações: [areas/emas.md](areas/emas.md).

## SIM — Modeling and Simulation of Artificial Societies

Estuda **simulações computacionais com muitos agentes** para entender como comportamentos
individuais geram padrões coletivos (o chamado comportamento emergente) em sociedades,
economias, ecossistemas, tráfego e organizações. Aqui o agente é um instrumento para estudar um
sistema complexo. `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando a simulação é central, seja como avanço de método, seja
como forma de explicar, prever ou avaliar um sistema complexo. A chamada cita ecologia e
biologia entre as aplicações. `[Material: guia AAMAS 2027 (gerado por IA)]`

Texto da chamada:

> Papers should be submitted to SIM when simulation is central to the contribution, either as a
> methodological advance or as a way to explain, predict, explore, or evaluate complex systems.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Modeling for agent-based simulation | Como definir os agentes, suas regras e o ambiente de uma simulação | Que regras individuais reproduzem o padrão observado na realidade? |
| Simulation of complex systems | Simular sistemas com muitas partes interagindo, em que o todo não é a soma das partes | Pequenas mudanças de comportamento individual causam grandes mudanças coletivas? |
| Modeling of societies and social simulations | Simular grupos humanos: opinião, cultura, cooperação, conflito | Como uma informação falsa se espalha numa população simulada? |
| Agent-based modeling and evaluation of public policies | Testar políticas públicas numa simulação antes de aplicá-las | Que política de vacinação reduz mais a transmissão na simulação? |
| Simulation techniques, tools, and platforms | Ferramentas e plataformas para construir e rodar simulações (por exemplo, NetLogo, Mesa) | Que plataforma permite simular milhões de agentes? |
| Analysis of agent-based simulations | Métodos para analisar e interpretar os resultados de uma simulação | Como saber que um padrão vem do modelo e não do acaso? |
| Calibration, verification, and validation of agent-based simulation systems | Ajustar parâmetros com dados reais e verificar se a simulação representa bem a realidade | Como provar que esta simulação é fiel ao sistema real? |
| Robustness, reliability, and trustworthiness of agent-based simulations | Garantir que as conclusões não mudem com pequenas alterações de parâmetros | A conclusão se mantém se mudarmos os parâmetros em 10%? |
| Design and implementation of large-scale agent-based simulations | Construir simulações com muitíssimos agentes de forma eficiente | Como simular uma cidade inteira com um agente por habitante? |
| High-performance computing and frameworks for agent-based simulation | Usar computação paralela, GPUs e clusters para acelerar simulações | Como paralelizar uma simulação sem perder a interação entre agentes? |
| Interactive and participatory simulation | Simulações em que pessoas participam ou interagem com os agentes | Gestores aprendem mais jogando uma simulação do que lendo um relatório? |
| LLM-supported agent-based simulation and modeling | Usar LLMs para dar comportamento mais realista aos agentes simulados ou ajudar a construir o modelo | Agentes guiados por LLM reproduzem comportamento humano melhor que regras fixas? |

**Leitura introdutória:** [Tutorial on agent-based modelling and
simulation](https://econpapers.repec.org/RePEc:taf:tjsmxx:v:4:y:2010:i:3:p:151-162), de Charles
Macal e Michael North (Journal of Simulation, 2010). `[Material: guia AAMAS 2027 (gerado por
IA)]`

Identificação: DOI [10.1057/jos.2010.3](https://doi.org/10.1057/jos.2010.3). Chave
`macal2010tutorial` em [referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** é literalmente um tutorial. Explica os conceitos básicos de modelagem
  baseada em agentes, mostra aplicações em várias disciplinas e apresenta ferramentas para
  construir modelos.
- **O que ler primeiro:** a parte de conceitos e a estrutura de um modelo baseado em agentes.
- **Atenção:** a versão do periódico tem acesso restrito. Os mesmos autores publicaram
  tutoriais introdutórios parecidos na Winter Simulation Conference (por exemplo, 2005, 2013 e
  2014), que costumam ser mais fáceis de encontrar abertos.

Conferência:

- `[A verificar]` Anos dos tutoriais na Winter Simulation Conference (2005, 2013, 2014) e se
  estão em acesso aberto.

Minhas anotações: [areas/sim.md](areas/sim.md).

## HAI — Human-Agent Interaction

Estuda **como pessoas e agentes interagem e trabalham juntos**: confiança, explicações, divisão
de controle e como o agente percebe e modela o humano. Muitos trabalhos da área avaliam o
sistema com estudos com usuários. `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando a interação humano-agente é central na pergunta, no
método ou na avaliação. Aspectos institucionais ou de governança vão para COINE; arquiteturas
de agentes generativos vão para GAAI. `[Material: guia AAMAS 2027 (gerado por IA)]`

Texto da chamada:

> Papers should be submitted to HAI when human-agent interaction is central to the research
> question, methodology, or evaluation. Papers focused primarily on institutional, normative,
> or governance aspects should be submitted to COINE; papers focused primarily on
> generative-agent architectures should be submitted to GAAI.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Human-agent interaction | O campo geral de como humanos e agentes se comunicam e colaboram | Que forma de interação deixa o usuário mais eficiente com o agente? |
| Agent-based analysis of human interactions | Usar agentes ou modelos de agentes para analisar como pessoas interagem entre si | Um modelo de agentes explica padrões de conversa em equipes humanas? |
| Socially interactive agents | Agentes que interagem de forma social (conversa, emoção, empatia) | Um agente que demonstra empatia melhora a adesão do usuário? |
| Trust and explainability in human-agent interactions | Fazer a confiança do humano corresponder à real capacidade do agente, e explicar decisões | Explicações fazem o usuário confiar mais, ou confiar melhor (só quando deve)? |
| Human-robot interaction and collaboration | Pessoas e robôs físicos trabalhando juntos | Como um robô sinaliza o que vai fazer para não assustar quem está perto? |
| Social robotics and social interactions | Robôs projetados para interação social (educação, cuidado, companhia) | Um robô social ajuda crianças a aprender um conteúdo? |
| Mixed-initiative and shared autonomy in human-agent interactions | Divisão de controle: quando o agente age sozinho, quando pergunta, quando o humano assume | Em que momento o agente deve parar e pedir confirmação? |
| Groups of humans and agents | Equipes mistas com várias pessoas e vários agentes | Como um agente deve se comportar numa reunião com várias pessoas? |
| Agent models and architectures for interaction with humans | Arquiteturas de agente feitas especificamente para interagir com pessoas | Que componentes um agente precisa para acompanhar o estado do usuário? |
| Design for human-agent interaction | Métodos de design de interfaces e interações com agentes | Como projetar a interface para o usuário perceber que está falando com um agente? |
| Virtual humans | Personagens digitais com aparência e comportamento humanos | Um tutor virtual com rosto é mais eficaz que um só por texto? |
| Theory of mind and user modeling in human-agent interaction | O agente inferir o que o humano sabe, quer ou sente | O agente percebe que o usuário está confuso e muda a explicação? |
| Modelling, detecting, and accounting for deception in human-AI teams | Lidar com engano em equipes humano-IA, venha do humano ou do agente | Como detectar que um agente está enganando o usuário? |
| Human cognitive modeling for agent interaction | Modelos de como as pessoas pensam (atenção, memória, carga cognitiva) usados pelo agente | O agente pode ajustar o volume de informação à carga cognitiva do usuário? |

**Leitura introdutória:** [Guidelines for Human-AI
Interaction](https://www.microsoft.com/research/publication/guidelines-for-human-ai-interaction/),
de Saleema Amershi e colegas (CHI, 2019). `[Material: guia AAMAS 2027 (gerado por IA)]`

Identificação: DOI [10.1145/3290605.3300233](https://doi.org/10.1145/3290605.3300233). Chave
`amershi2019guidelines` em [referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** propõe 18 diretrizes de como um sistema de IA deve se comportar com
  pessoas, agrupadas em quatro momentos: no primeiro contato, durante o uso, quando erra e ao
  longo do tempo. Mostra também como a área valida propostas com estudos envolvendo
  profissionais.
- **O que ler primeiro:** a tabela com as 18 diretrizes e a seção de validação.
- **Atenção:** trata de produtos com IA em geral, não especificamente de agentes autônomos.

Conferência:

- `[A verificar]` Número de diretrizes (18) e os quatro momentos em que são agrupadas.

Minhas anotações: [areas/hai.md](areas/hai.md).

## ROBOT — Robotics and Control

Estuda **robôs como agentes**: entidades com corpo, situadas no mundo físico, que precisam
perceber, raciocinar, planejar, aprender e agir de forma autônoma, sozinhas ou em equipes de
robôs. `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando a contribuição principal é sobre robôs autônomos,
sistemas multirrobô ou a interação de robôs com pessoas, agentes de software ou o ambiente
físico. Percepção, mapeamento ou controle entram quando contribuem claramente para robôs
autônomos. `[Material: guia AAMAS 2027 (gerado por IA)]`

Texto da chamada:

> This area welcomes papers whose primary contribution concerns autonomous robots, robotic
> agents, multi-robot systems, or the interaction of robots with humans, software agents, or
> physical environments. Relevant submissions include work on coordination, collaboration,
> swarms, distributed robotics, robot planning, robot learning, knowledge representation and
> reasoning for robots, long-term autonomy, execution monitoring, failure recovery, modeling
> and simulation, explainability, trust, ethics, decision-making, and control for autonomous
> robots.
>
> Submissions involving perception, vision, mapping, localization, manipulation, or control are
> welcome when these components are integrated into, or make a clear contribution to,
> autonomous robots or multi-robot systems.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Coordination and collaboration in robotic systems | Robôs combinando ações para cumprir uma tarefa juntos | Como dois braços robóticos carregam um objeto sem derrubá-lo? |
| Swarm and multi-robot collective behavior | Muitos robôs simples cujo comportamento coletivo emerge de regras locais, como um enxame | Regras simples fazem um enxame de drones cobrir uma área inteira? |
| Robots in adversarial settings | Robôs operando contra oponentes ou em ambientes hostis | Como um robô de patrulha se adapta a um invasor que aprende sua rotina? |
| Perception and vision for autonomous robots | Interpretar câmeras e sensores para entender o ambiente | Como o robô reconhece objetos com iluminação ruim? |
| Networked systems and distributed robotics | Robôs conectados em rede, compartilhando informação e decisões | Como robôs mantêm coordenação quando a comunicação falha? |
| Foundation models for autonomous robots and robot teams | Usar LLMs e modelos multimodais grandes para controlar ou planejar ações de robôs | Um robô consegue executar uma instrução em linguagem natural com segurança? |
| Knowledge representation and reasoning in robotic systems | Representar e raciocinar sobre o mundo físico (objetos, lugares, relações) | Como o robô sabe que a xícara está dentro do armário fechado? |
| Robot planning and decision-making | Decidir que ações o robô deve executar para atingir um objetivo | Em que ordem o robô deve executar as tarefas de uma casa? |
| Mapping, localization, and navigation for autonomous robots and robot teams | Construir um mapa, saber onde está nele e se deslocar até um destino | Como o robô se localiza num prédio sem GPS? |
| Autonomous robot manipulation and task execution | Pegar, mover e usar objetos com mãos ou garras | Como o robô pega objetos frágeis de formatos variados? |
| Decision-making and control for autonomous robots and robot teams | Controlar o movimento do robô ou da equipe em tempo real | Como manter uma formação de robôs estável com vento? |
| Robot learning for autonomy and adaptation | Robôs aprendendo habilidades por demonstração, tentativa e erro ou simulação | Uma habilidade aprendida em simulação funciona no robô real? |
| Long-term or lifelong autonomy for robotic systems | Robôs operando por semanas ou meses sem intervenção, adaptando-se a mudanças | Como o robô continua útil depois que o ambiente muda? |
| Execution monitoring and failure recovery for robots | Perceber que algo deu errado durante a execução e se recuperar | O robô percebe que deixou cair o objeto e tenta de novo? |
| Robot modeling and simulation for autonomous agents | Simular robôs e ambientes para testar e treinar antes do mundo real | Que diferenças entre a simulação e a realidade mais atrapalham? |
| Explainability, trust, and ethics for robots | Robôs explicáveis, confiáveis e que agem de forma ética | Como um robô explica por que parou de repente? |
| Hybrid systems of robots with humans and/or software agents | Sistemas que misturam robôs, pessoas e agentes de software | Como um agente de software coordena robôs e operadores humanos? |

**Leitura introdutória:** [Do As I Can, Not As I Say: Grounding Language in Robotic
Affordances](https://arxiv.org/abs/2204.01691), de Michael Ahn e colegas (CoRL, 2022),
conhecido como SayCan. `[Material: guia AAMAS 2027 (gerado por IA)]`

Identificação: arXiv [2204.01691](https://arxiv.org/abs/2204.01691); anais: PMLR 205, pp.
287–318. Chave `ahn2022saycan` em [referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** é uma ponte natural para quem vem de LLMs. O modelo de linguagem sugere
  passos de alto nível, e funções de valor de habilidades pré-treinadas dizem o que o robô de
  fato consegue fazer naquele ambiente.
- **O que ler primeiro:** abstract, introdução e a figura que explica a combinação "o que o LLM
  sugere" × "o que o robô consegue".
- **Atenção:** é um único sistema de um laboratório grande; não representa a área de robótica
  como um todo.

Conferência:

- `[A verificar]` Nos anais da CoRL (PMLR 205) o primeiro autor listado é Brian Ichter, não
  Michael Ahn; o arXiv lista Ahn primeiro. Decidir como citar.

Minhas anotações: [areas/robot.md](areas/robot.md).

## IASI — Innovative Applications and Societal Impact

Estuda **aplicações reais de agentes e o impacto que elas geram**. A contribuição não é um
algoritmo novo, e sim mostrar que agentes resolvem um problema concreto, com evidência de
benefício, viabilidade ou adoção. `[Material: guia AAMAS 2027 (gerado por IA)]`

**Quando vai para esta área:** quando a contribuição principal é a aplicação, a implantação, a
validação realista, o design com as partes interessadas ou o impacto social demonstrado. Se o
núcleo for um algoritmo, arquitetura, ferramenta ou método de simulação novo, vai para a área
técnica correspondente. A chamada pede que o artigo explique o contexto, o papel dos agentes, a
novidade e a evidência de impacto, e incentiva parcerias com quem vai usar o sistema.
`[Material: guia AAMAS 2027 (gerado por IA)]`

Texto da chamada:

> Submissions should clearly explain the application context, the role of agents, the novelty
> of the application, and the evidence of benefit, feasibility, adoption, or measurable impact.
> Collaborations with relevant stakeholders are strongly encouraged, especially where they
> demonstrate that the proposed approach addresses a real need and can be used, evaluated, or
> deployed in practice.
>
> Papers should be submitted to IASI when the primary contribution is an innovative
> application, deployment, realistic validation, stakeholder-driven design, or demonstrated
> societal impact of agent-based or agentic technologies. Papers whose primary contribution is
> a new algorithm, architecture, learning method, engineering tool, or simulation method should
> be submitted to the corresponding technical area unless the application or impact
> contribution is central.
> `[Material: chamada AAMAS 2027]`

Nomes dos subtópicos: `[Material: chamada AAMAS 2027]`. Colunas "O que é" e "Exemplo de
pergunta": `[Material: guia AAMAS 2027 (gerado por IA)]`.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Deployed or emerging applications of agent-based and agentic systems addressing real-world challenges | Sistemas de agentes já em uso ou prestes a ser usados em problemas reais | O sistema de agentes reduziu o tempo de atendimento depois de implantado? |
| Agent-based and agentic systems for social good, sustainability, public policy, education, health, science, industry, and critical domains | Aplicações em áreas de impacto social e domínios críticos | Agentes conseguem apoiar o monitoramento de espécies ameaçadas? |
| Realistic agent-based and agentic models of human organizations, institutions, and socio-technical systems | Modelos de agentes realistas o bastante para representar organizações reais | O modelo reproduz o funcionamento real de um órgão público? |
| Evaluation of the cognitive, social, organizational, or decision-support capabilities of agent-based and agentic systems in real-world settings | Avaliar agentes no mundo real, não só em benchmarks de laboratório | O agente ajuda de fato os profissionais a tomar decisões melhores no dia a dia? |
| Integration of agent-based and agentic systems with other AI, software, cyber-physical, robotic, simulation, or decision-support technologies | Juntar agentes com outros sistemas já existentes numa organização | Como integrar um agente aos sistemas legados de uma instituição? |
| Hybrid agent-based, agentic AI, and reinforcement learning solutions for real-world applications | Soluções reais que combinam simulação com agentes, agentes LLM e RL | Uma combinação de simulação e RL otimiza a logística de uma rede real? |
| Deployment, adoption, usability, robustness, safety, and maintainability of agent-based and agentic technologies in practice | O que acontece quando o sistema sai do protótipo: uso, manutenção, falhas reais | Por que usuários abandonam um agente depois de algumas semanas? |
| Challenges, best practices, and lessons learned from real-world deployments of agent-based and agentic technologies | Relatos sistemáticos do que deu certo e errado ao implantar agentes | Quais problemas só apareceram depois que o sistema entrou em produção? |
| Evaluation methodologies, benchmarks, and evidence of measurable impact for innovative applications | Como medir o impacto real de uma aplicação | Que métrica mostra que a aplicação trouxe benefício, e não só que funciona? |
| Stakeholder involvement, participatory design, and co-creation of agent-based and agentic applications | Construir a aplicação junto com quem vai usá-la | Envolver os usuários desde o início muda o que o sistema deve fazer? |
| Ethical, legal, societal, and environmental implications of deployed or emerging agent-based and agentic systems | Efeitos éticos, legais, sociais e ambientais de sistemas implantados | Qual o custo energético de manter este sistema de agentes rodando? |
| Frameworks, platforms, and tools supporting the implementation and deployment of innovative agent-based and agentic applications | Ferramentas que facilitam construir e implantar aplicações com agentes | Que plataforma permite a uma instituição pequena implantar agentes localmente? |

**Leitura introdutória:** [Using Game Theory for Los Angeles Airport
Security](https://ojs.aaai.org/index.php/aimagazine/article/view/2173), de James Pita e colegas
(AI Magazine, 2009). `[Material: guia AAMAS 2027 (gerado por IA)]`

Identificação: DOI [10.1609/aimag.v30i1.2173](https://doi.org/10.1609/aimag.v30i1.2173). Chave
`pita2009armor` em [referencias.bib](../../referencias/referencias.bib).

Comentários do guia sobre a leitura: `[Material: guia AAMAS 2027 (gerado por IA)]`

- **Por que esta:** conta como um agente de software (ARMOR) foi implantado no aeroporto de Los
  Angeles a partir de 2007 para randomizar patrulhas e postos de controle. Mostra o que a IASI
  valoriza: necessidade real, parceria com quem usa o sistema e avaliação no mundo real.
- **O que ler primeiro:** a descrição do problema, as decisões de projeto e a parte de
  implantação e avaliação.
- **Atenção:** é a versão de divulgação, mais acessível, do artigo da trilha industrial da
  AAMAS 2008. O método por trás é de teoria dos jogos (GTEP); a contribuição destacada aqui é a
  aplicação.

Conferência:

- `[A verificar]` Ano de início da implantação (2007) e a relação com o artigo da trilha
  industrial da AAMAS 2008.

Minhas anotações: [areas/iasi.md](areas/iasi.md).

## Glossário do guia

Termos que aparecem em várias áreas, com definição simplificada. `[Material: guia AAMAS 2027
(gerado por IA)]`

Os termos que ainda não existiam foram levados para o [glossário](../../glossario.md), na seção
"Termos da exploração AAMAS 2027", com a coluna operacional em branco. *Agente*, *SMA* e *SLM*
já tinham definição própria, diferente desta, e no glossário ficaram como estavam.

| Termo | Significado simplificado | Onde aparece |
| --- | --- | --- |
| Agente | Entidade que percebe um ambiente e age nele para atingir objetivos, com algum grau de autonomia | Todas |
| Sistema multiagente (SMA / MAS) | Vários agentes interagindo num mesmo ambiente, cooperando ou competindo | Todas |
| LLM / SLM | Modelo de linguagem grande / pequeno (geralmente abaixo de cerca de 10 bilhões de parâmetros) `[A verificar]` | GAAI, EMAS, SIM |
| Modelo de fundação (foundation model) | Modelo grande pré-treinado em muitos dados e adaptável a várias tarefas; LLMs são um tipo | GAAI, SOPS, ROBOT |
| BDI | Modelo de agente baseado em crenças (Beliefs), desejos (Desires) e intenções (Intentions) | RR, EMAS |
| MDP | Processo de decisão de Markov: modelo matemático de estados, ações, transições e recompensas, base do RL | LEARN, SOPS |
| POMDP | MDP em que o agente não observa o estado completo, só pistas sobre ele | LEARN, SOPS |
| Política (policy) | Regra que diz que ação o agente toma em cada situação | LEARN, SOPS |
| Recompensa (reward) | Sinal numérico que diz ao agente o quão bom foi o que ele fez | LEARN |
| Equilíbrio de Nash | Situação de um jogo em que nenhum agente ganha mudando sozinho de estratégia | GTEP, LEARN |
| Mecanismo (mechanism design) | Regras de uma interação projetadas para levar agentes egoístas a um bom resultado | GTEP |
| Comportamento emergente | Padrão coletivo que surge da interação entre agentes e não foi programado diretamente | SIM, ROBOT, LEARN |
| Norma | Regra de comportamento: obrigação, proibição ou permissão | COINE, GAAI |
| Neurossimbólico | Combinação de aprendizado neural com raciocínio simbólico (regras, lógica) | RR, EMAS, GAAI |
| Verificação formal | Provar matematicamente que um sistema satisfaz uma propriedade | RR, EMAS, GAAI |
| Benchmark | Conjunto de tarefas padronizado para comparar sistemas de forma justa | GAAI, EMAS, IASI |
| Prompt injection | Texto malicioso que tenta fazer o modelo seguir instruções que não vieram do usuário | GAAI |
| RLHF | Aprendizado por reforço a partir de feedback humano, usado para alinhar LLMs | LEARN, GAAI |
| Mixed-initiative | Interação em que tanto o humano quanto o agente podem tomar a iniciativa | HAI, GAAI |
| AgentOps | Práticas e ferramentas para operar, monitorar e rastrear agentes em produção, por analogia a DevOps | EMAS, GAAI |
