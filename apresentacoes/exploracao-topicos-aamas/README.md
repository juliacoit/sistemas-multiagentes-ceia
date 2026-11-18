---
titulo: "Apresentação — Exploração de tópicos (AAMAS 2027)"
status: rascunho
fontes: [notas/exploracao-aamas-2027/escolha-final.md, justificativas do formulário (rascunho de 16/11/2026)]
---

# Exploração de tópicos (AAMAS 2027)

Apresentação de **até 3 minutos, sem slides**, em **19/11/2026**, no encontro PDC 1 – Agentes
Inteligentes (14h–15h). `[Material: enunciado da atividade PDC]`
O conteúdo sai das justificativas do formulário. A preparação (leituras, o que aprender, o que
anotar) está em [preparacao.md](preparacao.md).

> Lembrete: 3 minutos dão cerca de 400 palavras faladas. O roteiro abaixo tem cerca de 360.
> Ensaiar com cronômetro.

## Estrutura

| # | Bloco | Mensagem | Tempo |
| --- | --- | --- | --- |
| 1 | Critério de escolha | Três tópicos ligados ao projeto: dois de GAAI, um de LEARN | ~0:15 |
| 2 | 1º tópico: memória | Memória de agente não é só RAG sobre documentos | ~0:45 |
| 3 | 2º tópico: falhas | Erro composto; ferramentas trocam um tipo de falha por outro | ~0:45 |
| 4 | 3º tópico: imitation learning | SLM ajustado com trajetórias é mais confiável que SLM só com prompt? | ~0:45 |
| 5 | Fio condutor e próximos passos | Os três tratam de como erros se propagam no tempo | ~0:20 |

## Roteiro de fala

Rascunho montado a partir das minhas justificativas do formulário. Ajustar para o meu jeito de
falar antes de ensaiar; a fala não precisa sair palavra por palavra.

1. **Critério de escolha.**
   Escolhi três tópicos ligados ao meu projeto no PDC, sistemas multiagentes confiáveis com
   SLMs. Dois são da área GAAI, onde já trabalho, e um é de LEARN, porque quero entender o lado
   do aprendizado em agentes.

2. **1º tópico: memória de longo prazo.**
   O primeiro é memória de longo prazo em agentes: como um agente guarda, atualiza e recupera
   informação além da janela de contexto e entre sessões. Trabalho com RAG no HerpIA, um
   chatbot para pesquisadores do RAN/ICMBio, e percebi que memória de agente não é só RAG
   sobre documentos. O agente precisa decidir o que guardar das interações, o que descartar e
   o que fazer quando uma informação fica desatualizada. Quero entender a diferença entre
   memória episódica, semântica e procedural, como no CoALA, e como medir se a memória melhora
   as decisões do agente, como faz o LongMemEval.

3. **2º tópico: detecção e recuperação de falhas.**
   O segundo é detecção e recuperação de falhas, que se liga ao "confiáveis" do projeto. Duas
   coisas me chamaram atenção. A primeira é o erro composto: com 95% de acerto por passo, uma
   tarefa de dez passos acerta só cerca de 60%. A segunda é que dar ferramentas ao agente
   troca um tipo de falha por outro: no ReAct, o agente alucina menos, mas entra mais em laços.
   Quero entender como classificar falhas de forma sistemática, por exemplo com a taxonomia
   MAST, e se SLMs locais, que falham mais, servem para testar mecanismos de recuperação.

4. **3º tópico: imitation learning.**
   O terceiro, de LEARN, é imitation learning: ajustar um SLM com trajetórias de um agente
   maior. No ReAct, modelos menores vão mal só com prompting, mas melhoram muito depois de
   ajustados com trajetórias. Minha pergunta é se um SLM ajustado assim é mais confiável do que
   um guiado só por prompt. Sei que minha base matemática ainda é limitada aqui: preciso de
   probabilidade e de MDPs. E quero entender onde termina o fine-tuning supervisionado e
   começa o aprendizado de agentes.

5. **Fio condutor e próximos passos.**
   O que liga os três é como erros se propagam no tempo: pela memória, pelos passos de uma
   tarefa e pelo aprendizado de um modelo que só imitou o especialista. Como próximo passo,
   quero ler esses papers por inteiro e pensar num primeiro experimento pequeno com SLMs
   locais.

> O bloco 5 depende das leituras da [preparação](preparacao.md#o-fio-condutor). Se eu não
> estiver segura da ligação com imitation learning, encerrar só com os próximos passos.

## Ensaios

| Data | Tempo | O que ajustar |
| --- | --- | --- |
|  |  |  |
|  |  |  |
|  |  |  |

## Perguntas prováveis

A coluna "Resposta curta" é minha: preencher com 1–2 frases depois das leituras. A coluna
"Pista" diz onde está a resposta.

| Pergunta | Resposta curta | Pista | Onde aprofundar |
| --- | --- | --- | --- |
| Memória de agente não é só RAG? |  | RAG = recuperar memória semântica que outra pessoa escreveu; memória episódica exige que o agente escreva (ação de aprendizado) | CoALA, seções 4.1, 4.3 e 4.5 |
| Como você avaliaria a memória do HerpIA? |  | Cinco habilidades do LongMemEval; atualização de conhecimento é a minha dúvida sobre informação desatualizada | LongMemEval, Tabela 1 e Seção 4 |
| A memória compartilhada propaga erros entre agentes? |  | Ainda é pergunta em aberto. O MAST cataloga a perda de histórico (FM-1.4), mas não a propagação por memória | Ficha do MAST |
| O MAST serve para um agente só? |  | Foi feito para multiagente e o paper não testa um agente só; FC2 não se aplica. Para um agente só, a divisão da Huyen | MAST, Seção 4; [nota de falhas](../../notas/agentes/05-modos-de-falha-e-avaliacao.md) |
| Por que testar recuperação de falhas com SLMs? |  | `[Hipótese]` falham mais, então geram casos a custo baixo. Risco: falhas de outro tipo | [Preparação, tópico 2](preparacao.md#tópico-2--detecção-e-recuperação-de-falhas) |
| A conta dos 60% supõe erros independentes? |  | Se 95% for o acerto condicional (dado que os passos anteriores acertaram), vale pela regra da cadeia | [Preparação, tópico 2](preparacao.md#tópico-2--detecção-e-recuperação-de-falhas) |
| O FireAct é imitation learning? |  | Os autores chamam de destilação; ajustar com demonstrações de especialista é behavioral cloning. Ganho de 77% é relativo (14,8 → 26,2 EM) | FireAct, Tabela 2 |
| Onde termina o fine-tuning supervisionado? |  | Quando os dados passam a depender das ações do próprio agente (DAgger) ou de recompensa (RL) | DAgger, abstract |
| Por que múltiplos agentes no seu projeto? |  | Ainda não sei se o problema precisa. O próprio MAST diz que os ganhos de MAS sobre agente único costumam ser pequenos | MAST, Abstract e Introdução |
| Se tivesse que escolher um só? |  | Memória: é onde tenho um caso concreto (HerpIA) | — |
