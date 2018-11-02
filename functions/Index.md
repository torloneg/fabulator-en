---
description: Description of Index function
---

# Index


## Index.Attr
return the attribute value


**params**
    |  |  |
    | :--- | :--- |
    | title | value  name of attribute of json object  |
    | type | string |
    | value |  |


```
example: {{  { name:'example', value:1} | Index.Attr('name') }} {{  { name:'example', value:1} | Index.Attr('value') }}

output: example
1

```
## Index.Attr
return the attribute value selected from a jsonpath path


**params**
    |  |  |
    | :--- | :--- |
    | title | path  |
    | type | string |
    | value |  |


```
example: 

output: 

```


