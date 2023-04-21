
BIN     = xz2017

CC      = cc -fast
CFLAGS  = 
EXTRA_CFLAGS = -I src -I src/spec_mem_io -I src/sha-2 -I src/common -I src/liblzma/api \
               -I src/liblzma/lzma  -I src/liblzma/common -I src/liblzma/check \
               -I src/liblzma/simple -I src/liblzma/delta  -I src/liblzma/lz -I src/liblzma/rangecoder \
               -DSPEC -DNDEBUG -DSPEC_XZ -DHAVE_CONFIG_H=1 -DSPEC_MEM_IO -DSPEC_AUTO_BYTEORDER=0x12345678
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP
LIBS = -static

# Intel
# CFLAGS = -std=c99

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES = \
    src/spec.c \
    src/spec_xz.c \
    src/pxz.c \
    src/common/tuklib_physmem.c \
    src/liblzma/common/common.c \
    src/liblzma/common/block_util.c \
    src/liblzma/common/easy_preset.c \
    src/liblzma/common/filter_common.c \
    src/liblzma/common/hardware_physmem.c \
    src/liblzma/common/index.c \
    src/liblzma/common/stream_flags_common.c \
    src/liblzma/common/vli_size.c \
    src/liblzma/common/alone_encoder.c \
    src/liblzma/common/block_buffer_encoder.c \
    src/liblzma/common/block_encoder.c \
    src/liblzma/common/block_header_encoder.c \
    src/liblzma/common/easy_buffer_encoder.c \
    src/liblzma/common/easy_encoder.c \
    src/liblzma/common/easy_encoder_memusage.c \
    src/liblzma/common/filter_buffer_encoder.c \
    src/liblzma/common/filter_encoder.c \
    src/liblzma/common/filter_flags_encoder.c \
    src/liblzma/common/index_encoder.c \
    src/liblzma/common/stream_buffer_encoder.c \
    src/liblzma/common/stream_encoder.c \
    src/liblzma/common/stream_flags_encoder.c \
    src/liblzma/common/vli_encoder.c \
    src/liblzma/common/alone_decoder.c \
    src/liblzma/common/auto_decoder.c \
    src/liblzma/common/block_buffer_decoder.c \
    src/liblzma/common/block_decoder.c \
    src/liblzma/common/block_header_decoder.c \
    src/liblzma/common/easy_decoder_memusage.c \
    src/liblzma/common/filter_buffer_decoder.c \
    src/liblzma/common/filter_decoder.c \
    src/liblzma/common/filter_flags_decoder.c \
    src/liblzma/common/index_decoder.c \
    src/liblzma/common/index_hash.c \
    src/liblzma/common/stream_buffer_decoder.c \
    src/liblzma/common/stream_decoder.c \
    src/liblzma/common/stream_flags_decoder.c \
    src/liblzma/common/vli_decoder.c \
    src/liblzma/check/check.c \
    src/liblzma/check/crc32_table.c \
    src/liblzma/check/crc32_fast.c \
    src/liblzma/check/crc64_table.c \
    src/liblzma/check/crc64_fast.c \
    src/liblzma/check/sha256.c \
    src/liblzma/lz/lz_encoder.c \
    src/liblzma/lz/lz_encoder_mf.c \
    src/liblzma/lz/lz_decoder.c \
    src/liblzma/lzma/lzma_encoder.c \
    src/liblzma/lzma/lzma_encoder_presets.c \
    src/liblzma/lzma/lzma_encoder_optimum_fast.c \
    src/liblzma/lzma/lzma_encoder_optimum_normal.c \
    src/liblzma/lzma/fastpos_table.c \
    src/liblzma/lzma/lzma_decoder.c \
    src/liblzma/lzma/lzma2_encoder.c \
    src/liblzma/lzma/lzma2_decoder.c \
    src/liblzma/rangecoder/price_table.c \
    src/liblzma/delta/delta_common.c \
    src/liblzma/delta/delta_encoder.c \
    src/liblzma/delta/delta_decoder.c \
    src/liblzma/simple/simple_coder.c \
    src/liblzma/simple/simple_encoder.c \
    src/liblzma/simple/simple_decoder.c \
    src/liblzma/simple/x86.c \
    src/liblzma/simple/powerpc.c \
    src/liblzma/simple/ia64.c \
    src/liblzma/simple/arm.c \
    src/liblzma/simple/armthumb.c \
    src/liblzma/simple/sparc.c \
    src/xz/args.c \
    src/xz/coder.c \
    src/xz/file_io.c \
    src/xz/hardware.c \
    src/xz/list.c \
    src/xz/main.c \
    src/xz/message.c \
    src/xz/options.c \
    src/xz/signals.c \
    src/xz/util.c \
    src/common/tuklib_open_stdxxx.c \
    src/common/tuklib_progname.c \
    src/common/tuklib_exit.c \
    src/common/tuklib_cpucores.c \
    src/common/tuklib_mbstr_width.c \
    src/common/tuklib_mbstr_fw.c \
    src/spec_mem_io/spec_mem_io.c \
    src/sha-2/sha512.c

OBJ     = $(SOURCES:.c=.o)

#VPATH   = src

ifeq ($(MAKECMDGOALS),xz2017_omp)
BIN       = xz2017_omp
OMP_FLAGS = -DSPEC_OPENMP
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
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp *.xz xz.err
