---
layout: default
title: Java
permalink: /linguaggi/java
custom_css: /assets/oop.css
---

## Basi di java

il tipo di dato è statico, quindi va dichiarato prima di essere usato.

### Classi

Usate per:

- definire nuovi tipi di oggetti
- collezione di metodi

Di base è uno schema che definisce COME gli oggetti/le istanze sono fatti e COME possono essere usati.

```java
public class A extends B {
    //corpo classe A
}
```

### Interfacce

Usate per:

- definire nuovi tipi di oggetti

Di base è una classe con solo metodi astratti (senza corpo) e costanti.

```java
public interface A extends B {
    //corpo interfaccia A
}
```

### Elementi di una classe

costruttore: metodo per creare un'istanza della classe. Ha il nome della classe. Possono esserci più costruttori con parametri diversi (overloading)

progetto: insieme di classi e interfacce

classi: insiemi di metodi, procedure, dati, oggetti

metodo: procedura

variabili d'istanza: variabili che appartengono all'oggetto, rappresentate in ciascuno degli oggetti che istanziano una classe

### Operatori

#### Operatori aritmetici

`+` : addizione

`-` : sottrazione

`*` : moltiplicazione

`/` : divisione

`%` : modulo (resto della divisione)

#### Operatori di confronto

`==` : uguale a

`!=` : diverso da

`>` : maggiore di

`<` : minore di

`>=` : maggiore o uguale a

`<=` : minore o uguale a

#### Operatori logici

`&&` : AND logico

`||` : OR logico

`!` : NOT logico

#### Operatori lativi

`++` : incremento di 1

`--` : decremento di 1

#### Operatori lambda

`->` : separa i parametri dalla funzione

### Costrutti

#### Costrutto IF

```java

if (boolean){
    return //se la condizione è vera
} else {
    return //se la condizione è falsa
}
```

#### Costrutto IF-ELSE IF

```java
if (boolean1){
    return //se la condizione1 è vera
} else if (boolean2){
    return //se la condizione2 è vera
} else {
    return //se nessuna condizione è vera
}
```

#### Costrutto WHILE

```java
while (boolean){
    instruction //esegue il blocco finché la condizione è vera
}
```

ovviamente se instruction = return, il ciclo si interrompe.

#### Costrutto DO-WHILE

```java
do {
    instruction //esegue il blocco almeno una volta
} while (boolean);
```

#### Costrutto FOR

```java
for (inizializzazione; condizione; incremento){
    instruction //esegue il blocco finché la condizione è vera
}
```

inizializzazione: prima volta
incremento: dopo ogni iterazione

#### Costrutto RETURN

permette di restituire un valore all'esterno

```java
return //esce dal metodo e restituisce il valore
```

#### Costrutto SWITCH

```java
switch (variabile) {
    case valore1:
        instruction1 //esegue il blocco se variabile = valore1
        break; //esce dal costrutto
    case valore2:
        instruction2 //esegue il blocco se variabile = valore2
        break; //esce dal costrutto
    default:
        instruction3 //esegue il blocco se variabile != valore1 e variabile != valore2
}
```

#### Costrutto THROW

```java
throw new Exception("messaggio di errore"); //genera un'eccezione e interrompe l'esecuzione del programma
```

#### Costrutto TRY-CATCH-FINALLY

```java
try {
    instruction //esegue il blocco e se c'è un errore passa al catch
} catch (Exception e) {
    instruction //esegue il blocco se c'è un errore nel try
} finally {
    instruction //esegue il blocco sempre, sia se c'è un errore che se non c'è (opzionale)
}
```

### Espressioni lambda

```java
(parametri) -> { //blocco di codice }
```

esempio:

```java
(x, y) -> { return x + y; }

Predicate<Integer> isEven = num -> num % 2 == 0
```

### Tipi di variabili

#### Tipi primitivi

`boolean`: `#true`, `#false`

`int`: numeri interi
`long`: numeri interi $\in \mathbb{Z}$
`float`: numeri decimali $\in \mathbb{R}$
`double`: numeri decimali $\in \mathbb{R}$

`char`: caratteri singoli ASCII

#### Oggetti

##### Oggetti wrapper

Convertono i tipi primitivi in oggetti. Questo serve per poter sfruttare metodi di utilità (es. conversione stringhe) e per inserirli in strutture dati (es. Collection, Map, List, Set)

`boolean` &rarr; `Boolean`

`int` &rarr; `Integer`
`long` &rarr; `Long`
`float` &rarr; `Float`
`double` &rarr; `Double`

`char` &rarr; `Character`

I wrapper possono assumere valore `null`

##### String

insieme di caratteri, immutabile, può essere concatenata con `+`

###### metodi:

`.length()`: restituisce la lunghezza della stringa

`.equals(String s)`: confronta due stringhe per uguaglianza

`.charAt(int i)`: restituisce il carattere alla posizione i

`.substring(int i, int j)`: restituisce la sottostringa da i a j-1

`.concat(String s)`: concatena due stringhe

`.equalsIgnoreCase(String str)`: confronta due stringhe per uguaglianza ignorando il case

`.toUpperCase()`: restituisce la stringa in maiuscolo

`.toLowerCase()`: restituisce la stringa in minuscolo

```java
String s = "ciao";
```

