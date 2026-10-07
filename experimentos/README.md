---
titulo: Experimentos — o que conta como experimento
status: em construção
fontes: []
---

# Experimentos

Esta pasta guarda propostas e, no futuro, execuções. Antes de pôr algo aqui, classifico o
que estou fazendo. As distinções abaixo são `[Interpretação]` minha, para uso interno.

| Tipo | Pergunta que responde | Tem hipótese? | Tem baseline? | Onde fica |
| --- | --- | --- | --- | --- |
| **Protótipo / demonstração** | "Isso funciona? Como é por dentro?" | Não | Não | [`prototipos/`](../prototipos/) |
| **Experimento** | "A mudança X causa o efeito Y?" | Sim, refutável | Sim | `experimentos/` |
| **Benchmark** | "Como vários sistemas se comparam na mesma tarefa?" | Não necessariamente | Os próprios sistemas comparados | `experimentos/` |
| **Produção** | "Isso atende usuários reais de modo confiável?" | Não | Metas de serviço | fora do escopo |

Regras que sigo:

1. Uma demonstração que funcionou uma vez não é evidência de nada além de "é possível".
2. Um experimento define **antes** de rodar o que é resultado positivo e o que é inconclusivo.
3. Toda comparação informa custo (tokens e tempo) junto com acurácia.
4. Resultado negativo ou inconclusivo também é registrado.

## Propostas

- [ReAct em SLMs](propostas/react-em-slms.md)
- [Confiabilidade de tool calling em SLMs](propostas/confiabilidade-tool-calling-slm.md)
