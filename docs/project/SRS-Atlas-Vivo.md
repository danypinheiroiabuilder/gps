# SRS — Atlas Vivo de Simbologia (One‑pager)

## 1. Visão resumida
- Projeto / módulo: Atlas Vivo de Simbologia (MVP)
- Objetivo: Oferecer um caderno virtual pessoal com fichas estruturadas e relações para pesquisa simbólica.

## 2. Escopo
- Incluído:
  - CRUD de fichas com campos estruturados
  - Relacionamento entre fichas (tabela de relações)
  - Busca por texto e filtros por tags/tipo
  - Export/Import JSON para backup/portabilidade
- Excluído:
  - Upload de PDFs e arquivos pesados
  - Visualizações gráficas complexas (grafo visual)
  - Multiusuário / permissões

## 3. Stakeholders
- Dono do Produto: Usuária responsável pelo GPS
- Usuário principal: pesquisador/praticante (uso pessoal)

## 4. Requisitos funcionais (nº, descrição, critério de aceite)
1. RF-001: Criar ficha — Deve permitir criar uma ficha com título, tipo, descrição, tags e referências. — Aceite: ficha aparece na listagem e é pesquisável pelo título.
2. RF-002: Editar/Excluir ficha — Deve permitir editar campos e excluir fichas (com confirmação). — Aceite: alterações persistem; exclusão remove relação ou solicita reassociação.
3. RF-003: Relacionar fichas — Permitir criar relações entre duas fichas com tipo de relação e nota. — Aceite: relação aparece na ficha e nas consultas relacionadas.
4. RF-004: Busca e filtro — Fornecer busca full‑text e filtros por tipo/tags. — Aceite: buscar por palavra-chave retorna fichas relevantes; filter por tag reduz resultados corretamente.
5. RF-005: Export/Import JSON — Exportar todo o banco de fichas e relações em JSON e importar de volta. — Aceite: import restaura as fichas e relações sem perda de campos.

## 5. Requisitos não-funcionais
- Performance: listagem de fichas paginada; resposta de busca < 300ms em dataset de 1k fichas.
- Segurança: dados armazenados localmente; nenhum segredo no repositório.
- Observabilidade: logs básicos de operações de criação/erro (local).

## 6. Fluxos principais (passos)
- Criar ficha → preencher campos obrigatórios → salvar → visualizar ficha.
- Relacionar fichas → selecionar ficha A → adicionar relação → salvar → verificar em ficha B.

## 7. Dependências técnicas
- Banco de dados relacional (Postgres recomendado) ou alternativa embarcada.
- Runtime: Node.js / Python (a definir pela implementação).

## 8. Critérios de aceite e teste
- Testes manuais: criar 10 fichas, relacionar 20 pares e verificar export/import.
- Testes automatizados: cobertura básica para operações CRUD e import/export.

## 9. Riscos e mitigação
- Risco: modelo de relações insuficiente — Mitigação: prototipar queries e ajustar esquema antes de migrar dados.

## 10. Histórico de versões / Aprovações
- Versão: 0.1 — Autor: (nome) — Aprovador: (a preencher) — Data: (a preencher)

