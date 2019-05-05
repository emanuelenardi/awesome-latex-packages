<!-- # Typesetting a set of slides -->
# Impaginare trasparenze

- [Why should I use LaTeX for presentations?](https://tex.stackexchange.com/questions/41116/)
- Don't use [Powerdot](https://www.overleaf.com/learn/latex/Powerdot) please.

## Beginners tutorials

- 🍃 [Beamer](https://www.overleaf.com/learn/latex/Beamer)

## Suggested readigs

- [L'Arte di fare una presentazione con Beamer](http://profs.sci.univr.it/~zorzim/PresentazioniBeamer.pdf)

## Stampare le trasparenze

```latex
\documentclass[handout]{beamer}

\usepackage[frame]{pgfpages}

\begin{document}
\setbeamercolor{background canvas}{bg=}

[...]

\end{document}
```
