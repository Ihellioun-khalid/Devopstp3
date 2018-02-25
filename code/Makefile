CC = gcc
CFLAGS = -O3 -fPIC -std=c99
LDFLAGS= -lpthread -L./lock_implementation -lmylock -std=c99
TARGET= queue_test
SRC=$(wildcard *.c)
OBJ=$(SRC:.c=.o)

export LD_LIBRARY_PATH=/Users/ihelliounkhalid/Desktop/Devopstp3/code/lock_implementation:$LD_LIBRARY_PATH

all : queue_test

queue_test : $(OBJ) 
	@$(CC) $^ -o $@ $(LDFLAGS)

queue.o : queue.h

%.o : %.c
	@$(CC) -c $^ $(CFLAGS)

test : lockimplementation code

lockimplementation :
	@cd lock_implementation ; \
	make ; \
	make clean ; \
	cd ..

code :
	@make

clean:
	@rm -rf *.o

