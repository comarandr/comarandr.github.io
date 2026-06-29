---
layout: default
title: Architettura degli elaboratori
permalink: /universita/architettura/
---

## Introduzione e definizioni

**Architettura di calcolo**: macchina capace di eseguire una sequenza di *istruzioni macchina*

**Programma**: *sequenza* di istruzioni macchina

**CPU(Central Processing Unit)**: componente che fisicamente esegue le istruzioni macchina

**Memoria principale**: dove risiedono programmi e dati su cui i programmi lavorano mentre vengono elaborati dla processore

**Memoria di massa**: dove risiedono i *file*, strutture in cui vengono preservati i programmi e dati ad architettura spenta

**Circuiti integrati**: circuiti contenuti dentro un *chip*. Adoperati per realizzare CPU e RAM

**Bit**: elemento base capace di assumere *2 configurazioni* stabili.

**Byte**: giustapposizione di 8 bit.

| Tabella Byte                                  |
| :-------------------------------------------: |
|**KB** (Kilobyte) = $2^{10}$ Byte ~ $10^3$ Byte|
|**MB** (Megabyte) = $2^{20}$ Byte ~ $10^6$ Byte|
|**GB** (Gigabyte) = $2^{30}$ Byte ~ $10^9$ Byte|

La memoria si ottiene giustapponendo più byte (e quindi bit)

Per accedere ai dati nella memoria bisogna individuarli, ovvero trovare la loro posizione. Perciò è necessario che siano indirizzati.

L'**indirizzamento** più efficiente è quello che adopera $n$ bit per indirizzare $2^n$ byte.

- es: se hai 2 byte (= $2^1$), basta 1 bit di indirizzamento:
  - un byte va in posizione con bit = 0
  - l'altro byte va in posizione con bit = 1

## Algebra Booleana

Si basa su due valori:

- 0 = falso
- 1 = vero

Operazioni fondamentali:

- \+ OR $\vee$
- \* AND $\wedge$
- \! NOT $\neg$

### Tabelle di verità

| A | B | A+B |
|:---:|:---:|:---:|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

| A | B | A*B |
|:---:|:---:|:---:|
|0|0|0|
|0|1|0|
|1|0|0|
|1|1|1|

| A | $\bar{A}$ |
|:---:|:---:|
|0|1|
|1|0|

Nota bene: una tabella di verita

- $k$ input = $k$ colonne
- $2^k$ righe

Data una tabella di verità, posso procedere in 2 modi:

- metodo algoritmico
- metodo duale

### Metodo algoritmico

tabella di $k$ colonne e $2^k$ righe

- considero le righe con output = 1
- ogni riga è una porta AND (prodotto input) in cui neghi gli input che valgono 0
- unisco tutto in una porta OR (sommo i prodotti)

### Metodo duale

tabella di $k$ colonne e $2^k$ righe

- considero le righe con output = 0
- ogni riga è una porta OR (somma input) in cui neghi gli input che valgono 1
- unisco tutto in una porta AND (moltiplico le somme)

### Operazioni dell'algebra

Posso ulteriormente semplificare le espressioni ottenute con i metodi precedenti, adoperando le seguenti proprietà:

| Proprietà | Or | And |
|:---:|:---:|:---:|
| Elemento nullo | $A + 0 = A$ | $A \cdot 0 = 0$ |
| Identità | $A + 1 = 1$ | $A \cdot 1 = A$ |
| Idempotenza | $A + A = A$ | $A \cdot A = A$ |
| Inverso | $A + \bar{A} = 1$ | $A \cdot \bar{A} = 0$ |
| Commutativa | $A + B = B + A$ | $A \cdot B = B \cdot A$ |
| Associativa | $A + (B + C) = (A + B) + C$ | $A \cdot (B \cdot C) = (A \cdot B) \cdot C$ |
| Distributiva | $A \cdot (B + C) = A \cdot B + A \cdot C$ | $A + (B \cdot C) = (A + B) \cdot (A + C)$ |
| Assorbimento | $A + (A \cdot B) = A$ | $A \cdot (A + B) = A$ |
| De Morgan | $\overline{A + B} = \bar{A} \cdot \bar{B}$ | $\overline{A \cdot B} = \bar{A} + \bar{B}$ |
|Negazione doppia| $\overline{\bar{A}} = A$ |
| $ \overline{ABC} \neq $ $\bar{A}\bar{B}\bar{C}$ |

