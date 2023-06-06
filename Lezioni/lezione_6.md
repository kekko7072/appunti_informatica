# Lezione 6
## Funzioni:

    DICHIARAZIONE: dichiaro che esiste da qualche parte. Dichiaro anche che tipo di parametri devo passare. Si mette nel header file (.h)

## NOTA:
    CALL STACK: pila di chiamate alle funzioni [TODO: fare esercizi]
   ```
    ________________________
    -                      -
    -                      -
    -                      -
    -                      -        CALL 
    ------------------------        STACK   
    -                      -   
    -  x[ø]                -    f(xx)
    -                      -    
    ________________________
    -                      -
    -  xx[ø]  risultato[]  -   <- RECORD DI ATTIVAZIONE
    -                      -
    -                      -    main()
    -                      -
    ________________________
    
```
    
## Puntatori:
    + Uso * per indicare cosa c'è un etichetta di un byte
        es. `int *p`
    
    + Uso & per andare a recuperare l'indirizzo dietro una variabile
        ex. 
            ```
            int a = 3;
            int *a_ptr;
            a_ptr = &a;
            ```
        ex.
            `int c = b + (*a_ptr);`
            
            