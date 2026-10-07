---
titulo: Modos de falha e avaliação de agentes
status: rascunho — expandir com os materiais
fontes: [Huyen 2025 (livro, cap. 6)]
---

# Modos de falha e avaliação de agentes

## Falhas de planejamento

| Falha | Exemplo | Detecção |
| --- | --- | --- |
| **Tool inválida** | O plano chama uma função que não existe | Fácil: comparar com o inventário |
| **Tool válida, parâmetros inválidos** | Função certa, com argumento a mais ou a menos | Fácil: validar contra a assinatura |
| **Tool válida, valores incorretos** | Função e assinatura certas, valor errado | **Difícil:** a chamada é bem formada e executa sem erro |

`[Material: Huyen 2025, livro]`

Outras falhas de planejamento: `[Material: Huyen 2025, livro]`

- **Falha de objetivo:** o plano não resolve a tarefa, ou resolve violando uma restrição
  dada (orçamento, prazo).
- **Erro de reflexão:** o agente afirma ter concluído a tarefa sem ter concluído.

`[Interpretação]` O erro de reflexão é o mais grave para confiabilidade, porque engana quem
confia no relato do próprio agente. Verificação de conclusão não pode depender só dele.

## Falhas de ferramenta

A tool certa foi chamada do jeito certo, e a saída veio errada. `[Material: Huyen 2025, livro]`

### Correção registrada: exemplo Kitty Vogue

Eu havia classificado a falha do exemplo Kitty Vogue como falha de planejamento. O correto é
**falha de ferramenta**: o plano e a chamada estavam certos, e a saída da tool é que estava
errada. A distinção importa porque o conserto é outro: corrigir a tool, não o planejador.

`[A verificar]` Reler o trecho do exemplo no material para descrever aqui qual tool falhou e
como.

## Eficiência

Um agente pode chegar à resposta certa gastando demais. `[Material: Huyen 2025, livro]`

## Métricas sugeridas

`[Material: Huyen 2025, livro]`

**Planejamento**

- De todos os planos gerados, quantos são válidos.
- Quantos planos é preciso gerar, em média, até obter um válido.
- De todas as chamadas de tool, quantas são válidas.
- Frequência de cada tipo de falha: tool inválida, parâmetros inválidos, valores incorretos.

**Eficiência**

- Número médio de passos por tarefa.
- Custo médio por tarefa.
- Tempo de cada tipo de ação; quais ações são mais caras.

## Erro composto

Se cada passo acerta 95% das vezes, uma tarefa de 10 passos acerta em

`0,95^10 ≈ 0,60`

`[Material: Huyen 2025, livro]`

`[Interpretação]` **Premissa escondida:** o cálculo supõe erros **independentes** entre os
passos e nenhuma correção. Na prática:

- Os erros podem ser correlacionados (uma observação errada contamina os passos seguintes),
  o que muda a conta.
- O agente pode detectar e corrigir um erro num passo posterior, o que melhora a taxa em
  relação ao produto simples.
- Nem todo passo é igualmente crítico.

O número serve como intuição de ordem de grandeza, não como previsão. `[Interpretação]`

`[Hipótese]` Em sistemas multiagentes a premissa de independência é ainda menos plausível,
porque os agentes leem as saídas uns dos outros.

## Perguntas em aberto

- Como medir "valores incorretos" em escala sem gabarito por chamada?
- Qual a taxa de erro de reflexão em SLMs, comparada à de modelos grandes?
