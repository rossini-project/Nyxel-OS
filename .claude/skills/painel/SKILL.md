---
name: painel
description: >
  Painel executivo do dia: lê toda a memória do negócio e devolve um resumo operacional com
  foco do dia, clientes que precisam de ação, dinheiro a receber, metas e alertas. É o comando
  de "bom dia" do Nyxel OS. Use quando o usuário disser "/painel", "painel", "meu dia",
  "resumo do dia", "como estão as coisas", ou no início de sessão se o usuário pedir visão geral.
---

# /painel — Painel executivo do dia

O comando mais importante do Nyxel OS no dia a dia. Lê o negócio inteiro e devolve
UM painel claro pra pessoa saber exatamente onde focar. Sem enrolação.

## Workflow

1. Ler: `_memoria/estrategia.md`, `clientes.md`, `financeiro.md`, `metas.md`,
   `historico.md`. (Empresa e preferências já estão no contexto da sessão.)

2. Montar o painel nesse formato (omitir seções vazias):

```
━━━ PAINEL · [data] ━━━
Foco do dia: [prioridade nº1 da estratégia]

🎯 Clientes que precisam de ação
- [Cliente] — [próximo passo pendente] [se atrasado: ⚠]

💰 Dinheiro
- A receber: R$ [soma das cobranças pendentes] ([N] cobranças)
- [cobrança vencida ou vencendo nos próximos 3 dias → destacar]

📈 Metas ([período])
- [meta]: [atual]/[alvo] [🟢/🟡/🔴]

⚡ Alertas
- [qualquer coisa atrasada, parada ou que precisa de decisão]

Sugestão: comece por [a ação de maior impacto pro foco atual].
```

3. Terminar com UMA recomendação acionável ligada ao foco da estratégia — não uma
   lista, a próxima ação certa.

## Regras
- Se a memória estiver vazia/placeholder, sugerir `/instalar` e parar.
- Cabe numa tela. Priorizar o que exige ação hoje; esconder o que está ok.
- Não inventar números — só o que está em `financeiro.md`/`metas.md`. Se faltar
  dado, dizer o que preencher.
- Marcar como atrasado o que passou da data em `clientes.md`/`financeiro.md`.
