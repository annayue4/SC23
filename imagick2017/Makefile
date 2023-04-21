
BIN          = imagick2017
BIN_CONVERT  = convert
BIN_VALIDATE = imagevalidate

CC      = cc -Ofast

# CCE   Use -D__ICC to avoid undefined __builtin_assume_aligned.
# Intel needs -std=c99
# GNU   may need -std=c99
CFLAGS	=  -D__ICC 
EXTRA_CFLAGS = -I./src -DSPEC -DSPEC_CPU -DNDEBUG
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP
LIBS = -static

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES = \
        src/coders/tga.c \
        src/filters/analyze.c \
        src/magick/accelerate.c \
        src/magick/animate.c \
        src/magick/annotate.c \
        src/magick/artifact.c \
        src/magick/attribute.c \
        src/magick/blob.c \
        src/magick/cache-view.c \
        src/magick/cache.c \
        src/magick/channel.c \
        src/magick/cipher.c \
        src/magick/client.c \
        src/magick/coder.c \
        src/magick/color.c \
        src/magick/colormap.c \
        src/magick/colorspace.c \
        src/magick/compare.c \
        src/magick/composite.c \
        src/magick/compress.c \
        src/magick/configure.c \
        src/magick/constitute.c \
        src/magick/decorate.c \
        src/magick/delegate.c \
        src/magick/display.c \
        src/magick/distort.c \
        src/magick/distribute-cache.c \
        src/magick/draw.c \
        src/magick/effect.c \
        src/magick/enhance.c \
        src/magick/exception.c \
        src/magick/feature.c \
        src/magick/fourier.c \
        src/magick/fx.c \
        src/magick/gem.c \
        src/magick/geometry.c \
        src/magick/hashmap.c \
        src/magick/histogram.c \
        src/magick/identify.c \
        src/magick/image.c \
        src/magick/layer.c \
        src/magick/list.c \
        src/magick/locale.c \
        src/magick/log.c \
        src/magick/magic.c \
        src/magick/magick.c \
        src/magick/matrix.c \
        src/magick/memory.c \
        src/magick/mime.c \
        src/magick/module.c \
        src/magick/monitor.c \
        src/magick/montage.c \
        src/magick/morphology.c \
        src/magick/option.c \
        src/magick/paint.c \
        src/magick/pixel.c \
        src/magick/policy.c \
        src/magick/prepress.c \
        src/magick/profile.c \
        src/magick/property.c \
        src/magick/quantize.c \
        src/magick/quantum-export.c \
        src/magick/quantum-import.c \
        src/magick/quantum.c \
        src/magick/random.c \
        src/magick/registry.c \
        src/magick/resample.c \
        src/magick/resize.c \
        src/magick/resource.c \
        src/magick/segment.c \
        src/magick/semaphore.c \
        src/magick/shear.c \
        src/magick/signature.c \
        src/magick/splay-tree.c \
        src/magick/static.c \
        src/magick/statistic.c \
        src/magick/stream.c \
        src/magick/string.c \
        src/magick/threshold.c \
        src/magick/timer.c \
        src/magick/token.c \
        src/magick/transform.c \
        src/magick/type.c \
        src/magick/utility.c \
        src/magick/version.c \
        src/magick/xml-tree.c \
        src/utilities/convert.c \
        src/wand/convert.c \
        src/wand/drawing-wand.c \
        src/wand/magick-image.c \
        src/wand/magick-wand.c \
        src/wand/mogrify.c \
        src/wand/pixel-wand.c \
        src/wand/magick-property.c \
        src/wand/pixel-iterator.c \
        src/wand/wand.c \
        src/magick/deprecate.c


SOURCES_VALIDATE = src/image_validator/ImageValidator.c

OBJ          = $(SOURCES:.c=.o)
OBJ_VALIDATE = $(SOURCES_VALIDATE:.c=.o)

VPATH   = src

ifeq ($(MAKECMDGOALS),imagick2017_omp)
BIN       = imagick2017_omp
OMP_FLAGS = -DSPEC_OPENMP
endif

# Executable is x$(BIN), execution script copied to $BIN.
$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ) $(BIN_VALIDATE) $(BIN_CONVERT)
	$(CC) $(CFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

$(BIN_CONVERT): 
	rm -f convert
	ln -s x$(BIN) convert

$(BIN_VALIDATE): $(OBJ_VALIDATE)
	$(CC) $(CFLAGS) -o $(BIN_VALIDATE) $(OBJ_VALIDATE) $(LDFLAGS) $(LIBS)

.c.o:
	$(CC) -c -o $@ $(EXTRA_CFLAGS) $(OMP_FLAGS) $(CFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) $(OBJ_VALIDATE) 

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp $(BIN_CONVERT) $(BIN_VALIDATE)
	-rm -f *_input.tga *_output.tga validate.out validate.err

