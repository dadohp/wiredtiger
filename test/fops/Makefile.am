AM_CPPFLAGS = -I$(top_builddir) -I$(top_srcdir)/src/include \
    -I$(top_srcdir)/test/utility

noinst_PROGRAMS = t
t_LDADD = $(top_builddir)/libwiredtiger.la

t_SOURCES = thread.h file.c fops.c t.c
t_LDFLAGS = -static

# Run this during a "make check" smoke test.
TESTS = $(noinst_PROGRAMS)
LOG_COMPILER = $(TEST_WRAPPER)

clean-local:
	rm -rf WT_TEST *.core
