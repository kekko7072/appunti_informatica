# Lezione 7
Controllo di versione (VCS) - git

Cosa memorizziamo:
    + Messaggio (commit)
    + Linee che abbiamo cambiato
    + File che abbiamo cambiato
    dunque memorizziamo solo le modifiche.

git config --global user.name "Nome Cognome"

git config --global user.email "s@studenti.unipd.it"

git config --global color.ui auto

Ogni commit ha un codice identificativo univoco.

Crea progetto: 
    git init 
    
Struttura repository:
    + Local Rep: File salvati 
    
    + Staging Area: file modificati da mandare (file da salvare con un etichetta)
    
    + Working copy: file modificati da mandare in repository
    
    + File non tracciati

    
Comandi:
    git add (aggiunge file pronti per stage)
    
    git commit (aggiungere un messaggio a file)
    
    git status