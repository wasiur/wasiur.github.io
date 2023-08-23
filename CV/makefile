.PHONY: all

all:		CV_KhudaBukhsh.pdf 

CV_KhudaBukhsh.pdf:	CV_KhudaBukhsh.tex force
	lualatex $<
	bibtex CV_KhudaBukhsh1.aux
	bibtex CV_KhudaBukhsh2.aux
	bibtex CV_KhudaBukhsh3.aux
	bibtex CV_KhudaBukhsh4.aux
	bibtex CV_KhudaBukhsh5.aux
	lualatex $<
	lualatex $<
	lualatex $<
	open CV_KhudaBukhsh.pdf

ListOfPublications.pdf:	ListOfPublications.tex force
	lualatex $<
	bibtex ListOfPublications1.aux
	bibtex ListOfPublications2.aux
	bibtex ListOfPublications3.aux
	bibtex ListOfPublications4.aux
	bibtex ListOfPublications5.aux
	lualatex $<
	lualatex $<
	lualatex $<
	open ListOfPublications.pdf

force:		;

.PHONY: clean

clean:
			latexmk -c
			rm -f *.auxlock *.snm *.nav *.out *.fdb_latexmk *.vrb *.table *.gnuplot *-blx.bib *.mtc* *.maf *.run.xml *.bbl


.PHONY: tikzclean

tikzclean:	clean
			rm -f externalized/*.pdf externalized/*.dpth externalized/*.log	externalized/*.idx externalized/*.run.xml externalized/*.dep externalized/*.md5 externalized/*.gnuplot externalized/*.table

.PHONY: nup

nup: main.pdf
		 pdfnup main.pdf

.PHONY: count 
count:
	texcount main.tex -inc -total
