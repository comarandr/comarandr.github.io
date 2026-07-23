---
layout: default
title: Scheme
permalink: /linguaggi/scheme/
---


Scheme è un linguaggio di programmazione funzionale derivato da Lisp.

## Lambda

Definizione degli argomenti di una funzione: `(lambda (args) () )`

Definizione di una funzione: `(define (nome-funzione args) () )`

```scheme
(define (nomeFunzione arg1 arg2)
  (lambda (arg1 arg2)
    (corpo funzione)))

(define aggiungi 
  (lambda (n)
    (+ n 2)))

>> (aggiungi 3)
5
```

Definire una costante `(let)`: (let ((nome-costante valore-costante)) (corpo))

```scheme
(define (penultima-lettera
    (lambda (parola)
        (let ((k (- (string-length parola) 2)))
            (substring parola k (+ k 1))
        )))

>> (penultima-lettera "cane")
"n"
```

GENERATORE CASUALE: `(random integer)``

```scheme
>> (random 2)
0
>> (random 2)
1
>> (random 2)
0
```

generale valore fino a 0 a integer-1 (esempio se integer = 2 i valori possibili sono 0 e 1)

## Stringhe ("...")

Le stringhe sono racchiuse tra virgolette doppie `"stringa"`. Posso usare il simbolo `\"`come escape.
Per rappresentare il simbolo escape in una stringa devo raddoppiarlo `\\` &rarr; `\`

**giustapposizione** : `(string-append string1 string2 ...)`

```scheme
(string-append "ca" "ne")
"cane"

(string-append "ca")
"ca"
```

**estrapolazione**: `(substring "stringa1" "posizione primo incluso" "posizione primo escluso")`

```scheme
(substring "canarino" 0 6)
"canari"

(substring "canarino" 5)
"ino"
```

nota:

| C | A | N | A | R | I | N | O |
|---|---|---|---|---|---|---|---|
| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |

nota: `substring`ammette anche soltanto un valore, in tal caso estrae dalla posizione iniziale fino alla posizione finale

**lunghezza**: `(string-length "stringa")`

```scheme
(string-length "canarino")
8
```

**uguaglianza**: `(string=? "stringa1" "stringa2")`

```scheme
(string=? "cane" "cane" "cane")
#true

(string=? "cane" "gatto" "cane")
#false
```

**confronto lessicografico**: ordine alfabetico

-`(string<?)`
-`(string>?)`
-`(string<=?)`
-`(string>=?)`

```scheme
(string>? "aaaaaaa" "b")
#false

(string>? "z" "bzzz")
#true

