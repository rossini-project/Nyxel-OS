---
name: email-profissional
description: >
  Rascunha um email profissional a partir de um contexto livre, ou responde
  diretamente a um email/dado recebido de terceiros (inclusive analisando
  arquivos anexados — CSV, Excel, PDF, print, email colado).
  Calibra o tom ao destinatário e ao objetivo do email.
  Use quando o usuário disser "escreve um email pra", "preciso mandar um email sobre",
  "como eu respondo isso", "faz um email pra [cliente/pessoa]", ou anexar um arquivo
  junto com o pedido de email.
---

# /email-profissional — Rascunho de Email

## Dependências

- **Contexto do negócio:** `_memoria/empresa.md`
- **Tom de voz:** `_memoria/preferencias.md`
- **Contexto do cliente (se for pra um cliente específico):** `_memoria/clientes.md` e a pasta do cliente, se existir

---

## Workflow

### Passo 1 — Coletar o contexto

**Se vier arquivo(s) junto com o comando** (CSV, Excel, PDF, print, ou o próprio email do cliente colado/encaminhado):
1. Ler e analisar o(s) arquivo(s) antes de qualquer outra coisa (mesma lógica do `/analisar-dados`: extrair números, pedidos, reclamações, prazos, o que está bom e o que preocupa).
2. Se for um email de terceiro sendo respondido, mapear cada pergunta/pedido — a resposta final precisa cobrir todos, não só o primeiro.
3. Se for dado numérico (planilha, relatório, fatura), extrair os números que vão ser citados no corpo do email — nunca arredondar ou estimar o que já está no arquivo.
4. Cruzar com `_memoria/clientes.md` e `_memoria/financeiro.md` se existirem, pra não citar número desatualizado.
5. Prosseguir direto pro Passo 2 com o que foi extraído. Só perguntar o que realmente não dá pra inferir do arquivo (ex: qual é o objetivo do email, se não estiver óbvio).

**Se não vier arquivo**, e o usuário não forneceu as informações necessárias, perguntar:
1. "Pra quem é o email? (nome, cargo, relação com você)"
2. "Qual é o objetivo? (cobrar, propor, responder, agradecer, seguir up...)"
3. "Tem algo específico que precisa constar ou que precisa evitar dizer?"

Se o usuário deu o contexto de forma livre (mesmo que bagunçado), extrai o que der e prossegue.

### Passo 2 — Escrever o email

**Considerar:**
- Tom proporcional à relação (cliente novo = mais cuidado, parceiro antigo = mais direto)
- Objetivo claro na abertura (não enterrar o pedido no final)
- Uma ação pedida por vez
- Encerramento sem redundância ("Qualquer dúvida, fico à disposição" é padrão — só usar se fizer sentido)
- Se veio de análise de arquivo/email do cliente: tecer os números e respostas direto na prosa do email (ex: "o CTR fechou em 3,2%, acima da média do mês passado" em vez de anexar uma tabela solta) e responder cada ponto que o cliente levantou, na ordem que ele perguntou

**Estrutura:**
```
Assunto: [linha de assunto direta, sem clicbait]

[Nome],

[Parágrafo 1 — contexto ou referência ao último contato]

[Parágrafo 2 — o ponto principal ou o pedido]

[Parágrafo 3 — próximo passo, se houver]

[Assinatura]
[Nome do usuário, de _memoria/empresa.md]
```

### Passo 3 — Apresentar opções de tom (quando fizer sentido)

Se o assunto for delicado (cobrança, feedback negativo, recusa), oferecer 2 versões:
- Versão A: mais direta
- Versão B: mais suave

Deixar o usuário escolher.

---

## Regras

- Tom segue `_memoria/preferencias.md`
- Nunca usar linguagem corporativa genérica sem necessidade
- Assunto do email deve ser específico e descritivo, não vago ("Seguimento", "Proposta")
- Se for um email de cobrança, ser direto mas sem agressividade
- Se for resposta a algo, citar o contexto na primeira linha
- Nunca inventar ou estimar número que devia vir do arquivo — se um dado não estiver claro no arquivo, avisar em vez de supor
- Se o arquivo analisado mostrar algo ruim (queda, atraso, erro), não esconder — endereçar direto no email com o próximo passo pra resolver
- Se o email do cliente tiver mais de um pedido/pergunta, confirmar que todos foram respondidos antes de fechar o rascunho
