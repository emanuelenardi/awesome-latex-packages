<!-- # Distributions -->
# Distribuzioni

- [TeX Distributions](https://www.latex-project.org/get/#tex-distributions)

## TeXLive

- [Guida a TeX Live in italiano](http://texdoc.net/texmf-dist/doc/texlive/texlive-it/texlive-it.pdf)
- [Guida a TeX Live in inglese](http://texdoc.net/texmf-dist/doc/texlive/texlive-en/texlive-en.pdf)

<!-- ## Table of contents -->
## Indice dei contenuti

- [Update TeX Live](#update-texlive)
- [Upgrade TeX Live](#upgrade-texlive)

<!-- ### Update TeXLive -->
### Aggiornare TeXLive

From section "_Native TeX Live_" of [Installing/updating packages after installation](https://tug.org/texlive/pkginstall.html)

Bear in mind that `tlmgr` is the command name of the TeX Live package manager

<!-- #### Update `tlmgr` itself -->
#### Aggiornare `tlmgr` stesso

```latex
tlmgr update --self
```

<!-- #### Update a specific package -->
#### Aggiornare un pacchetto specifico

```latex
tlmgr update <pkgname>
```

<!-- #### Update all packages -->
#### Aggiornare tutti i pacchetti

<!-- If you would like to see what would be done before doing it, run -->
```latex
tlmgr update --list
```

<!-- To install new packages and to update already installed ones -->
To install new packages and to update already installed ones
```latex
tlmgr update --all
```

<!-- ### Upgrade TeXLive -->
### Aggiornare TeXLive

<!-- From [Upgrade TeX Live distribution](https://tug.org/texlive/upgrade.html) "Please do a new installation", therefore see [Installing TeX Live over the Internet](https://tug.org/texlive/acquire-netinstall.html). -->
Da [Upgrade TeX Live distribution](https://tug.org/texlive/upgrade.html) "Fai una nuova installazione", quindi guarda [Installing TeX Live over the Internet](https://tug.org/texlive/acquire-netinstall.html).
