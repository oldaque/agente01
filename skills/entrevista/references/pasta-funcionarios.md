# A pasta Funcionários

A pasta Funcionários é onde moram todos os funcionários da pessoa. Cada
funcionário é uma pasta dentro dela e um **projeto próprio** no Claude: a pasta
dele aberta no app, com as conversas só dele e as versões só dele. Assim cada
um acumula o próprio contexto e os assuntos não se misturam.

O Agente 00, o gerente, também é um projeto dentro dela. Ele não contrata e
não faz o trabalho de ninguém: ele acompanha os funcionários e propõe
melhorias. Quem contrata é esta skill.

```text
Funcionários/                 ← a pasta Funcionários (não é projeto de ninguém)
├── indice.md                 ← lista dos funcionários e combinados gerais
├── Agente 00/                ← projeto do gerente
│   ├── .git                  ← versões só do Agente 00
│   ├── .claude/settings.json ← deixa o Agente 00 alcançar as pastas dos colegas
│   ├── AGENTS.md             ← a ficha do Agente 00
│   ├── CLAUDE.md             ← uma linha: @AGENTS.md
│   └── acompanhamento.md     ← memória dele: check-ups e pendências
└── <Nome>/                   ← um funcionário, projeto próprio
    ├── .git                  ← versões só dele
    ├── .gitignore            ← arquivos de chave fora das versões
    ├── AGENTS.md             ← a ficha
    ├── CLAUDE.md             ← uma linha: @AGENTS.md
    ├── registro.md           ← o que ele fez, correções, problemas
    ├── melhorias.md          ← propostas do Agente 00 (só quando houver)
    └── rotinas/              ← programas automáticos (só quando houver)
```

**Nunca crie `AGENTS.md` nem `CLAUDE.md` na raiz da pasta Funcionários.** O
Claude lê as instruções das pastas acima da que está aberta. Se a raiz tivesse
uma ficha, todo funcionário receberia também essa ficha e poderia se
confundir sobre quem é. A raiz só tem o `indice.md`, que ninguém lê sozinho:
esta skill e o Agente 00 abrem quando precisam.

O `CLAUDE.md` de uma linha em cada projeto garante que o Claude leia a ficha
ao abrir a pasta, mesmo onde ele não procura o `AGENTS.md` sozinho.

## Encontrar a pasta Funcionários

A skill é instalada para valer em qualquer projeto. Por isso, antes de tudo,
descubra onde está a pasta Funcionários, nesta ordem:

1. **A pasta aberta tem o `indice.md`** com o Agente 00: é ela. Mais uma
   contratação.
2. **A pasta aberta é de um funcionário ou do Agente 00** (tem `AGENTS.md`, e a
   pasta acima tem o `indice.md`): a pasta Funcionários é a de cima. Siga
   criando o novo funcionário lá e, no fim, diga em uma frase que da próxima
   vez é melhor contratar com a pasta Funcionários aberta.
3. **A pasta aberta se chama "Funcionários"** (ou foi criada para isso) e não
   tem `indice.md`: é a primeira vez. Use ela.
