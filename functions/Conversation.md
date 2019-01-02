---
description: Description of Convert
---

# Conversation


## Conversation.Joining
joining string with saparator


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | array  | 
    | index | int  | 
    | separator | string  | 
    | last_separator | string  | 

```
example: {{["Jhon","Max","Robert"]|Conversation.Joining(loop.index,',',' and')}}

output: Jhon, Max and Robert

```
---
```

```


