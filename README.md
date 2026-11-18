<p align="center">
  <img src="assets/logo.svg" width="112" height="112" alt="Agente 01">
</p>

<h1 align="center">Agente 01</h1>

<p align="center">
  Contrate o seu primeiro funcionário de IA no Claude, sem programar.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-plugin-12ad8e?style=flat-square" alt="Plugin do Claude Code">
  <img src="https://img.shields.io/badge/atualiza%C3%A7%C3%A3o-autom%C3%A1tica-12ad8e?style=flat-square" alt="Atualização automática">
  <img src="https://img.shields.io/badge/licen%C3%A7a-propriet%C3%A1ria-2d2a20?style=flat-square" alt="Licença proprietária">
</p>

> **Material proprietário, uso exclusivo dos alunos do curso.** Proibido uso
> comercial, cópia, fork público e redistribuição. Veja [LICENSE](LICENSE).
> © 2026 Rios Soluções em Tecnologia.

Skills do curso **Agente 01**.

| | Skill | O que faz |
|---|---|---|
| <img src="assets/logo.svg" width="32" alt=""> | [`entrevista`](skills/entrevista/) | Contrata um funcionário: entrevista você sobre o trabalho, prepara tudo sozinha e cria o funcionário como um projeto próprio, na sua pasta Funcionários. Na primeira vez, prepara o computador e cria o Agente 00. |
| <img src="assets/agente-00.svg" width="32" alt=""> | [`agente-00`](skills/agente-00/) | O check-up do Agente 00, o gerente que acompanha os seus funcionários e sugere melhorias. Nada muda sem você aprovar. |

## Como instalar

Abra o app do Claude no computador, vá na aba **Code**, abra a sua pasta
**Funcionários** e cole a mensagem que está na descrição da aula 03.

As skills chegam como um **plugin** do Claude Code, com atualização
automática: quando o curso atualiza este repositório, o Claude do aluno baixa
a versão nova sozinho (alguns minutos depois de abrir uma conversa) e ela vale
a partir da conversa seguinte. Ninguém precisa reinstalar.

O que a mensagem da aula 03 faz, por trás:

1. Acrescenta em `~/.claude/settings.json` (sem apagar o que já existe):

   ```json
   {
     "extraKnownMarketplaces": {
       "agente01": {
         "source": { "source": "github", "repo": "oldaque/agente01" },
         "autoUpdate": true
       }
     },
     "enabledPlugins": { "agente01@agente01": true }
   }
   ```

2. Se existirem cópias antigas em `~/.claude/skills/entrevista` ou
   `~/.claude/skills/agente-00` (instalação de antes do plugin), apaga essas
   duas pastas, para não ficar skill duplicada.
3. Pede para começar uma conversa nova, onde o plugin já aparece.

Quem tem o terminal pode fazer o mesmo com:

```bash
claude plugin marketplace add oldaque/agente01
claude plugin install agente01@agente01
```

e ligar a atualização automática em `/plugin` → **Marketplaces** →
`agente01` → **Enable auto-update**.

### Publicar uma versão nova

O plugin não tem número de versão de propósito: a versão é o commit. Todo
merge na `main` vira atualização para todos os alunos. Por isso, nada entra
na `main` sem revisão.

## Como fica a sua pasta Funcionários

```text
Funcionários/
├── indice.md      # a lista dos seus funcionários
├── Agente 00/     # o gerente, um projeto próprio
└── Ana/           # um funcionário, um projeto próprio
```

Cada funcionário tem a ficha, o registro do trabalho e as versões dele. Você
abre a pasta de cada um como um projeto no Claude, e eles não se misturam.

## Licença

Uso pessoal e exclusivo de quem comprou o curso. Não é código aberto. Não é
permitido vender, compartilhar, copiar para outro repositório, ensinar ou
incluir em outro produto. Detalhes em [LICENSE](LICENSE). Dúvidas ou pedido de
autorização: contato@oldaque.com