##### Array

Un array generico si definisce come segue:

`tipo[] nomeArray = new tipo[dimensione];`

il tipo può essere un tipo primitivo o un oggetto

- accesso lettura: `... = nome[i]`
- accesso scrittura: `nome[i] = valore`

Array in cui definisco oggetti: `{elemento1, elemento2, elemento3, ...}`

Array in più dimensioni:

- `tipo[][] nomeArray = new tipo[dimensione1][dimensione2];`
- `a = { {el11, el12}, {el21, el22} }`

##### List

Collezione di oggetti ordinata, può contenere duplicati (es. `ArrayList`, `LinkedList`)

`.add(E e)`: aggiunge un elemento alla collezione

`.remove(E e)`: rimuove un elemento dalla collezione

`.get(int i)`: restituisce l'elemento alla posizione i

`.set(int i, E e)`: sostituisce l'elemento alla posizione i con un nuovo elemento

`.contains(E e)`: verifica se un elemento è presente nella collezione

`.size()`: restituisce il numero di elementi nella collezione

##### Set

Collezione di oggetti senza duplicati

`.add(E e)`: aggiunge un elemento alla collezione

`.remove(E e)`: rimuove un elemento dalla collezione

`.contains(E e)`: verifica se un elemento è presente nella collezione

`.size()`: restituisce il numero di elementi nella collezione

##### Map

Collezione di coppie chiave-valore, le chiavi sono univoche

`.put(K key, V value)`: aggiunge una coppia chiave-valore alla collezione

`.get(K key)`: restituisce il valore associato ad una chiave

`.remove(K key)`: rimuove una coppia chiave-valore dalla collezione

`.containsKey(K key)`: verifica se una chiave è presente nella collezione

`.containsValue(V value)`: verifica se un valore è presente nella collezione

`.size()`: restituisce il numero di coppie chiave-valore nella collezione

##### Predicate (BiPredicate)

Accetta un argomento e restituisce un booleano, utile per filtrare collezioni

`.test(T t)`: verifica se l'argomento soddisfa la condizione del predicato

Nel caso di BiPredicate, accetta due argomenti e restituisce un booleano

`.test(T t, U u)`: verifica se i due argomenti soddisfano la condizione del predicato

`.and(Predicate other)`: restituisce un predicato che rappresenta la congiunzione logica di questo predicato e di un altro

`.or(Predicate other)`: restituisce un predicato che rappresenta la disgiunzione logica di questo predicato e di un altro

`.negate()`: restituisce un predicato che rappresenta la negazione logica di questo predicato

##### Queue

Collezione di oggetti con accesso FIFO (First In First Out).
Interfaccia, solitamente le implementazioni più comuni sono `LinkedList` e `PriorityQueue`.

*Inserimento*: Aggiunge un elemento alla fine (coda) della struttura

`.add(E e)`: aggiunge un elemento alla coda

`.offer(E e)`: aggiunge un elemento alla coda, restituisce false se non è possibile aggiungerlo

*Estrazione*: Rimuove e restituisce l'elemento in cima (testa)

`.remove()`: rimuove l'elemento in testa alla coda

`.poll()`: restituisce null se la coda è vuota, altrimenti rimuove e restituisce l'elemento in testa alla coda

*Ispezione*: Restituisce l'elemento in cima senza rimuoverlo

`.element()`: restituisce l'elemento in testa alla coda senza rimuoverlo, lancia un'eccezione se la coda è vuota

`.peek()`: restituisce l'elemento in testa alla coda senza rimuoverlo

`.isEmpty()`: verifica se la coda è vuota

##### Stream

Collezione di oggetti che permette di eseguire operazioni in sequenza (pipeline) su di essi, senza modificarli.

`.filter(Predicate p)`: restituisce un nuovo stream con gli elementi che soddisfano il predicato p

`.map(Function f)`: restituisce un nuovo stream con gli elementi trasformati dalla funzione f

`.forEach(Consumer c)`: esegue l'operazione c su ogni elemento dello stream

`.collect(Collector c)`: raccoglie gli elementi dello stream in una collezione o in un altro tipo di risultato

`.reduce(BinaryOperator op)`: riduce gli elementi dello stream ad un singolo valore utilizzando l'operatore binario op

```java
List<Integer> numeri = Arrays.asList(1, 2, 3, 4, 5, 6);

numeri.stream()           // 1. Sorgente
    .filter(n -> n % 2 == 0)  // 2. Operazione intermedia
    .map(n -> n * 2)          // 2. Operazione intermedia
    .forEach(System.out::println); // 3. Operazione terminale
    }
}

numeri.stream().filter().map().forEach();
// sorgente -> pari ->  * 2 -> stampa
```

##### Stack

Collezione di oggetti con accesso LIFO (Last In First Out)

`.push(arg)`: aggiunge arg in cima alla collezione

`.pop(arg)`: rimuove arg in cima alla collezione

`.peek()`: restituisce l'elemento in cima alla collezione senza rimuoverlo

`.empty()`: verifica se la collezione è vuota

#### Confronto == e .equals()

`==` : confronta due oggetti per riferimento (stesso oggetto in memoria), ottimo per primitivi

`.equals()`: confronta due oggetti per valore (stesso contenuto)

`=` : assegna un valore ad una variabile