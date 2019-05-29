---
title: Git e Github
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

# Comandos básicos
* add
* status
* commit
* log
* diff

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

# 
