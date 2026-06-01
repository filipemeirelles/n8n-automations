# 🤖 Telegram AI Responder

Bot Telegram que responde mensagens usando LLM via OpenRouter.

## Status: 🔨 Em construção

## Fluxo

```
Telegram (mensagem recebida)
  → n8n Webhook/Telegram Trigger
  → OpenRouter API (LLM)
  → Resposta via Telegram
```

## Nodes n8n

1. **Telegram Trigger** — recebe mensagens do bot
2. **OpenAI Chat** (configurado com OpenRouter) — gera resposta
3. **Telegram Send** — envia resposta ao usuário

## Configuração

### Credenciais necessárias
- Telegram Bot Token (via @BotFather)
- OpenRouter API Key

### Modelo recomendado
- `google/gemini-2.0-flash-exp:free` — rápido e gratuito
- Alternativa: `meta-llama/llama-3-8b-instruct:free`

## Arquivos

- `workflow.json` — export do workflow n8n (a ser adicionado)
- `README.md` — este arquivo

## Aprendizados

- OpenRouter funciona como drop-in da API OpenAI no n8n
- Modelos gratuitos são suficientes para bots de conversa
- Importante: configurar error handling para quando a API falha

---

*Workflow em desenvolvimento. JSON será adicionado quando estiver funcional.*
