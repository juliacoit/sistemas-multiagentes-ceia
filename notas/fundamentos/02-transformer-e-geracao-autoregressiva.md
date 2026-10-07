---
titulo: Transformer e geração autoregressiva
status: rascunho — expandir com os materiais
fontes: [slides "Geração de Texto Autoregressiva" (grupo de estudos), Vaswani et al. 2017, conhecimento externo]
---

# Transformer e geração autoregressiva

> Nota escrita a partir da lista de tópicos dos slides, sem os slides em mãos. Os tópicos
> vêm de `[Material: slides Geração de Texto Autoregressiva]`; as explicações são `[Externo]`
> até eu conferir cada uma contra o material.

## Transformer (2017): encoder vs. decoder

A arquitetura original tem duas pilhas. `[Externo]`

- **Encoder:** lê a entrada inteira; cada posição enxerga todas as outras.
- **Decoder:** gera a saída token a token; cada posição só enxerga as anteriores.

Os LLMs generativos atuais (família GPT, Qwen) usam só a pilha de decoder. `[Externo]`

## Attention: Q, K, V

Cada token produz três vetores: uma *query* (o que procuro), uma *key* (o que ofereço) e um
*value* (o que entrego). O peso de atenção entre dois tokens vem do produto entre a query de
um e a key do outro, normalizado por softmax; a saída é a média dos values ponderada por
esses pesos. `[Externo]`

**Multi-head attention** roda várias atenções em paralelo, cada uma com projeções próprias, e
concatena os resultados. Cada cabeça pode se especializar num tipo de relação. `[Externo]`

## Máscara causal

No treino, a sequência inteira entra de uma vez e o modelo prevê o token seguinte em todas as
posições em paralelo. Sem máscara, a posição `i` poderia olhar para `i+1`, que é justamente a
resposta. A máscara causal zera a atenção para posições futuras, e assim o treino reproduz a
condição da geração, em que o futuro ainda não existe. `[Externo]`

## Do token à amostra

```
tokens → embeddings → blocos do Transformer → logits → softmax → amostragem → próximo token
```

O token escolhido é anexado ao contexto e o processo se repete. `[Externo]`

| Estratégia | O que faz |
| --- | --- |
| **Greedy** | Escolhe sempre o token mais provável. Determinístico, tende à repetição. |
| **Temperatura** | Divide os logits por `T` antes do softmax. `T<1` concentra, `T>1` espalha. |
| **Top-k** | Amostra só entre os `k` tokens mais prováveis. |
| **Top-p** | Amostra no menor conjunto cuja probabilidade acumulada atinge `p`. |

`[Externo]`

`[Interpretação]` Essa etapa importa para agentes: uma chamada de tool é texto amostrado, e a
amostragem é uma das fontes de chamadas malformadas
([agentes/02](../agentes/02-tools-e-function-calling.md)).

## Treino em etapas

1. **Pré-treino autossupervisionado:** prever o próximo token em grandes volumes de texto. O
   rótulo é o próprio texto.
2. **SFT (supervised fine-tuning):** ajuste em pares instrução–resposta.
3. **Alinhamento:** ajuste por preferência ou por reforço para adequar o comportamento.

`[Externo]` `[A verificar]` Conferir a nomenclatura exata das etapas nos slides.

## GPT-2 vs. Qwen3

| Componente | GPT-2 | Qwen3 |
| --- | --- | --- |
| Normalização | LayerNorm | RMSNorm |
| Posição | Embeddings posicionais aprendidos | RoPE (rotação aplicada a Q e K) |
| Atenção | Multi-head padrão | GQA (grupos de cabeças de query compartilham K/V) |

`[Material: slides Geração de Texto Autoregressiva]` para a existência da comparação e dos
três itens; `[Externo]` para a descrição de cada um. `[A verificar]` os detalhes do Qwen3 na
documentação do modelo.

## Lacunas em aberto

- **Positional encoding:** ainda não estudei a fundo. Atenção é invariante à ordem, logo a
  posição precisa ser injetada; falta entender as opções (senoidal, aprendida, RoPE) e os
  trade-offs. `[A verificar]`
- **Por que GRPO foi usado no experimento dos slides?** Não sei a motivação. Perguntar ao
  autor da apresentação. `[A verificar]`
