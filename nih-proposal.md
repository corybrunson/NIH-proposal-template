---
title: NIH Grant Proposal Template
author:
- Jason Cory Brunson
date: 6 April 2018
titlepage: false
output:
  pdf_document:
    pandoc_args: [
      "--no-tex-ligatures"
    ]
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
---

\newcommand{\att}[1]{
\begin{center}
\normalfont\bfseries\uppercase{#1}
\end{center}
\setcounter{section}{0}
}

\renewcommand{\thesection}{\Alph{section}.}
\renewcommand{\thesubsection}{{\thesection}\arabic{subsection}.}
\renewcommand{\thesubsubsection}{{\thesubsection}\arabic{subsection}.}

\renewcommand{\section}[1]{
\refstepcounter{section}
{\normalsize\bfseries{\thesection\ }#1}
\setcounter{subsection}{0}
}
\renewcommand{\subsection}[1]{
\refstepcounter{subsection}
{\normalsize\uline{\thesubsection\ #1}}
\setcounter{subsubsection}{0}
}
\renewcommand{\subsubsection}[1]{
\refstepcounter{subsubsection}
{\normalsize\itshape{\thesubsubsection\ }#1}
}

<!--
https://www.latextemplates.com/template/nih-grant-proposal
https://www.soimort.org/notes/161117/
https://github.com/Wandmalfarbe/pandoc-latex-template/issues/3#issuecomment-302539900
https://verbosus.com/bibtex-style-examples.html
-->


\newpage
\att{Project Summary}

\lipsum[1]


\newpage
\att{Introduction}

The introduction is used to illustrate citations from the bibliography file [@article;@book;@incollection]


\newpage
\att{Specific Aims}

\lipsum[2-4]

**Aim 1:**
\lipsum[5]

**Aim 2:**
\lipsum[6]

**Aim 3:**
\lipsum[7]


\newpage
\att{Research Strategy}

# Significance

\lipsum[8-9]

## Impact

\lipsum[10]

## Merit

\lipsum[11]


# Investigators

## First Author

\lipsum[12]

## Second Author

\lipsum[13]


# Innovation

\lipsum[14-17]


# Approach

\lipsum[18]

## Resources

\lipsum[19-21]

## Proposed methodology

\lipsum[22-25]

<!--
pandoc nih-proposal.md -t latex -o nih-proposal.pdf -N --bibliography=nih-proposal.bib
-->


\newpage
\att{Bibliography and References Cited}
