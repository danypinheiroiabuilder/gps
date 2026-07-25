# CONTRIBUTING (Guia de Contribuição)

Obrigado por contribuir com o Framework de Inicialização de Projetos (GPS). Este documento descreve o fluxo mínimo esperado para mudanças, donos e aprovações.

1. Antes de começar
- Leia o documento mestre: `docs/framework/01-Contexto-Global.md`. Ele é a fonte da verdade.
- Busque PRs e issues abertas que possam conflitar.

2. Abrindo uma issue
- Use labels apropriados (`bug`, `enhancement`, `arch-change`, `security`, `needs-approval`).
- Para mudanças que afetam arquitetura, segurança, banco de dados ou permissões, abra uma issue de aprovação usando o template `/.github/ISSUE_TEMPLATE/approval-request.md`.

3. Trabalhando em uma branch
- Crie branch com nome descritivo: `feat/<assunto>` ou `fix/<assunto>`.
- Mantenha PRs pequenos e focados (preferivelmente < 500 LOC).

4. Pull Request
- Use o template `.github/PULL_REQUEST_TEMPLATE.md` e preencha todos os campos.
- Se a PR tocar arquitetura, assegure que `docs/framework/04-Arquitetura.md` e ADRs relevantes estejam atualizados.
- Para mudanças sensíveis (segurança/banco/permissões) inclua a issue de aprovação e aguarde confirmação da usuária antes de mesclar.

5. Revisão e Aprovação
- Nomeie revisores apropriados. Um aprovador humano deve confirmar alterações arquiteturais ou impactantes.
- Atenda comentários do revisor e atualize a PR; marque quando estiver pronta para reavaliação.

6. Mesclagem e Releases
- Garanta que CI passe (incluindo validações de docs).
- Atualize `CHANGELOG.md` com um resumo curto da mudança em "Unreleased".
- Para mudanças em produção, documente notas de deploy/rollback na própria PR.

7. Regras importantes
- Nunca commit secrets em arquivos (senhas, tokens, chaves). Use placeholders (`YOUR_API_KEY`) e variáveis de ambiente.
- Siga `.cursorrules` para gates de fase e segurança.
- Para mudanças que mudem o método (GPS) registre a alteração em `docs/framework/01-Contexto-Global.md`.

8. Contatos
- Para aprovações e dúvidas sobre o método, consulte a usuária responsável pelo GPS (mencione no PR/issue).

