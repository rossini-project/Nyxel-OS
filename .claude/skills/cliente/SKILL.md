---
name: cliente
description: >
  Abre o dossiê de um cliente — tudo que o sistema sabe sobre ele (status, histórico, valores,
  pendências, arquivos) num só lugar, e atualiza o registro. Use quando o usuário disser
  "/cliente", "abrir cliente X", "como está o X", "ficha do cliente", "atualizar o X".
---

# /cliente — Dossiê do cliente

Visão 360º de um cliente, lendo `_memoria/clientes.md`, `financeiro.md`,
`historico.md` e a pasta `clientes/<Nome>/`.

## Workflow

1. Identificar de qual cliente se trata (o usuário diz o nome; se ambíguo, listar
   os de `clientes.md`).

2. Montar o dossiê:
```
━━━ [Cliente] ━━━
Status: [estágio]   ·   Desde: [data]
O que precisa: [...]
Valor: [proposta/contrato]   ·   Financeiro: [recebido / pendente]
Última interação: [data — o que rolou]
Próximo passo: [ação + quando]

Arquivos: [o que existe em clientes/<Nome>/]
Histórico: [últimos 2-3 eventos do historico.md ligados a ele]
```

3. Se o usuário trouxer novidade (reunião, pagamento, mudança), atualizar
   `clientes.md` (e `financeiro.md`/`historico.md` quando couber) com cirurgia.

4. Oferecer a próxima ação útil (ex: "quer que eu escreva o follow-up?" →
   `/cobranca`; "preparar a reunião?" → `/reuniao`).

## Regras
- Fonte da verdade é `clientes.md` — toda atualização é gravada lá.
- Não misturar dados de clientes diferentes.
- Se o cliente não existe ainda, oferecer criar com `/novo-projeto`.
