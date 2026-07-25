# Framework de Inicialização de Projetos (GPS)

Este repositório contém o "Framework de Inicialização de Projetos" — uma metodologia em desenvolvimento para estruturar projetos de software desde a ideia até a implementação, usando documentação como fonte da verdade.

Principais objetivos:

- Estruturar qualquer projeto de software desde a ideia até a implementação.
- Definir fases claras de trabalho (00–06): Descoberta, Contexto Global, Estrutura Documental, Descoberta do Produto, Arquitetura, Implementação, Evolução.
- Usar documentação como base para orientar decisões e entregas.
- Trabalhar em conjunto com IAs (Claude, Cursor e outras) de forma organizada e consistente.
- Refinar o método continuamente a partir da experiência em projetos reais.

Como usar este repositório

1. Leia primeiro o documento mestre: `docs/framework/01-Contexto-Global.md`. Ele é a fonte da verdade do GPS.
2. Siga as fases na ordem recomendada:
   - `docs/framework/00-Descoberta.md` → validar problema
   - `docs/framework/01-Contexto-Global.md` → consolidar visão e restrições
   - `docs/framework/02-Estrutura-Documental.md` → como organizar docs
   - `docs/framework/03-Descoberta-do-Produto.md` → produto e critérios de aceite
   - `docs/framework/04-Arquitetura.md` → decisões técnicas (obrigatório antes da implementação)
   - `docs/framework/05-Implementacao.md` → entregar incrementos alinhados à arquitetura
   - `docs/framework/06-Evolucao.md` → feedback e ciclo de melhorias

Regras importantes (resumidas)

- Documento mestre: `docs/framework/01-Contexto-Global.md` — ler sempre antes de agir.
- Gate arquitetural: não avançar para implementação sem aprovação da Fase 04.
- Segurança / banco / permissões: qualquer mudança exige explicação de impacto e confirmação explícita da usuária.
- Nunca colocar senhas, tokens ou chaves em arquivos do repositório.
- Entregue soluções completas; indique arquivo e trecho exato; destaque em **negrito** o que puder quebrar em produção.

Colaboração com IAs

- Use os documentos como contexto primário ao interagir com agentes (Claude, Cursor, etc.). Sempre referencie o trecho relevante do Contexto Global ou da fase correspondente.
- Registre decisões, autores e aprovadores em `docs/framework/01-Contexto-Global.md` para manter rastreabilidade.

Contribuindo

- Atualize os documentos seguindo as regras do GPS.
- Para mudanças significativas no método, registre e justifique a alteração em `docs/framework/01-Contexto-Global.md`.
- Siga o fluxo de revisão do seu repositório (PRs, aprovações) antes de aplicar mudanças em produção.

Contato

Para dúvidas sobre o método ou solicitações de alteração, consulte a usuária responsável pelo GPS ou abra uma issue/PR com a justificativa.

