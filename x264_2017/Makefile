
BIN          = x264_2017
BIN_DECODE   = ldecod
BIN_VALIDATE = imagevalidate


CC      = cc -fast
CFLAGS	= -z muldefs   
# Order of includes is important because of some duplidate .h files.
EXTRA_CFLAGS = -I src/ldecod_src/inc -I src/x264_src -I src/x264_src/extras -I src/x264_src/common \
               -DSPEC -DNDEBUG -DSPEC_AUTO_BYTEORDER=0x12345678
LIBS = -static

# Intel
# CFLAGS = -std=c99

# rate  -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

# x264
SOURCES = \
        src/x264_src/common/mc.c\
        src/x264_src/common/predict.c\
        src/x264_src/common/pixel.c\
        src/x264_src/common/macroblock.c\
        src/x264_src/common/frame.c\
        src/x264_src/common/dct.c\
        src/x264_src/common/cpu.c\
        src/x264_src/common/cabac.c\
        src/x264_src/common/common.c\
        src/x264_src/common/mdate.c\
        src/x264_src/common/rectangle.c\
        src/x264_src/common/set.c\
        src/x264_src/common/quant.c\
        src/x264_src/common/deblock.c\
        src/x264_src/common/vlc.c\
        src/x264_src/common/mvpred.c\
        src/x264_src/encoder/analyse.c\
        src/x264_src/encoder/me.c\
        src/x264_src/encoder/ratecontrol.c\
        src/x264_src/encoder/set.c\
        src/x264_src/encoder/macroblock.c\
        src/x264_src/encoder/cabac.c\
        src/x264_src/encoder/cavlc.c\
        src/x264_src/encoder/encoder.c\
        src/x264_src/encoder/lookahead.c\
        src/x264_src/input/timecode.c\
        src/x264_src/input/yuv.c\
        src/x264_src/input/y4m.c\
        src/x264_src/output/raw.c\
        src/x264_src/output/matroska.c\
        src/x264_src/output/matroska_ebml.c\
        src/x264_src/output/flv.c\
        src/x264_src/output/flv_bytestream.c\
        src/x264_src/input/thread.c\
        src/x264_src/x264.c\
        src/x264_src/extras/getopt.c

#ldecod
SOURCES_DECODE =\
        src/ldecod_src/nal.c\
        src/ldecod_src/mbuffer_mvc.c\
        src/ldecod_src/image.c\
        src/ldecod_src/mb_access.c\
        src/ldecod_src/memalloc.c\
        src/ldecod_src/mc_prediction.c\
        src/ldecod_src/mb_prediction.c\
        src/ldecod_src/intra4x4_pred_mbaff.c\
        src/ldecod_src/loop_filter_mbaff.c\
        src/ldecod_src/context_ini.c\
        src/ldecod_src/configfile.c\
        src/ldecod_src/cabac.c\
        src/ldecod_src/sei.c\
        src/ldecod_src/leaky_bucket.c\
        src/ldecod_src/filehandle.c\
        src/ldecod_src/errorconcealment.c\
        src/ldecod_src/decoder_test.c\
        src/ldecod_src/img_process.c\
        src/ldecod_src/mv_prediction.c\
        src/ldecod_src/fmo.c\
        src/ldecod_src/output.c\
        src/ldecod_src/mc_direct.c\
        src/ldecod_src/rtp.c\
        src/ldecod_src/nalucommon.c\
        src/ldecod_src/config_common.c\
        src/ldecod_src/intra_chroma_pred.c\
        src/ldecod_src/transform8x8.c\
        src/ldecod_src/blk_prediction.c\
        src/ldecod_src/intra8x8_pred_mbaff.c\
        src/ldecod_src/erc_do_i.c\
        src/ldecod_src/io_tiff.c\
        src/ldecod_src/mbuffer.c\
        src/ldecod_src/block.c\
        src/ldecod_src/intra4x4_pred.c\
        src/ldecod_src/transform.c\
        src/ldecod_src/annexb.c\
        src/ldecod_src/ldecod.c\
        src/ldecod_src/macroblock.c\
        src/ldecod_src/vlc.c\
        src/ldecod_src/parset.c\
        src/ldecod_src/loop_filter_normal.c\
        src/ldecod_src/parsetcommon.c\
        src/ldecod_src/erc_do_p.c\
        src/ldecod_src/loopFilter.c\
        src/ldecod_src/intra16x16_pred_mbaff.c\
        src/ldecod_src/intra4x4_pred_normal.c\
        src/ldecod_src/intra16x16_pred_normal.c\
        src/ldecod_src/win32.c\
        src/ldecod_src/intra16x16_pred.c\
        src/ldecod_src/intra8x8_pred_normal.c\
        src/ldecod_src/io_raw.c\
        src/ldecod_src/img_io.c\
        src/ldecod_src/nalu.c\
        src/ldecod_src/quant.c\
        src/ldecod_src/intra8x8_pred.c\
        src/ldecod_src/erc_api.c\
        src/ldecod_src/header.c\
        src/ldecod_src/biaridecod.c\
        src/ldecod_src/input.c

# imagevalidate
SOURCES_VALIDATE = \
        src/image_validator/ImageValidator.c

OBJ          = $(SOURCES:.c=.o)
OBJ_DECODE   = $(SOURCES_DECODE:.c=.o)
OBJ_VALIDATE = $(SOURCES_VALIDATE:.c=.o)

#VPATH	= src

$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ) $(BIN_DECODE) $(BIN_VALIDATE)
	$(CC) $(CFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

$(BIN_DECODE): $(OBJ_DECODE)
	$(CC) $(CFLAGS) -o $(BIN_DECODE) $(OBJ_DECODE) $(LDFLAGS) $(LIBS)

$(BIN_VALIDATE): $(OBJ_VALIDATE)
	$(CC) $(CFLAGS) -o $(BIN_VALIDATE) $(OBJ_VALIDATE) $(LDFLAGS) $(LIBS)

.c.o:
	$(CC) -c -o $@ $(EXTRA_CFLAGS) $(CFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) $(OBJ_DECODE) $(OBJ_VALIDATE)

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN_DECODE) $(BIN_VALIDATE) *.264
	-rm -f BuckBunny.264 BuckBunny_New.264 BuckBunny.yuv frame*.yuv x264_stats.log*
	-rm -f log.dec dataDec.txt imagevalidate_frame_*.out imagevalidate_frame_*.err
	-rm -f ldecod.err ldecod.out x264.err x264.out
