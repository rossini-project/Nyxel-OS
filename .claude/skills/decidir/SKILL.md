---
name: decidir
description: >
  Ajuda a tomar uma decisão de negócio usando o contexto real da empresa (estratégia, finanças,
  clientes, metas) em vez de conselho genérico. Pesa opções, mostra trade-offs e recomenda uma.
  Use quando o usuário disser "/decidir", "me ajuda a decidir", "qual a melhor opção", "vale a
  pena fazer X", "devo aceitar esse cliente/projeto".
---

# /decidir — Decisão com contexto do negócio

A diferença do Nyxel OS pra um chat comum: ele decide de DENTRO do negócio, não no
vácuo. Usa estratégia, caixa e metas reais pra recomendar.

## Workflow

1. Entender a decisão. Se o usuário não deu as opções, perguntar quais são (no
   máximo 1-2 perguntas).

2. Ler `_memoria/estrategia.md`, `financeiro.md`, `metas.md`, `clientes.md` e usar
   como critério real (caixa disponível, foco atual, capacidade, prazo).

3. Responder no formato:
```
Decisão: [a pergunta]

Opção A — [nome]
  + [prós ligados ao SEU contexto]
  − [contras]
Opção B — [nome]
  + ...   − ...

Recomendo: [A ou B]
Porque, dado [foco/caixa/meta atual], [razão concreta].
Risco a vigiar: [o principal].
```

4. Se a decisão tiver impacto registrável (aceitar cliente, investir valor),
   oferecer anotar em `_memoria/historico.md` pra fechar o loop depois.

## Regras
- Sempre dar UMA recomendação, não só "depende". Pode ressalvar, mas se posicionar.
- Ancorar nos dados reais da memória — citar o número/fato que pesou.
- Se faltar um dado decisivo (ex: não sabe o caixa), dizer que isso muda a resposta
  e pedir.
