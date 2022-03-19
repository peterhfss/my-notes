# Git

* [Introdução](#introdução)
    * [O que é Git?](#o-que-é-git)
    * [Para que serve?](#para-que-serve)
    * [Instalação](#instalação)
* [Arquivo .gitignore](#arquivo-gitignore)
* [Comandos do Git](#comandos-do-git)
* [Branches](#branches)
    * [Comando git merge](#comando-git-merge)
    * [Comando git rebase](#comando-git-rebase)
    * [Resolvendo conflitos](#resolvendo-conflitos)
* [Desfazer alterações](#desfazendo-alterações)
* [Verificando modificações e salvando marcadores](#verificando-modificações-e-salvando-marcadores)


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
* <code>git clone</code>: comando para clonar um repositório informado no comando.
* <code>git remote add</code>: adicionar links para os repositórios remotos.
* <code>git remote</code>: lista todos os repositórios remotos.
* <code>git push</code>: comando para enviar o conteúdo do repositótio local para um repositório remoto.
* <code>git pull</code>: comando para buscar e baixar o conteúdo dos repositórios remotos para realizar a atualização imediata do repositório local.
* <code>git branch [nome_da_branch]</code>: cria uma branch nova.
* <code>git branch</code>: lista toda as branchs.
* <code>git checkout</code>: alterna para a branch que for informada.
* <code>git checkout -b [nome_da_branch]</code>: cria uma nova branch e passa a trabalahar nela.
* <code>git merge</code>: combina várias sequências de commits em um histórico unificado.
* <code>git rebase</code>: comando para mover ou combinar uma sequência de commits para um novo commit base.
* <code>git revert</code>: comando para reverter efeitos de commits anteriores.
* <code>git stash</code>: comando para gravar a condição atual do diretório ativo.
* <code>git diff</code>: comando para exibir as alterações nos commits.
* <code>git tag -a</code>: cria um objeto de tag não assinado e anotado.

**Obs**: *para sair do log de commits digite a tecla q.*

## Branches
---

As branches são ramificações que auxiliam o desenvolvimento de funcionalidades isoladas umas das outras.A branch ***master*** é a branch padrão que existe ao criar um novo repositório.

O objetivo de uso das branches esta no fato de separar esse desenvolvimento das funcionalidades em branches diferente para não causar atraso e nem impactar o funcionamento de outra funcionalidade.

### Comando git merge

Esse comando gera um novo commit , onde nele é informado  que houve uma mescla entre duas branches.

### Comando git rebase

Semelhante ao git merge ,mas com a diferença de que esse não gera um commit de merge e sim traz os commits de uma branch para outra.

### Resolvendo conflitos

Para resolvermos os conflitos que possam surgir ao executar o comando merge ou rebase:

* Visualizar no arquivo que foi informado as linhas <code><<<<<<< HEAD (Current Change)</code> e <code> ======= </code> terá o conteúdo do commit atual e a diferença entre esse commit estará  entre as linhas <code> ======= </code> e <code> >>>>>>> lista (Incoming Change) </code>.
* Identificado as diferenças, é preciso remover as informações indesejadas.
* Em seguida realize o comando <code>git add</code> para o arquivo alterado e então faça o commit.
* Após o commit realizado, o commit de merge irá ser feito.

## Desfazendo alterações
---

Para desfazer uma alteração antes de adicionar ao commit, o comando *git checkout -- <[arquivos]>*.

Para o caso de ser após  adicionar ao commit, primeiro é preciso o comando git reset HEAD <[arquivos]> e em seguida o *git checkout -- <[arquivos]>*.

Se for para reverter em um commit, é o comando git revert para ser utilizado.

## Verificando modificações e salvando marcadores
---

Com o comando <code>git diff</code> podemos visualizar as alterações que foram realizadas. Podemos também realizar comparações através desse comando.

Temos o comando <code>git tag</code> que possibilita salvarmos macros da aplicação.