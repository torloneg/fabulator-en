---
description: Description of Accounting
---

# Accounting


## Accounting.Fix
better rounding for floating point numbers


**params**
    |  |  |
    | :--- | :--- |
    | title | precision  |
    | type | int |
    | value |  |


```
example: {{  0.615 | Accounting.Fix(2)}}

output: 0.61

```
## Accounting.FormatColumn
format a list of values for column-display


**params**
    |  |  |
    | :--- | :--- |
    | title | symbol  |
    | type | string |
    | value |  |


```
example: {{ [123.5, 3456.49, 777888.99, 12345678, -5432] | Accounting.FormatColumn("$ ")}}

output: $  123.5,$  3456.49,$  777888.99,$  12345678,$  -5432

```
## Accounting.Money
format any number into currency


**params**
    |  |  |
    | :--- | :--- |
    | title | symbol  |
    | type | string |
    | value |  |


```
example: {{ 4999.99 | Accounting.Money("us")}}

output: $4,999.99

```
## Accounting.MoneyFormat
format any number into currency


**params**
    |  |  |
    | :--- | :--- |
    | title | symbol  |
    | type | string |
    | value |  |


```
example: {{ 4999.99 | Accounting.MoneyFormat("€", 2, ".", ",")}}

output: €4.999,99

```
## Accounting.NumberFormat
format a number with custom precision and localisation


**params**
    |  |  |
    | :--- | :--- |
    | title | symbol  |
    | type | string |
    | value |  |


```
example: {{ 9876543.21 | Accounting.NumberFormat(3, " ")}}

output: 9 876 543.210

```


