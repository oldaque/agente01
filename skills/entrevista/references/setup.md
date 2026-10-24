# Setup das ferramentas e acessos

Depois da entrevista, você prepara sozinho tudo de que o funcionário precisa.
A pessoa só entra quando a mão dela é indispensável.

## A regra

**Nunca peça à pessoa o que você consegue fazer.** Procurar o caminho,
instalar, configurar, escrever arquivos de configuração e testar é com você.
A pessoa faz só o que exige ela:

- Entrar na própria conta de um serviço.
- Clicar em "autorizar" ou "permitir" numa tela de acesso.
- Gerar uma chave de acesso no site do serviço e colar num arquivo que você
  já deixou pronto.
- Clicar num botão do app do Claude que você não consegue clicar.

## Para cada ferramenta da entrevista

### 1. Descobrir o melhor caminho

Verifique, nesta ordem, e fique com o primeiro que funcionar para o que o
funcionário precisa fazer (ler, criar, enviar, apagar):

1. **Já está disponível aqui?** Veja que conexões e ferramentas este Claude já
   tem. Se uma delas já alcança o serviço, use.
2. **Existe conexão oficial do serviço para o Claude?** Procure (na web, se
   puder) um conector ou servidor MCP oficial, publicado pelo próprio serviço
   ou pela Anthropic. Prefira o oficial a um de terceiros.
3. **Dá para fazer pelo navegador?** Se a pessoa usa o serviço logada no
   navegador, use o Claude in Chrome ou o OpenCLI para trabalhar na página
   como ela trabalharia.
4. **Dá para fazer com arquivos?** Se nenhum caminho acima servir, combine com
   a pessoa um jeito simples de o material chegar numa pasta (exportar,
   baixar, salvar) e de o resultado sair dela.

Os caminhos mudam com o tempo. Confira o que existe hoje em vez de confiar na
memória.

**Até 2 tentativas por caminho.** Se um caminho falhar duas vezes, não insista:
passe para o próximo da lista. Se o último também falhar, siga "Se não houver
caminho", lá embaixo.

Critérios de desempate: o que pede menos da pessoa, o que pede o menor acesso
possível (só leitura, se só ler basta) e o que funciona sem você estar na
conversa, se o trabalho precisa rodar sozinho.

### 2. Contar para a pessoa, em linguagem simples

Antes de qualquer passo que envolva a pessoa, diga as quatro coisas:

- **O que** você vai usar: "uma conexão do Claude com o seu [serviço]".
- **Por que**: "para a Ana conseguir ler [X] sem você copiar e colar".
- **Que acesso** isso pede: "ela vai poder ler e [criar/enviar/apagar] [X]; não
  vai mexer em [Y]".
- **O que exatamente a pessoa faz agora**: um passo só.

Não explique como a conexão funciona por dentro.

### 3. Fazer sozinho o que der

Git, Python e Node já vêm do setup técnico (`setup-tecnico.md`); use-os quando
um caminho precisar deles, sem pedir de novo.

Instale, configure e prepare tudo antes de chamar a pessoa. Se ela precisar
colar uma chave, crie antes o arquivo, já com o lugar certo marcado, dentro da
pasta do funcionário, e confira que ele está fora das versões (no `.gitignore`
da pasta dele).

### 4. Guiar a pessoa no que só ela pode fazer

- Um passo por mensagem. Diga onde clicar com o nome exato do botão ou do menu
  que ela vai ver.
- Espere ela dizer que fez. Confirme do seu lado que deu certo antes do
  próximo passo.
- Senha nunca vem pela conversa. Ela entra na conta direto na página do
  serviço.
- Chave de acesso também não vem pela conversa: ela cola no arquivo que você
  preparou e salva.
- Se algo der errado, não jogue a culpa nem o erro técnico na pessoa. Diga o
  que aconteceu em uma frase e qual é o próximo passo.
- Nunca peça para a pessoa repetir o mesmo passo mais de duas vezes. Na
  segunda falha, mude de caminho ou siga "Se não houver caminho".

### 5. Testar o acesso

Faça uma ação de teste que não muda nada (por exemplo, só ler ou listar) e
mostre o resultado à pessoa: "Pronto, a Ana já consegue ver [X]". Ações que
não têm volta não entram no teste.

## Se o trabalho precisa rodar sozinho

Não agende o trabalho do funcionário na contratação. Anote na ficha o dia e a
hora que a pessoa contou. Quem agenda é o próprio funcionário, quando a pessoa
pedir no projeto dele ("Todo dia de manhã, faça isso para mim"): a ficha já
diz como. Assim a pessoa vê primeiro o funcionário trabalhando com um pedido
curto e só depois liga a rotina.

Prepare o caminho para isso: o acesso escolhido precisa funcionar sem a pessoa
na conversa (critério de desempate acima).

## Se não houver caminho

Diga com franqueza que essa parte ainda não dá para ele fazer sozinho e
proponha o que ele consegue: preparar o trabalho para a pessoa só conferir e
clicar. Registre isso na ficha.

## O que vai para a ficha

Na seção de ferramentas e acessos, para cada uma:

- O serviço e o caminho de acesso (conexão, navegador ou pasta).
- O que ele pode fazer lá.
- Onde fica a chave, se houver: só o nome do arquivo, nunca o conteúdo.
