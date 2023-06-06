# Lezione 19
Git 
    branch: nasce come risposta alla presenza dei contesti diversi, un progetto grande ha per forza diversi contesti.
    Devo aprire un nuovo branch ogni volta che lavoro su un contesto diverso.
    Devo fare merge quando sono contento del risultato.
    
    Creazione di un nuovo branch:   
        git branch new-name 

    Spostare la working directory:
        git checkout branch-name
        
    Marge dei branch:
        git checkout branch-dove-mergare
        git merge branch-da-cui-prendere
        
    I conflitti non devono succedere, si fanno meeting e si decide cosa fa cosa.
    
    git branch -va
    
    
    git fetch 
    
    Prendi i commit da remoto
    git pull
    
    Eliminare i branch 
    git branch -d new_feature
    
    Eliminare branch remoto
    git branch -origin --delete new_feature
    
    
Best practice
    
    1. Commit di cambiamenti che sono legati fra loro
    2. commit frequenti
    3. non fate commit di lavori fatti a metà
    4. verificate che compili prima di fare commit
    5. scrivete buoni messaggi di commit
    6. git-hub non è un sistema di backup
    8. usate i branch
    9. mettetevi d'accorrdo sul flusso di lavoro
