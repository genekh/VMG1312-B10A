# Generated automatically from Makefile.in by configure.
# $Id: Makefile.in,v 1.3 2000/01/05 16:29:43 ghudson Exp $

SHELL=/bin/sh
INSTALL=/usr/bin/install -c
RANLIB=ranlib
srcdir=.
top_srcdir=.
prefix=./build
exec_prefix=./build/
libdir=${exec_prefix}/lib
includedir=${prefix}/include
mandir=${prefix}/man
AR=/opt/toolchains/uclibc-crosstools-gcc-4.4.2-1/usr/bin/mips-linux-uclibc-ar

#CC=gcc
CPPFLAGS=
CFLAGS=-g -O2 ${WARN_CFLAGS} ${ERROR_CFLAGS}
DEFS= 
LDFLAGS=
LIBS=
ALL_CFLAGS=${CPPFLAGS} ${CFLAGS} ${DEFS}
OBJS=	ares__close_sockets.o ares__get_hostent.o ares__read_line.o \
	ares_destroy.o ares_expand_name.o ares_fds.o ares_free_errmem.o \
	ares_free_hostent.o ares_free_string.o ares_gethostbyaddr.o \
	ares_gethostbyname.o ares_init.o ares_mkquery.o ares_parse_a_reply.o \
	ares_parse_ptr_reply.o ares_process.o ares_query.o ares_search.o \
	ares_send.o ares_strerror.o ares_timeout.o zylist.o

all: libares.a adig ahost install

libares.a: ${OBJS}
	${AR} cru $@ ${OBJS}
	${RANLIB} $@

adig: adig.o libares.a
	${CC} ${LDFLAGS} -o $@ adig.o libares.a ${LIBS}

ahost: ahost.o libares.a
	${CC} ${LDFLAGS} -o $@ ahost.o libares.a ${LIBS}

${OBJS}: ares.h ares_dns.h ares_private.h

.c.o:
	${CC} -c ${ALL_CFLAGS} $<

check:

install:

#	${top_srcdir}/mkinstalldirs ${DESTDIR}${libdir}
#	${top_srcdir}/mkinstalldirs ${DESTDIR}${includedir}
#	${top_srcdir}/mkinstalldirs ${DESTDIR}${mandir}/man3
	${INSTALL} -m 644 libares.a $(INSTALL_DIR)/lib/public
	${RANLIB} $(INSTALL_DIR)/lib/public/libares.a
	chmod u-w $(INSTALL_DIR)/lib/public/libares.a
#	${INSTALL} -m 444 ${srcdir}/ares.h ${DESTDIR}${includedir}
#	${INSTALL} -m 444 ${srcdir}/ares_destroy.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_expand_name.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_fds.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_free_errmem.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_free_hostent.3 \
#		${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_free_string.3 \
#		${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_gethostbyaddr.3 \
#		${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_gethostbyname.3 \
#		${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_init.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_init_options.3 \
#		${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_mkquery.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_parse_a_reply.3 \
#		${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_parse_ptr_reply.3 \
#		${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_process.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_query.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_search.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_send.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_strerror.3 ${DESTDIR}${mandir}/man3
#	${INSTALL} -m 444 ${srcdir}/ares_timeout.3 ${DESTDIR}${mandir}/man3

clean:
	rm -f ${OBJS} libares.a adig.o adig ahost.o ahost

distclean: clean
	rm -f config.cache config.log config.status Makefile
