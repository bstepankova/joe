################################################################################
#  THIS FILE IS 100% GENERATED BY ZPROJECT; DO NOT EDIT EXCEPT EXPERIMENTALLY  #
#  Read the zproject/README.md for information about making permanent changes. #
################################################################################
MAN1 = joed.1 joec.1
MAN3 = joe_server.3 joe_proto.3
MAN7 = joe.7
MAN_DOC = $(MAN1) $(MAN3) $(MAN7)

MAN_TXT = $(MAN1:%.1=%.txt)
MAN_TXT += $(MAN3:%.3=%.txt)
MAN_TXT += $(MAN7:%.7=%.txt)

EXTRA_DIST = asciidoc.conf $(MAN_TXT)

if INSTALL_MAN
dist_man_MANS = $(MAN_DOC)
endif

if BUILD_DOC
DISTCLEANFILES = $(MAN_DOC)

dist-hook : $(MAN_DOC)

SUFFIXES=.txt .xml .1 .3 .7

.txt.xml:
	asciidoc -d manpage -b docbook -f $(srcdir)/asciidoc.conf \
        -ajoe_version=@PACKAGE_VERSION@ -o$@ $<
.xml.1:
	xmlto man $<
.xml.3:
	xmlto man $<
.xml.7:
	xmlto man $<

joe_server.txt:
	./mkman $@
joe_proto.txt:
	./mkman $@
joed.txt:
	./mkman joed $@
joec.txt:
	./mkman joec $@
clean:
	rm -f *.1 *.3 *.7
doc:
	./mkman joe_server
	./mkman joe_proto
	./mkman joed joed
	./mkman joec joec

endif
################################################################################
#  THIS FILE IS 100% GENERATED BY ZPROJECT; DO NOT EDIT EXCEPT EXPERIMENTALLY  #
#  Read the zproject/README.md for information about making permanent changes. #
################################################################################
