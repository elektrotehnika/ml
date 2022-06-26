.dz-old:
	latex dz${NUM}.tex
	latex dz${NUM}.tex
	dvips -t letter -G0 -Ppdf -o dz${NUM}.ps dz${NUM}.dvi
	ps2pdf dz${NUM}.ps
	rm dz${NUM}.ps
	open dz${NUM}.pdf

.dz-sol:
	pdflatex -jobname=dz${NUM}-sol "\def\solutions{1} \input{dz${NUM}}"
	pdflatex -jobname=dz${NUM}-sol "\def\solutions{1} \input{dz${NUM}}"

.dz:
	pdflatex -jobname=dz${NUM} "\def\solutions{0} \input{dz${NUM}}"
	pdflatex -jobname=dz${NUM} "\def\solutions{0} \input{dz${NUM}}"

all:
	if [ -f dz1.tex ] ; then NUM=1 make .dz-sol ; fi
	if [ -f dz2.tex ] ; then NUM=2 make .dz-sol ; fi
	if [ -f dz3.tex ] ; then NUM=3 make .dz-sol ; fi
	if [ -f dz4.tex ] ; then NUM=4 make .dz-sol ; fi

dz1:
	NUM=1 make .dz .dz-sol

dz2:
	NUM=2 make .dz .dz-sol

dz3:
	NUM=3 make .dz .dz-sol

dz4:
	NUM=4 make .dz .dz-sol
