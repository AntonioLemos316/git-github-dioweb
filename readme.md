# Git e GitHub na dio

## Sistemas de controle de versão

- Controla as versões de um arquivo ao longo do tempo
- Registra o histórico de atualizações de um arquivo
- Gerencia quais foram as alterações, a data, autor, etc
- Organização, controle e segurança

## Tipos de Sistemas de controle de versão

- VCS Centralizado (CVCS) > ex: CVS, Subversion
- VCS Centralizado as versões ficam em um servidor centralizado, caso aconteça algum problema com o servidor ficamos sem poder contribuir até o servidor voltar.
- VCS Distribuído (DVCS) > ex: Git, Mercurial
- VCS Distribuído surgiu em busca de resolver problemas dos CVCS
- Clona o repositório completo, o que inclui o histórico de versões
- Cada clone é como um backup
- Possibilita um fluxo de trabalho flexível
- Possibilidade de trabalhar sem conexão à rede

## Git

- DVCS > Sistema de controle de versão distribuído
- Gratuito e Open Source
- Ramificações (branching) e fusões (merging) eficientes
- Leve e rápido
- https://git-scm.com/ about e documentation

## Fluxo básico no git

- git clone > clona um repositório git existente para um novo diretório(pasta)local
- git commit > grava alterações no repositório
- git pull > puxa as alterações do repositório remoto para o local(busca e mescla)
- git push > empurra as alterações do repositório local para o remoto

## GitHub

- Plataforma de hospedagem de código para controle de versão com Git, e colaboração
- Comunidade ativa
- Utilizado mundialmente
- Git !== GitHub

## Gitbash

- git config --global user.name "lemos"
- git config --global user.email "lemos@email.com"
- git config user.name
- git config user.email
- git config init.defaultBranch // master
- git config --global init.defaultBranch main
- git config init.defaultBranch // main
- git config --global --list // retorna configurações do global user, email, editor e outras
- git config credential.helper cache // temporario > mais de uma pessoa
- git config credential.helper store // permanente > uso pessoal

## Primeiros passos git e github criando e clonando repositórios

- Existem duas formas de obter um repositório git na máquina local
- Transformar um diretório local que não está sob controle de versão, num repositório Git com git init

<img src="./img/git-github001.PNG">

- Utilizando cd .git para acessar na pasta o caminho .git que é oculto, esse arquivo é responsavel por gerenciar nosso controle de versão

<img src="./img/git-github002.PNG">

- Utilizando o ls para ver os arquivos em .git

<img src="./img/git-github003.PNG">

- Clonando um repositório Git existente com git clone

<img src="./img/git-github004.PNG">

- Verificando com o ls a pasta que foi clonada

<img src="./img/git-github005.PNG">

- Podemos clonar o repositório com outro nome

<img src="./img/git-github006.PNG">

- Criando um repositório local e adicionando o git init e observando com cat config que ele não está associado a nenhum repositório online

<img src="./img/git-github007.PNG">

- Após utilizar o comando git remote add origin com a url do repositório online que queremos associar no repositório local, conseguimos ver que ele foi associado atraves de cat config

<img src="./img/git-github008.PNG">

## Salvando alterações locais

- Breve resumo do que foi estudo até agora

<img src="./img/git-github009.PNG">

- Com o git status observamos como esta o estado atual do repositório

<img src="./img/git-github010.PNG">

- Com o touch README.md criamos um arquivo na pasta e ao rodar o git status novamente ele mostra o estado atual e a alteração que foi feita e também mostra um sugestão do que pode ser feito

<img src="./img/git-github011.PNG">

- Com o git add e o nome do arquivo especificamos qual arquivo vamos colocar na staging area para ser incluído no próximo commit

<img src="./img/git-github012.PNG">

- Com o git commit -m"mensagem" criamos um novo commit no repositório git com uma mensagem associada ao commit

<img src="./img/git-github013.PNG">

- Com o git log podemos ver os históricos de commit em um repositório git

<img src="./img/git-github014.PNG">

- Com o git status observamos que não à nenhuma alteração a ser feita

<img src="./img/git-github015.PNG">

- Ao utilizar o mkdir e criar uma pasta vazia e rodar o git status ele não reconhece a pasta vazia como uma alteração

<img src="./img/git-github016.PNG">

- Ao utilizar o touch indicando a pasta criada anteriormente, criaremos um arquivo nela, em seguida rodaremos o git status e agora ele consegue ver a pasta

<img src="./img/git-github017.PNG">

- Com o comando echo o caminho da pasta > .gitignore estamos criando um arquivo .gitignore que dentro dele tera escrito o caminho da pasta

<img src="./img/git-github018.PNG">

- Com o git status podemos ver que o arquivo .gitignore foi listado com untracked e a pasta praticando-git-e-github foi ignorada

<img src="./img/git-github019.PNG">

- Ao utilizar echo > .gitignore, criamos um novo arquivo .gitignore vazio, ao roda o git status ele volta a ver a pasta que antes estava ignorada

<img src="./img/git-github020.PNG">

- Geralmente ao criar uma nova pasta existe uma convenção que é criar dentro dela um arquivo chamado .gitkeep para a pasta não ficar vazia

<img src="./img/git-github021.PNG">

- Com o git status e utilizando a convenção a pasta sera reconhecida mesmo estando "vazia"

<img src="./img/git-github022.PNG">

- Com o git add . estamos indicando que vamos adicionar todos os arquivos para a area de staging

<img src="./img/git-github023.PNG">

- Utilizando o git commit -m"mensagem" fizemos o nosso commit para o repositório do git

<img src="./img/git-github024.PNG">

- Com o git log observamos nosso histórico de commits

<img src="./img/git-github025.PNG">

## Desfazendo alterações no repositório local

- Utilizando o rm -rf .git para remover a força o diretório git

<img src="./img/git-github026.PNG">

- Com o git status vemos que o repositório não é mais um repositório git

<img src="./img/git-github027.PNG">

- Com o git restore e indicando o nome do arquivo, conseguimos voltar ao último estado do commit caso tenha feito alguma alteração, como apagar o conteúdo do arquivo. Obs: tomar cuidado ao utilizar esse comando

<img src="./img/git-github028.PNG">

- Com o git commit --amend -m "mens" alteramos a mensagem do nosso ultimo commit

<img src="./img/git-github029.PNG">

- Com o git reset --soft e o hash do commit, nós voltamos o commit anterior para a area de staging novamente

<img src="./img/git-github030.PNG">

- Com o git reset --mixed e o hash do commit, voltamos a area de trabalho antes da area de staging

<img src="./img/git-github031.PNG">

- Com o git reset --hard e o hash do commit, apagamos tudo e voltamos até o ultimo commit. Obs: muito cuidado ao usar esse comando

<img src="./img/git-github032.PNG">

- Utilizando o git reflog para ter um histórico mais detalhado do repositório local e todas essas alterações deve ser feitas antes de serem enviadas ao repositório remoto

<img src="./img/git-github033.PNG">

## Enviando e baixando alterações com o repositório remoto

- Pegando as alterações locais e colocando no repositório remoto

<img src="./img/git-github034.PNG">

<img src="./img/git-github035.PNG">

<img src="./img/git-github036.PNG">
