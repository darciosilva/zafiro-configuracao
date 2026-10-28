# 1. Configuração do Modelo LLM

## 🎯 Objetivo

Configurar o modelo de linguagem (LLM) que o Zafiro usa para processar e gerar respostas.

---

## 📋 Pré-requisitos

- Uma conta em um provedor de LLM
- Uma API key válida
- Créditos/saldo suficiente na conta

---

## 🔧 Passo a passo

### Passo 1: Escolha o provedor

| Provedor | Modelos populares | Link |
|----------|-------------------|------|
| OpenAI | gpt-4o, gpt-4o-mini | platform.openai.com |
| Anthropic | claude-sonnet-4, claude-haiku | console.anthropic.com |
| Google | gemini-2.0-flash | aistudio.google.com |
| OpenRouter | Centenas de modelos | openrouter.ai |
| Local | llama.cpp, Ollama | github.com/ggerganov/llama.cpp |

### Passo 2: Obtenha a API key

1. Acesse o console do provedor escolhido.
2. Vá em "API Keys" ou "Chaves de API".
3. Clique em "Criar nova chave".
4. **Copie e guarde em local seguro.**

> ⚠️ **Nunca compartilhe sua API key publicamente.**

### Passo 3: Configure no Zafiro

1. Abra o Zafiro.
2. Toque no ícone de **Configurações** (⚙️).
3. Vá em **Configurações de LLM**.
4. Toque em **Adicionar configuração**.
5. Preencha:
   - **Provedor:** selecione da lista
   - **API Key:** cole sua chave
   - **Modelo:** escolha o modelo desejado
   - **Base URL:** (opcional, para provedores compatíveis com OpenAI)

### Passo 4: Ajuste parâmetros

| Parâmetro | O que faz | Recomendação inicial |
|-----------|-----------|---------------------|
| Temperature | Criatividade (0 = preciso, 1 = criativo) | 0.7 |
| Max tokens | Tamanho máximo da resposta | 4096 |
| Top-p | Filtragem por probabilidade | 0.9 |

### Passo 5: Teste

Envie uma mensagem simples:
```
Olá, você está funcionando?
```

Se receber resposta → ✅ Configuração OK!

---

## ⚠️ Solução de problemas

| Erro | Causa provável | Solução |
|------|---------------|---------|
| 401 Unauthorized | API key inválida | Verifique se copiou a key completa |
| 403 Forbidden | Sem permissão | Verifique o plano da conta |
| 429 Rate limit | Excedeu limite | Aguarde ou aumente o plano |
| Timeout | Rede instável | Verifique conexão |
| Model not found | Nome errado | Confirme o nome exato do modelo |

---

## 💡 Dica: OpenRouter (vários modelos em uma key)

O OpenRouter permite usar centenas de modelos com uma única API key:
- Base URL: `https://openrouter.ai/api/v1`
- Modelo: `anthropic/claude-sonnet-4` ou `openai/gpt-4o-mini`
- Mais info: openrouter.ai

---

## 🔗 Próximo módulo

→ [2. Otimização de Tokens](../02-otimizacao-tokens/README.md)
