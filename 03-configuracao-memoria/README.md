# 3. Configuração de Memória

## 🎯 Objetivo

Configurar o sistema de memória persistente do Zafiro para que o agente lembre informações importantes entre sessões.

---

## 🧠 Como funciona

O Zafiro possui uma memória persistente que:
- Salva fatos entre conversas
- É injetada no contexto de cada nova sessão
- Usa a ferramenta `memory` (add, replace, remove)

---

## ⚙️ Configuração

### Onde ficam os dados

```
/data/user/0/com.niki914.zafiro/files/settings/
```

### Como salvar uma memória

Diga ao agente:
```
Lembre-se: meu nome é João e prefiro respostas curtas.
```

O agente usará a ferramenta `memory` com action `add`.

### Como atualizar

```
Atualize minha preferência: agora prefiro respostas detalhadas.
```

### Como remover

```
Esqueça a informação sobre meu nome.
```

---

## ✅ O que salvar na memória

| Tipo | Exemplo |
|------|---------|
| Preferências | "Prefiro respostas em PT-BR" |
| Configurações | "Meu servidor SSH é 192.168.1.50" |
| Convenções | "Projeto usa TypeScript com ESLint" |
| Limitações | "Não tenho root no dispositivo" |

## ❌ O que NÃO salvar

| Tipo | Motivo |
|------|--------|
| Progresso de tarefa | Fica desatualizado rápido |
| Senhas/tokens | Risco de segurança |
| Dados temporários | Ocupa espaço sem valor |
| Logs de execução | Melhor no histórico |

---

## 💡 Boas práticas

1. **Seja específico:** "Usuário prefira respostas concisas" ✓
2. **Formato declarativo:** fatos, não instruções
3. **Máximo ~10 itens:** memória demais polui o contexto
4. **Revise periodicamente:** remova o que não é mais relevante

---

## 🔗 Próximo módulo

→ [4. Integração SSH](../04-integracao-ssh/README.md)
