---
titulo: Sistemas Multiagentes Confiáveis — caderno de pesquisa (PDC/CEIA-UFG)
status: em construção
fontes: [ver referencias/materiais.md]
---

# Sistemas Multiagentes Confiáveis — caderno de pesquisa

Caderno de estudos e de produção da Júlia no PDC 2026–2027 do CEIA-UFG (parceria EMBRAPII),
projeto "Sistemas Multiagentes Confiáveis e Small Language Models em Arquiteturas
Computacionais Abertas", linha de Sistemas Multiagentes Confiáveis (LLMs). Acompanha os grupos
de estudo de Agentes e de NLP Avançado.

## Objetivo

Estudar e guardar o que é produzido no programa com mentalidade de pesquisa: cada nota separa
o que uma fonte diz do que é interpretação minha, e cada ideia de experimento nasce com
hipótese, baseline e critério de resultado.

Este repositório **não** redistribui materiais de terceiros. PDFs e slides ficam fora do
controle de versão; aqui só entram referências e notas escritas com as minhas palavras.

## Como navegar

| Pasta | O que tem |
| --- | --- |
| [notas/](notas/) | Notas conceituais. Comece pelo [mapa conceitual](notas/00-mapa-conceitual.md). |
| [papers/](papers/) | Análises críticas de artigos, uma por arquivo, no formato do [template](papers/_template.md). |
| [reunioes/](reunioes/) | Um registro por encontro dos grupos de estudo: material prévio, perguntas, pendências. |
| [apresentacoes/](apresentacoes/) | Estrutura e roteiro das apresentações que fiz. |
| [experimentos/](experimentos/) | Propostas de experimento e, no futuro, execuções. |
| [prototipos/](prototipos/) | Demonstrações didáticas, sem hipótese nem baseline. |
| [referencias/](referencias/) | Bibliografia (`referencias.bib`) e lista dos materiais usados. |
| [glossario.md](glossario.md) | Termos com definição operacional. |
| [ROADMAP.md](ROADMAP.md) | Leituras e tópicos pendentes. |

## Convenção de rótulos

Toda afirmação relevante nas notas carrega a origem:

| Rótulo | Significado |
| --- | --- |
| `[Material: <fonte>]` | A fonte indicada afirma isso. |
| `[Externo]` | Conhecimento de fora dos materiais do grupo. |
| `[Interpretação]` | Leitura ou síntese minha a partir das fontes. |
| `[Hipótese]` | Conjectura ainda não testada. |
| `[A verificar]` | Ponto que precisa ser conferido na fonte antes de ser usado. |

Um rótulo no fim de um parágrafo ou de um item vale para o parágrafo ou item inteiro.

## Convenção de status

Todo arquivo `.md` começa com um cabeçalho com `titulo`, `status` e `fontes`.

- `rascunho — expandir com os materiais`: escrito a partir de tópicos-semente, ainda não
  conferido linha a linha contra a fonte.
- `revisado`: conferido contra a fonte.
- `proposta`: experimento planejado, sem resultados.
- `demonstração`: protótipo didático.

Reuniões são numeradas em sequência; a data só é preenchida quando confirmada.
