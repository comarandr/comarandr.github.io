---
layout: default
title: Markdown
permalink: /linguaggi/markdown/
---

## Sintassi base

## Heading (titoli)

6 livelli di gerarchia, dal più grande al più piccolo, rappresentati da `#`:

\# Heading level 1
\## Heading level 2
\### Heading level 3
\#### Heading level 4
\##### Heading level 5
\###### Heading level 6

In alternativa, per i primi due livelli, è possibile usare `=` e `-`:

Titolo di primo livello
\==========

Titolo di secondo livello
\----------

## Paragraph (paragrafi)

Per i paragrafi, basta lasciare una riga vuota tra due blocchi di testo.

Paragraph 1

Paragraph 2

## Line breaks (interruzioni di linea)

Per forzare un'interruzione di linea, basta terminare la riga con due spazi e premere invio.

Ciao io.
Ciao tu.

## Bold (grassetto)

Racchiudere il testo tra due coppie di asterischi `**` o due coppie di underscore `__`.

\*\*ciao\*\*
\_\_ciao\_\_

## Italic (corsivo)

Racchiudere il testo tra una coppia di asterischi `*` o una coppia di underscore `_`.

\*ciao\*
\_ciao\_

## Bold and Italic (grassetto e corsivo)

Racchiudere il testo tra tre coppie di asterischi `***` o tre coppie di underscore `___`.

\*\*\*ciao\*\*\*
\_\_\_ciao\_\_\_

## Blockquote (citazioni)

Basta usare il simbolo `>` all'inizio della riga.

\> Questa è una citazione.

> citazione

Posso anche annidare le citazioni:

\> Questa è una citazione.
\>\> Questa è una citazione annidata.

> Citazione
>> Citazione annidata

## Lists (liste)

### Unordered Lists (liste non ordinate)

Basta aggiungere `-`, `*` o `+` all'inizio della riga.

\- Elemento 1
\- Elemento 2

- Elemento 1
- Elemento 2

Per annidare, basta aggiungere due spazi prima del simbolo della lista.

```
- Elemento 1
  - Elemento 1.1
  - Elemento 1.2
```

- Elemento 1
  - Elemento 1.1
  - Elemento 1.2

### Ordered Lists (liste ordinate)

Aggiungere un numero seguito da un punto all'inizio della riga.

\1. Elemento 1
\2. Elemento 2

1. Elemento 1
2. Elemento 2

Posso annidarle

```
1. Elemento 1
    1. Elemento 1.1
    2. Elemento 1.2
2. Elemento 2
```

1. Elemento 1
    1. Elemento 1.1
    2. Elemento 1.2
2. Elemento 2

### Elements of a list (elementi di una lista)

Per aggiungere un elemento nella lista, basta indentare di 4 spazi o un tab.

```
- Elemento 1
    Questo è un elemento della lista.
- Elemento 2
    Questo è un altro elemento della lista.
```

1. Elemento 1
    Questo è un elemento della lista.
2. Elemento 2
    Questo è un
    altro elemento della lista.
3. Elemento 3

## Blocchi codice

Indentare ogni riga con almeno 4 spazi o un tab.

    console.log("Hello, World!");
      console.log("This is a code block.");

backtick \``` seguiti eventualmente dal nome del linguaggio per creare un blocco di codice:

```javascript
console.log("Hello, World!");
console.log("This is a code block.");
```

## Code (inline code)

Racchiudere il testo tra due backtick \` per creare un codice inline.

\`console.log("Hello, World!");`

`console.log("Hello, World!");`

con due backtick \`` posso racchiudere del testo che contiene backtick:

``ciao `code` ciao``

## Horizontal Rule (linea orizzontale)

Usare tre o più asterischi `***`, trattini `---` o underscore `___` su una riga da soli

\---

---

## Links (collegamenti)

Usa la sintassi `[testo](url)`

\[Google](https://www.google.com)

[Google](https://www.google.com)

Posso anche aggiungere un titolo al link, racchiuso tra virgolette:

\[Google](https://www.google.com "Vai a Google")

[Google](https://www.google.com "Vai a Google")

## URLs and Email Addresses (URL e indirizzi email)

Racchiudere l'URL o l'indirizzo email tra `<` e `>` per creare un link automatico

<https://www.google.com>
<example@example.com>

### Formatting links (formattazione dei collegamenti)

per enfatizzare il testo del link, basta racchiuderlo tra asterischi `*` o underscore `_`:

**[Google](https://www.google.com)**
*[Google](https://www.google.com)*

Ulteriori formattazioni possono essere:

```md
[Google][1]
[Sito web][1]

[1]: https://www.google.com
```

Entrambi i link puntano a Google

[Google][1]
[Sito web][1]

[1]: https://www.google.com

## Images (immagini)

I riferimenti alle immagini seguono la sintassi:

\!\[testo]\(url)

## Escaping (caratteri speciali)

Per inserire un carattere speciale, basta precederlo con un backslash `\`

## Tables (tabelle)

```
| Colonna 1 | Colonna 2 | Colonna 3 |
| --------- | --------- | --------- |
| Riga 1, Colonna 1 | Riga 1, Colonna 2 | Riga 1, Colonna 3 |
```

| Colonna 1 | Colonna 2 | Colonna 3 |
| --------- | --------- | --------- |
| Riga 1, Colonna 1 | Riga 1, Colonna 2 | Riga 1, Colonna 3 |

### allineamento delle colonne

```
| Colonna 1 | Colonna 2 | Colonna 3 |
| :-------- | :-------: | --------: |
| sinistra | centrale | destra |
```

| Colonna 1 | Colonna 2 | Colonna 3 |
| :-------- | :-------: | --------: |
| sinistra | centrale | destra |

## Footnotes (note a piè di pagina)

```
Questa è una frase con una nota a piè di pagina.[^1]    

[^1]: Questa è la nota a piè di pagina.
```

Nota a piè di pagina[^1]

[^1]: Questa è la nota a piè di pagina.

## Definition Lists (liste di definizione)

```
Termine 1
: Definizione del termine 1
Termine 2
: Definizione del termine 2
```

Termine 1
: Definizione del termine 1

Termine 2
: Definizione del termine 2

## Strikethrough (barrato)

Per barrare il testo, basta racchiuderlo tra due tilde `~`

\~~testo barrato\~~

~~testo barrato~~

## Task Lists (liste di attività)

```
- [x] Attività completata
- [ ] Attività non completata
```

- [x] Attività completata
- [ ] Attività non completata
- [ ] Attività non completata

