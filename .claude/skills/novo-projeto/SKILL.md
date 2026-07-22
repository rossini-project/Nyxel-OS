---
name: novo-projeto
description: >
  Cria uma pasta de projeto/cliente nova com `CLAUDE.md` dedicado, depois de uma entrevista
  curta, e registra o cliente em `_memoria/clientes.md`. Use quando o usuário disser "novo
  projeto", "novo cliente", "/novo-projeto", "começar projeto pra X".
---

# /novo-projeto — Pasta de projeto novo com contexto dedicado

Cria uma pasta com `CLAUDE.md` próprio que herda o contexto da raiz e adiciona o
específico do projeto. Já amarra o cliente ao CRM (`_memoria/clientes.md`).

## Workflow

### Passo 1 — Entrevista (4 perguntas, uma por vez)
1. "Nome do projeto ou cliente?"
2. "É cliente novo, projeto interno ou iniciativa pessoal?"
3. "Objetivo principal? (uma frase)"
4. "Que entregas vai ter? (ads, site, conteúdo, proposta, automação — pode ser várias)"

### Passo 2 — Local
- **Cliente novo:** `clientes/<Nome>/` (confirmar convenção no `CLAUDE.md` da raiz).
- **Projeto interno:** `projetos/<nome>/` (criar `projetos/` se não existir).
- **Iniciativa pessoal:** perguntar onde prefere.

### Passo 3 — Estrutura
Criar a pasta com `CLAUDE.md` do projeto, `briefing.md` (com o que foi coletado), e
subpastas só pras entregas mencionadas (ex: `ads/`, `conteudo/`).

### Passo 4 — CLAUDE.md do projeto
```markdown
# [Nome]
> Projeto criado em [data]. Instruções aqui sobrescrevem as da raiz quando relevante.
## Sobre
[objetivo]
## Tipo
[cliente novo / projeto interno / iniciativa]
## Entregas previstas
- [...]
## Contexto que herda da raiz
Herda tom, marca e contexto de `_memoria/` e `identidade/` da raiz. Não duplicar.
## Específico desse projeto
[vazio — preencher conforme descobrir]
```

### Passo 5 — Registrar no CRM
Se for cliente, adicionar um bloco em `_memoria/clientes.md` com status inicial
(`prospect` ou conforme o usuário disse), valor (se houver) e a pasta criada.

### Passo 6 — Resumo
```
Pasta criada: [caminho]
✓ CLAUDE.md + briefing.md  ✓ Subpastas: [lista]  ✓ Registrado em clientes.md
Quando for trabalhar nele, abre o terminal dentro da pasta.
```

## Regras
- Nome da pasta: manter reconhecível (acentos ok, espaço vira hífen).
- Não criar subpasta que não foi pedida.
- Pasta com mesmo nome já existe → avisar e perguntar.
