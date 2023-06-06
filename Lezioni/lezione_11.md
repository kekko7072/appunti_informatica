# Lezione 11
Terminologia dell'errore:
    + Errore: il programma fa qualcosa di sbagliato. Gli error sono la causa dell essere umano.
    + Difetto (bug): Quando a causa di un errore, il software può avere una struttura incorretta
    + Fallimento: Quando a causa di un difetto, il software può comportarsi in modo incorretto durante la sua esecuzione.
    
    Bisgona testare nelle situazioni limite.
    
BUG: E' qualsiasi cosa he causi dolore all'utente.
    + Interfacce utente inconsistenti
    + Aspettative insoddisfatte
    + Scarse prestazioni
    + Arresti anomali
    
NON CAMBIARE CODICE A CASO QUANDO C'E' UN BUG, CORREGGI IL CODICE NON SCRIVERNE NUOVO.

TIPI DI ERRORI:
    1. Errore di compilazione.
        Leggere gli errori in output al compilatore.
    2. Programma di arresta anzitempo.
        Usare gdb e permette di andare piano piano e capire dove finisce.
    3. Loop infinito
        Usare gdb e con control + c permette di fermare il programma.
    4. Errore logico.
    
Provare a rigenerare il problema.

Domande da farsi:
    + Quale era la causa?
    + Questo errore esiste da qualche altra parte?

BOOK: David Agans ~ Debugging:
    1. Undestand the system
    2. Make it fail
    3. Quit thinking and look
    4. Divide and conquer
    5. Change one thing at a time
    6. Keep an Audit trail
    7. Check the plug
    8. Get a Fresh view
    9. If you didn't fix it, it ain't fixed