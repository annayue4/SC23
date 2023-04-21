
BIN     = mcf2017

CC      = cc -fast
CFLAGS	= -fno-strict-aliasing 
EXTRA_CFLAGS = -I src/spec_qsort -DSPEC -DNDEBUG
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP
LIBS = -static

# rate  -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES = mcf.c mcfutil.c readmin.c implicit.c pstart.c output.c \
	  treeup.c pbla.c pflowup.c psimplex.c pbeampp.c spec_qsort.c

OBJ     = $(SOURCES:.c=.o)

VPATH	= src:src/spec_qsort

$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN):	$(OBJ)
	$(CC) $(CFLAGS) $(LDFLAGS) -o x$(BIN) $(OBJ) $(LIBS)

.c.o:
	$(CC) -c $(EXTRA_CFLAGS) $(OMP_FLAGS) $(CFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ)

clobber: clean
	-rm -f $(BIN) x$(BIN) mcf.out
