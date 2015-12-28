SRCS=$(wildcard *.tex)

INDEX=idx
SRC=rapport
OUTEXT=pdf

TMP=*.aux *.log *.dvi *.toc *.bbl *.blg *.out *~

COMPIL=pdflatex
BIB=bibtex
IDX=makeindex
OPTIDX=-s index.ist
PRES=presentation


all : $(SRC) ; make clean

clean :
	rm -f $(TMP); cd Chapitres ; rm -f $(TMP)
       
$(SRC) : $(SRCS)
	$(BIB) $(SRC) ; $(COMPIL) $(SRC).tex ; $(IDX) $(OPTIDX) $(SRC).$(INDEX) ; $(BIB) $(SRC) ; $(COMPIL) $(SRC).tex ; $(COMPIL) $(SRC).tex

$(PRES) : $(SRCS)
	$(COMPIL) $(PRES).tex ; $(COMPIL) $(PRES).tex

