# ADR 0001 — Uso de banco relacional para o Atlas Vivo de Simbologia

Data: 2026-07-24
Status: proposta

## Contexto
O projeto busca registrar fichas simbólicas com campos estruturados e relações entre fichas para permitir consultas e cruzamentos. É necessário escolher um armazenamento que suporte consultas por campos, relacionamentos e import/export simples.

## Decisão
Usar um banco de dados relacional (Postgres) como armazenamento inicial para o Atlas Vivo de Simbologia.

## Alternativas consideradas
- Alternativa A — Graph DB (ex.: Neo4j): bom para travessias de grafos e consultas de caminho; porém aumenta complexidade operacional e o custo inicial de integração.
- Alternativa B — Document DB (ex.: MongoDB): flexible schema, fácil iteração, mas menos adequado para joins e garantias de integridade entre relações.
- Alternativa C — Arquivo local (Obsidian/Markdown): mais simples e sem infra, mas dificulta consultas estruturadas e export/import robusto.

## Trade-offs e justificativa
- Postgres oferece queries SQL, joins eficientes e maturidade operacional (backups, ferramentas). Para o MVP, as consultas requeridas (filtros por campos e relações simples) cabem bem em um esquema relacional com tabelas para fichas e para relações.
- Se no futuro for necessário otimizar travessias complexas de grafo, podemos adicionar uma camada de indexação/graph engine ou migrar consultas específicas para um banco de grafos.

## Impacto
- Código / infra: necessidade de conexão ao Postgres, migrations e scripts de backup/export.
- Operações e deploy: exigir configuração mínima de banco (local ou hospedado) e política de backup.

## Plano de migração (se aplicável)
1. Projetar esquema inicial (tabelas: fichas, relacoes, tags, referencias).
2. Implementar migrations e testes locais.
3. Validar consultas típicas (ex.: buscar fichas relacionadas em 2 saltos).
4. Se necessário, prototipar consulta em Graph DB para avaliar ganho.

## Aprovado por:
- 

