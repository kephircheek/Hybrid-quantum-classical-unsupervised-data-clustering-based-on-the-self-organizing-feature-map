.DEFAULT_GOAL:=main.pdf

.PHONY: clean
clean:
	git clean -fx main*

%.aux: %.tex
	pdflatex $<

%.bbl: %.aux *.bib
	bibtex $(basename $@)

%.pdf: %.tex %.bbl
	pdflatex $<
	pdflatex $<
