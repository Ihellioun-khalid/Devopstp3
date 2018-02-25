sleepinglock:sleeping_lock.c
	gcc -c sleeping_lock.c -O3 -fPIC
	gcc -o libmylock.so sleeping_lock.o -lpthread -shared

spinlock:spin_lock.c
	gcc -c spin_lock.c -O3 -fPIC
	gcc -o libmylock.so spin_lock.o -lpthread -shared
