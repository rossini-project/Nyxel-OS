---
name: atualizar
description: >
  Varre o projeto e atualiza os arquivos de contexto do Nyxel OS (`_memoria/*`, `CLAUDE.md`,
  `identidade/design-guide.md`) que ficaram desatualizados em relação ao estado real do
  workspace. Use quando o usuário disser "atualiza", "/atualizar", "varre o projeto" ou
  pedir uma reconciliação geral.
---

# /atualizar — Varredura e atualização de contexto

Compara o que está nos arquivos de contexto com o estado real do workspace e
propõe atualizações.

## Workflow

### Passo 1 — Levantamento
Listar: pastas na raiz, subpastas em `clientes/`, skills em `.claude/skills/`,
arquivos recentes (últimos 30 dias) em `clientes/<x>/`, `marketing/`, `saidas/`.

### Passo 2 — Comparação
Conferir contra a realidade:
- `_memoria/empresa.md` — clientes / serviços / ferramentas batem?
- `_memoria/clientes.md` — todos os clientes com pasta estão registrados? Status atual?
- `_memoria/financeiro.md` — cobranças pendentes e recebidos coerentes?
- `_memoria/estrategia.md` + `metas.md` — foco e metas ainda fazem sentido (datas)?
- `_memoria/historico.md` — eventos recentes relevantes foram registrados?
- `CLAUDE.md` — regras e estrutura de pastas batem com o que existe?
- `identidade/design-guide.md` — coerente com as últimas peças geradas?

### Passo 3 — Proposta
Lista curta numerada do que atualizar, com a evidência de cada item. Perguntar:
> "Quer que eu aplique? Posso aplicar todas, escolher algumas, ou nenhuma."

### Passo 4 — Aplicação
Editar com cirurgia — só a linha relevante, sem reformatar o documento. Mostrar o
diff de cada mudança.

## Regras
- Não inventar fatos — só registrar o que tem evidência no workspace.
- Evidência ambígua (pasta vazia "Cliente Novo") → perguntar antes de adicionar.
- Não apagar conteúdo — só atualizar e adicionar.
- Nada a mudar → "Tá tudo coerente, nada pra atualizar".
