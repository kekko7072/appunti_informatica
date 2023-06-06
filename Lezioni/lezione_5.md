# Lezione 5
Termini da usare

 - **identificatore**: Nome di una variabile

- **keyword**: [parola chiave/parola riservata] sono nomi non utilizzabili 
    ex. main
    
- **variabili**: deve essere creata e definita, puo essere definita su più punti
    ex. num_ling=0;  //è un assegnamento
         = : è operatore di assegnamento
         num_ling : LVALUE
         0 : RVALUE

- **costanti**: devono essere in maiuscolo e definite per preprocessing
    ex. #define MEMBRI_FAMIGLIA 5
    
    Nel C99 si puo scrivere anche così:
    ex. const int membri_famiglia = 5; 

- **operatori aritmetici**:
    - moltiplicazione `*`
    - sottratione `-`
    - divisione `/`
        ex. `17/5 = 3`
        ex. `17.0/5 = 3.4000`
    - resto di una divisione [%]
    - `n++` usa il valore e poi incrementa di 1
    - `n--` usa il valore e poi decrementa di 1
    - `++n` prima incrementa di 1 e poi usa il valore
    - `--n`  prima decrementa di 1 e poi usa il valore
    
- **cicli**: 
    - while: 
        ```
        while(cond)**
        // Blocco istruzioni
        ```
    - for:
        ```
        for(int i = 0; i < 100; i++)
        //Blocco istruzione
        ```