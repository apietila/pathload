CC=gcc

CFLAGS=-g -O2 -pthread  -DHAVE_PTHREAD=1 -DHAVE_LIBM=1 -DHAVE_LIBNSL=1 -DSTDC_HEADERS=1 -DHAVE_FCNTL_H=1 -DHAVE_STRINGS_H=1 -DHAVE_SYS_TIME_H=1 -DHAVE_UNISTD_H=1 -DTIME_WITH_SYS_TIME=1 -DSIZEOF_INT=4 -DSIZEOF_LONG=8 -DHAVE_STRFTIME=1 -DHAVE_GETHOSTNAME=1 -DHAVE_GETTIMEOFDAY=1 -DHAVE_SOCKET=1  -DTHRLIB
CPPFLAGS=
LIBS=-lnsl -lm  
LDFLAGS=

SOBJS=client.o client_func.o vars.o
OBJS=$(SOBJS)

TARGETS=pathload2

all:${TARGETS}

pathload2: $(SOBJS)
	 $(CC) $(SOBJS) -o pathload2 $(LIBS) $(LDFLAGS) $(CFLAGS)

client.o client_func.o: client.h  global.h

clean: 
	 rm -f ${OBJS} ${TARGETS} config.cache config.log  config.status

distclean: 
	 rm -f ${OBJS} ${TARGETS} config.cache config.log makefile config.status
