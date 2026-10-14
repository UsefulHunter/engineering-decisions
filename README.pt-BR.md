# engineering-decisions

🇺🇸 [Read in English](README.md)

Registro público de decisões técnicas: templates de **ADR** (Architecture Decision Record) e **RFC** (Request for Comments), mais exemplos completos escritos a partir de cenários fictícios.

O objetivo é praticar a escrita técnica de quem atua como Staff: explicar o contexto, comparar alternativas, assumir trade-offs e deixar um rastro que outra pessoa consiga entender meses depois.

> Todos os cenários deste repositório são fictícios ou baseados em informações públicas. Nenhum código, dado ou detalhe de empregador ou cliente é usado aqui.

## Estrutura

| Pasta | Conteúdo |
| --- | --- |
| [`templates/`](templates/) | Templates de ADR e RFC prontos para copiar |
| [`decisions/`](decisions/) | ADRs numerados (`NNNN-titulo-curto.md`) |
| [`rfcs/`](rfcs/) | RFCs completos, com alternativas, riscos e plano de rollout |
| [`notes/`](notes/) | Notas de estudo semanais que embasam as decisões |

Os documentos são escritos primeiro em português; as versões em inglês ficam ao lado, com o sufixo `.en.md`.

## ADR vs RFC

| | ADR | RFC |
| --- | --- | --- |
| **Quando** | Uma decisão já tomada (ou prestes a ser) | Uma proposta que precisa de discussão antes |
| **Tamanho** | 1 página | Várias páginas |
| **Foco** | O quê foi decidido e por quê | Problema, alternativas, riscos, rollout |
| **Ciclo de vida** | Imutável; é substituído por outro ADR | Evolui com comentários até ser aceito ou rejeitado |

Um RFC aceito normalmente gera um ou mais ADRs.

## Índice

### ADRs

| # | Título | Status |
| --- | --- | --- |
| [0001](decisions/0001-registrar-decisoes-de-arquitetura.md) | Registrar decisões de arquitetura com ADRs | Aceito |

### RFCs

_Em andamento (semanas 2–3)._

## Referências

- [Architecture Decision Records (adr.github.io)](https://adr.github.io/)
- [Documenting Architecture Decisions, Michael Nygard](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
- [MADR: Markdown Architectural Decision Records](https://adr.github.io/madr/)
- [Design Docs at Google](https://www.industrialempathy.com/posts/design-docs-at-google/)
- [System Design Primer](https://github.com/donnemartin/system-design-primer)
