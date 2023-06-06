# Lezione 4
Mai ricopiare funzioni 

Creare terzo file che copia i file e assicura che i file "dupicati" siano sempre gli stessi

## Compilare preprocessore:
    
    `cpp -P -o output.i input.txt`

## Guaride nel preprocessore per evitare import multipi:

    #ifndef nomefile_estensione
    #define nomefile_estensione
    [codice di definizione]
    #endif


## Compilazione con il warning di gcc
    
    `gcc -Wall -Werror -o program program.c`

    Cosi vedi i warning e li converti in errori