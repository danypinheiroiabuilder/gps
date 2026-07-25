# Exemplo C4 — diagrama de contexto simples (modelo)

Este arquivo mostra um exemplo mínimo de como documentar um diagrama C4 em texto e onde colocar artefatos (imagens/diagrama gerado).

1) Diagrama de contexto (Nivel 1) — descreva em texto:
- Sistema: NomeDoSistema — descreva funcionalidade curta.
- Pessoas: UsuarioFinal, Admin
- Sistemas externos: ServiçoAuth, BancoDados
- Conexões: Usuario → Sistema (usar autenticação), Sistema → ServiçoAuth (token)

2) Diagrama de Container (Nivel 2) — listar containers e responsabilidades:
- WebApp (React) — interface do usuário
- API (Node/Python) — lógica de negócio e orquestração
- Banco (Postgres) — dados relacionais
- Worker/Jobs — processamento assíncrono

3) Como anexar o diagrama:
- Gere imagem (ex.: Structurizr, C4-PlantUML, draw.io) e coloque em `docs/architecture/diagramas/`.
- No documento, adicione link para a imagem e legenda com as principais decisões.

4) Exemplo de nota de design:
- "O WebApp comunica-se com a API via HTTPS; a API usa filas para tarefas longas; o Postgres é regional e exige backups diários."

