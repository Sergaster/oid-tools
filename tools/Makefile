CC=gcc
CFLAGS=-Wall

all: parser_win potsum oidlist

utils: cert parser_openssl

parser_win: parser_win.o
	$(CC) parser_win.o -o parser_win

potsum: potlib.o potsum.o potread.o potwrite.o potlist.o xmalloc.o progname.o closeout.o fwriteerror.o

oidlist: oidlist.o potlib.o potread.o potlist.o xmalloc.o progname.o closeout.o fwriteerror.o

cert: cert.o
	$(CC) cert.o -o cert -lcrypto

parser_openssl: parser_openssl.o
	$(CC) parser_openssl.o -o parser_openssl -lcrypto

clean:
	rm -f *.o cert parser_win parser_openssl potsum oidlist
