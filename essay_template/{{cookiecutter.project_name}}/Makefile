# Renders final PDF output file
# -----------------------------

# Important file names
OUT_FILE = {{cookiecutter.output_filename}}
TEX_FILE = template.tex
BIB_FILE = biblio.bib
HIGHLIGHT_FILE = highlight.theme

# Main project directories
SRC_DIR = src
TEX_DIR = tex
FIG_DIR = fig
STY_DIR = sty
BIB_DIR = bib
OUT_DIR = out

.PHONY: format pdf

FILES=`cat toctree.txt`

pdf:
	@mkdir -p $(OUT_DIR)
	pandoc                        				\
	  --from         markdown     				\
	  --to           latex        				\
	  --out          $(OUT_DIR)/$(OUT_FILE) 		\
	  --template     $(TEX_DIR)/$(TEX_FILE) 		\
	  --pdf-engine   xelatex      				\
	  --resource-path=.:$(FIG_DIR)				\
	  --highlight-style $(STY_DIR)/$(HIGHLIGHT_FILE)	\
	  --bibliography $(BIB_DIR)/$(BIB_FILE) 		\
	  $(FILES)

format:
	@echo "Formatting files..."
	latexindent cover.tex -s -o cover.tex -y="defaultIndent: '  '"
	@echo "Deleting log file..."
	rm -f indent.log
	@echo "Done!"

clean:
	@echo "Cleaning output files..."
	rm -rf $(OUT_DIR)
	@echo "Done!"

