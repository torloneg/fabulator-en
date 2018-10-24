---
description: Description of Number
---

# Number


## Numeral.NumberToLanguage
returns an number in the language specified as an argument


*params*
    | title | language  |
    | type | list |
    | value | en,it |


```
example: {{ 1 | Numeral.NumberToLanguage('en')}}

output: one
```
## Numeral.OrdinalToLanguage
returns an ordinal number in the language specified as an argument


*params*
    | title | language  |
    | type | list |
    | value | en,it |


```
example: {{ 1 | Numeral.OrdinalToLanguage('en')}}

output: first
```


