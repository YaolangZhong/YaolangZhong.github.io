# CV build — edit main.tex, then run `make` to rebuild the PDF and
# sync it to ../assets/cv.pdf (the file the website links to).

main.pdf: main.tex
	latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
	cp main.pdf ../assets/cv.pdf
	$(MAKE) clean

.PHONY: clean
clean:
	latexmk -c
	rm -f main.aux main.fdb_latexmk main.fls main.log main.out
