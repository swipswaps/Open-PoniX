## Process this file with automake to produce Makefile.in

if WITH_RDPSND

# rdpsnd
rdpsnddir = $(PLUGIN_PATH)

rdpsnd_LTLIBRARIES = rdpsnd.la

rdpsnd_la_SOURCES = \
	rdpsnd_dsp.h rdpsnd.h \
	rdpsnd_main.c

rdpsnd_la_CFLAGS = -I$(top_srcdir)/include -I$(srcdir)/../common \
	-DPLUGIN_PATH=\"$(PLUGIN_PATH)\"

rdpsnd_la_LDFLAGS = -avoid-version -module

rdpsnd_la_LIBADD = ../common/libcommon.la

if RDPSND_ALSA
rdpsnd_la_SOURCES += rdpsnd_alsa.c
rdpsnd_la_CFLAGS += @ALSA_CFLAGS@
rdpsnd_la_LIBADD += @ALSA_LIBS@
endif

#	rdpsnd_pulse.c

# extra
EXTRA_DIST =

DISTCLEANFILES = 

endif

