DIST_SUBDIRS = x86 ppc sparc arm arm64 s390x amd64 ia64 mips

AM_CPPFLAGS = $(GLIB_CFLAGS) -I$(top_srcdir)

if INTERP_SUPPORTED
SUBDIRS = $(arch_target)
else
if ARM
# arm needs to build some stuff even in JIT mode
SUBDIRS = $(arch_target)
endif
endif

if INTERP_SUPPORTED

noinst_LTLIBRARIES = libmonoarch.la

libmonoarch_la_SOURCES = unknown.c

libmonoarch_la_LIBADD = $(arch_target)/libmonoarch-$(arch_target).la

endif

EXTRA_DIST = ChangeLog

