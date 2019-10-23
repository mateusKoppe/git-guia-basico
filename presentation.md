---
title: Git
subtitle: Do noob até o Wizard lv12
---

# Por que aprender git?
- Ferramenta de controle de versão
- Ótimo para trabalhar em equipe
- Uma ótima forma de backup
- Mantem o histórico de tudo
- Muito melhor que salvar código em GDrive ou Dropbox
- É de longe a ferramente mais adotada para versionamento no meio open-source
- Para ser o/a top da balada

# Um pouco de história
![Linus Torvalds criador do Git](./images/torvalds.jpg)

Foi criado em 2005 por Linus Torvalds para o versionamento do kernel Linux após desentendimento com a empresa responsável pelo DVCS. Foi rapidamente adotado por outros projetos.

# Sobre a apresentação

## Slides
[github.com/mateusKoppe/git-guia-basico](https://github.com/mateusKoppe/git-guia-basico)

## Links (muito) úteis
- [git-scm.com/book/pt-br/v1](https://git-scm.com/book/pt-br/v1)
- [github.github.com/training-kit/downloads/pt_BR/github-git-cheat-sheet.pdf](https://github.github.com/training-kit/downloads/pt_BR/github-git-cheat-sheet.pdf)
- [github.github.com/training-kit/downloads/pt_BR/github-git-cheat-sheet/](https://github.github.com/training-kit/downloads/pt_BR/github-git-cheat-sheet/)

# Um pouco sobre bash
```bash
pwd # Exibe o diretório atual
ls # Lista os arquivos e pastas no diretório
mkdir <pasta> # Cria um diretório
cd <pasta> # Entra no diretório informada
mv <atual> <novo> # Renomea um arquivo ou diretório
```

# Como instalar

## Linux
```
sudo apt install git # Debian based
```

## Mac
```
brew install git
```

## Windows
Baixe o executável no site oficial e instale

# Criando um repositório
Repositório é o local onde você armazenará e versionará o seu código.

Navege até o diretório do seu projeto e digite:
```bash
# Inicia um repositório vazio
git init
```
Quando você executar esse comando uma pasta `.git` será criada no diretório e essa pasta conterá todos os meta dados para gerenciar o seu repositório.

# Um pouco do conceito
O git funciona com base em snapshots, que armazenam as modificações que foram feitas ao longo do projeto.

Essas snapshots agem como "fotografias" que irão salvar o estado do projeto naquele momento, e então irão salvar essas mudanças em um commit.
![Exemplo de snapshot](./images/snapshots.png)

# Setup
Antes de começarmos é necessário configurar algumas informações no git, como por exemplo o nome e o e-mail do usuário já que esses dados que estarão atrelados ao commit.
```bash
git config --global user.name <name>
git config --global user.email <email>
```

## Sobre --global
Utilize apenas no seu computador pessoal, caso você queria definir a configuração apenas para um repositório específico use `--local` (já é o padrão)

# Precisando de ajuda?
```bash
git help # Lista comandos possíveis
git help [comando] # Exibe informações sobre o comando
```

# Comandos e conceitos básicos
O básico para "se virar".

* `git status`
* `git add`
* `git commit`
* `git reset`
* `git diff`

# git status
`git status` é o comando que você utilizará sempre que quiser informações sobre as modificações no repositório.
```bash
# Recebe status do repositório, dos arquivos
git status
```
Os arquivos no seu repositório estarão em um dos dois estados: untracket (não monitorado) ou tracked (monitorado).

# git status

## Tracked (monitorado)
Arquivos em tracked são os arquivos que já estavam na seu último commit, ou seja, o repositório já sabe da existencia desse arquivo.

O arquivo pode estar em um dos seguintes estados: unmodified (não modificado), modified (modificado), ou staged (selecionado).

## Untracked (não monitorado)
São os arquivos que ainda não fazem parte do histório do repositório ou ainda não foram selecionados.

# Dicas
Você pode passar a flag `-s` para ver uma versão curta e mais amigável do status.
```
git status -s
```

# git add
Quando você quiser adicionar/monitorar um arquivo para ser commitado você deve utilizar o comando `git add`, esse comando alterará o status do arquivo para staged.

(vai deixar o arquivo verdinho na lista)

```bash
# Adiciona arquivos para serem trackeados
git add <arquivo ou pasta>
```

# Dica
Caso esteja com preguiça de digitar manualmente todos os arquivos que foram modificados você pode simplesmente adicionar o diretório inteiro utilizando `.`, mas tome cuidado para não adicionar arquivo indesejáveis.

```bash
git add .
```

# git reset
> Adicionei um arquivo in staged sem querer, e agora?
Você pode usar `git reset` para retornar um arquivo para o seu status original.

Git status por padrão não irá fazer você perde código.

Outras funcionalidades do `git reset` serão listadas futuramente.

```bash
git reset <arquivo>
```

# git commit
Tudo pronto? Chegou a hora de salvar as mudanças em um commit com uma mensagem dizendo o que esse commit faz, para isso use o comando `git commit`.

O commit é justamente o que da essa ideia de snapshots, será com commits que você ira salvar determinados momentos do seu código e irá "encapsular" as mudanças selecionadas.

```bash
# Cria um commit abrindo-o em um editor
git commit

# De forma rápida:
git commit -m "<message>"
```

# git log
> E para ver isso aí??

Utilize git log para ver quais são os logs de commits do seu repositório.
```bash
# Exibe os logs
git log

# Uma linha por log
git log --oneline
```

# Dica
Você pode usar a flag `--oneline` para visualizar os commits em apenas uma linhas e `--graph` para visualizar o histório de commit em forma de gráfico.
```bash
git log --oneline
git log --graph
git log --oneline --graph # Why not both?
```

# git diff
```bash
# Exibe as diferenças que não foram adicionadas
git diff

# Exibe as que foram adicionadas:
git diff --cached
```

# Branchs
* git-branch
* git-checkout
* git-stash
* git-merge

# git-branch
```bash
# Lista as branchs criadas e exibe a brach atual
git branch

# Cria uma nova branch baseada na branch atual
git branch <name>

# Deleta uma branch
git branch -d <name>
```

# git-checkout
```bash
# Troca de branch
git checkout <name>

# Cria e troca de branch
git checkout -b <name>
```

# git-stash
```bash
# Salva as mudanças de uma branch e reseta-a
git stash

# Retorna as mudanças que foram salvas para a branch
git stash apply
```

# git-merge
```bash
# Junta os commits da branch atual com a branch alvo
git merge <name>
```

# Remote
Git não faria sentido se não houvesse uma forma de armazenar os repositório em algum lugar onde possa ser compartilhado para outras pessoas.

Crie um repositório online

##
* git-remote
* git-push
* git-pull
* git-clone

# Criando um repositório no Github
![](./images/create-online-repo.png)

# Criando um repositório no Github
![](./images/online-repo.png)

# git-remote
```bash
# Lista os repositórios adicionados
git remote

# Adiciona um repositório remoto
git remote add <name> <url>

# Por convenção o repositório principal geralmente
# é nomeado como origin
git remote add origin <url>
```

# git-push
```bash
# Push = Empurra
# Envia os commits da branch selecionada
# para o remote selecionado
git push <remote> <branch>

# O mais comum é
git push origin master
```

# git-pull
```bash
# Pull = Puxa
# Atualiza a branch selecionada de acordo com o
# remote selecionado
git pull <remote> <branch>
```

# git-clone
```bash
# Clona um repositório online
git clone <url> [<folder>]
```

# Gitignore
Caso seja necessário que o repositório ignore algum arquivo ou algumas pasta é possível criar um `.gitignore`, nele você insere quais arquivos deverão ser ignoradas no repositório.

# Variável HEAD
Reflete o branch e commit atual.
Você também pode utilizar `~<n>` para referenciar commits anteriores.

```
# Macetes
git push origin HEAD

git reset --head HEAD~1
```
