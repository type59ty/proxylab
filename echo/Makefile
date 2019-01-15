# Makefile for Proxy Lab 
#
# You may modify this file any way you like (except for the handin
# rule). You instructor will type "make" on your specific Makefile to
# build your proxy from sources.

CC = gcc
CFLAGS = -g -Wall
LDFLAGS = -lpthread

all: echoclient echoserver 

csapp.o: csapp.c csapp.h
	$(CC) $(CFLAGS) -c csapp.c

echoclient.o: echoclient.c csapp.h
	$(CC) $(CFLAGS) -c echoclient.c

echoclient: echoclient.o csapp.o
	$(CC) $(CFLAGS) echoclient.o csapp.o -o echoclient $(LDFLAGS)


echoserver.o: echoserver.c csapp.h
	$(CC) $(CFLAGS) -c echoserver.c

echoserver: echoserver.o csapp.o
	$(CC) $(CFLAGS) echoserver.o csapp.o -o echoserver $(LDFLAGS)


clean:
	rm -f *~ *.o echoclient echoserver

