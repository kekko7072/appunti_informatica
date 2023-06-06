# Lezione 9
+ sizeof(a) di un array dice la dimensione in bite dell array

+ sizeof(a)/sizeof(a[0]) da il numero di elementi presenti

+ size_t serve ad essere utilizzato per definire un indice che viene usato per indicizzare l'array stesso, alla fine è un unsigned int

+ Nelle funzioni io passo gli array per indirizzo (tramite i ptr) perchè sennò dovrei copiare elemento per elemento.

+ Nelle variabili abbiamo due tipi di passaggio:
    + passaggio per valore: passo direttamente il valore
    + passaggio per indirizzo: passo l'indirizzo 
    
+ Con const nei passaggi delle funzioni ci assicuriamto che l'array non venga modificato.
    
    es.
    int media(const int *vett, size_t n){
        //Qui dentro l'array non puo essere modificato
    }
    