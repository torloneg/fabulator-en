---
description: Description of Accounting
---

# Accounting


## Accounting.Fix
better rounding for floating point numbers


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | float  | 
    | precision | int  | digit number


### example:
```
{{  0.615 | Accounting.Fix(2)}}

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
    | value | array  | array of float number
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
    | value | float  | 
    | symbol | string  | 
    | precision | Int  | 
    | decimal | int  | 
    | thousand | int  | 


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
    | value | float  | 
    | symbol | string  | 
    | precision | int  | 
    | decimal | int  | 
    | thousand | int  | 


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
    | value | float  | 
    | symbol | string  | 
    | precision | int  | 


### example:
```
{{ 9876543.21 | Accounting.NumberFormat(3, " ")}}

```

### output:
```
9 876 543.210

```



