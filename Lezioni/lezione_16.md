# Lezione 16

Implementazione di funzioni di inserimento:

CMAKE:
    Dividere directory di file .c da file .h 
    -> Directory header file: include/
    -> Directory codice: src/
    Per riuscire a compilare il targhet eseguibile devi andare a cercare il file header nella directory include (nome convenzionale da usare):
    
    add_executable(eseguibile src/main.c src/part.c) 
    
    target_include_directories(eseguibile PRIVATE include) //Aggiunge la directory "include" che ha gli header file 
    

LIBRERIA:
    Bisogna cerca se esiste una libreria bisogna usarla.
    
    Librerie statiche: il codice viene compilato e aggiunto tutto il codice in memoria
        PROS: Nessuna dipendenza run-time
        CONS: Usa molta memoria + Necessità di essere ricompilato se la libreria viene aggiornata
        
         Comando per compilare libreria statica:
            gcc -c -Wall list.c
            ar crv liblist.a list.o  
         
         Comando per indicizzare l'archivio:
            run lib 
        
        COMPILARE IL MIO CODICE:
        gcc -o test_list test_list.o -L. -llist (libreria si chiama liblist)
         NOTA: -L. dice di cercare nella directory attuale
    
    Librerie dinamiche: il linker crea un file in cui le librerie dinamiche non sono dentro ma abbiamo un riferimento alle librerie dinamiche. Non le abbiamo dentro l'eseguibile ma sono dentro un altro spazio in memoria.
        PROS: Richiede meno memoria + Non richiede di compilare il programma dopo update libreria
        CONS: Le librerie devono essere presenti per poter eseguire il programma + Meno portabile
        
        Trova dipendenza:
            ldd test_list //Trova librerie da cui dipende
            
         Comando per compilare la libreria dinamica:
         gcc -c -Wall -fpic list.c 
         gcc -shared -o liblist.so list.o
         
        COMPILARE IL MIO CODICE:
        gcc -o test_list test_list.o -L. -llist (libreria si chiama liblist)
         NOTA: -L. dice di cercare nella directory attuale
       
      
        