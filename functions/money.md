---
description: Description of Money
---

# Money


## Money.Convert
converts the value of one currency into another


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | from | string  | currency from
    | to | string  | currency to


```
example: {{ 123 | Money.Convert("USD","EUR") }}

output: 108,03

```
## Money.Symbol
returns the symbol of a currency


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "USD" | Money.Symbol()}}

output: $

```
## Money.SymbolExt
TODO


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: TODO

output: TODO

```


