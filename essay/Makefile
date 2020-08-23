# Renders final PDF output file


LATEX_FORM_FILE=latex_formatter.yaml

.PHONY: format pdf

FILES=`cat toctree.txt`

pdf:
	pandoc                        \
	  --from         markdown     \
	  --to           latex        \
	  --template     template.tex \
	  --out          report.pdf   \
	  --pdf-engine   xelatex      \
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

