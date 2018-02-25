CC = gcc
CFLAGS = -O3 -fPIC -std=c99
LDFLAGS= -lpthread -shared
TARGET = libmylock.so

sleepinglock:sleeping_lock.c
	$(CC) -c sleeping_lock.c $(CFLAGS)
	$(CC) -o $(TARGET) sleeping_lock.o $(LDFLAGS)

spinlock:spin_lock.c
	$(CC) -c spin_lock.c $(CFLAGS)
	$(CC) -o $(TARGET) spin_lock.o $(LDFLAGS)
