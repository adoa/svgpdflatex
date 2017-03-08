# SVGPDFLATEX

Convert SVG images including LaTeX commands int PDF images.

This repository contains a bash script only.


## Usage

```
$ ./svgpdflatex path/to/drawing.svg header1.tex header2.tex […]
```

## Output

The script outputs a single PDF file into the same folder where the first argument is located.


## Notes

Beware the rough edges. This script is probably very fragile.

This script requires `incscape` to be installed with version at least 0.48.

