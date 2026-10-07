---
titulo: RAG vs. tools — quando recuperar não basta
status: rascunho — expandir com os materiais
fontes: [Roteiro de apresentação (grupo de estudos), conhecimento externo]
---

# RAG vs. tools

Dois casos do roteiro em que a recuperação por similaridade não resolve a pergunta, e o que
resolveria.

## Caso 1 — "Qual a idade do último presidente?"

A recuperação dos top-n trechos por embeddings falha por dois motivos:
`[Material: Roteiro de apresentação]`

- **A pergunta exige informação atual.** "Último" depende de quando a pergunta é feita. O
  índice reflete o momento em que foi construído.
- **A pergunta é multi-hop.** É preciso primeiro descobrir quem é a pessoa, depois a data de
  nascimento, depois calcular a idade. A pergunta original não se parece com o trecho que
  contém a data de nascimento, então esse trecho não é recuperado.

`[Interpretação]` A solução exige decompor: buscar, ler o resultado, formular uma segunda
busca, calcular. É um laço de decisão, ou seja, comportamento de agente
([nota 01](01-o-que-e-um-agente.md)).

## Caso 2 — Cruzar as vendas de duas semanas

O top-k devolve os `k` trechos mais parecidos com a pergunta. Isso é uma **amostra**, não o
conjunto completo. `[Material: Roteiro de apresentação]`

Somar ou comparar vendas exige **todas** as linhas das duas semanas. Uma agregação exaustiva
pede SQL ou código como tool. `[Material: Roteiro de apresentação]`

`[Interpretação]` O erro aqui é silencioso: o modelo recebe algumas linhas, soma o que
recebeu e devolve um número plausível e errado. É parente da falha "tool válida com valores
incorretos" ([nota 05](05-modos-de-falha-e-avaliacao.md)).

## Regra prática

| A pergunta pede... | Mecanismo adequado |
| --- | --- |
| Um trecho que responde diretamente | Recuperação por similaridade |
| Informação atual | Busca na web ou API |
| Composição de vários fatos | Laço de busca decidido pelo modelo |
| Agregação sobre o conjunto inteiro | SQL ou código |

`[Interpretação]` Síntese minha dos dois casos.

## Exemplo de combinação: Claude Code

O Claude Code combina tools genéricas (um shell, que faz quase qualquer coisa) com tools
dedicadas (ler arquivo, editar arquivo, buscar). `[Externo]` O conjunto de tools de um
produto pode mudar com o tempo; conferir a documentação antes de citar. `[A verificar]`

`[Interpretação]` A tool genérica dá cobertura; a dedicada dá previsibilidade, porque tem
entrada e saída estruturadas e é mais fácil de validar e de auditar. É um trade-off entre
capacidade e controle.

## Perguntas em aberto

- Um SLM consegue escrever o SQL certo com confiabilidade suficiente, ou o caso 2 só troca um
  erro silencioso por outro?
- Onde termina o "agentic RAG" e começa um agente com tool de busca? Ver
  [glossário](../../glossario.md).
