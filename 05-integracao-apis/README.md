# 5. Integração de APIs

## 🎯 Objetivo

Conectar o Zafiro a APIs externas para estender suas capacidades.

---

## 🌐 APIs já integradas

| Ferramenta | Função |
|-----------|--------|
| `py_web_search` | Pesquisa na web |
| `py_web_read` | Ler conteúdo de páginas |
| `py_github_search` | Buscar repositórios GitHub |
| `py_github_repo_info` | Info de um repositório |
| `py_download_file` | Baixar arquivos |
| `py_local_llm_status` | Verificar LLM local |

---

## 🔧 Criar uma API customizada

### Passo 1: Escreva o código

Toda ferramenta Python no Zafiro segue este padrão:

```python
def main(parametro: str) -> str:
    """Descrição do que a ferramenta faz."""
    import requests
    r = requests.get("https://api.exemplo.com/dados",
                     params={"q": parametro},
                     timeout=15)
    r.raise_for_status()
    return r.text
```

**Regras:**
- A função deve se chamar `main`
- Parâmetros com type hints (str, int, float, bool)
- A docstring vira a descrição da ferramenta
- Retorne str, dict ou list

### Passo 2: Registrar no Zafiro

1. Vá em **Configurações → Ferramentas Python**.
2. Toque em **Adicionar**.
3. Preencha Nome, Descrição e Cole o código.
4. Salve e teste.

### Passo 3: Usar

```
Use minha-ferramenta para buscar dados sobre "clima em São Paulo"
```

---

## 🔐 Boas práticas de segurança

- **Nunca** coloque API keys diretamente no código público.
- Use arquivos de configuração locais:
  ```python
  TOKEN_PATH = "/data/user/0/com.niki914.zafiro/files/settings/minha_api_key.txt"
  with open(TOKEN_PATH) as f:
      api_key = f.read().strip()
  ```
- Defina `timeout` em todas as requisições.
- Trate exceções com try/except.

---

## 📦 Exemplo: ferramenta de clima

```python
def main(cidade: str) -> str:
    """Busca o clima atual de uma cidade via API pública."""
    import requests
    try:
        r = requests.get(
            "https://wttr.in/" + cidade,
            params={"format": "j1"},
            timeout=10
        )
        r.raise_for_status()
        data = r.json()
        atual = data["current_condition"][0]
        return f"Clima em {cidade}: {atual['temp_C']}°C, {atual['weatherDesc'][0]['value']}"
    except Exception as e:
        return f"Erro: {e}"
```

---

## 🔗 Próximo módulo

→ [6. Configuração do System Prompt](../06-configuracao-system-prompt/README.md)
