---
layout: default
title: Fisica
permalink: /fisica/
---

## Fisica parte 1 - Cinematica

**RISULTATO DI MISURA**: $ x + \Delta x $

$x$ = valore di misura

$\Delta x$ = incertezza di misura

**MISURA INDIRETTA** $ Y = F(X_1, X_2, ... , X_n) $

$Y$ = grandezza derivata

$F$ = funzione

$X_1, X_2, ... , X_n$ = grandezze fisiche

**GRANDEZZE FONDAMENTALI**:

| Grandezza | Unità di misura | Simbolo |
| --- | --- | --- |
| Massa | chilogrammo | kg |
| Lunghezza | metro | m |
| Tempo | secondo | s |
| Temperatura | kelvin | K |
| Quantità di sostanza | mole | mol |
| Intensità di corrente | ampere | A |
| Intensità luminosa | candela | cd |

**CALCOLO DIMENSIONALE**:

omogenee = stesse dimensioni

- $A = B\ \iff\ [A] = [B]$ omogenee
- $A+B\ \iff\ [A] = [B]$ omogenee
- $[A\cdot B]\ \iff\ [A]\cdot[B]$ prodotto di dimensioni
- $[\Pi] \iff 1$ costanti sono adimensionali

**CIFRE SIGNIFICATIVE**:

$S: (97 \pm 1)m$

$\Delta T = (22 \pm 1)m$

| $ S \Delta T $ | 21 | 23 |
| --- | --- | --- |
| 96 | 4.571... | 4.173... |
| 98 | 4.619... | 4.217... |

$Vm$ varia da 4.619 - 4.173 = 0.446

**errore massimo assoluto**:

$Vm = (4.409... \pm 0.223...) m/s$

$ Vm = (4.4 \pm 0.2) m/s$

$0.2$ ordine grandezza errore

**NOTAZIONE SCIENTIFICA ED ERRORI**:

$250 \pm 10$ &rarr; $(2.50 \pm 0.10) \cdot 10^2$

$30.0 \pm 0.2$ &rarr; $(3.00 \pm 0.02) \cdot 10^1$

$0.0005 \pm 0.001$ &rarr; $(5 \pm 1) \cdot 10^{-3}$

**CIFRE SIGNIFICATIVE OPERAZIONI**:

- **SOMMA**: $A=2.5 \cdot 10^2 , B=30.0$ &rarr; $ A+B = 2.8 \cdot 10^2 $

  notare ordine di grandezza di $A$ sono le decine, di $B$ sono i decimi

- **PRODOTTO**: $A=2.5 \cdot 10^2 , B=30.0$ &rarr; $ A\cdot B = 7.5 \cdot 10^3 $

  notare che $A$ ha 2 cifre significative, $B$ ne ha 3, quindi il risultato avrà 2 cifre significative

- **FUNZIONE UNARIA**: $A=2.5 \cdot 10^2$ &rarr; $ \sqrt{A} = 1.6 \cdot 10^1 $

  notare che $A$ ha 2 cifre significative, quindi il risultato avrà 2 cifre significative

### CINEMATICA

**CINEMATICA**: descrizione del moto dei corpi

**POSIZIONE**: relativa a un PUNTO DI RIFERIMENTO

**ASSE COORDINATO**:

$P = x = \vec{OP}$

