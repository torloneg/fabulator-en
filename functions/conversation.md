---
description: Description of Convert
---

# Conversation


## Conversation.Joining
returns a separation character based on the index content. If not the last element returns *separator* otherwise *last_separator*


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | array  | input value received
    | index | int  | index content in the for/loop
    | separator | string  | normal separator
    | last_separator | string  | last separator

```
example: {{["Jhon","Max","Robert"]|Conversation.Joining(loop.index,',',' and')}}

output: Jhon, Max and Robert

```
---
```

```


