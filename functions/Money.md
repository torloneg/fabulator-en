---
description: Description of Money
---

# Money


## Money.Convert
converts the value of one currency into another


**params**
    |  |  |
    | :--- | :--- |
    | title | from  |
    | type | string |
    | value |  |
    | title | to  |
    | type | string |
    | value |  |


```
example: {{ 123 | Money.Convert("USD","EUR") }}

output: 108,03

```
## Money.Symbol
returns the symbol of a currency


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "USD" | Money.Symbol()}}

output: $

```
## Money.SymbolExt
TODO


**params**
    |  |  |
    | :--- | :--- |
    | title | TODO  |
    | type | TODO |
    | value |  |


```
example: TODO

output: TODO

```


