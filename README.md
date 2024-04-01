# Guia de utilização do GIT

## Índece

1. [O que é Git?](#o-que-e-git)
2. [Instalação](#instalacao)
3. [Configurando o Git](#conf-git)
4. [Criar/Clonar um Repositório](#criar-clonar-repo)
5. [Fluxo de Trabalho](#fluxo-de-trabalho)
6. [Alterações - Adicionar e Confirmar](#add-commit)
7. [Repositório Remoto](#repo-remoto)
8. [Ramificações](#ramos)
9. [Atualizar o Repositório](#atualizar-repo)

- [Referências](#refe)

<div id="o-que-e-git" />

## O que é Git?

Para começar, saiba diferenciar Git de Github. Github precisa do Git, mas Git não precisa de Github.<br>
Git é um software de versionamente, usado para gerenciar o desenvolvimento de software nas suas mais diversas versões.<br>
Todo profissional deve utilizar Git, nem mesmo que não faça push para lugar nenhum, só quem já perdeu um projeto ou um arquivo importante sabe a real importância de sempre utilizar Git.

<div id="instalacao" />

## Instalação 

Dependendo do sistema operacional que utilizar procure na internet a melhor forma de instalçao do Git na sua máquina.<br>
Eu uso Arch Linux BTW, então:<br>
`$ sudo pacman -S git` <br>
Para verificar se a instação foi feita com sucesso use: <br>
`$ git --version`

<div id="conf-git" />

## Configurando o Git

Após a instalação a primeira coisa a se fazer é configurar o usuário do Git local ou globalmente.<br>
Para isso use: <br>
`$ git config --global user.name "nome do usuario"` -> Configura o usuário globalmente <br>
`$ git config --global user.email "usuario@email.com"` -> Congigura um email globalmente <br>

<div id="criar-clonar-repo" />

## Criar/Clonar um Repositório

Para iniciar o Git em qualquer repositório uso o comando: <br>
`$ git init` <br>
Você também pode clonar um repositório que já existe com: <br>
`$ git clone /caminho/repositorio` <br>
Clonar um repositório remoto: <br>
`$ git clone http://url.com` ou `$ git clone user@host:/caminho/repositorio` <br>

<div id="fluxo-trabalho"/>

## Fluxo de Trabalho

O Git funciona com 3 "áreas" sendo elas: <br>
**Diretório de Trabalho** -> contém os arquivos vigentes. <br>
**Index(Stage)** -> área temporária. <br>
**HEAD** -> último commit. <br>

Diretório de trabalho (add)-> Index (commit)-> HEAD

<div id="add-commit"/>

## Alterações - Adicionar e Confirmar

Sempre antes de fazermos de fato uma alteração é bom usar o comando: <br>
`$ git status` <br>
Que mostrará todas as alterações feitas. <br>

Para adcionar uma mudança ao Index usamos: <br>
`$ git add <arquivo>` ou `$ git add *`<br>

**ATENÇÃO!** - Lembre de usar o arquivo `.gitignore` para dizer ao git o que **Não será adicionado/ignorado** principalmente com arquivos `.env` ou configurações que tenham senhas/chaves/tokens ou qualquer outra coisa que **Não deve ser compartilhada!**<br>

Para confirmar as alterações fazemos um commit: <br>
`$ git commit -m "Descrição da alteração"` <br>

Agora nossas mudanças estão no HEAD, mas ainda não foram para o **Repositório remoto**. <br>

<div id="repo-remoto" />

## Repositório Remoto

Caso não tenha clonado um repositório existente, precisa conectar seu repositório. <br>
`$ git remote add origin <servidor ou url>` <br>

Para enviar alterações ao repositório remoto, use: <br>
`$ git push origin main`, obs: **main** é o nome da Branch (ramo) do projeto, podendo ser também a **master**. <br>

<div id="ramos" />

## Ramificações

Branches ("Ramos") são utilizados para desenvolver funcionalidades, corrigir bugs, implementar novas versões isoladas umas das outras. A branch **main** ou **master** é a branch padrão de qualquer projeto. <br>

Criando uma branch: <br>
`$ git checkout -b funcionalidade_xyz`<br>

Retorne ao main com: <br>
`$ git checkout main` <br>

Remova uma Branch com: <br>
`$ git branch -d funcionalidade_xyz`

Uma branch não é disponível para outros a não ser que você disponibilize ela para os outros: <br>
`$ git push origin funcionalidade_xyz` <br>

<div id="atualizar-repo" />

## Atualizar o Repositório

Para atualizar seu repositório local, use: <br>
`$ git pull` <br>

Antes de fazer merge, podemos pré-vizualizar as alterações com: <br>
`$ git diff <branch origem> <branch destino>`

Para fazer merge da sua branch com sua branch ativa, use: <br>
`$ git merge <branch>`

<div id="refe" />

## Referências

[Git - Documentation](https://git-scm.com/doc)<br>
[GIT Tutorial Para Iniciantes](https://www.hostinger.com.br/tutoriais/tutorial-do-git-basics-introducao)<br>
[Entendendo GIT | (não é um tutorial!)](https://youtu.be/6Czd1Yetaac?si=NVYGp4dz8LCFuDX1)<br>
[Protegendo e Recuperando Dados Perdidos - Git, Backup, BTRFS](https://youtu.be/yfEhz9poqW8?si=ixbhgXMLlS6o8HM0)<br>
[Git - Guia prático](https://rogerdudler.github.io/git-guide/index.pt_BR.html)<br>
