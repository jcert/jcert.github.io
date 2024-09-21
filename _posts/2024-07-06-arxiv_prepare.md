---
title: 'Preparing for arXiv'
date: 2024-07-07
permalink: /posts/2024/07/arxiv/
sitemap: false
tags:
  - arXiv
  - operational
---


Preparing arXiv submission
======

Say that you are preparing to put some paper on arXiv,
your main TeX file is `main.tex`, what I usually do is
 - compile the latex locally
 - strip comments from the latex files
 - reduce the .bib to contain only the citation you need 
 - put the files needed for submission in a folder and zip them (\*.tex, \*.cls, \*.sty, \*.bst, \*.bib, \*.bbl, ...) 


## To strip the comments 
I usually do
```sh
sed 's/^\%.*$/\%/g' main.tex > aux1.tex 
sed 's/\([^\\]\)\%.*$/\1\%/g' aux1.tex > aux.tex 
if [[ $(grep -c \begin{comment aux.tex) -ne 0 ]]; then echo "remove the \begin{comment} manually"; fi  
diff main.tex aux.tex > aux.diff
```
 Then remove the `\begin{comment}` blocks manually, if there are any, 
 and then check the diff to see if anything got deleted by accident.

make sure the % is not escaped


## To reduce the .bib to contain only the citations we use

After compiling `main.tex` there will be a `main.aux` in the project folder, then run
`bibexport -o extracted.bib main.aux `

and replace your `X.bib` with `extracted.bib` (delete `X.bib` and rename `extracted.bib` into `X.bib`). 


Or, if I manually merge two bib files into `X.bib`, I use
`bibexport -a -o b.bib X.bib` to extract all unique entries (by their keys) into b.bib. 





##

check that all sets are describe with either `:` or `|`, but not both



post-doc ? 
https://euraxess.ec.europa.eu

https://universitypositions.eu/


https://academicpositions.com/


https://www.reddit.com/r/ControlTheory/wiki/academic_positions/#wiki_overall_organization




