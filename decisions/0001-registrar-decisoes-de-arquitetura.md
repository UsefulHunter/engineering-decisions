# 0001. Registrar decisões de arquitetura com ADRs

🇺🇸 [English version](0001-registrar-decisoes-de-arquitetura.en.md)

- **Status:** Aceito
- **Data:** 2026-10-14
- **Decisores:** Brian Icaro

## Contexto

Decisões técnicas costumam ficar espalhadas em threads de chat, reuniões e na memória
de quem estava presente. Quando alguém novo chega (ou quando o próprio autor volta ao
assunto meses depois), a pergunta "por que isso foi feito assim?" não tem resposta
confiável. O resultado é refazer discussões já encerradas ou, pior, reverter uma decisão
sem conhecer o motivo original.

Este repositório precisa de um formato padrão para registrar decisões de forma
curta, versionada e próxima do código.

## Fatores de decisão

1. Baixo atrito para escrever (se for caro, ninguém escreve)
2. Versionado junto com o código e revisável por pull request
3. Fácil de ler por alguém sem contexto
4. Histórico preservado: decisões antigas não são apagadas, são substituídas

## Opções consideradas

1. **ADRs em Markdown no repositório** (formato de Michael Nygard, com campos do MADR)
2. **Wiki ou ferramenta de documentação externa**
3. **Não registrar formalmente** (descrições de PR e conversas)

## Decisão

> Escolhemos **ADRs em Markdown dentro do repositório**, usando o template em
> [`templates/adr-template.md`](../templates/adr-template.md).

É a opção com menor atrito (fator 1) e a única que atende ao fator 2 sem esforço extra:
o ADR passa pelo mesmo fluxo de revisão do código. O template mistura a estrutura
enxuta de Nygard (contexto, decisão, consequências) com os campos explícitos do MADR
(fatores de decisão, opções, prós e contras), o que ajuda no fator 3.

## Consequências

### Positivas

- Cada decisão relevante tem um "porquê" pesquisável com `git log` e busca no repositório
- Decisões entram em code review, o que abre espaço para discussão assíncrona
- O índice no README vira um mapa da evolução da arquitetura

### Negativas / trade-offs aceitos

- Exige disciplina: ADR não escrito é igual a ADR inexistente
- Markdown no repositório é menos amigável para pessoas não técnicas do que uma wiki
- Decisões que cruzam vários repositórios precisam de um lugar central (como este)

### Riscos e mitigação

| Risco | Probabilidade | Impacto | Mitigação |
| --- | --- | --- | --- |
| ADRs virarem burocracia para decisões triviais | Média | Médio | Regra prática: só registrar decisões caras de reverter ou que afetam mais de um time |
| ADRs ficarem desatualizados | Média | Alto | Nunca editar a decisão; criar um novo ADR que substitui o anterior e atualizar o status |

## Regras de uso

- Numeração sequencial com 4 dígitos: `NNNN-titulo-em-kebab-case.md`
- Um ADR aceito é imutável. Mudou de ideia? Novo ADR com status "Substitui NNNN"
- Correções de digitação e links são permitidas

## Como validar

Depois do Bloco 1 (3 semanas), revisar: os ADRs escritos foram úteis para redigir o RFC?
Alguém sem contexto entende cada decisão lendo só o ADR?

## Links

- [Documenting Architecture Decisions, Michael Nygard (2011)](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
- [MADR](https://adr.github.io/madr/)
- [adr.github.io](https://adr.github.io/)
