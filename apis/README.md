# 🔌 Integração de APIs

Como criar ferramentas Python no Zafiro.

---

## 🐍 Estrutura do código

```python
def main(parametro: str) -> str:
    """Descrição da ferramenta."""
    import requests
    r = requests.get("https://api.exemplo.com", params={"q": parametro}, timeout=15)
    return r.text
```

---

## 📝 Cadastro

1. Acesse **Configurações → Ferramentas Python**.
2. Adicione nome, descrição e o código.

---

→ 📝 [System prompt](../system-prompt/README.md)
