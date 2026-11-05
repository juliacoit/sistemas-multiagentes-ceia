---
titulo: Roadmap de leituras e tópicos
status: em construção
fontes: [referencias/referencias.bib]
---

# Roadmap

Lista do que falta ler ou aprofundar. Cada item, quando for estudado, vira uma análise em
`papers/` ou uma nota em `notas/`.

## Leituras

- [ ] **Reflexion** (Shinn et al., 2023). Pergunta de leitura: o ganho vem da reflexão verbal
  ou de simplesmente ter mais tentativas? Qual o baseline com o mesmo número de tentativas?
- [ ] **Toolformer** (Schick et al., 2023). Pergunta de leitura: como o modelo aprende *quando*
  chamar uma tool, e o que isso diz sobre tool calling em modelos pequenos?

### Leituras introdutórias da exploração AAMAS 2027

Uma por área, indicadas no [guia das áreas](notas/exploracao-aamas-2027/guia-areas.md). O que
ler primeiro está no arquivo de cada área em
[notas/exploracao-aamas-2027/areas/](notas/exploracao-aamas-2027/areas/).

- **LEARN**
  - [ ] Stone & Veloso (2000), *Multiagent Systems: A Survey from a Machine Learning Perspective*.
- **GAAI**
  - [ ] Wang et al. (2024), *A Survey on Large Language Model based Autonomous Agents*.
- **GTEP**
  - [ ] Shoham & Leyton-Brown (2009), *Multiagent Systems: Algorithmic, Game-Theoretic, and Logical Foundations* (livro).
- **COINE**
  - [ ] Dorri, Kanhere & Jurdak (2018), *Multi-Agent Systems: A Survey*.
- **SOPS**
  - [ ] Stern et al. (2019), *Multi-Agent Pathfinding: Definitions, Variants, and Benchmarks*.
- **RR**
  - [ ] Rao & Georgeff (1995), *BDI Agents: From Theory to Practice*.
- **EMAS**
  - [ ] Bordini et al. (2020), *Agent Programming in the Cognitive Era*.
- **SIM**
  - [ ] Macal & North (2010), *Tutorial on Agent-Based Modelling and Simulation*.
- **HAI**
  - [ ] Amershi et al. (2019), *Guidelines for Human-AI Interaction*.
- **ROBOT**
  - [ ] Ahn et al. (2022), *Do As I Can, Not As I Say: Grounding Language in Robotic Affordances* (SayCan).
- **IASI**
  - [ ] Pita et al. (2009), *Using Game Theory for Los Angeles Airport Security*.

## Tópicos

- [ ] **MCP (Model Context Protocol)**: o que o protocolo padroniza e o que ele deixa de fora
  (ver distinção ReAct ≠ MCP em [papers/2022-yao-react.md](papers/2022-yao-react.md)).
- [ ] **Memória episódica**: relação com a taxonomia de memória da nota
  [agentes/04](notas/agentes/04-memoria.md).
- [ ] **Avaliação de agentes**: benchmarks, métricas por trajetória e não só por resposta final.
- [ ] **Observabilidade / AgentOps**: o que precisa ser registrado para auditar uma execução.
- [ ] **SLMs locais**: quais modelos, quais formatos de tool calling, quais limites práticos.

## Lacunas abertas nas notas

- [ ] Positional encoding ([fundamentos/02](notas/fundamentos/02-transformer-e-geracao-autoregressiva.md)).
- [ ] Por que GRPO foi usado no experimento dos slides de geração autoregressiva.
- [ ] O que justifica chamar um componente de "agente" ([agentes/01](notas/agentes/01-o-que-e-um-agente.md)).
