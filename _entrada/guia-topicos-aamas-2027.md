# Guia dos tópicos da AAMAS 2027

Nov 5, 2026 · @Júlia Coité

## Como usar este guia

Este guia explica, em português simples, as 11 áreas e todos os subtópicos da [chamada da trilha principal da AAMAS 2027](https://warwick.ac.uk/fac/sci/dcs/aamas2027/calls/call-for-main-track/). Serve para a atividade de exploração do PDC: primeiro leia a descrição de cada área, marque as que despertam curiosidade e só então desça para os subtópicos.

- **Nomes dos subtópicos:** estão no original em inglês, como aparecem na chamada. Use esses nomes no formulário e nas buscas de artigos; a tradução automática do site tem erros (por exemplo, *Search* virou "Pesquisa" e *prompt engineering* virou "engenharia rápida").
- **"Quando vai para esta área":** resume a regra da própria chamada sobre que tipo de contribuição pertence à área. É o critério da conferência, não opinião minha.
- **Explicações e exemplos de pergunta:** são meus, para ajudar a entender. Não são definições oficiais nem afirmações sobre o que a literatura já resolveu.
- **Glossário no final:** reúne termos que aparecem em várias áreas (MDP, BDI, equilíbrio, etc.). Anote ali também os conceitos que você encontrar e ainda não domina, como o professor pediu.

## LEARN — Learning and Adaptation

Estuda como agentes **melhoram o próprio comportamento** a partir de dados, experiência ou feedback, sozinhos ou junto com outros agentes que também aprendem. É a ponte entre Machine Learning e agentes.

**Quando vai para esta área:** quando a contribuição principal é um método de aprendizado, uma análise teórica de aprendizado ou um estudo empírico de aprendizado em agentes. Se o foco for a arquitetura, o workflow ou a avaliação de agentes baseados em LLM, a chamada manda para GAAI.

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

**Leitura introdutória:** [Multiagent Systems: A Survey from a Machine Learning Perspective](https://jmvidal.cse.sc.edu/library/stone00a.pdf), de Peter Stone e Manuela Veloso (Autonomous Robots, 2000).

- **Por que esta:** foi escrita como introdução ao campo de SMA do ponto de vista de Machine Learning. Organiza os sistemas por dois eixos simples: se os agentes são iguais ou diferentes, e quanto eles se comunicam.
- **O que ler primeiro:** introdução e a seção que apresenta essa organização.
- **Atenção:** é anterior ao deep learning; vale pelos conceitos, não pelos métodos.
- **Complemento:** capítulo 1 do livro *Reinforcement Learning: An Introduction*, de Sutton e Barto, disponível gratuitamente no site dos autores. Não tem matemática.

## GAAI — Generative and Agentic AI

Estuda agentes e sistemas multiagentes que **dependem de modelos generativos** (LLMs, SLMs, modelos multimodais) para agir, raciocinar, interagir e decidir. É a área mais nova da chamada e a mais próxima do projeto do PDC.

**Quando vai para esta área:** quando a contribuição central é sobre agentes cujas capacidades dependem substancialmente de modelos generativos. Avanços só no modelo de linguagem, engenharia de prompt, uso genérico de ferramentas ou tarefas generativas quaisquer ficam **fora** do escopo, a menos que contribuam claramente para agentes. Se o núcleo for um método geral de aprendizado, planejamento, engenharia ou interação humana, vai para a área correspondente.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Memory, state, context, long-lived interaction, and other architectural patterns | Como o agente guarda e recupera informação além da janela de contexto e ao longo de muitas sessões (memória episódica, semântica, procedural) | O que o agente deve lembrar ou esquecer entre conversas? |
| Orchestration and workflows of agents and tools | Como se organiza quem faz o quê: pipeline fixo, supervisor/worker, hierarquia, agentes em paralelo | Quando vale ter vários agentes em vez de um só com as mesmas ferramentas? |
| Runtime support, infrastructure, and engineering | A infraestrutura que executa agentes: estado, filas, isolamento, escalonamento (ideia de "LLM OS") | Como executar centenas de agentes com estado sem perder informação? |
| Embodied, multimodal, and grounded generative AI agents | Agentes que percebem e agem num ambiente (físico ou virtual) com imagens, áudio, sensores | Um agente consegue usar o que vê na tela para operar um aplicativo? |
| Open-ended, autonomous, and self-improving agents | Agentes que definem os próprios objetivos, exploram sem tarefa fixa ou melhoram a si mesmos com o tempo | Um agente consegue melhorar as próprias ferramentas sem supervisão? |
| Planning, reasoning, and long-horizon agentic workflows | Tarefas de muitos passos, em que pequenos erros se acumulam | Por que agentes falham mais à medida que a tarefa fica mais longa? |
| Agency and learning in generative and agentic AI | Como agentes generativos aprendem com experiência: fine-tuning com trajetórias, RL sobre LLMs, aprender a usar ferramentas | Treinar um SLM com trajetórias de sucesso reduz erros de chamada de ferramenta? |
| Interaction protocols for agentic AI | Padrões de comunicação agente–ferramenta e agente–agente (por exemplo, MCP e A2A) | Que garantias de segurança um protocolo de ferramentas precisa oferecer? |
| Coordination, cooperation, and negotiation in generative AI agents | Como agentes LLM dividem trabalho, cooperam ou negociam entre si | Agentes LLM conseguem chegar a um acordo justo numa negociação? |
| Normative reasoning and institutional constraints | Fazer agentes respeitarem regras, normas e restrições de uma organização | Como garantir que o agente siga uma política interna mesmo sob pressão do usuário? |
| Theory of mind, user modeling, and social reasoning | O agente modelar o que outros (pessoas ou agentes) sabem, querem ou acreditam | O agente percebe que o usuário entendeu errado e corrige? |
| Hybrid classic-generative agents | Agentes LLM que usam componentes clássicos: planejadores, solvers, regras, arquiteturas BDI | Um planejador clássico verificando o plano do LLM aumenta a taxa de sucesso? |
| Failure handling, recovery, and resilience in agentic AI | Detectar que o agente errou, impedir que o erro se propague e se recuperar | Um agente consegue perceber que a ferramenta devolveu lixo e tentar de outro jeito? |
| Modeling and analysis of generative AI agents | Modelar formal ou empiricamente o comportamento de agentes para entendê-lo | Dá para prever em que tipo de tarefa um agente vai falhar? |
| Instruction following and multi-turn agent behavior | Seguir instruções corretamente ao longo de muitas trocas de mensagem | O agente mantém as restrições dadas no início após 20 turnos? |
| Human-agent interaction for delegation, feedback, and task collaboration | Como humanos delegam tarefas a agentes LLM, dão feedback e colaboram | Quando o agente deve pedir confirmação antes de agir? |
| Agentic decision support and decision boundaries | Agentes que apoiam decisões humanas e os limites do que podem decidir sozinhos | Que decisões nunca devem ser tomadas pelo agente sem um humano? |
| Alignment, learning from human feedback, and controllability | Fazer o agente agir de acordo com intenções e valores humanos e permanecer controlável | Como garantir que o agente pare quando mandado parar? |
| Explainability, introspection, and debugging | Entender por que o agente fez algo e depurar suas decisões | Dá para rastrear qual passo da trajetória causou a resposta errada? |
| Assurance, verification, and safety | Garantias sobre o comportamento: proteção contra prompt injection, ações proibidas, limites | Como impedir que um texto malicioso numa página faça o agente executar uma ação? |
| Benchmarks, evaluation, and metrics | Como medir o desempenho de agentes: sucesso, custo, consistência, qualidade da trajetória | O agente acerta a mesma tarefa se rodar cinco vezes? |
| Generative AI-supported specification and implementation of agents and MAS | Usar IA generativa para especificar ou programar outros agentes e SMAs | Um LLM consegue gerar um SMA correto a partir de uma descrição em texto? |
| Agentic AI applications in science, software, education, and critical domains | Aplicações de agentes generativos em domínios concretos, com ênfase no agente | Um agente consegue apoiar pesquisadores na revisão de literatura com segurança? |

**Leitura introdutória:** [A Survey on Large Language Model based Autonomous Agents](https://arxiv.org/abs/2308.11432), de Lei Wang e colegas (Frontiers of Computer Science, 2024).

- **Por que esta:** propõe um framework unificado para construir agentes com LLM e depois passa por aplicações e por como esses agentes são avaliados. Dá vocabulário para quase todos os subtópicos acima.
- **O que ler primeiro:** abstract, introdução e a seção de construção de agentes (perfil, memória, planejamento, ação).
- **Atenção:** é um survey de um campo que muda rápido; muitos trabalhos citados são preprints sem revisão por pares.

## GTEP — Game Theory and Economic Paradigms

Estuda agentes que têm **interesses próprios e agem estrategicamente**: cada um tenta obter o melhor resultado sabendo que os outros fazem o mesmo. Usa teoria dos jogos, economia e escolha social para analisar e projetar essas interações.

**Quando vai para esta área:** quando o modelo estratégico, econômico, de teoria dos jogos ou de escolha social é central. Se o foco for normas, instituições, ética ou governança, vai para COINE, a menos que o modelo estratégico seja o centro.

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

**Leitura introdutória:** [Multiagent Systems: Algorithmic, Game-Theoretic, and Logical Foundations](https://masfoundations.org/), de Yoav Shoham e Kevin Leyton-Brown (Cambridge University Press, 2009). É um livro, com versão em PDF gratuita para leitura no site dos autores.

- **Por que esta:** cobre teoria dos jogos, escolha social, desenho de mecanismos e leilões com exemplos antes das provas. Também tem um apêndice com a base de probabilidade e MDPs.
- **O que ler primeiro:** a introdução e o capítulo inicial sobre jogos não cooperativos (jogos na forma normal e equilíbrio de Nash).
- **Atenção:** é rigoroso; pule as demonstrações na primeira leitura.

## COINE — Coordination, Organizations, Institutions, Norms, and Ethics

Estuda o **lado social** dos sistemas multiagentes: como agentes coordenam trabalho, se organizam em equipes e instituições, seguem normas, constroem confiança e agem de forma ética e responsável.

**Quando vai para esta área:** quando as dimensões social, institucional, normativa, organizacional, de governança ou ética são centrais. Estudos de interação com pessoas vão para HAI; arquiteturas de agentes generativos vão para GAAI.

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

**Leitura introdutória:** [Multi-Agent Systems: A Survey](https://openaccess.library.uitm.edu.my/Record/doaj-c0be898bdea54259bc13171be6109dc9), de Ali Dorri, Salil Kanhere e Raja Jurdak (IEEE Access, 2018), em acesso aberto.

- **Por que esta:** visão geral acessível de SMA, incluindo como agentes se organizam e coordenam, sem exigir base formal.
- **O que ler primeiro:** introdução e as seções sobre características e organização de SMAs.
- **Atenção:** é amplo; não aprofunda normas, confiança ou ética. Se um desses subtópicos te atrair, peça uma leitura específica.

## SOPS — Search, Optimization, Planning, and Scheduling

Estuda **algoritmos para decidir o que fazer e em que ordem**: buscar soluções num espaço de possibilidades, otimizar sob restrições, montar planos de ação e agendar tarefas no tempo. Atenção: *Search* aqui é **busca algorítmica**, não "pesquisa científica".

**Quando vai para esta área:** quando a contribuição principal é um método de busca, otimização, planejamento, agendamento ou teoria da decisão, mesmo que aplicado a robôs, humanos ou com apoio de LLMs (modelos de fundação).

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

**Leitura introdutória:** [Multi-Agent Pathfinding: Definitions, Variants, and Benchmarks](https://ojs.aaai.org/index.php/SOCS/article/view/18510), de Roni Stern e colegas (SoCS, 2019).

- **Por que esta:** apresenta um problema clássico de planejamento multiagente, planejar rotas de vários agentes sem colisão, com terminologia unificada e figuras claras. Dois dos autores, Roni Stern e Nathan Sturtevant, são chairs da área SOPS da AAMAS 2027.
- **O que ler primeiro:** introdução e a definição do problema clássico com os tipos de conflito.
- **Atenção:** foca em um único problema; serve para entender como a área formula e compara métodos.

## RR — Representation and Reasoning

Estuda como **representar formalmente o que um agente sabe, acredita e quer**, e como raciocinar sobre isso de forma rigorosa, geralmente com lógica. Inclui a verificação formal: provar matematicamente que um sistema se comporta como deveria.

**Quando vai para esta área:** quando a contribuição principal é um formalismo, método ou análise de representação ou raciocínio para agentes. Se o núcleo for planejamento ou otimização, vai para SOPS, salvo se o formalismo for central.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Neurosymbolic approaches | Combinar redes neurais (aprendem com dados) com raciocínio simbólico (regras e lógica explícitas) | Um LLM com um verificador lógico erra menos em raciocínio? |
| Argumentation | Representar argumentos e contra-argumentos e decidir quais "vencem" | Como um agente decide entre duas conclusões conflitantes com base em argumentos? |
| Agent theories and models | Teorias formais do que é um agente e de como ele funciona (por exemplo, o modelo BDI: crenças, desejos, intenções) | Que modelo formal descreve bem um agente baseado em LLM? |
| Explainability | Gerar explicações sobre o raciocínio e as decisões do agente | Como explicar por que o agente escolheu este plano e não outro? |
| Logics for agent reasoning | Lógicas especiais para falar de conhecimento, crença, tempo, obrigação e ação | Que lógica captura "o agente sabe que o outro não sabe"? |
| Ontologies for agents | Vocabulários formais de conceitos e relações de um domínio, compartilhados entre agentes | Como dois agentes de origens diferentes passam a entender os mesmos termos? |
| Reasoning about knowledge, beliefs, goals, actions, plans, and change in MAS | Raciocinar sobre o estado mental próprio e dos outros e sobre como o mundo muda com as ações | Como um agente atualiza suas crenças quando recebe informação contraditória? |
| Reasoning and problem solving in agent-based systems | Técnicas gerais de raciocínio e resolução de problemas aplicadas a agentes | Como um agente resolve um problema dividindo-o em subproblemas? |
| Verification of agents and multiagent systems | Provar (ou testar exaustivamente) que o sistema satisfaz uma propriedade, como "nunca executa ação proibida" | Dá para garantir que este SMA nunca entra num estado inseguro? |
| Autoformalization | Traduzir automaticamente texto em linguagem natural para uma representação formal (lógica, código) | Um LLM consegue transformar uma regra escrita em português numa fórmula lógica correta? |
| Logic-constrained learning | Aprendizado de máquina obrigado a respeitar regras lógicas conhecidas | Como treinar um modelo que nunca viole uma restrição conhecida? |
| Strategic reasoning and strategy logics | Lógicas para raciocinar sobre o que agentes conseguem garantir agindo estrategicamente | Este grupo de agentes consegue garantir o objetivo, não importa o que os outros façam? |

**Leitura introdutória:** [BDI Agents: From Theory to Practice](https://apice.unibo.it/xwiki/bin/view/Publication/BdiIcmas95?language=), de Anand Rao e Michael Georgeff (ICMAS, 1995).

- **Por que esta:** texto clássico e curto (8 páginas) que liga a teoria de agentes com crenças, desejos e intenções à sua implementação, usando uma aplicação de controle de tráfego aéreo como exemplo.
- **O que ler primeiro:** introdução e a parte que explica por que os três estados mentais são necessários.
- **Atenção:** tem trechos de lógica formal; pule-os na primeira leitura.

## EMAS — Engineering and Analysis of Multiagent Systems

Estuda **como construir, testar, implantar e manter** agentes e sistemas multiagentes como software. A pergunta central não é "o agente é inteligente?", e sim "como garanto que este sistema funciona e continua funcionando?".

**Quando vai para esta área:** quando a contribuição principal são métodos, ferramentas, linguagens, plataformas ou processos para engenharia de agentes. Se o LLM faz a tarefa principal e a engenharia de SMA é só pano de fundo, o artigo vai para outra área.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Requirements capture and formal specification of MAS | Levantar e escrever, de forma precisa, o que o sistema deve fazer | Como especificar o comportamento esperado de um SMA antes de implementá-lo? |
| Programming paradigms and languages for autonomous agents | Linguagens e estilos de programação feitos para agentes (por exemplo, Jason, baseada em BDI) | Que abstrações de programação tornam agentes mais fáceis de escrever? |
| Runtime infrastructures and deployment platforms for scalable MAS (cloud, edge, hybrid) | Plataformas que executam muitos agentes na nuvem, na borda ou em ambientes mistos | Como rodar um SMA parte num servidor e parte num dispositivo local? |
| Testing, debugging, verification, validation, certification, and DevOps for MAS | Como testar e depurar sistemas não determinísticos e manter um ciclo de entrega contínua (inclui AgentOps) | Como escrever testes automatizados para um agente que responde diferente a cada execução? |
| Scalability, fault tolerance, and performance engineering of MAS platforms | O sistema aguentar crescer e continuar funcionando quando partes falham | O que acontece com o SMA se um agente trava no meio da tarefa? |
| Engineering self-adaptive agents (lifecycle, continuous evolution, deployment pipelines) | Agentes que mudam de comportamento em produção, e como gerenciar isso com segurança | Como atualizar um agente em produção sem quebrar o resto do sistema? |
| Interoperability, business agreements, and agent-to-agent protocols | Agentes de fornecedores diferentes conseguirem trabalhar juntos | Como dois agentes de empresas diferentes negociam um contrato de serviço? |
| Declarative, logic-based, and BDI agent programming and architectures | Programar agentes descrevendo crenças, objetivos e planos em vez de código passo a passo | Uma arquitetura BDI torna um agente LLM mais previsível? |
| Engineering MAS-based simulations for rigorous analysis and experimentation | Construir simulações com agentes que sirvam de experimento confiável | Como garantir que uma simulação com agentes seja reproduzível? |
| Sociotechnical governance tools for norms, ethics, and accountability | Ferramentas de software para aplicar e auditar regras e responsabilidade | Como registrar automaticamente quem (ou que agente) decidiu cada ação? |
| Human-centered engineering for usability, transparency, and explainability | Projetar o sistema para que pessoas consigam usá-lo e entender o que ele faz | Como mostrar ao usuário o que o SMA está fazendo em tempo real? |
| Open-source toolchains, benchmarks, and reproducible MAS testbeds | Ferramentas abertas e ambientes de teste padronizados para comparar sistemas | Existe um ambiente aberto para comparar SMAs de forma justa? |
| Engineering learning agents, including platform design and online adaptation | Infraestrutura para agentes que aprendem durante a operação | Como monitorar um agente que continua aprendendo depois de implantado? |
| Engineering MAS with LLM methods | Usar LLMs como componentes ou ferramentas na engenharia de SMAs | Onde, num SMA, um LLM deve entrar e onde não deve? |
| Hybrid symbolic-subsymbolic agent systems (neurosymbolic architectures and platforms) | Plataformas que juntam componentes simbólicos (regras, lógica) e aprendidos (redes neurais) | Como integrar um planejador simbólico com um LLM numa mesma arquitetura? |
| Benchmarks, evaluation methodologies, and reproducible workflows for MAS | Métodos para avaliar SMAs de forma comparável e repetível | Como relatar resultados de SMA de modo que outro grupo consiga reproduzir? |
| Data-driven engineering processes for design, testing, and adaptation | Usar dados de execução (logs, traces) para melhorar projeto e testes | Os logs de falhas em produção podem gerar novos casos de teste automaticamente? |
| Engineering MAS-based autonomous systems | Engenharia de sistemas autônomos completos construídos como SMA | Como certificar um sistema autônomo composto por vários agentes? |

**Leitura introdutória:** [Agent Programming in the Cognitive Era](https://repositorio.pucrs.br/dspace/handle/10923/20079), de Rafael Bordini e colegas (Autonomous Agents and Multi-Agent Systems, 2020), com PDF no repositório da PUCRS.

- **Por que esta:** revisa a programação de agentes baseada em BDI e discute formas de integrar técnicas de IA e Machine Learning a esses agentes. É uma ponte direta entre o EMAS clássico e os agentes com LLM.
- **O que ler primeiro:** abstract, introdução e a parte que lista as formas de integrar IA a agentes BDI.
- **Contexto:** o primeiro autor é da PUCRS e um dos criadores da linguagem Jason, mostrando a tradição brasileira nesta área.

## SIM — Modelling and Simulation of Societies

Estuda **simulações computacionais com muitos agentes** para entender como comportamentos individuais geram padrões coletivos (o chamado comportamento emergente) em sociedades, economias, ecossistemas, tráfego e organizações. Aqui o agente é um instrumento para estudar um sistema complexo.

**Quando vai para esta área:** quando a simulação é central, seja como avanço de método, seja como forma de explicar, prever ou avaliar um sistema complexo. A chamada cita ecologia e biologia entre as aplicações.

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

**Leitura introdutória:** [Tutorial on agent-based modelling and simulation](https://econpapers.repec.org/RePEc:taf:tjsmxx:v:4:y:2010:i:3:p:151-162), de Charles Macal e Michael North (Journal of Simulation, 2010).

- **Por que esta:** é literalmente um tutorial. Explica os conceitos básicos de modelagem baseada em agentes, mostra aplicações em várias disciplinas e apresenta ferramentas para construir modelos.
- **O que ler primeiro:** a parte de conceitos e a estrutura de um modelo baseado em agentes.
- **Atenção:** a versão do periódico tem acesso restrito. Os mesmos autores publicaram tutoriais introdutórios parecidos na Winter Simulation Conference (por exemplo, 2005, 2013 e 2014), que costumam ser mais fáceis de encontrar abertos.

## HAI — Human-Agent Interaction

Estuda **como pessoas e agentes interagem e trabalham juntos**: confiança, explicações, divisão de controle e como o agente percebe e modela o humano. Muitos trabalhos da área avaliam o sistema com estudos com usuários.

**Quando vai para esta área:** quando a interação humano-agente é central na pergunta, no método ou na avaliação. Aspectos institucionais ou de governança vão para COINE; arquiteturas de agentes generativos vão para GAAI.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Human-agent interaction | O campo geral de como humanos e agentes se comunicam e colaboram | Que forma de interação deixa o usuário mais eficiente com o agente? |
| Agent-based analysis of human interactions | Usar agentes ou modelos de agentes para analisar como pessoas interagem entre si | Um modelo de agentes explica padrões de conversa em equipes humanas? |
| Socially interactive agents | Agentes que interagem de forma social (conversa, emoção, empatia) | Um agente que demonstra empatia melhora a adesão do usuário? |
| Trust and explainability in human-agent interactions | Fazer a confiança do humano corresponder à real capacidade do agente, e explicar decisões | Explicações fazem o usuário confiar mais, ou confiar melhor (só quando deve)? |
| Human-robot interaction and collaboration | Pessoas e robôs físicos trabalhando juntos | Como um robô sinaliza o que vai fazer para não assustar quem está perto? |
| Social robotics and social interactions | Robôs projetados para interação social (educação, cuidado, companhia) | Um robô social ajuda crianças a aprender um conteúdo? |
| Mixed-initiative and shared autonomy | Divisão de controle: quando o agente age sozinho, quando pergunta, quando o humano assume | Em que momento o agente deve parar e pedir confirmação? |
| Groups of humans and agents | Equipes mistas com várias pessoas e vários agentes | Como um agente deve se comportar numa reunião com várias pessoas? |
| Agent models and architectures for interaction with humans | Arquiteturas de agente feitas especificamente para interagir com pessoas | Que componentes um agente precisa para acompanhar o estado do usuário? |
| Design for human-agent interaction | Métodos de design de interfaces e interações com agentes | Como projetar a interface para o usuário perceber que está falando com um agente? |
| Virtual humans | Personagens digitais com aparência e comportamento humanos | Um tutor virtual com rosto é mais eficaz que um só por texto? |
| Theory of mind and user modeling in human-agent interaction | O agente inferir o que o humano sabe, quer ou sente | O agente percebe que o usuário está confuso e muda a explicação? |
| Modelling, detecting, and accounting for deception in human-AI teams | Lidar com engano em equipes humano-IA, venha do humano ou do agente | Como detectar que um agente está enganando o usuário? |
| Human cognitive modeling for agent interaction | Modelos de como as pessoas pensam (atenção, memória, carga cognitiva) usados pelo agente | O agente pode ajustar o volume de informação à carga cognitiva do usuário? |

**Leitura introdutória:** [Guidelines for Human-AI Interaction](https://www.microsoft.com/research/publication/guidelines-for-human-ai-interaction/), de Saleema Amershi e colegas (CHI, 2019).

- **Por que esta:** propõe 18 diretrizes de como um sistema de IA deve se comportar com pessoas, agrupadas em quatro momentos: no primeiro contato, durante o uso, quando erra e ao longo do tempo. Mostra também como a área valida propostas com estudos envolvendo profissionais.
- **O que ler primeiro:** a tabela com as 18 diretrizes e a seção de validação.
- **Atenção:** trata de produtos com IA em geral, não especificamente de agentes autônomos.

## ROBOT — Robotics and Control

Estuda **robôs como agentes**: entidades com corpo, situadas no mundo físico, que precisam perceber, raciocinar, planejar, aprender e agir de forma autônoma, sozinhas ou em equipes de robôs.

**Quando vai para esta área:** quando a contribuição principal é sobre robôs autônomos, sistemas multirrobô ou a interação de robôs com pessoas, agentes de software ou o ambiente físico. Percepção, mapeamento ou controle entram quando contribuem claramente para robôs autônomos.

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
| Mapping, localization, and navigation | Construir um mapa, saber onde está nele e se deslocar até um destino | Como o robô se localiza num prédio sem GPS? |
| Autonomous robot manipulation and task execution | Pegar, mover e usar objetos com mãos ou garras | Como o robô pega objetos frágeis de formatos variados? |
| Decision-making and control for autonomous robots and robot teams | Controlar o movimento do robô ou da equipe em tempo real | Como manter uma formação de robôs estável com vento? |
| Robot learning for autonomy and adaptation | Robôs aprendendo habilidades por demonstração, tentativa e erro ou simulação | Uma habilidade aprendida em simulação funciona no robô real? |
| Long-term or lifelong autonomy | Robôs operando por semanas ou meses sem intervenção, adaptando-se a mudanças | Como o robô continua útil depois que o ambiente muda? |
| Execution monitoring and failure recovery for robots | Perceber que algo deu errado durante a execução e se recuperar | O robô percebe que deixou cair o objeto e tenta de novo? |
| Robot modeling and simulation for autonomous agents | Simular robôs e ambientes para testar e treinar antes do mundo real | Que diferenças entre a simulação e a realidade mais atrapalham? |
| Explainability, trust, and ethics for robots | Robôs explicáveis, confiáveis e que agem de forma ética | Como um robô explica por que parou de repente? |
| Hybrid systems of robots with humans and/or software agents | Sistemas que misturam robôs, pessoas e agentes de software | Como um agente de software coordena robôs e operadores humanos? |

**Leitura introdutória:** [Do As I Can, Not As I Say: Grounding Language in Robotic Affordances](https://arxiv.org/abs/2204.01691), de Michael Ahn e colegas (CoRL, 2022), conhecido como SayCan.

- **Por que esta:** é uma ponte natural para quem vem de LLMs. O modelo de linguagem sugere passos de alto nível, e funções de valor de habilidades pré-treinadas dizem o que o robô de fato consegue fazer naquele ambiente.
- **O que ler primeiro:** abstract, introdução e a figura que explica a combinação "o que o LLM sugere" × "o que o robô consegue".
- **Atenção:** é um único sistema de um laboratório grande; não representa a área de robótica como um todo.

## IASI — Innovative Applications and Societal Impact

Estuda **aplicações reais de agentes e o impacto que elas geram**. A contribuição não é um algoritmo novo, e sim mostrar que agentes resolvem um problema concreto, com evidência de benefício, viabilidade ou adoção.

**Quando vai para esta área:** quando a contribuição principal é a aplicação, a implantação, a validação realista, o design com as partes interessadas ou o impacto social demonstrado. Se o núcleo for um algoritmo, arquitetura, ferramenta ou método de simulação novo, vai para a área técnica correspondente. A chamada pede que o artigo explique o contexto, o papel dos agentes, a novidade e a evidência de impacto, e incentiva parcerias com quem vai usar o sistema.

| Subtópico | O que é | Exemplo de pergunta |
| --- | --- | --- |
| Deployed or emerging applications of agent-based and agentic systems addressing real-world challenges | Sistemas de agentes já em uso ou prestes a ser usados em problemas reais | O sistema de agentes reduziu o tempo de atendimento depois de implantado? |
| Agent-based and agentic systems for social good, sustainability, public policy, education, health, science, industry, and critical domains | Aplicações em áreas de impacto social e domínios críticos | Agentes conseguem apoiar o monitoramento de espécies ameaçadas? |
| Realistic agent-based and agentic models of human organizations, institutions, and socio-technical systems | Modelos de agentes realistas o bastante para representar organizações reais | O modelo reproduz o funcionamento real de um órgão público? |
| Evaluation of cognitive, social, organizational, or decision-support capabilities in real-world settings | Avaliar agentes no mundo real, não só em benchmarks de laboratório | O agente ajuda de fato os profissionais a tomar decisões melhores no dia a dia? |
| Integration with other AI, software, cyber-physical, robotic, simulation, or decision-support technologies | Juntar agentes com outros sistemas já existentes numa organização | Como integrar um agente aos sistemas legados de uma instituição? |
| Hybrid agent-based, agentic AI, and reinforcement learning solutions for real-world applications | Soluções reais que combinam simulação com agentes, agentes LLM e RL | Uma combinação de simulação e RL otimiza a logística de uma rede real? |
| Deployment, adoption, usability, robustness, safety, and maintainability in practice | O que acontece quando o sistema sai do protótipo: uso, manutenção, falhas reais | Por que usuários abandonam um agente depois de algumas semanas? |
| Challenges, best practices, and lessons learned from real-world deployments | Relatos sistemáticos do que deu certo e errado ao implantar agentes | Quais problemas só apareceram depois que o sistema entrou em produção? |
| Evaluation methodologies, benchmarks, and evidence of measurable impact | Como medir o impacto real de uma aplicação | Que métrica mostra que a aplicação trouxe benefício, e não só que funciona? |
| Stakeholder involvement, participatory design, and co-creation | Construir a aplicação junto com quem vai usá-la | Envolver os usuários desde o início muda o que o sistema deve fazer? |
| Ethical, legal, societal, and environmental implications | Efeitos éticos, legais, sociais e ambientais de sistemas implantados | Qual o custo energético de manter este sistema de agentes rodando? |
| Frameworks, platforms, and tools supporting implementation and deployment | Ferramentas que facilitam construir e implantar aplicações com agentes | Que plataforma permite a uma instituição pequena implantar agentes localmente? |

**Leitura introdutória:** [Using Game Theory for Los Angeles Airport Security](https://ojs.aaai.org/index.php/aimagazine/article/view/2173), de James Pita e colegas (AI Magazine, 2009).

- **Por que esta:** conta como um agente de software (ARMOR) foi implantado no aeroporto de Los Angeles a partir de 2007 para randomizar patrulhas e postos de controle. Mostra o que a IASI valoriza: necessidade real, parceria com quem usa o sistema e avaliação no mundo real.
- **O que ler primeiro:** a descrição do problema, as decisões de projeto e a parte de implantação e avaliação.
- **Atenção:** é a versão de divulgação, mais acessível, do artigo da trilha industrial da AAMAS 2008. O método por trás é de teoria dos jogos (GTEP); a contribuição destacada aqui é a aplicação.

## Glossário

Termos que aparecem em várias áreas. As definições são simplificadas para orientar a leitura; aprofunde quando um deles for central para o tópico que você escolher. Acrescente nas últimas linhas os conceitos que você encontrar e ainda não domina.

| Termo | Significado simplificado | Onde aparece |
| --- | --- | --- |
| Agente | Entidade que percebe um ambiente e age nele para atingir objetivos, com algum grau de autonomia | Todas |
| Sistema multiagente (SMA / MAS) | Vários agentes interagindo num mesmo ambiente, cooperando ou competindo | Todas |
| LLM / SLM | Modelo de linguagem grande / pequeno (geralmente abaixo de cerca de 10 bilhões de parâmetros) | GAAI, EMAS, SIM |
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
| (seu conceito) |  |  |
| (seu conceito) |  |  |
