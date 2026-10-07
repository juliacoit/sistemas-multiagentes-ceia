---
titulo: "Proposta — ReAct em SLMs locais"
status: proposta
fontes: [yao2022react]
---

# ReAct em SLMs locais

**Status: proposta, sem resultados.**

## Problema

O artigo do ReAct relata que, em modelos menores, o método perde desempenho via prompting e
melhora com fine-tuning ([análise](../../papers/2022-yao-react.md)). Esses modelos não são os
SLMs abertos de hoje. Não sei como o ReAct se comporta nos modelos que o projeto consegue
rodar localmente.

## Pergunta

Como o desempenho e o custo do ReAct variam, em SLMs locais, com o formato do prompt, o
regime de uso e o tamanho do modelo?

## Hipóteses

- **H1.** Via prompting, o ReAct em SLMs tem taxa de laços e de chamadas malformadas alta o
  bastante para anular o ganho sobre o act-only. `[Hipótese]`
- **H2.** O formato do prompt (texto livre "Thought/Action" vs. tool calling nativo do chat
  template) muda a taxa de chamadas malformadas mais do que muda a acurácia. `[Hipótese]`
- **H3.** A diferença entre ReAct e act-only cresce com o tamanho do modelo. `[Hipótese]`

## Método

**Variáveis independentes**

| Variável | Níveis |
| --- | --- |
| Formato do prompt | ReAct em texto livre; tool calling nativo do template |
| Regime | Prompting few-shot; fine-tuning (segunda fase, se houver recurso) |
| Tamanho do modelo | Pelo menos três tamanhos da mesma família |

**Fixos:** conjunto de tools, limite de passos, parâmetros de amostragem, subconjunto de
tarefas, número de sementes.

**Tarefas:** começar por um subconjunto de HotpotQA, por ser um dos benchmarks do artigo.
`[A verificar]` Disponibilidade e licença dos dados e do ambiente de busca.

## Baseline

- **CoT** (raciocínio sem ação).
- **Act-only** (ação sem pensamento).

Todos com o mesmo modelo e o mesmo limite de tokens por tarefa.

## Métricas

| Métrica | Definição |
| --- | --- |
| Acurácia | Tarefas corretas / total |
| Custo em tokens | Tokens de entrada e de saída por tarefa |
| Custo em tempo | Tempo de parede por tarefa |
| Taxa de loops | Trajetórias que repetem a mesma ação com os mesmos argumentos N vezes |
| Taxa de tool calls malformadas | Chamadas que o parser rejeita / chamadas emitidas |

## Resultado positivo

H1 sustentada se, em pelo menos dois tamanhos de modelo, o ReAct via prompting não superar o
act-only em acurácia além do intervalo de confiança, com custo maior. H2 e H3 sustentadas se
o efeito aparecer na mesma direção em todos os tamanhos testados.

## Resultado inconclusivo

- Diferenças dentro da variação entre sementes.
- Acurácia perto de zero em todas as condições (efeito piso): a tarefa é difícil demais para
  esses modelos e não discrimina os métodos.
- Taxa de malformação tão alta que a acurácia mede o parser, não o método.

## Ablação

- Remover os exemplos few-shot.
- Remover os pensamentos mantendo o mesmo formato (isola o efeito do pensamento).
- Limitar o número de passos.

## Riscos

- Hardware limitado restringe tamanhos de modelo e número de repetições.
- Comparar famílias diferentes confunde tamanho com arquitetura e dados de treino; por isso a
  preferência por uma única família.
