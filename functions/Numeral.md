---
description: Description of Numeral
---

# Numeral


## Numeral.Add
Add a integer to a number

{% hint style="info" %}
*params*
    | title | Number to add  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{1 | Numeral.Add(1)}}

output: 2
```
## Numeral.Divide
divide a number by another number

{% hint style="info" %}
*params*
    | title | Number to divide  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{10 | Numeral.Divide(5)}}

output: 2
```
## Numeral.Format
return a number with a new format

{% hint style="info" %}
*params*
    | title | Format string  |
    | type | string |
    | value |  |
{% endhint %}

```
example: {{10000 | Numeral.Format('0,0.0000')}}

output: 10000
```
## Numeral.Plularize
returns a string based on the value of the number &#x3D;&#x3D; 1 ( singular ), &gt;1 (plural), &#x3D;&#x3D;0 ( undefined)

{% hint style="info" %}
*params*
    | title | singular  |
    | type | string |
    | value |  |
    | title | plural  |
    | type | string |
    | value |  |
    | title | undef  |
    | type | string |
    | value |  |
{% endhint %}

```
example: {{ 1 | Numeral.Plularize('singular','plural','undefined')}}

output: singular
```
## Numeral.Sign
Returns strings based on the sign of the number : positive, negative,parity

{% hint style="info" %}
*params*
    | title | positive  |
    | type | string |
    | value |  |
    | title | negative  |
    | type | string |
    | value |  |
    | title | parity  |
    | type | string |
    | value |  |
{% endhint %}

```
example: {{ -1 | Numeral.Sign('positive','negative','parity')}}

output: negative
```
## Numeral.Subtract
Subtracts a number from another number

{% hint style="info" %}
*params*
    | title | Number to subtracts  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{2 | Numeral.Subtract(1)}}

output: 1
```


