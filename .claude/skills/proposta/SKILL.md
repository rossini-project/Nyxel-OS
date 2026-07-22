---
name: proposta
description: >
  Cria uma proposta comercial profissional pra um cliente, na identidade visual da marca, a
  partir de uma entrevista curta. Gera HTML/PDF pronto pra enviar e registra no CRM. Use quando
  o usuário disser "/proposta", "fazer proposta", "proposta pra cliente X", "orçamento pro X".
---

# /proposta — Proposta comercial na identidade da marca

Transforma um briefing curto numa proposta que parece feita por uma agência —
aplicando `identidade/design-guide.md` e a voz de `_memoria/preferencias.md`.

## Workflow

### Passo 1 — Contexto
Checar se o cliente já existe em `_memoria/clientes.md` (puxar o que já se sabe).
Ler `identidade/design-guide.md` e `preferencias.md`.

### Passo 2 — Entrevista (só o que faltar)
1. "Pra quem é a proposta (cliente) e o que ele precisa?"
2. "O que você vai entregar? (escopo — itens)"
3. "Valor e forma de pagamento? (à vista / parcelado)"
4. "Prazo de entrega e validade da proposta?"

### Passo 3 — Montar a proposta
Gerar um HTML na identidade da marca (cores, fontes, logo do `design-guide.md`)
com as seções: capa (marca + nome do cliente), o problema/contexto, a solução
proposta, escopo detalhado, investimento, prazo, próximos passos, validade.
Texto na voz do usuário (sem jargão de pitch). Salvar em
`clientes/<Cliente>/proposta/Proposta - <Cliente> - <data>.html`.

### Passo 4 — PDF (se possível)
Oferecer converter pra PDF. Se houver ferramenta (ex: navegador/print, ou script
do workspace), gerar o PDF ao lado do HTML. Senão, instruir o usuário a abrir o
HTML e "imprimir como PDF".

### Passo 5 — Registrar
Atualizar `_memoria/clientes.md` (status → `proposta enviada`, valor, data) e
anotar em `_memoria/historico.md` ("proposta enviada pro X — R$ Y — aguardando").

## Regras
- Se `identidade/design-guide.md` estiver vazio, perguntar cores/fonte mínimas
  antes de gerar (ou sugerir e confirmar) — não entregar peça sem identidade.
- Não inflar escopo nem inventar entregáveis. Refletir o que o usuário disse.
- Valor sempre exatamente como o usuário definiu.
