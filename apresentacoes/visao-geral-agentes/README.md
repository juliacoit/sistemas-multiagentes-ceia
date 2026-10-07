---
titulo: "Apresentação — Visão geral da área de agentes"
status: rascunho — expandir com os materiais
fontes: [Huyen 2025 (livro, cap. 6), Google Whitepaper Agents 2024]
---

# Visão geral da área de agentes

Apresentação de 8 minutos para o grupo de estudos de Agentes
([reunião 03](../../reunioes/03-visao-geral-agentes.md)).

**Slides:** _placeholder — exportar o deck em PDF e linkar aqui._ O PDF não entra no
repositório (ver `.gitignore`); o link deve apontar para um local externo.

## Estrutura dos 9 slides

Organizada por componentes do agente, com um exemplo condutor (Kitty Vogue) que reaparece em
cada parte.

> `[A verificar]` A ordem e os títulos abaixo são uma reconstrução a partir dos tópicos.
> Conferir contra o deck final.

| # | Slide | Mensagem | Tempo |
| --- | --- | --- | --- |
| 1 | Título e pergunta | O que faz um agente dar certo? | 0:30 |
| 2 | O que é um agente | Percebe o ambiente e age; definido por ambiente e ações | 0:50 |
| 3 | Exemplo condutor: Kitty Vogue | Uma tarefa que exige várias ações encadeadas | 0:50 |
| 4 | Tools | Três categorias: conhecimento, capacidade, escrita | 1:00 |
| 5 | Planejamento | Separar gerar, validar e executar o plano | 1:00 |
| 6 | Reflexão | ReAct e Reflexion: avaliar e corrigir durante a execução | 1:00 |
| 7 | Memória | Interna, curto prazo, longo prazo | 0:50 |
| 8 | Modos de falha | Planejamento, ferramenta, eficiência; erro composto | 1:10 |
| 9 | Síntese | Fórmula de sucesso e perguntas em aberto | 0:50 |

## Roteiro de fala

1. **Abertura.** A pergunta que organiza a fala: do que depende o sucesso de um agente?
2. **Definição.** A de Russell & Norvig. O que muda com LLMs é que as tools ampliam o conjunto
   de ações. `[Material: Huyen 2025, livro]`
3. **Kitty Vogue.** Apresentar a tarefa e mostrar que ela não se resolve com uma única
   resposta do modelo.
4. **Tools.** As três categorias, cada uma ilustrada no exemplo.
5. **Planejamento.** Por que validar o plano antes de executar.
6. **Reflexão.** O que ela acrescenta e quanto custa.
7. **Memória.** Onde fica cada tipo de informação.
8. **Falhas.** A falha mais difícil de detectar é a tool válida com valor incorreto. No
   exemplo Kitty Vogue, a falha é de **ferramenta**, não de planejamento. Erro composto:
   0,95^10 ≈ 0,60, com a ressalva de que a conta supõe erros independentes.
9. **Síntese.** Ver abaixo.

## Síntese

> Sucesso de um agente = tools disponíveis + força do planejador, amplificado por reflexão e
> memória.

`[Interpretação]` A síntese é minha. O capítulo afirma que o sucesso depende das tools e do
planejador `[Material: Huyen 2025, livro]`; o "amplificado por reflexão e memória" é a forma
como eu organizei o restante do conteúdo.

## Perguntas prováveis

| Pergunta | Resposta curta | Onde aprofundar |
| --- | --- | --- |
| Qual a diferença entre agente e workflow? | No workflow o código decide a sequência; no agente, o modelo decide em tempo de execução. | [nota 01](../../notas/agentes/01-o-que-e-um-agente.md) |
| O modelo executa a tool? | Não. Ele gera texto; um parser extrai a chamada e o runtime executa. | [nota 02](../../notas/agentes/02-tools-e-function-calling.md) |
| LLMs planejam de verdade? | É um debate aberto; a pergunta útil é com que frequência o plano é executável e correto. | [nota 03](../../notas/agentes/03-planejamento-e-reflexao.md) |
| 0,95^10 vale sempre? | Não. Supõe erros independentes e nenhuma correção. | [nota 05](../../notas/agentes/05-modos-de-falha-e-avaliacao.md) |
| Isso já é multiagente? | Depende do critério; contar cada componente como agente dilui o termo. | [nota 01](../../notas/agentes/01-o-que-e-um-agente.md) |
| RAG é uma tool? | Pode ser vista como tool de aumento de conhecimento; não serve para agregação. | [nota 06](../../notas/agentes/06-rag-vs-tools.md) |
| Como se avalia um agente? | Por trajetória: validade de planos e chamadas, passos, custo e tempo. | [nota 05](../../notas/agentes/05-modos-de-falha-e-avaliacao.md) |
