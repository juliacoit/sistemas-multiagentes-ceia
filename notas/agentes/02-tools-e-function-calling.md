---
titulo: Tools e function calling
status: rascunho — expandir com os materiais
fontes: [Huyen 2025 (livro, cap. 6), Google Whitepaper Agents 2024, conhecimento externo]
---

# Tools e function calling

## Categorias de tools

Huyen agrupa as tools pelo que elas dão ao agente: `[Material: Huyen 2025, livro]`

| Categoria | Para que serve | Exemplos |
| --- | --- | --- |
| **Aumento de conhecimento** | Trazer contexto que o modelo não tem | Recuperador de texto, busca na web, consulta SQL |
| **Extensão de capacidade** | Cobrir o que o modelo faz mal | Calculadora, interpretador de código, conversor de unidades |
| **Ações de escrita** | Alterar o mundo | Enviar e-mail, gravar num banco de dados |

Ações de escrita são as que exigem mais cuidado, porque o efeito pode não ser reversível.
`[Interpretação]`

O whitepaper do Google usa outra taxonomia: `[Material: Google Whitepaper Agents]`

| Tipo | Onde executa |
| --- | --- |
| **Extensions** | Do lado do agente, que chama a API diretamente |
| **Functions** | Do lado do cliente: o modelo só produz nome e argumentos, e a aplicação decide executar |
| **Data Stores** | Acesso a dados externos, normalmente via busca vetorial |

`[Interpretação]` As duas taxonomias cortam por eixos diferentes: a de Huyen pergunta "para
quê", a do Google pergunta "quem executa e onde". Elas se combinam em vez de competir.

## Ponto central: o modelo não executa tools

O modelo só gera texto. O caminho completo de uma chamada: `[Externo]`

1. **Renderização.** O chat template (um template Jinja distribuído com o tokenizer)
   transforma as definições das tools em texto e as insere no contexto.
2. **Geração.** O modelo produz texto no formato de chamada que aprendeu no pós-treino.
3. **Parsing.** Um parser no servidor (em geral regex + JSON) extrai desse texto uma chamada
   estruturada: nome da função e argumentos.
4. **Execução.** O runtime da aplicação executa a função.
5. **Retorno.** O resultado volta ao contexto como uma nova mensagem, e o modelo continua.

Exemplos concretos dessa cadeia: o template no estilo Hermes, que delimita a chamada com
tags, e os parsers de tool calling do vLLM. `[Externo]` `[A verificar]` Conferir o formato
exato de cada um na documentação antes de citar.

Consequências: `[Interpretação]`

- Cada etapa falha de um jeito: template errado para o modelo, texto fora do formato, JSON
  inválido, função que lança exceção.
- "O modelo suporta tool calling" significa "foi treinado para emitir um formato que algum
  parser reconhece". Não há garantia de que o texto saia bem formado.
- Para SLMs, a etapa 2 é o ponto frágil, o que motiva a proposta
  [confiabilidade de tool calling](../../experimentos/propostas/confiabilidade-tool-calling-slm.md).

### Exemplo `lbs_to_kg`

Huyen ilustra com uma pergunta de conversão de libras para quilos. Com a tool `lbs_to_kg`
disponível, a resposta do modelo não é o número: é uma chamada com o nome da função e o
argumento em libras. Quem faz a conta é a função. `[Material: Huyen 2025, livro]`

## Custo em contexto

As definições das tools são renderizadas em **toda** requisição. Um "oi, tudo bem?" paga os
tokens de todas as tools declaradas, mesmo sem usar nenhuma. `[Externo]`

`[Hipótese]` Um inventário grande de tools prejudica também a escolha da tool certa,
sobretudo em modelos pequenos. É uma das variáveis da proposta de experimento acima.

## Modos de `tool_choice`

| Modo | Comportamento |
| --- | --- |
| `auto` | O modelo decide se chama uma tool |
| `required` | O modelo é obrigado a chamar ao menos uma |
| `none` | O modelo não pode chamar nenhuma |

`[Material: Huyen 2025, livro]`

## Perguntas em aberto

- Como cada servidor implementa `required`: por decodificação restrita ou só por instrução no
  prompt? `[A verificar]`
- Qual a taxa real de chamadas malformadas num SLM local? Ver
  [demonstração](../../prototipos/demo-chat-template-tool-calling/README.md) para inspecionar
  o mecanismo, e a proposta de experimento para medir.
