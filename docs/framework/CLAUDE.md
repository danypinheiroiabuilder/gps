# Guia para usar Claude com o GPS (PT‑BR, estilo otimizado para Claude)

Este arquivo traz um padrão de contexto e prompts em PT‑BR no estilo que funciona bem com Claude: instruções claras, estrutura de saída requerida e templates prontos para colar.

1) Como fornecer contexto (ordem e prioridade)
- Objetivo em 1 linha: qual a intenção da tarefa.
- Trecho do Contexto Global: cole a visão/restrições/fase atual (ou referencie `docs/framework/01-Contexto-Global.md`).
- Arquivos relevantes: liste caminhos e trechos curtos (ex.: `docs/framework/04-Arquitetura.md` — seção X).
- Expectativa de saída: formato (resumo, checklist, ADR, diffs) e nível de detalhe.

2) Regras essenciais de segurança
- Nunca inclua segredos (API keys, senhas) nos prompts — use `YOUR_API_KEY` como placeholder.
- Para qualquer dado sensível, peça validação humana antes de escrever no repositório.

3) Formato de resposta (sempre peça)
- Solicite seções claras: "Resumo", "Recomendações", "Ações Sugeridas", "Riscos" e "Referências".
- Para mudanças de código peça: arquivos afetados + trechos sugeridos (diff em markdown ou linhas aproximadas).

4) Templates de prompt (PT‑BR, prontos para colar)

Template — Revisão de proposta arquitetural
```
Você é um assistente técnico. Em até 300–500 palavras, avalie a proposta abaixo quanto a coerência com o Contexto Global e riscos.

Contexto:
- Objetivo: <uma linha com objetivo>
- Contexto Global: <cole trecho relevante do docs/framework/01-Contexto-Global.md ou referencie o arquivo>
- Arquitetura proposta: <cole ou resuma a seção de docs/framework/04-Arquitetura.md>

Tarefas:
1) Liste até 5 pontos fortes da proposta.
2) Liste até 5 riscos ou lacunas, priorizados por impacto (alto→baixo).
3) Para cada risco, proponha uma mitigação prática (1–2 frases).

Formato de saída:
- Use markdown com as seções: 'Resumo', 'Pontos Fortes', 'Riscos', 'Mitigações', 'Ações Recomendadas'.
```

Template — Gerar ADR
```
Você ajudará a redigir um ADR.
Contexto: <1–2 linhas que descrevem o problema técnico>
Decisão proposta: <frase curta>
Gere um ADR com: título, data, status (proposta/aprovada/recusada), contexto, decisão, alternativas consideradas, trade‑offs, impacto, plano de migração (se aplicável) e linha 'Aprovado por:' vazia.
```

Template — Solicitar patch (mudança de código)
```
Contexto: <objetivo curto>
Arquivos relevantes: <lista de caminhos>
Regras: não adicionar segredos; manter compatibilidade com a arquitetura aprovada.
Saída esperada: liste os arquivos e mostre trechos sugeridos (diff em markdown) ou explique linhas exatas a alterar.
```

5) Boas práticas (estilo Claude)
- Comece pedindo um resumo de 2–3 linhas antes de gerar saídas longas.
- Peça explicitamente que liste incertezas e suposições.
- Solicite referências ou linhas dos docs citados (ex.: 'veja `01-Contexto-Global.md` linha X–Y').
- Em decisões de segurança/dados, exija validação humana antes de qualquer commit.

6) Entregáveis prontos para PR
- Peça que o agente gere, ao final, um checklist curto copiável para a PR/issue (ex.: Gate da Fase 04, impacto em DB, testes necessários).

Exemplo rápido (workflow)
1. Cole o objetivo e contexto (Contexto Global + seção de arquitetura).  
2. Cole o template "Revisão de proposta arquitetural".  
3. Peça: "Resuma em 3 linhas e depois execute as tarefas".  
4. Revise a resposta, solicite ajustes e peça o checklist final para PR.

-- Fim --
-- Fim --

