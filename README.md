# SVGPDFLATEX

Convert SVG images including LaTeX commands into PDF images.

This repository contains a bash script only. This Bash script is intended for usage with a makefile, such as [pdflatex-makefile](https://github.com/ransford/pdflatex-makefile), where the correct dependencies can be included without too much work.

The rationale is that, unfortunately, many scolarly publishers require the figures to be submitted in a final format, not allowing any further (despite automatic) post-processing.


## Usage

```
$ ./svgpdflatex path/to/drawing.svg [header1.tex header2.tex ...]
```
The first argument is an `svg` file containing LaTeX commands.
All other (optional) arguments are `tex` files.
The latter will be included before processing the SVG file with LaTeX.

All intermediary files are handled inside a tamporary folder in `/tmp/latex/`, which on many Linux distributions is located in RAM.


## Output

The script outputs a single PDF file into the same folder where the first argument is located.


## Notes

Beware the rough edges. This script is probably very fragile.

This script requires `incscape` to be installed with version at least 0.48 and relies on the method of including SVG files into LaTeX documents described [here](https://ctan.org/pkg/svg-inkscape).

