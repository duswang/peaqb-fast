# $Id: Makefile.in,v 1.0 2003/05/21 19:01:10 oveRet Exp $

MISSING  = 
MISSLIBS =  ../fftw/.libs
CC       = cc
DEFINE = -DBASIC -DLITTLE
INCLUDE = -I/usr/local/include -I./include -I./missing/include -I../fftw
OPT = -O3 -Wall
LIB = -L./lib -L$(MISSLIBS)

all: 	wavedump getframe earmodelfft critbandgroup spreading \
	timespreading threshold levpatadapt modulation loudness \
	moddiff noiseloudness bandwidth nmr reldistframes boundary \
	detprob harmstruct energyth neural peaqb

wavedump: wavedump.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c wavedump.c 

getframe: getframe.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c getframe.c

earmodelfft: earmodelfft.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c earmodelfft.c

critbandgroup: critbandgroup.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c critbandgroup.c

spreading: spreading.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c spreading.c

timespreading: timespreading.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c timespreading.c

threshold: threshold.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c threshold.c

levpatadapt: levpatadapt.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c levpatadapt.c

modulation: modulation.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c modulation.c

loudness: loudness.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c loudness.c

moddiff: moddiff.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c moddiff.c

noiseloudness: noiseloudness.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c noiseloudness.c

bandwidth: bandwidth.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c bandwidth.c

nmr: nmr.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c nmr.c

reldistframes: reldistframes.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c reldistframes.c

boundary: boundary.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c boundary.c

detprob: detprob.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c detprob.c

harmstruct: harmstruct.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c harmstruct.c

energyth: energyth.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c energyth.c

neural: neural.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c neural.c

peaqb: peaqb.c
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -c peaqb.c $(MISSING)
	$(CC) $(OPT) $(DEFINE) $(INCLUDE) -o peaqb peaqb.o \
	wavedump.o getframe.o earmodelfft.o critbandgroup.o spreading.o \
	timespreading.o threshold.o levpatadapt.o modulation.o loudness.o \
	moddiff.o noiseloudness.o bandwidth.o reldistframes.o nmr.o boundary.o \
	detprob.o harmstruct.o energyth.o neural.o $(LIB) -lfftw -lm

install:
	rm -f /usr/local/bin/peaqb
	cp -f peaqb /usr/local/bin
clean:
	rm -f peaqb core *.o
