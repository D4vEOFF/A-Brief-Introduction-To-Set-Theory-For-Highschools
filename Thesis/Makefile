TEXCOMPILER = pdflatex
BIBCOMPILER = bibtex

.PHONY: all compile clean compile-no-bibtex

all: compile clean

all-no-bibtex: compile-no-bibtex clean

compile: bachelor_thesis.tex
	${TEXCOMPILER} bachelor_thesis.tex
	${BIBCOMPILER} ./components/literature/literature
	${TEXCOMPILER} bachelor_thesis.tex
	${TEXCOMPILER} bachelor_thesis.tex

compile-no-bibtex:
	${TEXCOMPILER} bachelor_thesis.tex
	${TEXCOMPILER} bachelor_thesis.tex

clean:
	find . -type f -name '*.(aux|dvi|aux|toc|lof|lot|out|bbl|blg|xmpi|synctex.gz)' -delete