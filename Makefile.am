bin_PROGRAMS = squashdelta

squashdelta_SOURCES = \
	src/compressor.cxx \
	src/compressor.hxx \
	src/hash.cxx \
	src/hash.hxx \
	src/squashfs.cxx \
	src/squashfs.hxx \
	src/util.cxx \
	src/util.hxx \
	src/squashdelta.cxx

squashdelta_CPPFLAGS = \
	$(LZO_CFLAGS) \
	$(LZ4_CFLAGS)
squashdelta_LDADD = \
	$(LZO_LIBS) \
	$(LZ4_LIBS)

EXTRA_DIST = NEWS
NEWS: configure.ac Makefile.am
	git for-each-ref refs/tags --sort '-*committerdate' \
		--format '# %(tag) (%(*committerdate:short))%0a%(contents:body)' \
		> NEWS
