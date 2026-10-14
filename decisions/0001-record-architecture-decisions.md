# 0001. Record architecture decisions with ADRs

🇧🇷 [Versão em português](0001-record-architecture-decisions.pt-BR.md)

- **Status:** Accepted
- **Date:** 2026-10-14
- **Deciders:** Brian Icaro

## Context

Technical decisions tend to be scattered across chat threads, meetings and the memory
of whoever was in the room. When someone new joins (or when the author returns to the
topic months later), the question "why was this done this way?" has no reliable answer.
The result is reopening settled discussions or, worse, reverting a decision without
knowing its original reason.

This repository needs a standard format for recording decisions that is short,
versioned and close to the code.

## Decision drivers

1. Low friction to write (if it is expensive, nobody writes it)
2. Versioned alongside the code and reviewable through pull requests
3. Easy to read for someone without context
4. History preserved: old decisions are not deleted, they are superseded

## Considered options

1. **Markdown ADRs in the repository** (Michael Nygard's format, with MADR fields)
2. **Wiki or external documentation tool**
3. **No formal record** (PR descriptions and conversations)

## Decision

> We chose **Markdown ADRs inside the repository**, using the template in
> [`templates/adr-template.md`](../templates/adr-template.md).

It is the lowest-friction option (driver 1) and the only one that meets driver 2 with no
extra effort: the ADR goes through the same review flow as the code. The template mixes
Nygard's lean structure (context, decision, consequences) with MADR's explicit fields
(decision drivers, options, pros and cons), which helps with driver 3.

## Consequences

### Positive

- Every relevant decision has a searchable "why" via `git log` and repository search
- Decisions go through code review, which opens room for asynchronous discussion
- The README index becomes a map of how the architecture evolved

### Negative / accepted trade-offs

- Requires discipline: an unwritten ADR is the same as no ADR
- Markdown in a repository is less friendly to non-technical people than a wiki
- Decisions spanning several repositories need a central place (like this one)

### Risks and mitigation

| Risk | Likelihood | Impact | Mitigation |
| --- | --- | --- | --- |
| ADRs turning into bureaucracy for trivial decisions | Medium | Medium | Rule of thumb: only record decisions that are expensive to reverse or affect more than one team |
| ADRs going stale | Medium | High | Never edit the decision; write a new ADR that supersedes the old one and update its status |

## Usage rules

- Sequential 4-digit numbering: `NNNN-title-in-kebab-case.md`
- An accepted ADR is immutable. Changed your mind? New ADR with status "Supersedes NNNN"
- Typo and link fixes are allowed
- The English file is the source; the `.pt-BR.md` file is its translation

## How to validate

After Block 1 (3 weeks), review: were the ADRs useful when writing the RFC?
Can someone without context understand each decision by reading only the ADR?

## Links

- [Documenting Architecture Decisions, Michael Nygard (2011)](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
- [MADR](https://adr.github.io/madr/)
- [adr.github.io](https://adr.github.io/)
