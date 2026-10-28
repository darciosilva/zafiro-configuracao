# 7. Configuração de Skills

## 🎯 Objetivo

Gerenciar skills — pacotes de instruções que ensinam novas capacidades ao agente Zafiro.

---

## 📦 O que são Skills?

Skills são pastas contendo um arquivo `SKILL.md` com instruções estruturadas que o agente carrega quando necessário. Elas permitem:
- Ensinar fluxos de trabalho específicos
- Adicionar conhecimento de domínio
- Criar rotinas reutilizáveis

---

## 📁 Estrutura de uma Skill

```
minha-skill/
├── SKILL.md          (obrigatório — instruções principais)
├── scripts/          (opcional — scripts auxiliares)
├── references/       (opcional — docs de referência)
└── assets/           (opcional — templates, ícones)
```

---

## 🔧 Como instalar Skills

### Opção 1: De um repositório GitHub (recomendado)

Peça ao agente:
```
Instale a skill do repositório: https://github.com/usuario/repo
```

O agente usará a skill `install-skill-from-github` automaticamente.

### Opção 2: Manualmente

1. Baixe a pasta da skill.
2. Cole em: `/data/data/com.niki914.zafiro/files/skills/`
3. A skill estará disponível no **próximo turno** de conversa.

### Opção 3: Criar do zero

Peça ao agente:
```
Crie uma skill que faz X quando o usuário pede Y.
```

O agente usará a skill `skill-creator` para guiá-lo.

---

## 📋 Skills úteis incluídas

| Skill | Finalidade |
|-------|-----------|
| `termux` | Conectar ao Termux via SSH |
| `zafiro-config` | Editar configurações JSON do Zafiro |
| `investigate-first` | Diagnosticar problemas antes de agir |
| `skill-creator` | Criar novas skills |
| `install-skill-from-github` | Instalar skills de repos públicos |

---

## ⚠️ Dicas

- Skills são lidas **uma vez por turno** — uma skill instalada agora só funciona no próximo turno.
- Não sobrescreva skills nativas do app.
- Prefira skills com `description` clara para melhor ativação automática.
- Teste a skill após instalar pedindo algo relacionado.

---

## 🔗 Próximo módulo

→ [8. Configuração Geral](../08-configuracao-geral/README.md)
