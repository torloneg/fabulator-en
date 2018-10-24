---
description: Description of Numeral
---

# Numeral

## Numeral.Add

Add a integer to a number

_params_ \| title \| Number to add \| \| type \| int \| \| value \| \|

**params**

|  |  |
| :--- | :--- |
| **test** | value |
| casa | ssssss |

```text
example: {{1 | Numeral.Add(1)}}

output: 2
```

## Numeral.Divide

divide a number by another number

_params_ \| title \| Number to divide \| \| type \| int \| \| value \| \|

```text
example: {{10 | Numeral.Divide(5)}}

output: 2
```

## Numeral.Format

return a number with a new format

_params_ \| title \| Format string \| \| type \| string \| \| value \| \|

```text
example: {{10000 | Numeral.Format('0,0.0000')}}

output: 10000
```

## Numeral.Plularize

returns a string based on the value of the number == 1 \( singular \), &gt;1 \(plural\), ==0 \( undefined\)

_params_ \| title \| singular \| \| type \| string \| \| value \| \| \| title \| plural \| \| type \| string \| \| value \| \| \| title \| undef \| \| type \| string \| \| value \| \|

```text
example: {{ 1 | Numeral.Plularize('singular','plural','undefined')}}

output: singular
```

## Numeral.Sign

Returns strings based on the sign of the number : positive, negative,parity

_params_ \| title \| positive \| \| type \| string \| \| value \| \| \| title \| negative \| \| type \| string \| \| value \| \| \| title \| parity \| \| type \| string \| \| value \| \|

```text
example: {{ -1 | Numeral.Sign('positive','negative','parity')}}

output: negative
```

## Numeral.Subtract

Subtracts a number from another number

_params_ \| title \| Number to subtracts \| \| type \| int \| \| value \| \|

```text
example: {{2 | Numeral.Subtract(1)}}

output: 1
```

