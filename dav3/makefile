

CC = gcc
CFLAGS=-Wall

all: simple
.PHONY : all

simple: main.o
	$(CC) $(CFLAGS) -o simple main.o
	
main.o: main.c
	$(CC) $(CFLAGS) -c -o main.o main.c
	
debug: clean  main.c
	$(CC) $(CFLAGS) -g -o test main.c 
	gdb -tui test
	
.PHONY: clean
clean:
	rm -rf *.o
