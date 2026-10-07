---
titulo: "ReAct: Synergizing Reasoning and Acting in Language Models"
status: rascunho — expandir com os materiais
fontes: [yao2022react]
---

# Yao et al., 2022 — ReAct

**Referência:** Yao, S.; Zhao, J.; Yu, D.; Du, N.; Shafran, I.; Narasimhan, K.; Cao, Y.
*ReAct: Synergizing Reasoning and Acting in Language Models.* arXiv:2210.03629.
<https://arxiv.org/abs/2210.03629>

> Análise escrita a partir das minhas anotações, sem o PDF aberto. Números e detalhes de
> tabelas estão marcados `[A verificar]` e precisam ser conferidos no artigo.

## Problema

Antes do ReAct, raciocínio e ação eram tratados em separado: Chain-of-Thought raciocina sem
consultar o mundo, e por isso pode alucinar fatos; agentes que só agem não têm onde manter um
plano nem interpretar o que observaram. `[Material: Yao et al. 2022]`

## Contribuição

Ampliar o espaço de ações do agente com **pensamentos**: `Â = A ∪ L`, em que `A` são as ações
sobre o ambiente e `L` é o espaço da linguagem. Um pensamento não altera o ambiente e não gera
observação; ele só atualiza o contexto que condiciona os passos seguintes.
`[Material: Yao et al. 2022]`

## Método

O modelo recebe exemplos few-shot de trajetórias no formato pensamento → ação → observação e
passa a gerar nesse formato. A cada ação, o ambiente devolve uma observação, que é anexada ao
contexto. `[Material: Yao et al. 2022]`

- Em tarefas de conhecimento, pensamento e ação se alternam a cada passo.
- Em tarefas de decisão, os pensamentos aparecem de forma esparsa, quando o modelo julga
  necessário.

`[Material: Yao et al. 2022]` `[A verificar]` Confirmar essa diferença na seção de método.

## Avaliação

| Benchmark | Tipo de tarefa |
| --- | --- |
| **HotpotQA** | Perguntas multi-hop |
| **FEVER** | Verificação de fatos |
| **ALFWorld** | Decisão em ambiente textual doméstico |
| **WebShop** | Decisão em navegação de compras |

`[Material: Yao et al. 2022]`

Baselines: prompting padrão, CoT, CoT com self-consistency, e ação sem pensamento
(act-only). `[Material: Yao et al. 2022]` `[A verificar]` Lista completa de baselines e o
modelo usado em cada experimento.

## Resultados

- **Tarefas de conhecimento:** o ReAct sozinho não supera o CoT de forma consistente; as
  melhores configurações combinam ReAct com CoT. `[Material: Yao et al. 2022]`
  `[A verificar]` Minha anotação diz "perde para CoT em tarefas de conhecimento". Preciso
  conferir se isso vale para os dois benchmarks ou só para o HotpotQA, e ajustar a frase.
- **Tarefas de decisão:** o ReAct supera o act-only. `[Material: Yao et al. 2022]`
- **Trade-off (Tabela 2):** o CoT erra mais por alucinar fatos; o ReAct erra mais por falha
  de raciocínio, incluindo trajetórias em que repete pensamentos e ações.
  `[Material: Yao et al. 2022]` `[A verificar]` Percentuais da tabela.
- **Modelos menores:** com prompting, o desempenho do ReAct cai; com fine-tuning, melhora e
  passa os outros métodos. `[Material: Yao et al. 2022]` `[A verificar]` Tamanhos dos modelos
  e quantidade de dados de fine-tuning.

`[Interpretação]` O último resultado é o mais relevante para o PDC: o formato ReAct é pesado
para modelos pequenos via prompt, e o ajuste fino muda o quadro. É o ponto de partida da
proposta [ReAct em SLMs](../experimentos/propostas/react-em-slms.md).

## Limitações

### Reconhecidas pelos autores

- Dependência dos exemplos few-shot e do limite de contexto.
- Erros de raciocínio e laços repetitivos.
- Uma busca que não retorna nada útil desvia a trajetória.

`[Material: Yao et al. 2022]` `[A verificar]` Conferir a lista na seção de discussão.

### Não discutidas

`[Interpretação]`

- **"Interpretabilidade" não é medida.** O artigo apresenta as trajetórias como mais
  interpretáveis, sem uma métrica nem um estudo com avaliadores que sustente isso.
- **Fidelidade dos pensamentos.** Nada garante que o pensamento escrito seja a causa da ação
  seguinte. Um pensamento plausível pode ser racionalização posterior.
- **Custo computacional não controlado.** O ReAct consome mais tokens e mais chamadas que os
  baselines; a comparação não é feita com orçamento igual.

## Relação com o PDC

- ReAct é **single-agent**, com tools e **sem memória persistente**. `[Interpretação]`
- Por isso serve como **baseline obrigatório** para qualquer comparação multiagente: se um
  SMA não supera um agente ReAct com as mesmas tools e o mesmo orçamento, a complexidade
  adicional não se justifica. `[Interpretação]`
- **ReAct ≠ MCP.** ReAct é um laço de controle (como o modelo decide o próximo passo). MCP é
  um protocolo de interface (como as tools são expostas). Um agente ReAct pode consumir tools
  via MCP; um não substitui o outro. `[Externo]`

## Perguntas em aberto

- Os pensamentos causam as ações? Como testar: intervir no pensamento e ver se a ação muda.
  `[Hipótese]`
- Com orçamento de tokens igualado, a vantagem em tarefas de decisão se mantém?
- O resultado de fine-tuning em modelos menores se reproduz em SLMs abertos atuais?
