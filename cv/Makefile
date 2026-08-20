LATEXMK := latexmk
OUTPUT_DIR := build
FULL_TARGET := Howerton_CV
SECTION_SOURCES := $(wildcard sections/*.tex)

.PHONY: all clean

all: $(OUTPUT_DIR)/$(FULL_TARGET).pdf

$(OUTPUT_DIR)/$(FULL_TARGET).pdf: $(FULL_TARGET).tex cvstyle.sty manuscripts.bib $(SECTION_SOURCES) ../_bibliography/papers.bib
	@mkdir -p $(OUTPUT_DIR)
	$(LATEXMK) -xelatex -interaction=nonstopmode -halt-on-error -file-line-error -outdir=$(OUTPUT_DIR) $(FULL_TARGET).tex

clean:
	$(LATEXMK) -C -outdir=$(OUTPUT_DIR) $(FULL_TARGET).tex
