# Lezione 14
Scrittura del codice in piu files:
    
    + Nel main lascio del main e importo il nuovo file
    #import "file.h"
    
    + Il nuovo file dovra essere strutturato su file.c
    
    + Aggiungo un file.h per informare il main.c per poter utilizzare il codice scritto in file.c . Mettiamo ad esempio le strutture (struct) nel file.h, mettiamo le cose di interfaccia negli header files. Aggiungo anche i prototipi delle funzioni.
        
Cmake è un build-system generator:
    genera il make per (Linux/macOS) e il Visual Studio project (Windows)

    1. Crea file CMakeLists.txt
    2. Crea cartella build 
        mkdir build
    3. Esegui il comando dentro la directory
        cd build && cmake ..
        