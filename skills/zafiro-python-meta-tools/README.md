# Zafiro Python Meta Tools Skill

Esta pasta contém uma skill independente para orientar agentes a criar, revisar, testar e documentar ferramentas Python Meta Tools para o Zafiro.

## Arquivo principal

- `SKILL.md`: instruções que o agente deve ler e seguir.

## Uso

Importe a pasta/arquivo no gerenciador de Skills do seu agente, conforme o formato que ele aceita. Se a plataforma exigir um arquivo `.skill`, veja se ela define um formato de pacote específico. Este ZIP contém a skill como Markdown, um formato comum para skills de agentes.

A skill não instala ferramentas no Zafiro e não testa código automaticamente. Ela orienta o agente a verificar o contrato real do executor, produzir código copiável e distinguir protótipos de ferramentas comprovadamente testadas.
