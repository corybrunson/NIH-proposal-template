---
title: NIH Grant Proposal Template
author: Jason Cory Brunson
date: 2021-02-07
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
  \renewcommand{\underline}{\uline}
  \usepackage{array}
  \usepackage{textcase}
  \usepackage{perpage}
  \MakePerPage{footnote}
---

<!--
\usepackage[compact]{titlesec}
\titlespacing\section{0pt}{0.5em minus 0em plus 0em}{0.5em minus 0em plus 0em}
-->

\renewcommand{\thesection}{}
\renewcommand{\thesubsection}{\Alph{subsection}}
\renewcommand{\thesubsubsection}{{\thesubsection}.\arabic{subsubsection}}
\renewcommand{\theparagraph}{{\thesubsubsection}.\alph{paragraph}}
\renewcommand{\thesubparagraph}{{\theparagraph}.\roman{subparagraph}}

\renewcommand{\section}[1]{
  \clearpage
  \begin{center}
  \normalsize\bfseries\MakeTextUppercase{#1}
  \end{center}
  %section counter (nested resets)
  \setcounter{subsection}{0}
  %float counters
  \setcounter{equation}{0}
  \setcounter{figure}{0}
  \setcounter{table}{0}
  %footnote counters
  \setcounter{footnote}{0}
  %spacing
  \setlength\parskip{0pt plus 0pt}
  \setlength\parindent{.5cm}
}
\renewcommand{\subsection}[1]{
  \refstepcounter{subsection}{
    \setlength\parindent{0cm}
    \normalsize\bfseries\uline{\thesubsection.\ #1}
  }
  \setcounter{subsubsection}{0}
}
\renewcommand{\subsubsection}[1]{
  \refstepcounter{subsubsection}{
    \setlength\parindent{0cm}
    \normalsize\itshape\uline{\thesubsubsection.\ #1}
  }
  \setcounter{paragraph}{0}
}
\renewcommand{\paragraph}[1]{
  \refstepcounter{paragraph}{
    \setlength\parindent{0cm}
    \normalsize\bfseries{\theparagraph.\ #1}
  }
  \setcounter{subparagraph}{0}
}
\renewcommand{\subparagraph}[1]{
  \refstepcounter{subparagraph}{
    \setlength\parindent{0cm}
    \normalsize\itshape{\thesubparagraph.\ #1}
  }
}

\renewcommand*{\thefootnote}{\fnsymbol{footnote}}


4+ months out:

- [ ] Who will be key personnel (e.g. mentors, collaborators, consultants)?
- [ ] Decide grant series, FOA (PA or RFA), and submission deadline
- [ ] Obtain (current) official instructions[^instructions]
- [ ] Who will administer the process and submit the proposal?
- [ ] What attachments are required, with descriptions and page limits?
- [ ] Know who will write supporting documents (e.g. mentor statements, letters of support, institutional environment, institutional commitment)?
- [ ] Select or schedule preliminary work (within existing research program)

3 months out:

- [ ] Draft and Specific Aims and distribute among key personnel
- [ ] Initialize bibliography (e.g. Zotero)
- [ ] Decide grant activity code, center/institute, and program (e.g. NOTI)
- [ ] Contact program officer
- [ ] Draft resource attachments (e.g. Facilities and Other Resources, Equipment, Budget Justification)
- [ ] Request letters of reference

2 months out:

- [ ] Revise and update attachments
- [ ] Draft project-related attachments (e.g. Candidate Information, Research Strategy), incorporating preliminary work
- [ ] Finalize & confirm grant activity code, center/institute, and program
- [ ] Request supporting documents

1 month out:

- [ ] Revise and update attachments
- [ ] Update NIH biosketch
- [ ] Write summary attachments (e.g. Project Summary/Abstract, Project Narrative)

[^instructions]: <https://grants.nih.gov/grants/how-to-apply-application-guide.html>


# Project Summary

\lipsum[1]


# Introduction

The introduction is used to illustrate citations from the bibliography file [@article; @book; @incollection].
Citations are formatted according to the Citation Style Language (CSL) style `national-institute-of-health-research.csl`.[^style-url]
(Note that abstract symbols are used for footnote superscripts in order to avoid confusion with numerical citation superscripts.)

While inline <span class="underline">underlined text</span> must be rendered using the Pandoc constructor, style elements like section headers can be underlined in their LaTeX definitions.
Because the constructor invokes the `\underline` command to render LaTeX documents, this command is redefined to the more convenient `\uline` from the **ulem** package in the front matter.

Below are illustrated each of the sectioning elements. In the rest of the document, only subsections and subsubsections are used within sections (attachments); paragraphs and subparagraphs are consistently formatted for convenience as needed, but should probably be used sparingly.

## Subsection

This is a subsection.

### Subsubsection

This is a subsubsection.

#### Paragraph

This is a paragraph.

##### Subparagraph

This is a subparagraph.

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
# PDF (via LaTeX)
pandoc nih-proposal.md \
  -t latex \
  -N \
  --bibliography=nih-proposal.bib \
  --citeproc \
  --csl=national-institute-of-health-research.csl \
  -o nih-proposal.pdf
# Microsoft Word (.docx)
pandoc nih-proposal.md \
  --bibliography=nih-proposal.bib \
  --citeproc \
  --csl=national-institute-of-health-research.csl \
  --reference-doc=nih-reference.docx \
  -o nih-proposal.docx
-->

<!--
# sources
https://www.latextemplates.com/template/nih-grant-proposal
https://www.soimort.org/notes/161117/
https://github.com/Wandmalfarbe/pandoc-latex-template/issues/3#issuecomment-302539900
https://verbosus.com/bibtex-style-examples.html
-->
