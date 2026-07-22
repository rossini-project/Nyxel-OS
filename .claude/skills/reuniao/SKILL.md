---
name: reuniao
description: >
  Prepara uma reunião (pauta + pontos a partir do histórico do cliente) e, depois, registra as
  notas e gera os follow-ups e próximos passos. Use quando o usuário disser "/reuniao", "preparar
  reunião", "tenho call com X", "anotar a reunião", "o que falar na reunião".
---

# /reuniao — Preparo e follow-up de reunião

Dois momentos: ANTES (preparar) e DEPOIS (registrar e acionar). Lê o dossiê do
cliente em `_memoria/clientes.md` e `historico.md`.

## Modo ANTES — preparar
1. Identificar o cliente e o objetivo da reunião.
2. Puxar o contexto (status, pendências, última interação, valores).
3. Entregar:
```
Reunião: [cliente] — [objetivo]
Contexto rápido: [onde a relação está]
Pauta sugerida:
  1. [...]  2. [...]  3. [...]
Pontos a confirmar / perguntar: [...]
Resultado ideal: [o que sair de lá]
```

## Modo DEPOIS — registrar
1. Pedir as notas (ou o usuário cola o que rolou).
2. Estruturar: decisões tomadas, pendências, prazos.
3. Atualizar `clientes.md` (próximo passo + status) e `historico.md` (o que foi
   decidido, com data).
4. Gerar os follow-ups: mensagens/tarefas (oferecer `/cobranca` ou `/proposta` se
   for o caso).

## Regras
- Pauta curta e focada no resultado — não roteiro genérico de reunião.
- Toda decisão/pendência vira registro em `clientes.md`/`historico.md` (closed-loop).
- Não inventar o que foi dito — estruturar só o que o usuário relatou.
