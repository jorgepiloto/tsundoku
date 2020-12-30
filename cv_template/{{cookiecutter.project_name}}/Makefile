# Renders final PDF output file


LATEX_FORM_FILE=latex_formatter.yaml
OUT_DIR=out

.PHONY: format pdf

FILES=`cat toctree.txt`

pdf:
	@mkdir -p $(OUT_DIR)
	pandoc                        		\
	  --from         markdown     		\
	  --to           latex        		\
	  --out          $(OUT_DIR)/cv.pdf 	\
	  --template     tex/cv_template.tex 	\
	  --pdf-engine   xelatex      		\
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

