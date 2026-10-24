# Agente 01

Skills do curso **Agente 01**: contrate o seu primeiro funcionário de IA no
Claude, sem programar.

| Skill | O que faz |
|---|---|
| [`entrevista`](skills/entrevista/) | Contrata um funcionário: entrevista você sobre o trabalho, prepara tudo sozinha e cria o funcionário como um projeto próprio, na sua pasta Funcionários. Na primeira vez, prepara o computador e cria o Agente 00. |
| [`agente-00`](skills/agente-00/) | O check-up do Agente 00, o gerente que acompanha os seus funcionários e sugere melhorias. Nada muda sem você aprovar. |

## Como instalar

Abra o app do Claude no computador, vá na aba **Code**, abra a sua pasta
**Funcionários** e cole a mensagem que está na descrição da aula 03.

O Claude baixa este repositório e copia as duas skills para a sua pasta de
skills (`~/.claude/skills/`), para valerem em qualquer projeto.

## Como fica a sua pasta Funcionários

```text
Funcionários/
├── indice.md      # a lista dos seus funcionários
├── Agente 00/     # o gerente, um projeto próprio
└── Ana/           # um funcionário, um projeto próprio
```

Cada funcionário tem a ficha, o registro do trabalho e as versões dele. Você
abre a pasta de cada um como um projeto no Claude, e eles não se misturam.
