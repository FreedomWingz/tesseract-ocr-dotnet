SUBDIRS =
AM_CPPFLAGS = \
    -I$(top_srcdir)/cutil -I$(top_srcdir)/ccutil \
    -I$(top_srcdir)/ccstruct -I$(top_srcdir)/dict \
    -I$(top_srcdir)/image -I$(top_srcdir)/viewer

include_HEADERS = \
    adaptive.h baseline.h blobclass.h chartoname.h \
    classify.h cluster.h clusttool.h cutoffs.h \
    extern.h extract.h \
    featdefs.h flexfx.h float2int.h fpoint.h fxdefs.h \
    intfx.h intmatcher.h intproto.h kdtree.h \
    mf.h mfdefs.h mfoutline.h mfx.h \
    normfeat.h normmatch.h \
    ocrfeatures.h outfeat.h picofeat.h protos.h \
    speckle.h xform2d.h

if !USING_MULTIPLELIBS
noinst_LTLIBRARIES = libtesseract_classify.la
else
lib_LTLIBRARIES = libtesseract_classify.la
libtesseract_classify_la_LDFLAGS = -version-info $(GENERIC_LIBRARY_VERSION)
libtesseract_classify_la_LIBADD = \
	../ccutil/libtesseract_ccutil.la \
	../cutil/libtesseract_cutil.la \
	../ccstruct/libtesseract_ccstruct.la \
	../dict/libtesseract_dict.la \
	../image/libtesseract_image.la \
	../viewer/libtesseract_viewer.la
endif

libtesseract_classify_la_SOURCES = \
    adaptive.cpp adaptmatch.cpp blobclass.cpp \
    chartoname.cpp classify.cpp cluster.cpp clusttool.cpp cutoffs.cpp \
    extract.cpp \
    featdefs.cpp flexfx.cpp float2int.cpp fpoint.cpp fxdefs.cpp \
    intfx.cpp intmatcher.cpp intproto.cpp kdtree.cpp \
    mf.cpp mfdefs.cpp mfoutline.cpp mfx.cpp \
    normfeat.cpp normmatch.cpp \
    ocrfeatures.cpp outfeat.cpp picofeat.cpp protos.cpp \
    speckle.cpp xform2d.cpp


