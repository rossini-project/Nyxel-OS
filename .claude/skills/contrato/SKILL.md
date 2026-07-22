---
name: contrato
description: >
  Gera um rascunho de contrato de prestação de serviço simples e claro a partir do escopo e
  valores acordados, na identidade da marca. Use quando o usuário disser "/contrato", "fazer
  contrato", "contrato pro cliente X", "formalizar o serviço".
---

# /contrato — Rascunho de contrato de prestação de serviço

Transforma o que foi combinado num contrato simples, em português claro, pronto pra
revisar e assinar. Puxa o que já se sabe do cliente em `_memoria/clientes.md`.

## Workflow

### Passo 1 — Coletar (só o que faltar)
1. "Quem contrata (cliente) e quem presta (você/empresa)? Dados básicos."
2. "Qual o escopo do serviço? (o que entra e o que NÃO entra)"
3. "Valor, forma e datas de pagamento?"
4. "Prazo de entrega e o que acontece em caso de atraso/cancelamento?"

### Passo 2 — Gerar
Montar o contrato com as cláusulas essenciais: partes, objeto, escopo (incl.
exclusões), valor e pagamento, prazo, propriedade/entrega do material,
confidencialidade, rescisão, foro. Linguagem clara, sem juridiquês desnecessário.
Aplicar a identidade no cabeçalho. Salvar em
`clientes/<Cliente>/contrato/Contrato - <Cliente> - <data>.html`.

### Passo 3 — Aviso e registro
Avisar que é um rascunho-base e, pra valores altos ou casos sensíveis, vale revisão
de um advogado. Registrar em `clientes.md`/`historico.md` que o contrato foi gerado.

## Regras
- **Sempre** incluir o aviso de que é modelo-base, não substitui consultoria
  jurídica. Nunca afirmar validade jurídica garantida.
- Refletir exatamente o escopo e valores acordados — não adicionar cláusulas que
  mudem o combinado sem avisar.
- Deixar marcados em [colchetes] os campos que o usuário precisa conferir/preencher.
