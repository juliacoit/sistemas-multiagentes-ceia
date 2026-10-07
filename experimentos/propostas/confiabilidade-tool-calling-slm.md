---
titulo: "Proposta — Confiabilidade de tool calling em SLMs"
status: proposta
fontes: [Huyen 2025 (livro, cap. 6), conhecimento externo]
---

# Confiabilidade de tool calling em SLMs

**Status: proposta, sem resultados.**

## Problema

Uma chamada de tool é texto amostrado que um parser precisa reconhecer
([nota 02](../../notas/agentes/02-tools-e-function-calling.md)). Em modelos pequenos, esse
texto sai malformado ou com a tool errada com mais frequência. Num agente, cada chamada
falha derruba a trajetória inteira
([erro composto](../../notas/agentes/05-modos-de-falha-e-avaliacao.md)).

## Hipóteses

- **H1.** Decodificação restrita por esquema (por exemplo, com a biblioteca `outlines`) reduz
  a taxa de chamadas malformadas em SLMs. `[Hipótese]`
- **H2.** Reduzir o inventário de tools apresentado ao modelo reduz a taxa de escolha da tool
  errada. `[Hipótese]`
- **H3.** A decodificação restrita **não** reduz, e pode aumentar, a taxa de chamadas bem
  formadas com valores incorretos. `[Hipótese]`

H3 é a que mais interessa: forçar o formato garante sintaxe, não garante que o valor esteja
certo, e transforma erros visíveis em erros silenciosos.

## Método

**Desenho fatorial 2 × 2**

| | Inventário completo | Inventário reduzido |
| --- | --- | --- |
| **Geração livre** | A (baseline) | B |
| **Decodificação restrita** | C | D |

**Fixos:** modelo, chat template, parâmetros de amostragem, conjunto de tarefas, sementes.

**Tarefas:** conjunto de pedidos com chamada esperada conhecida (nome e argumentos), incluindo
pedidos em que a resposta certa é **não** chamar tool nenhuma.

**Inventário reduzido:** definir antes como as tools são selecionadas (por exemplo, as `k`
mais relevantes por similaridade com o pedido). O seletor é um componente que também erra;
medir a taxa em que ele exclui a tool correta.

## Baseline

Condição A: geração livre com o inventário completo, usando o tool calling nativo do
template do modelo.

## Métricas

Seguem os tipos de falha da [nota 05](../../notas/agentes/05-modos-de-falha-e-avaliacao.md):

| Métrica | Definição |
| --- | --- |
| Taxa de malformação | Saídas que o parser rejeita / total |
| Tool inválida | Chamadas a tools inexistentes / chamadas |
| Parâmetros inválidos | Chamadas que violam a assinatura / chamadas |
| Valores incorretos | Chamadas bem formadas com argumento diferente do esperado / chamadas |
| Chamada indevida | Chamadas feitas quando o esperado era não chamar / casos sem tool |
| Custo | Tokens e tempo por pedido |

## Resultado positivo

- **H1:** a taxa de malformação em C e D fica abaixo da de A e B, fora do intervalo de
  confiança, sem queda na taxa de chamadas inteiramente corretas.
- **H2:** a taxa de tool errada em B e D fica abaixo da de A e C, descontados os casos em que
  o seletor excluiu a tool correta.
- **H3:** a taxa de valores incorretos em C e D é igual ou maior que em A e B.

## Resultado inconclusivo

- Malformação em A já próxima de zero (efeito teto): não há o que reduzir, e é preciso um
  modelo menor ou tarefas mais difíceis.
- Diferenças dentro da variação entre sementes.
- Conjunto de tarefas pequeno demais para separar os tipos de falha.
- O seletor de inventário erra tanto que o efeito de H2 não pode ser isolado.

## Ablação

- Variar o tamanho do inventário em mais de dois níveis.
- Trocar descrições longas das tools por curtas.
- Repetir com um segundo modelo, para saber se o efeito é do método ou daquele modelo.

## Riscos

- `[A verificar]` Compatibilidade do `outlines` com o servidor de inferência e com o formato
  de chamada do modelo escolhido.
- A decodificação restrita pode degradar a qualidade do conteúdo gerado; registrar isso como
  métrica, não como nota de rodapé.
