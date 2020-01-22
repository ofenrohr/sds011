# makefile for sds011. Janaury 2019 / paulvha

CC = gcc
DEPS = sds011_lib.h serial.h http_client.h
OBJ = sds.o serial.o sds011_lib.o http_client.o
LIBS = -lm -lcurl
CFLAGS = -Wall

.cpp.o: %c $(DEPS)
	$(CC) $(CFLAGS) -c -o $@ $<

sds : $(OBJ)
	$(CC) -o $@ $^ $(LIBS)

.PHONY : clean

clean :
	rm sds $(OBJ)
