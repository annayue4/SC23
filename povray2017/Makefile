
BIN          = povray2017
BIN_VALIDATE = imagevalidate

CXX     = CC -Ofast
CC      = cc -Ofast

CFLAGS	 = -static
CXXFLAGS = -static
EXTRA_CFLAGS   = -I src -I src/frontend -I src/base -I src/spec_qsort -DSPEC -DNDEBUG -DSPEC_LP64
EXTRA_CXXFLAGS = $(EXTRA_CFLAGS)
#Intel
#CFLAGS = -std=c99
#LDFLAGS = -lm -lsci

SOURCES = atmosph.cpp bbox.cpp bcyl.cpp benchmark.cpp bezier.cpp blob.cpp \
          boxes.cpp bsphere.cpp camera.cpp chi2.cpp colour.cpp colutils.cpp \
          cones.cpp csg.cpp discs.cpp express.cpp fncode.cpp fnintern.cpp \
          fnpovfpu.cpp fnsyntax.cpp fpmetric.cpp fractal.cpp function.cpp \
          hcmplx.cpp hfield.cpp histogra.cpp iff.cpp image.cpp interior.cpp \
          isosurf.cpp lathe.cpp lbuffer.cpp lightgrp.cpp lighting.cpp \
          mathutil.cpp matrices.cpp media.cpp mesh.cpp normal.cpp objects.cpp \
          octree.cpp optout.cpp parse.cpp parsestr.cpp parstxtr.cpp pattern.cpp \
          pgm.cpp photons.cpp pigment.cpp planes.cpp point.cpp poly.cpp polygon.cpp \
          polysolv.cpp povmsend.cpp povmsrec.cpp povray.cpp pov_mem.cpp pov_util.cpp \
          ppm.cpp prism.cpp quadrics.cpp quatern.cpp radiosit.cpp rad_data.cpp \
          ray.cpp rendctrl.cpp render.cpp renderio.cpp reswords.cpp sor.cpp \
          spheres.cpp sphsweep.cpp splines.cpp statspov.cpp super.cpp targa.cpp \
          texture.cpp tokenize.cpp torus.cpp triangle.cpp truetype.cpp txttest.cpp \
          userdisp.cpp userio.cpp vbuffer.cpp vlbuffer.cpp warps.cpp \
          fileinputoutput.cpp \
          povms.cpp \
          povmscpp.cpp \
          processoptions.cpp \
          stringutilities.cpp \
          textstream.cpp \
          textstreambuffer.cpp \
          defaultplatformbase.cpp \
          defaultrenderfrontend.cpp \
          messageoutput.cpp \
          processrenderoptions.cpp \
          renderfrontend.cpp \
          spec_qsort.c

SOURCES_VALIDATE = ImageValidator.c

TMPOBJ  = $(SOURCES:.cpp=.o)
OBJ     = $(TMPOBJ:.c=.o)

OBJ_VALIDATE = $(SOURCES_VALIDATE:.c=.o)

VPATH	= src:src/base:src/frontend:src/spec_qsort:src/image_validator
.SUFFIXES: .cpp

$(BIN):	x$(BIN) $(BIN).execute.script $(BIN_VALIDATE)
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o x$(BIN) $(OBJ) $(LIBS)

$(BIN_VALIDATE): $(OBJ_VALIDATE)
	$(CC) $(CFLAGS)  -o $(BIN_VALIDATE) $(OBJ_VALIDATE) $(LDFLAGS) $(LIBS)

.cpp.o:
	$(CXX) -c $(EXTRA_CXXFLAGS) $(CXXFLAGS) $<

.c.o:
	$(CC) -c $(EXTRA_CFLAGS) $(CFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) $(OBJ_VALIDATE) *.ti

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN_VALIDATE)  SPEC-benchmark.log SPEC-benchmark.tga SPEC-benchmark-*.pov
	-rm -f povray.out imagevalidate.out imagevalidate.err
