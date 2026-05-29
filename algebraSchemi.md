---
layout: default
title: Algebra lineare
permalink: /algebraLineare/
---


## Indice

1. [Spazi vettoriali](#spazi-vettoriali)
2. [Basi e dimensione](#basi-e-dimensione)
3. [Applicazioni lineari](#applicazioni-lineari)
4. [Sistemi lineari](#sistemi-lineari)
5. [Autovettori e autovalori](#autovettori-e-autovalori)

## operazioni

- n-pla: $(a_1, \ldots, a_n)$

- somma:

$$
(a_1 a_2 a_3) + (b_1 b_2 b_3) = (a_1 + b_1, a_2 + b_2, a_3 + b_3)
$$

- prodotto con scalare:

$$
\lambda \cdot (a_1 a_2 a_3) = (\lambda \cdot a_1, \lambda \cdot a_2, \lambda \cdot a_3)
$$

- prodotto scalare:

$$
<v \cdot w> = v_1 \cdot w_1 + v_2 \cdot w_2 + v_3 \cdot w_3
$$

- norma (radice del prodotto scalare di sè stesso):

$$
||v|| = \sqrt{v_1^2 + v_2^2 + v_3^2} = \sqrt{<v \cdot v>}
$$

- distanza (radice della norma della differenza):

$$
d(v, w) = \sqrt{(v_1 - w_1)^2 + (v_2 - w_2)^2 + (v_3 - w_3)^2} = \sqrt{||v - w||}
$$

- disuguaglianza triangolare:

$$
||a + b|| \leq ||a|| + ||b||
$$

- disuguaglianza di Cauchy-Schwarz:

$$
|\sum_{i=1}^n a_i \cdot b_i| \leq ||a|| \cdot ||b||
$$

$$
|<a \cdot b>| \leq ||a|| \cdot ||b||
$$

## formulette geometriche

**rette passanti per $O$**: $\mathcal{L}(v) = \{\lambda v : \lambda \in \mathbb{R}\}$ $\lambda$ parametro
**ortogonalità**: $<a \cdot b> = 0$ prodotto scalare nullo
**angolo tra due n-ple**:

$$
\alpha = arcos( \frac{<a \cdot b>}{||a|| \cdot ||b||})
$$

**rete affini**: $\mathcal{L}(v) + w = \lambda v + w \quad \forall \lambda \in \mathbb{R}$
**retta per 2 punti**: $ (1 -\lambda)P = \lambda Q : (\lambda (P-Q) + P) $
**combinazione affine**: $\alpha P + \beta Q \mid \alpha + \beta = 1 $
**combinazione connessa**: $\alpha P + \beta Q \quad \alpha , \beta \in [0,1] \; \land \; \alpha + \beta = 1 $

## Risoluzioni geometria dello spazio

**equazione retta**: $\begin{cases} x = v_1 \cdot t + p_1 \\ y = v_2 \cdot t + p_2 \\ z = v_3 \cdot t + p_3 \end{cases}$

$t(v_1 v_2 v_3) + (p_1 p_2 p_3)$

**retta per $2$ punti**: $ t(B-A) + A $

$\begin{cases} x = (b_1 - a_1) \cdot t + a_1 \\ y = (b_2 - a_2) \cdot t + a_2 \\ z = (b_3 - a_3) \cdot t + a_3 \end{cases}$

**spazio perpendicolare a $v (v_1 v_2 v_3)$**: $<v, x> = 0$
NB: in $\mathbb{R}^2$ è una retta

**spazio perpendicolare a $v (v_1 v_2 v_3)$ e passante per $P$**: $<v, x> = <v, P>$

**equazione del piano**: $\pi : ax + by + cz = d$

**retta perpendicolare al piano $\pi$**: $v = (a,b,c)$ perpendicolare al piano $\pi : ax + by +cz =d$
NB componenti vettori uguali a coefficienti piano

**retta passante per un punto $P(p_x, p_y, p_z)$ ovvero traslazione**: $d = a \cdot p_x + b \cdot p_y + c \cdot p_z$
$ax + by + cz = a \cdot p_x + b \cdot p_y + c \cdot p_z$

**piano contenente $2$ rette**: $\begin{cases} x = v_1 \cdot t + w_1 \cdot s \\ y = v_2 \cdot t + w_2 \cdot s \\ z = v_3 \cdot t + w_3 \cdot s \end{cases}$
forma parametrica da risolvere per ottenere forma cartesiana

**retta in $\mathbb{R}^2$ dati $2$ piani**: $r: \begin{cases} a_1 x + b_1 y + c_1 z = d_1 \\ a_2 x + b_2 y + c_2 z = d_2 \end{cases}$
parametrica (porre una variabile pari a t)

**rette parallele** $t(v_1 v_2 v_3) + Q; \quad s(v_1 v_2 v_3) + P $
stesso vettore direttore

**piano date due rette parallele**: serve un'altra direzione

**piano data una retta $r$ e un punto $A$**:

1. calcolo 2 punti della retta $r$
2. dati $P', P'' \in r$ e punto $A$ calcolo piano da rette $\vec{A P'}$ e $\vec{AP''}$

## Matrici

**matrice m x n** $A = \begin{bmatrix} a_{11} & a_{12} & \ldots & a_{1n} \\ a_{21} & a_{22} & \ldots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & \ldots & a_{mn} \end{bmatrix}$

m righe, n colonne

**matrice quadrata**: matrice con stesso numero di righe e colonne, appartenente a $\mathbb{R}^n$

**traccia**: $tr(A) = \begin{bmatrix} a_{11} & \ldots & \ldots & \ldots \\ \ldots & a_{22} & \ldots & \ldots \\ \vdots & \vdots & \ddots & \vdots \\ \ldots & \ldots & \ldots & a_{nn} \end{bmatrix}$

$$
tr(A) = \sum_{i=1}^n a_{ii}
$$

**matrice diagonale**: matrice quadrata con tutti gli elementi nulli tranne quelli sulla diagonale principale

$$
D = \begin{bmatrix} \lambda_1 & 0 & \ldots & 0 \\ 0 & \lambda_2 & \ldots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \ldots & \lambda_n \end{bmatrix}
$$

**matrice triangolare superiore**: matrice quadrata con tutti gli elementi nulli al di sotto della diagonale principale

$$
U = \begin{bmatrix} \lambda_{11} & x & \ldots & y \\ 0 & \lambda_{22} & \ldots & z \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \ldots & \lambda_{nn} \end{bmatrix}
$$

**matrice triangolare inferiore**: matrice quadrata con tutti gli elementi nulli al di sopra della diagonale principale

$$
L = \begin{bmatrix} \lambda_{11} & 0 & \ldots & 0 \\ x & \lambda_{22} & \ldots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ y & z & \ldots & \lambda_{nn} \end{bmatrix}
$$

**matrice trasposta**: le righe diventano colonne o viceversa

$$
A = \begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \\ \vdots & \vdots\\ a_{n1} & a_{n2} \end{bmatrix} \rightarrow A^T = \begin{bmatrix} a_{11} & a_{21} & \ldots & a_{n1} \\ a_{12} & a_{22} & \ldots & a_{n2} \end{bmatrix}
$$

$$
a_{ij} = (A^T)_{ji}
$$

**matrice simmetrica**: matrice quadrata che è uguale alla sua trasposta, $A = A^T \implies a_{ij} = a_{ji}$

**matrice antisimmetrica**: matrice quadrata che è uguale alla trasposta con segno opposto, $A = -A^T \implies a_{ij} = -a_{ji}$

## operazioni tra matrici

- somma/differenza: $$(A + B)_{ij} = A_{ij} + B_{ij}$$

**prodotto matriciale $ A \in \mathbb{R}^{m \times n}, B \in \mathbb{R}^{n \times p} $**:

$$
 \begin{matrix} A_1 \\ A_2 \end{matrix} \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \end{bmatrix} \cdot \begin{bmatrix} b_{11} & b_{12} \\ b_{21} & b_{22} \\ b_{31} & b_{32} \end{bmatrix} = \begin{bmatrix} <A_1, B^1> & <A_1 , B^2> \\ <A_2, B^1> & <A_2, B^2> \end{bmatrix}
 $$

$$
\begin{bmatrix}  a_{11} \cdot b_{11} + a_{12} \cdot b_{21} + a_{13} \cdot b_{31} & a_{11} \cdot b_{12} + a_{12} \cdot b_{22} + a_{13} \cdot b_{32} \\ \; & \; \\ a_{21} \cdot b_{11} + a_{22} \cdot b_{21} + a_{23} \cdot b_{31} & a_{21} \cdot b_{12} + a_{22} \cdot b_{22} + a_{23} \cdot b_{32} \end{bmatrix}
$$

Nota bene: $AB \neq BA$

- $\exists AB \implies A \cdot (B+C) = AB + AC$
- $\exists BA \implies (B+C) \cdot A = BA + CA$

**matrice inversa**:

- **sinistra**: $A^{-1} A = I_n$
- **destra**: $A A^{-1} = I_n$
- **inversa matrice quadrata**: $A^{-1} A = A A^{-1} = I_n$

**calcolo matrice inversa**:

1. calcolo la matrice dei complementi algebrici
2. trasposta della matrice dei complementi algebrici
3. divido per il determinante della matrice originale

**matrice ortogonale (quadrata)**: matrice $A$ tale che $A^T A = I_n$

**matrice simile (quadrata)**: matrice $C$ simile a matrice $A$ se esiste matrice invertibile $B$ tale che $C = B^{-1} A B$

stesso **endomorfismo** rappresentato in basi diverse

## Spazi vettoriali

**spazio vettoriale $V$**: insieme $V \neq \emptyset$ dove sono definite:

- **somma**: $V \times V \rightarrow V \quad v + w$
- **prodotto**: $\mathbb{R} \times V \rightarrow V \quad \lambda v$

**condizioni per essere spazio vettoriale**:

1. commutativa: $(u + v) + w = u + (v + w)$
2. elemento neutro somma: $v + 0 = v$
3. elemento opposto: $v + (-v) = 0$
4. $(\lambda + \delta) \cdot v = \lambda \cdot v + \delta \cdot v$
5. elemento neutro prodotto: $1 \cdot v = v$
6. $(\lambda \cdot \delta) \cdot v = \lambda \cdot (\delta \cdot v)$

**vettori**: elementi di uno spazio vettoriale

**proprietà spazio vettoriale**:

1. $\exist \bold{0} \in V : v + \bold{0} = v \quad \forall v \in V$ ed è _unico_
2. $\bold{0} \cdot v = \bold{0} \quad \forall v \in V$
3. $\alpha \cdot v \iff \alpha = 0 \lor v = \bold{0} $
4. $ v + u = v + w \iff u = w$
5. $(-1) \cdot v = < -v > $

**sottospazio vettoriale $W$**: sottoinsieme di $V$ che è esso stesso uno spazio vettoriale con le stesse operazioni di $V$

**condizione sottospazio vettoriale**:

$$
\lambda v + \mu w \in W \quad \forall v,w \in W \; \land \; \forall \lambda, \mu \in \mathbb{R}
$$

NOTA: se $0 \not\in W$ allora $W$ non è sottospazio vettoriale

se $W,U$ sottospazi vettoriali allora intersezione $W \cap U$ è sottospazio vettoriale

**combinazione lineare**: $ \lambda_1 v_1 + \lambda_2 v_2 + \ldots + \lambda_n v_n $ con $v_i$ vettori e $\lambda_i$ valori in $\mathbb{R}$

$$
 w = \sum_{i=1}^n \lambda_i v_i
$$

$w$ generato da $v_1, v_2, \ldots, v_n$

**inviluppo lineare**: insieme di tutte le combinazioni lineari di un insieme di vettori $S = \{v_1, v_2, \ldots, v_n\}$. È un sottospazio vettoriale

$$
 \mathcal{L}\<W\> = \mathcal{L}< v_1, v_2, \ldots, v_n > \ = \ \{ \lambda_1 v_1, \ldots, \lambda_n v_n \} : \lambda_i \in \mathbb{R}
$$

**dipendenza lineare**: $ \lambda v_1 + \lambda_2 v_2 + \ldots + \lambda_n v_n = 0 $ con almeno un $\lambda_i \neq 0$

**indipendenza lineare**: $ \lambda v_1 + \lambda_2 v_2 + \ldots + \lambda_n v_n = 0 \iff \lambda_1 = \lambda_2 = \ldots = \lambda_n = 0$

NOTA:
$v_0, v_1, \ldots, v_n$ **indipendenti**:

- se **tolgo** un vettore $v_i \implies$ rimangono **indipendenti**
- se **aggiungo** un vettore $v_{n+1}$ devo **verificare nuovamente** indipendenza

$v_0, v_1, \ldots, v_n$ **dipendenti**:

- se **tolgo** un vettore $v_i$ devo **verificare nuovamente** dipendenza
- se **aggiungo** un vettore $v_{n+1} \implies$ rimangono **dipendenti**

## Basi e dimensione

**dimensione $dim(V)$**: cardinalità massima dell'insieme di vettori indipendenti in $V$

**base**: $\{v_1, v_2, \ldots, v_n\}$ insieme di vettori linearmente indipendenti tali che $\mathcal{L}<v_1, v_2, \ldots, v_n> = V $

dati 2 sottospazi $U, W$ di $V$

- $\max\{dim(U), dim(W)\} \leq dim(U + W) \leq dim(U) + dim(W)$
- $dim(U + W) = dim(U) + dim(W) - dim(U \cap W)$

## Applicazioni lineari

**applicazione lineare $F: V \rightarrow W$**

**condizioni di linearità**:

1. $F(v + w) = F(v) + F(w)$
2. $F(\lambda v) = \lambda F(v)$

**nucleo o kernel**: $Ker(F) = \{v \in V : F(v) = 0_W\}$

**immagine o range**: $Im(F) = \{w \in W : \exists v \in V \text{ con } w = F(v)\}$

**nullità**: $dim(Ker(F))$

**rango**: $dim(Im(F))$

**iniettività**: $dim(Ker(F)) = \{0\} \iff F$ iniettiva

**suriettività**: $dim(Im(F)) = dim(W) \iff F$ suriettiva, oppure $Im(F) = W$

**isomorfismo**: iniettività e suriettività

**teorema nullità + rango**: $dim(V) = dim(Ker(F)) + dim(Im(F))$

$F(v_1), F(v_2), \ldots, F(v_p)$ L.I. $\iff v_1, v_2, \ldots, v_p$ L.I.

**matrice associata a una applicazione lineare**:

$$
A = [A^1 \; A^2 \; \ldots \; A^n] = \begin{bmatrix} \begin{bmatrix} \; \\ F(v_1) \\ \; \end{bmatrix}_{B'} & \begin{bmatrix} \; \\ F(v_2) \\ \; \end{bmatrix}_{B'} & \ldots & \begin{bmatrix} \; \\ F(v_n) \\ \; \end{bmatrix}_{B'} \\ \end{bmatrix}
$$

**matrice di cambiamento di base**: matrice associata all'identità $I_V$ tra due basi $B$ e $B'$

$B = (b_1, b_2, b_3)$, $B' = (b'_1, b'_2, b'_3)$

$B \rightarrow B'$

$$
M[id, B, B'] = \begin{bmatrix} \begin{bmatrix} \; \\ b_1 \\ \; \end{bmatrix}_{B'} \begin{bmatrix} \; \\ b_2 \\ \; \end{bmatrix}_{B'} \begin{bmatrix} \; \\ b_3 \\ \; \end{bmatrix}_{B'} \end{bmatrix}
$$

$$
\begin{array}{c} [b_1]_{B'} = (x_1, x_2, x_3) \ | \ x_1 b_1' + x_2 b_2' + x_3 b_3' = b_1 \\ [b_2]_{B'} = (x_1, x_2, x_3) \ | \ x_1 b_1' + x_2 b_2' + x_3 b_3' = b_2 \\ [b_3]_{B'} = (x_1, x_2, x_3) \ | \ x_1 b_1' + x_2 b_2' + x_3 b_3' = b_3 \end{array}
$$

$B' \rightarrow B$

$$
M[id, B', B] = \begin{bmatrix} \begin{bmatrix} \; \\ b'_1 \\ \; \end{bmatrix}_{B} \begin{bmatrix} \; \\ b'_2 \\ \; \end{bmatrix}_{B} \begin{bmatrix} \; \\ b'_3 \\ \; \end{bmatrix}_{B} \end{bmatrix}
$$

$$
\begin{array}{c} [b'_1]_{B} = (x_1, x_2, x_3) \ | \ x_1 b_1 + x_2 b_2 + x_3 b_3 = b'_1 \\ [b'_2]_{B} = (x_1, x_2, x_3) \ | \ x_1 b_1 + x_2 b_2 + x_3 b_3 = b'_2 \\ [b'_3]_{B} = (x_1, x_2, x_3) \ | \ x_1 b_1 + x_2 b_2 + x_3 b_3 = b'_3 \end{array}
$$

**caso di applicazioni lineari**:

$B' \rightarrow B \rightarrow \hat{B} \rightarrow \hat{B}'$

$$
M[id, B', \hat{B}'] = M[id, \hat{B}, \hat{B}'] \cdot M[id, B, \hat{B}] \cdot M[id, B', B]
$$

## Sistemi lineari

$$
AX = B
$$

$$
\begin{bmatrix} \begin{bmatrix} \; \\ A^1 \\ \; \end{bmatrix} & \ldots & \begin{bmatrix} \; \\ A^n \\ \; \end{bmatrix} \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ \ldots \\ x_n \end{bmatrix} = \begin{bmatrix} b_1 \\ \ldots \\ b_m \end{bmatrix}
$$

$$
x_1 \cdot A^1 + \ldots + x_n \cdot A^n = \begin{bmatrix} b_1 \\ \ldots \\ b_m \end{bmatrix}
$$

$$
\begin{cases} x_1 \cdot a_{11} + \ldots + x_n \cdot a_{n1} = b_1 \\ \vdots \\ x_1 \cdot a_{1m} + \ldots + x_n \cdot a_{nm} = b_m \end{cases}
$$

Il sistema può avere 3 tipi di soluzioni:

1. nessuna soluzione: $Ax = B$ è impossibile
2. una soluzione unica: $Ax = B$ è possibile e $Ker(A) = \{0\}$
3. infinite soluzioni: $Ax = B$ è possibile e $Ker(A) \neq \{0\}$

### Metodo di Gauss

$$
\begin{array}{c} \; \\ Ri \\ \; \\ Rj \\ \; \end{array} \begin{bmatrix} \ldots &\ldots & \ldots & \ldots \\ a_{i1} & a_{i2} & \ldots & a_{in} \\ \ldots &\ldots & \ldots & \ldots \\ a_{j1} & a_{j2} & \ldots & a_{jm} \\ \ldots &\ldots & \ldots & \ldots \end{bmatrix}
$$

VI sono 3 regole per operare sulle matrici, che siano righe o colonne:

- G1: $R_i \leftrightarrow R_j$
- G2: $R_i \leftrightarrow \lambda R_i$
- G3: $R_i \leftrightarrow R_i + R_j$

Ovviamente queste regole possono essere combinate

**procedimento**:

- opero sulla **matrice estesa** $ \begin{bmatrix} A & | & b \end{bmatrix} $

- trasformo la matrice in **matrice in forma echelon** con le regole di Gauss

  $$
  \begin{bmatrix} 0 & p_1 & * & * & * & * \\ 0 & 0 & 0 & p_2 & * & * \\ 0 & 0 & 0 & 0 & p_3 & * \\ 0 & 0 & 0 & 0 & 0 & 0 \end{bmatrix} \begin{array}{c} \; \\ \text{numero di pivot = rango} \\ \text{pivot in ultima colonna : sol. impossibile} \\ \; \end{array}
  $$

- riscrivo il sistema con la matrice a gradini

- risolvo il sistema con sostituzione all'indietro

**matrice inversa con metodo di Gauss**:

$$
\begin{bmatrix} A & | & I_n \end{bmatrix} \rightarrow \begin{bmatrix} I_n & | & A^{-1} \end{bmatrix}
$$

**Teorema di Rouché-Capelli**:

$rg(A) = rg (\begin{bmatrix} A | b \end{bmatrix})$ sistema ammissibile

- $rg(A) = rg (\begin{bmatrix} A|b \end{bmatrix}) = n (x_n)$ unica soluzione
- $rg(A) = rg (\begin{bmatrix} A|b \end{bmatrix}) < n (x_n)$ infinite soluzioni

$rg(A) \neq rg (\begin{bmatrix} A|b \end{bmatrix})$ sistema impossibile

### Calcolo del determinante

Dati $v_1, v_2, \ldots, v_n \mathbb{R}^n \; LD \implies det(v_1, v_2, \ldots, v_n) = 0$
Dati $v_1, v_2, \ldots, v_n \mathbb{R}^n \; LI \implies det(v_1, v_2, \ldots, v_n) \neq 0$

**determinante matrice 2x2**:

$$
det \begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix} = a_{11} a_{22} - a_{12} a_{21}
$$

**Regola di Sarrus**:

$$
 \begin{vmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{vmatrix} \begin{array}{cc} a_{11} & a_{12} \\ a_{21} & a_{22} \\ a_{31} & a_{32} \end{array} = \begin{array}{c} a_{11} a_{22} a_{33} + a_{12} a_{23} a_{31} + a_{13} a_{21} a_{32} \\ - (a_{13} a_{22} a_{31} + a_{11} a_{23} a_{32} + a_{12} a_{21} a_{33})\end{array}
 $$

**complemento algebrico**: $\bar a_{ij} = (-1)^{i+j} det(A_{ij}) = (-1)^{i+j} \cdot det M_{ij}$
$M_{ij}$ matrice ottenuta da $A$ eliminando riga $i$ e colonna $j$

**Sviluppo di Laplace**:
scelgo una riga o colonna e sviluppo il determinante rispetto a quella riga o colonna

$$
det(A) = \sum_{j=1}^n [(-1)^{i+j} \cdot a_{ij} \cdot det(M_{ij})]
$$

con $M_{ij}$ matrice ottenuta da $A$ eliminando riga $i$ e colonna $j$

- esempio con matrice 3x3 scegliendo la prima riga:

$$
\begin{vmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{vmatrix} = a_{11} \begin{vmatrix} a_{22} & a_{23} \\ a_{32} & a_{33} \end{vmatrix} - a_{12} \begin{vmatrix} a_{21} & a_{23} \\ a_{31} & a_{33} \end{vmatrix} + a_{13} \begin{vmatrix} a_{21} & a_{22} \\ a_{31} & a_{32} \end{vmatrix}
$$

**calcolo dell'inversa mediante determinante**:

1. calcolo la matrice dei complementi algebrici
2. trasposta della matrice dei complementi algebrici
3. divido per il determinante della matrice originale

in generale:

$$
b_{ij} = \frac{\bar{a}_{ji}}{\det(A)}
$$

**regola di Cramer**: $Ax = b$ con $A$ matrice quadrata invertibile, $x$ vettore incognito, $b$ vettore noto

$$
x_i = \frac{det(A_i)}{det(A)}
$$

$$
\bar{x_i} = \frac{det \begin{bmatrix} A^1 & & \ldots & A^{i-1} & \begin{bmatrix} \; \\ b \\ \; \end{bmatrix} & A^{i+1} & \ldots & A^n \end{bmatrix}}{det(A)}
$$

sostituisco la colonna $i$ di $A$ con il vettore $b$ e calcolo il determinante, poi divido per il determinante di $A$

## Autovettori e autovalori

$A - \lambda I$ matrice ottenuta sottraendo $\lambda$ alla diagonale principale di $A$

$$
 \begin{vmatrix} a_{11} - \lambda & \ldots & \ldots & \ldots \\ \ldots & a_{22} - \lambda & \ldots & \ldots \\ \vdots & \vdots & \ddots & \vdots \\ \ldots & \ldots & \ldots & a_{nn} - \lambda \end{vmatrix}
 $$

1. **polinomio caratteristico $\mathcal{P}(A)$**: $det (A - \lambda I) = 0$
2. **autovalori**: $\bar{\lambda}$ che rendono $\mathcal{P}(A) = 0$
3. calcolo autospazio originato dagli autovettori
