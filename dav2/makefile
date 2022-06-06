

CC = gcc
CFLAGS=-Wall

all: strend2
.PHONY : all

strend2: mygetchar.o main.o
	$(CC) $(CFLAGS) -o strend2 mygetchar.o main1.o
	
mygetchar.o: mygetchar.c
	$(CC) $(CFLAGS) -c -o mygetchar.o mygetchar.c

main.o: main.c
	$(CC) $(CFLAGS) -c -o main.o main.c
	
debug: clean mygetchar.c main.c
	$(CC) $(CFLAGS) -g -o test main.c mygetchar.c
	gdb -tui test
	
.PHONY: clean
clean:
	rm -rf *.o
