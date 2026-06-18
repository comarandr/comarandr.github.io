---
layout: default
title: Json
permalink: /linguaggi/Json/
---

## Introduzione

JSON (JavaScript Object Notation) è un formato per lo scambio di dati.

È costruito su due strutture:

- Una collezione di coppie chiave/valore (oggetto)
- Una lista ordinata di valori (array)

## Elementi chiave

**Object**: coppia non ordinata di nome/valore, delimitata da parentesi graffe `{}`
Ogni nome è seguito da due punti `:` e le coppie sono separate da virgole `,`

```json
{"name: "John", "age": 30, "city": "New York"}
```

**Array**: una collezione ordinata di valori, delimitata da parentesi quadre `[]`
I valori sono separati da virgole `,`

```json
{
    "fruits": ["apple", "banana", "cherry"]
}
```

## Tipi di dati

- **Stringa**: testo racchiuso tra virgolette doppie `{"name": "John"}` o singole `{'name': 'John'}`
- **Numero**: interi o decimali `{"age": 30}` o `{"price": 19.99}`
- **Oggetto**: una collezione di coppie chiave/valore delimitata da parentesi graffe `{"employee": {"name": "John", "age": 30}}`
- **Array**: una collezione ordinata di valori delimitata da parentesi quadre `{"fruits": ["apple", "banana", "cherry"]}`
- **Booleano**: `true` o `false` `{"isStudent": true}`
- **Null**: rappresenta un valore nullo `{"middleName": null}`

## Nested JSON Objects and nested JSON Arrays

I valori in un oggetto JSON possono essere altri oggetti JSON o array

```json
myObj = {
    "name": "John",
    "age": 30,
    "cars": "Ford", "BMW", "Fiat"
}
```

Ovviamente anche gli array possono essere annidati

```json
myObj = {
    "name": "John",
    "age": 30,
    "cars": [
        {"model": "Ford", "models": ["Fiesta", "Focus", "Mustang"]},
        {"model": "BMW", "models": ["320", "X3", "X5"]},
        {"model": "Fiat", "models": ["500", "500X"]}
    ]
}
```

Per accedere a un array annidato, usiamo un for-in loop per ogni array

```json
for (i in myObj.cars) {
    x+=myObj.cars[i].model + "</h1>";
    for (j in myObj.cars[i].models) {
        x+=myObj.cars[i].models[j] + "</h1>";
    }
}
```
