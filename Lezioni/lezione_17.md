# Lezione 17

PER DEBUGGARE TUTTO IL CODICE CON CMAKE:
    cd build && cmake -DCMAKE_BUILD_TYPE=Dedbug ..
    [al posto di semplice cd build && cmake ..]

LIBRERIE STATICHE: 
Per ogni libreria nella mia applicazione avrò una directory lib e poi una sotto-directory per ogni libreria

Nel CMAKE della libreria:

    add_library( list STATIC src/list.c) : Crea una libreria statica
     
    PUBLIC è un usage requiremeent (ma anche per costruire la libreria) in permette a chi utilizzera la libreira di recuperare i file in incloude
    
        target_incloude_directories( list PUBLIC include )
    
    PRIVATE è un build requirements che sere solo per chi fa la build della libreria
    
    add_library( LII::list ALIAS list ) : Questo comando non crea una nuova libreria ma da un soprannome con cui la possiamo chiamare ovunque LII::list , se sposto la directory della libreria 
    
NON SI CREA UNA LIBRERIA PER OGNI FILE .c

APPLICATION:
target_link_libraries( test_list_lib
    PRIVATE LII::list ) : Questo comando ricorda di linkare la libreria lista al progetto perche usando il nome globale, uso PRIVATE perchè è un build requirements
    

LIBRERIE DINAMICHE:

aggiungi in CMAKE del prgetto:
    # Always use '-fPIC'/'-fPIE' option.
    set( CMAKE_POSITION_INDEPENDENT_CODE ON )

aggingi nel CMAKE della libreria addingi:
    add_library( list SHARED src/list.c)
    