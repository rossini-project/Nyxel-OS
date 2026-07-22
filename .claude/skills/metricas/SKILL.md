---
name: metricas
description: >
  Atualiza e lê os KPIs do negócio (receita, clientes, conversão, metas) fechando o loop entre
  o que foi feito e o resultado. Use quando o usuário disser "/metricas", "como estão os números",
  "atualizar metas", "bati a meta?", "quanto faturei", "minha conversão".
---

# /metricas — KPIs em closed-loop

O coração da tese do Nyxel OS: medir pra ajustar. Lê `_memoria/metas.md`,
`financeiro.md`, `clientes.md`, `historico.md` e devolve onde o negócio está vs.
onde quer chegar.

## Workflow

1. Calcular a partir da memória:
   - **Receita** do período (de `financeiro.md`) vs. meta.
   - **Clientes** ativos / novos no período (de `clientes.md`).
   - **Conversão** do funil (propostas enviadas × fechadas, do `historico.md`).
   - Progresso de cada meta de `metas.md`.

2. Mostrar:
```
━━━ MÉTRICAS · [período] ━━━
Receita: R$ [x] / R$ [meta]  ([%]) [🟢/🟡/🔴]
Clientes ativos: [n]  ·  Novos: [n]
Conversão de proposta: [fechadas]/[enviadas] = [%]
Metas: [cada uma com status]

Leitura: [1-2 frases — o que os números dizem]
Ajuste sugerido: [o que mudar na estratégia, ligado ao gargalo]
```

3. Atualizar `metas.md` com os valores atuais e os status (🟢/🟡/🔴).

4. Se um número revelar algo (ex: conversão baixa), sugerir a ação e oferecer
   registrar a hipótese em `historico.md` pra validar no próximo ciclo.

## Regras
- Só calcular com dados reais da memória. Faltou dado → dizer o que preencher
  (ex: "registre os recebimentos em financeiro.md pra eu calcular a receita").
- Fechar o loop: toda leitura termina com um ajuste acionável, não só números.
- Não maquiar — se está 🔴, dizer com clareza e propor saída.
