
BIN     = exchange2_2017

FC      = ftn -Ofast #-O3 -hfp3
FFLAGS	= 
EXTRA_FFLAGS = -DSPEC -DNDEBUG
LIBS = -static

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES = exchange2.F90

OBJ     = $(SOURCES:.F90=.o)
.SUFFIXES: .F90

VPATH	= src

$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(FC) $(FFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.F90.o:
	$(FC) -c $(EXTRA_FFLAGS) $(FFLAGS) $<

.F.o:
	$(FC) -c $(EXTRA_FFLAGS) $(FFLAGS) $<

.f.o:
	$(FC) -c $(EXTRA_FFLAGS) $(FFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) *.mod

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN) s.txt puzzles.txt
