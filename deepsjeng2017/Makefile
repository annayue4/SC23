
BIN     = deepsjeng2017

CXX     = CC -Ofast
CXXFLAGS       = -DSMALL_MEMORY
EXTRA_CXXFLAGS = -DSPEC -DNDEBUG -DBIG_MEMORY
LIBS = -static

# If both SMALL_MEMORY and BIG_MEMORY are specified, SMALL memory will take precedence.
# refrate  -DSMALL_MEMORY
# refspeed -DBIG_MEMORY

SOURCES = \
    attacks.cpp bitboard.cpp bits.cpp board.cpp draw.cpp endgame.cpp epd.cpp \
    generate.cpp initp.cpp make.cpp moves.cpp neval.cpp pawn.cpp preproc.cpp \
    search.cpp see.cpp sjeng.cpp state.cpp ttable.cpp utils.cpp 

OBJ     = $(SOURCES:.cpp=.o)

VPATH	= src
.SUFFIXES: .cpp

$(BIN): x$(BIN) $(BIN).execute.script
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
