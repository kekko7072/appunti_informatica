# Lezione 21
Tesing in unity

1. importare unity.h
    2. aggiugnere nel main
        UNITY_BEGIN();
        RUN_TEST(test functione_che_devo_testare);
        
        return UNITY_END();
        
    SLeggere Unity Asdsertions Reference per vedere cosa si puo testare e comparare
    
    NOTA: Si possono comparare gli array.
    
    DALLA REPOSITORY DI UNITY SI COPIANO I TRE FILE DENTRO SRC
    unity_internals.h
    unity.c
    unity.h
    
    
    Ogni volta che esegue un test chiama prima e dopo:
    
     setUp(void) {
        /* Qui codice che viene eseguito prima del test */
     }
     
     tearDown(void) {
        /* Qui codice che viene eseguito dopo il test */
     }
     
     NON SIAMO COSTRETTI CON UNITY
     
     ES: TEST ALBERO ORDINATO
     METTO DENTRO UNA SERIE DI VALORI E VEDO SE SONO ORDINATI ALLA FINE.
     
     IL PROBLEMA E' PENSARE A TEST CHE HANNO SENSO
     
     SCRIVERE TEST PER OGNI MODULO