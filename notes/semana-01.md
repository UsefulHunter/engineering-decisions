# Semana 1: fundamentos de system design e ADRs

**Meta da semana (~5–6h):** ter o vocabulário básico de escalabilidade e publicar o template de ADR + o ADR 0001.

## Roteiro

| # | Atividade | Fonte | Tempo |
| --- | --- | --- | --- |
| 1 | Ler "How to approach a system design interview question" e "Performance vs scalability", "Latency vs throughput" | [System Design Primer](https://github.com/donnemartin/system-design-primer) | 1h |
| 2 | Ler "Availability vs consistency" (CAP), "Consistency patterns" e "Availability patterns" | System Design Primer | 1h |
| 3 | Ler "Cache" (client, CDN, app, DB; cache-aside, write-through, write-behind) e "Asynchronism" (filas, back pressure) | System Design Primer | 1h30 |
| 4 | Ler o post original de Michael Nygard e a página do MADR | [adr.github.io](https://adr.github.io/) | 45min |
| 5 | Revisar o template de ADR e o ADR 0001 deste repositório; ajustar ao seu estilo | este repo | 45min |
| 6 | Publicar o repositório no GitHub | — | 15min |

## Perguntas para responder com suas palavras

Escreva as respostas abaixo depois de estudar. São elas que transformam leitura em aprendizado.

1. Qual a diferença entre um sistema lento para **um** usuário e um sistema lento **sob carga**? Qual métrica mostra cada caso?
2. Em uma partição de rede, quando faz sentido escolher disponibilidade (AP) em vez de consistência (CP)? Dê um exemplo de frontend em que consistência eventual é aceitável e outro em que não é.
3. Cache-aside vs write-through: qual o risco de dados velhos em cada um? Como isso aparece para o usuário na tela?
4. Quando uma fila resolve um problema e quando ela só esconde o problema?
5. Que decisão técnica você já viu ser rediscutida por falta de registro? (Responda de forma genérica, sem detalhes de empregador.)

## Minhas notas

<!-- Escreva aqui -->

## Ideias de ADRs futuros

- [ ] Estratégia de cache no cliente (React Query/SWR vs estado global)
- [ ] Monorepo vs multirepo para um produto fictício
