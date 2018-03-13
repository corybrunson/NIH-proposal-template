# NIH Grant Proposal Template

## Motivation

Grantwriting is an increasingly important component of academic research, and young researchers in particular need to hone our written communication alongside our investigative and networking skills.
This template aims to simplify the grant proposal formatting process in order to allow grantwriters to concentrate on the writing.

## Usage

The template uses [Markdown](https://daringfireball.net/projects/markdown/) formatting with \LaTeX metadata from [the NIH Grant Proposal template](https://www.latextemplates.com/template/nih-grant-proposal).
Use the following [Pandoc](https://pandoc.org/MANUAL.html) call to produce the PDF:

```bash
pandoc nih-proposal.md -o nih-proposal.pdf
```

## Needs

I'm new both to grantwriting and to Pandoc, but a search for Markdown grant proposal templates yielded no results. This initial attempt omits important elements of document structure, including wrapped figures, which [require more proficiency](http://blog.hartleygroup.org/2016/01/18/wrapping-figures-in-pandoc-pdfs/) than i can bring. So i invite anyone with ideas for improving this template to suggest them via an [issue](/../../issues) or a [pull request](/../../pulls)!

- Add some example footnotes and citations. Refer to [Yao's boilerplating post](https://www.soimort.org/notes/161117/).
- Figure out how to [remove the title page](https://github.com/Wandmalfarbe/pandoc-latex-template/issues/3#issuecomment-302539900).
- Add a table and a figure to the text, text-wrapped if possible.
