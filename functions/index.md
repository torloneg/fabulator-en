---
description: Description of Index function
---

# Index


## Index.Attr
return the attribute value


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | object  | input value received
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
    | input | object  | input value received
    | path | string  | string in jsonpath format

```
example: 

output: 

```


