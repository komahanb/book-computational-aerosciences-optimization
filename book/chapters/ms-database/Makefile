# Auto-generated chapter Makefile
CHAPTER=chapter-standalone
TEX=$(CHAPTER).tex
PDF=$(CHAPTER).pdf

LATEX=pdflatex -interaction=nonstopmode -halt-on-error -file-line-error
BIBTEX=bibtex

.PHONY: all clean

all: $(PDF)

$(PDF): $(TEX) chapter.tex ../../tex/chapter-standalone-preamble.tex
	$(LATEX) $(TEX)
	-$(BIBTEX) $(CHAPTER)
	$(LATEX) $(TEX)
	$(LATEX) $(TEX)

clean:
	rm -f $(PDF) $(CHAPTER).aux $(CHAPTER).bbl $(CHAPTER).blg $(CHAPTER).log \
	  $(CHAPTER).out $(CHAPTER).toc $(CHAPTER).lof $(CHAPTER).lot \
	  $(CHAPTER).synctex.gz $(CHAPTER).nlo $(CHAPTER).nls $(CHAPTER).ilg
