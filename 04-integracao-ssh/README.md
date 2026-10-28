# 4. Integração SSH

## 🎯 Objetivo

Permitir que o Zafiro execute comandos em servidores remotos via SSH.

---

## 📋 Pré-requisitos

- Um servidor com SSH habilitado (VPS, Raspberry Pi, outro PC)
- Usuário e credenciais de acesso
- Rede acessível (mesma LAN ou IP público)

---

## 🔧 Configuração no Zafiro

### Passo 1: Adicionar conexão

1. Abra o Zafiro.
2. Vá em **Configurações → SSH**.
3. Toque em **Adicionar host**.
4. Preencha:

```
Nome:     meu-servidor
Host:     192.168.1.100
Porta:    22
Usuário:  meu-usuario
```

### Passo 2: Autenticação

**Opção A — Senha:**
- Selecione "Senha" e digite.

**Opção B — Chave privada (recomendado):**
- Selecione "Chave privada".
- Cole o conteúdo da chave (formato PEM/OpenSSH).
- Salve.

> 💡 Para gerar uma chave: `ssh-keygen -t ed25519` no terminal.

### Passo 3: Testar

Peça ao agente:
```
Conecte ao meu-servidor e rode: uname -a
```

---

## 📋 Comandos úteis

| Comando | O que faz |
|---------|-----------|
| `ls -la` | Listar arquivos |
| `df -h` | Espaço em disco |
| `free -m` | Memória RAM |
| `top -bn1` | Processos ativos |
| `systemctl status nginx` | Status de serviço |

---

## ⚠️ Segurança

- **Prefira chave privada** em vez de senha.
- **Nunca** exponha a porta SSH à internet sem firewall.
- Use porta não padrão (ex: 2222) para reduzir scans automáticos.
- Limite hosts confiáveis na configuração do Zafiro.

---

## 🐛 Solução de problemas

| Problema | Solução |
|----------|---------|
| Connection refused | Verifique se o SSH está rodando no servidor |
| Permission denied | Confira usuário/chave/senha |
| Timeout | Verifique IP, porta e firewall |
| Host key verification | Aceite a fingerprint na primeira conexão |

---

## 🔗 Próximo módulo

→ [5. Integração de APIs](../05-integracao-apis/README.md)
