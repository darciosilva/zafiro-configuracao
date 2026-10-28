# Integração de APIs

Como estender o Zafiro criando ferramentas Python personalizadas.

---

## Estrutura de uma ferramenta Python

Toda ferramenta registrada no Zafiro deve conter a função `main`:

```python
def main(parametro: str) -> str:
    """Descrição simples da função."""
    import requests
    response = requests.get("https://api.exemplo.com/dados", params={"q": parametro}, timeout=15)
    return response.text
```

---

## Como cadastrar

1. Abra **Configurações → Ferramentas Python**.
2. Clique em **Adicionar**.
3. Preencha nome, descrição e cole o código Python.
4. Salve.

---

## Recomendações de segurança

- Defina `timeout` em todas as requisições HTTP.
- Leia chaves de API a partir de arquivos locais em vez de inseri-las direto no código.

---

## Próximo passo

→ [System Prompt](../system-prompt/README.md)
