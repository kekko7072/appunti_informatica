# Lezione 12
Memoria dinamica e valgrind

Memoria dinamica: Allocazione di memoria dinamica viene gestita a basso livello.

    malloc: è un comando che alloca size byte, uso sempre sizeof() per sapere la quantità di byte perchè la dimensione delle variabili variano da calcolatore a calcolatore. Malloc ritorna un indirizzo, se è null vuol dire che non c'è l'ha fatta.
    
        void *mallloc(size_t size)
        
    free: libera la memoria precendentemente allocata
    
        void free(void *ptr)
        
valgrind: E' un framework per una serire di struenti per l'analisi dinamica dei programmi.

    1. Compile gcc -Wall -g -o file file.c
    2. valgrind ./file