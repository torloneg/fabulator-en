---
description: Description of Accounting
---

# Accounting


## Accounting.Fix
better rounding for floating point numbers


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | float  | input value received
    | precision | int  | digit number


### example:
```
{{  0.611 | Accounting.Fix(2)}}

```

### output:
```
0.61

```

## Accounting.FormatColumn
format a list of values for column-display


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | array  | input value received as array
    | symbol | string  | monetary symbol


### example:
```
{{ [123.5, 3456.49, 777888.99, 12345678, -5432] | Accounting.FormatColumn("$ ")}}

```

### output:
```
$  123.5,$  3456.49,$  777888.99,$  12345678,$  -5432

```

## Accounting.Money
format any number into currency


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | float  | input value received
    | symbol | string  | currency symbol
    | precision | Int  | decimal places
    | decimal | int  | decimal point separator
    | thousand | int  | thousands separator


### example:
```
{{ 4999.99 | Accounting.Money("us")}}

```

### output:
```
$4,999.99

```

## Accounting.MoneyFormat
format any number into currency


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | float  | input value received
    | symbol
type: string
description: currency symbol |   | 
    | precision
type: Int
description: decimal places |   | 
    | decimal
type: int
description: decimal point separator |   | 
    | thousand
type: int
description: thousands separator |   | 


### example:
```
{{ 4999.99 | Accounting.MoneyFormat("€", 2, ".", ",")}}

```

### output:
```
€4.999,99

```

## Accounting.NumberFormat
format a number with custom precision and localisation


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | float  | input value received
    | symbol | string  | currency symbol
    | precision | int  | decimal places


### example:
```
{{ 9876543.21 | Accounting.NumberFormat(3, " ")}}

```

### output:
```
9 876 543.210

```



