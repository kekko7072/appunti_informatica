# Lezione 22
Ottimizzare le prestazioni dei vostri programmi.

    Non ottimizzare a caso, ma bisogna capire dove perde tempo il programma e ottimizzare dove serve.
    
    Problemi della ottimizzazione:
        + talvolta diventa meno manutenibile, a questo punto è meglio che sia mantenibile ma piu lento.
        + possibilità di introdurre bug perchè si modifica codice, importante fare regression test.
        
     NON OTTIMIZZARE:
        se funciona già bene non serve
        
    5 PASSI:
        1. Analizzare il tempo di esecuzione
            + Comando unix time ./executable
                permette di vedere tempo di esecuzione
                    real: Tempo del wall clock time (tempo reale)
                    user: Tempo impiegato per far andare il codice del programma
                    sys: Tempo impiegato dal sistema operativo per eseguire il programma
            
            + E' sbagliato misurare il tempo così:
                gettimeofday(&start, NULL); //REAL TIME
                //CODICE
                gettimeofday(&end, NULL); //REAL TIME
                
                Perchè ci dice che è passato del tempo ma non da informazioni utili sui tempi porcessi 
                
            + E' meglio usare :
                clock_t begin = clock(); //USER e SYS TIME
                //CODICE
                clock_t end = clock();  //USER e SYS TIME
                
                Questo è meglio perchè misuro il tempo effettivo che il computer passa nel programma
            
            
        2. Identificare i punti del programma che meritano attenzione
            Si usa il programma Gprof (Gnu Performance Profiler) che permette di fare profiling, ovvero statistiche sull'esecuzione del programma. Si riesce così ad individuare le funzioni critiche con: tempo di esecuzione, numero di chimate, etcc..
            
            Compilare: 
            gcc -Wall -pg -o test test.c
            
            Eseguire 
            ./test
            si genera un gmon.out Gnu performance data
            
            Creazione del report 'analysis.txt'  
            gprof test gmon.out  > analisys.txt
            
        3. Usare altri algoritmi e strutture dati
            Prima di andare a modificare il codice, cerca di ottimizzare anche con il compilatore.
    
            gcc -Ox 
            dove x puo essere: 1, 2, 3 (in base al grado di ottimizzazione)
            
            NOTA: COMPILA IL PROGETTO CON -O1, -O2, -O3 E FAI ESECUZIONE E REPORT CON TIME
            
        4. Migliorare l'efficienza nell'uso della memoria
            + Usare dati piu piccoli
            + Calcolare il dato invece di memorizzarlo
            + Abilitare l'ottimizzazione del compilatore
                gcc .Os mysort.c -o mysort
                
                
OTTIMIZZARE PRIMA E' SBAGLIATO, OTTIMIZZAZIONE SI FA MA SOLO SE NECESSARIO                