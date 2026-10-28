# 2. Otimização de Tokens

## 🎯 Objetivo

Reduzir o consumo de tokens (e custos) sem perder qualidade nas respostas do Zafiro.

---

## 💡 Por que isso importa?

- Cada token consumido = dinheiro gasto (em provedores pagos)
- Contexto acumulado pode estourar o limite do modelo
- Respostas mais longas = mais tempo de espera

---

## 🛠️ Técnicas de otimização

### Técnica 1: Escolha o modelo certo para a tarefa

| Tarefa | Modelo recomendado | Custo |
|--------|-------------------|-------|
| Tarefas simples (perguntas rápidas) | gpt-4o-mini / haiku | 💰 |
| Tarefas complexas (código, análise) | gpt-4o / sonnet | 💰💰💰 |
| Uso local/offline | llama.cpp (7B) | Grátis |

### Técnica 2: System prompt enxuto

**Evite:**
```
Você é um assistente muito útil e inteligente que ajuda o usuário
em todas as suas tarefas de forma amigável, sempre respondendo
em português brasileiro de forma clara e detalhada...
```

**Prefira:**
```
Assistente Android. Responda em PT-BR. Seja direto.
```

> Cada palavra no system prompt é consumida em **toda** mensagem.

### Técnica 3: Gerencie o contexto

- **Memória:** salve apenas fatos duráveis (preferências, configs)
- **Histórico:** inicie nova conversa para tarefas independentes
- **Ferramentas:** configure `max_results` baixo em buscas

### Técnica 4: Ferramentas eficientes

- Prefira ferramentas que retornam JSON compacto
- Evite ferramentas que devolvem logs inteiros
- Use `keyword` em `py_web_read` para extrair apenas o trecho relevante

---

## 📊 Estimativa de economia

| Cenário | Tokens/sessão | Custo mensal (aprox) |
|---------|--------------|---------------------|
| Sem otimização | ~8000 | Alto |
| Com otimização | ~2000 | 75% menor |

---

## 🔍 Como monitorar

- Verifique o painel de uso do seu provedor (OpenAI Dashboard, Anthropic Console, etc.)
- No Zafiro, observe o tamanho das respostas — respostas muito longas indicam desperdício

---

## ✅ Checklist de otimização

- [ ] Modelo adequado ao uso diário
- [ ] System prompt curto e objetivo
- [ ] Memória com poucos itens relevantes
- [ ] Ferramentas com limites configurados
- [ ] Histórico limpo periodicamente

---

## 🔗 Próximo módulo

→ [3. Configuração de Memória](../03-configuracao-memoria/README.md)
