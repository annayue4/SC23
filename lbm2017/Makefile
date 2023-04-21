
BIN     = lbm2017

CC      = cc -Ofast
CFLAGS  = 
EXTRA_CFLAGS = -DSPEC -DNDEBUG
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP -DLARGE_WORKLOAD

SOURCES = lbm.c main.c

OBJ     = $(SOURCES:.c=.o)

VPATH   = src

ifeq ($(MAKECMDGOALS),lbm2017_omp)
BIN       = lbm2017_omp
OMP_FLAGS = -DSPEC_OPENMP -DLARGE_WORKLOAD
endif


$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ) $(SOURCES)
	$(CC) $(CFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LDFLAGS) $(LIBS)

.c.o:
	$(CC) -c $(EXTRA_CFLAGS) $(OMP_FLAGS) $(CFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ)

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp *.of
