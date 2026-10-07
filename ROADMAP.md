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
