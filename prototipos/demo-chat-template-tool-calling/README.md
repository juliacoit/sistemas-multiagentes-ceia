---
titulo: "Demonstração — chat template e tool calling num Qwen local"
status: demonstração — não implementada
fontes: [conhecimento externo]
---

# Demonstração: chat template e tool calling

> **Isto é uma DEMONSTRAÇÃO didática, não um experimento.** Não há hipótese, baseline nem
> métrica. O objetivo é ver o mecanismo por dentro. Nada observado aqui é evidência sobre
> confiabilidade; para isso existe a proposta
> [confiabilidade de tool calling](../../experimentos/propostas/confiabilidade-tool-calling-slm.md).

## Objetivo

Inspecionar, num modelo Qwen rodando localmente, o que acontece numa chamada de tool: o texto
que o modelo recebe e o texto que ele gera
([nota 02](../../notas/agentes/02-tools-e-function-calling.md)).

## O que observar

1. **O template.** Abrir o chat template do tokenizer e localizar o trecho que renderiza as
   tools.
2. **O prompt renderizado.** Aplicar o template a uma conversa com uma tool declarada e ler o
   texto resultante, sem tokenizar.
3. **O custo.** Contar os tokens do prompt com e sem tools para a mensagem "oi, tudo bem?".
4. **A geração.** Gerar a resposta a um pedido que exige a tool e imprimir a saída **sem**
   remover tokens especiais.
5. **O parsing.** Extrair nome e argumentos da saída com um parser mínimo e ver em que casos
   ele quebra.
6. **O retorno.** Anexar o resultado da função como mensagem e gerar a resposta final.

## Plano de implementação

- [ ] Escolher o modelo e o tamanho. `[A verificar]` Qual variante do Qwen cabe no hardware
  disponível.
- [ ] Script ou notebook com os seis passos acima.
- [ ] Registrar as saídas observadas num arquivo de notas nesta pasta.

Pesos de modelo não entram no repositório (`*.gguf` está no `.gitignore`).

## O que esta demonstração não mostra

- Com que frequência a chamada sai malformada.
- Se outro modelo ou outro template se comporta do mesmo modo.
- Qualquer coisa sobre agentes com mais de um passo.
