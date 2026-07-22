---
name: mapear-rotinas
description: >
  Mapeia tarefas repetitivas do usuário e gera skills personalizadas pra automatizá-las.
  Entrevista curta sobre o que se repete toda semana, propõe skills concretas e cria as
  aprovadas em `.claude/skills/`. Use quando o usuário pedir "/mapear-rotinas", "criar skills
  personalizadas", "automatizar minhas tarefas" ou "o que dá pra automatizar".
---

# /mapear-rotinas — Tarefas repetitivas viram skills

Descoberta + criação. Transforma o que o usuário repete em automações ativas.

## Workflow

### Passo 1 — Descoberta (3 perguntas, uma por vez)
1. "Quais 3 tarefas você repete toda semana e queria não ter que pensar mais?"
2. "Pra cada uma, qual o input típico? (link, planilha, nome de cliente...)"
3. "E o output esperado? (5 slides, email pronto, PDF...)"

### Passo 2 — Conferir o que já existe
Ver se alguma tarefa já é coberta por uma skill nativa ou do Nyxel OS. Se sim:
> "A tarefa X já é resolvida por `/<nome>`. Quer usar essa em vez de criar nova?"

### Passo 3 — Proposta
Pra cada tarefa sem cobertura, propor:
```
### /<nome>
**O que faz:** [frase]   **Input:** [...]   **Output:** [...]
**Dependências:** [arquivos de _memoria/, identidade/, ferramentas]
```
Mostrar tudo junto e perguntar quais criar (todas / algumas / nenhuma / ajustar).

### Passo 4 — Criar as aprovadas
Pra cada uma: pasta `.claude/skills/<nome>/` + `SKILL.md` (frontmatter com `name` e
`description` de trigger claro, workflow em passos, dependências, regras). Calibrar
tom por `_memoria/preferencias.md` e `empresa.md`. Arquivos de apoio dentro da pasta.

### Passo 5 — Resumo
```
Criei [N] skills: ✓ /<nome1> ✓ /<nome2> ...
Pra usar: digita / e o nome em qualquer sessão. Pra ajustar: edita o SKILL.md.
```

## Regras
- Não criar skill pra tarefa de uma vez só — tem que ser repetível.
- Máximo 5 por sessão (mais → dividir em rodadas).
- Toda skill precisa de `description` com trigger claro, senão nunca é encontrada.
- Depende de ferramenta que o usuário não tem → avisar e oferecer versão simples.
