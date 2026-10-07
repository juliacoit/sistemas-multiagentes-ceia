---
titulo: NLP e modelagem de linguagem
status: rascunho — expandir com os materiais
fontes: [slides "Introdução ao NLP" (grupo de estudos), conhecimento externo]
---

# NLP e modelagem de linguagem

> Nota escrita a partir da lista de tópicos dos slides, sem os slides em mãos. Os tópicos
> vêm de `[Material: slides Introdução ao NLP]`; as explicações são `[Externo]` até eu
> conferir cada uma contra o material.

## Modelagem de linguagem

Um modelo de linguagem atribui probabilidade a sequências de tokens. Pela regra da cadeia,
isso equivale a prever cada token dado os anteriores:

`P(w1..wn) = Π P(wi | w1..wi-1)` `[Externo]`

É essa formulação que torna possível gerar texto um token por vez
([fundamentos/02](02-transformer-e-geracao-autoregressiva.md)).

## Limites dos n-gramas

Um modelo de n-gramas aproxima o contexto pelos `n-1` tokens anteriores e estima as
probabilidades por contagem. `[Externo]` Três limites:

- **Contexto curto:** dependências além da janela são invisíveis.
- **Esparsidade:** a maioria das sequências possíveis nunca aparece no corpus, e a contagem
  dá zero. Suavização atenua, não resolve.
- **Sem generalização entre palavras parecidas:** "gato" e "felino" são símbolos sem relação.

O terceiro limite é o que motiva representações densas. `[Interpretação]`

## Perceptron e MLP

- **Perceptron:** combinação linear das entradas seguida de um limiar. Só separa classes
  linearmente separáveis. `[Externo]`
- **MLP:** camadas de perceptrons com não linearidade entre elas, treinadas por
  retropropagação. `[Externo]`

## Representações

| Representação | Ideia | Limite |
| --- | --- | --- |
| **One-hot** | Vetor do tamanho do vocabulário com um único 1 | Todas as palavras equidistantes; dimensão enorme |
| **Bag of words** | Contagem das palavras do documento | Perde a ordem |
| **Embeddings** | Vetor denso aprendido | Um vetor por palavra, independente do contexto (nos estáticos) |
| **Word2Vec / CBOW** | Aprende o embedding prevendo a palavra central a partir das vizinhas | Estático; palavras fora do vocabulário ficam sem vetor |

`[Externo]` A tabela resume o conhecimento geral da área.

## Tokenização por subpalavras (BPE)

O BPE parte de caracteres e funde, repetidamente, o par de símbolos adjacentes mais
frequente, até atingir o tamanho de vocabulário desejado. Palavras raras são decompostas em
pedaços conhecidos, o que elimina o problema de palavra fora do vocabulário. `[Externo]`

## Lacunas

- `[A verificar]` Conferir nos slides quais desses pontos foram apresentados com outra ênfase
  ou com exemplos próprios, e trocar os rótulos `[Externo]` por `[Material]` onde couber.
- `[A verificar]` Os slides tratam de Skip-gram além de CBOW?
