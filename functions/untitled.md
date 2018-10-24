---
description: Description of Number
---

# Number


## Numeral.NumberToLanguage
returns an number in the language specified as an argument

{% hint style="info" %}
*params*
    | title | language  |
    | type | list |
    | value | en,it |
{% endhint %}

```
example: {{ 1 | Numeral.NumberToLanguage('en')}}

output: one
```
## Numeral.OrdinalToLanguage
returns an ordinal number in the language specified as an argument

{% hint style="info" %}
*params*
    | title | language  |
    | type | list |
    | value | en,it |
{% endhint %}

```
example: {{ 1 | Numeral.OrdinalToLanguage('en')}}

output: first
```



