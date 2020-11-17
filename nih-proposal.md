---
title: NIH Grant Proposal Template
author: Jason Cory Brunson
date: 2020-11-17
titlepage: false
documentclass: article
fontsize: 11pt
header-includes: |
  \usepackage{palatino}
  \renewcommand*\familydefault{\sfdefault}
  \usepackage[T1]{fontenc}
  \linespread{1.05}
  \usepackage{lipsum}
  \usepackage{amsfonts, amsmath, amsthm, amssymb}
  \usepackage{graphicx}
  \usepackage{booktabs}
  \usepackage{wrapfig}
  \usepackage[labelfont=bf]{caption}
  \usepackage[top=.5in,bottom=.5in,left=.5in,right=.5in]{geometry}
  \pagestyle{empty}
  \DeclareSymbolFont{letters}{OML}{txr}{m}{it}
  \usepackage{sectsty}
  \usepackage{multirow}
  \usepackage[normalem]{ulem}
  \usepackage{array}
  \usepackage{textcase}
  \usepackage{perpage}
  \MakePerPage{footnote}
---

\setlength\parskip{0pt plus 0pt}
\setlength\parindent{.5cm}

\renewcommand{\thesection}{}
\renewcommand{\thesubsection}{{\thesection}\Alph{subsection}.}
\renewcommand{\thesubsubsection}{{\thesubsection}\arabic{subsection}.}

<!--
\usepackage[compact]{titlesec}
\titlespacing\section{0pt}{0.5em minus 0em plus 0em}{0.5em minus 0em plus 0em}
-->

\renewcommand{\section}[1]{
  \newpage
  \begin{center}
  \normalsize\bfseries\MakeTextUppercase{#1}
  \end{center}
  \setcounter{section}{0}
}
\renewcommand{\subsection}[1]{
  \refstepcounter{subsection}{
    \setlength\parindent{0cm}
    \normalsize\bfseries\uline{\thesubsection\ #1}
  }
  \setcounter{subsubsection}{0}
}
\renewcommand{\subsubsection}[1]{
  \refstepcounter{subsubsection}{
    \setlength\parindent{0cm}
    \normalsize\itshape\uline{\thesubsubsection\ #1}
  }
}

\renewcommand*{\thefootnote}{\fnsymbol{footnote}}


# Project Summary

\lipsum[1]


# Introduction

The introduction is used to illustrate citations from the bibliography file [@article; @book; @incollection].
Citations are formatted according to the Citation Style Language (CSL) style `national-institute-of-health-research.csl`.[^style-url]

[^style-url]: <https://github.com/citation-style-language/styles/blob/master/national-institute-of-health-research.csl>


# Specific Aims

\lipsum[2-4]

**Aim 1:**
\lipsum[5]

**Aim 2:**
\lipsum[6]

**Aim 3:**
\lipsum[7]


# Research Strategy

## Significance

\lipsum[8-9]

### Impact

\lipsum[10]

### Merit

\lipsum[11]


## Investigators

### First Author

\lipsum[12]

### Second Author

\lipsum[13]


## Innovation

\lipsum[14-17]


## Approach

\lipsum[18]

### Resources

\lipsum[19-21]

### Proposed methodology

\lipsum[22-25]


# Bibliography and References Cited


<!--
pandoc nih-proposal.md \
  -t latex \
  -o nih-proposal.pdf \
  -N \
  --bibliography=nih-proposal.bib \
  --csl=national-institute-of-health-research.csl
-->

<!--
https://www.latextemplates.com/template/nih-grant-proposal
https://www.soimort.org/notes/161117/
https://github.com/Wandmalfarbe/pandoc-latex-template/issues/3#issuecomment-302539900
https://verbosus.com/bibtex-style-examples.html
-->
