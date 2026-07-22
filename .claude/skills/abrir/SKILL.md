---
name: abrir
description: >
  Abre uma sessão de trabalho carregando a memória do negócio (empresa, preferências,
  estratégia, clientes, finanças, metas) e devolve um resumo curto. Use quando o usuário
  disser "abrir", "começar o dia", "/abrir", ou no primeiro turno de uma sessão.
---

# /abrir — Abertura de sessão

Curto e direto. Carrega contexto e devolve uma síntese pra começar a trabalhar.
Para uma visão operacional completa do dia, o usuário usa `/painel`.

## Workflow

1. Ler, em ordem: `_memoria/empresa.md`, `preferencias.md`, `estrategia.md`,
   `clientes.md`, `financeiro.md`, `metas.md`, e checar se `identidade/design-guide.md`
   está preenchido.

2. Se `empresa.md`, `preferencias.md` ou `estrategia.md` estiver em branco
   (placeholder), responder e parar:
   > "Vi que `_memoria/<arquivo>.md` ainda não foi preenchido. Quer rodar `/instalar`?"

3. Se preenchido, devolver UMA mensagem curta:
```
[Nome do negócio] — [o que faz em 5-8 palavras]
Foco atual: [prioridade da estratégia]
[Se houver: clientes ativos: N · cobrança pendente: R$ X]

Pronto. Quer ver o dia inteiro? Roda /painel. Ou me diz o que vamos fazer.
```

4. Não listar arquivos lidos. Não confirmar leitura. Só usar o contexto.

## Regras
- Resposta cabe em 6 linhas no terminal.
- Não fazer perguntas além do convite final.
- Se `design-guide.md` estiver em branco, não mencionar aqui — só vira problema
  quando uma skill visual for chamada.
