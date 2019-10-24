# Git: Guia básico :scroll:
 
Repositório com a o conteúdo de Git, em formato MD e PDF.

## Gerando o PDF
O PDF é gerado a partir do arquivo `git-guia-basico.md` utilizando [Pandoc](https://pandoc.org/).

Se você tiver essa depêndencia instalada você pode utilizar o Makefile para gerar o novo PDF. Para isso execute:
```bash
make
```

Caso você não queria utilizar o Makefile você pode utilizar Pandoc diretamente:
```bash
pandoc git-guia-basico.md -t beamer -o git-guia-basico.pdf
```

## Contribuindo
Correções, dúvidas, sugestões, e dicas são sempre bem vindas, se você tiver algo para contribuir [crie ume issue](https://github.com/mateusKoppe/git-guia-basico/issues/new) e contribua com o projeto :smiley:.

Pull requests também são bem vindos.
