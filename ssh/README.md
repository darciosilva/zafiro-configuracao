# Integração SSH

Como conectar o Zafiro a servidores remotos e ao próprio Termux.

---

## Configuração de conexão

1. No Zafiro, acesse **Configurações → SSH**.
2. Toque em **Adicionar host**.
3. Preencha o endereço (IP ou hostname), porta (padrão 22 ou a porta do Termux, ex: 8022) e usuário.
4. Escolha o método de autenticação:
   - **Chave privada (recomendado):** Cole o conteúdo da chave PEM/OpenSSH.
   - **Senha:** Digite a senha cadastrada.

---

## Uso

Para executar um comando remoto:
```
ssh@meu-servidor ls -la
```

---

## Próximo passo

→ [Integração de APIs](../apis/README.md)
