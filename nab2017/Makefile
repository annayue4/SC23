
BIN     = nab2017

CC      = cc -Ofast
CFLAGS	= 
EXTRA_CFLAGS = -I src/specrand -I src/regex-alpha \
               -DSPEC -DNDEBUG -DNOREDUCE -DNOPERFLIB
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP
LIBS = -static

# rate SPEC_SUPPRESS_OPENMP
# speed SPEC_OPENMP

SOURCES = nabmd.c sff.c nblist.c prm.c memutil.c molio.c molutil.c errormsg.c \
          binpos.c rand2.c select_atoms.c reslib.c database.c \
          traceback.c chirvol.c specrand.c regcomp.c regerror.c regexec.c regfree.c

OBJ     = $(SOURCES:.c=.o)

VPATH	= src:src/regex-alpha:src/specrand

ifeq ($(MAKECMDGOALS),nab2017_omp)
BIN       = nab2017_omp
OMP_FLAGS = -DSPEC_OPENMP
endif

# Executable is x$(BIN), execution script copied to $BIN.
$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(CC) $(CFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.c.o:
	$(CC) -c $(EXTRA_CFLAGS) $(OMP_FLAGS) $(CFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ)

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp
	-rm -f hkrdenq aminos gcn4dna 1am0 3j1n


nabmd.o: nabcode.h
nblist.o: defreal.h
sff.o: nab.h defreal.h nabtypes.h memutil.h eff.c intersect.c gbsa.c debug.h
prm.o: nab.h defreal.h nabtypes.h errormsg.h
memutil.o: nab.h defreal.h nabtypes.h
molio.o: nab.h defreal.h nabtypes.h
molutil.o: nab.h defreal.h nabtypes.h errormsg.h memutil.h
errormsg.o: errormsg.h
binpos.o: memutil.h
rand2.o: defreal.h
select_atoms.o: nab.h defreal.h nabtypes.h
reslib.o: nab.h defreal.h nabtypes.h errormsg.h memutil.h chirvol.h database.h
database.o: database.h
traceback.o: errormsg.h
chirvol.o: nab.h defreal.h nabtypes.h
