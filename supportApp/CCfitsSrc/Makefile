TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

ifeq ($(WITH_CCFITS),YES)
  ifeq ($(CCFITS_EXTERNAL),NO)

    LIBRARY = CCfits
    ifeq ($(SHARED_LIBRARIES),YES)
      USR_CFLAGS += -DPIC -DNOLIBTOOL
      CCfits.dll: USR_CFLAGS_WIN32 += -DDLL_EXPORT
    endif

    INC += CCfits/AsciiTable.h
    INC += CCfits/BinTable.h
    INC += CCfits/CCfits.h
    INC += CCfits/ColumnCreator.h
    INC += CCfits/ColumnData.h
    INC += CCfits/Column.h
    INC += CCfits/ColumnT.h
    INC += CCfits/ColumnVectorData.h
    INC += CCfits/ExtHDU.h
    INC += CCfits/ExtHDUT.h
    INC += CCfits/FITSBase.h
    INC += CCfits/FitsError.h
    INC += CCfits/FITS.h
    INC += CCfits/FITSUtil.h
    INC += CCfits/FITSUtilT.h
    INC += CCfits/HDUCreator.h
    INC += CCfits/HDU.h
    INC += CCfits/ImageExt.h
    INC += CCfits/Image.h
    INC += CCfits/KeyData.h
    INC += CCfits/KeywordCreator.h
    INC += CCfits/Keyword.h
    INC += CCfits/KeywordT.h
    INC += CCfits/NewKeyword.h
    INC += CCfits/PHDU.h
    INC += CCfits/PHDUT.h
    INC += CCfits/PrimaryHDU.h
    INC += CCfits/Table.h

    INC += CCfits/CCfits

    CCfits_SRCS += AsciiTable.cxx
    CCfits_SRCS += BinTable.cxx
    CCfits_SRCS += ColumnCreator.cxx
    CCfits_SRCS += Column.cxx
    CCfits_SRCS += ColumnData.cxx
    CCfits_SRCS += ColumnVectorData.cxx
    CCfits_SRCS += ExtHDU.cxx
    CCfits_SRCS += FITSBase.cxx
    CCfits_SRCS += FITS.cxx
    CCfits_SRCS += FitsError.cxx
    CCfits_SRCS += FITSUtil.cxx
    CCfits_SRCS += HDUCreator.cxx
    CCfits_SRCS += HDU.cxx
    CCfits_SRCS += KeyData.cxx
    CCfits_SRCS += KeywordCreator.cxx
    CCfits_SRCS += Keyword.cxx
    CCfits_SRCS += PHDU.cxx
    CCfits_SRCS += Table.cxx

    LIB_LIBS += cfitsio

  endif # ($(CCFITS_EXTERNAL),NO)
endif # ($(WITH_CCFITS),YES)

        
include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

$(INSTALL_INCLUDE)/os/$(OS_CLASS)/CCfits/CCfits : ../CCfits
	$(ECHO) "Installing OS dependent include file $@"
	@$(INSTALL) -d -m $(INSTALL_PERMISSIONS) $< $(@D)
