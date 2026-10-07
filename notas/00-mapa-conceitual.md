---
titulo: Mapa conceitual — do Transformer ao sistema multiagente
status: rascunho — expandir com os materiais
fontes: [notas deste repositório]
---

# Mapa conceitual

Fio condutor das notas: cada etapa acrescenta uma capacidade à anterior e também um novo
modo de falhar. A cadeia é `[Interpretação]` minha, como forma de organizar o estudo.

```
Transformer ──> attention ──> LLM ──> tool use ──> agente ──> sistema multiagente
```

| Etapa | O que acrescenta | O que pode dar errado | Nota |
| --- | --- | --- | --- |
| **Modelagem de linguagem** | Prever o próximo token a partir do contexto | Contexto curto, vocabulário esparso | [fundamentos/01](fundamentos/01-nlp-e-modelagem-de-linguagem.md) |
| **Transformer e attention** | Cada token consulta todos os anteriores | Custo cresce com o contexto | [fundamentos/02](fundamentos/02-transformer-e-geracao-autoregressiva.md) |
| **LLM** | Geração autoregressiva com pré-treino em larga escala | Alucinação; conhecimento congelado | [fundamentos/02](fundamentos/02-transformer-e-geracao-autoregressiva.md) |
| **Tool use** | Texto gerado vira chamada a código externo | Chamada malformada; parâmetro errado | [agentes/02](agentes/02-tools-e-function-calling.md) |
| **Agente** | O modelo decide a sequência de ações | Erro composto ao longo dos passos | [agentes/01](agentes/01-o-que-e-um-agente.md), [03](agentes/03-planejamento-e-reflexao.md), [04](agentes/04-memoria.md), [05](agentes/05-modos-de-falha-e-avaliacao.md) |
| **Sistema multiagente** | Vários agentes interagem | Falhas de coordenação; custo multiplicado | [agentes/01](agentes/01-o-que-e-um-agente.md) (seção crítica) |

## Ideias que atravessam as etapas

- **Tudo é texto no contexto.** Tools, resultados, pensamentos e memória recuperada chegam ao
  modelo como tokens. Isso liga a máscara causal e a amostragem (fundamentos/02) ao tool
  calling (agentes/02). `[Interpretação]`
- **O modelo não executa nada.** Quem age é o runtime ao redor. Confiabilidade é propriedade
  do sistema inteiro, não só do modelo. `[Interpretação]`
- **Recuperar não é agregar.** Busca por similaridade devolve uma amostra; perguntas que
  exigem o conjunto completo pedem outra tool ([agentes/06](agentes/06-rag-vs-tools.md)).
- **Baseline antes de multiagente.** Um agente único com tools (ReAct) é o ponto de comparação
  de qualquer arquitetura multiagente ([papers/2022-yao-react.md](../papers/2022-yao-react.md)).
  `[Interpretação]`
