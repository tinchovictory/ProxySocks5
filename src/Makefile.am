bin_PROGRAMS    = socksv5 hello_test request_test netutils_test
socksv5_SOURCES = main.c \
                  hello.h hello.c \
		  request.h request.c \
                  netutils.h netutils.c \
		  buffer.h buffer.c \
                  socks5.h socks5.c

TESTS = hello_test request_test netutils_test \
        buffer_test
check_PROGRAMS = hello_test request_test netutils_test \
                 buffer_test

hello_test_SOURCES = hello_test.c hello.c hello.h buffer.c buffer.h
hello_test_CFLAGS  = @CHECK_CFLAGS@ 
hello_test_LDADD   = @CHECK_LIBS@

request_test_SOURCES = request_test.c request.c request.h buffer.c buffer.h
request_test_CFLAGS  = @CHECK_CFLAGS@
request_test_LDADD   = @CHECK_LIBS@

netutils_test_SOURCES = netutils_test.c netutils.h netutils.c buffer.c buffer.h
netutils_test_CFLAGS  = @CHECK_CFLAGS@
netutils_test_LDADD   = @CHECK_LIBS@

buffer_test_SOURCES = buffer_test.c buffer.h
buffer_test_CFLAGS  = @CHECK_CFLAGS@
buffer_test_LDADD   = @CHECK_LIBS@


# si se utilizó converage lo limpiamos
# https://gcc.gnu.org/onlinedocs/gcc-7.1.0/gcc/Gcov-Data-Files.html
clean-local:
	rm -f *.gcno *.gcda

