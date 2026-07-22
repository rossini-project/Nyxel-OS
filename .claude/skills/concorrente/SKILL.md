---
name: concorrente
description: >
  Analisa um concorrente (site, redes, oferta, preço, posicionamento) e devolve onde ele é forte,
  onde tem brecha, e como o usuário se diferencia. Use quando o usuário disser "/concorrente",
  "analisar concorrente", "o que o X faz", "como me diferencio do Y", "espionar a concorrência".
---

# /concorrente — Análise de concorrência

Pega um concorrente e devolve inteligência útil pra decisão — não relatório
genérico. Usa o contexto do negócio (`_memoria/empresa.md`, `estrategia.md`) pra
focar no que importa pro usuário.

## Workflow

1. Pedir o concorrente (nome + site/Instagram, se tiver). Se o usuário tiver
   acesso à web/ferramentas, buscar a oferta pública; senão, trabalhar com o que
   o usuário souber.

2. Mapear: o que ele vende, pra quem, faixa de preço (se visível), como se
   posiciona, pontos fortes da comunicação, e fraquezas/lacunas visíveis (reviews,
   o que não oferece).

3. Devolver:
```
━━━ [Concorrente] ━━━
Oferta: [o que vende / pra quem]
Preço: [faixa, se visível]
Forte em: [...]
Brechas: [onde deixa a desejar — sua oportunidade]

Como VOCÊ se diferencia: [2-3 ângulos reais, ligados ao seu negócio]
Ação sugerida: [o movimento concreto — preço, mensagem, oferta]
```

4. Oferecer registrar os achados úteis (ex: brecha a explorar) em `estrategia.md`
   ou `historico.md`.

## Regras
- Diferenciação tem que ser real e ancorada no negócio do usuário, não slogan.
- Não afirmar dados que não verificou (preço, faturamento) — marcar como estimativa.
- Foco em "o que faço com isso", não em descrição neutra do concorrente.
