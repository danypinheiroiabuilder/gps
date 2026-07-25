# SECURITY — Reporte e regras básicas

Objetivo: orientar como reportar vulnerabilidades e como tratar mudanças sensíveis.

1. Reporte de vulnerabilidades
- Para reportar uma vulnerabilidade ou exposição de dados, abra uma issue com label `security` e marque a usuária responsável.
- Inclua: descrição do problema, passos para reproduzir (se aplicável), evidências e impacto potencial.

2. Resposta e timelines
- Ao receber um reporte, um mantenedor deve confirmar o recebimento em 48 horas.
- Priorize correções de segurança com PRs de emergência quando necessário.

3. Regras de prevenção
- Nunca commit secrets (senhas, tokens, chaves). Use variáveis de ambiente e secrets managers.
- Automatize escaneamento de segredos no CI (ex.: truffleHog, git-secrets) quando possível.

4. Mudanças sensíveis
- Mudanças que afetem autenticação, autorização, banco de dados ou políticas de retenção requerem:
  - Issue de aprovação (`approval-request.md`)
  - Revisão de segurança por um responsável indicado
  - Plano de rollback documentado na PR

5. Contato de emergência
- Indique aqui o canal/usuária para reportes críticos (mencione por nome/email ou canal).

