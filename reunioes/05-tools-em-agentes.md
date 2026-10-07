---
titulo: "Reunião 05 — Tools em agentes"
status: rascunho — expandir com os materiais
fontes: [Roteiro de apresentação (grupo de estudos), Huyen 2025 (livro, cap. 6), Google Whitepaper Agents 2024]
grupo: Agentes
data: a confirmar
---

# Reunião 05 — Tools em agentes

## Tema

Como um modelo "chama" uma tool, quando recuperação não basta, e como produtos reais combinam
tools.

## Material prévio

- "Roteiro de apresentação" ([referencias/materiais.md](../referencias/materiais.md)).
- Capítulo 6 de *AI Engineering* (Huyen, 2025), seção de tools.
- Whitepaper "Agents" do Google, seção de ferramentas.

## Minhas perguntas, por bloco

> `[A verificar]` Os blocos abaixo foram montados a partir dos tópicos que anotei. Falta
> conferir contra o roteiro se a divisão e a ordem dos blocos são essas.

### Bloco 1 — Quando o RAG não basta

- Por que o top-n por embeddings falha em "qual a idade do último presidente"?
- Por que o top-k não serve para cruzar as vendas de duas semanas?
- O que distingue uma pergunta de recuperação de uma pergunta de agregação?

### Bloco 2 — O que é uma tool

- Como as categorias de Huyen (conhecimento, capacidade, escrita) se relacionam com as do
  Google (Extensions, Functions, Data Stores)?
- Quem executa a chamada em cada caso?

### Bloco 3 — Como o modelo chama uma tool

- Se o modelo só gera texto, em que ponto o texto vira execução?
- O que o chat template faz com as definições das tools?
- O que acontece quando o texto gerado não é um JSON válido?
- Quanto custa, em tokens, declarar tools que não são usadas?

### Bloco 4 — Tools em produtos reais

- Por que o Claude Code combina um shell genérico com tools dedicadas?
- O que se ganha e o que se perde com cada tipo?

## O que foi discutido

_A preencher a partir das minhas anotações do encontro._

## O que ficou em aberto

- Como cada servidor implementa `tool_choice: required`. `[A verificar]`
- Taxa de chamadas malformadas em SLMs: vira a proposta
  [confiabilidade de tool calling](../experimentos/propostas/confiabilidade-tool-calling-slm.md).

## Notas relacionadas

- [notas/agentes/02](../notas/agentes/02-tools-e-function-calling.md)
- [notas/agentes/06](../notas/agentes/06-rag-vs-tools.md)
