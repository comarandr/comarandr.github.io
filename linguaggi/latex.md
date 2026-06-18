---
layout: default
title: LaTeX
permalink: /linguaggi/LaTeX/
---

## Creare un documento

Per creare un documento, basta scrivere:

```tex
\documentclass{article} %tipo di documento
\usepackage{nome_pacchetto} %per i pacchetti
\title{titolo}
\author{autore}
\date{data}
\begin{document} % inizio del documento
\maketitle % per mostrare titolo, autore, data
\tableofcontents % per mostrare la tabella dei contenuti
...
\newpage % per cambiare pagina
...
\end{document}
```

La sintassi minima è la seguente

```tex
\documentclass{article}
\begin{document}
...
\end{document}
```

## Suddividere un testo

La suddivisione viene enumerata automaticamente

- **Parte**: `\part{part_name}`
- **Sezione**: `\section{section_name}`
- **Sottosezione**: `\subsection{subsection_name}`
- **Paragrafo**: `\paragraph{paragraph_name}`
- **Sottoparagrafo**: `\subparagraph{subparagraph_name}`
- **nuova pagina**: `\newpage`

## Comandi di scrittura

- **non compilazione**: `\verbatim{testo non compilato}` per esempio posso usarlo per scrivere `\verbatim{\part \\}` &rarr; `\part \\`
- **tabulazione**:

```tex
\begin{tabbing} 
col1 \ col2 \ col3 
\end{tabbing}
```

ottengo

```txt
col1    col2    col3
```

- **colore testo**: `\textcolor{color_name}{testo}`
- **corsivo**: `\textit{testo}`
- **grassetto**: `\textbf{testo}`
- **sottolineato**: `\underline{testo}`

## Tabelle

Per prima cosa inizializziamo la tabella richiamando l'ambiente `tabular`:

```tex
\begin{tabular}{condizioni}
...
\end{tabular}
```

parametri:

- **l,c,r**: allineamento a sinistra, al centro o a destra
- **p{width}**: per specificare la larghezza di una colonna, esclude parametri di allineamento
- **|**: per inserire una linea verticale
- **@{...}**: per spaziare le colonne

Costruzione della tabella:

- **&**: per separare le colonne
- **\\**: per andare a capo
- **\hline**: per inserire una linea orizzontale
- **\cline{i-j}**: per inserire una linea orizzontale tra colonna i e j
- **\multicolumn{ncol}{allineamentoOrizz}{...}**: per unire n colonne, condizioni e testo sono opzionali