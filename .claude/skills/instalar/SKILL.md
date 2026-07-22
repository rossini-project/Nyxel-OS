---
name: instalar
description: >
  Instala o Nyxel OS no negócio do usuário. Entrevista sobre empresa, tom de voz,
  foco atual, metas, finanças e identidade visual, e preenche toda a memória
  estruturada (`_memoria/*`), o `identidade/design-guide.md` e adapta o `CLAUDE.md`
  ao perfil. Configura também os hooks e ativa o painel automático. Use quando o
  usuário acabou de baixar/abrir o Nyxel OS e quer instalar, ou pedir "instalar",
  "rodar /instalar", "primeiro setup", "configurar o Nyxel OS".
---

# /instalar — Instalação do Nyxel OS

Primeiro comando que o comprador roda. **Não pode falhar e não pode soar
burocrático.** É uma conversa de descoberta: pergunta uma coisa por vez, escuta de
verdade, não enfileira tudo. O sistema sai daqui sabendo quem é a empresa, como
fala, onde está o foco, e com a identidade aplicada.

Tom da entrevista: acolhedor, de quem está montando algo valioso junto. O
comprador pode ser leigo em Claude Code — nunca usar jargão técnico sem explicar.

## Pré-checagem

### 1. Nome da pasta
Conferir `basename "$(pwd)"`. Se for `nyxel-os`, `Nyxel OS`, `nyxel-os-main` ou
genérico, avisar (sem travar):
> "Dica: quando terminarmos, renomeie esta pasta pro nome do seu negócio — ela
> passa a SER o seu negócio, não 'Nyxel OS'. Te lembro no fim. Bora?"

### 2. Já tem contexto?
Conferir se `_memoria/empresa.md` já tem conteúdo real (não placeholder). Se sim:
> "Já tem contexto preenchido aqui. Quer recomeçar do zero ou complementar o que
> falta?"
Setup limpo → seguir direto.

---

## Fase 1 — Perfil

> "Qual desses mais combina com o seu negócio?
> 1. Solopreneur / criador solo
> 2. Freelancer (atende clientes por projeto)
> 3. Agência / consultoria (equipe pequena, vários clientes)
> 4. Empresa estabelecida (com setores)"

A resposta ajusta a linguagem do `CLAUDE.md` e quais áreas enfatizar (ex:
freelancer usa muito `clientes/`; solopreneur foca marca pessoal).

---

## Fase 2 — Entrevista (uma pergunta por vez)

Esperar a resposta de cada uma antes de seguir. Resposta vaga → pedir concretude
**uma vez**, depois registrar o que vier.

**Negócio (→ `_memoria/empresa.md`):**
1. "Como você chama o que faz? (nome da empresa ou seu nome, se for marca pessoal)"
2. "O que sua empresa entrega, numa frase do jeito que você falaria pro vizinho?"
3. "Quem te paga? (perfil de cliente real, sem persona genérica)"
4. "Trabalha sozinho ou tem equipe? Que ferramentas já usa?"

**Voz (→ `_memoria/preferencias.md`):**
5. "Como você gosta de se comunicar — mais direto, mais formal, mais próximo?"
6. "Tem algo que você NÃO quer que apareça nos textos? (ex: emoji, jargão)"
7. "Se puder, cola aqui um texto seu de verdade (email, post) pra eu pegar a sua
   voz." _(opcional — se vier, guardar como exemplo)_

**Foco (→ `_memoria/estrategia.md`):**
8. "Qual a sua prioridade nº1 nos próximos meses?"
9. "O que mais trava o crescimento hoje — o teu gargalo?"
10. "Tem um marco concreto com data? (ex: fechar X clientes até tal mês)"

**Metas e finanças (→ `_memoria/metas.md` + `financeiro.md`):**
11. "Tem uma meta de receita mensal? (pode ser aproximada — pula se preferir)"
12. "Tem clientes ativos agora? Quantos, e algum com cobrança pendente?"
    _(se sim, registrar em `clientes.md` e `financeiro.md` de forma resumida)_

---

## Fase 3 — Identidade visual (→ `identidade/design-guide.md`)

> "Vamos dar o rosto da sua marca pro sistema. Você já tem identidade definida
> (cores, fontes, logo) ou quer que eu sugira uma do zero?"

- **Tem:** perguntar cores principais, fontes e onde está o logo; preencher o guia.
- **Não tem:** sugerir uma paleta + fontes do Google Fonts coerentes com o
  negócio, confirmar com o usuário, e registrar.

Se o usuário não quiser cuidar disso agora, deixar o guia marcado como pendente e
avisar que skills visuais vão pedir isso depois.

---

## Fase 4 — Escrever os arquivos

Preencher, com cirurgia (sem reformatar os modelos além do necessário):
- `_memoria/empresa.md`, `preferencias.md`, `estrategia.md`
- `_memoria/clientes.md`, `financeiro.md`, `metas.md` (com o que veio; senão deixa
  os modelos prontos pro uso)
- `identidade/design-guide.md`
- Ajustar o cabeçalho do `CLAUDE.md` ao perfil escolhido (sem quebrar as regras).

Confirmar cada bloco preenchido em uma linha curta (não despejar o arquivo todo).

---

## Fase 5 — Ativar e fechar

1. Confirmar que os hooks estão ativos (o painel vai abrir sozinho nas próximas
   sessões). Se o `settings.json` não estiver aplicado, instruir: "feche e reabra
   o Claude Code pra ativar as automações".
2. Lembrar de renomear a pasta pro nome do negócio (se ainda estiver genérica).
3. Fechar com um resumo de 3 linhas do que o sistema já sabe + o convite:
   > "Pronto. O Nyxel OS já conhece seu negócio. Rode `/painel` pra ver seu dia, ou
   > me diga o que vamos fazer."

## Regras

- Uma pergunta por vez. Nunca enfileirar. Conversa, não formulário.
- Nunca inventar dado de negócio — registrar só o que o usuário disse.
- O `/instalar` roda uma vez. Pra mudanças depois, é `/atualizar`.
- Se o usuário pular uma pergunta, seguir sem insistir — o sistema funciona
  parcial e melhora com o uso.
