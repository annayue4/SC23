
BIN     = perlbench2017

CFLAGS	= -fast -DSPEC_LINUX_X64 -fno-strict-aliasing
EXTRA_CFLAGS = -I ./src -I ./src/dist/IO -I ./src/cpan/Time-HiRes \
               -I ./src/cpan/HTML-Parser -I ./src/ext/re -I ./src/specrand \
               -DSPEC -DNDEBUG -DPERL_CORE -DDOUBLE_SLASHES_SPECIAL=0 -D_LARGE_FILES \
               -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64 -DSPEC_LP64 
LIBS = -lm -static

# -DSPEC_LINUX_X64
# -DSPEC_LINUX_AARCH64

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES  =  src/av.c src/caretx.c src/deb.c src/doio.c src/doop.c src/dump.c \
            src/globals.c src/gv.c src/hv.c src/keywords.c src/locale.c \
            src/mg.c src/numeric.c src/op.c src/pad.c src/perl.c \
            src/perlapi.c src/perlio.c src/perlmain.c \
            src/perly.c src/pp.c src/pp_ctl.c src/pp_hot.c \
            src/pp_pack.c src/pp_sort.c src/pp_sys.c \
            src/regcomp.c src/regexec.c src/run.c \
            src/scope.c src/sv.c src/taint.c src/toke.c \
            src/universal.c src/utf8.c src/util.c src/reentr.c src/mro_core.c src/mathoms.c \
            src/specrand/specrand.c \
            src/dist/PathTools/Cwd.c \
            src/dist/Data-Dumper/Dumper.c \
            src/ext/Devel-Peek/Peek.c \
            src/cpan/Digest-MD5/MD5.c \
            src/cpan/Digest-SHA/SHA.c \
            src/DynaLoader.c \
            src/dist/IO/IO.c \
            src/dist/IO/poll.c \
            src/cpan/MIME-Base64/Base64.c \
            src/Opcode.c \
            src/dist/Storable/Storable.c \
            src/ext/Sys-Hostname/Hostname.c \
            src/cpan/Time-HiRes/HiRes.c \
            src/ext/XS-Typemap/stdio.c \
            src/ext/attributes/attributes.c \
            src/cpan/HTML-Parser/Parser.c \
            src/ext/mro/mro.c \
            src/ext/re/re.c \
            src/ext/re/re_comp.c \
            src/ext/re/re_exec.c \
            src/ext/arybase/arybase.c \
            src/ext/PerlIO-scalar/scalar.c \
            src/ext/PerlIO-via/via.c \
            src/ext/File-Glob/bsd_glob.c \
            src/ext/File-Glob/Glob.c \
            src/ext/Hash-Util/Util.c \
            src/ext/Hash-Util-FieldHash/FieldHash.c \
            src/ext/Tie-Hash-NamedCapture/NamedCapture.c \
            src/cpan/Scalar-List-Utils/ListUtil.c 
OBJ     = $(SOURCES:.c=.o)

#VPATH	= src

ifeq ($(MAKECMDGOALS),perlbench2017_speed)
BIN       = perlbench2017_speed
endif


$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ) 
	$(CC) $(CFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.c.o:
	$(CC) -c -o $@ $(EXTRA_CFLAGS) $(OMP_FLAGS) $(CFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ)

clobber: clean
	-rm -f $(BIN) x$(BIN)
	-rm -f *.out *.err *.pm *.pl *.in *.rc regen WORDS dictionary lib rules validate
	-rm -rf t