4. **Nenhum desses casos:** procure uma pasta `Funcionários` com `indice.md`
   só em Documentos e na Área de Trabalho da pessoa. Não procure pelo
   computador inteiro. Achou: confirme com ela ("Achei a sua pasta
   Funcionários em Documentos. É essa?"). Não achou: é a primeira vez.
   Proponha criar `Funcionários` em Documentos e, se este Claude conseguir,
   crie você.

Pasta de passagem (Downloads, Área de Trabalho solta) ou cheia de arquivos que
não têm a ver: não use como pasta Funcionários. Proponha Documentos.

## Primeira vez: o onboarding

Sem `indice.md`, é o primeiro funcionário. Antes da entrevista:

1. **Pedir uma aprovação só para o onboarding inteiro.** Diga algo como:

   > Antes de contratar o seu primeiro funcionário, vou preparar a casa. Vou
   > fazer três coisas: organizar a sua pasta Funcionários; preparar o seu
   > computador, instalando linguagens de programação e um programa que
   > guarda versões dos arquivos (serve para voltar atrás se algo der errado
   > e para deixar rotinas automáticas); e criar o Agente 00, o gerente que
   > acompanha os seus funcionários e sugere melhorias. Eu cuido de tudo. Se
   > o computador pedir a sua senha, eu te aviso antes. Posso seguir?

   Se ela recusar o preparo do computador, faça o resto sem ele. A pasta
   Funcionários e o Agente 00 não são opcionais: sem eles, ninguém acompanha
   os funcionários.
2. **Perguntar como ela quer ser chamada.** O nome vai no índice e nas fichas.
   Nunca use o nome da conta do computador: ela pode ser de outra pessoa.
3. **Setup técnico:** siga [`setup-tecnico.md`](setup-tecnico.md).
4. **Criar o `indice.md`** na raiz, a partir de
   [`../assets/indice.modelo.md`](../assets/indice.modelo.md).
5. **Criar o Agente 00** (ver "O Agente 00", abaixo).
6. **Agendar o check-up do Agente 00** (ver abaixo).
7. **Avisar**, em uma frase: "Pronto, a casa está preparada e o Agente 00 já
   está de olho. Agora vamos contratar o seu primeiro funcionário."

## Mais um funcionário

Com o `indice.md` já existindo:

- Leia o índice e as fichas que já existem. Use a ficha mais parecida como
  modelo de formato e confira que o novo não repete o trabalho de outro.
- Pule o que já foi feito: o onboarding inteiro e os acessos já conectados
  que o novo também vai usar.
- No fim, acrescente o novo funcionário na tabela do índice.

## A pasta do funcionário

Dentro da pasta Funcionários, crie a pasta com o nome do funcionário e:

- o `CLAUDE.md` de uma linha (`@AGENTS.md`);
- o `registro.md`, a partir de
  [`../assets/registro.modelo.md`](../assets/registro.modelo.md);
- o `.gitignore`, já com os arquivos de chave que o setup vai criar;
- se o trabalho acontece em pastas do computador fora da pasta Funcionários
  (por exemplo, a pasta onde a pessoa guarda os arquivos de clientes), o
  `.claude/settings.json` liberando só essas pastas, com o caminho completo,
  no mesmo formato do Agente 00 (abaixo). A ficha diz o que ele pode fazer
  em cada uma;
- a guarda de versões ativada nesta pasta (ver
  [`setup-tecnico.md`](setup-tecnico.md)), se o preparo do computador foi
  feito.

O registro existe porque nem todo Claude consegue reler conversas antigas: é
ele que o Agente 00 lê no check-up.

## O projeto do funcionário

No fim da contratação, a pasta do funcionário vira um projeto próprio no
Claude. Se este Claude consegue abrir uma conversa nova numa pasta, faça você.
Se não, guie a pessoa a abrir a pasta do funcionário como projeto, um passo de
cada vez, com o nome exato dos botões que ela vai ver. É nesse projeto que ele
trabalha daqui em diante.

## O Agente 00

O gerente da pasta Funcionários. Nasce sempre, no onboarding, como um projeto
próprio:

1. Crie a pasta `Agente 00` dentro da pasta Funcionários.
2. Crie a ficha `AGENTS.md` a partir de
   [`../assets/agente-00.modelo.md`](../assets/agente-00.modelo.md), o
   `CLAUDE.md` de uma linha e o `acompanhamento.md` a partir de
   [`../assets/acompanhamento.modelo.md`](../assets/acompanhamento.modelo.md).
3. Crie `Agente 00/.claude/settings.json` liberando a pasta Funcionários
   inteira, com o caminho completo dela:

   ```json
   {
     "permissions": {
       "additionalDirectories": ["<caminho completo da pasta Funcionários>"]
     }
   }
   ```

   É isso que deixa o Agente 00 ler as pastas dos colegas e deixar propostas
   nelas. Um funcionário só recebe esse arquivo para as pastas de fora que o
   trabalho dele usa, nunca para a pasta Funcionários inteira.
4. Ative a guarda de versões na pasta do Agente 00, se o preparo do
   computador foi feito.

O Agente 00 não contrata. Se a pessoa pedir a ele um funcionário novo, ele
explica que quem contrata é a skill do Agente 01, com a pasta Funcionários
aberta, e ajuda a abrir.

**Frequência do check-up.** Pergunte, já com a sua sugestão:

> O Agente 00 vai dar uma olhada nos seus funcionários e te contar o que
> observou. Eu deixaria uma vez por semana, na segunda de manhã, antes de a
> semana começar. Se preferir, pode ser todo dia. Pode ser segunda?

Recomende semanal: cada check-up gasta uso do plano do Claude, e no começo uma
vez por semana basta.

**Automação.**

- **Se este Claude consegue agendar tarefas** (as tarefas agendadas do
  próprio app): agende você uma tarefa recorrente, na frequência combinada,
  que abre uma conversa nova no projeto do Agente 00 e faz o check-up com a
  skill `agente-00`. Prefira sempre o agendador do Claude ao do computador.
- **Se o app não tem agendador, mas o computador tem** e roda o Claude sem
  ninguém na frente: use o do computador, com o Claude só com as permissões
  de que o check-up precisa, e diga à pessoa em uma frase que ficou assim e
  que o computador precisa estar ligado na hora.
- **Se não consegue:** diga isso com clareza e combine a palavra que a pessoa
  manda no projeto do Agente 00: "check-up". A ficha dele também oferece o
  check-up quando ele atrasa.

Até 2 tentativas para agendar. Anote no índice a frequência e o jeito.