$ \vert \vec{OP'} \vert = \vert \vec{OP} \vert $

<img src="AsseCoordinato.jpeg" alt="Asse Coordinato" width="400"/>

$ x \text{ posizione} \begin{cases} \vert \vec{OP} \vert \text{ se } \vec{OP}  \text{ concorde nel verso positivo} \\\\ - \vert \vec{OP} \vert \text{ se } \vec{OP} \text{ discorde nel verso positivo} \end{cases} $

**DUE DIMENSIONI**:

#### Legge oraria del moto

descrive la posizione in un dato istante

<img src="leggeOraria.jpeg" alt="Legge Oraria" width="400"/>

#### Moto rettilineo uniforme

intervalli di tempo uguali = spostamenti uguali

LEGGE ORARIA:

$$x(t) = At + x_0$$

$x_0$: posizione iniziale

$t$: istante di tempo

$A$: costante di proporzionalità

$n\Delta x=A \cdot n\Delta t$ &nbsp; &nbsp; con $n$ numero di istanti

VELOCITÀ MEDIA: $$v_m = \frac{\Delta x}{\Delta t}$$

VELOCITÀ ISTANTANEA: $$v = \lim_{\Delta t \to 0} \frac{\Delta x}{\Delta t}$$

<img src="rettilineoUniforme.jpeg" alt="Rettilineo Uniforme" width="500"/>

#### Moto rettilineo uniformemente accelerato

accelerazione costante, velocità aumenta linearmente

$v(t) = Bt + v_0$

$a_m = \frac{\Delta v}{\Delta t}$

$v(t) = a_m t + v_0$

**ACCELERAZIONE MEDIA**: $$a_m = \frac{\Delta v}{\Delta t}$$

**ACCELERAZIONE ISTANTANEA**: $$a(t) = \lim_{\Delta t \to 0} \frac{\Delta v}{\Delta t} = \frac{dv(t)}{dt}$$

<br>

<img src="uniformementeAccelerato.jpeg" alt="Uniformemente Accelerato" width="800"/>

#### IN BREVE

**SPAZIO**: legge oraria $x = x(t)$

**VELOCITÀ**: derivata della legge oraria $v = \frac{dx}{dt}$

**ACCELERAZIONE**: derivata della velocità $a = \frac{dv}{dt} = \frac{d^2x}{dt}$

#### Interludio matematico

basi di matematica

#### Moto uniformemente accelerato

| 1 dimensione | |
| --- | --- |
| legge oraria: | $$ x(t) = \frac{1}{2} a_0 t^2 + v_0 t + x_0 $$ |
| velocità: | $$ v(t) = a_0 t + v_0 $$ |
| accelerazione: | $$ a(t) = a_0 $$ |

| 2 dimensioni | |
| --- | --- |
| legge oraria: | $$ \vec{r}(t) = \frac{1}{2} \vec{a_0} t^2 + \vec{v_0} t + \vec{r_0} $$ |
| velocità: | $$ \vec{v}(t) = \vec{a_0} t + \vec{v_0}$$ |
| accelerazione: | $$ \vec{a}(t) = \vec{a} $$ |

Scegliamo asse y parallelo ad $a_0$

In questo modo scomponiamo il moto in due moti indipendenti:

- componente $ P_y $: moto uniformemente accelerato
- componente $ P_x $: moto rettilineo uniforme

Ottenendo quindi 

$$
\begin{cases}
x(t) = v_{0x} t + x_0 \\\\
y(t) = \frac{1}{2} a_0 t^2 + v_{0y} t + y_0
\end{cases}
$$

#### Moto armonico

La legge oraria del moto armonico è:

$$
x(t) = x_0 \cos(\omega t + \varphi_0)
$$

ed è caratterizzata dai 3 parametri:

- $x_0$: ampiezza del moto
- $\omega$: frequenza angolare o pulsazione
- $\varphi_0$: fase iniziale

##### $\omega_0$: pulsazione

La posizione in $ t $ e in $ t+T $ deve essere la stessa, per definizione di periodo $T$.
Poichè $\cos$ ha periodo $2\pi$, si ricava la seguente relazione:

$$
\omega_0 T = 2\pi \qquad T = \frac{2\pi}{\omega_0} \qquad \omega_0 =\frac{2\pi}{T}
$$

##### $x_0$: ampiezza

$x(t)$ oscilla tra $-x_0$ e $x_0$. Questo si può facilmente dimostrare considerando $ x = x_0 \cos(\omega t + \varphi_0) $, in quanto la funzione $\cos$ oscilla tra -1 e 1 indipendentemente dall'argomento.

$$
x_{\max} = x_0 \cdot \cos_{\max} = x_0 \cdot 1 = x_0 \\\\
x_{\min} = x_0 \cdot \cos_{\min} = x_0 \cdot (-1) = -x_0
$$

##### $\varphi_0$: fase iniziale

disallineamento della funzione rispetto all'origine degli istanti di tempo. Poichè la funzione è
$$
x(t) = x_0 \cos(\omega_0 t + \varphi_0) \\\\ x = x_0 \cos(\alpha + k)
$$
possiamo facilmente osservare che $\varphi_0 = k$ indica il disallineamento rispetto allo zero del coseno ponendo $t=0$.

##### Velocità del moto armonico

Poichè abbiamo $x(t) = x_0 \cos(\omega_0 t + \varphi_0)$, possiamo ricavare la velocità derivando la legge oraria:
$$
v(t) = \frac{dx}{dt} = -\omega_0 x_0 \sin(\omega_0 t + \varphi_0)
$$

Osservo attentamente che:

- ampiezza dipende dalla pulsazione: $-x_0 \omega_0, +x_0 \omega_0$
- fase invariata: $\varphi_0$
- periodo invariato: $T = \frac{2\pi}{\omega_0}$

##### Accelerazione del moto armonico

Analogamente, ricaviamo l'accelerazione derivando la velocità:

$$
a(t) = -\omega_0^2 \cdot x_0 \cos(\omega_0 t + \varphi_0) = -\omega_0^2 \cdot x(t)
$$

Noto : $x_0 \cos(\omega_0 t + \varphi_0) = x(t)$

Osserviamo che:

- ampiezza dipende dalla pulsazione: $-x_0 \omega_0^2, +x_0 \omega_0^2$
- fase invariata: $\varphi_0$
- periodo invariato: $T = \frac{2\pi}{\omega_0}$

L'accelerazione è **proporzionale** alla posizione del corpo.

##### Relazione $ x^2 \omega_0^2 + v^2 $

Considerando la quantità $ x^2 \omega_0^2 + v^2 $, sostituiamo $x$ e $v$ con le rispettive leggi orarie:

$$
x^2 \omega_0^2 + v^2 = x_0^2 \omega_0^2
$$

ovvero una quantità che rimane costante nel moto, conservandosi.

#### Moto circolare

moto che avviene lungo una circonferenza di raggio $R$ con centro in $O$.

La legge oraria risulta pertanto essere:

$$
\Theta = \theta t
$$

in un moto essenzialmente unidimensionale, con

- velocità angolare $\theta$ costante
- posizione angolare $\Theta$ che varia linearmente con il tempo

##### Moto circolare uniforme