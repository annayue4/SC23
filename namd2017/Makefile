
BIN     = namd2017

CXX     = CC -Ofast
CXXFLAGS     = 
EXTRA_CXXFLAGS = -I src -DSPEC -DNDEBUG -DNAMD_DISABLE_SSE

# rate  -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES = Compute.C ComputeList.C ComputeNonbondedFEP.C \
          ComputeNonbondedLES.C ComputeNonbondedPProf.C \
          ComputeNonbondedStd.C ComputeNonbondedUtil.C \
          LJTable.C Molecule.C Patch.C PatchList.C ResultSet.C \
          SimParameters.C erf.C spec_namd.C

OBJ     = $(SOURCES:.C=.o)

VPATH	= src

$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(CXX) $(CXXFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.C.o:
	$(CXX) -c $(EXTRA_CXXFLAGS) $(CXXFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ)
	-rm -f *.ti

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN).out
