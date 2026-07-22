---
name: salvar
description: >
  Salva o trabalho do Nyxel OS no GitHub (commit + push). Na primeira vez configura o
  repositório remoto. Use quando o usuário disser "salvar", "salva no github", "commit",
  "push", "/salvar" ou pedir backup do trabalho.
---

# /salvar — Salvar no GitHub

Skill de uma função só: garantir que o trabalho está no GitHub. Fácil pra quem
nunca usou git.

## Workflow

### Primeira vez (repositório não inicializado)
Detectar com `git rev-parse --is-inside-work-tree`. Se falhar:
1. Perguntar:
   > "Primeiro backup. Você já tem um repositório no GitHub pra esse workspace?
   > 1. Sim, me passa a URL (ex: https://github.com/usuario/nome.git)
   > 2. Não, vou criar agora — me dá um nome (ex: meu-negocio)"
2. **Opção 1:** `git init` → `git add .` → `git commit -m "Setup inicial"` →
   `git branch -M main` → `git remote add origin <URL>` → `git push -u origin main`.
3. **Opção 2:** checar `gh --version`. Se tiver: `git init`, commit inicial,
   `gh repo create <nome> --private --source=. --push`. Se não: instruir a instalar
   o `gh` (cli.github.com) ou criar o repo em github.com/new e voltar com a URL.

### Commits seguintes (já configurado)
1. `git status`. Sem mudanças → "Tá tudo sincronizado" e parar.
2. Mostrar status curto e perguntar:
   > "Vou comitar tudo isso. Quer descrever a mudança numa frase ou uso resumo automático?"
3. Mensagem do usuário, ou gerar uma (1 linha: "Atualiza X" / "Cria proposta pra Y").
4. `git add .` → `git commit -m "<msg>"` → `git push`.
5. Confirmar com o link (de `git remote get-url origin`):
   > "Sincronizado. Ver no GitHub: <URL>"

## Regras
- Nunca usar `--force` sem o usuário pedir. Nunca `git reset --hard` sem confirmação.
- Push falhou por divergência → avisar e oferecer `git pull --rebase` antes.
- Sem `user.name`/`user.email` configurados → perguntar e configurar com
  `git config --global` na primeira vez.
