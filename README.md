# ticklabels.command - read ticks labels from commands


## Overview

A small [PGFPlots](https://ctan.org/pkg/pgfplots) library to read tick labels from the content of a command through a key `ticklabels from command`

## Installation

Place tikzlibrarypgfplots.ticklabels.command.code.tex in a directory read by your tex compiler. 

## Licence

[Gnu General Public version, 3](https://ctan.org/license/gpl3), as for [PGFPlots](https://ctan.org/pkg/pgfplots).

## Motivation and usage

It is suitable to write 
```latex
'\newcommand{\myticks}{1,2,3}
```
and then to set 
```latex
xtick=\myticks
```
as parameter to axis.
However, this cannot be done for 
`xticklabels` as the content 
if the command is considered as the first label.
This small library provides a new key `xticklabels from command` in which the labels are expanded.
```latex
'\newcommand{\mytickslabels}{a,b,c}
\begin{axis}[xticklabels from command=\mytickslabel]
...
\end{axis}
```

## TODO

Add minor ticks

## Note

This is an alpha version.
