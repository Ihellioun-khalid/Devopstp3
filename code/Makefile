CC = gcc
CFLAGS = -O3 -fPIC -std=c99
LDFLAGS= -lpthread -L./lock_implementation -lmylock -std=c99
TARGET= queue_test
export LD_LIBRARY_PATH=/Users/ihelliounkhalid/Desktop/Devopstp3/code/lock_implementation:$LD_LIBRARY_PATH
all : queue_test

queue_test : main.o queue.o 
	$(CC) main.o queue.o -o queue_test $(LDFLAGS)

queue.o : queue.c queue.h
	$(CC) -c queue.c queue.h $(CFLAGS)

main.o : main.c
	$(CC) -c main.c $(CFLAGS)

clean:
    rm -rf *.o $(EXEC)



