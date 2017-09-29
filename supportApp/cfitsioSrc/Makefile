TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

ifeq ($(WITH_CFITSIO),YES)
  ifeq ($(CFITSIO_EXTERNAL),NO)

    USR_CFLAGS += -Dg77Fortran
    USR_CFLAGS += -DHAVE_UNISTD_H=1
    USR_CFLAGS += -DHAVE_FTRUNCATE=1
    USR_CFLAGS += -DHAVE_LONGLONG=1
    USR_CFLAGS += -DHAVE_SHMEM_SERVICES=1
    USR_CFLAGS += -DHAVE_NET_SERVICES=1
    USR_CFLAGS += -D_LARGEFILE_SOURCE=1
    USR_CFLAGS += -D_FILE_OFFSET_BITS=64

    LIBRARY = cfitsio
    ifeq ($(SHARED_LIBRARIES),YES)
      USR_CFLAGS += -DPIC -DNOLIBTOOL
      cfitsio.dll: USR_CFLAGS_WIN32 += -DDLL_EXPORT
    endif

    INC += drvrsmem.h
    INC += fitsio2.h
    INC += fitsio.h
    INC += longnam.h

    cfitsio_SRCS += buffers.c
    cfitsio_SRCS += cfileio.c
    cfitsio_SRCS += checksum.c
    cfitsio_SRCS += drvrfile.c
    cfitsio_SRCS += drvrgsiftp.c
    cfitsio_SRCS += drvrmem.c
    cfitsio_SRCS += drvrnet.c
    cfitsio_SRCS += drvrsmem.c
    cfitsio_SRCS += editcol.c
    cfitsio_SRCS += edithdu.c
    cfitsio_SRCS += eval_f.c
    cfitsio_SRCS += eval_l.c
    cfitsio_SRCS += eval_y.c
    cfitsio_SRCS += f77_wrap1.c
    cfitsio_SRCS += f77_wrap2.c
    cfitsio_SRCS += f77_wrap3.c
    cfitsio_SRCS += f77_wrap4.c
    cfitsio_SRCS += fitscore.c
    cfitsio_SRCS += fits_hcompress.c
    cfitsio_SRCS += fits_hdecompress.c
    cfitsio_SRCS += getcol.c
    cfitsio_SRCS += getcolb.c
    cfitsio_SRCS += getcold.c
    cfitsio_SRCS += getcole.c
    cfitsio_SRCS += getcoli.c
    cfitsio_SRCS += getcolj.c
    cfitsio_SRCS += getcolk.c
    cfitsio_SRCS += getcoll.c
    cfitsio_SRCS += getcols.c
    cfitsio_SRCS += getcolsb.c
    cfitsio_SRCS += getcolui.c
    cfitsio_SRCS += getcoluj.c
    cfitsio_SRCS += getcoluk.c
    cfitsio_SRCS += getkey.c
    cfitsio_SRCS += group.c
    cfitsio_SRCS += grparser.c
    cfitsio_SRCS += histo.c
    cfitsio_SRCS += imcompress.c
    cfitsio_SRCS += iraffits.c
    cfitsio_SRCS += modkey.c
    cfitsio_SRCS += pliocomp.c
    cfitsio_SRCS += putcol.c
    cfitsio_SRCS += putcolb.c
    cfitsio_SRCS += putcold.c
    cfitsio_SRCS += putcole.c
    cfitsio_SRCS += putcoli.c
    cfitsio_SRCS += putcolj.c
    cfitsio_SRCS += putcolk.c
    cfitsio_SRCS += putcoll.c
    cfitsio_SRCS += putcols.c
    cfitsio_SRCS += putcolsb.c
    cfitsio_SRCS += putcolu.c
    cfitsio_SRCS += putcolui.c
    cfitsio_SRCS += putcoluj.c
    cfitsio_SRCS += putcoluk.c
    cfitsio_SRCS += putkey.c
    cfitsio_SRCS += quantize.c
    cfitsio_SRCS += region.c
    cfitsio_SRCS += ricecomp.c
    cfitsio_SRCS += scalnull.c
    cfitsio_SRCS += simplerng.c
    cfitsio_SRCS += swapproc.c
    cfitsio_SRCS += wcssub.c
    cfitsio_SRCS += wcsutil.c

    ifeq ($(ZLIB_EXTERNAL),YES)
      ifdef ZLIB_INCLUDE
        USR_INCLUDES += $(ZLIB_INCLUDE)
      endif
      ifdef ZLIB_LIB
        z_DIR        = $(ZLIB_LIB)
        LIB_LIBS     += z
      else
        LIB_SYS_LIBS += z
      endif
    else
      LIB_LIBS += zlib
    endif

  endif # ($(CFITSIO_EXTERNAL),NO)
endif # ($(WITH_CFITSIO),YES)

        
include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

