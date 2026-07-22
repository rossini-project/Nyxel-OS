---
name: cobranca
description: >
  Escreve mensagens de cobrança e follow-up no tom da marca — firmes mas cordiais — pra clientes
  com pagamento pendente ou propostas sem resposta. Use quando o usuário disser "/cobranca",
  "cobrar cliente", "lembrar pagamento", "follow-up", "mandar cobrança pro X".
---

# /cobranca — Cobranças e follow-ups que não soam chatos

Cobrar é desconfortável — o Nyxel OS escreve a mensagem certa, no tom certo, sem
queimar o relacionamento. Lê `_memoria/financeiro.md`, `clientes.md` e `preferencias.md`.

## Workflow

1. Identificar o alvo: o usuário disse o cliente, ou puxar de `financeiro.md`
   (cobranças pendentes/vencidas) e `clientes.md` (propostas sem resposta).

2. Para cada cobrança, perguntar/confirmar o canal (WhatsApp, email) e o tom
   (lembrete leve / firme / última tentativa).

3. Escrever a mensagem:
   - **Lembrete leve:** cordial, assume esquecimento, dá o caminho fácil de pagar.
   - **Firme:** objetivo, valor + vencimento + o que acontece, sem agressividade.
   - **Follow-up de proposta:** retoma valor, remove fricção, propõe próximo passo.
   Sempre na voz de `preferencias.md`. Curta. Pronta pra copiar e enviar.

4. Oferecer registrar a tentativa em `historico.md` (data + cliente + tipo) pra
   acompanhar a régua de cobrança.

## Regras
- Nunca ameaçar ou usar tom hostil. Firmeza ≠ grosseria.
- Valor e data exatamente como em `financeiro.md` — não inventar.
- Oferecer 1-2 variações de tom, não dez. Deixar o usuário escolher e enviar.
- Se já houver tentativas anteriores no histórico, escalar o tom com bom senso.
