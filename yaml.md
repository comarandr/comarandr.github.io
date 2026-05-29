# Schemi YAML

## Introduzione

YAML (YAML Ain't Markup Language) è uno standard di serializzazione dei dati leggibile per tutti i linguaggi di programmazione.

Consenste di memorizzare i dati strutturati in una gerarchia.

## Sintassi di base

**commenti**: iniziano dal carattere `#` e continuano fino alla fine della riga.

**struttura e identazione**: la struttura e la gerarchia dei data è determinata dall'indentazione. L'indentazione deve essere consistente

```yaml
livello_1:
  livello_2:
    livello_3: valore
  altro_livello_2: altro_valore
```

generalmente l'indentazione è rappresentata da **2 spazi**.
È possibile usare tabulazione, ma ci possono essere problemi di parsing.

## Tipi di dati

- **stringhe**: possono essere racchiuse tra virgolette doppi o singole oppure no

```yaml
stringa_senza_virgolette: Ciao mondo
stringa_con_virgolette: "Ciao mondo"
stringa_con_virgolette_singole: 'Ciao mondo'
```

- **stringhe multilinea**: possono essere rappresentate con `|` o `>`.

```yaml
stringa_multilinea_con_pipe: |
  Questa è una stringa
  multilinea che mantiene
  i ritorni a capo.
```

stringa_multilinea_con_maggiore: `>``

- **numeri**: riconosciuti vari formati

  - naturali: `42`, `-7`
  - negativi: `-17`
  - float: `3.1451`
  - scientifico: `1.23e+02`
  - ottale: `0o77`
  - esadecimale: `0xFF`

- **booleani**: case insensitive, riconosce vari formati
  
  - vero: `true`, `True`, `TRUE`, yes, `Yes`, `YES`, on, `On`
  - `false`, `False`, `FALSE`, no, `No`, `NO`, off, `Off`

- **null**: rappresentato in vari modi

  - esplicito:`null`, `Null`, `NULL`, `~` o stringa vuota
  - implicito: valore vuoto

- **date e timestamp**: in formato ISO 8601

  - data: `2024-06-01`
  - timestamp: `2024-06-01T12:34:56Z`

- **collezioni**: principalmente liste e dizionari

  - **liste**: su più righe con `-` o inline con `[]`

  ```yaml
  lista_multiriga:
  - elemento1
  - elemento2
  - elemento3

  lista_inline: [elemento1, elemento2, elemento3]
  ```

  - **dizionari (mapping)**: associano chiavi a valori

  ```yaml
  # formato multiriga
  persona:
    nome: Mario
    età: 30

  # formato compatto
    persona_compatta: {nome: Mario, età: 30}
  ```

## Caratteristiche avanzate

**ancore e alias**: permette di creare riferimento con il carattere `&` e riutilizzarli con `*`.

```yaml
template: &config_base
  porta: 8080
  timeout: 30
  
server_dev:
    <<: *config_base #Merge del template
    ambiente: development

server_prod:
    <<: *config_base
    porta: 80 # Override del template
    ambiente: production
```

**tag**: per specificare il tipo di dato

```yaml
boolean: !!bool yes
intero: !!int 42
float: !!float 3.14
stringa: !!str 12345
timestamp: !!timestamp 2024-06-01
```

**multidocumento**: consente di avere più documenti in un unico file, separati da `---`

```yaml
---
# Primo documento
database: mysql
---
# Secondo documento
database: postgresql
---
# Terzo documento
database: mongodb
... #Terminatore opzionale
```
