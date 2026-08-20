# CV LaTeX Source

This directory contains the complete LaTeX source for the CV. Building it does not replace the PDF currently linked from the website.

## Build

The CV requires XeLaTeX, Biber, and Latexmk. From the repository root, run:

```bash
make -C cv
```

The generated CV is `cv/build/Howerton_CV.pdf`. Build artifacts are ignored by Git. To remove them, run `make -C cv clean`.

## Source Organization

- `Howerton_CV.tex` defines the document and bibliography formatting.
- `cvstyle.sty` contains typography, colors, margins, headers, and reusable layout commands.
- `sections/` contains the editable CV sections.
- Published entries come from `_bibliography/papers.bib`; submitted and in-preparation entries come from `manuscripts.bib`.

The live file at `assets/pdf/Howerton_CV.pdf` and the `/cv/` website route remain unchanged.
