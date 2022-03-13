# Git

* Introdução
    * O que é Git?
    * Para que serve?
    * Instalação
* Arquivo .gitignore
* Comandos do Git

## Introdução
---

### O que é Git?
Git é um sistema de controle de versão distribuído que é bastante utilizando no desenvolvimento de software.

### Para que serve?
Com o Git podemos registrar o histórico de edições de qualquer tipo de arquivo, dessa forma ao utilizarmos no desenvolvimento de software, iremos possuir um controle sobre as versões que possam surgir ao longo do projeto. Outro ponto importante é questão de flexibilidade no fluxo de trabalho, segurança e desempemnho proporcionados pelo Git.

### Instalação

No site oficial do [Git](https://git-scm.com/downloads), podemos escolhar qual sistema operacional utilizamos e baixar o instalador para o SO escolhido.

Após instalado o Git, é preciso realizar os seguintes comandos: 
> git config --local user.name "Seu nome aqui"
>
> git config --local user.email "seu@email.aqui"

## Arquivo .gitignore

É possível criar um arquivo .gitignore no diretório raiz do seu repositório e dentro dele informar para o Git quais arquivos e pastas devem ser ignorados ao fazer um commit. 

## Comandos do Git
---

* <code>git init</code>: cria um repositório na pasta que esse comando foi executado.
* <code>git status</code>: verifica o estado atual do repositório.
* <code>git add <file_name></code>: adiciona o arquivo informado da pasta atual para ser motitorado pelo Git.
* <code>git add . </code>: adiciona todos os arquivos da pasta atual para serem motitorados pelo Git.
* <code>git commit [-a] [-m "message"]</code>: efetiva as alterações realizadas informando uma mensagem com uma descrição resumida sobre essas alterações(commit).
* <code>git log</code>: exibi o histórico de commits.
* <code>git log -p</code>: exibi o log com o diff.
* <code>git log --online</code>: exibi o log em uma única linha.
* <code>git log --pretty="parametros de formatacao"</code>: exibi o log de acordo com a formatação enviada como parâmetro.



**Obs**: *para sair do log de commits digite a tecla q.*