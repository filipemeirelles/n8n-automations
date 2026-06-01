# 📖 Setup Guide

Guia completo para configurar o ambiente n8n + OpenRouter.

## 1. n8n Self-Hosted

### Docker (recomendado)
```bash
docker run -d \
  --name n8n \
  -p 5678:5678 \
  -v n8n_data:/home/node/.n8n \
  n8nio/n8n
```

### npm
```bash
npm install -g n8n
n8n start
```

Acesse: http://localhost:5678

## 2. OpenRouter API

1. Crie conta em https://openrouter.ai
2. Gere uma API key em https://openrouter.ai/keys
3. Modelos gratuitos disponíveis:
   - `google/gemini-2.0-flash-exp:free` — rápido, bom para maioria dos casos
   - `meta-llama/llama-3-8b-instruct:free` — bom para chat
   - `mistralai/mistral-7b-instruct:free` — alternativa leve

## 3. Configurar OpenRouter no n8n

1. **Settings** → **Credentials** → **Add Credential**
2. Tipo: **OpenAI API**
3. Configuração:
   - **API Key**: sua chave OpenRouter
   - **Base URL**: `https://openrouter.ai/api/v1`
4. Salve e teste a conexão

> ⚠️ O n8n usa o formato OpenAI para LLM credentials. OpenRouter é compatível — só muda a base URL.

## 4. Telegram Bot (para workflows Telegram)

1. Fale com [@BotFather](https://t.me/BotFather) no Telegram
2. Envie `/newbot` e siga as instruções
3. Copie o token do bot
4. No n8n: **Credentials** → **Telegram API** → cole o token

## 5. Exportar/Importar Workflows

### Exportar
- Abra o workflow no n8n
- Menu (⋮) → **Download** → salva como JSON

### Importar
- **Workflows** → **Import from File** → selecione o JSON
- Configure as credenciais
- Ative o workflow

---

*Guia atualizado conforme aprendo e configuro novas integrações.*