### Porte NAND e NOR

**NAND**: $\overline{A \cdot B}$

|A|B|$\overline{A \cdot B}$|
|:---:|:---:|:---:|
|0|0|1|
|0|1|1|
|1|0|1|
|1|1|0|

**NOR**: $\overline{A + B} = \bar{A} \cdot \bar{B}$

|A|B|$\overline{A + B}$|
|:---:|:---:|:---:|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|0|

Nota bene: 
$\overline{AB}$ = NAND
$\overline{A} \cdot \overline{B}$ = NOR

### Porte OR esclusivo (XOR e NXOR)

$A \overline{B} + \overline{A}B = (A+B)(\overline{A}+\overline{B})$

|A|B|XOR|
|:---:|:---:|:---:|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|

$AB + \overline{A}\overline{B} = \overline{(A+B)(\overline{A}+\overline{B})}$

|A|B|NXOR|
|:---:|:---:|:---:|
|0|0|1|
|0|1|0|
|1|0|0| 
|1|1|1|

### Mappe di Karnaugh

(...)

## Circuiti combinatori

### Circuiti logici di base

## Numeri binari

**Notazione posizionale**: ogni cifra ha un peso che dipende dalla sua posizione

$$
\sum_{i=0}^{n-1} d_i \cdot B^i \qquad 0 \leq d_i < B
$$

binario: 

| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |

**Alfabeto esadecimale**:

$$
0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F
$$

### Conversione da base B a base 10

**Notazione posizionale**:

$$
\sum_{k=-m}^{q} d_k \cdot B^k = d_q \cdot B^q + ... + d_{-m} \cdot B^{-m}
$$

es:
$$
1011_2 = 1 \cdot 2^3 + 0 \cdot 2^2 + 1 \cdot 2^1 + 1 \cdot 2^0 = 8 + 0 + 2 + 1 = 11
$$

**Accumulazione parte intera**: accumulo progressivamente il peso delle cifre nella sequenza

[immagine]

**Accumulazione parte frazionaria**: accumulo progressivamente il peso delle cifre nella sequenza

[immagine]

$B \rarr 10$ = Accumulazione parte intera + Accumulazione parte frazionaria

### Conversione da base 10 a base B

(...)

### Codifiche $\mathbb{Z}$

- **Segno e valore assoluto**: 1 bit per segno + valore binario

  $+9 = 00001001_2$
  $-9 = 10001001_2$

- **Complemento a 1**: cambio di segno negando (complementando) i bit

  $+9 = 00001001_2$
  $-9 = 11110110_2$

- **Complemento a 2**: cambio di segno complementando i bit e sommando 1

  $+9 = 00001001_2$
  $-9 = 11110111_2 \quad (11110110 + 00000001)$

- **Eccesso N**: zero puntato su N
  
  es: N = 128 &rarr; $10000000_2$
  +1 = $10000001_2$
  +0 = $10000000_2$
  -1 = $01111111_2$

- **Complemento a 2 a N bit**:

  - $[0, 2^N - 1]$ notazione binaria
  - $[-1, 2^N - 2]$ nego bit valore assoluto e aggiungo 1
  - $-i = 2^N - i \;$ -(i-esimo) in notazione binaria

  es N = 8
  $-1 = 11111111_2$ (11111110 + 00000001, complemento 1 + 1)
  $-2 = 11111110_2$ (11111101 + 00000001)
  $-2^{N-1} = -2^7 = 10000000_2$ (01111111 + 00000001)

  passo da $N$ a $M$ bit aggiungendo $M-N$ bit

### Operazioni