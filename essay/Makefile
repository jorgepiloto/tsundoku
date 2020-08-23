# Renders final PDF output file

.PHONY: pdf

FILES=`cat index.txt`

pdf:
	pandoc                        \
	  --from         markdown     \
	  --to           latex        \
	  --template     template.tex \
	  --out          report.pdf   \
	  --pdf-engine   xelatex      \
	  $(FILES)
