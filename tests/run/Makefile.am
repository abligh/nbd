if GNUTLS
TLSSRC = $(top_srcdir)/crypto-gnutls.c $(top_srcdir)/crypto-gnutls.h $(top_srcdir)/buffer.c $(top_srcdir)/buffer.h
else
TLSSRC =
endif
TESTS_ENVIRONMENT=$(srcdir)/simple_test
TESTS = cfg1 cfgmulti cfgnew cfgsize write flush integrity dirconfig list rowrite tree rotree unix tls #integrityhuge tlshuge
check_PROGRAMS = nbd-tester-client
nbd_tester_client_SOURCES = nbd-tester-client.c $(top_srcdir)/cliserv.h $(top_srcdir)/netdb-compat.h $(top_srcdir)/cliserv.c
if GNUTLS
nbd_tester_client_SOURCES += $(top_srcdir)/buffer.h $(top_srcdir)/buffer.c $(top_srcdir)/crypto-gnutls.h $(top_srcdir)/crypto-gnutls.c
endif
nbd_tester_client_CFLAGS = @CFLAGS@ @GLIB_CFLAGS@
nbd_tester_client_CPPFLAGS = -I$(top_srcdir)
nbd_tester_client_LDADD = @GLIB_LIBS@
EXTRA_DIST = integrity-test.tr integrityhuge-test.tr simple_test certs/client-key.pem certs/client-cert.pem certs/server-cert.pem certs/ca-cert.pem certs/ca.info certs/client.info certs/server-key.pem certs/ca-key.pem certs/server.info certs/README.md
cfg1:
cfgmulti:
cfgnew:
cfgsize:
write:
flush:
integrity:
integrityhuge:
dirconfig:
list:
rowrite:
tree:
rotree:
unix:
tls:
tlshuge:
