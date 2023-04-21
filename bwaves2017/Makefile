
BIN     = bwaves2017

FC      = ftn -Ofast
FFLAGS	= 
EXTRA_FFLAGS = -DSPEC -DNDEBUG
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES = block_solver.F flow_lam.F flux_lam.F \
          jacobian_lam.F shell_lam.F fill1.F fill2.F

OBJ     = $(SOURCES:.F=.o)

VPATH	= src

ifeq ($(MAKECMDGOALS),bwaves2017_omp)
BIN       = bwaves2017_omp
OMP_FLAGS = -DSPEC_OPENMP
endif

$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(FC) $(FFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.F.o:
	$(FC) -c $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

.f.o:
	$(FC) -c $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ)

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp
	-rm -f bwaves_*.out *_dqnrm.log *_resid.log
