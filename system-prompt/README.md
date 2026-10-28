# Configuração do System Prompt

Como ajustar o comportamento padrão do agente Zafiro.

---

## Estrutura recomendada

Organize o prompt em blocos objetivos:

```markdown
# PAPEL
Você é um assistente de automação no Android.

# REGRAS DE EXECUÇÃO
- Execute ações reais em vez de apenas descrevê-las.
- Valide o resultado dos comandos antes de confirmar a conclusão.
- Responda em Português do Brasil.

# RESTRIÇÕES
- Não exponha credenciais ou tokens em logs.
```

---

## Local dos arquivos

Os perfis ficam armazenados em:
`/data/user/0/com.niki914.zafiro/files/settings/agent_profiles.json`

---

## Próximo passo

→ [Skills](../skills/README.md)
