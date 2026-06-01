# 🤖 n8n Automations

> Automações inteligentes construídas com **n8n** (self-hosted) e **LLMs** via OpenRouter.

[![n8n](https://img.shields.io/badge/n8n-self--hosted-FF6D5A?logo=n8n&logoColor=white)](https://n8n.io)
[![OpenRouter](https://img.shields.io/badge/OpenRouter-models_gratuitos-7C3AED?logo=openai&logoColor=white)](https://openrouter.ai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📋 Sobre

Repositório central das minhas automações n8n — workflows que resolvem problemas reais usando IA, APIs e integrações.

**Stack:** n8n self-hosted · OpenRouter (modelos gratuitos: Gemini Flash, Llama, etc.) · Telegram · Google Sheets · Webhooks

**Objetivo:** Construir um portfólio de automações práticas enquanto transiciono para AI Automation Specialist.

---

## 🗂️ Estrutura

```
n8n-automations/
├── README.md
├── workflows/           # Exportes JSON dos workflows n8n
│   ├── 01-telegram-ai-responder/
│   ├── 02-message-classifier/
│   └── ...
├── docs/                # Documentação detalhada por workflow
│   └── setup-guide.md
└── assets/              # Screenshots, diagrams
```

---

## 🚀 Workflows

| # | Workflow | Status | Descrição |
|---|----------|--------|-----------|
| 01 | Telegram AI Responder | 🔨 Em construção | Bot Telegram que responde usando LLM via OpenRouter |
| 02 | Message Classifier | ⏳ Planejado | Classifica mensagens por intenção (suporte, venda, info) |
| 03 | Lead Qualifier | ⏳ Planejado | Qualifica leads automaticamente via Telegram/WhatsApp |
| 04 | Finance Tracker | ⏳ Planejado | Extrai e categoriza gastos de mensagens/notificações |

---

## ⚙️ Setup

### Pré-requisitos

- [n8n](https://n8n.io/) (self-hosted ou cloud)
- [OpenRouter](https://openrouter.ai/) API key (modelos gratuitos disponíveis)
- (Opcional) Telegram Bot Token — via [@BotFather](https://t.me/BotFather)

### Como importar um workflow

1. Abra seu n8n
2. Vá em **Workflows** → **Import from File**
3. Selecione o JSON em `workflows/<nome-do-workflow>/workflow.json`
4. Configure as credenciais (OpenRouter API key, Telegram token, etc.)
5. Ative o workflow

### Configurando OpenRouter no n8n

1. No n8n, vá em **Settings** → **Credentials**
2. Adicione credencial do tipo **OpenAI API** (compatível com OpenRouter)
3. Base URL: `https://openrouter.ai/api/v1`
4. API Key: sua chave do OpenRouter
5. Use modelos gratuitos como `google/gemini-2.0-flash-exp:free` ou `meta-llama/llama-3-8b-instruct:free`

> 💡 **Dica:** OpenRouter funciona como drop-in replacement da API OpenAI. Mesmo formato, mesma configuração no n8n — só muda a base URL e a key.

---

## 📚 O que estou aprendendo

- **n8n**: workflows, nodes, expressions, credenciais, webhooks
- **APIs REST**: consumo, autenticação, tratamento de erros
- **LLM APIs**: OpenRouter, modelos gratuitos vs pagos, prompt engineering
- **Automação**: triggers, conditional logic, error handling, logging

---

## 🎯 Roadmap

- [x] Setup n8n self-hosted
- [x] Integração OpenRouter com modelos gratuitos
- [ ] Workflow 01: Telegram AI Responder (portfólio #1)
- [ ] Workflow 02: Message Classifier
- [ ] Repo com estrutura documentada + screenshots
- [ ] Workflows 03-04: projetos mais complexos

---

## 📬 Contato

**Filipe Meirelles** — AI Automation Specialist em formação

[![GitHub](https://img.shields.io/badge/GitHub-filipemeirelles-181717?logo=github)](https://github.com/filipemeirelles)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Filipe_Meirelles-0A66C2?logo=linkedin)](https://linkedin.com/in/filipemeirelles)

---

*Este repositório faz parte do meu plano de transição de carreira para AI Automation. Cada workflow é um problema real resolvido.*
