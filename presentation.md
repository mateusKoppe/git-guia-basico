---
title: Git
subtitle: Do noob até o Wizard lv12
author: Mateus Koppe
---

# Um pouco de história

![Linus Torval criador do Git](./images/torval.jpg)

Foi criado em 2005 por Linus Torval para o versionalmento do kernel Linux e foi rapidamente adotado por outros projetos.

# Como instalar

## Debians based
```
sudo apt install git
```

## Red-Hat based
```
sudo dnf install git
```

## Arch based
```
sudo pacman -S git
```

## Windows
Não sei, procura lá

# Setup
```bash
git config --global user.name <name>
git config --global user.email <email>
```

# Criando um repositório
```bash
# Inicia um repositório vazio
git init
```

# Comandos e conceitos básicos
* git-add
* git-status
* git-commit
* git-log
* git-diff

# git-add
```bash
# Adiciona arquivos para serem trackeados
git add <files>
```

# git-status
```bash
# Recebe status do repositório, dos arquivos
git status

```

# git-diff
```bash
# Exibe as diferenças que não foram adicionadas
git diff

# Exibe as que foram adicionadas:
git diff --cached
```

# git-commit
```bash
# Cria um commit
git commit

# De forma rápida:
git commit -m "<message>"
```

# git-log
```bash
# Exibe os logs
git log

# Uma linha por log
git log --oneline
```

# Remote
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
