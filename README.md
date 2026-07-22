# Nyxel OS

> O sistema operacional do seu negócio dentro do Claude Code.

Você está prestes a instalar o **Nyxel OS** — a versão completa de um sistema que
transforma o Claude Code no centro de operação da sua empresa. Em alguns minutos,
seu negócio vai ter memória própria, identidade visual aplicada em tudo, automações
que rodam sozinhas e **27 skills** cobrindo operação, comercial, financeiro,
clientes, conteúdo e métricas.

Bora voar.

---

## Ligando o sistema

Dois caminhos. Escolhe o que combina contigo.

### Pelo Claude (mais rápido)

Abre o Claude Code em qualquer pasta e cola:

```
Clona o https://github.com/rossini-project/Nyxel-OS.git na pasta atual,
entra nela e roda o /instalar.
```

Ele clona, entra na pasta nova e dispara a entrevista de setup. Você só responde.

### Pelo terminal (mais previsível)

```
git clone https://github.com/rossini-project/Nyxel-OS.git
cd Nyxel-OS
code .
```

Na janela do VS Code que abrir: terminal integrado → `claude` → `/instalar`.

---

Quando o `/instalar` terminar, renomeia a pasta `Nyxel-OS/` pro nome do teu
negócio (fecha o VS Code, renomeia no Explorer/Finder, abre de novo). A pasta
não fica como "Nyxel-OS" — ela é o teu negócio agora.

O `/instalar` roda uma vez só. Entrevista sobre empresa, tom de voz, foco atual,
metas, finanças e identidade visual, e monta toda a memória do sistema. Depois
disso, é só usar.

---

## O sistema (27 skills)

**Operação e decisão** — o jeito de rodar o dia a dia
`/abrir` carrega o contexto e resume a sessão · `/painel` mostra o dia inteiro
(foco, clientes, dinheiro, metas, alertas) · `/foco` aponta a próxima ação de
maior impacto · `/decidir` decide com base no negócio real (estratégia, caixa,
metas) · `/salvar` faz commit + push no GitHub · `/atualizar` varre o projeto e
reconcilia a memória · `/novo-projeto` cria pasta isolada por cliente/iniciativa
· `/mapear-rotinas` transforma o que você repete em skill sua.

**Comercial e dinheiro** — onde o negócio fecha e cobra
`/proposta` gera proposta comercial na sua identidade · `/funil` mostra o
pipeline de vendas e o que travou · `/cobranca` escreve cobranças e follow-ups
no tom certo · `/contrato` rascunha contrato de prestação de serviço ·
`/metricas` fecha o loop entre o que foi feito e o resultado · `/oportunidades`
acha os movimentos de maior retorno agora.

**Clientes** — relação e contexto
`/cliente` abre o dossiê 360º de um cliente · `/reuniao` prepara e registra
reuniões + follow-ups · `/concorrente` analisa a concorrência e sua
diferenciação.

**Conteúdo, SEO e ads** — vitrine e aquisição
`/carrossel` cria carrosséis com a identidade da marca · `/publicar-tema` pega
um tema e entrega artigo + carrossel + legendas · `/seo` roda o fluxo completo
de SEO em etapas · `/responder-avaliacoes` escreve respostas humanas pras
reviews do Google · `/aprovar-post` publica blog + Instagram + Facebook num
comando · `/anuncio-google` monta a campanha em CSV pro Google Ads Editor ·
`/relatorio-ads` lê exports de Google + Meta e gera relatório semanal.

**Produção** — ferramentas do dia a dia
`/analisar-dados` lê CSV/XLSX/PDF e gera resumo executivo · `/email-profissional`
rascunha email a partir de contexto livre.

---

## A tese

IA não é uma ferramenta que sua empresa usa. É o sistema operacional em que ela
roda. Cada processo crítico que hoje roda em open loop (decide → executa → não
mede → repete cego) vira closed loop dentro do Nyxel OS (decide → executa →
captura → realimenta → ajusta sozinho).

O sistema não substitui você. Vira parte da sua empresa.

---

## Como o Nyxel OS pensa

`_memoria/` é o cérebro. Quem é a empresa, como ela fala, foco atual, clientes,
finanças e metas. O Claude lê isso antes de cada resposta. Quanto melhor a
memória, melhor o sistema.

`identidade/` é o rosto. Cores, fontes, logo, padrão visual. Todo material que o
sistema gera (carrossel, proposta, slide, peça) respeita isso.

`.claude/skills/` são os comandos. `.claude/agents/` são os sub-agentes
especializados (estrategista, copywriter, analista) pra tarefas mais profundas.

---

## Suporte

Dúvidas: nyxel.com.br. Comece sempre por `/instalar` e depois `/painel`.

Nyxel — sistemas e sites que inovam o mercado.
