# Docs as Code — instruções e checklist básico

Objetivo: manter documentação confiável, versionada e validada automaticamente.

1) Estrutura sugerida
- `docs/` — documentação principal
- `docs/architecture/` — diagramas e decisões arquiteturais
- `docs/adr/` — ADRs
- `docs/templates/` — templates reutilizáveis

2) Ferramentas recomendadas
- Render: MkDocs ou Docusaurus (opcional, escolha por preferência)
- Validação: link-checker, markdownlint
- CI: pipeline que roda validação de links, markdownlint e verifica imagens faltando

3) Padrões mínimos
- Use templates para SRS, ADR, MVP Canvas.
- Sempre preencha metadata básica (autor, data, versão).
- Não escreva segredos nos docs.

4) Checklist de CI (sugestão)
- [ ] markdownlint passou
- [ ] link-checker passou (nenhum link quebrado)
- [ ] imagens referenciadas existem
- [ ] templates preenchidos quando exigido (ex.: ADR tem aprovador)

5) Integração com PRs
- Exija que PRs que modificam docs preencham o checklist do PR template.
- Automatize validações via CI e falhe a PR se link-checker ou markdownlint falharem.

