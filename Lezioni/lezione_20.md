# Lezione 20
TESTING

    + Testare il probrama serve per capire come funziona il software anche quando mettiamo dati sbagliati.

    + Tramite il TESTING è impossibile dimostrare che un programma è privo di bug
    
    + Pragmeticamente convincerti che uno specifico programma probabilmente funziona

INTERNAL TESTING
    Progettare il programma perchè si testi da solo, dunque modifichiamo il codice interno.
    
    # Macro assert:
        un solo parametro, che può essere vero o falso. Serve per verificare parametri invariani, deve essere vera quella condizione.
        - se vero:
            + non fa niente
        - se falso:
            + stampa un messaggio su stderr "assert at line x failed"
            + termina il progesso
        
        es:
        Validare parametri
            size_t Str_getLength(const char *str){
                assert(str != NULL);
            }
        Controllare flussi logici non possibili
        switch(state){
            case START; ... break;
            case COMMENT: ... break: 
            default: assert(0); /* Never should get here so put 0 (FALSE) */
        }
    
    
    1. Testare invarianti
        Verificare aspetti di una struttura datic he non devono variare
             
    2. Controllare sempre i valori di ritorno delle funzioni
    
        es.
                if (function(value) == ERROR_CODE) {
                    // TODO GESTIRE L'ERROE
                } else {
                    // TODO function HA FUNZIONATO
                }
        

    
    3. Modificare il codice temporaneamente
        Temporaneamente cambiare il codice per generare dei limiti artificiali o creare dei test di stress
    
    4. Lasciare il codice di test intatto
        Non rimuovere il codice di test quando il programma è finito
        
        Dovete usare degli strumenti per evitare che il codice sia inefficiente o non chiaro:
            + racchiudere le chiamate in assert()
            + Usare le direttive del processore #ifdef .. #endif
    
    5. Testare in modo incrementale
        Creare SCAFFHOLD e STUB per testare il codice che vi interessa
       
        SCAFFHOLD: Codice temporaneo che chiama il codice della funzione che volete testare e butta dentro in input
        
        STUB: Codice temporanero che è chiamato dal codice che volete testare
        
    6. Fault injection (testa il tuo testing)
        intenzionalmente metto un bug per vedere se il codice ti test nel sistema di testing
    
EXTERNAL TESTING
    Progettare dei dati/del software per testare il programma ma non prevede di mettere mano al codice con codice di test.
    
    Tipologie di testing esterno:
    
    1. Statement testing
        Testare le linee di codice, le facciamo andare almeno una volta tutte
        
        "Verificare che ogni istruzione in un programma sia eseguita almeno una volta durante il testing del programma."
        
    2. Path testing
        Verificare che qualsiasi percorso venga svolto ed eseguito almeno una volta
        
        Non si puo fare il path testing per programmio complessi
        
    3. Boundary testing
        Testare il programma nel comportamento ai limiti
        
        "Utilizza dei valori di input che si trovano appena sotto, o appena sopra i limiti definiti del dominio di input; e utilizza dei valori di input che protano l'output a trovarsi appena sotto o appena sopra i limiti definiti per il dominio di output."
        
        NOTA: 
            + OBBLIGATORIO DA FARE MA NON CONTROLLARE COSE BANALI
            + SE TEST FALLISCE NON MODIFICARE TU MA RIPORTA IL PROBLEMA AL DEV
        
        
    4. Stress testing
        Testare il comportamento per un periodo molto lungo
        
        "Testing per valutare un sistema o ua componente ai limiti o alter ai ai limiti delle specifiche."
        
        Cosa generare:
            + input molto grandi
            + input casuali