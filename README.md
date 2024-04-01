# Guia de utilização do GIT

## Índece

1. [O que é Git?](#o-que-e-git)
2. [Instalção](#instalacao)
3. [Conffigurando o Git](#conf-git)
4. [Criar/Clonar um Repositório](#criar-clonar-repo)
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

<div id="refe" />

## Referências

[Git - Documentation](https://git-scm.com/doc)<br>
[GIT Tutorial Para Iniciantes](https://www.hostinger.com.br/tutoriais/tutorial-do-git-basics-introducao)<br>
[Entendendo GIT | (não é um tutorial!)](https://youtu.be/6Czd1Yetaac?si=NVYGp4dz8LCFuDX1)<br>
[Protegendo e Recuperando Dados Perdidos - Git, Backup, BTRFS](https://youtu.be/yfEhz9poqW8?si=ixbhgXMLlS6o8HM0)<br>

