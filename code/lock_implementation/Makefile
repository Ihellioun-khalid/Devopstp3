CC = gcc
CFLAGS = -O3 -fPIC -std=c99
LDFLAGS= -lpthread -shared
TARGET = libmylock.so
SRC=$(wildcard *.c)
OBJ=$(SRC:.c=.o)

sleepinglock:sleeping_lock.c
	@$(CC) -c $^ $(CFLAGS)
	@$(CC) -o $(TARGET) sleeping_lock.o $(LDFLAGS)
	@make clean

spinlock:spin_lock.c
	@$(CC) -c $^ $(CFLAGS)
	@$(CC) -o $(TARGET) spin_lock.c $(LDFLAGS)
	@make clean
clean:
	@rm -rf *.o
