
BIN     = fotonik3d2017

FC      = ftn -Ofast #-O3 -hfp3
FFLAGS	= 
EXTRA_FFLAGS = -I src -DSPEC -DNDEBUG
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP
LIBS = -static

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES = \
    parameter.f90 \
    globalvar.F90 \
    readline.f90 \
    power.F90 \
    calcflops.F90 \
    communicate.F90 \
    huygens.F90 \
    update.F90 \
    material.F90 \
    mur.F90 \
    PlaneSource.F90 \
    PEC.F90 \
    init.F90 \
    leapfrog.F90 \
    timerRoutine.f90 \
    UPML.F90 \
    yeemain.F90 \
    writeout.F90 \
    MPI_dummy.F90

TMPOBJ  = $(SOURCES:.F90=.o)
OBJ     = $(TMPOBJ:.f90=.o)

VPATH	= src
.SUFFIXES: .F90 .f90

ifeq ($(MAKECMDGOALS),fotonik3d2017_omp)
BIN       = fotonik3d2017_omp
OMP_FLAGS = -DSPEC_OPENMP
endif

$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(FC) $(FFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.F90.o:
	$(FC) -c $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

.f90.o:
	$(FC) -c $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) *.mod

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp
	-rm -f *.dat *.def pscyee.out TEwaveguide.m fotonik3d.out


calcflops.o: \
    globalvar.o \
    power.o \
    PlaneSource.o \
    parameter.o \

communicate.o: \
    globalvar.o \
    parameter.o \

globalvar.o: \
    parameter.o \

huygens.o: \
    globalvar.o \
    parameter.o \

init.o: \
    globalvar.o \
    huygens.o \
    update.o \
    mur.o \
    PlaneSource.o \
    PEC.o \
    power.o \
    material.o \
    UPML.o \
    communicate.o \

leapfrog.o: \
    parameter.o \
    globalvar.o \
    huygens.o \
    update.o \
    mur.o \
    PEC.o \
    PlaneSource.o \
    power.o \
    material.o \
    UPML.o \
    communicate.o \

material.o: \
    globalvar.o \
    parameter.o \
    readline.o \

mur.o: \
    globalvar.o \
    material.o \
    parameter.o \

PEC.o: \
    globalvar.o \
    parameter.o \

PlaneSource.o: \
    globalvar.o \
    parameter.o \
    readline.o \

power.o: \
    globalvar.o \
    parameter.o \

update.o: \
    globalvar.o \
    parameter.o \

UPML.o: \
    globalvar.o \
    material.o \
    parameter.o \

yeemain.o: \
    mur.o \
    PEC.o \
    PlaneSource.o \
    power.o \
    communicate.o \
    globalvar.o \
    UPML.o \

writeout.o: \
    globalvar.o \
    parameter.o \

MPI_dummy.o: \
    parameter.o \

