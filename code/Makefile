#Ihellioun khalid et Ahmed sarraj
CC = gcc
CFLAGS = -O3 -fPIC
LDFLAGS= -lpthread -L./lock_implementation -lmylock
TARGET= queue_test
SRC=$(wildcard *.c)
OBJ=$(SRC:.c=.o)

all : $(TARGET)

queue_test : $(OBJ)
	@$(CC) $^ -o $@ $(LDFLAGS)

main.o : queue.h

%.o : %.c
	@$(CC) -c $^ $(CFLAGS)

test : lockimplementation code

lockimplementation :
ifeq ($(TEST),spinlock)
	@cd lock_implementation ; \
	make spinlock ; \
	make clean
	@cd ..
endif
ifeq ($(TEST),sleepinglock)
	@cd lock_implementation ; \
	make sleepinglock ; \
	make clean
	@cd ..
endif
ifeq ($(TEST),)
	@cd lock_implementation ; \
	make ; \
	make clean
	@cd ..
endif
code :
	@make all
	@make clean

ifneq ($(NB_THREADS),)
	./queue_test
	@make mrpropre
endif

clean :
	@rm -rf *.o
	@rm -rf *.h.gch
mrpropre :
	make clean
	@rm -rf queue_test

