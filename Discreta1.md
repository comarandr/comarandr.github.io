# Matematica discreta

## Indice

1. [Contare](#contare)
2. [Insiemi](#insiemi)
3. [Relazioni](#relazioni)
4. [Funzioni](#funzioni)
5. [Induzione](#induzione)
6. [Sommatorie](#sommatorie)
7. [Probabilità](#probabilità)
8. [Matematica degli interi](#matematica-degli-interi)
9. [Segno permutazioni (parità e disparità)](#segno-permutazioni-parità-e-disparità)
10. [Principio della piccionaia](#principio-della-piccionaia)
11. [Principio di somma e del prodotto](#principio-di-somma-e-del-prodotto)
12. [Principio di inclusione-esclusione](#principio-di-inclusione-esclusione)
13. [Teoria dei Grafi](#teoria-dei-grafi)

## Contare

## Insiemi

**Insieme**: concetto porimitivo, collezione di oggetti detti elementi
**Cardinalità $|A|$**: numero di elementi di un insieme $A$
**Insieme vuoto $\emptyset$**: insieme senza elementi, $|\emptyset| = 0$
**A sottoinsieme di B**: $A \subseteq B$ se ogni elemento di A è anche in B
**prodotto cartesiano $A \times B$**: insieme di tutte le coppie $(a, b)$ con $a \in A$ e $b \in B$

## Relazioni

**riflessiva**: $x \smile x\ \forall x$
**antiriflessiva**: $\neg (x \smile x)\ \forall x$

**simmetrica**: $x \smile y \implies y \smile x$
**antisimmetrica**: $x \smile y\ \implies \neg (y \smile x)$

**transitiva**: $(x \smile y) \land (y \smile z) \implies (x \smile z)$

**D'ORDINE**: irriflessiva, antisimmetrica e transitiva
**D'EQUIVALENZA**: riflessiva, simmetrica e transitiva

Le relazioni d'equivalenza implicano una partizione dell'insieme in classi di equivalenza

### Congruenza modulo $n$ $x \equiv_n y$

Resto della divisione intera tra due numeri

$12 \mod 3 = 0$ | $-12 \mod 3 = 0$
$13 \mod 3 = 1$ | $-13 \mod 3 = 2$
$14 \mod 3 = 2$ | $-14 \mod 3 = 1$

dato $x \equiv_n y$ allora:

- $x-y \equiv_n 0$
- $x + z \equiv_n y + z$
- $x \cdot z \equiv_n y \cdot z$

considerando anche $z_1 \equiv_n z_2$:

- $x+z_1 \equiv_n y+z_2$
- $x \cdot z_1 \equiv_n y \cdot z_2$

