# Como usar o Git e Github

## Instalando o GIT

* [Link com os downloads](https://git-scm.com/downloads)

## Criar um projeto novo

* Criar uma nova pasta no PC com o nome do seu projeto

* Abrir o VSCode na pasta criada

* Criar um novo arquivo `README.md`

* Escrever dentro dele `Olá mundo, nesse projeto você aprenderá alguns comandos do Git`

* Salvar o arquivo

Vamos adiante

* Abrir o Git Bash

* Digitar o comando `git init`, para inicializar o repositório

Com o comando acima será criada uma pasta `.git` dentro da pasta do projeto , não apague esta pasta pois nela estão as configuração do git

* Digite o comando `git add README.md` para colocar o arquivo na área de stagging 

<img src="https://i1.wp.com/www.markus-gattol.name/misc/mm/si/content/git_git_add.png">

* `git commit -m "primeiro commit"` para comitar as alterações no repositório

* `git branch -M "main"` para alterar o nome da branch principal de `master` para `main` (isso é uma boa prática atualmente recomendada)

## Repositório no Github

* Depois de você ter criado a sua conta na plataforma, você irá em `Criar novo repositório`

Você vai preencher com as informações do projeto, então dar o nome do repositório, colocar uma breve descrição e criar

Logo depois vai aparecer essa página um pouco cinza e confusa e com vários comandos (pode até perceber que alguns deles jpa usamos), mas o que você tem que fazer é bem simples, apenas copie o link que aparecer para você

* Para passar o commit do meu repositório local (da minha máquina) para um repositório na plataforma do Github, usamos o `git remote add origin <link do repositório>`

* `origin` é o nome utilizado para referenciar o nosso repositório

Agora já temos o nosso repositório local conectado com o respositório do Github, porém o `commit` que damos na máquina não sobe automaticamente para a plataforma

* Para isso digite o comando `git push -u origin main`

Agora se recarregarmos a página iremos ver o nosso arquivo aqui na plataforma!

## Alterando e adicionando arquivo

Beleza, agora que temos o nosso repositório no Github configurado direitinho, podemos usar e abusar do que o Git oferece, afinal é pra isso que estamos utilizando ele né?
Primeira coisa que faremos então é alterar esse arquivo que já commitamos

* Adiciona mais uma frase no arquivo `Essa é uma alteração`

* Além disso iremos criar um novo arquivo `Projeto.md`, onde escreveremos `Esse é o arquivo onde desenvolverei o meu projeto`

* Agora então precisamos subir essa alteração, pra isso seguiremos os mesmos passos de `git add .` (agora ponto `.` pois adiciona todos os arquivos) e `git commit -m "Primeira alteração"`

* Lembrando que para alterar algo no nosso respositório do Github precisamos dar o push, então `git push origin main` (sem o -u)

## Branch

* Para criarmos uma nova branch, digite o comando `git checkout -b "nome-da-brach"`
Esse comando além de criar a branch já entra nela com o checkout

* Crie um novo arquivo, salve e comite as alterações
* 
* Para enviarmos as alterações para a branch certifique-se que está na branch correta e digite o comando `git push origin nome-da-branch`

Agora se olharmos o nosso Github, existe 2 branches, a `main` e a `nome-da-nova-branch`


Vamos supor que eu ainda não tivesse terminado de desenvolver a feature da nova branch, eu poderia continuar tranquilamente na `nova branch` até terminar!

Mas, e se eu precisasse por algum motivo voltar em outra branch e desenvolver a partir do que deixei lá? Sem problemas, a única coisa que você precisa fazer nesse caso é `git checkout nome-da-branch`, e pra voltar depois é só `git checkout nome-da-nova-branch` novamente

Beleza! Agora desenvolvi tudo o que queria aqui na `nova-branch`, como que junto ela com a branch main sem problemas?

## Merge

* Agora o que precisamos fazer é ir para a nossa branch principal `git checkout main` e lá faremos o merge com a `nova-branch` que criamos, com `git merge nome-nova-branch`

Pronto, agora tudo o que tinha de alteração na `nova-branch` juntou com a branch `main`

* Para finalizarmos, digitamos o comando `git push origin main`

## Clone

Como vocês poderiam baixar um código de um repositório?

Sempre que você entrar em um repositório, seja o seu ou o de qualquer outra pessoa, terá um botão `Code`, que quando você clica e aparece um link:

* Basta copiar e colar ele no terminal git bash

* O comando baixar o projeto para a sua máquina é o `git clone url-do-repositório`

Não é necessário criar um repositório antes disso, como fizemos anteriormente com o `git init`. Dessa vez, basta abrir o terminal e clonar o projeto e tudo aparecerá!

## Pull

Se existir mais de uma pessoa trabalhando no mesmo porjeto pode haver constantes alterações no repositório, como vocês podem atualizar na máquina de vocês?

* Basta vocês executarem o comando `git pull`, ele irá trazer todas as alterações feitas no repositório do Github para o seu repositório local


## Pull request

O último conceito que quero ensinar para vocês é o de Pull Request, vamos entender como ele funciona:

* Após você ter dado um fork no projeto e ele ter ido pra sua conta, você poderá alterar o projeto e adicionar as funcionalidades que deseja

* Você pode por exemplo dar um fork no meu repositório de `Formulário` para adicionar uma validação de campos ou qualquer outra coisa que acha válido

* Depois disso, você poderá salvar o projeto, dar o `git add .`, `git commit -m "validação de botões"` e `git push origin main`

Isso significa que a branch do seu repositório está 1 commit "na frente" da branch original

Você irá colocar um nome intuitivo, que demonstre a funcionalidade adicionada e o ideal é que você também crie uma boa descrição do que desenvolveu, não somente explicando o que é, mas ensinando ao dono do repositório original a forma como ele poderá testar também

Depois disso, basta esperar para que o dono da branch original aceite o seu pull request

## Finalização

Existem diversas outras funcionalidades do Git e do Github, porém tenho certeza que com tudo isso que vocês viram hoje vocês já conseguem desenvolver um projeto de uma forma bem legal

Recomendo sempre vocês darem uma olhada na [documentação do Git](https://git-scm.com/doc), pois qualquer dúvida que apareça pode ser respondida por lá na explicação
