---
layout: default
title: Fisica 2026
permalink: /fisica_2026/
---

## Introduzione

Fisica: descrizione dei fenomeni naturali attraverso modelli matematici.

Grandezze fisiche: entità osservabili nei fenomeni naturali a cui è possibile associare quantità matematiche.

Legge fisica: relazione tra almeno due grandezze fisiche

### Cinematica

#### Concetti fondamentali

**moto**: variazione di posizione nel tempo di un corpo rispetto ad altri corpi considerati fissi

**sistema di riferimento**: usato per descrivere il moto di un corpo

**traiettoria**: linea descritta da un punto materiale durante il suo moto

**Legge oraria**: relazione fra il tratto di traiettoria percorso $s$ e il tempo $t$

Il tratto di traiettoria percorso durante un moto è una quantità vettoriale detta spostamento $s$

#### Velocità

**velocità scalare media**: rapporto tra lo spazio percorso $s$ e l'intervallo di tempo $t$ impiegato a percorrerlo

$$
v_m = \frac{s(t_2)-s(t_1)}{t_2-t_1}
$$

**velocità istantanea**: limite della velocità media per $t_2 \to t_1$
$$
v = \lim_{\Delta t \to 0} \frac{s(t + \Delta t)-s(t)}{\Delta t} = \frac{ds}{dt}
$$

la velocità istantanea è la tangente

Calcolo dimensionale della velocità:

$$
[V] = \frac{[L]}{[T]}
$$

<img src="./vettoreVelocita.jpeg" height="230px">

$$
\vert \vec{v} \vert = \sqrt{v_x^2 + v_y^2}
$$

$$
\text{componente orizzontale } = \vert \vec{v_x} \vert = \vert \vec{v} \vert \cos \alpha
$$

$$
\text{componente verticale } = \vert \vec{v_y} \vert = \vert \vec{v} \vert \sin \alpha
$$

#### Accelerazione

variazione nel tempo della velocità

**accelerazione media**: rapporto tra la variazione di velocità $\Delta v$ e l'intervallo di tempo $\Delta t$ in cui avviene

$$
\vec{a_m} = \frac{\vec{v}(t_2)-\vec{v}(t_1)}{t_2-t_1}
$$

**accelerazione istantanea**: limite dell'accelerazione media per $t_2 \to t_1$

$$
\vec{a} =\frac{d\vec{v(t_1)}}{dt}
$$

calcolo dimensionale dell'accelerazione:

$$
[L][T]^{-2}
$$

#### Moti notevoli

**moto rettilineo**: la direzione della velocità è costante e coincidente con la traiettoria

**moto curvilineo**: il vettore accelerazione **non** è tangente alla traiettoria, ovvero possiede una componente, detta **normale**, perpendicolare alla traiettoria

##### Moto rettilineo uniforme

- traiettoria rettilinea
- $v$ costante in modulo
- $a = 0$

- legge oraria: $$x = x_0 + v_0t$$

##### Moto rettilineo uniformemente accelerato

- corpo parte da fermo e si muove in linea retta
- $a$ costante in modulo e direzione
- velocità varia soltanto in modulo

Se corpo non parte da fermo, l'importante è che $v_0$ abbia la stessa direazione di $a$.

$$
v = v_0 + at
$$

Legge oraria:

$$
x = x_0 + v_0t + \frac{1}{2}at^2
$$  

- grafico spazio-tempo: parabola
- grafico velocità-tempo: retta con coefficiente angolare $a$

##### Moto circolare uniforme

Moto di un punto $P$ che si muove a velocità $v$ con modulo costante e direzione variabile.

velocità lineare periferica: velocità con cui $P$ si muove lungo la circonferenza

velocità angolare $w$: velocità di rotazione del raggio $R$ nel seguire $P$

per definizione

$$
w = \frac {\Delta \theta}{\Delta t}
$$

velocità lineare periferica:

$$
v = wR
$$

accelerazione:

$$
a = v \omega = \frac{v^2}{R} = w^2 R
$$

accelerazione normale o **centripeta**: direzione perpendicolare alla traiettoria, verso il centro della circonferenza

##### Moto armonico

moto di un punto che percorre avanti e indietro con periodicità un segmento

legge oraria:

$$
x = A \sin (\omega t + \phi)
$$

con:

- $A$: ampiezza del moto
- $\omega$: pulsazione del moto
- $\phi$: fase iniziale del moto

La pulsazione $\omega$ è legata alla **frequenza** del moto, definita come numero di cicli per secondo:

$$
\omega = 2 \pi f
$$

L'inverso della frequenza è il **periodo** del moto, ovvero il tempo necessario a compiere un ciclo completo:

$$
T = \frac{1}{f} = \frac{2 \pi}{\omega}
$$

### Dinamica

#### Forze e leggi di Newton

studio del moto in relazione alle cause che lo generano, ovvero le **forze** (grandezze vettoriali)

Posso causare:

- variazione dello stato di moto (corpo non vincolato), misurata con metodo dinamico
- deformazione (corpo vincolato), misurata con metodo statico

**principio di relatività galileiana**: le leggi fisiche sono invarianti nei sistemi di riferimento inerziali

1. **principio di inerzia**: ogni corpo persiste nel suo stato di quiete o di moto rettilineo uniforme a meno che non sia costretto a cambiare stato da forze applicate
2. **principio fondamentale della dinamica**: la forza agente imprime al moto un'accelerazione proporzionale ad essa, con costante di proporzionalità pari alla massa del corpo

$$
\vec{F} = m \vec{a}
$$

3. **principio di azione e reazione**: a ogni forza di azione corrisponde una forza di reazione uguale in modulo, opposta in direzione e applicata su un corpo diverso

**Newton (N)**: unità di misura statica di forza, 1 Newton è la forza che imprime a un corpo di massa 1 kg un'accelerazione di 1 $m/s^2$

**Diagramma corpo libero**: rappresentazione grafica delle forze che agiscono su un corpo

### Quantità di moto

**quantità di moto**: prodotto tra massa e velocità di un corpo

$$
\vec{p} = m \vec{v}
$$

**Teorema della conservazione della quantità di moto**: in un sistema isolato, la quantità di moto totale è costante

Dato che $ p = m \cdot v$, possiamo riscrivere il secondo principio della dinamica come:

$$
\vec{F} = \frac{d\vec{p}}{dt}
$$

Quando agiscono forze esterne la variazione della quantità di moto nel tempo è uguale alla risultante delle forze esterne

### Termodinamica

### Elettromagnetismo

#### Elettrostatica

I fenomeni elettrici dipendono dalla propietà della materia di possedere **carica elettrica**, che può essere **positiva** o **negativa**.

- attrazione tra cariche di segno opposto
- repulsione tra cariche di segno uguale

**Principio di conservazione della carica elettrica**: carica elettrica di una quantità di materia è uguale alla somma algebrica delle cariche elementari che la costituiscono

#### Legge di Coulomb

(copilot) La forza elettrostatica tra due cariche puntiformi è direttamente proporzionale al prodotto delle cariche e inversamente proporzionale al quadrato della distanza che le separa:

$$
\vec{F} = K \frac{q_1 q_2}{r^2} \frac{\vec{r}}{r}
$$

**Coulomb (C)**: carica posta nel vuoto a distanza di 1 metro da una carica uguale ad essa 

$$ K = 8.99 \times 10^9 \frac{N \cdot m^2}{C^2} $$

### Entropia