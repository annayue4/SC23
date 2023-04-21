
BIN     = leela2017

CXX     = CC -fast

CXXFLAGS       = 
EXTRA_CXXFLAGS = -I src -DSPEC -DNDEBUG
LIBS = -static

# rate  -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP


SOURCES = \
    FullBoard.cpp \
    KoState.cpp \
    Playout.cpp \
    TimeControl.cpp \
    UCTSearch.cpp \
    GameState.cpp \
    Leela.cpp \
    SGFParser.cpp \
    Timing.cpp \
    Utils.cpp \
    FastBoard.cpp \
    Matcher.cpp \
    SGFTree.cpp \
    TTable.cpp \
    Zobrist.cpp \
    FastState.cpp \
    GTP.cpp \
    MCOTable.cpp \
    Random.cpp \
    SMP.cpp \
    UCTNode.cpp

TMPOBJ  = $(SOURCES:.cpp=.o)
OBJ     = $(TMPOBJ:.c=.o)


VPATH	= src
.SUFFIXES: .cpp

$(BIN):	x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(CXX) $(CXXFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.cpp.o:
	$(CXX) -c $(EXTRA_CXXFLAGS) $(CXXFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) 

clobber: clean
	-rm -f $(BIN) x$(BIN)
