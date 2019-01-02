---
description: Description of Number
---

# Number


## Numeral.NumberToLanguage
returns an number in the language specified as an argument


**params**
     | name | type  | description
     | :--- | :---  | :---        |
     |  | list  | 


```
example: {{ 1 | Numeral.NumberToLanguage('en')}}

output: one
```
## Numeral.OrdinalToLanguage
returns an ordinal number in the language specified as an argument


**params**
     | name | type  | description
     | :--- | :---  | :---        |
     |  | list  | 


```
example: {{ 1 | Numeral.OrdinalToLanguage('en')}}

output: first
```


