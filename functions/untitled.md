---
description: Description of Number
---

# Number


## Numeral.NumberToLanguage
returns an number in the language specified as an argument

{% hint style="info" %}
*params*
    *language list en,it
{% endhint %}

```
input: {{ 1 | Numeral.NumberToLanguage('en')}}

output: one
```
## Numeral.OrdinalToLanguage
returns an ordinal number in the language specified as an argument

{% hint style="info" %}
*params*
    *language list en,it
{% endhint %}

```
input: {{ 1 | Numeral.OrdinalToLanguage('en')}}

output: first
```

