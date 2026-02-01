CHAPTERS_FILE := build/chapters.tex
STRUCTURE_FILE := manifest.yml
GEN_SCRIPT := scripts/generate_book.py

.PHONY: default clean

default: $(CHAPTERS_FILE)
	pdflatex book.tex
	bibtex book
	makeindex book.nlo -s nomencl.ist -o book.nls
	pdflatex book.tex
	pdflatex book.tex

$(CHAPTERS_FILE): $(STRUCTURE_FILE) $(GEN_SCRIPT)
	python3 $(GEN_SCRIPT) $(STRUCTURE_FILE) $(CHAPTERS_FILE)

clean:
	rm -f *.aux *.log *.bbl *.blg *.out *.nlo *.nls *.ilg *.lof *.lot *.toc *.synctex.gz \
		book.pdf *~
	rm -f $(CHAPTERS_FILE)
