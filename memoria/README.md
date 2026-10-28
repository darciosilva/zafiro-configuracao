# Configuração de Memória

Como funciona a memória persistente do Zafiro e como gerenciá-la.

---

## Funcionamento

O Zafiro armazena fatos em um arquivo JSON local em `/data/user/0/com.niki914.zafiro/files/settings/`. Esses fatos são injetados nas conversas futuras.

---

## Operações

- **Adicionar:** Peça para o agente salvar um fato (ex: "Lembre-se que uso o diretório /sdcard/projetos").
- **Atualizar:** Solicite a alteração de um registro antigo.
- **Remover:** Peça para apagar dados obsoletos.

---

## Recomendações

- Salve apenas preferências duráveis, convenções de código e caminhos de sistema.
- Não guarde dados temporários, logs longos ou senhas na memória.

---

## Próximo passo

→ [Integração SSH](../ssh/README.md)
