# 6. Configuração do System Prompt

## 🎯 Objetivo

Personalizar o comportamento, personalidade e regras do agente Zafiro através do system prompt.

---

## 📝 O que é o System Prompt?

É o texto que define **quem** o agente é e **como** deve se comportar. Ele é injetado no início de toda conversa.

---

## 📁 Onde fica

```
/data/user/0/com.niki914.zafiro/files/settings/agent_profiles.json
```

---

## ✏️ Estrutura recomendada

```markdown
# PAPEL
Você é [descrição do papel].

# REGRAS
- Regra 1
- Regra 2

# FORMATO DE RESPOSTA
- Formato desejado

# RESTRIÇÕES
- O que não fazer
```

---

## ✏️ Exemplos

### Básico
```
Assistente pessoal Android. Responda em português. Seja direto e conciso.
```

### Desenvolvedor
```
Você é um engenheiro de software sênior.
- Linguagens: Python, Kotlin, TypeScript
- Sempre mostre código funcional
- Explique brevemente antes do código
- Use boas práticas e tratamento de erros
```

### Automação
```
Agente de automação Android.
- Execute ações reais, não descreva
- Valide resultados antes de prosseguir
- Peça confirmação para ações destrutivas
- Responda em PT-BR
```

---

## 🔧 Como editar

### Via Zafiro (interface)
1. Configurações → Perfis de Agente
2. Selecione ou crie um perfil
3. Edite o texto
4. Salve

### Via arquivo
Edite `agent_profiles.json` na pasta de settings do Zafiro.

---

## 💡 Dicas

| Dica | Motivo |
|------|--------|
| Seja específico | Evita respostas genéricas |
| Use bullets | Mais claro que parágrafos |
| Defina restrições | Evita comportamentos indesejados |
| Teste com perguntas simples | Valide antes de uso pesado |
| Mantenha curto | Cada palavra consome tokens |

---

## ⚠️ Erros comuns

- **Prompt muito longo:** desperdiça tokens em toda mensagem.
- **Instruções contraditórias:** confundem o modelo.
- **Sem idioma definido:** respostas podem vir em inglês.
- **Sem restrições:** o agente pode fazer ações indesejadas.

---

## 🔗 Próximo módulo

→ [7. Configuração de Skills](../07-configuracao-skills/README.md)
