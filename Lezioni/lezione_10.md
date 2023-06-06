# Lezione 10
Debugging codice con gdb

gcc -Wall -g -Og -o media media.c

    flag -g crea sistema debugging
    
gdb media
    fa partire il debuggatore e si tira su il file media
    
    + run (o r): 
        serve per eseguire il programma
    
    + break name_function (o nome_file.c:numero:_linea) :
        mette dei punti di fermo, ovvero punti che fanno eseguire il programma fino a quel punto e poi a quella linea lì si ferma l'esecuzione
   
    + info break (o control X + A):
        da le informazioni relative ai punti di break
        + delete numero_punto_di_break:
            elimina il punto di break            

    + next: 
        esegue la linea dopo una riga per volta, detto anche step over.
        
    + step:
        esegue un passo se è una dicharazione, se c'è una funzione esegue la funione ed entra in profondità
            
    + where:
        permette di visualizzare lo stack delle chiamate di funzione 
    
    + finish:
        ci riporta nel nostro stack, finisce la funzione e ci riporta al record di attivazione
    + info args:
        ci stampa a schermo le variabili
            
    + print nome_variabile