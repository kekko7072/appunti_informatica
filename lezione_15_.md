# Lezione 15

Struct e Puntatori

    p->on_hand : -> è loperatore di dereferenziazione per le struct corrisponde a (*p).on_hand
    
    void print_part(const struct part *p): il const serve per dire che la variabile p non deve essere modificata. Il const deve essere usato
    
    print_part(&part1): cosi devo passare i parametri
    
    Se lo devo modificare uso il puntatore senza const, se invece lo devo modifcare lo passo con il puntatore e const.
    
    Ottima scrittura del struct:
        
        void build_part(struct part *p, int number, const char *name, int on_hand){
            p->number = number;
            strcpy(p->name, name);
            p->on_hand = on_hand;
        }
        
        int main(){
            struct part part1;
            build_part(&part, 528, "Disk drive, 10");
        }
        
Liste concatenate

    La lista è una sequenza di elementi. 
    Quando aggiungo gli elementi io li metto all'inizio perche cosi accedo al primo
    Nella memoria ogni elemento è distaccato dall'altro perchè si trovano su indirizzi diversi.
    Ogni dato ha indirizzo elemento successivo ma anche elemento precedente.
            __________
        -->| ELEMENTO |-->
           |  LISTA   |
        <--|__________|<--
        
    La struttura dati ha l'obiettivo di memorizzare molti dati dello stesso tipo.
    
    Implementazione:
   
    stuct node {
        int value; //dato contenuto nel nodo
        struct node *next; //puntatore al nodo successore
    }
    
    int main(){
        stuct node *head = NULL; //ptr all'head della lista
        
        //nuovo nodo
        struct node *new_node;
        new_node = malloc(sizeof(struct node));
        
        //aggiorno la testa della lista
        head = new_node;
    }
