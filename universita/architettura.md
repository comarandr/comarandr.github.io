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

| Tabella Byte |
| --- |
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

