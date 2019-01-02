---
description: Description of Index function
---

# Index


## Index.Attr
return the attribute value


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | object  | object
    | attribute | string  | value  name of attribute of json object

```
example: {{  { name:'example', value:1} | Index.Attr('name') }} {{  { name:'example', value:1} | Index.Attr('value') }}

output: example
1

```
## Index.Attr
return the attribute value selected from a jsonpath path


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | object  | 
    | path | string  | 

```
example: 

output: 

```


