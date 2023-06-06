# Lezione 13
[VEDI SLIDE]

Controlla se c'è liberazione della memoria:
    vlagrind --leak-check=full ./executable
    
Controlla se lists of detected and suppressed errors:
    vlagrind -s ./executable
    
Incapsulamento: una volta che ho creato il tipo chi usa il tipo deve usare le funzioni per fare le operazioni e non deve usare l'operatore dot nel main ma deve usare le funzioni per operare con il tipo. A chi usa il tipo non deve interessare come è fatto il tipo all'interno