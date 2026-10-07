---
titulo: O que é um agente
status: rascunho — expandir com os materiais
fontes: [Huyen 2025 (livro, cap. 6), Google Whitepaper Agents 2024]
---

# O que é um agente

## Definição

Um agente é qualquer coisa que percebe o ambiente e age sobre ele. A definição é de Russell &
Norvig e é o ponto de partida do capítulo. `[Material: Huyen 2025, livro]`

Duas consequências dessa definição: `[Material: Huyen 2025, livro]`

- O agente é caracterizado pelo **ambiente** em que opera e pelo **conjunto de ações** que
  pode executar.
- Em agentes baseados em LLM, o conjunto de ações é ampliado pelas **tools** a que o modelo
  tem acesso ([nota 02](02-tools-e-function-calling.md)).

## Componentes

O whitepaper do Google descreve o agente em três partes: `[Material: Google Whitepaper Agents]`

| Componente | Papel |
| --- | --- |
| **Modelo** | Toma as decisões. |
| **Ferramentas** | Ligam o modelo ao mundo externo. |
| **Camada de orquestração** | Laço que recebe informação, raciocina e escolhe a próxima ação, até atingir o objetivo ou um ponto de parada. |

## Workflow vs. agente

No workflow, a sequência de passos está no código; no agente, o modelo escolhe a sequência
durante a execução. `[Interpretação]` Teste prático: se consigo desenhar o grafo de execução
antes de rodar, é workflow. Ver [glossário](../../glossario.md).

`[A verificar]` Conferir se algum dos materiais faz essa distinção com esses termos ou se ela
vem de fora.

## Seção crítica: quando um componente merece ser chamado de agente?

Huyen observa que, se cada componente de um sistema (planejador, validador de planos,
executor, classificador de intenção) for contado como um agente, então a maioria dos agentes
já é multiagente. `[Material: Huyen 2025, livro]`

`[Interpretação]` Esse critério dilui o termo. Se qualquer chamada a um modelo com papel
próprio é "um agente", "sistema multiagente" passa a descrever quase todo pipeline com mais
de um prompt, e deixa de separar arquiteturas que se comportam de modo diferente. Para a
linha de pesquisa isso é um problema prático: não dá para estudar a confiabilidade de SMAs
sem saber o que conta como um.

**Pergunta registrada:** o que justifica chamar um componente de agente?

Propriedades candidatas para diferenciar os três casos: `[Hipótese]`

| Propriedade | Pipeline | Supervisor / worker | SMA "real" |
| --- | --- | --- | --- |
| Quem decide o próximo passo | O código | O supervisor | Cada agente, localmente |
| Estado próprio por componente | Não | Parcial (contexto do worker) | Sim |
| Objetivo próprio por componente | Não (função fixa) | Subtarefa delegada | Sim, podendo conflitar |
| Comunicação | Saída → entrada, fixa | Só via supervisor | Entre pares, com conteúdo decidido pelos agentes |
| O resultado depende da interação | Não | Pouco | Sim (negociação, crítica, divisão emergente) |

Critério provisório: só chamo de sistema multiagente quando há mais de uma entidade com
decisão, estado e objetivo próprios, **e** a interação entre elas altera o resultado em
relação ao que um único agente com as mesmas tools produziria. `[Hipótese]`

O último ponto é testável: comparar contra um baseline de agente único
([papers/2022-yao-react.md](../../papers/2022-yao-react.md)).

## Perguntas em aberto

- O whitepaper do Google traz um critério próprio para separar agente de modelo com tools?
  `[A verificar]`
- A literatura clássica de SMA (anterior a LLMs) tem um critério que eu deveria adotar em vez
  de inventar um? `[A verificar]`
