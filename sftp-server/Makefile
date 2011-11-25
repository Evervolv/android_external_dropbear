CC       = arm-linux-androideabi-gcc
CPPFLAGS =
CFLAGS   = -I. $(CPPFLAGS) -march=armv7-a -mfloat-abi=softfp
LDFLAGS  = -s
OBJS     = sftp-server.o sftp-common.o sftp-server-main.o \
		addrmatch.o bufaux.o buffer.o compat.o log.o \
		openbsd-compat/bsd-misc.o openbsd-compat/bsd-statvfs.o \
		openbsd-compat/fmt_scaled.o openbsd-compat/getopt.o openbsd-compat/port-tun.o \
		openbsd-compat/pwcache.o \
		openbsd-compat/strmode.o openbsd-compat/strtonum.o openbsd-compat/vis.o \
		match.o misc.o \
		xmalloc.o

sftp-server : $(OBJS)
	$(CC) $(LDFLAGS) $(OBJS) -o $@

clean :
	rm -f $(OBJS) sftp-server
