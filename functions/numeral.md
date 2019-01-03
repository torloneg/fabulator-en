---
description: Description of Numeral
---

# Numeral


## Numeral.Add
Add a integer to a number


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | 
    | value | int  | 


```
example: {{1 | Numeral.Add(1)}}

output: 2
```
## Numeral.Divide
divide a number by another number


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | 
    | value | int  | 


```
example: {{10 | Numeral.Divide(5)}}

output: 2
```
## Numeral.Format
return a number with a new format


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | 
    | format | string  | 


```
example: {{10000 | Numeral.Format('0,0.0000')}}

output: 10,000.0000

```
## Numeral.Plularize
returns a string based on the value of the number &#x3D;&#x3D; 1 ( singular ), &gt;1 (plural), &#x3D;&#x3D;0 ( undefined)


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | 
    | singular | string  | 
    | plural | string  | 
    | undef | string  | 


```
example: {{ 1 | Numeral.Plularize('singular','plural','undefined')}}

output: singular
```
## Numeral.Sign
Returns strings based on the sign of the number : positive, negative,parity


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | 
    | positive | string  | 
    | negative | string  | 
    | parity | string  | 


```
example: {{ -1 | Numeral.Sign('positive','negative','parity')}}

output: negative
```
## Numeral.Subtract
Subtracts a number from another number


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | 
    | int | int  | 


```
example: {{2 | Numeral.Subtract(1)}}

output: 1
```


