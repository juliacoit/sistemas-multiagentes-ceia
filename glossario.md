---
titulo: Glossário operacional
status: rascunho — expandir com os materiais
fontes: [Huyen 2025 (livro, cap. 6), Google Whitepaper Agents 2024, conhecimento externo]
---

# Glossário operacional

Cada termo tem uma definição **operacional**: como eu reconheceria ou mediria aquilo num
sistema real. As definições são `[Interpretação]` minha, salvo quando outro rótulo aparece.
Elas servem para eu usar os termos de modo consistente, não para fixar o uso da área.

## Arquiteturas

| Termo | Definição operacional |
| --- | --- |
| **Workflow** | Sequência de passos cujo fluxo de controle está escrito no código. Reconheço porque consigo desenhar o grafo de execução antes de rodar. |
| **Pipeline** | Workflow linear: a saída de um passo é a entrada do seguinte, sem desvios decididos pelo modelo. |
| **Agente** | Sistema em que o modelo decide, em tempo de execução, qual ação tomar a seguir com base no que observou. Reconheço porque o número e a ordem dos passos variam entre execuções da mesma tarefa. |
| **Tool-using agent** | Agente cujas ações são chamadas a ferramentas externas. Reconheço pelo laço gerar chamada → executar → devolver resultado ao contexto. |
| **Planner / executor** | Separação em que um componente produz o plano e outro o executa. Reconheço porque o plano existe como artefato inspecionável antes de qualquer ação. |
| **Supervisor / worker** | Um componente distribui subtarefas e agrega resultados; os demais só respondem a ele. Reconheço porque os workers não se comunicam entre si. |
| **Hierarquia de agentes** | Supervisor/worker em mais de um nível. Reconheço pela árvore de delegação com profundidade maior que 1. |
| **Agentes peer-to-peer** | Agentes que trocam mensagens sem um coordenador fixo. Reconheço porque não há um nó pelo qual toda mensagem passa. |
| **Sistema multiagente (SMA)** | Ver a discussão em [notas/agentes/01](notas/agentes/01-o-que-e-um-agente.md). Critério provisório: mais de uma entidade com objetivo, estado e decisão próprios, cuja interação muda o resultado. `[Hipótese]` |
| **Agentic RAG** | Recuperação em que o modelo decide se, quando e o que buscar, podendo reformular e repetir a busca. Reconheço porque o número de buscas por pergunta não é fixo. |

## Estado e memória

| Termo | Definição operacional |
| --- | --- |
| **Sistema com estado** | Guarda informação entre passos de uma mesma execução. Teste: reiniciar no meio muda o comportamento. |
| **Sistema com memória** | Guarda informação entre execuções diferentes. Teste: uma segunda sessão se comporta de outro modo por causa da primeira. |

## Propriedades

| Termo | Definição operacional |
| --- | --- |
| **Autonomia** | Quantas decisões o sistema toma sem aprovação humana. Meço por passos executados por intervenção humana. |
| **Confiabilidade** | Não é uma medida única. Decomponho nas oito dimensões abaixo. |

### Dimensões de confiabilidade

| Dimensão | Como medir |
| --- | --- |
| **Correção** | Taxa de tarefas com resultado certo segundo um gabarito ou avaliador. |
| **Groundedness** | Fração das afirmações da resposta sustentadas por evidência recuperada ou observada. |
| **Robustez** | Queda de desempenho sob perturbação da entrada (paráfrase, ruído, tool indisponível). |
| **Consistência** | Variância do resultado em execuções repetidas da mesma tarefa. |
| **Observabilidade** | Fração dos passos (pensamentos, chamadas, resultados) que fica registrada e legível. |
| **Auditabilidade** | Possibilidade de reconstruir, a partir dos registros, por que uma ação foi tomada. |
| **Recuperação de erros** | Taxa de falhas intermediárias que o sistema detecta e corrige sozinho. |
| **Controle humano** | Existência de pontos de aprovação, interrupção e reversão, e se eles funcionam em teste. |

## Infraestrutura e modelos

| Termo | Definição operacional |
| --- | --- |
| **MCP** | Model Context Protocol: protocolo aberto que padroniza como uma aplicação expõe tools e contexto a um modelo. É interface, não estratégia de decisão. `[Externo]` `[A verificar]` detalhes na especificação. |
| **AgentOps** | Práticas de operação de agentes: registro de trajetórias, avaliação contínua, controle de custo. Reconheço pela existência de traces por execução. `[Externo]` |
| **SLM** | Small Language Model. Não há corte de tamanho consensual; aqui uso "modelo que roda localmente no hardware disponível ao projeto". `[Interpretação]` `[A verificar]` definição adotada pelo projeto. |
