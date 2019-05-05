<!-- # Typesetting a set of slides -->
# Impaginare trasparenze

- [Why should I use LaTeX for presentations?](https://tex.stackexchange.com/questions/41116/)
- Don't use [Powerdot](https://www.overleaf.com/learn/latex/Powerdot) please.

<!-- ## Beginners tutorials -->
## Tutorial per principianti

- 🍃 [Beamer](https://www.overleaf.com/learn/latex/Beamer)

<!-- ## Suggested readigs -->
## Letture consigliate

- [L'Arte di fare una presentazione con Beamer](http://profs.sci.univr.it/~zorzim/PresentazioniBeamer.pdf)

## Stampare le trasparenze

```latex
\documentclass[handout]{beamer}

\usepackage[frame]{pgfpages}
\pgfpagesuselayout{6 on 1}[a4paper, border shrink=5mm]

\begin{document}
\setbeamercolor{background canvas}{bg=}

[...]

\end{document}
```
