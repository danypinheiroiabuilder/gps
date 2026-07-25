# Fase 01 — Contexto Global

> **Documento mestre do GPS.** Deve ser lido sempre antes de qualquer decisão de fase, arquitetura ou implementação.

## 1. Por que essa fase existe?

O Contexto Global é a fonte única de verdade sobre o projeto: visão, restrições, stakeholders, critérios de sucesso e o estado atual do GPS. Sem ele, cada conversa reinicia do zero e as fases posteriores divergem. Tudo o que for decisão permanente ou restrição dura deve viver (ou ser referenciado) aqui.

## 2. Quais perguntas preciso responder?

- Qual é a visão do projeto em uma frase?
- Quais objetivos mensuráveis definem sucesso?
- Quem são os stakeholders e qual o papel de cada um (decide, usa, bloqueia, informa)?
- Quais restrições são inegociáveis (prazo, stack, compliance, orçamento, segurança)?
- Qual é o estado atual do GPS (fase ativa, o que está aprovado, o que está bloqueado)?
- O que já foi descartado e por quê?
- Onde estão os documentos das demais fases e qual é a fonte da verdade de cada tema?
- Quais riscos abertos ainda não têm mitigação?

## 3. O GPS da Fase

1. Consolidar a saída da Descoberta (00) em visão e objetivos.
2. Listar stakeholders com papéis e canais de decisão.
3. Registrar restrições duras e premissas explícitas.
4. Definir critérios de sucesso e métricas iniciais.
5. Manter um quadro de status do GPS (fase atual + aprovações).
6. Linkar os documentos das fases 02–06 e indicar o que está vigente.
7. Atualizar este arquivo a cada mudança material de escopo, restrição ou aprovação.

### Status do GPS (preencher por projeto)

| Fase | Status | Aprovado por | Data |
|------|--------|--------------|------|
| 00 Descoberta | | | |
| 01 Contexto Global | | | |
| 02 Estrutura Documental | | | |
| 03 Descoberta do Produto | | | |
| 04 Arquitetura | | | |
| 05 Implementação | | | |
| 06 Evolução | | | |

## 4. Controle de Qualidade/Checklist

- [ ] Visão do projeto escrita e revisada
- [ ] Objetivos e critérios de sucesso definidos
- [ ] Stakeholders e papéis mapeados
- [ ] Restrições e premissas documentadas
- [ ] Tabela de status do GPS preenchida e atualizada
- [ ] Links para as demais fases presentes e válidos
- [ ] Decisões descartadas registradas (para não reabrir sem motivo)
- [ ] Documento marcado como mestre e referenciado nas regras do agente (`.cursorrules`)
 
## Framework de Inicialização de Projetos (metodologia)

Este repositório adota o \"Framework de Inicialização de Projetos\" — uma metodologia em desenvolvimento para:

- Estruturar qualquer projeto de software desde a ideia até a implementação.
- Definir fases claras de trabalho (descoberta, contexto, arquitetura, desenvolvimento etc.).
- Usar documentação como base para orientar o desenvolvimento.
- Trabalhar em conjunto com IAs (Claude, Cursor e outras) de forma organizada e consistente.
- Refinar o método continuamente a partir da experiência em projetos reais.

O \"Framework de Inicialização de Projetos\" é o método: em vez de resolver um problema isolado, este projeto cria um processo reutilizável que poderá ser aplicado a projetos futuros.

Esta seção serve como declaração de intenção e fonte de verdade metodológica; qualquer alteração relevante do método deve ser registrada aqui e aprovada conforme as regras do GPS.
