CC=gcc

INC=-I../FANN-2.2.0-Source/src/include
LIBS=-L../FANN-2.2.0-Source/src -lfann -lm

CFLAGS=-g $(INC)

train: train.o
	$(CC) -o $@ $^ $(LIBS)

simple: simple.o
	$(CC) -o $@ $^ $(LIBS)

train.o: train.c
	$(CC) -c $^ $(CFLAGS)

simple.o: simple.c
	$(CC) -c $^ $(CFLAGS)

clean:
	rm -f train.o simple.o train simple core xor_float.net
