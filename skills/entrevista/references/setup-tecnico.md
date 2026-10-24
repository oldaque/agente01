# Setup técnico inicial

Faz parte do onboarding, só no primeiro funcionário. Se o `indice.md` da pasta
Funcionários diz que o preparo já foi feito (ou recusado), pule as partes 1 e
2 e use só a parte 3 em cada pasta nova.

Antes da entrevista, prepare o computador com o básico que os funcionários
vão usar: **Git**, **Python** e **Node**. Com eles, cada funcionário guarda as
versões dos próprios arquivos (e recupera uma versão antiga) e escreve
pequenos programas que deixam rotinas automáticas. Algumas conexões do setup
também dependem deles.

A pessoa não precisa saber nada disso além do essencial.

## 1. A aprovação

A aprovação vem junto com a do onboarding inteiro (ver
`pasta-funcionarios.md`), numa frase só, sem detalhes técnicos. Uma aprovação
vale para os três. Se a pessoa disser não, siga sem eles: o funcionário
trabalha do mesmo jeito, só sem versões e sem rotinas automáticas. Anote isso
no `indice.md`.

## 2. Fazer sozinho

1. Descubra o sistema do computador (Mac, Windows, Linux).
2. Veja o que já está instalado. O que já existe e funciona não se reinstala.
3. Instale o que falta pelo caminho oficial do sistema ou do próprio
   programa. Nada de instalador de site desconhecido.
4. Confira que cada um funciona antes de seguir.

Se o computador pedir a senha da pessoa ou um clique de permissão, diga
exatamente o que vai aparecer e o que ela faz ("Vai abrir uma janela pedindo a
senha do seu computador. Digite e clique em OK."). A senha é digitada na
janela do computador, nunca na conversa.

Não explique o que cada programa é, a menos que ela pergunte. Se perguntar,
uma frase basta.

## 3. Versões em cada projeto

Cada projeto guarda as próprias versões: a pasta do Agente 00 e a pasta de
cada funcionário têm o seu Git. A raiz da pasta Funcionários não tem.

Ao criar cada pasta:

- Ative o Git nela, só no computador. Nunca envie a pasta para nenhum serviço
  online.
- Crie o `.gitignore` antes da primeira versão, com qualquer arquivo de chave
  de acesso ou senha, e confira que ele ficou de fora.
- Guarde a primeira versão quando a ficha for salva.

Depois, cada funcionário guarda uma versão na própria pasta sempre que a
ficha mudar ou um programa for criado ou alterado. O Agente 00 guarda uma
versão na pasta dele no fim de cada check-up, e na pasta do funcionário
quando aplica uma melhoria aprovada.

Para a pessoa, isso aparece só como: "Guardei uma versão, dá para voltar se
precisar."

## 4. Freios

- Até 2 tentativas por instalação. Se falhar, siga sem aquele programa e diga
  em uma frase o que fica de fora.
- O setup técnico não pode travar o resto. Se nada instalar, continue para a
  entrevista.

## Quando o funcionário escreve programas

Isto já vai escrito na ficha, para o funcionário seguir no dia a dia:

- Quando um passo se repete e um pequeno programa resolveria, o funcionário
  propõe em linguagem simples ("Posso deixar essa parte automática. Quer?").
  Com o "sim", ele escreve, testa e guarda o programa em `rotinas/`, na pasta
  dele, e registra na ficha o que a rotina faz e quando roda.
- Programa novo ou alterado é melhoria: só com aprovação, como qualquer
  mudança na ficha.
- O programa só mexe nos lugares e acessos que a ficha já autoriza.
