# Appunti informatica 2022/ 2023
Appunti per il ripasso del corso di informatica industriale:
## Lezione 1 UNIX / LINUX
Introduzione a UNIX / LINUX
## Lezione 2 FILE
Operazione sui file.
## Lezione 3 DATI
Cenni sui flussi di dati
## Lezione 4 COMPILAZIONE
Compilazione e preprocessore
## Lezione 5 TERMINOLOGIA
Terminologia
## Lezione 6 STACK
Cenni sullo stack
## Lezione 7 VCS GIT
Controllo di versione (VCS) con git
## Lezione 8 GIT 
Come usare git e come committare
## Lezione 9 ARRAY
Cenni sugli array
## Lezione 10 DEBUGGING
Debugging codice con gdb
## Lezione 11 ERRORI
Cenni sugli errori
## Lezione 12 MEOMORIA DINAMICA
Cenni sulla memoria dinamica
## Lezione 13 VALGRIND
Cenni di VALGRIND
## Lezione 14 MODULARITA'
Nella lezione 14 abbiamo appreso come organizzare il codice in più file per una migliore modularità e manutenibilità. Abbiamo visto che il file principale (main.c) può importare altri file utilizzando l'istruzione '#include "file.h"', e il codice correlato può essere suddiviso in file.c separati. Abbiamo anche imparato l'importanza dei file di intestazione (header files), che contengono le dichiarazioni delle strutture e i prototipi delle funzioni per consentire al file principale di utilizzare il codice scritto nei file separati. Inoltre, abbiamo introdotto CMake come un generatore di sistemi di compilazione, che ci consente di creare file di progetto per diversi ambienti di sviluppo come Make e Visual Studio. L'uso di CMake semplifica il processo di compilazione e gestione del nostro codice.
## Lezione 15 STRUCT E PUNTATORI
Nella lezione 15 abbiamo approfondito le struct e i puntatori. Abbiamo imparato che l'operatore '->' è utilizzato per dereferenziare un puntatore a una struct. Abbiamo anche visto come utilizzare il modificatore 'const' per specificare che una variabile non deve essere modificata. Successivamente, abbiamo esaminato le liste concatenate come una struttura dati che consente di memorizzare una sequenza di elementi collegati tra loro attraverso puntatori. Ogni elemento della lista contiene un dato e un puntatore al successivo. Infine, abbiamo mostrato un esempio di implementazione di una lista concatenata utilizzando struct e puntatori.
## Lezione 16 CMAKE
Nella lezione 16 abbiamo discusso l'implementazione di funzioni di inserimento in CMake e l'utilizzo di librerie statiche e dinamiche. Abbiamo suddiviso i file .c e .h in directory separate (src/ e include/) e utilizzato il comando 'target_include_directories' per aggiungere la directory degli header file al target eseguibile. Per le librerie statiche, abbiamo compilato il codice e creato un archivio con il comando 'ar'. Per le librerie dinamiche, abbiamo utilizzato l'opzione '-fpic' per la compilazione e creato una libreria con il comando 'gcc -shared'. Infine, abbiamo mostrato come compilare il nostro codice utilizzando le librerie sia statiche che dinamiche.
## Lezione 17 LIBRERIE
Nella lezione 17 abbiamo esplorato l'utilizzo delle librerie statiche e dinamiche in CMake. Abbiamo imparato a creare librerie statiche con il comando 'add_library' e a specificare le directory di inclusione utilizzando 'target_include_directories'. Inoltre, abbiamo introdotto l'uso di alias per le librerie con 'add_library ALIAS' e l'importanza di linkare correttamente le librerie alle applicazioni tramite 'target_link_libraries'. Per le librerie dinamiche, abbiamo configurato l'opzione '-fPIC'/'-fPIE' nel CMake del progetto e creato una libreria dinamica utilizzando 'add_library' con il flag 'SHARED'.## Lezione 18 Progettare programmi
Progettare programmi
## Lezione 19 GIT + GITHUBH
Nella lezione 19 abbiamo appreso che i branch in Git sono utilizzati per gestire contesti diversi all'interno di un progetto, aprendo nuovi branch per lavorare su contesti separati e facendo merge quando soddisfatti del risultato, e sono state condivise alcune best practice come fare commit frequenti, evitare commit di lavori incompleti, compilare prima di committare e utilizzare GitHub come repository principale anziché come sistema di backup.
## Lezione 20 TESTING
Nella lezione 20 abbiamo esplorato il testing interno, che prevede la modifica del codice per il testing automatico, e il testing esterno, che si basa sulla progettazione di dati o software per testare il programma senza modifiche dirette al codice, fornendo una panoramica completa delle strategie di testing.
## Lezione 21 UNITY
Nella lezione 21 abbiamo appreso come utilizzare Unity per il testing, importando il file 'unity.h' e aggiungendo i test nel main con UNITY_BEGIN(), RUN_TEST() e UNITY_END(). È possibile confrontare array e i test possono includere funzioni setUp() e tearDown(). È importante pensare a test significativi e scrivere test per ogni modulo del progetto.
## Lezione 22 OTTIMIZZAZIONE
- Nella lezione 22 abbiamo appreso l'importanza di ottimizzare le prestazioni dei programmi, focalizzandoci sulle aree che richiedono miglioramenti specifici.
- Tuttavia, è necessario bilanciare l'ottimizzazione con la manutenibilità e svolgere i test di regressione per evitare l'introduzione di bug. L'analisi del tempo di esecuzione e l'identificazione dei punti critici tramite Gprof possono aiutare in questo processo.
- È anche importante considerare l'utilizzo di algoritmi e strutture dati più efficienti, nonché migliorare l'uso della memoria attraverso strategie come la riduzione delle dimensioni dei dati e il calcolo al volo. L'ottimizzazione del compilatore può essere un'opzione da considerare.
- Infine, è fondamentale evitare di ottimizzare prematuramente e concentrarsi sull'ottimizzazione solo se necessario.