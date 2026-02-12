Você é um Product Manager sênior e deve escrever um PRD (Product Requirements Document) completo, claro e acionável, em PT-BR, para a funcionalidade descrita a seguir.

### Descrição da funcionalidade (fonte)
"O modo Ask é para fazer perguntas e entender coisas, sem alterar seu código. Você pode perguntar sobre um arquivo específico, um erro, uma função, uma stack trace ou até conceitos gerais. O Cursor lê o contexto do projeto (arquivos abertos, seleção, etc.) e responde como um “mentor técnico”, explicando o que está acontecendo e por quê. Ele não modifica nada, só analisa e explica."

### Instruções de saída
Escreva o PRD com os tópicos abaixo, nesta ordem, usando Markdown, com linguagem objetiva e detalhes implementáveis:

1) **Resumo executivo**
- O que é o “Ask Mode”, para quem é, e qual problema resolve.
- Principais benefícios e diferenciais (ex.: não altera código).

2) **Contexto e motivação**
- Dor do usuário e cenário atual.
- Por que agora / oportunidade.

3) **Objetivos e não-objetivos**
- Objetivos mensuráveis.
- Itens explicitamente fora de escopo (ex.: edição automática de arquivos).

4) **Personas e casos de uso**
- Perfis (ex.: dev júnior, dev sênior, tech lead).
- 6–10 casos de uso concretos (ex.: “entender stack trace”, “explicar função”, “analisar arquivo X”, “explicar conceito”).

5) **Jornada do usuário e UX**
- Fluxo passo a passo (do clique/atalho até a resposta).
- Como o contexto é capturado (arquivos abertos, seleção, etc.).
- Estados: carregando, sem contexto suficiente, erro, resposta longa, resposta com trechos de código.
- Regras de apresentação (ex.: citações de trechos, referências a arquivos/linhas quando possível).

6) **Requisitos funcionais**
- Lista priorizada (P0/P1/P2).
- Comportamento do sistema: 
  - Garantia de “não modificar código”.
  - Tipos de perguntas suportadas.
  - Como lidar com ambiguidades (pedir mais contexto vs. assumir).
  - Como tratar stack traces e logs.
  - Como responder “como mentor técnico” (explicar o porquê, não só o quê).

7) **Requisitos não-funcionais**
- Performance (latência alvo), confiabilidade, segurança, privacidade.
- Observabilidade (logs, métricas, tracing).
- Limites (tamanho de contexto, número de arquivos, tokens).

8) **Políticas e guardrails**
- Regras para não sugerir alterações automáticas.
- Como sinalizar quando uma sugestão é hipotética.
- Redução de alucinação: exigir referências ao contexto quando aplicável.

9) **Dependências e suposições**
- IDE/editor, indexação, acesso a arquivos, permissões, etc.

10) **Métricas de sucesso**
- Adoção, retenção, satisfação, taxa de resolução, tempo para entendimento, etc.

11) **Riscos e mitigação**
- Ex.: contexto insuficiente, respostas incorretas, vazamento de dados, latência.

12) **Critérios de aceitação (Gherkin)**
- Pelo menos 8 critérios Given/When/Then cobrindo: perguntas sobre arquivo, função, erro, stack trace, conceitos gerais, falta de contexto, e garantia de não-modificação.

13) **Plano de rollout**
- Beta, flags, coleta de feedback, iteração.

14) **Perguntas em aberto**
- Liste 10+ dúvidas que precisam ser respondidas para implementar com segurança.

### Formato e qualidade
- Seja específico (não genérico).
- Inclua exemplos de interações (perguntas do usuário e respostas esperadas).
- Onde fizer sentido, proponha alternativas e justifique trade-offs.
- Não invente capacidades fora do texto; quando precisar assumir algo, marque como **Suposição**.