(string<? "1011" "11")
#true
```

**estrapolazione di un carattere**: `(string-ref "stringa" posizione-carattere)`

```scheme
(string-ref "canarino" 6)
#\n
```

nota: carattere è diverso dalla stringa

**stringa di n caratteri #\c**: `(make-string n #\carattere)`

```scheme
(make-string 3 #\a)
"aaa"
```

**conversione a maiuscolo**: `(string-upcase "stringa")`

```scheme
(string-upcase "ciao")
"CIAO"
```

**conversione a minuscolo**: `(string-downcase "stringa")`

```scheme
(string-downcase "CIAO")
"ciao"
```

## Caratteri (#\carattere)

**identificazione carattere**: `char=? #\carattere1 #\carattere2` &rarr; booleano #true o #false

```scheme
(char=? #\2 #\3)
#false

(char=? #\2)
#true

(char=? "e")
char=?: expects a char, given "e"
```

NOTA: errore perché "e" è una stringa, accadrebbe lo stesso se usassi come argomento lo spazio vuoto senza precederlo con `#\`. Per rappresentare lo spazio vuoto posso usare `\#space``

**conversione a maiuscolo**: `(char-upcase #\carattere)`

```scheme
(char-upcase #\a)
#\A
```

**conversione a minuscolo**: `(char-downcase #\carattere)`

```scheme
(char-downcase #\A)
#\a
```

**confronto caratteri**: confronta gli integer dei caratteri secondo la tabella ASCII

- `char>?`
- `char<?`
- `char>=?`
- `char<=?`

```scheme
(char>? #\0 #\a)
#false

> char->integer #\0
48

> char->integer #\a
97
```

## Numeri

**operazioni**: `(operatore operando operando)` &rarr; valore

- `(+ 2 3 4 5 6 7)`
- `(* 2 4 67 109)`

**esponenziale generico**: `(expt base esponente)` &rarr; valore 

nota bene: `expt` ≠ `exp`
`exp`usa il numero di nepero $e$ come base

```scheme
(expt 2 3)
8
```

**esponenziale base $e$**: `(exp esponente)` &rarr; valore

```scheme
(exp 1)
#i2.7182818284... ~ approssimazione e
```

**radice quadrata**: `(sqrt radicando)` &rarr; valore

```scheme
(sqrt 4)
2
```

**confronti** `(confronto num1 num2)` &rarr; booleano #true o #false

- `(< num1 num2)`
- `(> num1 num2)`
- `(<= num1 num2)`
- `(>= num1 num2)`

```scheme
(> 3 3)
#false

(>= 3 3)
#true

(=> 3 3)
=>: this function is not defined
```

nota, va messo prima il maggiore o il minore!

**quoziente**: `(quotient dividendo divisore)` &rarr; valore

```scheme
(quotient 4 5)
0

(quotient 5 4)
1
```

Nota: $4 \div 5 = 0*5 + 4 \quad 5 \div 4 = 1*4 + 1$

**resto divisione**: `(remainder dividendo divisore)` &rarr; valore

```scheme
(remainder 4 5)
4

(remainder 5 4)
1
```

**valore assoluto**: `(abs valore)` &rarr; valore

```scheme
(abs -3)
3

(abs 3)
3
```

**massimo**: `(max num1 num2 ...)` &rarr; valore

```scheme
(max 3 4 5 6 7)
7  
```

**minimo**: `(min num1 num2 ...)` &rarr; valore

```scheme
(min 3 4 5 6 7)
3
```

**pari?**: `(even? num)` &rarr; booleano #true o #false

```scheme
(even? 4)
#true
```

**dispari?**: `(odd? num)` &rarr; booleano #true o #false

```scheme
(odd? 4)
#false  
```

## Booleani (\#true o \#false)

**not logico**: `(not C1)` &rarr; booleano

```scheme
(not (= 3 4))
#true

(not (= 3 3))
#false
```

**and logico**: `(and C1 C2 ...)` &rarr; booleano

```scheme
(and (= 3 2) (= 3 3))
#false

(and (= 3 3) (= 4 4))
#true
```

**or logico**: `(or C1 C2 ...)` &rarr; booleano

```scheme
(or (= 3 2) (= 3 3))
#true

(or (= 3 2) (= 1 0))
#false
```

**controllo di tipo**:

- `number?``
- `string?`
- `char?`
- `integer?`

**confronti tra numeri caratteri e stringhe**:

- `number=?`
- `string=?`
- `char=?`

## Conversioni di tipo

**integer a Carattere**: `(integer->char integer)` &rarr; carattere

```scheme
(integer->char 48)
#\0
```

**carattere a integer**: `(char->integer carattere)` &rarr; integer

```scheme
(char->integer #\0)
48
```

**stringa a lista**: `(string->list "stringa")` &rarr; lista di caratteri

```scheme
(string->list "cane")
(list #\c #\a #\n #\e)
```

**lista a stringa**: `(list->string (list #\c #\a #\n #\e))` &rarr; stringa

```scheme
(list->string (list #\c #\a #\n #\e))
"cane"
```

**stringa a numero**: `(string->number "stringa")` &rarr; numero

```scheme
(string->number "1234")
1234
```

**numero a stringa**: `(number->string numero)` &rarr; stringa

```scheme
(number->string 1234)
"1234"
```

**carattere a stringa**: `(string carattere)` &rarr; stringa

```scheme
(string #\b)
"b"
```

**stringa a carattere**: `(string-ref "stringa" posizione)` &rarr; carattere

```scheme
(string-ref "c" 0)
#\c
```

## Integer

Ordine di interi che corrispondono ai caratteri codificati (es. 48 corrisponde a `#\0`, 49 corrisponde a `#\1`, 50 corrisponde a `#\2` ecc.)

```scheme
(integer->char (+ (char->integer #\A) 1))
#\B

(integer->char (+ (char->integer #\5) 1))
#\6
```

## Costrutti

**if**; `(if (condizione? oggetto) (se vero) (se falso)) = (if C E1 E2)`

nota: se vale condizione si valuta soltanto E1

```scheme
(if true 0 1)
0

(if false 0 1)
1
```

**cond**: `(cond (C1 E1) (C2 E2) ... (Cn En))`

```scheme

(define numero
  (lambda (n)
    (cond ((> n 0) (string-append "positivo"))
          ((< n 0) (string-append "negativo"))
          ((= n 0) (string-append "zero"))
)))

>> (numero -58)
"negativo"
```

nota: con più condizioni vere si applica la prima; per includere tutti i casi posso terminare con (... (Else En))

## Liste (el1 el2 ... eln)

**lista vuota**: `null`

```scheme
>>null
'()
```

restituisce sempre la lista vuota, svolge la funzione di primitivo; utile per costruire liste di un elemento con `cons`

**null?**: `(null? lista)` &rarr; booleano #true o #false

```scheme
(null? '())
#true

(null? '(1 2 3))
#false 
```

**lista primo elemento**: `(car lista)` &rarr; primo elemento della lista

```scheme
(car '(1 2 3))
1
```

**resto della lista**: `(cdr lista)` &rarr; resto della lista

```scheme
(cdr '(1 2 3))
(2 3)
(cdr '(1))
'()
```

**secondo elemento lista**: `(cadr lista) = (car (cdr lista))` &rarr; secondo elemento della lista

```scheme
(cadr '(2 3 4))
3
```

**costruzione di una lista**: `cons el1 (cons el2 (... (cons eln lista) ...))` &rarr; lista

```scheme
cons 3 null
(list 3)

cons "cane" (cons #\0 (cons 3 null))
(list "cane" #\0 3)

(cons 3 (cons 4 5)
cons: second argument must be a list, but received 4 and 5
```

nota: il secondo argomento di `cons` deve essere una lista, altrimenti restituisce un errore

**costruzione di una lista con `list`**: `(list el1 el2 ... eln)` &rarr; lista

```scheme
list 2 "cane" (+ 3 4) (null? (list 3 4))
(list 2 "cane" 7 #false)
```

Notare che list nel caso del terzo elemento (+ 3 4) e del quarto elemento (null? (list 3 4)) valuta gli argomenti

**costruzione lista**: ‘(el1 el2 el3 …)

```scheme
‘(2 “cane” (null? ‘(3 4) ) )
(list 2 "cane" (list 'null? (list 'quote (list 3 4))))
```

La procedura ‘ non calcola le funzioni all’interno della lista

**numero elementi - lunghezza lista**: `(length lista1)`

```scheme
(length (list 5 6 7))
3
```

**elemento in posizione k**: `(list-ref lista1 k)` con 0 < k < (length lista1 – 1)

```scheme
(list-ref (list “cane” “gatto” “canarino” “kilo”) 3)
“kilo”
```

**unire liste**: `(append lista1 lista2 lista3 …)`

```scheme
(append (list "cane" #\k) (list 908 22) (list "44"))
(list "cane" #\k 908 22 "44")
```

**invertire ordine elementi lista**: `(reverse lista1)`

```scheme
(reverse (list "cane" #\k 908 22 "44"))
(list "44" 22 908 #\k "cane")
```

## ARGOMENTI PROCEDURALI

**applicare funzione a lista elementi**: `(map funzione lista)`

```scheme
(map (lambda (x) (* 2 x)) ‘(1 2 3 4 5))`
`(list 2 4 6 8 10)
```