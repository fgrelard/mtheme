SRC = demo.tex
PDF = demo.pdf
AUX = demo.aux
TEXC := xelatex
TEXC_OPTS += -shell-escape
TEXMFHOME = $(shell kpsewhich -var-value=TEXMFHOME)
INSTALL_DIR = $(TEXMFHOME)/tex/latex/mthemeub

.PHONY: clean install

all: clean $(PDF)

$(AUX):
	$(TEXC) $(TEXC_OPTS) $(SRC)

$(PDF): beamerthememub.sty $(AUX) $(SRC)
	$(TEXC) $(TEXC_OPTS) $(SRC)

clean:
	@rm -f $(PDF)
	@rm -f $(AUX)

install:
	mkdir -p $(INSTALL_DIR)
	cp *.sty $(INSTALL_DIR)
