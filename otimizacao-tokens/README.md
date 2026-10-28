# Otimização de Tokens

Como reduzir o consumo desnecessário de tokens nas requisições.

---

## Práticas de economia

### 1. Seleção do modelo
Use modelos leves para tarefas corriqueiras (como `gpt-4o-mini` ou modelos menores via `freellmapi`) e reserve modelos avançados para análises complexas.

### 2. System prompt direto
Evite textos longos ou redundantes no prompt do sistema.
- **Evite:** Instruções prolixas repetindo que o agente deve ser educado e amigável.
- **Prefira:** Regras diretas com o papel, restrições e idioma.

### 3. Limpeza de contexto
- Mantenha na memória apenas fatos estáveis.
- Inicie uma nova conversa quando mudar totalmente de assunto.
- Defina limites razoáveis (`max_results`) ao utilizar ferramentas de busca na web.

---

## Próximo passo

→ [Memória](../memoria/README.md)
