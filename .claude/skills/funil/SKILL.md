---
name: funil
description: >
  Mostra e move o pipeline de vendas — todos os clientes/prospects por estágio, o que está
  parado e qual o próximo passo de cada um. Use quando o usuário disser "/funil", "pipeline",
  "meus prospects", "como está o funil", "quem falta responder".
---

# /funil — Pipeline de vendas

Visão de quem está entrando como cliente e onde cada negociação travou. Lê e
atualiza `_memoria/clientes.md`.

## Workflow

1. Ler `_memoria/clientes.md` e organizar por estágio:
   `prospect → proposta enviada → negociando → ativo`.

2. Mostrar o funil:
```
━━━ FUNIL ━━━
Prospect (N)
  - [Cliente] — [o que precisa] — próximo: [ação]
Proposta enviada (N)
  - [Cliente] — R$ [valor] — enviada [data] [se >7 dias: ⚠ follow-up]
Negociando (N)
  - [Cliente] — [pendência]
Ativo (N)
  - [Cliente]

Valor em jogo (proposta+negociando): R$ [soma]
```

3. Apontar o que está parado e sugerir a ação (ex: "3 propostas sem resposta há +7
   dias — quer que eu escreva os follow-ups com `/cobranca`?").

4. Se o usuário disser que algo mudou (fechou, perdeu, avançou), atualizar o status
   em `clientes.md` e registrar em `historico.md`.

## Regras
- Não inventar prospects — só o que está em `clientes.md`.
- Destacar follow-ups vencidos (proposta enviada há mais de ~7 dias sem resposta).
- Manter `clientes.md` como fonte única da verdade; toda mudança de estágio é
  gravada lá.
