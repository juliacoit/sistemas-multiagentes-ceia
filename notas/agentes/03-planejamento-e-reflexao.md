---
titulo: Planejamento e reflexão
status: rascunho — expandir com os materiais
fontes: [Huyen 2025 (livro, cap. 6), Yao et al. 2022 (ReAct)]
---

# Planejamento e reflexão

## Desacoplar planejamento de execução

Gerar o plano e executá-lo são etapas separadas. Primeiro o plano é produzido, depois
validado, e só então executado. Assim um plano ruim é barrado antes de gastar chamadas de
tool. `[Material: Huyen 2025, livro]`

## Validação de planos

Duas formas de validar: `[Material: Huyen 2025, livro]`

- **Heurísticas:** regras baratas, como rejeitar planos que usam tools inexistentes ou que
  passam de um número máximo de passos.
- **Juízes:** outro modelo avalia se o plano é razoável.

`[Interpretação]` O juiz é mais um componente que pode errar. Usar um modelo para validar
outro traz a pergunta de quem valida o validador, que volta na discussão de confiabilidade.

## Granularidade e planejamento hierárquico

Um plano pode ser escrito em alto nível (em linguagem natural) ou em baixo nível (chamadas
exatas de função). `[Material: Huyen 2025, livro]`

- Plano detalhado é fácil de executar e difícil de gerar; quebra quando uma tool muda de nome
  ou de assinatura.
- Plano de alto nível é mais robusto a mudanças nas tools, mas precisa de um tradutor para
  chamadas concretas.
- O planejamento hierárquico combina os dois: primeiro o plano geral, depois o detalhamento
  de cada etapa.

## Fluxos de controle

| Fluxo | Descrição |
| --- | --- |
| **Sequencial** | Uma ação depois da outra; a segunda depende da primeira |
| **Paralelo** | Ações independentes executadas ao mesmo tempo |
| **Condicional (if)** | O resultado de um passo decide o próximo |
| **Laço (loop)** | Repetir até uma condição ser satisfeita |

`[Material: Huyen 2025, livro]`

## LLMs planejam?

O capítulo registra o debate em vez de resolvê-lo: `[Material: Huyen 2025, livro]`

- **LeCun** sustenta que LLMs autoregressivos não planejam.
- **Kambhampati** argumenta que eles extraem conhecimento útil para planos, mas os planos
  resultantes não são executáveis de modo confiável.
- **Hao et al. (2023)** apontam que planejar exige prever o estado resultante de cada ação, e
  propõem usar o próprio LLM como modelo de mundo.

`[A verificar]` Conferir no livro a formulação exata de cada posição antes de citá-las em
apresentação.

`[Interpretação]` Para a pesquisa, a pergunta útil é empírica: em que condições o plano
gerado é executável e correto, e com que frequência.

## Reflexão: ReAct e Reflexion

- **ReAct** intercala pensamento, ação e observação a cada passo. A reflexão acontece dentro
  da trajetória. `[Material: Yao et al. 2022]` Análise em
  [papers/2022-yao-react.md](../../papers/2022-yao-react.md).
- **Reflexion** separa a reflexão num momento próprio: depois de uma tentativa, um avaliador
  julga o resultado e o agente escreve o que aprendeu, para usar na tentativa seguinte.
  `[Material: Huyen 2025, livro]` `[A verificar]` Ler o artigo original (está no
  [ROADMAP](../../ROADMAP.md)).

A reflexão tem custo: mais tokens e mais latência a cada passo. `[Material: Huyen 2025, livro]`

## Perguntas em aberto

- Reflexão melhora o resultado ou só aumenta o número de tentativas? Qual o baseline justo?
  `[Hipótese]` Parte do ganho atribuído à reflexão pode vir de mais amostras.
- Em SLMs, o pensamento gerado ajuda ou consome contexto sem retorno?
