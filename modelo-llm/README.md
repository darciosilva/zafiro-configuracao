# Configuração do Modelo LLM

Como configurar os modelos de linguagem utilizados pelo Zafiro.

---

## Provedores e API Keys

Você pode utilizar provedores comerciais ou servidores locais/proxies de API.

### Provedores comerciais

| Provedor | Modelos | URL do Console |
|----------|---------|----------------|
| OpenAI | gpt-4o, gpt-4o-mini | platform.openai.com |
| Anthropic | claude-sonnet-4, claude-haiku | console.anthropic.com |
| Google | gemini-2.0-flash | aistudio.google.com |
| OpenRouter | Diversos provedores | openrouter.ai |

---

## Recomendações: Tokens Gratuitos com freellmapi no Termux

Para economizar e utilizar modelos sem custo alto de API, é possível rodar o servidor/proxy do **freellmapi** direto no Termux dentro do próprio dispositivo Android.

### Como configurar:

1. Acesse o repositório do projeto: https://github.com/tashfeenahmed/freellmapi
2. No Termux, instale as dependências e rode o serviço do freellmapi.
3. O serviço disponibiliza um endpoint local (ex: `http://127.0.0.1:8080/v1` ou porta configurada).
4. No Zafiro:
   - Vá em **Configurações → LLM**.
   - Selecione o provedor compatível com OpenAI.
   - Altere a **Base URL** para o endereço local do Termux (`http://127.0.0.1:8080/v1`).
   - Insira a chave fornecida pelo freellmapi.

Isso garante acesso a tokens gratuitos diretamente no dispositivo.

---

## Parâmetros recomendados

- **Temperature:** `0.7` (equilíbrio entre precisão e fluidez)
- **Max Tokens:** `4096`
- **Top-P:** `0.9`

---

## Próximo passo

→ [Otimização de Tokens](../otimizacao-tokens/README.md)
