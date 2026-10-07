---
titulo: Memória em agentes
status: rascunho — expandir com os materiais
fontes: [Huyen 2025 (livro, cap. 6)]
---

# Memória em agentes

## Três mecanismos

| Mecanismo | Onde está a informação | Persistência |
| --- | --- | --- |
| **Conhecimento interno** | Nos pesos do modelo | Só muda com novo treino |
| **Memória de curto prazo** | No contexto da conversa | Dura a execução; limitada pela janela |
| **Memória de longo prazo** | Em armazenamento externo, acessado por recuperação | Persiste entre execuções |

`[Material: Huyen 2025, livro]`

`[Interpretação]` A mesma informação pode estar em mais de um lugar. A decisão de projeto é
onde colocar cada coisa: o que é necessário em toda requisição vai para o contexto; o que é
raro e volumoso vai para o armazenamento externo.

## Por que um agente precisa de memória

- **Não estourar o contexto:** o que não cabe é guardado fora.
- **Persistir entre sessões:** sem isso, cada conversa começa do zero.
- **Manter consistência:** respostas anteriores ficam disponíveis para referência.

`[Material: Huyen 2025, livro]` `[A verificar]` Conferir a lista completa de motivos no livro.

## Gestão de memória

Quando o contexto enche, é preciso decidir o que sai: `[Material: Huyen 2025, livro]`

| Estratégia | Como funciona | Risco |
| --- | --- | --- |
| **FIFO** | Remove as mensagens mais antigas | O início da conversa costuma conter o objetivo |
| **Sumarização** | Substitui trechos antigos por um resumo | O resumo pode omitir o que seria necessário depois |
| **Reflexão** (Liu et al., 2023) | Depois de cada ação, o agente decide se a informação nova entra na memória, se funde com a existente ou se substitui algo desatualizado | Depende do julgamento do próprio modelo |

`[A verificar]` Confirmar no livro qual trabalho de Liu et al. (2023) é citado e completar a
entrada em `referencias/referencias.bib`.

`[Interpretação]` Toda estratégia de gestão é com perda. Para confiabilidade, o que foi
descartado e quando precisa ficar registrado, senão uma falha causada por informação perdida
não pode ser auditada.

## A verificar: memória episódica

`[A verificar]` Ainda não estudei como a divisão acima se relaciona com a taxonomia de
memória episódica, semântica e procedural usada em parte da literatura de agentes. Dúvidas:

- A memória de longo prazo descrita aqui corresponde à episódica (registro de experiências
  passadas), à semântica (fatos), ou a ambas sem distinção?
- Guardar trajetórias inteiras de execuções anteriores conta como memória episódica?

Tópico listado no [ROADMAP](../../ROADMAP.md).

## Perguntas em aberto

- Em sistemas multiagentes, a memória é compartilhada ou individual? O que muda na
  confiabilidade em cada caso? `[Hipótese]` Memória compartilhada propaga erros de um agente
  para os outros.
