# LaTeX beamer template for presentations at BOKU

This template can be used to create presentations to be held for or at BOKU university.

## Provided files
The following files and folders are present:
- **_images/**: folder where header images for titlepage and section pages are located
- **beamerthemeboku.sty**: styling package for usage as beamer theme
- **bokucolors.sty**: contains color definition corresponding to corporate design of BOKU
- **slides.tex**: this is the main file where the slides (frames) are defined
- **slides_16-9.pdf** / **slides_4-3.pdf**: showcase of presentation slides in 16:9 and 4:3 format, respectively

## Compilation process  
To get the compilation process correct one has to run `pdflatex` once, then `biber` (as backend for `biblatex`) once and again two times `pdflatex` to ensure correct *.pdf* creation and get proper linking.
One can also use the `latexmk`-command in following forms:
- `latexmk -pdf`: compiles all *.tex* files
- `latexmk -pdf -pv`: as before and additionally opens a preview of the *.pdf*
- `latexmk -pdf slides.tex`: just compiles *slides.tex* and generates *slides.pdf*

To clear all temporary files made during compilation process for LaTeX just execute:
- `latexmk -c` (lowercase c)
- `latexmk -C` (uppercase C): does the same as `latexmk -c` and additionally removes the generated *.pdf* file

> **Note**
> When `latexmk` doesn't work, make sure that the *latexmk* package is installed on your system.
> Usually it comes with the provided LaTeX distributions like *TeX Live* or *MiKTeX*. If somehow it is still not installed it has to be installed via the distributions package manager or you can install it manually.
