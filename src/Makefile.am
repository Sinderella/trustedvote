TESTS = libtrustedvote/libtrustedvote-test

bin_PROGRAMS = trustedvoted/trustedvoted
check_PROGRAMS = libtrustedvote/libtrustedvote-test
lib_LTLIBRARIES = libtrustedvote/libtrustedvote.la

# libtrustedvote/libtrustedvote.la

libtrustedvote_libtrustedvote_la_CPPFLAGS = \
	-I$(top_srcdir)/include \
	$(BOOST_CPPFLAGS)
libtrustedvote_libtrustedvote_la_LDFLAGS = \
	-version-info 0:0:0 \
	$(BOOST_LDFLAGS)
libtrustedvote_libtrustedvote_la_LIBADD = \
	-lstdc++fs
libtrustedvote_libtrustedvote_la_SOURCES = \
	libtrustedvote/config.cpp

# libtrustedvote/libtrustedvote-test

libtrustedvote_libtrustedvote_test_CPPFLAGS = \
	-I$(top_srcdir)/include \
	-DBOOST_TEST_DYN_LINK \
	$(BOOST_CPPFLAGS)
libtrustedvote_libtrustedvote_test_LDFLAGS = \
	$(BOOST_LDFLAGS)
libtrustedvote_libtrustedvote_test_LDADD = \
	libtrustedvote/libtrustedvote.la \
	-lstdc++fs \
	$(BOOST_UNIT_TEST_FRAMEWORK_LIB)
libtrustedvote_libtrustedvote_test_SOURCES = \
	libtrustedvote/config.test.cpp \
	libtrustedvote/test-main.cpp

# trustedvoted/trustedvoted

trustedvoted_trustedvoted_CPPFLAGS = \
	-I$(top_srcdir)/include \
	$(PTHREAD_CFLAGS) \
	$(BOOST_CPPFLAGS)
trustedvoted_trustedvoted_LDFLAGS = \
	$(BOOST_LDFLAGS)
trustedvoted_trustedvoted_LDADD = \
	libtrustedvote/libtrustedvote.la \
	$(BOOST_ASIO_LIB) \
	$(PTHREAD_CFLAGS)
trustedvoted_trustedvoted_SOURCES = \
	trustedvoted/main.cpp
