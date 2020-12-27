# NIH Grant Proposal Template

## Motivation

Grantwriting is an increasingly important component of academic research, and early-career researchers in particular need to hone our written communication alongside our investigative and networking skills.
This template aims to simplify the grant proposal formatting process in order to allow grantwriters to concentrate more on the writing.

## Usage

The template uses [Markdown](https://daringfireball.net/projects/markdown/) formatting with LaTeX metadata adapted from [this NIH Grant Proposal template](https://www.latextemplates.com/template/nih-grant-proposal).
Use the following [Pandoc](https://pandoc.org/MANUAL.html) call to produce the PDF via the LaTeX engine:

```bash
pandoc nih-proposal.md \
  -t latex \
  -N \
  --bibliography=nih-proposal.bib \
  --citeproc \
  --csl=national-institute-of-health-research.csl \
  -o nih-proposal.pdf
```

Alternatively, use the following call to produce a Microsoft Word (`.docx`) file:

```bash
pandoc nih-proposal.md \
  --bibliography=nih-proposal.bib \
  --citeproc \
  --csl=national-institute-of-health-research.csl \
  --reference-doc=nih-reference.docx \
  -o nih-proposal.docx
```

Both calls are commented out at the end of `nih-proposal.md`.

## Needs

The current template omits important elements of document structure, including wrapped figures, which [require more proficiency](http://blog.hartleygroup.org/2016/01/18/wrapping-figures-in-pandoc-pdfs/) than i can bring. So i invite anyone with ideas for improving this template to suggest them via an [issue](/../../issues) or a [pull request](/../../pulls)!
