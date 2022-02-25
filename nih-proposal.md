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
    \vspace{1ex}
    \setlength\parindent{0cm}
    \large\bfseries{#1}
  }
  \setcounter{subsubsection}{0}
}
\renewcommand{\subsubsection}[1]{
  \refstepcounter{subsubsection}{
    \vspace{1ex}
    \setlength\parindent{0cm}
    \normalsize\bfseries{#1}
  }
  \setcounter{paragraph}{0}
}
\renewcommand{\paragraph}[1]{
  \refstepcounter{paragraph}{
    \vspace{1ex}
    \setlength\parindent{0cm}
    \normalsize\itshape{#1}
  }
  \setcounter{subparagraph}{0}
}
\renewcommand{\subparagraph}[1]{
  \refstepcounter{subparagraph}{
    \vspace{1ex}
    \setlength\parindent{0cm}
    \normalsize{#1}
  }
}

\renewcommand*{\thefootnote}{\fnsymbol{footnote}}


Attachments checklist (K series):[^page-limits]

- [ ] Project Summary or Abstract
- [ ] Project Narrative
- [ ] Introduction to Resubmission or Revision Application (when applicable)
- [ ] Candidate Information and Goals for Career Development and Research Strategy
- [ ] Specific Aims
- [ ] Training in the Responsible Conduct of Research
- [ ] Candidate's Plan to Provide Mentoring
- [ ] Plans and Statements of Mentor and Co-mentor(s)
- [ ] Letters of Support from Collaborators, Contributors, and Consultants
- [ ] Description of Institutional Environment
- [ ] Institutional Commitment to Candidate's Research Career Development
- [ ] Biographical Sketch[^biosketch]

[^page-limits]: following the NIH page on Page Limits: <https://grants.nih.gov/grants/how-to-apply-application-guide/format-and-write/page-limits.htm>
[^biosketch]: templates: Word (NIH) <https://grants.nih.gov/grants/forms/biosketch.htm>, LaTeX <https://github.com/corybrunson/latex-nihbiosketch>


# Project Summary

This attachment is used to illustrate various style elements.

## Citations

Inline citations [@article; @book; @incollection] can be tagged from the bibliography file.

### Formatting

Citations are formatted according to the Citation Style Language (CSL) style `council-of-science-editors.csl`,[^style-url] which retains information about conference proceedings and working papers (for example) lost by the previously-used `national-institute-of-health-research.csl`.
(Note that abstract symbols are used for footnote superscripts in order to avoid confusion with numerical citation superscripts.)

## Underlined text

While inline <span class="underline">underlined text</span> must be rendered using the Pandoc constructor, style elements like section headers can be underlined in their LaTeX definitions.
Because the constructor invokes the `\underline` command to render LaTeX documents, this command is redefined to the more convenient `\uline` from the **ulem** package in the front matter.

## Headers and sections

Top-level headers or sections are treated as separate attachments and begin on new pages.

The remaining levels are subsections (such as this one), subsubsections, paragraphs, and subparagraphs (illustrated below). These are consistently formatted for convenience, but lower levels should probably be used sparingly.

### Subsubsection

This is a subsubsection.

#### Paragraph

This is a paragraph.

##### Subparagraph

This is a subparagraph.

Custom formatting of inline paragraph headers, as is done in the Specific Aims attachment, may be preferred to paragraph or subparagraph headers that occupy whole lines.

[^style-url]: <https://github.com/citation-style-language/styles/blob/master/council-of-science-editors.csl>


# Specific Aims

This template is being prepared to accomplish three research aims:

**Aim 1:**
Reduce time spent formatting, consolidating, and revising NIH applications by allowing researchers to work entirely in plain-text Markdown[^md] during the writing process.

[^md]: <https://www.markdownguide.org/>

**Aim 2:**
Raise awareness of the "Markdown + Pandoc"[^pandoc] workflow among researchers who might benefit from adopting it.

**Aim 3:**
Add a line item to my personal CV.

[^pandoc]: <https://pandoc.org/MANUAL.html>


# Bibliography and References Cited


<!--
# PDF (via LaTeX)
pandoc nih-proposal.md \
  -t latex \
  -N \
  --bibliography=nih-proposal.bib \
  --citeproc \
  --csl=council-of-science-editors.csl \
  -o nih-proposal.pdf
# Microsoft Word (.docx)
pandoc nih-proposal.md \
  --bibliography=nih-proposal.bib \
  --citeproc \
  --csl=council-of-science-editors.csl \
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
