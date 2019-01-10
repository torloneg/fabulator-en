---
description: Description of Number
---

# Number


## Numeral.NumberToLanguage
returns an number in the language specified as an argument


**params**
     | name | type  | description
     | :--- | :---  | :---        |
     | input | string  | number to be transformed into natural language
     | language | list  | *en* for english or *it* for italian


```
example: {{ 1 | Numeral.NumberToLanguage('en')}}

output: one
```
## Numeral.OrdinalToLanguage
returns an ordinal number in the language specified as an argument


**params**
     | name | type  | description
     | :--- | :---  | :---        |
     | input | string  | number to be transformed into natural language
     | language | list  | *en* for english or *it* for italian


```
example: {{ 1 | Numeral.OrdinalToLanguage('en')}}

output: first
```


