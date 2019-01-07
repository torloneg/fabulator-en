---
description: Description of Accounting
---

# Accounting

## Accounting.Fix

better rounding for floating point numbers

**params**

| name | type | description |
| :--- | :--- | :--- |
| input | float |  |
| precision | int | digit number |

### example:

```text
{{  0.615 | Accounting.Fix(2)}}
```

### output:

```text
0.61
```

## Accounting.FormatColumn

format a list of values for column-display

**params**

| name | type | description |
| :--- | :--- | :--- |
| input | array | array of float number |
| symbol | string | monetary symbol |

### example:

```text
{{ [123.5, 3456.49, 777888.99, 12345678, -5432] | Accounting.FormatColumn("$ ")}}
```

### output:

```text
$  123.5,$  3456.49,$  777888.99,$  12345678,$  -5432
```

## Accounting.Money

format any number into currency

**params**

| name | type | description |
| :--- | :--- | :--- |
| input | float |  |
| symbol | string |  |
| precision | Int |  |
| decimal | int |  |
| thousand | int |  |

### example:

```text
{{ 4999.99 | Accounting.Money("us")}}
```

### output:

```text
$4,999.99
```

## Accounting.MoneyFormat

format any number into currency

**params**

| name | type | description |
| :--- | :--- | :--- |
| input | float |  |
| symbol | string |  |
| precision | int |  |
| decimal | int |  |
| thousand | int |  |

### example:

```text
{{ 4999.99 | Accounting.MoneyFormat("€", 2, ".", ",")}}
```

### output:

```text
€4.999,99
```

## Accounting.NumberFormat

format a number with custom precision and localisation

**params**

| name | type | description |
| :--- | :--- | :--- |
| input | float |  |
| symbol | string |  |
| precision | int |  |

### example:

```text
{{ 9876543.21 | Accounting.NumberFormat(3, " ")}}
```

### output:

```text
9 876 543.210
```

