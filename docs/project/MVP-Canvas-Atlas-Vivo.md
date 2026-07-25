# MVP Canvas — Atlas Vivo de Simbologia (MVP)

## Nome do MVP
Atlas Vivo de Simbologia (MVP)

## 1. Objetivo
- Objetivo mensurável: permitir criar e relacionar fichas simbólicas estruturadas; meta inicial: 100 fichas interligadas em 30 dias.

## 2. Problema principal
- O conhecimento simbólico e esotérico é não-linear. Anotações estáticas não permitem visualizar a teia de conexões entre disciplinas (tarô, astrologia, mitologia).

## 3. Usuários / Personas
- Usuário principal: pesquisador individual / praticante (uso pessoal, laboratório fechado).

## 4. Proposta de valor do MVP
- Uma ferramenta pessoal que organiza fichas simbólicas com campos estritos e links, permitindo descoberta e navegação por relações sem exigir anotações manuais dispersas.

## 5. Hipótese de valor
- Se fornecermos fichas estruturadas e links entre elas, então o pesquisador encontrará padrões e conexões relevantes mais rápido, porque poderá consultar e cruzar campos de forma consistente.

## 6. Funcionalidades mínimas (backlog do MVP)
- Ficha (card) com campos obrigatórios: título, tipo (ex.: símbolo, entidade, fonte), descrição, tags, referências.
- Relacionamento entre fichas (link simples, tipo e nota sobre a relação).
- Busca por texto e filtros por tipo/tags.
- Interface simples para criar/editar fichas (formulário).
- Export/Import em JSON (backup/portabilidade).

## 7. Métricas de sucesso (KPI)
- Métrica primária: número de fichas interligadas (meta inicial: 100 em 30 dias).
- Métricas secundárias: tempo médio para criar uma ficha (< 5 min), taxa de reutilização de fichas (percentual de fichas referenciadas por outras).

## 8. Restrições / Dependências
- Sem upload de PDFs ou arquivos pesados no MVP.
- Sem visualizações gráficas complexas (apenas listas/tabelas e links).
- Uso estritamente pessoal (single‑user) — sem controle de multiusuário.
- Dependência técnica mínima: banco de dados local (Postgres ou equivalente embarcado).

## 9. Riscos principais
- Risco: modelo de dados inadequado para consultas de relações (impacto: médio) — Mitigação: escolher esquema com tabelas de relacionamento e índices; validar com consultas típicas antes de implantar.
- Risco: perda de dados por falta de backup (impacto: alto) — Mitigação: export/backup simples em JSON e instrução de backup automático.

## 10. Próximo passo (go/no-go)
- Decisor: Usuária responsável pelo GPS
- Critério de go: MVP Canvas preenchido + pelo menos 1 evidência (nota/entrevista) e aprovação da usuária.

