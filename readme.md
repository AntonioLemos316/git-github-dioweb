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

## Primeiros passos git e github

- Existem duas formas de obter um repositório git na máquina local
- Transformar um diretório local que não está sob controle de versão, num repositório Git // git init

<img src="./img/git-github001.PNG">

- cd .git // acessar na pasta o caminho .git que é oculto, esse arquivo é responsavel por gerenciar nosso controle de versão

<img src="./img/git-github002.PNG">

- utilizando o ls para ver os arquivos em .git

<img src="./img/git-github003.PNG">

- Clonando um repositório Git existente
