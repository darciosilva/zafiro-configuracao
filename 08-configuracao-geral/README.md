# 8. Configuração Geral

## 🎯 Objetivo

Ajustar configurações gerais do Zafiro para melhorar a experiência de uso.

---

## ⚙️ Interface

| Configuração | Opções | Onde encontrar |
|-------------|--------|----------------|
| Tema | Claro / Escuro / Sistema | Configurações → Aparência |
| Bola flutuante | Ativar / Desativar | Configurações → Interface |
| Notificações | Ativar / Silenciar | Configurações → Notificações |
| Idioma | Português / English | Configurações → Idioma |

---

## 🔐 Permissões de Execução

O Zafiro tem níveis de permissão para cada tipo de ação:

| Nível | Exemplo | Comportamento |
|-------|---------|---------------|
| Livre | Ler tela, abrir app, consultar | Executa sem pedir |
| Com cuidado | Alterar config, instalar app | Executa e notifica |
| Confirmação | Excluir dados, enviar msg, root | Pede confirmação antes |

**Como ajustar:** Configurações → Regras de Execução → selecione o nível por categoria.

---

## 🕐 Timeout e Logs

- **Timeout de execução:** tempo máximo para uma ferramenta rodar (padrão: 30s).
- **Logs de debug:** ative para diagnosticar problemas; desative em uso normal para economizar recursos.

---

## 📂 Armazenamento

| Diretório | Uso |
|-----------|-----|
| `/data/user/0/com.niki914.zafiro/files/downloads` | Downloads do agente |
| `/data/user/0/com.niki914.zafiro/files/settings` | Configurações JSON |
| `/data/data/com.niki914.zafiro/files/skills` | Skills instaladas |
| `/data/user/0/com.niki914.zafiro/files/tool_output` | Saída de ferramentas |

> ⚠️ Arquivos fora desses diretórios podem precisar de permissão de armazenamento.

---

## 🔧 Editando configurações via arquivo

Para edições avançadas, os arquivos JSON ficam em:
```
/data/user/0/com.niki914.zafiro/files/settings/
```

Use a skill `zafiro-config` ou peça ao agente:
```
Mostre as configurações atuais do Zafiro.
```

---

## ⚠️ Dicas

- Faça backup antes de editar JSONs manualmente.
- Se algo quebrar, delete o arquivo de config e reinicie o app para recriar padrões.
- Não exponha tokens ou chaves em arquivos de configuração compartilhados.

---

## 🔗 Próximo módulo

→ [9. Contribuição](../09-contribuicao/README.md)
