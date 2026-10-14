# engineering-decisions

🇧🇷 [Leia em português](README.pt-BR.md)

A public log of technical decisions: **ADR** (Architecture Decision Record) and **RFC** (Request for Comments) templates, plus complete examples written from fictitious scenarios.

The goal is to practice the kind of technical writing expected at Staff level: explain the context, compare alternatives, own the trade-offs and leave a trail that someone else can follow months later.

> Every scenario in this repository is fictitious or based on public information. No code, data or details from any employer or client are used here.

## Structure

| Folder | Contents |
| --- | --- |
| [`templates/`](templates/) | Ready-to-copy ADR and RFC templates |
| [`decisions/`](decisions/) | Numbered ADRs (`NNNN-short-title.md`) |
| [`rfcs/`](rfcs/) | Full RFCs with alternatives, risks and rollout plan |
| [`notes/`](notes/) | Weekly study notes behind the decisions (Portuguese only) |

Documents are written in Portuguese first; English versions sit next to them with the `.en.md` suffix.

## ADR vs RFC

| | ADR | RFC |
| --- | --- | --- |
| **When** | A decision already made (or about to be) | A proposal that needs discussion first |
| **Size** | 1 page | Several pages |
| **Focus** | What was decided and why | Problem, alternatives, risks, rollout |
| **Lifecycle** | Immutable; superseded by a new ADR | Evolves with comments until accepted or rejected |

An accepted RFC usually produces one or more ADRs.

## Index

### ADRs

| # | Title | Status |
| --- | --- | --- |
| [0001](decisions/0001-registrar-decisoes-de-arquitetura.en.md) | Record architecture decisions with ADRs | Accepted |

### RFCs

_In progress (weeks 2–3)._

## References

- [Architecture Decision Records (adr.github.io)](https://adr.github.io/)
- [Documenting Architecture Decisions, Michael Nygard](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
- [MADR: Markdown Architectural Decision Records](https://adr.github.io/madr/)
- [Design Docs at Google](https://www.industrialempathy.com/posts/design-docs-at-google/)
- [System Design Primer](https://github.com/donnemartin/system-design-primer)
